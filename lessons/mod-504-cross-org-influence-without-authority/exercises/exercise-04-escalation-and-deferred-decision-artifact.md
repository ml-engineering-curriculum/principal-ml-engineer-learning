# exercise-04: Escalation Protocol, Worked Escalation, and Deferred-Decision Artifact

**Estimated effort:** 3 hours

## Objective

Author the three artifacts that close chapter 6's protocol into an operable system: (1) the *escalation protocol document* that names when and how you escalate a cross-org disagreement, (2) *one worked escalation* taken end-to-end for a specific bet from your mod-502 portfolio, and (3) *one deferred-decision artifact* with the revisit criteria that keeps it from becoming dead scope. The output is the shelf of artifacts a principal needs on hand before a bet starts drifting.

Chapter 6 named the three-way question every cross-org disagreement resolves into — *escalate*, *grind*, *defer* — and the artifacts that carry each state. This exercise authors the templates and one lived instance each for escalate and defer. The grind protocol is a lightweight state in chapter 6; exercise-03's coalition tracker is where grind lives. Here you build what happens when grind runs out.

## Prerequisites

- **Mod-504 chapter 6 read end-to-end.** All six sections — the three-way question, escalation protocol, grind protocol, deferred-decision artifact, dead-scope discipline, the escalation-and-deferral log.
- **Mod-504 chapters 3 and 4 read end-to-end.** The partnership contracts (chapter 3) are the structure the escalation routes through; the coalition tracker (chapter 4) is the input to the escalation-and-deferral log.
- **Exercises 01, 02, and 03 complete.** The FAQ's *deferred* entries from exercise-01, the escalation paths from exercise-02's partnership contracts, and the shift-signals / slipping-commits from exercise-03's trackers are the inputs this exercise processes.
- **Mod-502 chapter 6 skimmed.** The signal-tracking cycle is where the revisit conditions for deferred decisions are watched.
- **Mod-503 chapter 7 skimmed.** The org-wide architecture review body is one of the modal venues the escalation protocol runs under.

## Problem statement

Chapter 6 § *the three-way question* names a discipline most first-cycle principals never acquire — the discipline of *naming the state* a bet is in before deciding what to do about it. First-cycle principals default to grind; second-cycle principals over-correct into escalation and burn the partnership contracts; third-cycle principals discover that defer is a valid, honorable outcome and start using it, and immediately discover that most orgs treat *defer* as *dead* unless the artifact prevents it.

Your job on this exercise is to author the artifact system that makes the state-naming discipline enforceable:

- The *escalation protocol* document the principal's team can read cold — when to escalate, how to escalate, what the artifact shape is, what post-escalation discipline looks like, what the escalation budget is.
- *One worked escalation* — a complete escalation artifact for a specific disagreement on a bet from your mod-502 portfolio, as if you were about to walk it into a CTO's or CEO's calendar next week. The artifact is one to two pages; the exercise walks the shape chapter 6 §2 named.
- *One deferred-decision artifact* — for a different bet (or a different clause of the same bet), the artifact that keeps the deferral alive across cycles. Chapter 6 §4 is the shape.
- The *escalation-and-deferral log* that carries the state of every current-cycle decision. Chapter 6 §6 is the schema.

These four together are what chapter 1's defensibility test 5 (*escalation-and-deferral discipline*) grades.

## Requirements

Populate a workspace directory `exercise-04-escalation-and-deferral/`. Suggested layout:

```
exercise-04-escalation-and-deferral/
├── README.md                             # scope and cross-references to prior exercises
├── escalation-protocol.md                # the principal's team-facing protocol document
├── worked-escalation/
│   ├── 00-context.md                     # the bet, the parties, the deadlock
│   ├── 01-escalation-artifact.md         # the chapter 6 §2 one-to-two page artifact
│   ├── 02-pre-brief-plan.md              # pre-briefing the four peer executives
│   ├── 03-meeting-run-sheet.md           # the 15–30-minute escalation meeting
│   └── 04-post-escalation-24h-memo.md    # the memo that lands within 24 hours
├── deferred-decision/
│   ├── 00-context.md                     # the bet, the readiness gap, why defer
│   ├── 01-deferred-decision-artifact.md  # the chapter 6 §4 document
│   └── 02-revisit-cadence-plan.md        # how the deferral stays alive
├── escalation-and-deferral-log.md        # chapter 6 §6 schema; at least 8 rows
└── pre-mortem.md                         # chapter 6 § *escalation is expensive* applied to this cycle
```

### `README.md` — scope

