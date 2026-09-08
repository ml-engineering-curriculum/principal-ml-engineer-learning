# Setting the Review Bar and the Escalation Path to Principal Weight

> Chapter 4 of mod-505. Prerequisite: chapter 2 § *Class A — the canonical review pattern* and § *Class B — the north-star architectural revision*; mod-503 chapter 7 (running the org-wide architecture-review body); mod-502 chapter 7 (paired-artifact frame). Downstream: chapter 5 (technical culture) treats the review bar as one of the two most visible culture signals; chapter 6 (personal cadence) audits the review bar's freshness.

## Two bars, not one

ServiceNow's *Principal ML Engineer* posting phrases the target for this chapter directly: *"set the architectural patterns the group works from. Own the hard design calls, run the design reviews, and raise the bar on agentic design."* Two verbs matter — *own the hard design calls* names the bar for the specific review; *raise the bar* names the calibration work that lifts every team's reviews. This chapter treats both.

The review bar is not a single number. It is a *tiered* bar that varies with the artifact's altitude, and the principal's job is to *calibrate* the tier — not to run every review at maximum rigor. Running every review at north-star rigor is one of the failure modes named later in the chapter; running every review at senior-tech-lead rigor is the other.

Two altitudes carry the load. Both are principal-scope; each demands a different review shape.

- **Portfolio-scope RFC.** The mod-410 exercise-02 exec-audience RFC, the staff engineer's multi-team blueprint, the portfolio TCO. Owned at staff scope (`staff-ml-engineer-learning` mod-410). The principal sits in these reviews as a *calibrator*, occasionally, and mostly to *coach the reviewers* rather than to run the review themselves.
- **North-star scope revision.** A version-bump of the reference architecture (mod-503 chapter 6), a new canonical API contract (mod-503 chapter 4), a change to the shared eval standard (chapter 2 § Class D). Owned at principal scope (this track). The principal *runs* these reviews as the chair, and the rigor is the highest bar the org runs.

The escalation path — the third topic of the chapter — is the mechanism that lifts a *lower-altitude* review to *principal weight* when the lower review reveals a bar-crossing question the local reviewers cannot resolve. Escalations that are not gated on this criterion produce the *principal-as-super-reviewer* failure mode; escalations that never happen produce the *silent-drift* failure mode.

## The portfolio-scope RFC bar

A portfolio-scope RFC — a staff engineer's multi-team blueprint, an exec-audience RFC for a fiscal cycle, a portfolio TCO defence — is authored by a staff engineer for a leadership audience (VP-of-ML, adjacent-team VPs, the peer platform-side staff lead). The principal is not the primary reviewer of most of these; the primary reviewers are peer staff engineers plus the audience the RFC is written for. The principal's calibration surface is *what "reviewed" means* at this altitude.

### The eight axes the review has to touch

Any principal-scope calibrator reading a portfolio-scope RFC is checking that the review has substantive coverage across eight axes. Any single axis where the review is silent is either a bar issue or an escalation trigger.

1. **The direction the RFC commits leadership to.** Does the RFC name what leadership is being asked to commit to and by when? A portfolio RFC without a specific ask is a *manifesto*, not a decision-ask. Mod-410 exercise-02 is the shape reference; the principal's calibration check is that the RFC's ask is specific enough for leadership to commit or refuse.
2. **The alternatives considered.** Two to four named alternatives, each with a one-paragraph teardown. A single-alternative RFC has skipped the *tradeoff* half of engineering. Mod-503 chapter 6 § *evolution plan* is the parent shape.
3. **The cross-team consequences.** Which teams' work changes, when, and by how much. Absent-neighbor blindness is the single most common gap.
4. **The eval / launch bar the direction commits to clearing.** What has to be true before the direction is *executed*, not just *ratified*. Chapter 2 § *Class D* is the reference; a portfolio RFC that assumes the shared eval standard rather than naming its own launch bar is a gap.
5. **The rollback / reversibility position.** Which parts of the direction are reversible; which lock in for multiple fiscal years. A portfolio RFC whose entire direction is a one-way door needs the risk narrative to be extremely tight.
6. **The capacity and TCO envelope.** The engineering capacity, the GPU / cost envelope, the on-call / operational cost, and the operational-team growth the direction implies. `staff-ml-engineer-learning` mod-407 owns the portfolio-TCO shape; the principal's calibration check is that the number is *credible* and *sourced*, not aspirational.
7. **The responsible-AI / governance posture.** Which risk-tier (mod-503 chapter 8 § *contract 1*) the direction sits in, which governance touchpoints activate, which policies land as obligations. `staff-ml-engineer-learning` mod-409 owns the portfolio-scope responsible-AI framing; the principal calibrates that the RFC's posture matches what the north-star architecture (mod-503) expects.
8. **The measurable success criteria and the sunset criteria.** How will leadership know, in 6 / 12 / 18 months, that the direction is working? What would cause it to be sunset? Mod-502 chapter 4 (non-goals and sunset criteria) is the reference.

