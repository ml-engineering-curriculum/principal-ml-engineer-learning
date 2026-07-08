# Running the Org-Wide Architecture-Review Body

> Chapter 7 of mod-503. Prerequisite: chapters 1–6. Downstream: chapter 8 walks the seams the review body maintains with the peer platform-side principals and with governance.

## Why a review body

A north-star architecture that publishes on a cadence (chapter 5) and holds an evolution plan (chapter 6) still needs a *forum* where changes get proposed, debated, ratified, and rejected in the open. Absent the forum, one of two things happens:

1. **Silent divergence.** Teams ship changes that de-facto violate the shape or the contracts; the artifact drifts into "aspirational" over multiple quarters.
2. **Bottleneck-on-principal.** Every change routes to the principal individually; the principal becomes the choke point on the org's ability to ship; leverage collapses.

The org-wide architecture-review body is the corrective. It is a *standing forum* the principal chairs, on a regular cadence, with a bounded membership drawn from the ML org, the platform-side principals, product-team leadership, and the governance branch. It is where the reference architecture is *enforced as a working contract*, not a proposal.

This chapter fixes the body's charter, membership, cadence, and — most importantly — the four decision modes the principal exercises inside it: **block**, **nudge**, **escalate**, **defer**. Deferring to the staff-scope multi-team blueprint owner (mod-501 chapter 6 hand-off) is a specific and load-bearing case of "defer" that this chapter walks explicitly.

## The body's charter

The charter is a short, published document on the canonical location (chapter 5). Suggested shape:

> **Charter — Org-Wide Applied-ML Architecture Review.** The review body is the standing forum where changes touching the org-scope reference architecture — the six-plane shape, the four canonical APIs, the evolution plan — are debated, ratified, and recorded. It meets biweekly; its outputs are (i) decisions logged on the canonical location, (ii) version-bumps proposed for the next quarterly refresh, (iii) items escalated to the peer platform-side principals, the executive branch, or the CTO/SVP peer set. The body does not own multi-team blueprint reviews, which are chaired by staff-scope blueprint owners and cited here on request. Membership and cadence are named below and refreshed annually.

Four properties are load-bearing.

- **Standing** — not ad-hoc. The body meets on a cadence whether or not there are items on the queue; empty sessions are fine and useful. Ad-hoc review bodies do not carry weight.
- **Chaired by the principal** — the principal owns the queue, sets the agenda, and holds the decision authority described below. The chair role is the level-48 "adjudicated" work.
- **Bounded** — a body of forty people is not a review body. Membership is bounded and named (§ below).
- **Bounded scope** — the body owns the *reference architecture* and its seams. Multi-team blueprint reviews are elsewhere; team-level design reviews are elsewhere. Chapter 2's altitude discipline is the reference.

## Membership

A working review body has five representative populations. Individuals may cover more than one seat.

- **Chair.** The principal ML engineer authoring the reference architecture. Sets agenda, chairs, holds the four decision modes.
- **ML-org representatives.** Two or three staff engineers or staff-plus tech leads whose blueprints most frequently intersect the reference architecture (typically the ranking blueprint owner, the Gen-AI blueprint owner, the shared-substrate blueprint owner). They carry the "will this actually work in the blueprint" answer.
- **Platform-side principals.** The peer principal from [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) (substrate engineer) and the peer principal from [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) (platform architect) as *voting* members on any decision that touches the substrate seams (chapter 8). The seats are load-bearing; when they are absent, substrate-affecting decisions defer.
- **Product-team representatives.** One or two senior engineers from the product-team side, rotating on a quarter-by-quarter cadence. They carry the "will this work for us as consumers" answer and the "we cannot migrate on that horizon" answer.
- **Governance representative.** A representative from [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) or the responsible-AI function, as a voting member on any decision touching the governance slice (chapter 3) or a governance-bet class change (chapter 6 §4).

Two guests-rotating slots is often useful — SRE reps whose systems care about the observability slice; peer principals from adjacent research or applied-science tracks whose work will land in the shape at the next refresh.

The chair's job is to keep the membership *at the right altitude*. The body is not a director's staff meeting; it is not a design-review board; it is not an architecture guild. It is a peer forum among people who own real seams with the artifact.

## Cadence

- **Biweekly regular session.** 60–90 minutes. Two to five items on the queue.
- **Quarterly refresh review.** The session that immediately precedes chapter 5's quarterly refresh publication. Longer (120 minutes typical); the agenda is the refresh's changelog.
- **Semi-annual major review.** Aligned with the mod-502 strategy refresh cadence. Typically half a day. The agenda is the reference architecture's semi-annual major review from chapter 5.
- **Annual grand refresh session.** Aligned with the fiscal year. Full day. The agenda is the shape itself (six-plane decomposition, four-contract set) plus year-ahead planning.

