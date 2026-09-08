# exercise-04: Org-Wide Architecture-Review Charter

**Estimated effort:** 2 hours

## Objective

Draft the *charter*, *membership*, and *first review-body session* of the org-wide applied-ML architecture-review body (chapter 7). Then walk three worked items through the four decision modes — **block**, **nudge**, **escalate**, **defer** — and log them to the recent-decisions log in the shape chapter 7 § *written outputs* fixes.

The output populates `review-log/charter.md` and `review-log/2026-<Q>-<DD>-session-01.md` in the exercise-01 artifact. The three worked items are the *forcing function* that verifies your charter and membership actually support the four decision modes.

## Prerequisites

- Exercise-01 complete — the artifact skeleton with an empty `review-log/` directory.
- Exercise-02 complete — the four canonical contracts. The review body's job is to enforce them; you need them written.
- Exercise-03 complete — the evolution plan. Many of the review-body's items derive from it.
- Chapter 7 read end-to-end.
- Chapter 8 skimmed — the peer-principal seam and the governance seam determine review-body membership.

## Problem statement

Chapter 7 opens with the two failure modes an unenforced reference architecture falls into: **silent divergence** (teams ship changes that violate the shape and drift accumulates over quarters) and **bottleneck-on-principal** (every change routes to the principal individually; leverage collapses). The org-wide architecture-review body is the corrective — a standing forum, chaired by the principal, with a bounded named membership.

Your job on this exercise is not to run a review body in practice (that requires an org). It is to draft the *charter*, define the *membership*, sketch the *first session*, and walk *three items* through the four decision modes such that the log entry chapter 7 § *written outputs* fixes could be posted to the canonical location tomorrow.

Chapter 7's four decision modes are the load-bearing craft. Every item in your first session must fit into exactly one of block / nudge / escalate / defer. At least one item must exercise each mode.

## Requirements

Populate `review-log/` with two files.

### `review-log/charter.md` — the standing charter

The charter is a short document that a new member (or an outside auditor) can read in five minutes and understand the body's scope, cadence, and authority. Chapter 7 § *the body's charter* is the template. Include:

