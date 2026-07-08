# Hand-Off Contracts to Platform Principals and to Governance

> Chapter 8 of mod-503. Prerequisite: chapters 1–7. Downstream: this chapter closes the module. The next module (mod-504 cross-org influence without authority) walks the *practice* of holding these seams in the room, and mod-505 (technical bar) walks the review-bar side.

## Why seams, not silos

The reference architecture only stays alive if it is *held in place* by the peer principals whose systems it depends on and whose systems depend on it. Chapter 7's review body ratifies decisions inside the ML architecture's own scope; this chapter names the *inter-artifact seams* — the contracts the ML principal holds with two peer populations:

1. **Peer platform-side principals** — the substrate the ML architecture stands on. The contracts here run *downward* (the ML architecture cites platform contracts) and *sideways* (the ML architecture co-owns interfaces with the platform architecture).
2. **Peer executive branch (governance and policy)** — the policy the ML architecture converts into enforceable obligations. The contracts here run *upward* (the ML architecture receives policy) and *sideways* (the ML architecture negotiates the shape of the enforcement).

Two properties are shared across both classes.

- **The seams are contracts, not sentiments.** They have named owners, named authorship rights, named citation formats, and named change-management practices. "Good relationship with the platform team" is not a seam; the specific SLO tier the training-cluster contract commits to is a seam.
- **The seams are versioned like everything else.** Chapter 5's version discipline extends to the seams. When a substrate contract's version moves, the reference architecture cites the new version; when a governance policy's version moves, the reference architecture updates the mapping. Neither is a surprise event.

Missing these seams — leaving them implicit — is the single most common way a north-star architecture *works on paper and fails in practice*. Chapter 7 named the review-body as the enforcement forum; this chapter names *what is being enforced*.

## §1 — Peer platform-side principals

The two peer principals on the platform side are:

- **[`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) — Principal AI-Infrastructure Engineer.** Owns the substrate that the ML architecture stands on: compute (training cluster, inference cluster, batch cluster), storage (object store, feature-store storage layer, registry storage layer), networking, and the developer-experience contract for the substrate. Mod-505 of that track (long-term technical bets) is the closest structural parallel to mod-502 of this track; mod-503-equivalents there walk the platform reference architecture.
- **[`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) — Principal AI-Infrastructure Architect.** Owns the north-star platform architecture on the AI-infrastructure side — the cross-org substrate reference architecture and its canonical APIs (the platform-side analogue of what this module authors).

The two peer roles have different center-of-gravity:

- The AI-Infrastructure *Engineer* thinks in substrate-choice-and-operation. Their canonical output includes a substrate-reference architecture with SLO tiers, capacity envelopes, and operational discipline. The ML architecture cites their substrate contracts; the ML architecture's chapter 3 planes stand on those substrates.
- The AI-Infrastructure *Architect* thinks in cross-substrate interfaces. Their canonical output includes the org-scope AI infrastructure API surface. The ML architecture's chapter 4 contract set has a *co-author relationship* with theirs — often, the ML function's inference-gateway contract and the platform architect's serving-substrate contract share types (entity IDs, model URIs, latency tiers) that must be canonicalized above both artifacts.

### The four substrate seams

Naming them explicitly is what keeps the two artifacts coherent.

**Seam A — Training-cluster contract.** The interface between the ML training plane (chapter 3 plane 3) and the platform substrate. Owned by the platform-side principals; cited by this reference architecture. Contract carries: pipeline-template submission APIs, GPU / accelerator allocation SLO tier, artifact-output URI convention, distributed-training substrate identity (Ray / SLURM / hyperscaler-native), fault-recovery semantics. When it changes: minor bumps are absorbed by chapter 3 without artifact-visible change; major bumps route through the review body (chapter 7) with the peer platform-side principal present.

**Seam B — Inference-cluster substrate contract.** The interface between the ML serving plane (chapter 3 plane 6) and the platform substrate. Owned by platform side; cited here. Contract carries: model-server runtime interface, autoscaler contract, latency SLO tier ceilings (what the substrate can commit to per tier), cost-per-inference envelope, edge deployment topology. The ML function's gateway contract (chapter 4) sits *on top of* this substrate contract; the two are versioned independently but reviewed jointly.