The purpose of publishing the cadence is that a proposer knows *when their item will be heard* and can plan accordingly. Cadence variability is the first symptom of a review body slipping.

## The four decision modes

At every session, on every item, the chair exercises one of exactly four decision modes. Naming them explicitly is what makes the body honest and its outputs enforceable.

### Mode 1 — Block

**When.** A proposal violates the reference architecture — the six-plane shape, one of the four contracts' invariants, the evolution-plan discipline, or a governance obligation. The proposal is not "worse than an alternative"; it is *inconsistent* with the artifact.

**How.** The chair blocks explicitly. The block is logged with the specific chapter and clause of the artifact the proposal violates (e.g. *"blocked: violates feature-contract invariant on point-in-time correctness — chapter 4 § feature invariants"*). The block is not personal; it is contract-level.

**What the proposer does next.** They may (a) revise and re-propose, (b) propose a change to the artifact itself (which becomes a different item on the queue, likely escalated to the semi-annual review), (c) accept the block and drop the proposal.

**When *not* to block.** The chair does *not* block on preference — "I would have done it differently". Blocks are for artifact-inconsistent proposals. Chapter-2 altitude discipline applies: blocking on preference is a symptom of the principal doing staff-scope work by other means.

**Examples of legitimate blocks.**

- A serving proposal that bypasses the inference-gateway contract and calls a model server directly. Contract-violating.
- A registry change that would allow production traffic to a `registered` (not-yet-`blessed`) model without a canary declaration. Invariant-violating.
- An eval change that would remove the require-signed-report step at launch. Rule 15 of the *Rules of ML*; contract-violating.
- A feature-store proposal that eliminates point-in-time correctness in exchange for lower latency. Invariant-violating.

### Mode 2 — Nudge

**When.** The proposal is consistent with the artifact but is *below the bar of what the review body would like to see*. Not violating; just weak in ways the artifact's practices could improve.

**How.** The chair returns the proposal with specific, named feedback: *"nudge: acceptable, but consider adopting the shared eval-set family instead of authoring a per-team one — chapter 4 § eval-harness family catalogue"*. The proposal is not blocked; the proposer decides whether to take the nudge or ship as proposed with the nudge on record.

**What the proposer does next.** They incorporate the feedback, or they ship as-is with the nudge visible. The visibility is the point — if the nudge was well-placed and the team ships without it, the *pattern* becomes visible in the recent-decisions log and can inform the next quarterly refresh.

**When *not* to nudge.** The chair does not nudge on style. A proposal in a coherent shape gets one round of nudges; endlessly-iterating nudges are a symptom of a chair who cannot decide.

**Examples of legitimate nudges.**

- A registry model card that is minimal-but-legal; nudge to enrich it toward the field's Model Card standard ([Mitchell et al.](https://arxiv.org/abs/1810.03677)).
- A feature-store definition that meets the contract but does not use the shared entity-key taxonomy; nudge to align.
- An eval-set proposal that is well-scoped but does not cite a canonical baseline; nudge to include one.
- A canary rollout plan that meets the gateway contract but does not use the recommended shadow-first pattern; nudge to add a shadow lane.

### Mode 3 — Escalate

**When.** The proposal is at *higher altitude* than this body owns, or requires a decision from a peer principal, the executive branch, or the CTO/SVP peer set. Escalation is not a rejection; it is a *routing* decision.

**How.** The chair escalates to the specific peer authority with the specific decision the peer needs to make. Common destinations:

- **Peer platform-side principals.** A change that requires substrate-side commitment (an SLO tier retitration, a substrate re-platform decision, a new inference-cluster capability) escalates to the peer principals at [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) and [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning). Chapter 8 walks the seam.
- **Executive branch (policy / governance).** A change that touches a policy the peer executive branch owns — high-risk-system tier definition, regulatory-obligation activation, external audit obligation — escalates to [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) or the responsible-AI function.
- **CTO / SVP peer set.** A change that affects strategic direction — a new capability class landing that has budgetary or cross-org implications; a substrate re-platform that changes the overall ML function's cost envelope — escalates to the CTO or SVP peer set. Mod-504 walks the cross-org influence craft that makes this escalation productive rather than adversarial.
- **Executive branch (product).** A change that would materially reshape what product teams can consume — a deprecation with a horizon shorter than product-team migration bandwidth allows, a new mandatory routing profile — escalates to product-side VP/SVP for consent.

