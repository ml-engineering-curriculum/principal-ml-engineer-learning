# exercise-02: Canonical API Contract Surface

**Estimated effort:** 3 hours

## Objective

Author the *four canonical API contracts* — feature, model-registry, eval-harness, inference-gateway — that plug into the artifact skeleton built in exercise-01. Each contract must be *stable enough that product teams can build against it for years* and *versionable enough that the ML org can evolve it* (chapter 1's fifth defensibility test; chapter 4 § *the stability-vs-versioning tension*).

The output is the `contracts/` subtree of the artifact from exercise-01 — one directory per contract with the eight required elements chapter 4 fixes. It is not an OpenAPI file. An OpenAPI file (or protobuf, GraphQL schema, Thrift IDL) is *one of the eight elements*; the others are what turn a schema into a contract.

## Prerequisites

- Exercise-01 complete — the artifact skeleton with `contracts/{feature,registry,eval,gateway}/README.md` stubs.
- Chapter 4 read end-to-end; chapter 5 § *version discipline* skimmed.
- One case study you can quote from — at least one of the following at hand while you draft: Uber [*Meet Michelangelo*](https://www.uber.com/blog/michelangelo-machine-learning-platform/), LinkedIn [*Feathr*](https://engineering.linkedin.com/blog/2022/open-sourcing-feathr---linkedin-s-feature-store-for-productive-machine-), Airbnb [*Zipline*](https://medium.com/airbnb-engineering/zipline-airbnbs-machine-learning-data-management-platform-d0dc06e7a3c0), Netflix [Metaflow](https://netflixtechblog.com/tagged/metaflow), Meta [*Applied ML at Facebook*](https://engineering.fb.com/2018/05/09/core-infra/applied-machine-learning-at-facebook-a-datacenter-infrastructure-perspective/).
- A schema editor (OpenAPI, protobuf, GraphQL SDL — pick one and use it consistently across all four contracts).
- Google's [*Rules of Machine Learning*](https://developers.google.com/machine-learning/guides/rules-of-ml) open in a tab. Rules 15 (every launch cites an eval report), 29 (training / serving skew), and 32 (reuse the same feature extraction code) are the invariants you are converting into contract-level enforcement.

## Problem statement

The four contracts from chapter 4 sit at the top edge of the six-plane diagram — the seam between the ML function and its two consumers: product teams (upward) and the org's launch / governance / SRE bodies (sideways). Each of the four does a distinct job, but all four must share canonical types (entity types, URIs, timestamps, freshness tiers) so that a caller reading one contract's docs recognizes the shapes in the others.

Your job is to write the *contract-side* of each of the four — the eight required elements per contract, plus the canonical-types document all four cite. You are *not* implementing the substrate behind them; you are *specifying* what a substrate implementation would have to honor. The specification is the artifact.

Read chapter 4 § *what a canonical API contract has to do* for the eight required elements. Read chapter 4 § *failure modes to avoid* for the four patterns your drafts should not fall into (schema-only, tool-as-contract, contracts-without-shared-types, eval-bar-only-in-review).

## Requirements

Populate the `contracts/` subtree from exercise-01. Suggested layout inside each contract directory:

```
contracts/<name>/
├── README.md                # the contract text (the eight elements)
├── v1/                      # current major
│   ├── schema.<yaml|proto>  # request/response schema
│   └── examples/            # 2-3 request/response examples
├── CHANGELOG.md             # per-contract semver log
└── invariants-tests/        # optional; described below
```

Also add one file above `contracts/`:

```
contracts/canonical-types.md  # shared entity types, URIs, freshness tiers
```

### For each of the four contracts, the `README.md` must contain (chapter 4 § *what a canonical API contract has to do*)

1. **Purpose and audience** — one paragraph. Who calls it, from which side of the org, and what job the contract exists to do.
2. **Versioning discipline** — the semver-with-support-window rule for this contract. What guarantees hold within a major; what breaks at a major; how many majors are supported at once; the migration horizon (typically two quarters after a new major ships).
3. **Schema** — the request/response shapes at each endpoint. Link to `v1/schema.<yaml|proto>`; do not inline more than a small readable example. Include at least one worked example per endpoint under `v1/examples/`.
4. **Invariants** — what must be true regardless of caller. Feature: point-in-time correctness (Rule 29), same feature same value across offline/online, named freshness tier, owner metadata. Registry: provenance completeness, single source of truth, state-machine legality, non-optional governance metadata. Eval: every launch cites a signed report (Rule 15), named eval-set catalog, compare-against required, signed report. Gateway: alias resolution, registry-first routing, safety pre/post filters, trace correlation, governance-tier routing.
5. **SLOs** — availability, latency, freshness, throughput, cost budget (whichever apply, per tier). Name the tiers; the numeric envelopes are negotiated with the peer platform-side principal (chapter 8 seam) and go in the appendix.
6. **Failure modes** — what the caller sees on partial failure, on overload, on version mismatch. Enumerated as typed errors (`FEATURE_NOT_FOUND`, `FEATURE_STALE`, `LINEAGE_INCOMPLETE`, `INVALID_TRANSITION`, `POLICY_SIGNATURE_MISSING`, `CONTRACT_UNSUPPORTED`, etc.). Never leave failure implicit.
7. **Ownership** — who authors updates, who reviews, who signs off. Cite the review-body forum from chapter 7. Cite the specialist-track hand-off (`ai-infra-ml-platform-learning` for build, practitioner tracks for practice).
8. **Evolution rules** — what change is a patch, a minor, a major. This section is the input to exercise-03's evolution plan; it must be consistent with chapter 4 § *evolution rules* for each contract and with chapter 5 § *version discipline*.

### The `contracts/canonical-types.md` — required

The four contracts share a small set of types. Chapter 4 § *failure modes to avoid* names the "four-contracts-without-shared-types" trap. This file exists to prevent it. Include at minimum:

- **Entity types** — the canonical entity taxonomy (`user`, `item`, `session`, `transaction`, or the org-specific equivalents). Each entity type has a canonical ID format (`u_abc123`, `i_xyz789`) and a schema. Cited by the feature contract's `entity` field, by the gateway contract's `entity` field, and by any registry metadata that names entity scope.
- **URI conventions** — `registry://models/{name}/{version}`, `evals://harness/{report_id}`, `runs://mlflow/{run_id}`, `s3://.../` for artifact URIs. Cited by the registry contract's `artifact_uri`, `producing_run_uri`, `eval_report_uri`; by the gateway contract's `model_uri_served`; by the eval contract's `eval_report_uri`.
- **Timestamp discipline** — ISO 8601 UTC, always. Cited by every contract's `as_of` and `timestamp` fields.
- **Freshness tier taxonomy** — `real-time / near-real-time / batch / daily` for feature freshness; `online-low / online-standard / batch` for inference latency SLO. Cited by the feature contract's `freshness_tier` and by the gateway contract's `options.latency_slo_tier`.
- **Model alias convention** — the caller-facing shape (`ranking.session-ranker`, `search.query-embedder`) versus the substrate-facing URI (`registry://models/...`). Cited by the gateway contract for alias resolution.
- **Risk tier taxonomy pointer** — a pointer to the governance peer's tier definition (chapter 8 § *contract 2 — risk-tier definition and classification*). The ML side cites; it does not author.

### The `contracts/<name>/CHANGELOG.md` — required per contract

- One entry: `## v1.0 — <YYYY-MM-DD>` — the first release of the contract.
- Semver conventions at the bottom (patch / minor / major rules for this specific contract, quoted from your README's *Evolution rules* section).
- A "support window" note stating the ML org supports the current major and the previous major concurrently, with a documented migration horizon.

### The `invariants-tests/` directory — optional but strongly recommended

Chapter 4 § *the "schema-only" failure mode* is the reason for this. A contract's invariants are not real until they are tested. For at least one contract (the feature contract is the highest-leverage), sketch three test cases (as pseudocode or plain text) that a compliance harness would run against a substrate implementation to prove the invariants hold:

- **Feature contract, invariant test 1** — point-in-time correctness: given a labeled event at timestamp T, a training read at T must return the feature value as of T, not the latest value. Test rig: seed the substrate with two feature-value writes, one at T-1h and one at T+1h; assert the training read at T returns the T-1h value.
- **Feature contract, invariant test 2** — same-feature-same-value: for a given (feature name, entity key, timestamp), the online read and the training read at the same timestamp return the same value at the same feature version.
- **Feature contract, invariant test 3** — freshness SLO: given the feature is declared at `near-real-time` tier, the online read's `as_of` must be within the declared tier's window; else a typed `FEATURE_STALE` error is returned, never a null.

These sketches are what a platform-team build engineer implements against. They are not the whole test harness; they are the *specification* of what the harness has to prove.

## Starter guidance

- **Write the invariants before the schema.** The eight elements are ordered by author-side priority. Invariants are what the contract *promises*; the schema is one way of representing the promise. If you draft schema first you will find yourself defending your schema choice from an invariant that wasn't clear yet. Chapter 4 § *the "schema-only" failure mode* is the reference.
- **Keep the schema small.** The chapter-4 sketches for the four contracts are already at roughly the size a v1 contract should be. Additional endpoints belong in a later minor bump, not in v1. Over-scoping v1 is how contracts get stuck.
- **Reuse canonical types everywhere.** If your feature contract's `entity` field and your gateway contract's `entity` field are different shapes, you have failed chapter 4 § *the "four contracts but they don't share types" trap*. Draft `canonical-types.md` first; import from it in each schema.
- **Cite Rules of ML explicitly.** Rule 15 (every launch cites an eval report), Rule 29 (training / serving skew), Rule 32 (reuse feature extraction), Rule 44 (keep the first model simple). At least one of these citations should appear in three of your four contracts' *Invariants* sections. If none do, your invariants are underspecified.
- **Named failure modes, always.** Every error surface must be a *typed enum* value — never a silent null, never a 500-with-freeform-message. This is the discipline that makes the contract enforceable at the review body (chapter 7).
- **Pick one schema language and stay in it.** Do not draft the feature contract in OpenAPI and the registry contract in protobuf. The consumers of the four contracts overlap; consistent schema tooling is a load-bearing part of the ergonomics chapter 5 § *the tooling stack* discusses.
- **Version discipline lands in v1.** Every contract's `CHANGELOG.md` names its semver conventions from v1.0. Retro-fitting them at v2 is chapter 5 § *aspirational versioning* in action.

## Acceptance criteria

Your artifact is done when it can pass all of the following:

- [ ] `contracts/{feature,registry,eval,gateway}/README.md` each contains the eight required elements from chapter 4 § *what a canonical API contract has to do*, in the order given.
- [ ] Each contract's `v1/schema.<yaml|proto>` file exists and validates against the schema tool's linter.
- [ ] Each contract has at least one worked example under `v1/examples/`.
- [ ] `contracts/canonical-types.md` names entity types, URI conventions, timestamps, freshness tiers, and model alias convention; the four contract schemas import types from it (not from each other).
- [ ] Each contract's `CHANGELOG.md` has a `v1.0` entry and semver conventions.
- [ ] Every contract's `Invariants` section cites at least one specific mechanism (Rule 15, Rule 29, state-machine legality, alias resolution, etc.) from chapter 4 or from *Rules of ML*.
- [ ] Every contract's `Failure modes` section enumerates typed errors, not free-form messages.
- [ ] The `Evolution rules` section on each contract is consistent with chapter 4 § *evolution rules* for that specific contract (adding an optional field is minor; changing a required-field shape is major; etc.) and gives *at least one worked example* of each of patch / minor / major.
- [ ] The `SLOs` section names *tiers*, not numeric envelopes. (Numeric envelopes go in a substrate appendix and are negotiated with the platform peer.)
- [ ] Nowhere in the contract text does an implementation detail leak (specific storage engine, specific model server framework, specific autoscaler policy). Contract text is substrate-independent.
- [ ] At least one contract has three `invariants-tests/` sketches. The feature contract is the recommended target.
- [ ] Reading the four contracts side by side, the same entity type name and the same URI convention appear in all four (chapter 4 § *the "four contracts but they don't share types" trap*).

## Stretch goals

- **Publish an SDK stub for one contract.** Generate a client stub in one language (Python, Go, or TypeScript) from the schema, and write a two-line `README.md` for the SDK repo. This closes the loop between the contract artifact and product-team consumption (chapter 5 § *the tooling stack*, contract sources published to SDK repos on merge).
- **Add a "compare against the case study" section.** For each contract, cite the closest case-study analog and note where your contract borrows and where it diverges. Uber Michelangelo Palette for feature. Uber Michelangelo Model Store / Netflix Metaflow for registry. Meta's ranker eval literature or [Netflix's experimentation platform posts](https://netflixtechblog.com/tagged/experimentation) for eval. Meta / Uber serving posts for gateway.
- **Write the "consumer onboarding" doc for one contract.** For product teams building their first integration against the contract — a 200-word document that walks the six scenarios from chapter 4 § *test your contracts against product-team scenarios*.
- **Set up contract-lint CI.** A GitHub Action (or GitLab equivalent) that runs `spectral lint` (for OpenAPI) or `buf lint` (for protobuf) on every PR touching `contracts/`. This is chapter 5 § *the tooling stack* in enforcement.
- **Draft one worked `major bump` scenario for one contract.** Pick the gateway contract, invent a plausible major bump (e.g. `entity` field shape changes to accommodate multi-tenant callers), and write the migration plan — support window dates, deprecation announcements, product-team migration playbook. This exercise's output is the input to exercise-03.

## Deliverable location

Local workspace / personal git repo, extending the exercise-01 artifact. The `contracts/` subtree is what this exercise fills in; the artifact-level `README.md` from exercise-01 should now link into each of the four contract `README.md` files.
