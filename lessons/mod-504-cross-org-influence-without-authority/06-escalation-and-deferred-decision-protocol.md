# The Escalation and Deferred-Decision Protocol

> Chapter 6 of mod-504. Prerequisite: chapters 1–5. Downstream: exercise-04 authors the escalation log, one worked escalation, and one deferred-decision artifact. This chapter closes the module.

## The three-way question every cross-org disagreement resolves into

Every material cross-org disagreement — a bet the coalition tracker (chapter 4) is failing to converge, an objection the FAQ (chapter 5) cannot yet resolve, a partnership contract (chapter 3) whose peer disagrees on direction, a canonical API contract (mod-503 chapter 4) whose consumer refuses to build against it — presents the IC-principal with a three-way question:

1. **Escalate.** Bring the decision to an executive who has line authority over the parties in disagreement (usually the CTO, the CEO, or a peer executive-branch counterpart with authority over the specific dimension).
2. **Grind.** Keep working the disagreement at the technical layer — more evidence, more 1:1s, more artifact refinement, more coalition sequencing.
3. **Defer.** Accept that the org is not yet ready for the bet and *document the not-yet decision* with a named revisit condition so the next cycle can pick it up.

The three-way question is the single most under-taught skill at principal altitude. First-cycle principals default to grind — persistence being the modal virtue of high-performing individual contributors — and grind past the point where the grind is productive. Second-cycle principals over-correct into escalation and burn the partnership contracts (chapter 3). Third-cycle principals discover that defer is a valid, honorable outcome and start using it; and immediately discover that most orgs treat *defer* as *dead*, so they invest in the *deferred-decision artifact* that keeps a deferral alive across cycles.

This chapter walks the three-way question, the escalation protocol, the grind protocol, and the deferred-decision artifact.

The framing anchors to the composite of the previous five chapters. Chapter 1 named the escalation-and-deferral discipline as one of the five defensibility tests. Chapter 3 named the escalation paths per peer executive counterpart. Chapter 4 named the coalition tracker's *shift signals* column as the escalation-and-deferral fuel. Chapter 5 named the FAQ's *deferred* entries as the artifact-side surface. This chapter walks the protocol that runs through all four.

## §1 — Which of the three states is this in?

The single most useful discipline in this chapter is *naming the state*. A material bet in the mod-502 portfolio that is not moving is in one of the three states. The principal's job — before doing anything about it — is to name which. A bet whose state is uncertain is a bet whose next move is under-determined.

Read the coalition tracker (chapter 4 §2) with the following criteria in mind.

### Criteria for escalate

A cross-org disagreement is *ready to escalate* when:

- **The specific decision is well-defined.** A single, resolvable question the escalator will answer. Not *"should we invest more in Gen-AI?"* — *"should the ML function underwrite the FY26 post-training program capacity ask of X-Y engineers, given the CFO's current envelope proposal of Z?"*.
- **The parties in disagreement are named.** The specific two-or-three peers whose disagreement is blocking the bet. Not *"the org isn't sure"* — *"the CFO is at Z, the CAIO is at X, the direction requires resolving this by <date>"*.
- **The parties have already tried to resolve at the technical layer.** Chapter 3's per-peer resolution paths (the joint monthly, the quarterly deep-dive, the co-authored artifact) have been used and not converged. Escalation-before-partnership-attempt is a partnership-breaking move.
- **The escalator is the right altitude.** For a CAIO / CFO disagreement, the escalator is the CTO or the CEO. For a CAIO / Head of AI Governance disagreement, the escalator is the General Counsel or the CEO. Chapter 3 § *escalation path* per peer is the reference. Escalating to the wrong altitude either fails (the escalator does not have authority) or works but breaks the partnership contract (the escalator overrides a peer they should not have been asked to override).
- **The decision has a deadline that grinding cannot make.** If the bet's revisit-signal or the org's planning cycle passes without a decision, the bet's window closes. This is what makes escalation the *right* move — grind will not make the deadline; escalation might.