**What the proposer does next.** Wait for the peer decision, then return to the body with the peer decision on record.

**When *not* to escalate.** The chair does not escalate to avoid making a decision that is within the body's charter. Escalation is for out-of-scope items, not for deferrals-of-conflict. Chapter 6's version-bump trigger table is the reference for what's in-scope.

### Mode 4 — Defer

**When.** The proposal is in scope but is *owned by another forum* — most commonly, the staff-scope multi-team blueprint. The principal defers to that forum rather than re-doing its review.

**How.** The chair defers *by name*: *"deferred to the ranking blueprint review, owned by [staff engineer name]. Charter of that review covers this decision."* The deferral is logged; the artifact-side impact (if any) is scheduled for a later session after the deferred forum reports.

**What the proposer does next.** Take the item to the named forum. Return only if the deferred forum's decision needs artifact-side ratification.

**When *not* to defer.** The chair does *not* defer as a way of avoiding a decision the body owns. Defers are for genuinely-elsewhere-owned decisions, not for artifact-scope items the chair finds inconvenient.

## The "defer to the multi-team blueprint owner" case, walked

This is the most under-practiced case in the four modes, and the one where new principals most often fail. Every one of the mod-501 chapter 6 hand-off contracts to `staff-ml-engineer-learning` is a form of "defer at this altitude":

- A proposal that reshapes the ranking blueprint's internal design — how retrieval and reranking compose, what candidate generators are used, what caches sit where — is *not* the reference architecture's job to review. It is the staff-scope blueprint owner's job (`staff-ml-engineer-learning` mod-401 / mod-402). The principal *defers*.
- The principal's contribution to that review is *the contract*: the ranking blueprint has to honor the feature contract, the inference-gateway contract, the eval-harness contract, and the registry contract. The blueprint owner owns everything *inside* those contracts. The principal owns the contracts themselves.
- The tell that the principal has descended into staff scope: the review body is debating specific model architectures, specific caches, specific team roadmaps. Chapter 2's downward-altitude-slip failure mode is exactly this in disguise.

The counter-tell that the principal has ascended into staff-avoidance: the review body has no visibility on the multi-team blueprints at all. There should be a light-touch reporting rhythm — the staff blueprint owners bring monthly summaries to the review body, with any contract-impacting decisions flagged for the body's ratification. Chapter 8 walks the seam.

## Session shape and agenda

A working session has a fixed shape.

1. **Agenda posted 48 hours before.** Each item names the proposer, the summary, the specific artifact section it touches, and the requested decision mode (block / nudge / escalate / defer / ratify). Absence of a mode-request is fine; the chair picks. Absence of the artifact section it touches is a sign the item is not ready.
2. **Round of updates.** Each represented population reports on anything from their side the body should know (5 minutes total). Not blockers; context.
3. **Items.** 10–15 minutes each. The proposer presents the shape (not the reasoning) in three minutes; the body debates; the chair calls the decision mode; the decision is logged. Repeat.
4. **Closing summary.** The chair summarises the decisions and confirms the follow-ups.

**What is *not* on the agenda.** Team-specific status updates. Individual model launches without an artifact-touching angle. Blueprint reviews that a staff-scope blueprint owner is already chairing. Retros unrelated to artifact changes.

A body that fills its sessions with "not on the agenda" items is not doing review-body work. Chair discipline is what protects the body's altitude.

## Written outputs — the recent-decisions log

Every session produces one atomic output: the recent-decisions log entry on the canonical location. Structure:

```
## Review body — 2026-06-24

Chair: [principal]
Members present: [list]
Members absent: [list, with reason]

### Item 1 — Registry major bump proposal for GPAI compliance URI
Proposer: [staff engineer / governance rep]
Summary: Add required field gpai_compliance_uri to registry blessing.
Artifact section: chapter 4 § registry invariants; chapter 6 § governance bets.
Decision: Ratified as **major bump on registry contract v2 → v3**, EOL for v2 = 2027-Q1. Whole-artifact minor bump at next refresh.
Follow-ups: (1) Contract source PR by [proposer] by 2026-07-08; (2) Product-team migration announcement by [chair] with EOL date; (3) Escalation to peer platform-side principal for storage-schema impact.

### Item 2 — Ranking blueprint re-platform proposal
Proposer: [ranking blueprint owner]
Summary: Consolidate feed / search / notifications ranking onto shared retrieval-and-ranking substrate.
Artifact section: chapter 6 § portfolio bets.
Decision: **Deferred** to ranking blueprint review (chair: [ranking blueprint owner]). Reference-architecture side: minor bump at next refresh to document the plug-in points; no contract shape change.
Follow-ups: Blueprint owner reports at next review body session on 2026-07-08 with contract-touching decisions flagged.

### Item 3 — Proposal to bypass eval-harness for internal-tools models
Proposer: [product-team rep]
Summary: For low-risk internal-tools models, propose skipping the eval-harness step.
Artifact section: chapter 4 § eval-harness invariants; Rule 15 of Rules of ML.
Decision: **Blocked**. The eval-harness contract's invariant "every launch cites a signed eval report" is not defeasible per contract. Nudge: for genuinely low-risk internal-tools models, the eval-harness can carry a light-bar profile; proposal reformed as a light-bar profile at eval-harness contract level.
Follow-ups: (1) Light-bar profile proposal from proposer by 2026-07-22; (2) Coordinate with eval-program owner.
```