- **Purpose.** One paragraph. What the body reviews (the six-plane shape, the four canonical APIs, the evolution plan) and what it does not (multi-team blueprint reviews, team-level design reviews). Cite chapters 2 and 7 explicitly for the altitude boundary.
- **The four load-bearing charter properties** — standing (not ad-hoc), chaired by the principal, bounded (membership is bounded and named), bounded scope (chapter 2's altitude discipline is the reference). Chapter 7 § *the body's charter*.
- **Membership.** Named populations (chapter 7 § *membership*) with a specific placeholder for each seat: chair (the principal), two-to-three ML-org staff engineers (name their blueprints — ranking, Gen-AI, shared-substrate — even if names are placeholder), two peer platform-side principals (one from `ai-infra-principal-engineer-learning`, one from `ai-infra-principal-architect-learning`), one-to-two product-team representatives (with a quarter-by-quarter rotation policy noted), one governance representative (from `head-of-ai-governance-learning`). Two guest-rotating seats. State that the platform-side and governance seats are *voting* members on decisions touching their scope.
- **Cadence.** Chapter 7 § *cadence* — biweekly regular / quarterly refresh review / semi-annual major review / annual grand refresh session, with placeholder next-session dates.
- **The four decision modes.** Reproduce the mode names (block / nudge / escalate / defer) with a one-sentence definition each, quoting from chapter 7 § *the four decision modes*.
- **Session shape.** Chapter 7 § *session shape and agenda*. Agenda posted 48 hours before; round of updates; items (10–15 minutes each); closing summary. Explicit "what is not on the agenda" section.
- **Recent-decisions log conventions.** Where the log lives (a link into the canonical location from exercise-01), the log's format (chapter 7 § *written outputs*), the log's audience (product-team engineers, peer principals, governance, auditors).
- **What the body does *between* sessions** — pre-triage, cross-linking, coalition-building, feedback into mod-502. Chapter 7 § *what the review body should be doing outside the sessions*.
- **Charter revision cadence** — annual, aligned with the fiscal year, ratified at the annual grand refresh session.

### `review-log/2026-<Q>-<DD>-session-01.md` — the first review-body session log

Chapter 7 § *written outputs — the recent-decisions log* fixes the log's shape. Use it. Include:

- **Header** — date, chair (the principal), members present, members absent (with reason). If any voting-required seat is absent, note the impact on ratification.
- **Round of updates** — one sentence per represented population. Not blockers; context.
- **Three items**, each 10-15 minutes of session-time equivalent, with the log shape:
  - **Item summary** — one paragraph. Proposer and their affiliation.
  - **Artifact section touched** — the specific chapter and section of the reference architecture the item acts on. This is the load-bearing citation; without it the item is not ready (chapter 7 § *session shape and agenda*).
  - **Decision** — exactly one of block / nudge / escalate / defer. The mode is chosen and named.
  - **Follow-ups** — a numbered list of who does what by when.

### The three worked items — one required per decision mode (at minimum three across the four modes)

Chapter 7 gives four modes and four example scenarios per mode. Draft your three items so that at least one is a *block*, one is a *nudge*, and one is either an *escalate* or a *defer*. Ideally all four modes fire in the first session; three is the minimum. The items must be drawn from your artifact — real items derived from your exercise-02 contracts, exercise-03 evolution plan, or exercise-05 seam drafts. Do not invent items unrelated to your artifact.

Suggested item shapes to adapt:

- **A "block" item.** A proposal that violates one of the four contract invariants — e.g. a proposal to route production traffic to an `eval-passed` (not-yet-`blessed`) model without a canary declaration (chapter 4 registry invariants; chapter 7 § *examples of legitimate blocks*).
- **A "nudge" item.** A proposal that meets the contracts but is below the field bar — e.g. a model-card entry that is minimal-but-legal, nudged toward the [Mitchell et al. Model Cards](https://arxiv.org/abs/1810.03677) standard (chapter 7 § *examples of legitimate nudges*).
- **An "escalate" item.** A proposal requiring peer-principal consent — e.g. a training-cluster SLO tier retitration that the peer platform-side principal has to co-decide (chapter 8 § *contract with the Principal AI-Infrastructure Engineer*).
- **A "defer" item.** A proposal that reshapes a specific blueprint — e.g. the internal design of the ranking retrieval-and-reranking blueprint, which is `staff-ml-engineer-learning` mod-401 / mod-402 scope. Chapter 7 § *the "defer to the multi-team blueprint owner" case, walked* is explicit that this is the most under-practiced case.

Each item's *Decision* line must cite the specific chapter and section that justifies the mode chosen. Chapter 7 § *written outputs* is the standard.

## Starter guidance

- **Draft the charter before the session.** A session log that references a charter no one has read is a body that will slip within two sessions. Chapter 7 § *why a review body* names the "silent divergence" and "bottleneck-on-principal" failure modes; both are what an unstated charter permits.
- **Membership at the right altitude.** Chapter 7 § *membership* names the five representative populations. If your membership list has fewer than three of the five, the body is under-populated for what chapter 7 § *the body's charter* expects. If it has more than seven or eight seated members, you are likely descending into a design-review board (chapter 7 § *membership-inflates* failure mode). Aim for six to eight seats.
- **The mode is chosen; it is not negotiated.** The chair calls the mode. If your log has a decision line reading "block or nudge, depending on the follow-ups", chapter 7 § *chair-becomes-approver* / *body-avoids-conflict* is the failure mode. Pick a mode; commit.
- **Cite the artifact for every decision.** Chapter 7 § *written outputs* is explicit: every decision references the specific chapter and section of the reference architecture it acts on. This is what makes the log "living". Without the citation, the log is meeting minutes.
- **Blocks are contract-level, not preference-level.** Chapter 7 § *when not to block* — the chair does not block on "I would have done it differently". Blocks are for artifact-inconsistent proposals. Your block item's citation must reference a contract *invariant*, not a preference.
- **Defers name the destination forum.** Chapter 7 § *the "defer to the multi-team blueprint owner" case, walked* — the deferral must name the forum by name and by chair. "Deferred pending discussion" is not a deferral; it is body-avoids-conflict in disguise.
- **The log is short.** Chapter 7 § *written outputs* is explicit: one page for a two-hour session is fine. Debates live in the room. The log is a decision record, not a transcript.

## Acceptance criteria

Your artifact is done when it can pass all of the following:

- [ ] `review-log/charter.md` contains the ten sections listed in *Requirements*: purpose, four properties, membership, cadence, four decision modes, session shape, log conventions, between-sessions work, revision cadence.
- [ ] The charter names all five representative populations from chapter 7 § *membership*, with placeholder seats for each. Platform-side and governance representatives are marked as *voting* on their scope.
- [ ] The cadence names biweekly / quarterly refresh / semi-annual major / annual grand refresh with placeholder dates.
- [ ] `review-log/2026-<Q>-<DD>-session-01.md` follows the log shape from chapter 7 § *written outputs* — header, round of updates, items with the four required fields, closing summary.
- [ ] At least three items in the session log. At least one is a *block*, one is a *nudge*, and one is either an *escalate* or a *defer*.
- [ ] Every item's *Decision* line cites a specific chapter and section of the reference architecture (chapter 4 § feature invariants, chapter 6 § capability bets, chapter 8 § contract 2, etc.). No decision is uncited.
- [ ] The *block* item's citation is to a contract invariant (chapter 4), not to a preference or style guide.
- [ ] The *defer* item names the destination forum by name and by chair.
- [ ] No item in the log exceeds one page of body text; the whole session log is one to two pages total.
- [ ] Every item derives from an actual artifact section (contract from exercise-02, evolution-plan bet from exercise-03, seam contract from chapter 8 / exercise-05). No items are unrelated to the artifact.
- [ ] The charter's "what is not on the agenda" section names at minimum: team-specific status updates, individual model launches without an artifact-touching angle, blueprint reviews chaired elsewhere, unrelated retros. Chapter 7 § *session shape and agenda*.

## Stretch goals

- **Walk the six failure modes.** Chapter 7 § *failure modes for the review body* names six (chair-becomes-approver, body-avoids-conflict, membership-inflates, no-visibility-into-multi-team-blueprints, log-is-empty, log-is-a-novel). For each, write a one-sentence description of the specific hygiene *your* charter and log conventions use to prevent it.
- **Draft session two, or session three.** Chapter 5 § *the publication cadence* and chapter 7 § *cadence* connect at the quarterly refresh review. Draft the session log for the quarterly refresh review that comes after your exercise-04 first session — its agenda is the refresh's changelog. This exposes any gaps in exercise-01's changelog conventions.
- **Draft a rotating deputy-chair rota.** Chapter 7 § *what the review body should be doing outside the sessions* names pre-triage as one of the between-session activities. Sketch a rotation among the ML-org staff-engineer members so that one is deputy-chair each quarter, responsible for pre-triage and agenda-drafting between sessions.
- **Draft the "policy-to-contract mapping" review flow.** For a governance-class item on your queue (from exercise-03), walk the specific back-and-forth between the review body and the governance peer's forum. This connects to exercise-05 and to chapter 8 § *communication rhythm with governance*.
- **Draft a member-satisfaction survey.** A quarterly one-page survey the chair sends to members: (i) are we at the right altitude? (ii) are the modes being applied consistently? (iii) is the log being read by product teams? Chapter 7's failure modes are more preventable when the body has a lightweight feedback loop.

## Deliverable location

Local workspace / personal git repo, extending the exercise-01 artifact. The `review-log/` subtree is what this exercise populates; the artifact-level `README.md` from exercise-01 should now link to `review-log/charter.md` and to the session-01 log.