If all five criteria are met, escalate. Section §2 walks the protocol.

### Criteria for grind

A cross-org disagreement is *ready to keep grinding* when:

- **The disagreement is at the evidence layer.** The parties disagree because they hold different information; more evidence would move them. Chapter 4 § *shift signals* is what tells you what evidence would move the specific stakeholder.
- **The evidence is achievable within the horizon that matters.** A pilot, a benchmark, a customer signal, a competitive move that can be observed. Not *"if only we had ten years of data"*.
- **The bet's window has not closed.** The mod-502 chapter 6 signal-tracking cycle is still saying the bet is in-window; the next planning cycle can still absorb the bet.
- **The partnership contracts (chapter 3) still hold.** The peer executives are still willing to have the 1:1s, ratify the co-authored artifacts, take the pre-briefings. If a partnership contract has visibly frayed, grinding the technical layer will not fix it; the fix is at the contract layer.
- **The principal's own energy budget still fits.** Grind consumes IC-principal attention. A bet the principal has ground for two cycles is a bet consuming attention that could be spent on other portfolio rows. Section §5 (dead-scope discipline) is the corrective when the grind has become a sunk cost.

If all five criteria are met, grind. Section §3 walks the protocol.

### Criteria for defer

A cross-org disagreement is *ready to defer* when:

- **The disagreement is at a layer the org is not yet ready to resolve.** Not lack of evidence; not lack of coalition. A structural constraint — the org's regulatory environment has not yet clarified, the org's business direction is in-flux above the CTO, the org's competitive posture has not yet resolved, the org's substrate has not yet matured — that makes the bet's ratification premature.
- **A specific revisit condition can be named.** *"This bet is deferred pending <specific external signal or specific internal state change>, expected by <named date or named event>."* If no revisit condition can be named, the bet is not defer; it is dead scope (section §5) or grind (needs more work to define).
- **The deferral is documented.** Section §4 walks the deferred-decision artifact — the document that makes the deferral survive across cycles.
- **The four peer executive counterparts (chapter 3) can name the deferral in one sentence.** *"The X bet is deferred pending Y, expected by Z"*. If they cannot, the deferral has not been socialised, and the next cycle will treat it as dead.
- **The bet is worth the memory cost.** Not every deferred bet is worth carrying across cycles. The deferral is an active investment; the artifact has a maintenance cost. Section §5 walks the dead-scope discipline that closes deferrals that are no longer worth the cost.

If all five criteria are met, defer. Section §4 walks the protocol.

## §2 — The escalation protocol

Escalation is a mechanism the IC-principal has, in bounded quantity, to break a decision. The bound is important: an IC-principal who escalates every disagreement erodes the credibility of every future escalation. Chapter 3 § *"the peer's authority is what you borrow"* is the ground truth; escalation is the case where the borrowing becomes explicit and visible.

### Pre-conditions

Before escalating:

1. **The four peer executive counterparts (chapter 3) know the escalation is coming.** Not "know after". Not "learn from the CTO's calendar". Every peer executive whose portfolio the decision touches receives a 1:1 or a briefing note *before* the escalation lands on the escalator's calendar. This is the standing *never surprise your peer* discipline (chapter 3).
2. **The specific question is written down.** The escalator will read one paragraph before the escalation meeting. Draft it. The paragraph names the decision, the parties, the specific ratified positions of each, and the specific outcome the escalation would produce.
3. **Both sides of the disagreement have been co-authored.** The principal is *not* the plaintiff in an adversarial escalation; the principal is the *technical author* who presents both sides fairly. Chapter 3 § *the peer's authority is what you borrow* extends here: the escalator will be more willing to rule when the principal has presented the peer's position accurately, in language the peer endorses.
4. **The alternative outcomes are enumerated.** Not one — three or four. The escalation is *"here are the three possible resolutions and their consequences"*, and the escalator picks one. The escalator who is presented with a binary or with only the principal's preferred outcome will (correctly) defer the decision.

