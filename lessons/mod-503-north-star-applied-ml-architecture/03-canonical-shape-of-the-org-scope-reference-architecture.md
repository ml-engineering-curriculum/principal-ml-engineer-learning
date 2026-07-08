# The Canonical Shape of the Org-Scope Reference Architecture

> Chapter 3 of mod-503. Prerequisite: chapters 1 and 2. Downstream: chapter 4 makes the seams between the planes concrete as canonical API contracts; chapter 5 walks the discipline that keeps the diagrams *living*.

## Why fix a shape at all

Chapter 2 held that a reference architecture is a *choice*, not a menu. Nowhere does that discipline bite harder than the top-level decomposition. If the shape is not fixed, every product team draws its own, every platform partner argues with a different shape, and the "convergence" property from chapter 1 goes silently unenforced. The single most useful thing a principal does in the first draft is *pick a shape and defend it*.

The shape below is the modal shape across the applied-ML literature (Huyen; the *Rules of ML*; the Meta / Uber / Airbnb / Netflix / LinkedIn case studies). It is not the only defensible shape, but a draft that deviates has to pay for the deviation. Match it unless you can argue why a different shape lifts your specific org.

## The six planes

At portfolio-and-industry altitude, the org-scope reference architecture decomposes into six planes:

1. **Data plane** — sources, ingestion, canonical schemas, retention, and residency.
2. **Feature plane** — offline / online features, the feature contract, the point-in-time correctness discipline.
3. **Training plane** — pipelines, distributed-training substrate, experiment tracking, artifact lineage.
4. **Registry plane** — the model registry, the blessing / retirement lifecycle, and the source-of-truth for what is deployable.
5. **Evaluation plane** — the eval-harness contract, offline / online eval, canary and A/B infrastructure.
6. **Serving plane** — the inference gateway, online and batch inference, routing, safety, and observability.

Two cross-cutting concerns wrap the six:

- **Observability** — metrics, logs, traces, drift and quality monitors — is *not a plane*; it is a slice through every plane, owned jointly with the platform SRE counterparts.
- **Governance / responsible AI** — policy sign-off, model cards, risk register, high-risk classification — is *not a plane*; it is a slice through the registry, evaluation, and serving planes, owned jointly with the peer executive branch ([`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning)).

Two adjacent substrates are *cited* but not owned by this architecture:

- **Compute substrate** — the training cluster, the inference cluster, the batch cluster, the object storage, and their control plane. Owned by the peer platform-side principal ([`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning)).
- **Corporate substrate** — identity, secrets, network, cost accounting, and data-catalogue root — owned by the corporate engineering and security orgs. Cited only.

Chapter 4 walks the four canonical APIs (feature contract on the feature plane, registry contract on the registry plane, eval-harness contract on the evaluation plane, inference-gateway contract on the serving plane). Chapter 8 walks the seams with the two adjacent substrates.

## Plane 1 — Data

**Purpose.** The org-scope canonical dataset boundary. Where product event streams, business systems, and third-party data become *entities* the ML function reasons about (user, item, session, transaction, driver, listing, ad-request, ...).

**Load-bearing elements.**

- **Canonical entities and their keys.** Fixing "what is a user id? what is an item id?" at the org level is a principal-scope decision; ambiguity here shows up as feature-store bugs, model / product mismatch, and eval-set drift. In many orgs the ML principal shares this decision with the peer analytics / data-warehouse principal and the peer platform-side principal. Chapter 8 names the seam.
- **Event stream contracts.** The schema, ordering guarantees, and reprocessing semantics of the top-level event streams the ML function consumes. Not every event stream in the company; the ones the ML function's models depend on.
- **Retention and residency.** How long each canonical dataset lives, in which region, under which regulatory framework. Baseline compliance discipline; often driven by [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) or the peer legal function. Cited in the architecture, not decided in it.
- **Offline warehouse and online store correspondence.** The discipline that lets the same entity look the same across the offline warehouse and the online store — the pre-condition for the feature contract's point-in-time correctness (plane 2). Rules 29 and 32 of the *Rules of ML* live here.

**Common failure modes.**

- **Overreach.** The data plane in the ML architecture becomes a duplicate of the corporate data platform. If your architecture describes the whole data warehouse, you have descended into the peer platform-side architect's scope. Cite, don't re-draw.
- **Underreach.** The data plane is silent on the entity keys and the event-stream contracts, and product teams end up negotiating them in RFCs one at a time. This is the shape's job to fix.

**Hand-offs.** Ingestion and warehousing depth belong to the peer data-platform / data-engineering track. Feature engineering does *not* belong here; that is plane 2. Downstream, plane 2's feature contract *presupposes* that plane 1's canonical entity keys are stable.

