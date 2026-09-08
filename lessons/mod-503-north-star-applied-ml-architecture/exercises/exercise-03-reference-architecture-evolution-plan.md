# exercise-03: Reference Architecture Evolution Plan

**Estimated effort:** 3 hours

## Objective

Author the *evolution plan* section of the north-star architecture — the fixed section of the artifact (chapter 6 § *the evolution plan section in the artifact*) that answers, for each bet the strategy commits to in the current cycle, *how the shape and the four contracts absorb it without a rewrite*. This is the artifact-side response to the mod-502 strategy portfolio.

The output populates `evolution-plan.md` from exercise-01's skeleton with real content and a version-bump trigger table calibrated for your chosen org.

## Prerequisites

- Exercise-01 complete — the artifact skeleton with `evolution-plan.md` stub carrying the five fixed sections.
- Exercise-02 complete — the four canonical contracts with their per-contract *evolution rules* sections. This exercise composes the per-contract rules into an org-scope plan.
- Chapter 6 read end-to-end. The four bet classes (capability / substrate / portfolio / governance) and the version-bump trigger table are the operational reference for the exercise.
- Mod-502 chapter 2 five-row bet portfolio at hand. If you completed the mod-502 exercise-01 one-pager, use its bets; otherwise sketch a plausible five-row portfolio for your chosen org (chapter 6 § *why an evolution plan matters* frames the pairing).

## Problem statement

A north-star architecture that cannot absorb a new bet without a rewrite is not a north-star architecture (chapter 1 § *five properties of a defensible north-star architecture*, property 3). The evolution plan is the artifact-side proof that the shape holds.

Your job is to write the evolution plan section for *your current cycle*. Every bet in your strategy portfolio must have a plug-in decision (§1–§4 of chapter 6): which plane(s) it lands on, which contract(s) bump and to what level, what consumer migration horizon it triggers, and what the review body (chapter 7 / exercise-04) will need to ratify.

The plan is *short*. Chapter 6 § *the evolution plan section in the artifact* names two pages typical, five pages outer bound. If your draft grows past that, you have descended into strategy-portfolio work; hand it back to mod-502.

## Requirements

Populate `evolution-plan.md` with the five fixed sections from chapter 6.

### Section 1 — Current-cycle bets, by class

For each bet in your strategy portfolio (three to five bets is typical):

- **Bet name** and one-sentence summary, quoting from your mod-502 one-pager.
- **Architectural class** — capability / substrate / portfolio / governance. Chapter 6 §§1–4 walk each class's modal plug-in point.
- **Plug-in point(s) on the six-plane shape** — which plane(s) reshape; which contracts change and by what version-bump level.
- **Consumer migration horizon** — if a contract major is triggered, when does the deprecated major reach EOL. Chapter 5 § *version discipline* is the reference (typical horizon: two quarters after the new major ships).
- **Cross-artifact citations** — which mod-502 strategy row this bet corresponds to; which chapter-8 seam contract (if any) this bet touches.
- **Review-body ratification status** — proposed / accepted / deferred / escalated (chapter 7 § *the four decision modes*).

At least one bet per class (capability / substrate / portfolio / governance) is ideal for the exercise. If your strategy portfolio doesn't cover all four classes, add a *hypothetical* row per uncovered class labeled "illustrative — not in current portfolio" so the plan documents your thinking for each.

### Section 2 — In-flight version bumps