- Which mod-502 bet or portfolio row the worked escalation is on, and which bet the deferred-decision artifact is on. Keep them distinct; the two artifacts should not resolve the same disagreement.
- The cross-references to exercises 01, 02, and 03 — which FAQ entries, which partnership-contract escalation paths, which coalition-tracker shift signals and slipping commits feed this exercise.
- One paragraph on scope: this exercise is *authorship*, not *running*. Chapter 6 § *escalation is expensive* is honoured by *not* actually walking an escalation; the artifact is the acceptance test.

### `escalation-protocol.md` — the team-facing protocol document

Chapter 6 §2 is the content minimum. This document is what you hand to a new ML-function staff engineer so they understand how the principal handles cross-org disagreements and why. Sections:

1. **The three-way question** — one paragraph. Escalate, grind, defer. Chapter 6 §1 § *which of the three states is this in?* is the model. Why state-naming is the load-bearing move.
2. **Pre-conditions for escalation** — chapter 6 §2 § *pre-conditions* enumerated. The five criteria (specific decision, named parties, prior-attempt-at-technical-layer, right-altitude escalator, deadline grinding cannot make).
3. **The escalation artifact shape** — chapter 6 §2 § *the escalation artifact* — all eight sections: the decision, the parties, why-not-resolvable-at-technical-layer, what-each-resolution-means, what-the-principal-recommends, what-the-peers-recommend, the deadline, the follow-up.
4. **The escalation meeting shape** — chapter 6 §2 § *the escalation meeting*. The 15–30 minute meeting, the roles (escalator, parties, principal), the ratification cadence.
5. **Post-escalation discipline** — chapter 6 §2 § *after the escalation*. The 24-hour memo, the follow-up 1:1 with the over-ridden peer within a week, the escalation-and-deferral log entry.
6. **The escalation budget** — chapter 6 §2 § *escalation is expensive*. The two-per-fiscal-year modal, the five-is-high reading, the ten-signals-a-partnership-failure reading. The three *budget over-draw* signals and the corrective (return to the partnership contracts, not more careful escalation).
7. **Grind — the quick-reference** — chapter 6 §3 compressed to a half-page. The signal watch, the coalition-tracker refresh, the three exit criteria.
8. **Defer — the quick-reference** — chapter 6 §4 compressed to a half-page. The purpose of the artifact, the revisit-condition writing discipline, the revisit cadence. Point readers at `deferred-decision/` for the full example.
9. **Dead scope — the discipline** — chapter 6 §5. The close-out protocol, the archive-not-delete rule, the re-open criteria.
10. **How this protocol operates over the partnership contracts** — one paragraph. Reference the four exercise-02 contracts' escalation paths; the protocol does not replace them, it operates them.

Length: three to five pages. Readable in one sitting.

### `worked-escalation/` — one escalation taken end-to-end