### The escalation artifact

A short document — one to two pages. Sections:

- **The decision.** One paragraph. The specific question the escalator will answer.
- **The parties.** Named. Their titles. Their current positions, verbatim.
- **Why we cannot resolve at the technical layer.** One paragraph. Cite the specific stage B 1:1s (chapter 4) that were held and did not converge.
- **What each resolution would mean.** For each of the three-or-four possible outcomes, a paragraph on the consequence — capacity, direction, timeline, partnership impact.
- **What the principal recommends and why.** One paragraph. The principal has a technical view; state it and defend it. The escalator will use this as the starting point but is not obliged to follow it.
- **What the peer parties recommend and why.** One paragraph per peer party, in their voice, ideally endorsed by them before the escalation.
- **The deadline.** When the decision must be resolved by, and what happens if it is not.
- **The follow-up.** What the principal will do with the decision once made — how it lands in the strategy, the reference architecture, the coalition tracker.

Chapter 3's *never surprise your peer* is what enables the paragraph *"what the peer parties recommend and why, endorsed by them"*. Without pre-briefing, that paragraph is impossible to author honestly; without the paragraph, the escalation is one-sided and the escalator will (correctly) discount the principal's framing.

### The escalation meeting

Fifteen to thirty minutes with the escalator. Structure:

- **The escalator states the question back.** They read the artifact before the meeting; the meeting opens with them summarising it. If they cannot, the artifact has failed at the writing layer; withdraw and rewrite.
- **The parties are present (or represented).** The peer executives whose positions are being adjudicated are in the room or on the call. If they are not, the escalator is being asked to rule without hearing the parties — the modal outcome is deferral, not decision.
- **The principal walks the four-or-three outcomes.** Five minutes. Neutral tone. The recommendation is stated but not defended aggressively.
- **The peers state their positions.** Ten minutes total across the peers. This is where the pre-briefing pays off — the peers already agreed to the paragraph the principal has already written; they are ratifying it in the room.
- **The escalator decides.** In the meeting, on the spot, if possible. If not, with a named date by which the decision will be made. Not *"we'll think about it"* — a decision-making cadence.
- **The follow-up is confirmed.** Who does what by when. The principal's coalition tracker (chapter 4) absorbs the outcome.

### After the escalation

- **The decision is written down within 24 hours.** A one-page memo to the coalition tracker's stakeholders. The escalator's decision, the parties' positions, the follow-up commits.
- **The partnership contracts are held.** The peer executive whose position was over-ridden by the escalation is *followed up with in a 1:1 within a week*. The escalation is a normal mechanism, not a betrayal; the 1:1 is where the partnership contract absorbs it. Skipping this 1:1 is the fastest way to break a partnership contract.
- **The escalation log absorbs the decision.** Section §6 walks the log.

### Escalation is expensive

Every escalation consumes the principal's *escalation budget* — the finite credibility the escalator (CTO / CEO) extends to the principal for bringing them decisions. Two escalations per fiscal year is the modal cadence for a mid-cycle principal; five is high; ten is a signal that the partnership contracts (chapter 3) are failing and the fix is at that layer, not at the escalation layer.

Signs the escalation budget is being over-drawn:

- The escalator's calendar for the principal shortens over successive cycles.
- The escalator's decisions increasingly default to *"work it out at the peer layer"* — a diplomatic *"stop escalating to me"*.
- The peer executive counterparts start to *anticipate* the escalation and route around the principal by escalating first — a rupture of the partnership contract.

If any of these signs surface, the corrective is not more careful escalation; it is a return to the partnership contracts (chapter 3) and the coalition sequence (chapter 4). The escalations that are being run are downstream of a partnership failure the principal has not yet named.

## §3 — The grind protocol

