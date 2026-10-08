# exercise-03: Cross-Org Coalition Sequencing Plan

**Estimated effort:** 3 hours

## Objective

Author the *coalition sequencing plan* for one named bet from your mod-502 portfolio — the single artifact system that converts the exercise-01 triplet (one-pager, deep-dive, FAQ) and the exercise-02 partnership contracts into a ratified-and-executed decision across the org. The output is the current-cycle coalition tracker, plus the four stage artifacts (pre-read distribution list, one-on-one prep notes, decision-room agenda, follow-up commitment tracker) that chapter 4 §1 names.

This is where the triplet from exercise-01 and the contracts from exercise-02 become an *executable* ratification sequence, in the Twilio sense (chapter 4 § *reading the practice against Twilio's framing*). Without this exercise, the two prior exercises produce documents that do not move.

## Prerequisites

- **Mod-504 chapter 4 read end-to-end.** Especially §1 (the four-stage sequence), §2 (the coalition tracker schema), §3 (the three named failure modes), §4 (reading the practice against Twilio's framing).
- **Mod-504 chapter 3 read end-to-end.** The four partnership contracts' cadences are the standing calendar entries this sequence operates over.
- **Mod-504 chapter 5 read end-to-end.** The three artifacts the sequence consumes (one-pager, deep-dive, FAQ) and how they ship together.
- **Exercise-01 complete.** You need the SVP / CTO-audience triplet as the artifact the pre-read distributes.
- **Exercise-02 complete.** You need the four partnership contracts as the standing cadences the stage B 1:1s run through.
- **Mod-502 chapter 2 skimmed.** Your bet portfolio row-list is where you pick the bet this exercise sequences.
- **Mod-503 chapter 7 skimmed.** The responsible-AI review body is one of the modal decision-room venues; the chapter's session-shape vocabulary is the reference.

## Problem statement

Chapter 4 named the four stages. The modal first-cycle failure is to collapse them: distribute the one-pager, hold one "walk-through" meeting, declare the bet ratified, and discover six months later that nothing executed. The four stages exist as separate stages because each has distinct entrance and exit criteria; collapsing them is how coalitions silently fail.

Your job on this exercise is to walk one bet through the full four-stage sequence as a *plan* — not to actually run it. For a hypothetical FY26-Q1 decision-room on one of your mod-502 bets, you draft:

- The *coalition tracker* (chapter 4 §2) with every named stakeholder, their role in this bet, their current position (your best read), and the shift signals from the chapter 4 § *stage B* discipline.
- The *pre-read distribution plan* (stage A) — who gets what artifact, on what reading window, with what return channel.
- The *one-on-one prep notes* (stage B) — one prep note per executive-branch counterpart and per peer VP who will speak in the room, each with the specific ask, the anticipated objection (from the FAQ), and the shift-signal watch.
- The *decision-room agenda* (stage C) — the room's chair, the five-to-ten slide walkthrough, the Q&A structure, the ratification sentence the chair is expected to deliver.
- The *follow-up commitment tracker* (stage D) — the specific commits the room is expected to produce, with named owners, dates, and the leading-indicator cadence that would flag slippage.

The output is a single workspace directory, inspected as a system. Chapter 4 §4 (*executable roadmaps*) is the acceptance frame: the plan is done when a peer reading it can see how your coalition becomes a shippable commit list.

## Requirements

Populate a workspace directory `exercise-03-coalition-sequencing/`. Suggested layout:

```
exercise-03-coalition-sequencing/
├── README.md                              # which bet, which decision-room, which cycle
├── coalition-tracker.md                   # chapter 4 §2 schema; one row per stakeholder
├── stage-a-pre-read-distribution.md       # distribution list, windows, return channels
├── stage-b-one-on-one-prep-notes/
│   ├── 00-prep-ordering-and-rationale.md  # the ordering discipline (chapter 4 § stage B)
│   ├── caio-prep.md
│   ├── governance-prep.md
│   ├── ciso-prep.md
│   ├── cfo-prep.md
│   ├── peer-vp-platform-prep.md
│   ├── peer-vp-product-prep.md
│   └── chair-pre-brief.md                 # the chair of the decision-room
├── stage-c-decision-room-agenda.md        # the room: chair, slot, slides, Q&A, ratification sentence
├── stage-d-commitment-tracker.md          # named commits with owners / dates / leading-indicator cadence
├── pre-mortem.md                          # chapter 4 §3 failure modes applied to this bet
└── retrospective-plan.md                  # the "what will we check in 90 days?" cadence
```

### `README.md` — bet selection and scope

- **The bet.** Which row from your mod-502 bet portfolio. One paragraph: the posture, the current-year state, why this is the bet the coalition is working.
- **The decision-room.** Which specific venue is the ratification room — the CTO's monthly technical council, the CAIO's investment review, a joint SVP-Engineering/Product session, the responsible-AI review body, or a board sub-committee. Chapter 4 § *stage C* enumerates the modal venues; pick one and justify.
- **The cycle.** The specific calendar window — the next fiscal planning cycle, a strategy semi-annual refresh, a one-off out-of-cycle decision. Chapter 4 § *stage A* reading windows reference this.
- **The ask.** One sentence. The specific decision the room is being asked to ratify. Not *"direction on the Gen-AI bet"* — *"underwrite the FY26 post-training-program capacity envelope of X–Y engineers for the two enterprise workflows named in exercise-01's bet-portfolio row 4"*. The sharpness of this sentence is what every other artifact in the sequence inherits.

### `coalition-tracker.md` — chapter 4 §2 schema

One row per named stakeholder. Columns are chapter 4 §2's full schema:

- Stakeholder (name, title, org affiliation)
- Role in this bet (*executive-branch peer*, *voting VP*, *reviewing VP*, *ratifying staff engineer*, *informed stakeholder*, *chair*)
- Pre-read status
- 1:1 status
- Position (current best read, verbatim where possible)
- Conditions (verbatim where possible)
- Shift signals (what would move them from *not-aligned* to *aligned*)
- Commit (the specific commit expected from them)
- Commit status
- Last touched

Minimum 12 rows. The four peer executive counterparts (CAIO, governance, CISO, CFO) are rows. The decision-room chair is a row. At least two peer VPs (Platform, Product) are rows. At least three staff-plus engineers (your own ML function and one peer-platform function) are rows. If your worked org has a board sub-committee this would touch, the chair of that committee is a row.

Fill each row with your best-read position. For hypothetical orgs, use plausible positions; label them hypothetical in `README.md`.

### `stage-a-pre-read-distribution.md` — distribution plan

Per chapter 4 § stage A. A compact table plus a short narrative.

Table columns: stakeholder name, artifact tier they receive (one-pager / deep-dive / FAQ / specific deep-dive section), delivery date, reading window (3 / 5 / 7 business days per chapter 4 § stage A), return channel (document comments / Slack thread / scheduled 1:1 / email reply).

Narrative:

- Which stakeholders get *only* the one-pager, which get the one-pager-plus-FAQ, which get the full deep-dive. Chapter 4 § stage A § *audience-matched artifact tier* is the discipline.
- The *distribution window calibration* per audience. A CTO's three-day minimum; a peer VP's five-day; a peer platform-side principal's seven-day.
- The *return channel* per stakeholder. Chapter 4 § stage A § *comments that pile up unanswered turn the pre-read into wallpaper* is the discipline; name where comments go, who triages them, and how fast you respond.
- The *acknowledgement discipline*. Chapter 4 § stage A § *exit criteria* — every stakeholder acknowledges receipt. Name the mechanism (email reply, tracker check-mark, Slack reaction).

### `stage-b-one-on-one-prep-notes/` — per-stakeholder prep

One file per executive-branch counterpart (four files from exercise-02's contracts), one per peer VP who will speak in the room (minimum two: Platform, Product), and one for the chair of the decision-room. Plus `00-prep-ordering-and-rationale.md`.

**`00-prep-ordering-and-rationale.md`** — the order the 1:1s are held in, with justification. Chapter 4 § stage B § *the list of 1:1s is ordered* is the discipline: peer executives first, then peer VPs, then peer staff-plus engineers. Name the exceptions (if any) and why.

**Each per-stakeholder prep note** has these sections:

1. **Stakeholder** — one paragraph. Who they are, which org, their relationship to this bet, their standing partnership contract (if an exec-branch counterpart from exercise-02).
2. **Prior-cycle history** — any relevant history. Positions they held on past bets, commits they kept or broke, visible org-level constraints they are under. If this is a new relationship, say so.
3. **The specific ask for this 1:1** — one or two sentences. Not *"walk through the artifact"* — a named commit you are asking them for. Chapter 4 § stage B § *you have a specific ask per 1:1* is the discipline.
4. **The anticipated objection — steel-manned** — one paragraph in the stakeholder's voice. Chapter 4 § stage B § *steel-man their objection before the 1:1* is the discipline. Pull from the exercise-01 FAQ section for this audience; if you cannot pull a clean one, author it fresh and flag the FAQ gap.
5. **Your response — three-sentence form** — the response you plan to give. Cites a specific exercise-01 deep-dive section, mod-503 chapter, or peer artifact. If the honest answer is a defer (chapter 6), say so.
6. **The shift signals you are watching for** — what would move this stakeholder from *not-aligned* to *aligned*. Chapter 4 § stage B § *track shift signals* is the discipline.
7. **The follow-up you will carry out** — the specific document edit, data pull, or joint conversation you will own as output from the 1:1, with a date.
8. **The partnership-contract touchpoint (if an exec-branch counterpart)** — which clause of the exercise-02 contract this 1:1 is running under (the standing cadence, usually). Chapter 4 § stage B § *route through the partnership contracts* is the discipline.

**`chair-pre-brief.md`** — the pre-brief for the decision-room's chair. Separate from the stakeholder prep notes because the chair is not voting; they are ratifying. Chapter 4 § stage C § *the chair carries the ratification* is the discipline. Sections:

- Who the chair is (title; which decision-room from `README.md`).
- The ratification sentence you expect them to deliver, verbatim (two or three sentences).
- The three outcomes they should walk in prepared for — *ratified as proposed*, *ratified with the addition of X*, *deferred pending Y* — with the vocabulary for each.
- The specific items that remain genuinely open going into the room (if any), so the chair is not surprised.

### `stage-c-decision-room-agenda.md` — the room

Chapter 4 § stage C is the reference. Sections:

- **The room.** The specific venue, the chair, the attendees, the pre-reads they received. One paragraph.
- **The agenda.** 15–30 minutes of floor time (chapter 4 § stage C § *the room is short* is the discipline). Minute-by-minute: who speaks, what they say, how long. The modal shape: 2 minutes for the chair to open and summarise the pre-read, 5–8 minutes for the principal to walk the two-to-three slides, 15 minutes of Q&A anchored in the FAQ, 2 minutes for the chair to state the ratification.
- **The slides** — one line per slide, 2–3 total. Chapter 4 § stage C's modal: slide 1 is the direction sentence plus the bet-portfolio table; slide 2 is the three asks (exercise-01 one-pager's *what we ask of leadership*); optional slide 3 is the one specific commit that is still open.
- **The expected Q&A.** The three to five objections you expect in the room, drawn from the FAQ. For each, which stakeholder is likely to raise it, which stage B 1:1 pre-settled it, and the one-sentence room-level answer.
- **The ratification sentence.** The specific sentence you expect the chair to deliver. Chapter 4 § stage C § *the ratified decision is stated in the room* is the discipline. If you cannot write it in advance, the room is under-sequenced.
- **The *what is not on the agenda* note.** Items that are explicitly out of scope for this room — items for the VP layer, items for the responsible-AI review body, items for the peer platform-side principal's review body.
- **The 48-hour room-log plan.** Who writes the log, where it ships, which coalition-tracker column the commits flow into. Chapter 4 § stage C § *exit criteria* is the discipline.

### `stage-d-commitment-tracker.md` — follow-up discipline

Chapter 4 § stage D is the reference. A compact table plus a cadence narrative.

Table columns: commit (one sentence), responsible peer (name from the coalition tracker), named owner on their side (if different), named date, leading-indicator cadence (how often the commit's progress is checked), slippage trigger (what would reclassify the commit from *in-progress* to *slipping*), escalation plan (chapter 6) if the commit breaks.

Narrative:

- Which bi-weekly / monthly 1:1 (from exercise-02's contracts) will walk the tracker.
- Which specific *commitment-velocity* number you are watching (chapter 4 § stage D § *commitment velocity is a signal* — modal 80% close within 90 days).
- How a slipping commit flows back into the coalition sequence (new 1:1, FAQ update, possible re-ratification).
- How a broken commit flows into chapter 6's escalation log (link to exercise-04 if authored).

### `pre-mortem.md` — chapter 4 §3 applied

Chapter 4 §3 names three failure modes. Walk each against your specific bet and plan.

- **Surprise-in-the-room.** Which stakeholder is most likely to raise a surprise objection, what the surprise would be, and the hygiene change in your stage B that would prevent it. Name the specific 1:1 and the specific question you would add.
- **Coalition-of-one.** Which peer executive from exercise-02 is currently *not* carrying the artifact into rooms you are not in, and what you will change in the next refresh cycle to shift that. Chapter 3 § *the peer's authority is what you borrow* is the reference.
- **No commitment-tracking.** Which commit on `stage-d-commitment-tracker.md` is at highest risk of silent death (long dates, low leading-indicator cadence, past-cycle history of slippage), and the hygiene plan to catch it early.

Each sub-section: one paragraph on the specific risk, one paragraph on the hygiene change.

### `retrospective-plan.md` — the 90-day check-in

Chapter 4 § stage D § *commitment velocity is a signal* is the reference, extended with chapter 1 § *reliable, repeatable practice*. One short page.

- **What you will check in 90 days.** Named commits closed vs. slipping vs. broken. The commitment-velocity number.
- **What you will check in 180 days.** The strategy-refresh question: does the bet still look right? Any shift signals from the coalition tracker that would trigger a mod-502 chapter 5 emergency-refresh?
- **The retro cadence.** Chapter 4 § stage D § *the bi-weekly 1:1 with the CAIO walks the tracker* is the modal cadence; name yours.
- **What a *bad* retrospective would surface.** Chapter 4 §3 failure modes materialising; chapter 6 § *escalation budget* over-draw; partnership-contract drift. Name the leading indicators you would watch for.

## Starter guidance

- **Pick a bet you have real conviction on.** The coalition tracker's *shift signals* column is only honest if you have thought hard about what would move each stakeholder. A bet you are faking will produce a plan that reads thin.
- **Pick a decision-room you have seen in action.** If your current org does not host a CTO's monthly technical council, pick a room pattern you have observed from a prior org or from the industry case-study literature in `resources.md`. Name the pattern in `README.md`.
- **Walk the four stages in order, not in parallel.** Stage A's distribution list determines who gets a stage B 1:1; stage B's shift signals determine the stage C agenda; stage C's ratification sentence determines the stage D commits. Writing stage D before stage A is a common first-cycle failure.
- **Steel-man every stage B objection.** Chapter 4 § stage B § *steel-man their objection* is the discipline. If every peer's objection in your prep notes is dismissible, you have not steel-manned.
- **Draft the chair's ratification sentence early.** Chapter 4 § stage C § *the ratified decision is stated in the room* — if you cannot write the ratification sentence now, you are not ready to walk the room. The sentence is the room's north star.
- **Keep the coalition tracker single-document.** Chapter 4 §2 § *the tracker is one document* is the discipline. Do not split into "my tracker" and "the CAIO's tracker".
- **Keep names realistic.** For a hypothetical org, use plausible titles and realistic span-of-control numbers. Chapter 1's *worked micro-example* is the model: specific enough to be legible, generic enough to not misattribute to a real org.
- **Make the plan survive the week.** Chapter 4 § stage B § *a 1:1 you walk into cold* is a specific test: if the plan assumes you have 20 minutes to prep each 1:1 and your calendar does not realistically give you that, redesign.
- **Cross-reference exercises 01 and 02 directly.** Every FAQ entry you cite in a prep note is a specific exercise-01 FAQ section-and-entry. Every partnership-contract cadence you cite is a specific exercise-02 contract-and-section.
- **Treat stage D as the output.** Chapter 4 § stage D § *closure is the definition of success* — the whole plan exists to produce the commit list in `stage-d-commitment-tracker.md`. If that document reads thin, the rest of the plan has not landed.

## Acceptance criteria

Your plan is done when it passes all of the following:

- [ ] `README.md` names a specific bet from your mod-502 portfolio, a specific decision-room venue, a specific cycle window, and a one-sentence ask.
- [ ] `coalition-tracker.md` has at least 12 rows and uses chapter 4 §2's full ten-column schema. The four peer executive counterparts and the chair are rows.
- [ ] Every row's *shift signals* column is filled with a specific, observable signal — not *"more clarity"*, not *"when the org is ready"*.
- [ ] `stage-a-pre-read-distribution.md` tables every stakeholder with their artifact tier, delivery date, reading window (3 / 5 / 7 business days per chapter 4), and return channel.
- [ ] `stage-b-one-on-one-prep-notes/` contains at least seven prep notes: the four peer executive counterparts, two peer VPs, and the chair pre-brief. The ordering-and-rationale document explains the sequence.
- [ ] Each per-stakeholder prep note has all eight required sections (stakeholder, prior-cycle history, specific ask, steel-manned objection, response, shift signals, follow-up, partnership-contract touchpoint).
- [ ] Each stage B steel-manned objection ties to a specific exercise-01 FAQ entry (or flags the FAQ gap and adds the entry back to exercise-01).
- [ ] `stage-c-decision-room-agenda.md` has a minute-by-minute agenda totalling 15–30 minutes of floor time, 2–3 named slides, and the expected ratification sentence written in full.
- [ ] The *expected Q&A* section names three to five specific objections, which stakeholder raises each, which stage B 1:1 pre-settled it, and the one-sentence room-level answer.
- [ ] `stage-d-commitment-tracker.md` names at least five commits with responsible peer, owner, date, leading-indicator cadence, slippage trigger, and escalation plan.
- [ ] `pre-mortem.md` walks all three chapter 4 §3 failure modes against this specific bet, each with a specific hygiene change.
- [ ] `retrospective-plan.md` names what you check at 90 and 180 days and the modal cadence.
- [ ] The plan reads as a *single artifact system*. A peer reading `README.md` + `coalition-tracker.md` + `stage-c-decision-room-agenda.md` + `stage-d-commitment-tracker.md` in sequence can describe the coalition's current state and expected outcome without further briefing.
- [ ] Every peer executive counterpart from exercise-02 appears in both the coalition tracker and the stage B prep notes. The partnership-contract cadences from exercise-02 are the actual cadences the stage B 1:1s run under; no new standing cadences are invented.
- [ ] The FAQ entries from exercise-01 that get walked in stage B 1:1s are enumerated. Any new objections surfaced in prep that are not in the FAQ are listed as *FAQ gaps* for the next exercise-01 refresh.

## Stretch goals

- **Author a shadow coalition tracker for a *second* bet.** Pick a smaller bet from the same mod-502 portfolio and author its coalition tracker only (schema, 8–10 rows, shift signals). The second tracker shows whether the schema generalises or whether the first was over-fitted to one bet.
- **Draft the pre-read package email.** The actual email the stakeholders receive at stage A. Chapter 4 § stage A § *distribution windows* and § *the exit criteria* are the discipline. Three paragraphs max — what this is, when the room is, what response you need by when.
- **Author a *coalition-tracker refresh ritual* document.** The procedure for the standing 1:1 with the CAIO (exercise-02) that walks the tracker in five minutes. Chapter 4 § stage D § *the tracker is refreshed on the standing 1:1 cadence* is the reference. Model: the five-minute block, the three rows per cycle that get a close look, the shift-signal check, the slipping-commit flag.
- **Model the *coalition-of-one* failure in reverse.** For each of your four peer executive counterparts, draft one paragraph on which rooms *they* are carrying your artifact into that you are not. Chapter 4 §3 failure mode 2 is the discipline. This is the test of whether the partnership contracts are actually loading the direction.
- **Draft the *post-ratification* 1:1 agenda for each exec-branch counterpart.** Chapter 4 § stage D § *follow-up commitment tracking* says the bi-weekly walks the tracker; author the specific five-minute block agenda for each of the four peers, for the first post-room 1:1. Different peers care about different commits; the agendas should differ.
- **Draft the *coalition-history* appendix for a cross-cycle view.** Pick two or three stakeholders who have been on multiple cycles' trackers and sketch what their multi-cycle position-shift history looks like. Chapter 4 §2 § *the tracker persists across bets* is the reference; this is where the memory becomes signal.

## Deliverable location

Local workspace / personal git repo, extending the workspace from exercises 01 and 02. Do not commit into this curriculum repo. The coalition tracker and the commitment tracker are what exercise-04 reads to populate its escalation-and-deferral log — the slipping commits from stage D are the escalation candidates chapter 6 processes.
