# The Evolution Plan and Version-Bump Triggers

> Chapter 6 of mod-503. Prerequisite: chapters 1–5. Downstream: chapter 7 walks the review body that ratifies the plug-in decisions this chapter frames; chapter 8 walks the seams that carry the evolution across substrate boundaries.

## Why an evolution plan matters

An architecture that cannot absorb a new bet without a rewrite is not a north-star architecture. It is a snapshot that will be replaced next planning cycle, and product teams will treat it accordingly. Chapter 1's *evolution discipline* property is what turns "the shape the org converges on" from an aspiration into a working contract.

The evolution plan is the artifact — inside the reference architecture — that answers three questions:

1. Where does a new bet **plug in** to the six-plane shape and the four canonical APIs, without shape-level surgery?
2. Which changes are **contract patches or minor bumps** that ship at the next quarterly refresh, and which trigger a **contract major** or a **whole-artifact major**?
3. Which changes are **outside the reference architecture's scope** entirely and hand off to the peer platform-side principal, the peer platform architect, or the executive branch (chapter 8)?

An evolution plan is not itself a strategy document; the mod-502 strategy portfolio is. It is the *architecture-side response* to the strategy: for each bet, where in the shape it lands and how the shape absorbs it. Publishing the response *before* the bet lands is what lets the org's teams commit to the bet without renegotiating the shape.

## The four bet classes at portfolio altitude

The mod-502 chapter 2 five-row bet portfolio names the modelling-side bets. This chapter's plug-in framing groups them into four *architectural classes*, because the plug-in point is often shared across strategically-different bets:

- **Capability bets** — Gen-AI direction, foundation-model program, agentic-AI direction, safety-model program. New capability *classes* that need new registry metadata, new eval-set families, new inference modes.
- **Substrate bets** — training-cluster re-platform, inference-cluster re-platform, feature-store re-platform, registry re-platform. Almost always driven with the peer platform-side principal; the reference architecture holds *contract shape* stable across a substrate re-platform.
- **Portfolio bets** — RecSys re-platform, safety-system re-platform, personalization consolidation. Product-area-wide bets that reshape *how* multiple product teams use the same substrate.
- **Governance bets** — new high-risk-system tier per EU AI Act, a new sign-off requirement per an internal risk-committee decision, a new documentation obligation per ISO/IEC 42001. Almost always driven with [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning); the reference architecture converts the policy into an enforceable contract-level obligation.

Each class has a modal plug-in point, described in §§1–4 below. The evolution plan lists the current-cycle bets by class and their specific plug-in decisions.

## §1 — Capability bets: plug into the registry, eval-harness, and inference gateway

A new capability class typically leaves the data, feature, and training planes' *shapes* intact and reshapes the top three planes: registry, evaluation, and serving.

**Registry impact.** A new capability class often introduces a new *risk tier* and *model card sub-schema*. Example: Gen-AI models introduce a text-input model card sub-schema (prompt space, tool-use surface, output safety). Agentic-AI models introduce an *action space* declaration. These land as additive fields on the registry contract — **minor bump** — unless a required-at-blessed field is added, which is a **major bump**.

**Eval-harness impact.** A new capability class virtually always introduces new eval-set families. Example: agentic-AI capability requires a *task-completion* eval-set family, a *tool-use safety* eval-set family, and often a *cost / step-count* budget eval. Adding new eval-set families is a **minor bump** on the eval-harness contract; changing the shape of the bar (moving from single-metric to composite) is a **major bump**.

**Inference-gateway impact.** New capability classes sometimes introduce new *inference modes* (streaming for token-by-token outputs; multi-turn session state for agentic capabilities) or new *safety profile* variants. Adding a new mode with a default is **minor**; changing the request shape is **major**.

**What does not need to change.** The feature and data planes' shapes generally do not change for a capability bet. The training plane's contract shape generally does not change — a new training-pipeline template lands on the *substrate* (owned by the peer platform-side principal, chapter 8), but the contract that a product team relies on stays stable.