**Seam C — Storage substrate contracts.** Three sub-seams: **object storage** (model artifacts, dataset snapshots — cited by registry contract), **feature-store storage** (offline warehouse + online store — cited by feature contract), **registry storage** (the registry's authoritative store, an audit log, a transactional DB — cited by registry contract). Owned by platform side; cited here. When the platform team re-platforms a storage sub-substrate, the ML architecture's contract-level SLOs are unaffected unless the change tightens or loosens the underlying envelope. Chapter 5 § substrate re-platform is the reference.

**Seam D — Observability substrate contract.** The interface between the observability slice (chapter 3 cross-cutting) and the corporate observability substrate. Owned by the corporate observability team (usually SRE-adjacent), cited here through the platform-side principal. Contract carries: metrics endpoint conventions, trace context propagation, log-ingestion pipeline, dashboards-as-code conventions. The ML architecture defines the ML-specific taxonomy on top of the substrate; the substrate is not this artifact's to own.

### The co-authored interfaces

Some interfaces are *jointly owned* between the ML principal and the AI-infrastructure architect, because neither artifact alone can dictate them.

**Canonical entity types.** *User ID*, *item ID*, *ad request ID*, and their peers — the types the feature contract, the inference-gateway contract, the substrate's tracing conventions, and the corporate data warehouse's canonical schemas all use. If either principal defines them alone, the other artifact has a competing definition. In practice these types live in a *shared canonical-types document* above both artifacts, ratified jointly, and cited by both.

**Model URI convention.** `registry://models/{name}/{version}` (or its peer). The registry contract on the ML side and the serving-substrate contract on the platform side both parse this URI. The convention is jointly owned; either side changing it unilaterally breaks the other.

**Trace-context conventions.** The ML architecture cares about ML-specific trace tags (model URI served, feature version, eval-report URI). The platform observability substrate cares about substrate-specific tags (cluster, region, pod). The *convention for tag propagation* — how ML tags survive substrate boundaries — is jointly owned.

**SLO tier taxonomy.** *Online-low / online-standard / batch* on the serving side; *real-time / near-real-time / batch / daily* on the feature side. These tiers are common vocabulary between the two artifacts; the tier definitions and the numeric envelopes are jointly ratified.

Jointly-owned interfaces have a shared review touchpoint — the semi-annual major review (chapter 5 §2) is the modal cadence, with interim reviews at the review body (chapter 7) as needed.

### Communication rhythm with the platform-side principals

The seam is not just documents; it is a working rhythm.

- **Standing 30-min weekly.** Chair (ML principal) plus at least one of the two platform-side principals. Any live seam question, cross-artifact ratification, or coordination call happens here. Rotating agenda is fine; the meeting existing on the calendar is what carries most of the value.
- **Cross-attendance at review bodies.** The platform-side principals attend the ML architecture-review body (chapter 7); the ML principal attends the platform-side review bodies. The reciprocity keeps the artifacts in phase.
- **Joint publication for the annual grand refresh.** The two artifacts co-author the annual major refresh section that covers the substrate seams. This is the shape mod-504 (cross-org influence) walks in practice.

### Common failure modes at the platform-side seam

- **The ML architecture re-owns the substrate.** The ML principal writes chapter-3 planes that name specific Kubernetes clusters, specific accelerator SKUs, specific autoscaler policies. This has descended into platform-side scope. Fix: cite; do not own.
- **The platform architecture re-owns the ML contracts.** The platform-side artifact names how the model registry works, what an eval-set family is, or what a canary rollout should look like at the ML function's level. This has ascended into ML-side scope. Fix: cite; do not own.
- **Joint-ownership interfaces have two competing definitions.** Entity types differ; model URI convention differs; SLO tier tiers do not agree. Fix: the jointly-owned document above both artifacts is not optional; make it, ratify it, and cite from both.
- **The seams are not versioned.** Substrate contract changes ship without the ML architecture noticing. Fix: chapter 5 version discipline extends to the seams; the peer principals cite each other's whole-artifact versions.

### The specific hand-off contract with each peer

Below is a compact form of the contract the ML principal holds with each peer. This is the shape a joint charter (a short document, ratified annually) takes.

**Contract with the Principal AI-Infrastructure Engineer.**

- The ML architecture *cites* the substrate reference-architecture version; it does not re-author it.
- The peer *cites* the ML architecture's four canonical APIs by version; they do not re-author them.
- Changes to Seams A, B, C, D are proposed at either review body; ratification requires both principals present.
- SLO tier envelopes are jointly ratified at the semi-annual major review.
- Incident response involving a seam is jointly chaired: the ML principal for the ML-facing action, the peer for the substrate-facing action.

**Contract with the Principal AI-Infrastructure Architect.**

- Canonical types (entity types, URI conventions, trace tags) live in a jointly-owned document above both artifacts.
- SLO tier taxonomy is jointly ratified.
- Changes to co-authored interfaces are proposed at either review body; ratification requires both principals present.
- The two artifacts publish their major-refresh cycles in phase; version-bumps that affect the co-authored interfaces are coordinated.

## §2 — Peer executive branch: governance and policy

The peer branch — [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) and, in some orgs, an adjacent [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning) role — owns policy authorship. This module owns policy *implementation* through contract obligations. Neither owns the other's work; both depend on each other.

The seam has three named contracts.

### Contract 1 — Policy-to-contract mapping

**Purpose.** For every governance obligation that lands on the ML function — internal risk-committee decision, regulatory activation (EU AI Act GPAI obligations, high-risk-system tier obligations), external audit requirement (ISO/IEC 42001), sector-regulator rules ([NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) profiles, [OMB memoranda](https://www.whitehouse.gov/omb/information-and-regulatory-affairs/) on federal AI use, [CFPB](https://www.consumerfinance.gov/) or [OCC](https://www.occ.gov/) fintech rules, [NYC Local Law 144](https://www.nyc.gov/site/dca/about/automated-employment-decision-tools.page)) — there is a *documented mapping* to the specific contract-level obligations the ML architecture enforces.

**Shape.** A table on the canonical location (chapter 5) with columns: policy citation → obligation summary → mapped contract → contract-level obligation shape → effective date → sign-off status. Every row's contract-level obligation shape is enforceable at contract time, not review time.

**Owner.** Co-authored. The governance-branch peer authors the policy; the ML principal authors the contract-level obligation. The mapping is ratified at the review body (chapter 7) with the governance rep present.

**Example row.** EU AI Act GPAI obligation → GPAI-tier models must publish training-data documentation and post-training safety evaluation → registry contract → required `gpai_compliance_uri` at `blessed`; required GPAI-safety eval-set family at eval-harness → 2027-Q1 → *pending sign-off from governance peer, ML review body*.

### Contract 2 — Risk-tier definition and classification

**Purpose.** The reference architecture's registry contract carries a `risk_tier` field, and its gateway contract routes accordingly. The *definition* of the tiers and the *classification* of a specific model into a tier are not the ML architecture's to author.

**Shape.** The governance-branch peer publishes the risk-tier taxonomy (e.g. *low / medium / high / GPAI / high-risk-system*), with definitions and examples. The ML architecture *cites* the taxonomy. Classification of a specific model into a tier is a joint decision (the governance peer's rules; the model owner's declaration; the ML principal's review-body ratification if disputed).

**Owner.** Governance-branch peer authors; ML principal cites and enforces.

**Failure modes.** ML architecture writing its own risk-tier taxonomy; governance branch trying to author the enforcement shape. Both are common; the cross-ratification review-body practice is the corrective.

### Contract 3 — Documentation and audit-artifact conventions

**Purpose.** The contract-level obligations often generate documentation artifacts — model cards, datasheets for datasets, risk registers, decision logs. The *shape* of these artifacts (what a model card includes; what a datasheet includes; how a decision is logged) is co-authored.

**Shape.** The governance branch cites the field-canonical documentation frames — [Model Cards for Model Reporting](https://arxiv.org/abs/1810.03677), [Datasheets for Datasets](https://arxiv.org/abs/1803.09010), the org-specific extensions — and publishes the org-specific templates. The ML architecture's registry contract carries the model-card URI reference; the ML architecture's eval-harness contract carries the eval-report shape; the ML architecture's review body's decision log carries the artifact-side decision record.

**Owner.** Co-authored. Field-canonical templates cited from primary sources; org-specific extensions ratified jointly.

### Communication rhythm with governance

- **Standing 30-min biweekly.** Chair (ML principal) plus governance peer. Any policy update, mapping decision, or classification dispute is handled here. When either peer is absent, decisions defer.
- **Cross-attendance at review bodies.** The governance peer is a member of the ML review body (chapter 7 § membership) on any governance-slice item; the ML principal attends the governance forums that ratify org-wide policy.
- **Joint publication at the annual grand refresh.** The two peers co-author the annual major refresh section that covers the governance slice and the policy-to-contract mapping table.

### Common failure modes at the governance seam

- **Policy without contract-level obligation.** The governance branch publishes a policy; the ML architecture never enforces it at contract level; the policy quietly does not apply. Fix: every policy has a row in the mapping table; if no contract can enforce it, the policy is not implementable, and the governance peer knows before the policy publishes.
- **Contract-level obligation without policy backing.** The ML architecture adds a required field that no policy asked for; the field cannot be adjudicated when a proposal argues to drop it. Fix: co-authored, cross-ratified.
- **The mapping table decays.** Regulatory horizons roll forward and nobody updates the effective dates. Fix: the mapping table is a first-class object; the semi-annual major review re-reads it.
- **The ML architecture writes its own policy.** The ML principal drafts what "high-risk" means and enforces it. The governance branch has not consented; a peer principal or an external auditor challenges. Fix: the ML principal enforces; the governance peer defines. This is a durable boundary.

## §3 — When to escalate above both seams

Some decisions rise above both peer seams and need to reach the CTO / SVP peer set or the executive branch. Chapter 7's *escalate* mode routes here.

**Substrate re-platform with material cost implications.** A training-substrate re-platform that changes the ML function's compute envelope by a material fraction is not a peer-principal decision; it is an executive-branch decision at least. Mod-504 walks the cross-org influence craft that carries the ask.

**A new capability class with cross-org budgetary or hiring implications.** A foundation-model program approval, an agentic-AI platform investment, a Gen-AI supplier consolidation — each of these is above the two peer seams and reaches the CTO / SVP peer set. The ML principal does not decide alone; they *propose* jointly with the mod-502 strategy owner (which may be themselves).

**A regulatory obligation with cross-org compliance implications.** EU AI Act obligations reach beyond the ML function — they touch product surfaces, contracts with customers, legal disclosures. Escalation to the executive branch is expected and required.

**A cross-substrate incident with architecture-level findings.** A post-incident review that names an architecture-level finding — e.g. a canary rollout led to a serving outage because the gateway contract's canary allocation contract was violated — often has to reach the CTO / SVP for cross-org action beyond either peer principal.

The mod-504 material owns the *craft* of these escalations. This chapter names the *seam*; mod-504 walks the room.

## §4 — What this chapter does not do

- It does not author the platform-side reference architecture. That belongs to [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning).
- It does not author policy. That belongs to [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) and the executive branch.
- It does not write substrate operational discipline. That belongs to [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) and the SRE / platform operations forum.
- It does not carry the cross-org influence craft that makes these seams work in practice. That is mod-504's material.

What this chapter does is name the seams as *contracts* the reference architecture depends on and cite them at their current versions. That naming is what turns the reference architecture from a self-contained document into a *networked* artifact — one that is honest about what it depends on and what depends on it.

## Testing your seam discipline

Six questions to sketch against your draft. If any answer is "unclear", the seam is not yet a contract; make it one.

1. Which platform-side principal owns the substrate that your training plane runs on? Which specific version of their reference architecture do you cite?
2. Where is the canonical entity-type document that both your feature contract and the platform's tracing conventions cite? Is it up to date?
3. If the governance branch activates a new obligation next quarter, on which page (or which row of which mapping table) does the mapping between policy and your contract-level obligation live?
4. If the platform team wants to change the training-cluster SLO tier envelope, at which review-body meeting is that ratified, and who votes?
5. If your registry contract needs a new required field for a governance obligation, is that added by the ML principal alone, or is the governance peer a co-signer?
6. When was the last time an incident review named an architecture-level finding, and did the finding update the artifact (via a review-body-ratified change) or drift into hallway lore?

Six clean answers means the seams are contracts. Any one unclear means work to do.

## Summary

- The reference architecture holds two classes of seams: peer platform-side principals (substrate and platform architecture) and peer executive branch (governance and policy). Neither is optional.
- Peer platform-side seams: four substrate contracts (training cluster, inference cluster, storage, observability) that the ML architecture cites; four co-authored interfaces (canonical entity types, model URI convention, trace-context conventions, SLO tier taxonomy) jointly owned. Standing weekly with peer principals; cross-attendance at review bodies; joint publication at the annual grand refresh.
- Peer executive-branch (governance) seams: three contracts (policy-to-contract mapping, risk-tier definition and classification, documentation and audit-artifact conventions) with the governance peer authoring policy and the ML principal authoring contract-level obligation. Standing biweekly with the governance peer; cross-attendance at review bodies; joint publication at annual grand refresh.
- Escalation above both seams reaches the CTO / SVP peer set. Mod-504 owns the cross-org influence craft; this chapter names the seam.
- Six-question test for seam discipline: substrate citation, canonical types, policy mapping, SLO ratification, co-signing on required fields, incident-to-artifact loop. Any unclear answer means work to do.
- The reference architecture is a *networked* artifact — honest about what it depends on and what depends on it. This chapter's contracts are what make the network real.
