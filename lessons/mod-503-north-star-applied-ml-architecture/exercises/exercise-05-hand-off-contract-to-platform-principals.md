# exercise-05: Hand-Off Contract to Platform Principals and to Governance

**Estimated effort:** 2 hours

## Objective

Author the *inter-artifact seam contracts* the ML principal holds with two peer populations — peer platform-side principals (substrate and platform architecture) and peer executive branch (governance and policy). These are the contracts that turn the reference architecture from a self-contained document into a *networked* artifact (chapter 8 § *what this chapter does not do*).

The output populates `seams/platform-side.md` and `seams/governance.md` in the exercise-01 artifact with named seam contracts, co-authored interfaces, and communication rhythms.

## Prerequisites

- Exercise-01 complete — the artifact skeleton with `seams/platform-side.md` and `seams/governance.md` stubs.
- Exercises 02–04 complete — the four contracts, the evolution plan, and the review-body charter. Every seam citation points back to one of these.
- Chapter 8 read end-to-end. Chapter 6 §§2 and 4 (substrate and governance bets) provide the plug-in-side view; chapter 7 provides the ratification forum.
- Basic familiarity with the peer platform-side tracks: [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning), [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning), and the governance track [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning).

## Problem statement

Chapter 8 opens with the failure mode this exercise prevents: an architecture that *works on paper and fails in practice* because its seams are left implicit. "Good relationship with the platform team" is not a seam; *the specific SLO tier the training-cluster contract commits to* is a seam. Missing these seams is the single most common way a north-star architecture ossifies within two cycles.

Your job is to name the seams as *contracts* — named owners, named authorship rights, named change-management practice — for the two peer populations. This is not a diplomacy exercise; it is a specification exercise. The output is what the ML principal shows the peer principals to say *"here is how our two artifacts are wired together"*.

## Requirements

### `seams/platform-side.md` — required content

Chapter 8 §1 fixes the shape. Populate:

**Section 1 — Named peer principals.** Two named peer roles from `ai-infra-principal-engineer-learning` (Principal AI-Infrastructure Engineer) and `ai-infra-principal-architect-learning` (Principal AI-Infrastructure Architect). One paragraph on each — what they own; what artifact they publish; what current version of that artifact you cite; when their next major refresh is expected.

**Section 2 — The four substrate seams.** Chapter 8 § *the four substrate seams* (Seams A–D). Each seam gets a subsection covering:

- **Seam name and one-sentence purpose.** e.g. "Seam A — Training-cluster contract. The interface between the ML training plane (chapter 3 plane 3) and the platform substrate."
- **Peer artifact citation.** A specific document / URL on the peer principal's side, with a current version number. Placeholder text is fine (`Platform reference architecture v2.4 §4.2 — Training-cluster contract`), but the *shape* of the citation must be there.
- **What the seam contract carries.** The specific interface elements: submission APIs, SLO tier ceilings, artifact URI convention, failure-mode surface. Chapter 8 § *seam A* through *seam D* enumerate them.
- **Change-management rule.** Chapter 8 § *contract with the Principal AI-Infrastructure Engineer* — changes proposed at either review body; ratification requires both principals present; SLO envelopes ratified at semi-annual major review.
- **Impact on ML-side contracts.** Which of the four canonical APIs (exercise-02) cites this seam. Seam A is cited by the training-plane implementation but not by any of the four contracts directly. Seam B is cited by the inference-gateway contract. Seam C is cited by feature and registry contracts. Seam D is cited by every plane's observability slice.

**Section 3 — The co-authored interfaces.** Chapter 8 § *the co-authored interfaces*. For each of the four (canonical entity types, model URI convention, trace-context conventions, SLO tier taxonomy):

- **What it is.** One sentence.
- **Why it is co-authored.** Neither principal can define it unilaterally without breaking the other artifact.
- **Where the shared document lives.** A pointer to a shared canonical-types document above both artifacts. This aligns with exercise-02's `contracts/canonical-types.md` — cross-link the two.
- **Ratification cadence.** Semi-annual major review is the modal cadence; interim ratifications at either review body.

**Section 4 — Communication rhythm.** Chapter 8 § *communication rhythm with the platform-side principals*. Named rhythms:

- Standing 30-minute weekly with at least one platform-side principal. Rotating agenda is fine; the meeting existing on the calendar is what carries value.
- Cross-attendance at review bodies (chapter 7). The platform-side principals attend the ML architecture-review body; the ML principal attends the platform-side review bodies.
- Joint publication for the annual grand refresh — the two artifacts co-author the substrate-seams section.

**Section 5 — Common failure modes and correctives.** Chapter 8 § *common failure modes at the platform-side seam*. Four failure modes with their correctives:

