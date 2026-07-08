# The Canonical API Contract Surface — Feature, Registry, Eval-Harness, Inference-Gateway

> Chapter 4 of mod-503. Prerequisite: chapter 3 (the six planes). Downstream: chapter 5 walks how these contracts are published under version discipline; chapter 6 walks what a version bump looks like; chapter 7 walks what the review body enforces at the contract boundary.

## Why exactly four contracts

The canonical API surface names the seams between the ML function and the two audiences that consume its output: product teams (upward) and the org's launch / governance / SRE bodies (sideways). Four contracts do most of the work at portfolio-and-industry altitude:

1. **Feature contract** — how the org reads features online and offline.
2. **Model-registry contract** — the source of truth for what is deployable.
3. **Eval-harness contract** — the pre-launch bar every launch traces to.
4. **Inference-gateway contract** — the sole ingress for calling models.

Every other API inside the six planes is either implementation detail (per-plane build teams' concern) or a private substrate seam with the peer platform-side principal (chapter 8). The canonical API surface is deliberately small: four contracts, each carrying substantial load. Adding a fifth contract at this altitude requires arguing that one of the four cannot absorb the responsibility. Removing one requires arguing that the org can absorb the responsibility somewhere else without fragmenting again.

Read this chapter next to the mod-502 chapter 2 five-row bet portfolio. Each contract is the *stable interface* that lets a bet in the strategy portfolio evolve without renegotiating the seam every planning cycle.

## What a canonical API contract has to do

A contract at this altitude is not an OpenAPI file. It is the *set of promises* the ML function makes to its consumers, of which the OpenAPI file (or protobuf schema, or GraphQL schema, or Thrift IDL) is one artifact. Each contract must state:

- **The purpose and audience** — one paragraph. Who is on which side, and what job the interface exists to do.
- **The versioning discipline** — semver-like or explicit-schema-version. What is guaranteed to be stable within a major; what can break at a major; how many majors are supported at once. Chapter 5 walks the publication cadence.
- **The schema** — request and response shapes at each endpoint. Canonical types (entity ids, timestamps, uris) shared across contracts.
- **The invariants** — what must be true regardless of the caller. For example, point-in-time correctness for the feature contract; lineage completeness for the registry contract.
- **The SLOs** — availability, latency, freshness, throughput, cost budget, whichever apply.
- **The failure modes** — what the caller sees on partial failure, on overload, on version mismatch. Never leave this implicit.
- **The ownership** — who authors updates, who reviews, who signs off.
- **The evolution rules** — what change is a patch, what is a minor, what is a major. Chapter 6 walks the version-bump triggers at portfolio scale.

If any of those eight is missing, the contract is not enforceable and the "convergence" property (chapter 1) is quietly aspirational.

## Contract 1 — Feature contract

### Purpose

The org-scope canonical way to read a feature — offline (for training) or online (for serving) — with point-in-time correctness enforced by the contract, not by team discipline. The single artifact that ends per-team feature fragmentation.

### Sketch

Two endpoints, one for training-time reads, one for serving-time reads. The training endpoint is a batch API; the serving endpoint is a request-response API. Both address features by canonical name plus canonical entity key.

```yaml
# Serving-time read
POST /v1/features/read
request:
  entity: { type: "user", id: "u_abc123" }
  features:
    - name: "user.session_count_7d"
    - name: "user.embedding_v3"
    - name: "user.risk_tier_1h"
  freshness_tier: "near-real-time"   # 'real-time' | 'near-real-time' | 'batch' | 'daily'
  timestamp: "2026-07-08T14:22:03Z"   # optional; server default is now
response:
  values:
    user.session_count_7d: { value: 42, as_of: "2026-07-08T14:20:05Z" }
    user.embedding_v3:     { value: [ ...384 floats... ], as_of: "2026-07-08T14:20:05Z" }
    user.risk_tier_1h:     { value: "medium", as_of: "2026-07-08T14:22:00Z" }
  contract_version: "1.4"
```

```yaml
# Training-time read (batch)
POST /v1/features/read_batch
request:
  entity_column: "user_id"
  entity_type: "user"
  as_of_column: "event_time"
  input_uri: "s3://.../labels/2026-07-01.parquet"
  features:
    - name: "user.session_count_7d"
    - name: "user.embedding_v3"
    - name: "user.risk_tier_1h"
  output_uri: "s3://.../training/2026-07-01.parquet"
response:
  status: "completed"
  rows: 1234567
  feature_versions:
    user.session_count_7d: "v3.2"
    user.embedding_v3:     "v3.0"
    user.risk_tier_1h:     "v1.7"
  contract_version: "1.4"
```

### Invariants

- **Point-in-time correctness** (Rule 29 of the *Rules of ML*). The training endpoint reads *the feature value that was available at the labeled timestamp*, not the latest value. The contract *guarantees* this; it is not the caller's responsibility to get right.
- **Same feature, same value.** For a given (feature name, entity key, timestamp), both endpoints resolve to the same value at the same feature version.
- **Named freshness tier.** Every online-served feature is stamped to one of the org-scope tiers (chapter 3 plane 2). Serving latency and freshness SLO tier are the contract's guarantees.
- **Ownership metadata.** Every feature has a named owner (team or shared platform team), a source dataset lineage, and a documented computation. Discoverable via `GET /v1/features/{name}`.

### SLOs

Latency, availability, and freshness are per-tier. The reference architecture names the *tiers*; specific numeric SLOs are set per feature and enforced by the platform team that owns the substrate. Chapter 8 walks the SLO-negotiation seam with the peer platform-side principal.

### Failure modes

- Feature not found → typed error `FEATURE_NOT_FOUND`; the caller does *not* silently receive a null.
- Feature stale beyond SLO → typed error `FEATURE_STALE` with `as_of` timestamp; the caller decides whether to proceed or reject.
- Version mismatch (client requested `v1.4` schema; server is on `v1.5`) → the server serves the client's version as long as it is within the support window; outside the window returns `CONTRACT_UNSUPPORTED`. Chapter 5 walks the support window.

### Evolution rules

Adding a new feature is a *no-op* against the contract (the contract is about the *shape of the read*, not the specific features). Adding a new freshness tier is a **minor** version bump. Changing the schema of `response.values.{feature}` is a **major** version bump. Chapter 6 walks the org-scope triggers.

### Hand-offs

Feature-store *build* to [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning). Feature-engineering *practice* to the practitioner tracks. The reference architecture cites both.

## Contract 2 — Model-registry contract

### Purpose

The single source of truth for what is deployable, what is blessed, and what has been retired. Every launch cites a registered model version by URI. Every rollback cites a previous registered version by URI. There is no "unregistered production model" as a legal state.

### Sketch

Registration is one endpoint; state transitions and reads are more.

```yaml
POST /v1/models/register
request:
  name: "ranking.session-ranker"
  version: "2026.07.03-a1b2c3"
  framework: "pytorch"
  artifact_uri: "s3://.../models/session-ranker/2026.07.03-a1b2c3/"
  producing_run_uri: "runs://mlflow/12345"
  feature_versions:
    - name: "user.session_count_7d"
      version: "v3.2"
    - name: "user.embedding_v3"
      version: "v3.0"
  dataset_versions:
    - name: "sessions.labeled"
      version: "2026.06.30"
  eval_report_uri: "evals://harness/98765"
  model_card_uri: "cards://catalog/session-ranker/2026.07.03"
  risk_tier: "low"
  owner:
    team: "ranking"
    on_call: "pd://schedule/ranking-oncall"
response:
  registry_uri: "registry://models/ranking.session-ranker/2026.07.03-a1b2c3"
  state: "registered"
  contract_version: "2.1"
```

```yaml
POST /v1/models/{registry_uri}/transition
request:
  to_state: "canary"   # 'registered' | 'eval-passed' | 'canary' | 'blessed' | 'deprecated' | 'retired'
  reason: "eval-report meets bar for canary"
  signed_by: [ "ranking-tl@org", "eval-harness-bot" ]
```

### Invariants

- **Provenance completeness.** A model cannot reach state `eval-passed` without an `eval_report_uri` that resolves. It cannot reach `blessed` without policy sign-off entries. It cannot reach `canary` or beyond with a broken `producing_run_uri` or a missing `feature_versions` list.
- **Single source of truth.** The registry is the *sole* source for the model URIs the inference-gateway resolves aliases against. No serving system reads from an S3 prefix directly.
- **State-machine legality.** A model in `retired` state cannot be routed traffic. Attempting to route to `retired` is a gateway error, not a policy discussion.
- **Governance metadata is not optional.** Model card and risk tier are required at `blessed`. High-risk-tier models require additional signatures (see Chapter 8's seam with governance).

### SLOs

Registry availability is a hard SLO — an outage blocks *both* new blessings and rollbacks. In practice this means the registry substrate is boring — a database + object store + an audit log. The reference architecture's SLO tier is *the same as the org's identity system's SLO tier*. Cite the peer platform contract, don't invent a new one.

### Failure modes

- Register with missing lineage → typed error `LINEAGE_INCOMPLETE`, no partial write.
- Transition to `blessed` without required signatures → typed error `POLICY_SIGNATURE_MISSING`, listing which are missing.
- Transition to a state not legal from the current state → typed error `INVALID_TRANSITION`.

### Evolution rules

Adding a required field to registration is a **major** bump — every producer breaks. Adding an optional field is a **minor**. Adding a new state to the lifecycle (e.g. `pre-blessing-review`) is a **major**. Removing a state is a **major**. Chapter 6 walks org-scope triggers.

### Hand-offs

Registry *build* to [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning). Policy authorship to [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning). Chapter 8 walks the governance seam.

## Contract 3 — Eval-harness contract

### Purpose

The pre-launch bar every launch traces to. A candidate model + a canonical dataset + a canonical eval-set produces a *signed eval report* whose URI is required by the registry to reach `eval-passed`.

### Sketch

```yaml
POST /v1/evals/submit
request:
  candidate:
    registry_uri: "registry://models/ranking.session-ranker/2026.07.03-a1b2c3"
  eval_sets:
    - name: "ranking.session-canonical"
      version: "2026-q2"
    - name: "safety.harm-canonical"
      version: "2026-q2"
    - name: "fairness.demographic-slices"
      version: "2026-q2"
  bar:
    name: "ranking.production-bar"
    version: "v4"
  compare_against:
    registry_uri: "registry://models/ranking.session-ranker/2026.06.20-x9y8z7"
response:
  eval_report_uri: "evals://harness/98765"
  status: "queued"
  contract_version: "1.3"
```

```yaml
GET /v1/evals/{eval_report_uri}
response:
  status: "complete"
  metrics_by_slice:
    ranking.session-canonical:
      ndcg_at_10:    0.712    # baseline: 0.703
      recall_at_100: 0.874    # baseline: 0.869
    safety.harm-canonical:
      harm_rate:     0.0018   # baseline: 0.0019
    fairness.demographic-slices:
      max_slice_regression: 0.008   # threshold: 0.010
  bar_result: "passed"
  regression_flags: []
  cost_report:
    training_gpu_hours: 214
    inference_p95_latency_ms: 47
    inference_cost_per_kilo_req_usd: 0.42
  signature: "..."
```

### Invariants

- **Every launch cites an eval-report URI.** Rule 15 of the *Rules of ML* is the reference. The gateway will not route traffic to a model without a passing eval report resolvable through the registry.
- **Named eval-set catalog.** Golden sets, safety sets, and fairness sets are *first-class named objects* with their own version discipline. A model cleared against `ranking.session-canonical v2026-q2` cannot claim clearance against `v2026-q3`.
- **Compare-against is required.** Every launch is a delta against a named baseline; regression is a first-class result, not a footnote.
- **Signed report.** The eval report is signed by the harness so a downstream reader (registry, launch review, incident-response) can verify the report is what the harness actually produced.

### SLOs

Eval-harness throughput and latency are their own SLO tier. The reference architecture names *tiers* (fast bar for canary, deep bar for blessed) and expects the substrate to meet them. Actual numbers are per-org.

### Failure modes

- Missing eval-set version → typed error, launch cannot proceed.
- Report failed to sign → typed error, treat as if no report exists.
- Regression flag triggered → the *response* explicitly names it; the registry cannot silently ignore it during a state transition.

### Evolution rules

Adding a new eval-set family is a **minor** bump. Changing the bar semantics (e.g. moving from single-metric threshold to composite score) is a **major**. Retiring an eval-set is a **major** — every consumer that referenced it must be updated. Chapter 6 walks the trigger discipline.

### Hand-offs

Eval-tooling depth to [`model-evaluation-engineer-learning`](https://github.com/ml-engineering-curriculum/model-evaluation-engineer-learning) / [`ai-eval-engineer-learning`](https://github.com/ml-engineering-curriculum/ai-eval-engineer-learning). Cross-team eval program to [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-405 / mod-406. Bar authorship co-owned with governance.

## Contract 4 — Inference-gateway contract

### Purpose

The single ingress product teams call to run inference against any model in the org. Routing, canary allocation, A/B group assignment, input validation, output filtering, rate limiting, and cost enforcement happen behind the gateway. Product teams do not directly call model servers.

### Sketch

```yaml
POST /v1/predict/{model_alias}
headers:
  X-Idempotency-Key: "..."
  X-Trace-Id: "..."
  X-Caller: "product-team/feed-service"
request:
  entity: { type: "user", id: "u_abc123" }
  features:
    # optional: for backfilled / offline requests; server otherwise resolves via feature contract
    user.session_count_7d: 42
    user.embedding_v3: [ ...384 floats... ]
  context:
    surface: "feed.home"
    ab_group: "auto"
    experiment_ids: [ "exp-2026-q2-ranker" ]
  options:
    latency_slo_tier: "online-low"   # 'online-low' | 'online-standard' | 'batch'
    safety_profile: "standard"       # 'strict' | 'standard' | 'permissive'
response:
  prediction:
    ranked_items: [ "i_xyz", "i_uvw", "i_lmn" ]
  model_uri_served: "registry://models/ranking.session-ranker/2026.07.03-a1b2c3"
  routing:
    canary_bucket: "control"
    ab_group_assigned: "treatment_v3"
  safety:
    filtered_items: 0
    action: "none"
  contract_version: "3.2"
```

### Invariants

- **Alias resolution.** `{model_alias}` is a canonical name resolvable to a specific `registry_uri` via the registry contract. The gateway *does not* accept a raw model URI at the top level; alias-first is what makes canaries and rollbacks org-safe.
- **Registry-first routing.** The gateway will not route to a model registry URI in state `retired` or below `blessed` unless the request is inside an explicitly-approved canary window.
- **Safety pre- and post-filters at the edge.** The gateway applies the safety profile at input validation and output filtering; per-team model servers do not carry the burden.
- **Trace correlation.** Every response carries `model_uri_served`; every request emits a trace record that ties (caller, alias, model URI served, canary bucket, latency) to a single trace ID.
- **Governance-tier routing.** High-risk-tier models (per registry metadata) require the caller to declare an appropriate `context.surface` and `safety_profile`; wrong pairings are rejected at the gateway.

### SLOs

Latency and availability per tier. `online-low` is the tightest tier and drives cost; `online-standard` is the modal tier; `batch` is queued. The tiers are the contract; the per-model numbers are negotiated at launch.

### Failure modes

- Alias not found → typed error, no fallback to a "similar" model.
- Model in `retired` state → typed error, not silent rerouting.
- Rate limit or cost cap exceeded → typed error with the specific reason (rate, cost).
- Safety profile mismatch → typed error at the gateway; product team fixes their call, not the model server.

### Evolution rules

Adding a new response field is **minor**. Changing the shape of `request.entity` is **major**. Adding a new latency SLO tier is **minor**. Removing a tier is **major**. Chapter 6 walks org-scope triggers.

### Hand-offs

Gateway *build* to [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning). Substrate to [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning). Latency depth per model to [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning). Safety-policy authoring to [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning).

## The stability-vs-versioning tension

The single hardest craft in this chapter is holding the two properties at once:

- **Stable enough for product teams to build against.** A product team that integrated against version 3.0 of the inference gateway six months ago should still work on 3.4 today. Team velocity and org convergence both depend on this.
- **Versionable enough that the ML org can evolve.** A frontier-capability shift (e.g. adding structured output for Gen-AI ingress), a governance shift (e.g. EU AI Act high-risk-system tier), or a new eval discipline (e.g. red-team eval sets) should be absorbable without asking every consumer to redo their integration.

The discipline that resolves the tension:

1. **Semver-with-support-window.** Each contract carries a major version. The ML org supports at least the current and the previous major *simultaneously*. Product teams have a documented migration horizon (typically two quarters after a new major ships) to move.
2. **Additive by default.** New capabilities land as optional fields, new endpoints, or new enums with a default. Removals or shape changes trigger a major.
3. **Deprecation with named end-of-life.** Deprecated fields carry a named removal date. The date is a commitment leadership can hold you to; sliding it silently is the failure the discipline exists to prevent.
4. **Advertised via the contract.** Every response carries `contract_version`; every SDK/client can log it. Support-window drift is visible in observability data, not discovered by breakage.
5. **Version-bump triggers are principal-scope decisions.** Chapter 6 walks the trigger table; the review-body (chapter 7) enforces it.

## Failure modes to avoid — patterns from the case-study literature

The four contracts share a set of failure modes documented across the case-study literature (Uber's Michelangelo posts; Airbnb's Bighead → Zipline transition; Netflix's Metaflow evolution; LinkedIn's Feathr open-sourcing). Watch for:

- **The "we have OpenAPI so we have a contract" trap.** A schema is a fifth of the contract. Invariants, SLOs, failure modes, ownership, and evolution rules matter more. A team that satisfies your OpenAPI file but violates your point-in-time correctness invariant has not honored the feature contract.
- **The "the tool is the contract" trap.** *"We use MLflow" is not a model-registry contract.* MLflow is a tool; the contract is what the org enforces around it (states, provenance completeness, sign-off). Same for Vertex AI, SageMaker, DataRobot, and their peers.
- **The "we have four contracts but they don't share types" trap.** If the entity id in the feature contract is not the same type as the entity id in the inference-gateway contract, you have four contracts pretending to be four contracts. Canonical types (entity types, URIs, timestamps, model aliases, freshness tiers) live above the contracts and are cited by each.
- **The "eval bar is enforced only in review" trap.** Rule 15 of the *Rules of ML* — every launch cites an eval report — is a contract-level enforcement, not a review-body suggestion. If the gateway will route a model without a resolvable, valid eval report, the bar is unenforced in the moment it matters most.

## Test your contracts against product-team scenarios

Sketch the following six scenarios against your contracts. If any one requires the product team to reason at implementation detail below the contract, the contract has a leak.

1. A new product-team engineer wants to add ranked search results to their surface. They only know their entity types and the alias of the target model. Can they read the features, call inference, and log a trace with only the four contracts? *(They should be able to.)*
2. The ML org wants to canary a new model version to 5% of feed traffic. Which contract carries the canary allocation? *(Registry + gateway.)*
3. The governance team declares a new high-risk-system tier requiring an additional input-safety check. Which contracts change? *(Registry gains a required field; gateway gains a routing rule. Feature and eval-harness are unaffected.)*
4. A Gen-AI capability launches with structured output. Which contract carries the new response shape? *(Inference-gateway, minor bump if additive.)*
5. A regression is caught post-launch. Which contract carries the rollback? *(Gateway routes to the previous registered version via alias; registry supplies the previous version.)*
6. A new product area is created and needs to bootstrap. Which contracts do they read first? *(All four; the reference architecture assumes each contract is discoverable from a known root URL. Chapter 5.)*

## Summary

- Four contracts do the load-bearing work at portfolio-and-industry altitude: feature, model-registry, eval-harness, inference-gateway.
- Each contract carries eight required elements: purpose, versioning discipline, schema, invariants, SLOs, failure modes, ownership, evolution rules. A schema alone is not a contract.
- The feature contract enforces point-in-time correctness and named freshness tiers. The registry contract enforces provenance completeness and a small state machine (registered → eval-passed → canary → blessed → deprecated → retired). The eval-harness contract enforces a signed, compared-against-baseline eval report as the gate. The inference-gateway contract enforces alias-first routing, safety filters at the edge, and observability of what was actually served.
- Hold the stability / versionability tension with semver-plus-support-window, additive-by-default evolution, named deprecation end-of-life, and contract-version stamping on every response.
- Watch for the four common failure modes: schema-only contract, tool-as-contract, four-contracts-without-shared-types, and eval-bar-only-in-review.
- Chapter 5 walks how these contracts are published, versioned, and kept living. Chapter 6 walks the org-scope version-bump triggers. Chapter 7 walks how the review body enforces them.