Grind is the mode of a bet that is not ready to be ratified and not ready to be deferred. It is the mode most under-articulated in curricular material — most curricula either romanticise persistence or vilify it — and both readings miss the discipline.

The grind protocol has three components: **the signal watch**, **the coalition-tracker refresh**, and **the exit criteria**.

### The signal watch

A grinding bet is a bet that is *waiting on a specific signal* to move. The signal is enumerated on the coalition tracker's *shift signals* column (chapter 4) and cross-referenced with the mod-502 chapter 6 signal-tracking cycle. Examples:

- A benchmark result from a pending eval that would clarify the technical direction.
- A competitor move that would either de-risk or de-motivate the bet.
- A CFO cycle boundary that would clarify the capacity envelope.
- A regulatory clarification that would resolve a Head of AI Governance objection.
- A peer platform-side principal's substrate maturation that would unblock the seam.

The signal is *specific and observable*. Not *"more clarity"* — *"the FY26 CFO cycle completing on YYYY-MM-DD, at which point the capacity envelope resolves"*.

### The coalition-tracker refresh

While a bet is grinding:

- The coalition tracker's rows for this bet are refreshed on the standing 1:1 cadence.
- New shift signals surfaced in 1:1s are added.
- Stakeholders whose position has shifted (even if only slightly) are updated.
- The *last touched* column on every row is refreshed by contact.
- Rows that have not been touched for two cycles are re-audited: is the stakeholder still relevant to this bet, or has their org's relationship to the bet changed?

### Exit criteria

A grinding bet exits grind mode in one of three ways:

1. **The signal arrives and the bet becomes ratifiable.** Return to chapter 4 stage C (the decision-room).
2. **The signal arrives and the bet becomes un-ratifiable.** Move to section §5 (dead-scope discipline).
3. **The signal does not arrive within the bet's window.** Move to section §4 (defer).

The failure mode is *grinding without an exit criterion*. A bet that has been grinding for two cycles without a named exit criterion is a bet in *silent dead scope*. Section §5 is the corrective.

## §4 — The deferred-decision artifact

Defer is the outcome most curricular material treats as failure. It is not. Defer is the *ratified statement* that the org is not yet ready for the bet, with a *named revisit condition* that keeps the bet alive across cycles. A ratified deferral is the discipline that separates a defensible principal from one whose portfolio is littered with bets nobody remembers.

### Purpose

The deferred-decision artifact exists to answer three questions, at the next cycle:

1. **What was decided last cycle?** *"This bet was deferred, not killed."*
2. **What would make us re-open it?** *"The specific revisit condition — a named external signal, a named internal state change, a named date — that triggers the re-open."*
3. **Who owns the revisit?** *"The IC-principal, in partnership with the CAIO, per the annual strategy refresh cycle. The next scheduled check-in is <date>."*

Without the artifact, the deferral becomes dead scope by default — the next cycle's principal (or the next cycle's version of the same principal) does not remember the bet and does not revisit it. The artifact is a *memory instrument*.

### Shape

A short document, one to two pages, stored in a canonical location (the same location the strategy and the reference architecture ship to, per mod-503 chapter 5 § *single canonical location*). Sections:

- **The bet.** One paragraph. What was being considered.
- **What was the ratified decision.** One sentence. *"Deferred pending <revisit condition> until <date>."*
- **Who ratified.** The peer executive counterparts (chapter 3) present at the decision. The coalition tracker's row for this decision.
- **Why deferred, not killed.** One paragraph. The specific reasons the bet is worth carrying forward — the strategic value, the org's likely readiness horizon, the cost of *not* carrying it.
- **The revisit condition.** Specific and observable. Not *"when the org is ready"* — *"when the FY27 CFO cycle boundary lands, or when the responsible-AI review body issues its Q3 refresh, whichever is earlier"*. Multiple revisit conditions are fine; each is enumerated.
- **The revisit owner.** The IC-principal is the modal owner; the CAIO is the modal co-owner. Named.
- **The revisit cadence.** How often the artifact is *touched* — the standing bi-weekly with the CAIO, the monthly strategy refresh 1:1, the quarterly review. Named.
- **The dead-scope trigger.** Section §5's discipline: the specific condition under which this deferral becomes dead scope and is closed. Not *"if we lose interest"* — *"if the strategic value evaporates because <specific>, or if the revisit condition is confirmed impossible because <specific>, or if two consecutive cycles pass without progress on the revisit signal"*.