## Plane 2 — Feature

**Purpose.** The org-scope feature substrate. The shape that turns "raw data + a definition" into a *feature value at a point in time* usable both by training (offline, at labeled points in time) and by serving (online, at request time).

**Load-bearing elements.**

- **The feature contract** (chapter 4). Canonical read APIs — batch read for training, online read for serving — the org-scope schema, the point-in-time correctness guarantee, the freshness SLO. Uber's *Michelangelo Palette* / *Feature Store*, LinkedIn's Feathr, and Airbnb's Zipline are the canonical case studies.
- **Feature definition ownership.** Who owns a feature — a product team, a shared ML team, a platform team? The reference architecture names ownership *classes* (team-owned, shared-owned, platform-owned) and the review discipline for each (chapter 7). It does not name specific features.
- **Point-in-time correctness.** The discipline that the training set's feature values match the values that were available at the training-time timestamp, not the latest values. This is the single most common bug in production ML pipelines; the reference architecture makes it a contract-level invariant.
- **Freshness SLO tier.** The org-scope tiers: *real-time* (seconds), *near-real-time* (minutes), *batch* (hours), *daily*. Each tier is a contract product teams can build against.

**Common failure modes.**

- **Feature-per-team fragmentation.** Every team defines and stores features their own way; the offline / online consistency is per-team. The reference architecture exists to end this failure mode; if your draft would leave it in place, it is not doing its job.
- **Contract without discipline.** The contract exists but does not enforce point-in-time correctness. Product teams silently accept training / serving skew. Rule 29 of *Rules of ML* is the reference; chapter 4 makes it a testable acceptance criterion.

