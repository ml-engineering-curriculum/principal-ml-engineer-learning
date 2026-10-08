# exercise-03: Calibrate a Staff-Plus Hiring Loop End-to-End

**Estimated effort:** 3 hours

## Objective

Instantiate chapter 3's practice on one specific staff-plus hiring loop: author the loop-chair coaching plan (chapter 3 § *coaching the loop chair*), author the rubric-based principal-track interview design (chapter 3 § *the rubric-based principal-track interview*), author the debrief protocol the loop will run (chapter 3 § *the four calibration decisions*), and author the one-page bar-raising interview-change proposal (chapter 2 § Class C) the review will ratify. Four artifacts, each sitting on a different seam of the staff-plus-loop machinery.

The exercise does *not* ask you to run an actual loop. It asks you to produce the artifacts a principal would carry *into* a loop: the pre-loop coaching plan for the chair, the interview design, the debrief protocol, and the leverage-move proposal the pattern feeds. In production the loop runs; the artifacts are what pre-exist it.

## Prerequisites

- **Chapter 3 read end-to-end.** The seam with `staff-ml-engineer-learning` mod-410 exercise-03 (individual-interview design is their scope; loop-level calibration is yours), the staff-plus loop structure, the four calibration decisions (hire / no-hire from ratings shape, level from verb-object, bar-clear vs. role-fit, loop-quality), the four coaching beats, the rubric-based principal-track interview kinds, and the five failure modes.
- **Chapter 2 § *Class C — the bar-raising interview change*.** The leverage-move class the fourth artifact instantiates. Chapter 2's class-C selection discipline and co-author discipline both apply.
- **Mod-501 chapter 1 (verb-and-object vocabulary).** The verb-object table is the substrate for the staff-vs-principal level call. Without it, the principal-track interview rubric is impressionistic.
- **Mod-501 chapter 2 (reading a principal posting).** The signal-reading practice applied to a candidate's portfolio is directly adjacent to the probing discipline the principal-track interview applies in the room.
- **[`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-03.** The staff-scope interview-design exercise the mentee / loop chair you are coaching has probably done (or should have). Reading it before you coach is what keeps the seam clean.
- **Optional: an actual req you have in flight.** If the ML org has an open staff-plus req you are the calibrator on, write the exercise against that req. If not, be explicit about the composite — one named band (Principal), one named scope (e.g., Gen-AI product org), one named rubric axis set.

## Problem statement

Pick a staff-plus hiring loop (real or composite). Specify the band (Staff / Senior Staff / Principal / Sr. Principal / Distinguished), the role scope (Gen-AI, RecSys, platform, ML security — pick one), the number of interviews (5–7), and the current loop-chair's experience (new chair, 2 prior loops, 4+ prior loops). Produce four artifacts.

- **The loop-chair coaching plan.** The pre-loop 1:1, the silent-debrief playbook, the post-loop 1:1 agenda. Chapter 3 § *coaching the loop chair* four-beat structure, specialised to this chair's experience level and the specific candidate on-paper profile.
- **The rubric-based principal-track interview design.** The specific interview (one of: portfolio deep-dive at principal altitude, org-scope architecture-and-tradeoffs, cross-org-influence behavioural — pick one), with its rubric, its calibration anchors (what *staff* evidence looks like vs. what *principal* evidence looks like), its 60–75 minute agenda, and its scoring instructions.
- **The debrief protocol.** The agenda, the rules of engagement, the specific sequencing of the four calibration decisions, the rubric for the staff-vs-principal split call, the escalation path if the loop deadlocks.
- **The Class C bar-raising interview-change proposal.** The one-page change proposal that this loop's calibration will ratify — current state of the interview or rubric, the specific gap, the proposed change, the evidence from the debrief, the migration plan. Chapter 2 § *Class C how to author it* is the pattern reference.

The four artifacts together constitute the principal-side preparation for one well-run staff-plus loop plus the one Class C leverage-move output chapter 3 § *loop-quality decision follow-up* names. They are also the artifacts chapter 6 § *committed-leverage-move check* audits against if Move 1 or Move 2 (exercise-02) is a Class C move.

## Requirements

Populate a workspace directory `exercise-03-staff-plus-loop-calibration/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-03-staff-plus-loop-calibration/
├── README.md                       # index; loop profile (band, scope, chair, candidate)
├── loop-chair-coaching-plan.md     # four-beat chapter 3 § *coaching the loop chair* arc
├── principal-track-interview.md    # the specific rubric-based interview design
├── debrief-protocol.md             # the agenda and decision sequencing
├── class-c-change-proposal.md      # the one-page Class C bar-raising interview-change
└── appendices/
    ├── level-decision-rubric.md    # verb-object table instantiated for this req
    └── anti-trap-checklist.md      # the five failure modes mapped to this loop's risks
```

### `loop-chair-coaching-plan.md` — the four-beat arc

Chapter 3 § *coaching the loop chair* is the reference. The plan is written for this specific chair at their specific experience level; chapter 3 is explicit that coaching a new chair looks different from coaching an experienced one. 2–3 pages.

- **Chair profile — 3–5 lines.** Named engineer, L-band, prior loop count, prior calibration gaps (if observed in prior loops), their current staff-plus-loop role (chair of this loop, loop participant on other loops, etc.).
- **Candidate on-paper profile — 3–5 lines.** The candidate's portfolio shape (what the resume and the pre-interview materials say), the req band (what the hiring committee set), the specific gaps you expect the loop to probe (e.g., *"candidate has 12 years of staff-scope evidence; req is Principal — the gap is whether the candidate's own verb has landed on org-and-industry-scope objects"*).
- **Beat 1 — the pre-loop 1:1 (30 minutes).** Agenda for the 1:1 with the chair before the loop runs. Specific questions you will ask (chapter 3 § *beat 1*: *"which axes are load-bearing for this req? which are check-the-box? how will you handle the strong-coding / weak-design split?"*). Explicit framing of the staff-vs-principal call per the verb-object table (`appendices/level-decision-rubric.md` reference).
- **Beat 2 — silent debrief attendance.** What you are watching for during the chair's debrief. Chapter 3 § *beat 2*: does the chair steer onto the rubric or the vibes; does the chair surface the quiet interviewer's read; does the chair force the level call as sharply as the hire call. A specific list of 4–6 behaviours you are observing silently and taking notes on.
- **Beat 3 — targeted intervention (if required).** The two or three specific situations in which you would speak (loop about to make an indefensible call; deadlock the chair has openly asked for help with). The *absent-you effectiveness* test chapter 2 § *leverage property 2* applies — your default is silence.
- **Beat 4 — the post-loop 1:1 (20–30 minutes, within 2 working days).** Agenda. What went well, what the chair would do differently, which of the four calibration decisions was hardest, whether any pattern from this loop is a Class C leverage-move candidate (which feeds `class-c-change-proposal.md`). Explicit coaching on *decision quality*, not on *procedural mimicry* of your style (chapter 3 § *failure mode 5*).

Constraint: the coaching plan is written to this chair, not to the generic chair. If you cannot personalise it to the chair's experience and the candidate's profile, the loop will land in the generic-coaching trap chapter 3 § *failure mode 5* names.

### `principal-track-interview.md` — the specific interview design

Chapter 3 § *the rubric-based principal-track interview* names three kinds; pick one and author it in full. 2–3 pages.

- **Interview kind — one line.** Portfolio deep-dive at principal altitude, org-scope architecture-and-tradeoffs, or cross-org-influence behavioural. Note which one and why this one fits this specific req (chapter 3 § *the staff-vs-principal call, specifically* names the common patterns).
- **Interview length — 45–75 minutes.** With the specific minute budget per section (10 min intro, 45 min walk-and-probe, 10 min candidate Q&A, 10 min scribing).
- **Pre-read.** What the interviewer reads before the interview. For a portfolio deep-dive, the specific artifact the candidate has submitted and the specific sections the interviewer should probe. For an org-scope architecture-and-tradeoffs, the prompt the candidate has 30 minutes to prepare and the solution-space notes the interviewer should hold in mind. For a cross-org-influence behavioural, the 2–3 stories the candidate has pre-flagged in the pre-interview questionnaire.
- **The rubric — 4–6 axes.** Each axis has: an axis name, a *staff* anchor (what landing at staff altitude looks like on this axis), a *principal* anchor (what landing at principal altitude looks like on this axis), the specific probing questions that elicit the differentiating signal, and the scoring convention (clearly-staff / staff-with-stretch / clearly-principal / principal-with-weakness / no-decision).
- **The verb-object anchor.** Mod-501 chapter 1's verb-object table is the substrate. The rubric should explicitly cite the principal-scope verbs (*coach L40 engineers*, *multiply the effectiveness of every ML team*, *set the technical bar*, *influence cross-org without authority*) and ask: *does the candidate's own verb reliably land on the principal-scope objects named in the table?*
- **Anti-trap guidance.** Three to five explicit traps the interviewer should guard against (chapter 3 § *the four calibration decisions* names: pleasantness-as-hire-signal, years-as-level-proxy, *they'd stretch into principal*, charisma-narrative over artifact-and-mechanism). Each trap gets one line of guidance.
- **Scribing shape.** What the interviewer writes down during and after the interview. For each rubric axis, a one-sentence summary of the candidate's evidence; a direct quote (where notable); a scored anchor. Scribing shape is what makes the debrief defensible rather than impressionistic.

Constraint: the rubric must *differentiate*. If both the *staff* anchor and the *principal* anchor read as "candidate reasons well about tradeoffs," the rubric has not landed — the axis is too generic. The rubric only pays if a staff-level candidate and a principal-level candidate would score visibly differently on it.

### `debrief-protocol.md` — the agenda and decision sequencing

Chapter 3 § *the four calibration decisions* is the content; the protocol is the ritual. 1–2 pages.

- **Debrief timing and length.** Within 24–48 hours of the last interview, 90 minutes, chair-led. Pre-read of all interviewer notes required.
- **Agenda — ordered.**
  1. **Chair reads out the shape of ratings** (chapter 3 § *decision 1 signal*). Not the average; the shape. Which interviews cleared cleanly; which cleared with a caveat; which produced a no-decision.
  2. **Each interviewer presents their interview's evidence** (not the rating first; the evidence). 5 minutes each. The rubric drives the evidence; the evidence drives the rating.
  3. **Open discussion — hire / no-hire** (chapter 3 § *decision 1*). The chair steers the discussion onto the rubric; names the specific interview evidence that drives each voice's read.
  4. **Open discussion — level (staff / senior staff / principal / sr. principal / distinguished)** (chapter 3 § *decision 2*). The chair forces the staff-vs-principal call per the verb-object anchor (`appendices/level-decision-rubric.md`). The chair guards against the *years-as-proxy* and *stretch* anti-patterns explicitly.
  5. **Bar-clear vs. role-fit** (chapter 3 § *decision 3*). If the loop is a hire, is this the right hire for *this* req? If not, is the candidate bar-clear for a different req the org is running?
  6. **Loop-quality check** (chapter 3 § *decision 4*). Did every interview produce the evidence it was designed to? Did any interview run shallow? Does the loop need an add-on, or is the evidence sufficient?
  7. **Chair writes the recommendation** (in-meeting first draft). The hire / no-hire, the level, the bar-clear-vs-role-fit note, the loop-quality notes, the escalation (if any) to the hiring committee. The draft is read back to the room before the meeting ends.
- **Rules of engagement.**
  - No averaging ratings (chapter 3 § *failure mode 2*).
  - No pleasantness-as-hire-signal (chapter 3 § *decision 1 trap*).
  - No *"let's hire and let promo sort the level"* (chapter 3 § *failure mode 4*).
  - Rubric-first: every claim is grounded in rubric-axis evidence.
  - Chair holds the room; the principal is silent unless chapter 3 § *beat 3* fires.
- **Escalation to the hiring committee.** If the loop deadlocks (chapter 3 § *decision 1 escalation path*), the chair writes a one-page summary that names the split and the specific evidence each side reads. The escalation is written and shared with the committee; verbal escalation is not sufficient.
- **The post-loop coaching trigger.** Any one of the four calibration decisions that was hardest for the chair is a `loop-chair-coaching-plan.md` § beat 4 agenda item. Any pattern that recurs across loops (chapter 3 § *decision 4 follow-up*) is a `class-c-change-proposal.md` candidate.

Constraint: the protocol is for *this chair* at *this loop*. The modal failure is a generic protocol copy-pasted across loops; the specifics (chair experience, candidate profile, req band) should visibly shape at least two of the agenda items.

### `class-c-change-proposal.md` — the leverage-move proposal

One page. Chapter 2 § *Class C how to author it* is the pattern reference. This artifact is where the loop's calibration becomes a durable org-wide change — the single most repeatable principal-side output of a well-run loop series.

- **Working title.** 10–15 words. *"Portfolio-deep-dive rubric v2: add explicit coaching-verb probing per mod-501 chapter 1."* Not *"improve the deep-dive."*
- **Current state.** One paragraph. The specific interview or rubric the proposal changes, as it currently stands. Grounded in the debriefs that surfaced the gap — ideally more than one loop (3 loops in a quarter is the chapter 2 § *Class C how to author it* reference pattern).
- **The gap.** One paragraph. The specific calibration gap the current state produces (e.g., *"three of six portfolio deep-dives in Q3 did not probe the mod-501 chapter 1 *coach* verb, resulting in three level calls where the staff-vs-principal evidence was weaker than the rest of the loop supported"*). Grounded in named debriefs, not impression.
- **Proposed change.** One paragraph. The specific rubric axis addition, the specific interviewer-training change, or the specific scoring-anchor update. Specific enough that an interviewer could run the new version next week.
- **Evidence.** Two or three bullets. The named debriefs or the named loop-outcome signals that justify the change.
- **Migration plan.** One paragraph. Who trains on the new rubric; when it goes live (first trial loops in month 1, ratification session in month 2, org-wide default in month 3); who runs the ratification session (hiring committee chair with the principal and 1–2 loop chairs as co-authors); when it is re-reviewed (6 months post-launch).
- **Co-authors.** Named explicitly. Chapter 2 § *Class C how to author it* names the shape: hiring committee chair plus 1–2 loop chairs who have run enough loops to see the gap first-hand.
- **Landing criteria.** Reproduced from chapter 2 § *Class C how you know it landed*: 6 months (interviewers cite the change by name in debriefs); 12 months (at least one hiring decision flipped because of the new rubric); 24 months (new hires on the far side are visibly stronger on the targeted axis).

Constraint: one page. If the proposal needs two pages, it is a program — split into a core change (one page) and a program note (separate artifact outside this exercise's deliverable set).

### `appendices/level-decision-rubric.md` — the verb-object table instantiated

Half a page to one page. The mod-501 chapter 1 verb-object table reduced to this req's level call.

- **The principal verbs** that this req is hiring on (coach, multiply, set, influence) with the specific principal-scope objects at this org (the ML org's technical direction, the north-star architecture, the technical bar, the cross-org influence up to SVP / CTO).
- **The staff verbs and objects** this candidate is likely to already demonstrate (own, lead, design, architect) with the staff-scope objects (the multi-team blueprint, the portfolio-scope RFC, the portfolio TCO).
- **The *same verb, different object* distinction.** The modal confusion is a candidate whose verb and object both *sound* like principal evidence but, on probing, reduce to staff-scope evidence (chapter 3 § *the staff-vs-principal call, specifically*). The appendix names 2–3 specific *same verb, different object* traps for this req.

Constraint: this is the rubric the chair uses to force the level call. If the appendix is generic — if it reads the same for every req — it is not calibrated to this loop and will not land.

### `appendices/anti-trap-checklist.md` — the five failure modes

Half a page. Chapter 3's five failure modes mapped to this specific loop's risks.

For each of the five failure modes (sitting on every loop, averaging ratings, confusing bar-clear with role-fit, deferring the level call, coaching the chair into your style), name one specific way this loop could fall into that mode and one specific guard against it.

Constraint: the checklist is specific to this loop. If the guards are generic (*"keep an eye on it"*), rewrite them.

## Starter guidance

- **Pick a real loop if you have one.** The exercise's fidelity scales with the specificity of the inputs. A real loop with a named chair, a named candidate (anonymised fine), and a specific band produces artifacts that are 10x more useful than a generic composite.
- **Author the principal-track interview design before the coaching plan.** The coaching plan references the interview; if the interview is not fully designed first, the coaching plan will handwave. Chapter 3 § *the rubric-based principal-track interview* is the substrate; the coaching plan sits on it.
- **The rubric is the artifact — do not substitute vibes.** The modal failure of a principal-track interview is a rubric that reads well on paper but does not differentiate in practice. If you cannot write a *staff* anchor and a *principal* anchor for the same axis that would score visibly differently on the same candidate, the axis is not calibrated — redesign it.
- **The chair is who grows; the hire is the by-product.** Chapter 3 § *coaching the loop chair* is explicit on the hierarchy of outcomes. The hire is the loop's immediate output; the chair's growth is the principal's durable output. Write the coaching plan accordingly — it is the longer-horizon artifact.
- **The Class C proposal grows out of the debrief, not the other way around.** If the proposal is pre-written and the debrief is reverse-engineered to support it, chapter 2 § *failure mode: measured on activity* is the parent anti-pattern. Draft the proposal from the actual debrief evidence (or honestly flagged *potential* debrief evidence if the loop is composite).
- **Interact with exercise-02 explicitly.** If one of exercise-02's committed moves is Class C, the proposal here is where its substance lives — same artifact, different workspace. Cross-reference. If exercise-02's committed moves are not Class C, the proposal here is a candidate for the option list (exercise-02 § `option-list.md`) with a specific threshold criterion.
- **Time-box each artifact.** Coaching plan: 45 minutes. Principal-track interview design: 60 minutes (this is the most-worked artifact). Debrief protocol: 30 minutes. Class C proposal: 30 minutes. Appendices: 15 minutes each. Total: roughly 3 hours. If you exceed 4 hours, you are over-authoring one of the artifacts.

## Acceptance criteria

The exercise is done when:

- [ ] `README.md` names the loop's band (Staff / Senior Staff / Principal / Sr. Principal / Distinguished), the role scope, the number of interviews, and the chair's prior-loop experience.
- [ ] `loop-chair-coaching-plan.md` is personalised to this chair's experience level — the plan for a 2-loops chair would be visibly different from the plan for a 4+-loops chair.
- [ ] The coaching plan covers all four beats (pre-loop 1:1, silent debrief, targeted intervention, post-loop 1:1) with specific agendas, specific questions, and specific behaviours to observe.
- [ ] `principal-track-interview.md` picks one of the three interview kinds and authors it in full — length, pre-read, rubric, verb-object anchor, anti-trap guidance, scribing shape.
- [ ] Each rubric axis has distinct *staff* and *principal* anchors that would score visibly differently on the same candidate.
- [ ] The verb-object anchor cites mod-501 chapter 1's table explicitly and names the principal-scope objects this req probes for.
- [ ] `debrief-protocol.md` is specific to this chair and candidate — generic protocols are rewritten before submission.
- [ ] The protocol's agenda sequences the four calibration decisions in the chapter 3 order (hire / no-hire → level → bar-clear vs. role-fit → loop-quality).
- [ ] The protocol's rules of engagement include at least chapter 3's four anti-traps (no averaging, no pleasantness-as-hire, no *stretch-into-principal*, no deferring the level call).
- [ ] `class-c-change-proposal.md` fits on one page and includes current state, gap, proposed change, evidence, migration plan, named co-authors, and landing criteria.
- [ ] The proposal's landing criteria are reproduced from chapter 2 § *Class C how you know it landed* with specialisation to this proposal's scope.
- [ ] `appendices/level-decision-rubric.md` names the principal verbs, principal objects, staff verbs, staff objects, and at least 2–3 *same verb, different object* traps specific to this req.
- [ ] `appendices/anti-trap-checklist.md` maps each of chapter 3's five failure modes to a specific risk and a specific guard for this loop.
- [ ] The exercise passes the *coaching-plan ownership test*: another principal reading `loop-chair-coaching-plan.md` could coach the same chair without your presence. If they could not, the plan is impressionistic.
- [ ] The exercise passes the *rubric-differentiation test*: for each principal-track interview rubric axis, you can describe one specific candidate response that would score at the *staff* anchor and one that would score at the *principal* anchor.
- [ ] The exercise passes the *drift-mode check*: none of chapter 3's five failure modes are visible in the artifacts (sitting on every loop, averaging ratings, confusing bar-clear with role-fit, deferring the level call, coaching the chair into your style).

## Stretch goals

- **Run the pre-loop 1:1 with a real peer.** Ask a staff engineer or peer principal to play the chair. Walk through `loop-chair-coaching-plan.md` § beat 1 live. Their pushback on your questions is the fastest way to find the questions that are too generic.
- **Author the add-on-interview protocol.** If `debrief-protocol.md` § decision 4 (loop-quality) determines the evidence is insufficient, what does the add-on interview look like? One page: the specific gap it fills, the specific interviewer who runs it, the specific candidate-ask, the timeline. Chapter 3 § *decision 4 action* is the parent reference.
- **Pair this exercise with the mod-410 exercise-03 (staff-scope interview design).** Draft the mod-410 exercise-03 artifact for the specific interview `principal-track-interview.md` covers — i.e., the staff-scope version of the same interview. The comparison surfaces exactly what the principal-scope rubric adds. If the two artifacts read identically on paper, one of them is not at the right altitude.
- **Design the second-order chair-coaching artifact: the loop-chair training program.** If 3+ chairs you have coached have shown the same gap, a chair-training program is a Class C candidate at the chair-population level. One page: the program's goal, the modal gap, the training shape, the certification criterion, the ongoing cadence. This is a different Class C change than the per-interview rubric change.
- **Compose with exercise-04 (review bar + escalation charter).** If a hiring loop deadlocks and escalates to the hiring committee, the escalation artifact shape is identical to the chapter 4 § *escalation artifact* shape — trigger, local-state, specific-question, named-decision-date. Author the hiring-committee-escalation artifact for a composite deadlock scenario; use it as a cross-exercise test.
- **Author the *loop-chair handoff* document.** When a loop chair's rotation ends and a new chair steps in, what artifact does the outgoing chair hand the incoming chair? One page: the loops the outgoing chair ran, the calibration patterns they observed, the Class C proposals they flagged, the open coaching threads with the principal. This is the chair-coaching equivalent of chapter 6's personal-cadence artifact for chairs.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-03-staff-plus-loop-calibration/` is what you extend across loops over the fiscal year: each new loop adds to the chair-coaching plan's longitudinal view; each Class C proposal that ratifies lands into the organisation's canonical interview-and-rubric bank; the debrief protocols stack into a chair-handoff artifact (stretch goal 6). If one of exercise-02's committed leverage moves is Class C, `class-c-change-proposal.md` is where its substance lives; otherwise it lands on exercise-02's option list.