The principal reads for the *presence and substance* of each axis; the principal does not usually re-do the analysis inside each axis (that is the staff engineer's work). Absence on any axis is the calibration signal — either the RFC needs a revision, or the reviewers missed the axis, or the axis is legitimately deferred (in which case the deferral is documented per mod-504 chapter 6 § *deferred-decision artifact*).

### The principal's specific reads

Beyond the presence check, four principal-specific reads sit on top of the eight axes.

- **The organisational-context read.** Does the RFC land in the shape the north-star architecture and the North Star strategy expect? A portfolio RFC that assumes a different reference-architecture shape than mod-503 v-current is either wrong or is *signaling a needed revision to the architecture* — and the principal's calibration is to name which. This is the most durable principal-only read; peer staff reviewers do not have the whole-org context.
- **The precedent read.** Does the RFC cite prior RFCs, decisions, or leverage moves that share its problem class? An RFC that reinvents an argument the org has already settled is a signal about *review culture*, not just about the RFC. This is what feeds Class A leverage-move candidates (chapter 2).
- **The altitude read.** Is the RFC at portfolio altitude, or is it drifting up into North-Star territory (in which case it should be handled by mod-503) or drifting down into single-team RFC territory (in which case it does not belong in this review body)? Mod-503 chapter 2 § *two altitude-slip failure modes* is the reference; the same slip happens on RFCs, not just architectures.
- **The escalation read.** If any axis reveals a bar-crossing question — a governance obligation the staff engineer cannot commit the org to, a cost envelope that cannot be underwritten at the portfolio VP's authority, a cross-team consequence that requires an adjacent VP's ratification — the RFC needs an *escalation* to principal weight (the third section of this chapter). The principal is often the first person in the review reading for this escalation trigger.

### What the principal is *not* doing

- **Not re-authoring.** The RFC belongs to the staff engineer. The principal's comments are shape-shifting or precedent-citing; they are not *"here is how I would write the eval section."* Mod-410 exercise-02 is the staff engineer's practice; the principal coaches, does not co-write.
- **Not adding a ninth axis.** Every principal has favorite axes. Adding one to every RFC review inflates the bar without lifting it. Class A leverage-move discipline (chapter 2) is the correct place to add an axis if the axis is genuinely load-bearing; do not do it one review at a time.
- **Not running the review.** For portfolio-scope RFCs, the review chair is typically a staff engineer or the peer VP-of-ML. The principal sits in as a calibrator. Chairing every portfolio review is the *become-the-super-reviewer* failure mode.

## The north-star-scope revision bar

At north-star scope — a version-bump on the reference architecture, a new canonical API, a change to the shared eval standard — the principal *is* the chair (mod-503 chapter 7 is the parent forum), and the bar is set accordingly. The rigor is the highest the org runs.

### The seven-check north-star review checklist

The north-star review checklist is longer than the portfolio-RFC axis list because the artifact is *durable* — it will shape the org's work for multiple fiscal years. Missing a check produces long-tail cost.

1. **The paired-artifact discipline.** Is there a one-pager plus a deep-dive (mod-502 chapter 7)? A north-star revision published as only a long RFC misses the executive-audience artifact and will not ratify above the ML function.
2. **The version-bump justification.** Which of the mod-503 chapter 6 § *version-bump triggers* justifies this revision? A revision without a named trigger is either premature (the trigger is not yet hit) or under-scoped (the actual trigger is bigger than the revision addresses).
3. **The additive-by-default discipline.** Are the contract changes additive (new fields, new endpoints) or breaking (removed fields, changed semantics)? Breaking changes have a hard bar: a deprecation window, a migration plan per consumer team, a *specific* team-by-team migration commitment. Mod-503 chapter 4 § *stability-vs-versioning* is the reference.
4. **The peer-platform-side co-authorship.** Has the revision been co-authored with the peer platform-side principal (mod-503 chapter 8)? A north-star revision authored without the platform-side counterpart tends to name interfaces the substrate cannot actually support.
5. **The governance posture.** Which of the responsible-AI / governance obligations the revision changes, and which policies it lands. Mod-503 chapter 8 § *contracts 1–3* is the reference.
6. **The migration plan with named owners and dates.** For every consumer team, who commits to migrating and by when. The plan is a *coalition* (mod-504 chapter 4), not a mandate; the migration commitments are collected as part of the review.
7. **The rollback plan.** If the revision has to be rolled back, what does that look like? Which version reverts to which; how long the rollback window is; who is authorised to trigger it. North-star revisions are not one-way doors; the rollback plan is what keeps them from becoming so.

### The review meeting itself

A north-star revision review meeting is a specific ritual, not a generic sync. Mod-503 chapter 7 § *session shape and agenda* is the parent reference; the addenda specific to this chapter:

- **Pre-read is required and enforced.** Attendees have read the one-pager and skimmed the deep-dive. Attendees who have not are asked to leave; the chair does not walk the deep-dive line-by-line in the room. Enforcement makes the bar credible; permissiveness erodes it in a single cycle.
- **The four decision modes are named.** *Block*, *nudge*, *escalate*, *defer* (mod-503 chapter 7 § *four decision modes*). Every material point resolves into one of the four before the meeting ends. Leaving a point unresolved is a *defer* decision with a named next-review date, not a soft ellipsis.
- **The *"what is not on the agenda"* section.** Named explicitly at the top. Items that belong at the portfolio-scope RFC level; items that belong at the governance-review body; items that belong at the peer platform-side principal's review body. This is the discipline that keeps the room at the right altitude.
- **The rationale is captured, not just the decision.** For each *block* or *nudge*, the specific rationale is captured in the review log — not merely *"we asked the author to revise section 5,"* but *"we asked the author to revise section 5 because the migration plan does not name Team X's commit, and Team X's real-time features are the load-bearing consumer of the v3 → v4 change; without a Team X commit the migration is not defensible."* Rationale is what makes the review reproducible.

### The principal's specific responsibilities as chair

- **Set the agenda in advance.** Pre-read distribution 5 working days before the meeting, with the "what is not on the agenda" section already drawn.
- **Keep the room at the altitude.** When the discussion drifts into staff-scope RFC territory, name the drift and re-anchor. This is where the *own the hard design calls* verb from the ServiceNow target sentence lives.
- **Force the resolution.** Every material point resolves into a decision mode before the meeting ends. Softness is not a decision.
- **Write the meeting note.** The chair — the principal — writes the meeting note within one working day, distributes it to the attendees, and posts it in the canonical location (mod-503 chapter 5). Notes drafted by anyone else erode the bar.

## The escalation path

The escalation path from a lower-level review to principal weight is the mechanism that makes the tiered bar work. Without it, either every principal-weight decision has to be re-litigated in the north-star review body (creating a review backlog), or bar-crossing decisions get made at the lower level and only surface as problems later.

### The four escalation triggers

An escalation from a lower review to principal weight is warranted when — and only when — one of these four triggers fires.

1. **The direction requires a north-star architecture revision.** The RFC's direction, if ratified, requires the reference architecture (mod-503) to change. Example: the RecSys team's next re-platform needs a new real-time feature contract that the current north-star architecture does not have. The staff engineer cannot ratify the north-star change; the escalation lifts the question to the north-star review body.
2. **The direction crosses a governance obligation the staff engineer cannot commit to.** The RFC's direction lands the org in a higher risk tier (mod-503 chapter 8 § *contract 1*), triggers a regulatory obligation the org has not previously operationalized, or requires a policy-to-contract mapping (mod-503 chapter 8 § *governance seam*) that has not been drawn. The staff engineer cannot commit the org to policy; the escalation lifts the question to the principal in partnership with the Head of AI Governance (mod-504 chapter 3 § *counterpart 2*).
3. **The direction has cross-org consequences that require executive-branch partnership.** The RFC's direction, if ratified, requires a peer executive's commit (CFO underwriting a capacity envelope, CISO signing off on a threat-model change, CAIO / VP-of-ML holding a specific board-facing narrative). The staff engineer cannot invoke the partnership contracts (mod-504 chapter 3); the escalation lifts the question to the principal.
4. **The direction is stuck on a technical judgment the local reviewers are split on.** The RFC's local review has produced a deadlock (a principal-scope technical question the local reviewers cannot resolve without the whole-org context the principal carries). Example: two staff engineers disagree on whether a new agentic pattern should sit inside the north-star architecture's serving plane or should stand up its own plane. Neither has the whole-org context; the principal does.

### The four escalation *anti-*triggers

Escalations often happen for reasons that are *not* on the list. Naming the anti-triggers is what keeps the bar from collapsing into *"escalate everything to the principal."*

- **"The team wants a principal to sign off."** A team's desire for principal sign-off is *not* an escalation trigger; it is often a sign that the local reviewer is not exercising the authority they have. Fix: coach the local reviewer to make the call, and only escalate if trigger 1–4 actually fires.
- **"The decision is important."** All portfolio-scope RFCs are important; not all are principal-weight. Importance is not altitude. Fix: name which of triggers 1–4 the decision fires; if none, the decision belongs at the local altitude.
- **"The principal has opinions."** The principal has opinions on many things; that is not an escalation criterion. If the principal has an opinion on a portfolio-scope RFC that does not fire triggers 1–4, the correct action is a review comment, not an escalation. Fix: keep an opinion-only reaction as a review comment; escalate only if a trigger fires.
- **"The team wants to move faster than the local review body."** A team using principal escalation to bypass the local review body is a *governance-loop-hop* failure. Fix: send the escalation back to the local review body with a note; if the local review body is genuinely blocking the team without cause, that is a Class A leverage-move candidate (chapter 2).

### The escalation artifact

An escalation is a written artifact, not a hallway conversation. Shape:

- **One paragraph — the trigger.** Which of the four triggers fires, and the specific evidence for it. (*"Trigger 1: the RFC's direction requires a new real-time-feature contract that mod-503 v3.4 does not carry. The current contract is v3.3.2; the RFC proposes fields the v3 contract cannot express without breaking additive-by-default."*)
- **One paragraph — the local review's state.** What the local reviewers have concluded, where they are split, what they have agreed to defer to the escalation.
- **One page — the specific question for the principal.** Not *"please review,"* but *"we are asking: (a) can the north-star architecture accommodate this change without a v3 → v4 major, or does this justify the v4 major we discussed in the mod-503 chapter 6 evolution plan? (b) if (a) is v4, what is the migration commitment we can pre-commit to?"*
- **A named decision date.** *"We need a decision by 2026-11-15 to hold the RecSys re-platform Q1 milestone."* Absence of a date turns escalations into open-ended asks; the principal's backlog then determines the answer.

### The principal's response

The principal's response to an escalation is one of four actions.

- **Ratify at principal weight.** The principal reads the artifact, holds a 30-minute discussion with the local reviewers, and commits the decision — often adding a version-bump entry to the mod-503 chapter 6 evolution plan.
- **Send back with specific asks.** The escalation is legitimate but the artifact is not yet decidable. The principal writes back with the specific asks (an additional analysis, an additional stakeholder consult) and a re-review date.
- **Convene the north-star review body.** The escalation is bigger than a bilateral call; it needs the review body forum. The principal schedules the north-star review body session and adds the item to its agenda.
- **Return to local scope.** The escalation does not fire a valid trigger. The principal writes back with the reason (which of the anti-triggers applies) and returns the decision to the local review body. This is a coaching moment for the local reviewer; do not skip it.

Each response is written and posted in the canonical location. The response *shape* is what teaches the local review bodies to escalate correctly next time; verbal-only responses lose the teaching.

## Interaction with the review body forums

The review bar sits inside a lattice of review-body forums, each with its own scope. Naming the forums keeps the escalation path legible.

- **Local team review body.** Owns single-system RFCs and per-team design reviews. Owned by the team's staff engineer or senior tech lead.
- **Portfolio review body.** Owns portfolio-scope RFCs and multi-team blueprints. Owned by the staff engineer or the peer VP-of-ML.
- **The org-wide architecture-review body.** Owns north-star revisions. Owned by the principal (this track). Mod-503 chapter 7 is the parent reference.
- **The responsible-AI review body.** Owns risk-tier decisions, launch-gate exceptions, regulatory activations. Owned by the Head of AI Governance ([`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) peer track); the principal partners under mod-504 chapter 3 § *counterpart 2*.
- **The hiring committee.** Owns loop-level and hire-level ratification. Owned by the hiring committee chair (usually a VP-of-Engineering / VP-of-ML); the principal sits as a calibrator per chapter 3.

An escalation crosses forums (from portfolio to org-wide, from local to portfolio, from architecture to responsible-AI). The escalation artifact names the forum the escalation is heading to and — critically — the forum it is *not* going to. Escalations that skip forums (a local team review skipping straight to the org-wide architecture-review body) are a *governance-loop-hop* pattern; the fix is to send the escalation to the correct next forum, not to accept the skip.

## Failure modes

- **Running every review at north-star rigor.** The *tier-collapse* failure. Every portfolio RFC gets the eight-axis read plus the seven-check north-star review; the review bar is uniform and unaffordable. Fix: name the tier at the top of every review; run only the tier's discipline.
- **Never chairing the north-star review.** The principal defers the north-star review body to a delegate; the delegate cannot force resolution at north-star altitude. Fix: chair it yourself. The chairing is the leverage.
- **Escalating on opinion, not on trigger.** Escalations that carry the principal's opinion but do not fire any of the four triggers erode the local reviewers' authority. Fix: apply the four-trigger discipline.
- **Refusing to escalate.** Local reviewers who never escalate because *"the principal is busy"* produce silent-drift decisions the org later has to un-decide. Fix: the review pattern (Class A leverage move) includes explicit escalation criteria; publish them so escalations are ratified as *the right thing to do*, not *bothering the principal*.
- **Reviewing without capturing rationale.** Reviews whose meeting notes are one-line summaries do not teach; the next cycle re-litigates. Fix: the chair writes the note within one working day, with rationale per material point.
- **Coaching the reviewers through the review's outcome, not through the review's process.** A principal who sends every review's outcome back to the reviewer with corrections but never coaches on *how the reviewer got there* creates dependency, not skill. Fix: separate outcome-feedback from process-coaching; the latter is the chapter 1 § *bar-calibration behaviour* signal for L40 mentees.

## A worked micro-example

For grounding, here is what the *review-bar summary* on a principal's practice reads like at defensible altitude.

> **Review-bar practice (FY26-Q3, v1.4).** North-star architecture-review body sessions chaired in FY26: 3 (Q1, Q2, Q3). All three produced published meeting notes in canonical location within 1 working day; all four decision modes (block, nudge, escalate, defer) invoked at least once across the three. Version-bump revisions: 2 (v3.3 → v3.4 real-time feature-contract additive; v2.6 → v2.7 eval-harness observability). Portfolio-scope RFCs calibrated (I sat as reader, staff engineer chaired): 8. Escalations from portfolio to north-star: 3 — 1 ratified at principal weight (v3.4 above), 1 returned to local scope (opinion-only, no trigger), 1 sent to the responsible-AI review body per anti-trigger 4 handoff. Class A leverage-move signal: the *rationale-captured* discipline is inconsistently applied across the 8 portfolio-scope reviews I sat on — 3 of 8 meeting notes were one-line summaries. Drafting a canonical review-pattern v2 addendum with two staff engineer co-authors for FY26-Q4 ratification. Retirement candidates: the FY24 launch-review checklist v1 has been superseded by v2.

Notice the shape: named forums, chair vs. sit-as-reader distinction, the four decision modes, escalation counts with their resolution, a specific Class A signal, retirement candidates. Not "reviewed many things this quarter."

## Summary

- The review bar is *tiered*, not uniform. Portfolio-scope RFCs (owned by staff scope, `staff-ml-engineer-learning` mod-410) get an eight-axis substance check plus four principal-specific reads. North-star-scope revisions (owned by this track, mod-503 chapter 7 is the parent forum) get a seven-check north-star review at the highest rigor. Running every review at north-star rigor is the *tier-collapse* failure.
- On portfolio-scope RFCs, the principal is a *calibrator* who reads for presence and substance across the eight axes, does not re-author, and does not add axes one review at a time. The four principal-specific reads (organisational-context, precedent, altitude, escalation-trigger) are what only the principal can bring.
- On north-star-scope revisions, the principal *chairs* the review. The chair holds pre-read enforcement, the four decision modes (block / nudge / escalate / defer), the *what-is-not-on-the-agenda* section, and — critically — writes the meeting note themselves within one working day.
- The escalation path from lower reviews to principal weight fires on exactly four triggers: north-star-architecture-change required, governance obligation the staff engineer cannot commit to, cross-org consequence that requires executive-branch partnership, technical deadlock at the local level. Four *anti*-triggers rule out escalations that are only about principal opinion, importance, principal-sign-off desire, or a governance-loop-hop.
- The escalation is a written artifact with the trigger, the local state, the specific question, and a named decision date. The principal's four responses (ratify, send back, convene the review body, return to local scope) are all written and posted in the canonical location.
- Six failure modes: running every review at north-star rigor, never chairing the north-star review, escalating on opinion, refusing to escalate, reviewing without capturing rationale, outcome-feedback instead of process-coaching.
- Chapter 5 treats the review bar as one of the two most visible culture-signaling surfaces the principal owns — culture is *what the bar rewards*, not what the principal says.