### Worked micro-example — Gen-AI capability class

Suppose the mod-502 strategy commits to Gen-AI-integration for two consumer product areas (chapter 2 row 1 of the strategy). The architecture-side response:

- **Registry.** Add optional `gen_ai_profile` object to model registration (supplier, model family, context window, tool-use surface). Add `prompt_governance_uri` field for prompt-template lineage. Both additive → registry contract **minor bump** (say `v2.1 → v2.2`).
- **Eval-harness.** Add eval-set families: `gen_ai.harm-canonical`, `gen_ai.jailbreak-canonical`, `gen_ai.factuality-canonical`, `gen_ai.tool-use-safety`. All additive → eval-harness contract **minor bump**.
- **Serving-gateway.** Add `latency_slo_tier: "streaming"` and `response.stream` shape as an alternative response format. Additive → gateway contract **minor bump**.
- **Whole-artifact bump.** No single major bump implied → whole-artifact **minor** at the next quarterly refresh.

None of the six planes changes shape. No product-team migration horizon is triggered. The evolution plan documents the plug-in decisions above and links them to the strategy row.

## §2 — Substrate bets: hold contract shape stable, change substrate

The peer platform-side principal ([`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) mod-505 long-term technical bets) drives most substrate bets — a training-cluster re-platform, an inference-substrate consolidation, a feature-store storage substrate swap.

The architecture-side response is *usually contract-preserving*: the training plane's substrate changes from Ray to a hyperscaler-native offering, or from one Kubernetes flavor to another; the training pipeline template contract (part of the substrate seam chapter 8) changes shape only if the SLO tier changes or the failure mode surface changes. The reference architecture's *contract* to product teams should not.

**When a substrate bet does trigger a contract change:**

- If the substrate's SLO envelope tightens or loosens materially, the affected contract's SLO tier definitions update. Feature contract freshness SLO tier retitration is a **minor bump**; adding a new tier is a **minor bump**; removing a tier is a **major bump**.
- If the substrate change eliminates a category of failure mode, the contract's failure-mode enumeration can be tightened. A **minor bump** (fewer typed errors possible) is usually correct.
- If the substrate change changes the observability model (e.g. trace propagation shape), a **minor bump** with a compatibility window is usually correct.

**When a substrate bet is out of scope for this artifact:**

If the peer platform-side principal's substrate change does not touch the four canonical APIs' shape or SLO tiers, it is *out of scope for this reference architecture*. The peer principal's artifact documents the change; the ML-side reference architecture cites the peer artifact's new version but does not itself bump.

Chapter 8 walks the seam-negotiation practice.

## §3 — Portfolio bets: rewrite a portfolio, not a plane

Portfolio bets — a RecSys re-platform, a safety-system re-platform, a consolidation of previously-federated ranking stacks — reshape *how a portfolio of product teams uses the substrate*, not *the substrate itself*. This is the class most likely to blur with staff-scope work.

The reference architecture's response is to name what happens on each plane at *shape level* and to defer everything else to the staff-scope multi-team blueprint owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-401 / mod-402.

Example: a RecSys re-platform that consolidates feed, search, and notifications ranking into a shared retrieval-and-ranking substrate.

- **Data plane.** No shape change. Same canonical entities (user, item, session, ad-request).
- **Feature plane.** Feature contract shape does not change. New features land under the standard contract with the standard onboarding process.
- **Training plane.** No contract change. The staff blueprint may adopt a shared training-pipeline template, but that is inside the substrate seam.
- **Registry plane.** Model names in the registry get more coherent (`ranking.session-ranker` replaces per-team names). Contract does not change.
- **Evaluation plane.** Golden set catalog gets a new *consolidated* ranking family, potentially retiring per-team families over a support window. **Minor bump** to add the family, **major bump** to retire families with active consumers.
- **Serving plane.** Alias set consolidates (`ranking.feed`, `ranking.search`, `ranking.notifications` under a shared model or shared substrate). Contract shape does not change.

The whole-artifact response is *usually* a minor bump documenting the plug-in points and citing the staff blueprint. It is *not* the reference architecture's job to design the RecSys re-platform; it is its job to *hold the shape stable* while the re-platform happens beneath it.

## §4 — Governance bets: convert policy into contract obligations

A governance bet is a new obligation from [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) or from a regulator that lands on the ML function. Examples: EU AI Act GPAI obligations activate for a model family; NIST AI RMF profile updates require a new risk-slice family in evaluation; an internal risk-committee decision requires an additional sign-off on high-risk-tier models.

The architecture-side response converts *policy prose into contract-level obligations*.

- **Registry plane.** Add a required field or a required signature for a specific risk tier (e.g. GPAI-tier models require `gpai_compliance_uri`). **Major bump** on the registry contract if it becomes required; **minor bump** if optional first, then major on flip.
- **Evaluation plane.** Add a required eval-set family for the applicable risk tier. **Minor bump** on eval-harness contract; the *bar* semantics may shift, which is a major.
- **Serving plane.** Add a routing rule (e.g. GPAI-tier models must route through additional edge-safety checks). **Minor bump** on gateway contract; changing request shape is major.
- **Whole-artifact bump.** Governance bets that change required-at-blessed obligations are typically a **whole-artifact minor** on next quarterly refresh; a bar-semantics change is a whole-artifact major.

The evolution plan documents the policy-to-contract mapping explicitly. The review body (chapter 7) is where the mapping gets ratified with the governance branch — the principal does not author governance policy, and the governance branch does not author contract shape. The two authors negotiate.

## The version-bump trigger table

Consolidated view of what triggers what. Use this as the operational reference the principal maintains on the canonical location (chapter 5).

| Change class                                                    | Contract impact                | Whole-artifact impact | Consumer migration horizon | Owner       |
| --------------------------------------------------------------- | ------------------------------ | --------------------- | -------------------------- | ----------- |
| Adding an optional field on a contract                          | Patch or minor                 | Patch                 | None                       | Principal   |
| Adding a new endpoint on a contract                             | Minor                          | Minor                 | None                       | Principal   |
| Adding a new eval-set family                                    | Eval-harness minor             | Minor                 | None                       | Principal   |
| Adding a new SLO tier                                           | Affected contract minor        | Minor                 | None                       | Principal + platform peer |
| Adding a new inference mode                                     | Gateway minor                  | Minor                 | None                       | Principal   |
| Adding a required-at-blessed registry field                     | Registry major                 | Minor                 | 2 quarters                 | Principal + governance |
| Retiring an SLO tier                                            | Affected contract major        | Minor                 | 2 quarters                 | Principal + platform peer |
| Retiring an eval-set family with active consumers               | Eval-harness major             | Minor                 | 2 quarters                 | Principal + eval program |
| Changing the shape of a request object                          | Affected contract major        | Minor                 | 2 quarters                 | Principal   |
| Changing the bar semantics on eval-harness                      | Eval-harness major             | Major                 | 2 quarters                 | Principal + eval program + governance |
| Changing the six-plane decomposition                            | Every contract may shift       | Major                 | 3+ quarters                | Principal, chaired at review body |
| Adding a fifth canonical API                                    | New contract at major v1       | Major                 | New contract from day one  | Principal, chaired at review body |
| Substrate re-platform without contract change                   | None                           | Patch                 | None                       | Platform peer + citation |
| Governance policy → contract obligation                         | Affected contract minor→major  | Minor→Major           | 1–2 quarters               | Principal + governance |
| Bet-portfolio change (mod-502)                                  | Determined by bet class above  | Minor at least        | Per row above              | Principal   |
| Post-incident finding at architecture level                     | Affected contract minor→major  | Minor                 | Named in incident report    | Principal   |

The table is a reference, not a substitute for the review body's judgement. The review body is where a change is classified — chapter 7. What the table gives you is the *default classification*; unusual cases are the review body's job.

## The evolution plan section in the artifact

On the canonical location (chapter 5), the evolution plan is a *fixed section* of the artifact. It has a small, stable shape:

1. **Current-cycle bets, by class.** For each bet the mod-502 strategy commits to in the current cycle, the class (capability / substrate / portfolio / governance), the plug-in point(s) on the six-plane shape, and the expected contract impact per §§1–4 above. One row per bet.
2. **In-flight version bumps.** Which contract majors are in flight, with their EOL dates for the deprecated majors and the acceptance criteria for the new majors.
3. **Currently-supported majors, per contract.** The N-and-N-1 support-window state for each of the four contracts and whole-artifact.
4. **Deferred items.** Things the review body has explicitly deferred to a later cycle, with the trigger that would move them forward.
5. **Out-of-scope items.** Things the review body has explicitly declined and referred to a peer principal or the executive branch. Chapter 7 owns the "declined and deferred" hygiene.

The section is *short*. Two pages is typical; five pages is the outer bound before it becomes its own document. If it grows past that, the reference architecture has drifted into strategy-portfolio work and needs to hand back to mod-502.

## Common failure modes for the evolution plan

- **Every bet is a rewrite.** Every new bet triggers a whole-artifact major. Usually a symptom of the six-plane shape being wrong, or of the contracts leaking implementation detail (chapter 4). Fix: revisit chapter 3's shape and chapter 4's contract discipline before adding another bet.
- **No bet is a bump.** Everything is a "no change" answer. Usually a symptom of the contracts being under-specified (invariants and SLOs not enforced) so changes look free. Fix: enforce chapter 4's eight required elements; a real contract's real invariants get renegotiated when new capabilities land.
- **The plan tracks strategy at the wrong altitude.** The evolution plan becomes a copy of the strategy roadmap. Fix: the evolution plan tracks *shape and contract impact*; the strategy portfolio tracks *bets*. Cite the strategy row, don't duplicate the strategy row.
- **Deprecation dates slide silently.** The migration horizon is never enforced. Fix: chapter 7's review body is the enforcement point; chapter 5's contract-version stamping in observability data makes the slide visible.
- **Substrate bets get lifted into shape work.** A peer platform-side principal's substrate re-platform ends up being narrated as a whole-artifact change even though no contract shape moves. Fix: cite the peer artifact, do not re-narrate it.

## Test your evolution plan against three questions

1. Can a new bet land in the mod-502 strategy portfolio without the reference architecture needing more than a minor bump? If the answer is *"probably yes for most classes"*, the shape is doing its job.
2. Can a product team pin against `reference architecture v3.2` today and still be building against it two quarters after v3.3 ships? If yes, the support window is real.
3. When a governance obligation lands from a regulator, is there a named location on the canonical page (chapter 5) where the policy-to-contract mapping is written? If yes, the seam with governance is honest.

If any of the three answers is *no*, the fix is upstream of this chapter — usually in chapter 3 (shape) or chapter 4 (contract discipline). This chapter cannot save a shape that has not committed to convergence in the first place.

## Summary

- The evolution plan is a *fixed section* of the reference architecture that names how a new bet from mod-502 plugs into the shape, without a rewrite.
- Bets fall into four classes: capability (registry / eval / gateway plug-in), substrate (contract-preserving unless SLO tier moves), portfolio (shape stable, staff-scope blueprint reshaped), governance (policy converted to enforceable contract obligations).
- Use the version-bump trigger table as the default classification. The review body (chapter 7) is where unusual cases get classified.
- The evolution plan section is small — bets by class, in-flight bumps, current support windows, deferred and out-of-scope items. Two pages typical.
- Watch the five failure modes: rewrite-per-bet, no-bump-ever, evolution-plan-as-strategy-clone, silent-deprecation-slide, substrate-lifted-into-shape-work.
- The plan's tests are three: new bets absorb at minor; product teams' pinning survives a version cycle; governance obligations have a named mapping location. If any fail, fix upstream.