### The revisit condition — writing discipline

The revisit condition is the load-bearing sentence of the artifact. It is what makes the deferral survive.

- **Specific.** Not *"when we have more data"* — *"when the FY27 Q1 eval-set refresh includes <specific benchmark>"*.
- **Observable.** Not *"when the market is ready"* — *"when a competitor ships a comparable capability, or when our customer research indicates <specific signal>"*. Signals the org would *notice* in the ordinary course of business, or signals the mod-502 chapter 6 signal-tracking cycle is watching for.
- **Time-bounded.** Not *"eventually"* — *"by FY27-Q2, or the deferral is re-evaluated for dead-scope"*.
- **Multiple where appropriate.** A bet with three plausible re-open paths is a bet with three revisit conditions, any of which triggers. Enumerate.

### The revisit cadence — practice

- **Standing check-in on the 1:1 cadence.** The bi-weekly with the CAIO (chapter 3) walks the deferred-decision log for two-to-three minutes. Bets whose revisit conditions are approaching get flagged.
- **Semi-annual full walk-through.** At the strategy refresh cycle (mod-502 chapter 5), the deferred-decision log is walked in full. Bets whose revisit conditions have triggered move back into the coalition sequence; bets whose dead-scope triggers have activated move to dead scope.
- **The artifact is refreshed with every touch.** Notes on the current state of the revisit signal. Notes on the state of the four peer executives' portfolios that would affect the bet. Notes on the mod-502 signal-tracking cycle's read on the bet.

## §5 — Dead-scope discipline

Some bets are not deferred. They are *dead*. A bet becomes dead when:

- The revisit condition has been proven unlikely or impossible.
- The strategic value has evaporated (the underlying opportunity has passed).
- The org's direction has moved and the bet is no longer coherent with the strategy.
- The bet has been in defer state for more than two full strategy-refresh cycles without progress on the revisit signal.

Dead-scope discipline is *closing* the bet — moving it from the deferred-decision log to a *dead-scope log* — and *not carrying its memory cost forward*. Every bet on the deferred-decision log has an ongoing cost: the standing check-in time, the artifact-maintenance overhead, the working-memory occupancy in the principal's and the CAIO's minds. Bets that are dead soak that cost with no chance of return.

### Closing a bet — protocol

- **Draft the close-out note.** One paragraph on the deferred-decision artifact: *"On <date>, this bet was closed to dead scope because <named reason>. The revisit condition <named> did not materialise; the strategic value has evaporated because <named>."*
- **Ratify the close in the standing 1:1 with the CAIO.** The CAIO is the modal co-owner; they co-close.
- **Note it in the semi-annual strategy refresh.** The deep-dive companion's *open questions and known unknowns* section (mod-502 chapter 7) absorbs closed bets so the reader can trace the history.
- **Move the artifact to the dead-scope log.** The artifact is not deleted; it is *archived*. If the same bet resurfaces in a future cycle, the archived artifact is the pre-mortem the next-cycle principal can draw on.

### When to reopen a dead bet

A bet in dead scope can be re-opened if:

- A material signal shifts the fundamental read. Not marginal — material.
- The strategic value returns because the org's direction moved back to the frame the bet was originally coherent with.
- A peer executive-branch counterpart brings new information that changes the read.

A re-open is a *conscious decision*, not a drift. The re-open triggers a new coalition sequence (chapter 4) — this is a new bet, sharing history with an old one, not a resumption.