Pick a specific disagreement from your mod-502 portfolio that would plausibly need escalation this fiscal year. Modal shape: two peer executive counterparts (e.g., CAIO wants to accelerate a Gen-AI bet; CFO's envelope cannot absorb it) deadlocked on a specific decision with a cycle-boundary deadline. Avoid trivial deadlocks (resolvable at the technical layer) and avoid impossible deadlocks (no plausible escalator altitude).

**`00-context.md`** — one page. What the bet is, which exercise-01 one-pager row it corresponds to, which exercise-02 partnership-contract seams it crosses, what the specific decision in deadlock is, which stage B 1:1s have already been held (reference exercise-03's prep notes), and why the technical layer has not converged. Chapter 6 §2 § *pre-conditions* checklist applied: show the five criteria met.

**`01-escalation-artifact.md`** — chapter 6 §2 § *the escalation artifact* in full. One to two pages. All eight sections (decision, parties, why-not-resolvable, what-each-resolution-means, principal-recommendation, peer-recommendations, deadline, follow-up). The paragraph *what the peer parties recommend and why* is in each peer's voice, with their verbatim position where you have it from exercise-03's coalition tracker.

Three to four alternative outcomes are enumerated. Not two (chapter 6 §2 § *the alternative outcomes are enumerated* is explicit: not binary); not seven (unwieldy). Each outcome has a one-paragraph consequence note (capacity, direction, timeline, partnership impact).

**`02-pre-brief-plan.md`** — one page. Chapter 6 §2 § *pre-conditions* criterion 1 (*the four peer executive counterparts know the escalation is coming*). A table listing each of the four peer executives, the date you pre-brief them, the specific framing you walk through with each, and the standing partnership-contract cadence (from exercise-02) you use to deliver the pre-brief. Chapter 3 § *never surprise your peer* is the discipline. If the escalation is between two of the four peers, the other two still get a pre-brief.

**`03-meeting-run-sheet.md`** — one page. Chapter 6 §2 § *the escalation meeting* shape. 15–30 minutes, minute-by-minute:

- Minute 0–2: the escalator states the question back to open the meeting.
- Minute 2–5: parties present (if not the four peer counterparts themselves, their representatives).
- Minute 5–10: principal walks the four outcomes in neutral tone.
- Minute 10–20: peers state their positions; the pre-briefing pays off because the paragraphs are already written.
- Minute 20–25: escalator decides, or names the date-certain by which they will.
- Minute 25–30: follow-up confirmed; next steps named; the coalition tracker's absorbing commits enumerated.

Include the *fallback decision cadence* — if the escalator cannot decide on the spot, chapter 6 §2 § *the escalation meeting* names the named-date discipline. Draft the fallback sentence the principal expects to hear and respond to.

**`04-post-escalation-24h-memo.md`** — one page. Chapter 6 §2 § *after the escalation*. The one-page memo that lands within 24 hours. Sections: the ratified decision (one sentence), the parties' positions (one line each), the follow-up commits (named owners and dates), the coalition-tracker rows that will be updated, the escalation-and-deferral log row that will be added. Plus the *within-a-week 1:1 with the over-ridden peer* note — which peer, which exercise-02 partnership-contract cadence, what you plan to walk through.

### `deferred-decision/` — one deferred decision taken end-to-end

Pick a different bet (or a different clause of a related bet). Modal shape: a bet whose strategic value is clear but whose org readiness is not — a structural constraint (regulatory environment unclear, substrate immature, business direction above the CTO in flux, competitive posture not resolved) makes ratification premature.

**`00-context.md`** — one page. What the bet is, why it is not grind (the readiness gap is not resolvable by more evidence or more coalition work), why it is not escalate (there is no altitude at which an executive can resolve the structural constraint), why it is not dead (the strategic value is clear enough to be worth memory cost). Chapter 6 §1 § *criteria for defer* checklist applied: show the five criteria met.

**`01-deferred-decision-artifact.md`** — chapter 6 §4 § *shape* in full. One to two pages. All eight sections (the bet, the ratified decision, who ratified, why-deferred-not-killed, revisit condition, revisit owner, revisit cadence, dead-scope trigger).

The *revisit condition* is the load-bearing section. Chapter 6 §4 § *the revisit condition — writing discipline* is the standard: specific, observable, time-bounded, multiple-where-appropriate. If you cannot pass the writing-discipline test on the revisit condition, the bet is not defer; it is grind (needs more work to define) or dead scope.

**`02-revisit-cadence-plan.md`** — one page. Chapter 6 §4 § *the revisit cadence — practice*. The three-cadence pattern:

- Standing check-in on the 1:1 cadence (which exercise-02 partnership-contract 1:1, two-to-three minute block).
- Semi-annual full walk-through at the strategy refresh (mod-502 chapter 5 cadence).
- Artifact refresh with every touch — what notes get added, who adds them.

Plus the *when-this-becomes-dead-scope* paragraph — the specific condition that would move this deferral to dead scope, and who is empowered to close it (modal: the IC-principal plus the CAIO, co-close per chapter 6 §5).

### `escalation-and-deferral-log.md` — the log

Chapter 6 §6 is the schema. At least eight rows across the four states. Mix: at least two *escalate* rows (one in-flight, one decided), at least three *grind* rows (feeding from exercise-03's coalition tracker's grinding bets), at least two *deferred* rows (one is the artifact above; the other is an older deferral), at least one *dead* row (archived; one-sentence close-out note).

Columns per chapter 6 §6 § *schema*: decision title, associated bet, state, sub-state (per state), peer executives involved, coalition-tracker cross-reference, last touched, next action.

Below the table, a short narrative:

- The current cycle's *escalation-budget read*. How many escalations so far this fiscal year; what the modal / high / failure-signal cadence is from chapter 6 § *escalation is expensive*; your current read on the partnership-contract health as a result.
- The deferred-decision shelf's size and health. How many bets are deferred; how many have revisit conditions approaching; how many are at risk of dead-scoping without a close.
- The dead-scope archive's pattern. How often bets re-opened from archive in the past; what the modal re-open trigger has been.

### `pre-mortem.md` — chapter 6 §2 *escalation is expensive* applied

One short page. For *this* cycle's planned escalations and deferrals, name the specific failure modes you are most at risk of:

- **Over-escalation.** Which of this cycle's would-be escalations should actually be grinds, and what would it take to catch that before escalating. Chapter 6 §1 § *criteria for escalate* criterion 3 (*prior-attempt-at-technical-layer*) is the test.
- **Partnership-contract breakage from a visible escalation.** Which peer executive is at highest risk of reading the current cycle's escalations as the principal routing around them. Chapter 6 § *the escalation budget is being over-drawn* three signals applied.
- **Silent dead-scope.** Which bets on the deferred shelf are closest to becoming dead-without-a-close, and the specific revisit-cadence hygiene change that would catch them.

## Starter guidance

- **Pick a worked escalation that is actually plausible.** Not a slam-dunk ("the CFO will obviously agree"), not an impossible ("the CEO will decide between two product lines in a 20-minute meeting"). Chapter 6 §1 § *criteria for escalate* criterion 1 (*specific, resolvable question*) is the test. If you cannot write the one-paragraph decision cleanly, the escalation is not well-formed.
- **Honour the pre-brief discipline in the artifact.** Chapter 6 §2 § *the parties* in the escalation artifact names the peers' positions *in their voice, ideally endorsed by them before the escalation*. For a hypothetical worked example, draft the paragraph as if the peer had endorsed it; make it something the peer *would* endorse. Chapter 3 § *never surprise your peer* is the discipline.
- **Enumerate three or four outcomes, not two.** Chapter 6 §2 § *the alternative outcomes are enumerated* is explicit about why binary enumerations fail. If you can only draft two outcomes, you have not thought broadly enough.
- **The deferred-decision's revisit condition is the whole artifact's leverage point.** Chapter 6 §4 § *the revisit condition — writing discipline* has four criteria; test your draft against each. *"When we have more data"* fails. *"When the FY27-Q1 eval-set refresh includes the three enterprise-workflow benchmarks named in exercise-01 deep-dive section 7, scheduled for YYYY-MM-DD"* passes.
- **Pick the deferred bet from the FAQ.** Exercise-01's acceptance criteria required three *deferred* FAQ entries. Pick one of those three for the full deferred-decision artifact. The FAQ entry's one-line *"deferred pending <signal>, expected by <date>"* becomes this exercise's load-bearing section.
- **Log before you draft.** The escalation-and-deferral log is the simpler artifact; it is also the one that tells you whether the escalation and the defer artifacts should actually be authored or whether they are premature. Draft the log first, inspect the balance of states, then pick the escalation and deferred items.
- **Walk the partnership-contract escalation paths.** For the worked escalation, the pre-brief plan references the four exercise-02 contracts' *escalation path* sections. If the escalation path for the deadlock does not match any of the four, the deadlock is not what you think it is; re-check whether the escalation is at the right altitude (chapter 6 §1 criterion 4).
- **Keep the protocol document team-facing.** The protocol is the document your ML-function staff-plus engineers can read without you present. It is not your personal process notebook. Chapter 1 § *reliable, repeatable practice* is the discipline — the protocol document is what makes the practice repeatable.
- **Honour chapter 6's refusal to romanticise defer.** Chapter 6 §4 opens with *"defer is the outcome most curricular material treats as failure. It is not."* Honour that in your deferred-decision artifact: write it as a ratified, defensible outcome, not as a face-saving alternative to escalate.
- **Treat the dead-scope row as a learning artifact.** The log's at-least-one dead row is where the principal practises the discipline of writing off strategic bets. Chapter 6 §5 § *closing a bet* is the shape. Draft the one-sentence close-out note; it is harder than it looks.

## Acceptance criteria

Your artifact set is done when it passes all of the following:

- [ ] `escalation-protocol.md` has all ten required sections. The pre-conditions, the artifact shape, the meeting shape, and the post-escalation discipline each match chapter 6 §2 exactly. The escalation-budget section names the two / five / ten modal / high / failure-signal cadences from chapter 6.
- [ ] The protocol is readable in one sitting (three to five pages) and uses no jargon a new ML-function staff engineer would not understand.
- [ ] `worked-escalation/` has all five required files.
- [ ] `01-escalation-artifact.md` has all eight sections from chapter 6 §2 § *the escalation artifact*. It fits on one or two pages.
- [ ] The escalation artifact enumerates three or four alternative outcomes, not two. Each has a one-paragraph consequence note.
- [ ] The *what the peer parties recommend and why* paragraph(s) are in each peer's voice and reference a specific exercise-03 coalition-tracker row.
- [ ] `02-pre-brief-plan.md` has a table with all four peer executive counterparts, each with a pre-brief date, framing, and partnership-contract cadence.
- [ ] `03-meeting-run-sheet.md` has a minute-by-minute agenda totalling 15–30 minutes with a fallback decision cadence drafted.
- [ ] `04-post-escalation-24h-memo.md` fits on one page and has the ratified decision, parties' positions, follow-up commits, coalition-tracker-row updates, log row, and the within-a-week 1:1 note.
- [ ] `deferred-decision/` has all three required files.
- [ ] `01-deferred-decision-artifact.md` has all eight sections from chapter 6 §4 § *shape*.
- [ ] The *revisit condition* passes chapter 6 §4 § *writing discipline*: specific, observable, time-bounded, multiple-where-appropriate.
- [ ] `02-revisit-cadence-plan.md` names the standing-1:1 touchpoint (which exercise-02 contract), the semi-annual full-walk cadence, the artifact-refresh discipline, and the dead-scope trigger.
- [ ] `escalation-and-deferral-log.md` has at least eight rows mixing escalate (at least two), grind (at least three), deferred (at least two), dead (at least one). The chapter 6 §6 schema's eight columns are populated for every row.
- [ ] The log's narrative names the escalation-budget read for the cycle, the deferred-shelf size and health, and the dead-scope archive pattern.
- [ ] `pre-mortem.md` walks the three named risks (over-escalation, partnership-contract breakage from escalation visibility, silent dead-scope) with specific references to this cycle's artifacts.
- [ ] Every escalation path invoked matches one of the four exercise-02 partnership contracts' escalation-path sections. No new escalation paths are invented in this exercise.
- [ ] At least one FAQ *deferred* entry from exercise-01 is lifted to a full deferred-decision artifact here.
- [ ] At least one slipping commit from exercise-03's stage-D commitment tracker surfaces as a *grind* row or as a trigger for the escalation.

## Stretch goals

- **Draft the *re-ratification* artifact for the worked escalation.** Chapter 6 §2 § *after the escalation* names the within-a-week 1:1 with the over-ridden peer. Draft the agenda for that 1:1 — three to five minutes, under the exercise-02 partnership-contract cadence, with the specific partnership-repair framing (*"here is what the escalation ratified, here is how we move forward, here is the next cycle's co-authorship opportunity I want to carry you on"*). This is the artifact that makes escalations non-partnership-breaking.
- **Author a *parallel* deferred-decision artifact that walks defer-to-dead for a bet that has been in defer for two cycles.** Chapter 6 §5 § *closing a bet* is the shape. The one-paragraph close-out note, the archived-not-deleted practice, the dead-scope-log row. This is the discipline that keeps the shelf clean.
- **Author the *budget-reset* post-mortem for a principal whose escalation budget has been over-drawn.** Chapter 6 § *escalation is expensive* names the three budget-over-draw signals. Draft the one-page post-mortem — the three signals observed, the root-cause partnership-contract failure, the corrective-action plan at the chapter 3 layer. This is where the hard lesson lives.
- **Draft a *dual-track* escalation protocol document for the fifth-counterpart case.** Exercise-02 stretch goal 3 asked for one contract with a fifth counterpart (Chief Data Officer, General Counsel). Extend the escalation protocol to cover that counterpart's escalation path. Chapter 6 §2's framework is modular; the extension is the test.
- **Draft the *board-sub-committee* escalation case.** Chapter 2 and chapter 3 named the board sub-committee as the rare, highest-altitude venue. For a hypothetical bet that would reach board escalation, draft the escalation artifact (chapter 6 §2 § *the escalation artifact*) in that voice. The CAIO is a co-author, not a party; the CFO is a party. This is the escalation shape most principals never author; drafting it builds the vocabulary.
- **Author the *cross-cycle learning note* for the escalation-and-deferral log.** One page summarising what the log's archive is teaching across the current and prior cycles: which escalations were well-formed and which were not; which deferrals became bets and which became dead; which partnership contracts the pattern of escalations is revealing stress in. Chapter 1 § *reliable, repeatable practice* is the reference; the learning note is what makes the practice second-cycle better than first-cycle.

## Deliverable location

Local workspace / personal git repo, extending the workspace from exercises 01–03. Do not commit into this curriculum repo. The escalation-and-deferral log is the artifact that chapter 1's defensibility test 5 reads against; the test is passed when the log is up-to-date and the state of every bet is named.