For each contract major bump currently in flight (either from this cycle's plug-in decisions or from a prior cycle still within its support window):

- **Contract and version** — e.g. `registry contract v2 → v3`.
- **Trigger** — which bet or which governance obligation drove the bump.
- **EOL date for the previous major** — the commitment the ML org holds itself to.
- **Acceptance criteria for the new major** — what the review body will require to see before the new major reaches "supported".
- **Migration playbook link** — pointer to the consumer-facing playbook (draft form is fine at this stage).

If no bumps are in flight, name that state explicitly and move on. The absence of bumps is itself informative.

### Section 3 — Currently-supported majors, per contract

A small table with one row per contract (feature / registry / eval / gateway) plus the whole-artifact row:

| Contract | Current major | Prior supported major | Migration horizon |
| -------- | ------------- | --------------------- | ----------------- |
| Feature contract | v1 | (none — first cycle) | n/a |
| Registry contract | v2 | v1 (EOL 2026-Q4) | 2 quarters |
| Eval-harness contract | v1 | (none) | n/a |
| Inference-gateway contract | v3 | v2 (EOL 2027-Q1) | 2 quarters |
| Reference architecture (whole-artifact) | v3.2 | v3.1 (EOL 2026-Q4) | 1 quarter |

The table is what a product-team engineer scans to see what they can pin against. Chapter 5 § *version discipline* is the discipline this table enforces.

### Section 4 — Deferred items

Items the review body has explicitly deferred to a later cycle. For each:

- **Item summary.**
- **Reason for deferral** — usually one of: waiting on a peer principal (chapter 8), waiting on a strategy decision (mod-502), waiting on prior-major EOL, capacity-limited at the review body.
- **Trigger that would move it forward** — the specific event or date after which the item is expected back on the queue.

Deferred items are load-bearing. Chapter 7 § *the four decision modes* names defer as a first-class decision; leaving deferred items on the plan (rather than dropping them) is the discipline that stops "quiet abandonment" (chapter 7 § *body-avoids-conflict* failure mode).

### Section 5 — Out-of-scope items

Items the review body has explicitly declined and referred to a peer principal or the executive branch. For each:

- **Item summary.**
- **Where it was routed** — peer principal (name the track and role), executive branch, CTO / SVP peer set. Chapter 7 § *escalate* and chapter 8 § *when to escalate above both seams* are the references.
- **What the artifact does about it** — usually "cites the peer's decision; makes no shape change". Sometimes "waits for the peer's decision; then updates the seam citation".

### The version-bump trigger table — required as an appendix

Reproduce chapter 6 § *the version-bump trigger table* as an appendix to `evolution-plan.md`, calibrated to your specific contracts. Add or remove rows if your contracts differ from chapter 4's four (e.g. if you argued for a fifth contract in your artifact). The table is the operational reference the principal and the review body cite when classifying a change.

## Starter guidance

- **Read chapter 6 §§1–4 with your portfolio in hand.** Every bet in your portfolio maps to at least one of the four classes. If your instinct is "this bet is different", pause: it is usually a hybrid (a capability bet with a governance obligation attached; a substrate bet with a portfolio consolidation attached). Name the primary class and note the secondary.
- **Start with the version-bump trigger table.** Once the table is calibrated, filling in the per-bet rows becomes mechanical — each bet is a subset of rows in the table. If you find yourself hand-classifying each bet from first principles, the table is not yet doing its work.
- **Two pages, not five.** The plan is small on purpose. If yours grows past three pages, look for content that belongs elsewhere: strategy-level narration (mod-502), staff-scope blueprint detail (mod-401 / mod-402 in `staff-ml-engineer-learning`), review-body debate transcripts (chapter 7's log). Each of these has a home; the evolution plan is not it.
- **Every substrate bet should be contract-preserving.** Chapter 6 §2 is explicit: substrate re-platforms should not force ML-side contract changes. If your draft has a substrate bet that *does* force a contract change, sanity-check it against §2 — is the substrate change genuinely tightening/loosening an SLO envelope, or is the ML contract leaking implementation detail (chapter 4 failure mode)?
- **Portfolio bets defer to the staff scope.** Chapter 6 §3 is explicit: portfolio bets reshape *how a portfolio of product teams uses the substrate*, not the shape itself. The plan's job is to name the plug-in points and *defer everything else to the staff-scope multi-team blueprint*. Chapter 7 § *the "defer to the multi-team blueprint owner" case, walked* is the review-body-side counterpart.
- **Governance bets are co-authored.** Chapter 6 §4 and chapter 8 § *contract 1 — policy-to-contract mapping* are two sides of the same seam. For any governance bet in your plan, the row must name the governance peer (from `head-of-ai-governance-learning`) as a co-author, and the row must appear in the chapter-8 § *policy-to-contract mapping* table (exercise-05).
- **Draft one review-body item per bet.** Every plug-in decision is a review-body item. When you draft the plan, sketch (in the margin or a scratch file) what the review-body item would look like for each bet — proposer, artifact section, requested decision mode. This is direct input to exercise-04.

## Acceptance criteria

Your artifact is done when it can pass all of the following:

- [ ] `evolution-plan.md` contains all five fixed sections in the order chapter 6 § *the evolution plan section in the artifact* names.
- [ ] Every bet in your mod-502 strategy portfolio appears in section 1 with a class, plug-in point(s), and consumer migration horizon.
- [ ] Every architectural class (capability / substrate / portfolio / governance) appears at least once in section 1 (real bets or illustrative rows).
- [ ] Section 3 covers all four canonical contracts and the whole-artifact row.
- [ ] Section 4 (deferred) and section 5 (out-of-scope) each have at least one entry, with the trigger / routing named. If genuinely empty, state so and explain why.
- [ ] The version-bump trigger-table appendix is present, calibrated to your specific contract set.
- [ ] No bet in section 1 has "whole-artifact major" as its impact — with at most one exception explicitly argued for. Chapter 6 § *common failure modes for the evolution plan* § *every bet is a rewrite* is the reference.
- [ ] Every governance-class bet in section 1 names a co-author on the governance side.
- [ ] Every substrate-class bet in section 1 names a peer platform-side principal (from `ai-infra-principal-engineer-learning` or `ai-infra-principal-architect-learning`) as a co-author.
- [ ] The plan is two to three pages of body prose (excluding the trigger-table appendix). Chapter 6's outer bound is five pages.
- [ ] Every bet cross-references a mod-502 strategy row (real or exercise-fictional) by name.
- [ ] Nowhere in the plan does specific team-scale narration ("Q3 ranking team roadmap"), specific per-model architecture, or specific cluster topology appear. Chapter 6 § *the plan tracks strategy at the wrong altitude* is the reference.

## Stretch goals

- **Draft the "policy-to-contract mapping" preview.** For any governance bet in your plan, pre-draft the row that will land in `seams/governance.md` (exercise-05). One row per governance obligation, columns: policy citation → obligation summary → mapped contract → contract-level obligation shape → effective date → sign-off status.
- **Write the migration playbook for one contract major.** Pick the most consequential in-flight bump from section 2. Draft the two-quarter migration playbook for product-team consumers: announcement channel, deprecation warning cadence, cutoff dates, escalation path if migration blocks a product-team launch.
- **Add a "risk register" section.** For each bet, name the top one or two ways it could fail and what the artifact would look like if the failure happened. This is the closest analog to an SRE-style pre-mortem at architecture altitude and is often what the review body finds most useful.
- **Walk the plan against the chapter-6 three-question test.** For each of chapter 6 § *test your evolution plan against three questions*, write a two-sentence answer specific to your plan. If any answer is unclear, revisit the plan (or its upstream chapter 3 / chapter 4 dependencies) before considering the exercise done.
- **Draft a "declined and deferred" hygiene routine.** Chapter 6 § *common failure modes for the evolution plan* § *deprecation dates slide silently* and chapter 7 § *the review body should be doing outside the sessions* both point to a working hygiene. Sketch it: what the chair does with deferred items between sessions, how a stale deferred item gets bumped.

## Deliverable location

Local workspace / personal git repo, extending the exercise-01 artifact. The fleshed-out `evolution-plan.md` should now be pointed at from the artifact-level `README.md` (exercise-01) and from the four contracts' *Evolution rules* sections (exercise-02).