## §6 — The escalation-and-deferral log

A single document that carries the state of every current-cycle escalation, grind, and deferred decision. The log is the artifact-side of this chapter, in the same spirit as the coalition tracker (chapter 4 §2) is the artifact-side of chapter 4.

### Schema

One row per material bet-related decision. Columns:

| Column | What it holds |
| ------ | ------------- |
| **Decision title** | Short (~10 words) — what is being decided. |
| **Associated bet** | The mod-502 portfolio row this decision affects. |
| **State** | *Escalate* / *Grind* / *Deferred* / *Dead*. Chosen and named. |
| **Sub-state (per state)** | For *Escalate*: pre-brief-done / in-flight / decided. For *Grind*: current signal watch. For *Deferred*: revisit condition and date. For *Dead*: close date and reason. |
| **Peer executives involved** | The four (chapter 3) subset relevant. |
| **Coalition-tracker cross-reference** | The row(s) in the coalition tracker (chapter 4 §2) that carry the stakeholder detail. |
| **Last touched** | Date. |
| **Next action** | The single specific next action, with a named owner and date. |

### Discipline

- **The log is walked on the standing 1:1 cadence.** The bi-weekly with the CAIO includes a look at the log for two-to-three minutes. Slipping or drifting items get flagged.
- **The log is refreshed with every touch.** State-change happens *explicitly* — a grind that becomes a defer is a log-edit, not a silent drift.
- **The log is short.** Twenty-five to forty rows total, across all four states, across the current-cycle portfolio. A log with a hundred rows has absorbed items that should be in dead scope.
- **The log is shared with the four peer executive counterparts.** Chapter 3 § *artifact flow* extends here. Each peer sees the escalations and deferrals that involve them.
- **The log persists across cycles.** Rows do not disappear when they close; they move to the archived-decisions section of the log. The archive is the memory instrument.

### What the log is *not*

- **Not a to-do list.** The log is a *state document*. Tasks live on the coalition tracker.
- **Not a personnel review.** Peer executives whose positions get over-ridden by an escalation are not annotated with the outcome; the log is neutral. The follow-up 1:1 (section §2) is where the partnership contract absorbs the outcome.
- **Not the escalation artifact itself.** The log points at the escalation artifact; it does not contain it. Escalation artifacts (section §2) are one-to-two-page documents; the log is one row per.

## Summary

- Every cross-org disagreement at principal altitude resolves into one of three states: escalate, grind, or defer. The single most useful discipline is *naming the state*. A bet whose state is uncertain is a bet whose next move is under-determined.
- Escalation is expensive. Five conditions gate whether to escalate; four sections author the escalation artifact; the pre-briefing of the four peer executive counterparts (chapter 3) is what makes the escalation constructive rather than partnership-breaking. Modal cadence is two escalations per fiscal year; ten is a sign the partnership contracts are failing.
- Grind is the mode of a bet waiting on a specific, observable signal. The signal watch, the coalition-tracker refresh, and the exit criteria are the discipline. Grinding without an exit criterion is silent dead scope.
- Defer is a *ratified* outcome, not a failure. The deferred-decision artifact makes the deferral survive across cycles — the revisit condition is the load-bearing sentence, specific and observable and time-bounded. The four peer executive counterparts can name the deferral in one sentence.
- Dead-scope discipline closes deferrals that are no longer worth the memory cost. The close is explicit, ratified with the CAIO, and noted in the semi-annual strategy refresh.
- The escalation-and-deferral log carries the state of every current-cycle decision. Shared with the four peer executives; walked on the standing 1:1 cadence; refreshed with every touch. Persists across cycles as a memory instrument.
- This chapter closes the module. Exercise-04 authors the escalation log, one worked escalation, and one deferred-decision artifact. Chapter 4's coalition tracker, chapter 5's FAQ, and chapter 3's partnership contracts are the artifact system this chapter's protocol runs through.