- ML architecture re-owns the substrate → cite; do not own.
- Platform architecture re-owns the ML contracts → cite; do not own.
- Joint-ownership interfaces have two competing definitions → the shared canonical-types document is not optional.
- Seams are not versioned → chapter 5 version discipline extends to the seams.

**Section 6 — The specific hand-off contract with each peer.** Chapter 8 § *the specific hand-off contract with each peer*. Reproduce the two compact contracts (one with the AI-Infrastructure Engineer, one with the AI-Infrastructure Architect). Adapt language for your specific org's naming conventions if applicable; the *shape* of the contract must be there.

### `seams/governance.md` — required content

Chapter 8 §2 fixes the shape. Populate:

**Section 1 — Named governance peer(s).** From `head-of-ai-governance-learning` and, if applicable, an adjacent `chief-ai-officer-learning` role. One paragraph on each — what they own; what policy documents they publish; which specific policies apply to the ML function today (with citations).

**Section 2 — The three seam contracts.** Chapter 8 § *contract 1 / 2 / 3*.

- **Contract 1 — Policy-to-contract mapping.** A table with columns: policy citation → obligation summary → mapped contract → contract-level obligation shape → effective date → sign-off status. At least three rows populated with real citable policies:
  - [EU AI Act (Regulation 2024/1689)](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:L_202401689) — GPAI or high-risk-system obligations mapped to registry and/or eval-harness contract.
  - [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) — appropriate profile mapped to eval and registry.
  - [Mitchell et al. Model Cards](https://arxiv.org/abs/1810.03677) and [Gebru et al. Datasheets for Datasets](https://arxiv.org/abs/1803.09010) — documentation-artifact conventions mapped to registry and eval.
- Optional additional rows for org-specific or sectoral policies ([NYC Local Law 144](https://www.nyc.gov/site/dca/about/automated-employment-decision-tools.page), [CFPB fintech guidance](https://www.consumerfinance.gov/), sector-specific regs).
- **Contract 2 — Risk-tier definition and classification.** The taxonomy (`low / medium / high / GPAI / high-risk-system` or the org-specific equivalent). Explicitly *cite* the governance peer's taxonomy; do not author it here. Name the classification process: who declares a model's tier at registration; who ratifies if disputed; where the classification lives in the registry contract (chapter 4 registry `risk_tier` field).
- **Contract 3 — Documentation and audit-artifact conventions.** Cite Model Cards and Datasheets for Datasets as the field-canonical templates. Name the org-specific extensions and where they live. Cross-link to the registry contract's `model_card_uri` field and the eval-harness contract's report structure.

**Section 3 — Communication rhythm.** Chapter 8 § *communication rhythm with governance*.

- Standing 30-minute biweekly with the governance peer. Absence of the peer causes decisions to defer.
- Cross-attendance at review bodies — governance peer is a member of the ML review body on any governance-slice item.
- Joint publication at the annual grand refresh — the two peers co-author the governance-slice section.

**Section 4 — Common failure modes and correctives.** Chapter 8 § *common failure modes at the governance seam*. Four failure modes with their correctives:

- Policy without contract-level obligation → every policy has a row in the mapping table.
- Contract-level obligation without policy backing → co-authored, cross-ratified.
- Mapping table decays → semi-annual major review re-reads it.
- ML architecture writes its own policy → the ML principal enforces; the governance peer defines.

**Section 5 — Escalation to the executive branch.** Chapter 8 §3 § *when to escalate above both seams*. Named escalation triggers:

- Substrate re-platform with material cost implications.
- New capability class with cross-org budgetary / hiring implications.
- Regulatory obligation with cross-org compliance implications.
- Cross-substrate incident with architecture-level findings.

For each, name the intended recipient (CTO / SVP peer set / executive branch), the cross-org influence craft carrier (mod-504), and the citation format the artifact uses when the escalation completes.

### The six-question seam-discipline test — required at the bottom of each file

Chapter 8 § *testing your seam discipline* names six questions. Answer each in one or two sentences with pointers into your artifact. Any unanswered question is documented seam work still to do.

## Starter guidance

- **Draft policy-to-contract mapping first.** The mapping table is the concrete artifact governance peers most want to see. If you can produce one populated table with three real citable policies, everything else in `seams/governance.md` orbits around it. Chapter 8 § *contract 1 — policy-to-contract mapping* is the shape.
- **Cite, don't author.** Chapter 8 opens: the seams are contracts, not sentiments. For the platform-side seams, that means citing peer-artifact versions; for the governance seams, that means citing policy documents by their primary-source URLs. If your draft names an obligation without a citation, the seam is not yet a contract.
- **Shared canonical-types is a single document, not a duplicated one.** Chapter 8 § *canonical entity types* — the types live in a jointly-owned document above both artifacts. Cross-link your `seams/platform-side.md` § *co-authored interfaces* to your exercise-02 `contracts/canonical-types.md`. If those two files disagree, you have violated chapter 4's four-contracts-without-shared-types trap by another name.
- **The two artifacts publish in phase.** Chapter 8 § *joint publication for the annual grand refresh*. If your annual grand refresh date does not align with the peer platform-side principal's annual refresh, the seams will drift within a cycle. Name the alignment explicitly, and note the fallback if the peer's cadence moves.
- **Governance owns definition; you own enforcement.** Chapter 8 § *contract 2 — risk-tier definition and classification*. This is a durable boundary. If your draft has the ML principal defining "high-risk", the governance peer will (rightly) push back. Cite the taxonomy; do not author it.
- **Escalation is a routing decision, not a rejection.** Chapter 7 § *escalate* and chapter 8 § *when to escalate above both seams* are two sides of the same seam. The seam contract with the executive branch is what makes the escalation *productive* — mod-504 walks the craft, but the artifact-side citation format is what this exercise fixes.

## Acceptance criteria

Your artifact is done when it can pass all of the following:

- [ ] `seams/platform-side.md` contains all six sections listed in *Requirements*: named peers, four substrate seams, co-authored interfaces, communication rhythm, failure modes, specific hand-off contracts.
- [ ] Each of the four substrate seams (A / B / C / D) has a subsection with peer artifact citation, what the seam carries, change-management rule, and impact on ML-side contracts.
- [ ] Each of the four co-authored interfaces (entity types, model URI convention, trace-context conventions, SLO tier taxonomy) has a subsection cross-linking to exercise-02's `contracts/canonical-types.md`.
- [ ] `seams/governance.md` contains all five sections: named governance peer(s), three seam contracts, communication rhythm, failure modes, escalation to executive branch.
- [ ] The policy-to-contract mapping table has at least three rows, each citing a real policy (EU AI Act; NIST AI RMF; Model Cards / Datasheets are all fair game).
- [ ] The risk-tier taxonomy in `seams/governance.md` cites the governance peer's document, does not author the taxonomy from scratch.
- [ ] The six-question seam-discipline test from chapter 8 § *testing your seam discipline* is answered at the bottom of each file, with pointers into your artifact.
- [ ] Every failure-mode subsection has both the failure mode named and the specific corrective the seam contract enforces.
- [ ] The communication rhythms named (weekly platform-side; biweekly governance; cross-attendance; joint annual publication) are consistent with chapter 8's cadences.
- [ ] Nowhere in either file does the ML principal claim authorship of a policy or of a substrate contract. Nowhere does the peer claim authorship of an ML-side contract. Chapter 8 § *what this chapter does not do*.
- [ ] The escalation section names all four triggers (substrate re-platform / new capability class / regulatory obligation / cross-substrate incident) with a specific recipient and a mod-504 pointer.

## Stretch goals

- **Draft the annual grand refresh joint-publication outline.** Chapter 8 § *joint publication for the annual grand refresh* — the two artifacts co-author the substrate seams section. Sketch the outline of that co-authored section: shared canonical-types header, seam-by-seam status, in-flight version bumps, next-year plug-in points.
- **Populate one full row of the policy-to-contract mapping.** Pick EU AI Act GPAI obligations. Draft the row completely: the exact article citations from Regulation 2024/1689, the summarized obligation, which of your four contracts (registry, eval, gateway) enforces it, the specific field or invariant that carries the enforcement, the effective date, and the sign-off status placeholder. This is what a governance peer will read when they audit the artifact.
- **Draft a "seam-drift dashboard" spec.** A dashboard the ML principal and the peer principals could co-consult to see whether the seam contracts are drifting: version-mismatch counts (from chapter 5 § *contract-version stamping on every response*), open review-body items by seam, deferred items whose triggers have fired. This connects chapter 5, chapter 7, and chapter 8 in one operational instrument.
- **Draft the incident-response seam.** When a cross-substrate incident hits (chapter 8 § *when to escalate above both seams*), who chairs the joint post-incident review? What does the artifact-side update look like if the post-incident review names an architecture-level finding? Chapter 8 § *contract with the Principal AI-Infrastructure Engineer* names joint chairing; sketch what that looks like.
- **Draft a "when the peer artifact bumps a major" playbook.** If the peer platform-side reference architecture ships a major version bump next quarter, what does your artifact do? Semi-annual major review agenda item? Immediate interim refresh? Chapter 5 § *the two named emergency triggers* is the reference.

## Deliverable location

Local workspace / personal git repo, extending the exercise-01 artifact. The `seams/` subtree is what this exercise populates; the artifact-level `README.md` from exercise-01 should now link to `seams/platform-side.md` and `seams/governance.md`, and the exercise-03 evolution plan's governance rows should cross-reference the policy-to-contract mapping table populated here.