**Hand-offs.** Feature-store *build* belongs to [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning). Feature-engineering *practice* belongs to the practitioner tracks ([`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning), [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning)). The architecture cites, does not duplicate.

## Plane 3 — Training

**Purpose.** The org-scope training substrate: how models get built, tracked, reproduced, and connected to their producing dataset and consuming registry entry.

**Load-bearing elements.**

- **Training pipeline templates.** The paved-road patterns product teams start from — small model, mid-tier fine-tune, large-scale distributed. Each is a template with named substrate under it (chapter 8: the training-cluster contract with the peer platform-side principal).
- **Experiment tracking.** Every training run traceable to its inputs (dataset version, feature version, code version, hyperparameters) and its outputs (model artifact, metrics, cost). This is the lineage that plane 4's registry requires to accept a model.
- **Distributed-training substrate.** The parallelism recipes (data parallel, tensor parallel, pipeline parallel, sharded data parallel / FSDP) and the substrate they run on. The recipe layer belongs to [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning); the substrate belongs to [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning). The reference architecture cites both.
- **Reproducibility.** A model in the registry must be reproducible from named inputs. Not "identical bit-for-bit" — reproducible in the applied-ML sense (same dataset version, same feature version, same code version, close-enough metrics).

**Common failure modes.**

- **Per-team training paths.** Every team has their own DAG framework, their own experiment tracker, and their own artifact convention. Bar for entry into plane 4 is different per team. The registry cannot enforce a bar because there is no bar.
- **Substrate leaking into the reference architecture.** The training plane starts naming specific Ray configurations, specific torchrun flags, specific storage layouts. That's blueprint. Lift.

**Hand-offs.** Recipe depth to [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning), [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning), [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning). Substrate to [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning).

## Plane 4 — Registry

**Purpose.** The single source of truth for what is deployable, what is blessed, and what has been retired. The registry contract is one of the four load-bearing APIs (chapter 4).

**Load-bearing elements.**

- **Model identity.** A registered model is *(name, version, framework, artifact-uri, producing-run-uri, feature-version, dataset-version, eval-report-uri, blessing-state, owner)*. Nothing less is enough for plane 5 (eval) or plane 6 (serving) to trust it.
- **The blessing lifecycle.** The states: *registered* → *eval-passed* → *canary* → *blessed* → *deprecated* → *retired*. Which state can be routed traffic; which state can be deleted. This is a small state machine; drawing it explicitly is a chapter 5 diagram.
- **Provenance and lineage.** The registry knows the training run that produced the model, the feature versions the training used, and the dataset version the feature versions read from. This is what makes a post-launch incident *diagnosable* rather than *forensic*.
- **Policy and governance metadata.** Model card, risk tier, sign-off signatures. Cross-cut with the governance slice. The [Model Cards](https://arxiv.org/abs/1810.03677) framing is the reference; [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) authors the specific policy.

**Common failure modes.**

- **Registry as a filesystem.** The registry is nothing more than an S3 prefix with model tarballs. No blessing state, no lineage, no policy. Serving reads whatever it points at. This is the common "we have an MLflow instance" anti-pattern; MLflow (or its peer tools) is the *tool*, not the *contract*.
- **Multiple registries.** Different teams register in different places. Now serving has to know which registry to trust for which model. The reference architecture ends this.

**Hand-offs.** Registry *build* belongs to [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning). Registry *policy* is co-owned with governance.

## Plane 5 — Evaluation

**Purpose.** The org-scope pre-launch bar: no model reaches production traffic without a pass through the eval harness the architecture names. Aligned with Rules 14–27 of *Rules of ML*.

**Load-bearing elements.**

- **The eval-harness contract** (chapter 4). Canonical eval-run APIs: submit a candidate model + a canonical dataset version + an eval-set version, receive a signed eval report. Every launch cites an eval-report-uri.
- **Offline-vs-online evaluation.** Offline: retrospective on labeled or logged data, cheap, fast, high-variance-to-online. Online: shadow / A-B / interleaving, expensive, slow, closest to ground truth. The architecture names *when each is required* and the pairing between them.
- **Canonical eval-set discipline.** Golden sets that survive multiple model generations; test sets rotated deliberately; safety and fairness slices that are not optional. The eval-set catalogue is a first-class object.
- **The bar for launch.** *"What does an eval report have to show for a launch to proceed?"* Not the specific numeric bar — that is per-product-area — but the *shape* of the bar (a required metric, a required safety slice, a required regression check, a required cost check). This shape is what makes eval a contract rather than a suggestion.

**Common failure modes.**

- **Per-team eval frameworks.** Ranking has one, ads has another, safety has a third. Nobody can compare results. Launching a model with cross-product-area impact requires four sign-offs from four eval systems. The architecture ends this.
- **Eval that only runs offline.** Post-launch surprises are frequent; the org has no shadow / canary discipline. Rule 30 of *Rules of ML* is the reference.

**Hand-offs.** Eval-tooling depth belongs to [`model-evaluation-engineer-learning`](https://github.com/ml-engineering-curriculum/model-evaluation-engineer-learning) and [`ai-eval-engineer-learning`](https://github.com/ml-engineering-curriculum/ai-eval-engineer-learning). Cross-team eval program depth belongs to [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-405 / mod-406.

## Plane 6 — Serving

**Purpose.** The org-scope inference substrate. Where models produce predictions in response to requests — online at request time, batch on a schedule, streaming on an event.

**Load-bearing elements.**

- **The inference-gateway contract** (chapter 4). One ingress product teams call: `POST /predict/{model_or_alias}` with a canonical request shape. Routing to the specific model, model version, canary allocation, and A / B group happens behind the gateway.
- **The three inference modes.** *Online* (single-request low-latency), *batch* (bulk offline scoring), *streaming* (per-event inference on a Kafka-like topic). Each mode has a latency SLO tier and a cost profile the architecture names.
- **Routing and canary.** Traffic splits, shadow deployments, A/B, model-mirror. The gateway makes these visible to the org rather than per-team.
- **Safety and cost enforcement at the edge.** Input validation, output filters (for generative models), rate limits, cost caps. This is the layer that turns "the model registry says this is blessed" into "product teams can call it safely without knowing the specifics".

**Common failure modes.**

- **Per-team inference stacks.** Every team runs their own serving service, their own autoscaler, their own routing logic. Cross-team traffic engineering is impossible. The gateway is the fix.
- **Serving contract without gateway.** The contract exists but product teams call the model server directly, bypassing routing. Now no rollout is safe. The gateway is not optional.

**Hand-offs.** Serving substrate and gateway *build* belong to [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning) and [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning). Model-specific latency depth belongs to [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning).

## The cross-cutting slice — observability

Every plane emits metrics, logs, and traces. The observability slice makes those legible together — a request that came in through the gateway, hit model version *m*, read feature version *f* against dataset version *d*, and returned prediction *p* is one traceable event. The reference architecture names the *taxonomy* of what is observed (input distributions, feature freshness, prediction distributions, latency, cost) and the *ownership* of each (data plane owner for freshness, feature plane owner for coverage, registry owner for provenance, serving owner for latency and traffic).

The tooling is shared with the peer platform-side principal — the substrate is a corporate observability stack (a Prometheus + Grafana + Elastic or equivalent), not an ML-specific tool. The reference architecture cites the substrate and names the ML-specific taxonomy on top of it.

## The cross-cutting slice — governance and responsible AI

Policy sign-off, high-risk-system classification (EU AI Act obligations), model cards ([Mitchell et al.](https://arxiv.org/abs/1810.03677)), datasheets for datasets ([Gebru et al.](https://arxiv.org/abs/1803.09010)), and the risk register cut across planes 4, 5, and 6. The reference architecture names *which plane each obligation attaches to*:

- Model card and risk tier live on the registry entry (plane 4).
- The eval report includes required policy-relevant slices (plane 5) — safety, fairness, robustness.
- Serving enforces routing constraints based on registered risk tier (plane 6) — high-risk systems require additional runtime safeguards.

The policy authoring itself is [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning)'s job. The architecture cites the policy documents at their known URLs and turns them into enforceable seams — not by re-writing them, but by wiring the sign-off into the registry and the eval harness. Chapter 8 walks the seam.

## Reading the shape as a diagram

Chapter 5 walks the discipline that makes a diagram *living*. For the current chapter, the useful mental picture is a horizontal band diagram:

```
+------------------------------------------------------------------+
|  Product teams                                                   |
|  (call the inference gateway, subscribe to feature freshness,    |
|   consume model-card and risk-tier metadata)                     |
+---|---------------------------|------------------|---------------+
    | inference-gateway API     | feature API      | registry API  (chapter 4)
    v                           v                  v
+------------------------------------------------------------------+
|  Serving plane   |  Evaluation plane   |  Registry plane          |
|                  |                                                |
|  Training plane  |  Feature plane      |  Data plane              |
|                                                                    |
|                     Observability slice (all planes)               |
|                     Governance slice (registry / eval / serving)    |
+---|-----------|-----------|-----------|-----------|----------------+
    | training-cluster API    | inference-cluster API    | object storage  (chapter 8 seams)
    v                         v                          v
+------------------------------------------------------------------+
|  Platform substrate (owned by ai-infra-principal-engineer)       |
+------------------------------------------------------------------+
```

That is not the diagram you ship — chapter 5 handles the shippable diagram — but it is the mental model behind it. The top edge is the ML org / product-team seam and the bottom edge is the ML org / platform seam. The four canonical APIs live at the top edge; the platform contracts live at the bottom edge. Everything else is the shape the org converges on.

## Testing the shape against your org

For calibration, sketch these five questions and see whether your draft answers them without descending into blueprint:

1. If a new product area launches next year and needs an ML feature, which contract does its team build against on day one? (Answer: the feature contract for reads, the inference-gateway contract for calls, the model-card metadata on the registry for governance sign-off — all named in the architecture.)
2. If a new bet lands — say, an agentic-AI capability — which plane changes shape? (Answer: usually plane 5 gains a new eval-set family and plane 6 gains a new inference mode. Plane 4 gains new metadata on the registry entry. The rest do not change shape. Chapter 6 walks the discipline.)
3. If the platform team re-platforms the training cluster, which plane changes? (Answer: plane 3 changes what it runs *on*; the training-plane *contract* does not change. The reference architecture is stable across the substrate re-platform.)
4. If a launch causes a post-launch incident, which planes carry the traceable evidence? (Answer: registry says what was blessed; eval says what report cleared it; feature plane says what freshness was expected; serving says what traffic saw. The observability slice ties them together.)
5. If regulation changes (EU AI Act high-risk-system tier obligations shift), which planes carry the new obligations? (Answer: registry entry gains a required field; eval report gains a required section; serving gains a routing rule. Chapter 8 walks the seam with governance.)

If your draft cannot answer these without descending into "which team, which quarter", it is still in blueprint. Lift.

## Summary

- The org-scope reference architecture decomposes into six planes: data, feature, training, registry, evaluation, serving. Two cross-cutting slices — observability, governance / responsible AI — thread through them.
- Two substrates are cited but not owned: compute substrate (peer platform-side principal) and corporate substrate (corporate engineering / security).
- Each plane has a fixed purpose, a small set of load-bearing elements, and a named hand-off to the practitioner tracks that own the recipe. The reference architecture names shape and ownership; it does not name model architecture, framework, or cluster topology.
- The four canonical APIs — feature contract, registry contract, eval-harness contract, inference-gateway contract — live at the top edge of the diagram, between the ML function and the product teams. Chapter 4 makes them concrete.
- The bottom edge — training-cluster, inference-cluster, storage — meets the peer platform-side principal's substrate. Chapter 8 walks the seams.
- Test the shape by asking what a new product area, a new bet, a substrate re-platform, an incident, and a regulatory shift each change. A defensible shape absorbs each of those with the plane-and-contract discipline still legible.