Two properties matter about the log.

- **It is short.** One page for a two-hour session is fine. This is not meeting minutes; it is a decision log.
- **It cites the artifact.** Every decision references the specific chapter and section it acts on. This is what makes the artifact "living" — the log ties decisions to sections of the artifact that then update.

The log is publicly visible on the canonical location. Product-team engineers can read the log to see recent decisions before they propose their next integration. Peer principals can read it to see where the ML function is heading. Governance can audit it. This is the review body's *communication instrument*.

## Failure modes for the review body

- **Chair-becomes-approver.** Every item routes through the chair; the chair makes every call unilaterally; membership is nominal. Fix: rotate the agenda-setting role among members for two sessions; require voting on non-trivial items; visible ratio of "chair-decides" to "body-decides" should trend toward the latter.
- **Body-avoids-conflict.** Items that require blocking or hard escalation are quietly moved to a future session, never firing. Fix: name the "carry-over count" for each item in the log; anything carried over three times becomes a chair decision on the spot.
- **Membership-inflates.** The body grows to twenty people; sessions become status-report calisthenics; nothing gets decided. Fix: cap membership; rotate slots; refer non-members to the log.
- **No visibility into multi-team blueprints.** The body has no idea what the staff-scope blueprint owners are doing; artifact drift shows up as a surprise at the semi-annual review. Fix: monthly light-touch reports from blueprint owners.
- **Log-is-empty.** Sessions happen; the log is one line each. The body's memory does not persist across quarters. Fix: an intern-quality secretary drafts the log; the chair reviews and posts.
- **Log-is-a-novel.** The log records every debate detail; nobody reads it. Fix: the log records decisions and follow-ups, not debates. Debates live in the room.

## What the review body should be doing *outside* the sessions

The body's real leverage often happens between sessions.

- **Pre-triage.** The chair (or a rotating deputy) triages incoming items into the four modes and drafts the agenda. Many items resolve without a full session — a nudge over a comment, an escalation with a written note.
- **Cross-linking.** The chair keeps a small backlog of items pending review-body ratification, and cross-links them to the next likely session. This lets proposers plan.
- **Coalition-building with peers.** Chapter 8's platform-side principal seam is mostly maintained *between* sessions, in one-on-one conversations. The review body ratifies decisions; it does not manufacture consent.
- **Feedback to the mod-502 strategy owner.** When a bet in the strategy is repeatedly generating architecture-side pain — an evolution that doesn't fit, a contract change that keeps getting proposed and rejected — the chair carries that pattern back to mod-502's authoring cycle. The two artifacts are paired; they inform each other.

## Summary

- The org-wide architecture-review body is a standing forum, chaired by the principal, with a bounded named membership (chair + ML-org reps + platform-side principals + product-team reps + governance rep). It is where the reference architecture is enforced as a working contract.
- The chair exercises exactly four decision modes: **block** (contract-inconsistent), **nudge** (below the bar but consistent), **escalate** (out of scope; route to a peer principal or the executive branch), **defer** (owned by another forum; most commonly the staff-scope multi-team blueprint).
- The "defer to the multi-team blueprint owner" case is load-bearing. The principal owns the *contracts*; the blueprint owner owns everything *inside* the contracts. The principal does not duplicate the blueprint review.
- Cadence: biweekly regular, quarterly refresh review, semi-annual major review, annual grand refresh session. Session shape is fixed; the recent-decisions log is the atomic output on the canonical location (chapter 5).
- Watch six failure modes: chair-becomes-approver, body-avoids-conflict, membership-inflates, no-visibility-into-blueprints, log-is-empty, log-is-a-novel.
- Real leverage happens between sessions: pre-triage, cross-linking, coalition-building, feedback into mod-502. Chapter 8 walks the platform-side seams the body maintains and the executive-branch seams for governance.
