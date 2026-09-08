# Coalition-Building as an Engineering Discipline

> Chapter 4 of mod-504. Prerequisite: chapter 1 (working definition), chapter 2 (audience boundary), chapter 3 (partnership contracts). Downstream: exercise-03 authors the current-cycle coalition tracker for a bet from the learner's mod-502 portfolio; chapter 5 authors the artifacts the coalition consumes; chapter 6 walks the escalation and deferral protocol the tracker feeds.

## Why "engineering discipline" and not "soft skill"

The chapter title carries the whole framing. The vast majority of curricular material on cross-org influence treats coalition-building as a *soft skill* — a matter of persuasion, empathy, relationship-tending, and executive presence. Those are real inputs; chapter 1 § *not soft-skills-only stakeholder management* acknowledged they are necessary. They are not sufficient, and framing coalition-building as *only* those is what makes it non-repeatable at principal altitude.

Treating coalition-building as *engineering* changes what you produce. An engineering discipline has:

- **A named sequence of stages** the work moves through, with entrance and exit criteria at each.
- **An instrumented state** — an artifact that carries the current position, updated as things shift, that a peer can read cold and understand.
- **A pre-mortem** — the enumerated failure modes and the mitigations, drafted before the work runs.
- **A commitment-tracking layer** — the loop that closes when the commit made in a room is honored in the following weeks.
- **A retrospective** — what shifted, what did not, and what the next cycle carries.

This chapter walks the four stages of the sequence (§1), the coalition tracker as the instrumented state (§2), the pre-mortem and the three named failure modes (§3), and the commitment-tracking layer (§4). Exercise-03 has you author the sequence, the tracker, and the pre-mortem for a real bet from your own mod-502 portfolio.

The framing is anchored to Twilio's *"lead cross-functional engineering efforts, breaking down complex initiatives into executable roadmaps"* — the sentence carries the two words that make the framing work: *engineering* and *executable*. Both cut the soft-skills-only reduction; both convert a coalition into a shippable output.

## §1 — The four-stage coalition sequence

Every material coalition, at principal altitude, moves through four named stages. The stages are not always sequential (later stages sometimes loop back to earlier ones), but the *entrance and exit criteria* for each are load-bearing. Skipping a stage or entering it under-prepared is where coalitions fail.

### Stage A — Pre-read distribution

**Purpose.** Before the coalition has any conversation, every named stakeholder has read the artifact you are ratifying against. The artifact is the mod-502 one-pager (for principal-scope stakeholders) or the mod-503 canonical API contract (for platform-side stakeholders) or the deep-dive companion (for staff engineers who will execute). Chapter 5 walks the artifact craft; this stage is about the *distribution* discipline.

**Entrance criteria.**

- The artifact is at v-published version. Not draft; not "coming soon". A stakeholder reading v0.7 and being asked to ratify v1.0 in the meeting is reading and reacting to a document they cannot yet trust.
- The audience-matched artifact tier (chapter 2) is selected per stakeholder. The SVP / CTO gets the one-pager. The VP of Platform gets the deep-dive companion's substrate section. The staff engineer on the Ranking team gets their portfolio-scope section of the deep-dive.
- The distribution list is *complete*. Missing stakeholders discovered mid-sequence are the leading indicator of surprise-in-the-room later.

**Exit criteria.**

- Every named stakeholder has *acknowledged receipt* — a lightweight signal (an email reply, a message in the shared channel, a check-mark in the coalition tracker) that they have the artifact and know when the decision-room is.
- Each has been *asked* whether they will read before the room, with the option to defer the read and delay the room. A stakeholder who admits *"I won't have time to read this before Thursday"* is a stakeholder who cannot ratify Thursday; better to know now.
- Pre-read comments have a *return channel* — a document to comment on, a Slack thread, a scheduled 1:1 (see stage B). Comments that pile up unanswered turn the pre-read into wallpaper.

**Discipline.**

- **Distribution windows are calibrated to reading time.** A one-pager to a CTO: 3 business days minimum. A 15-page deep-dive to a peer VP: 5 business days. A canonical API contract to a peer platform-side principal: 7 business days. Shorter than this and you have distributed under-read, which is worse than not distributing at all — you have converted the artifact into a decoration.
- **The pre-read is not a substitute for the 1:1.** Some stakeholders will read carefully and come to the room aligned; most will not. The pre-read is table-setting; stage B is where the alignment happens.
- **Track the reads.** The coalition tracker (§2) has a *pre-read status* column per stakeholder. Populate it. The gaps show up as pre-1:1 items in stage B.

### Stage B — One-on-one prep

**Purpose.** Before the decision-room, every executive stakeholder who will speak has *already had a 1:1 with the principal* in which they walked through the artifact, raised their concerns, heard the principal's response, and either aligned or named the specific reason they cannot align. The decision-room ratifies what has been converged in the 1:1s; it does not host the negotiation.

This stage is where the vast majority of the ratification actually happens. A first-cycle principal treats stage B as *prep for the room*; a defensible practice treats stage B as *where the room's outcome is set*. The room itself is the ratification ceremony.

**Entrance criteria.**

- Stage A is complete for the stakeholders you are 1:1-ing with. You are walking through an artifact they have seen.
- The list of 1:1s is *ordered* — the peer executive-branch counterparts (chapter 3) first, then peer VPs whose function's commitment you need, then peer staff-plus engineers whose ratification the peer VPs will look to. Peer executives before peer VPs, because the CAIO's or CFO's endorsement is what makes the peer VPs' commit easy.
- You have a *specific ask* per 1:1. Not *"walking through the artifact"* — a specific commit you are asking this person for, drafted before the 1:1.

**Exit criteria (per 1:1).**

- The stakeholder has *stated their position* on the specific ask — aligned, aligned-with-condition, not-aligned. A 1:1 that ends with the stakeholder in a fuzzy middle is a 1:1 you did not close.
- Their *conditions*, if any, are recorded verbatim. The coalition tracker (§2) has a *conditions* column; populate it.
- The *follow-up* is named — a document edit, a data pull, a joint conversation with a third party — with a named owner and a named date.

**Discipline.**

- **Prep before every 1:1.** Twenty minutes of preparation is more valuable than the meeting itself. What did they push back on last time? What is their org's current constraint? What did they say at the last review? A 1:1 you walk into cold is one where the stakeholder correctly infers you are not treating their input as consequential.
- **Steel-man their objection before the 1:1.** If you cannot articulate their strongest objection in one sentence before you enter the room, you are not ready. Chapter 5 § *the FAQ* is the artifact discipline that funds this practice.
- **Track shift signals.** A 1:1's most valuable output is *what would have to change for them to align*. That is a *shift signal*. The coalition tracker's *shift signals* column is where they go; chapter 6 § *when to escalate* uses them.
- **Route through the partnership contracts.** For the four peer executives (CAIO, governance, CISO, CFO), the 1:1 is the standing calendar entry from chapter 3, not a special-ask meeting. You are using the contract, not creating a new one.

### Stage C — The decision-room

**Purpose.** The room where the ratification is announced. It is *not* the room where the substantive negotiation happens — that is stage B. The decision-room is the ratification ceremony, plus the last-mile alignment on any items that were still open after stage B.

The rooms this stage refers to are typically one of:

- **The CTO's monthly technical council** — the SVP-and-CTO altitude review of ML-function direction. Modal ratification venue for the mod-502 strategy.
- **The CAIO's investment review** — the executive-branch tier's cross-function investment discussion. Modal ratification venue for capacity envelopes.
- **The org-wide architecture review body** (mod-503 chapter 7) — the modal ratification venue for canonical API changes and version bumps.
- **The responsible-AI review body** — the ratification venue for launch approvals and risk-tier decisions.
- **A joint SVP-of-Engineering / SVP-of-Product session** — the modal ratification venue for cross-function bets.
- **A board technology sub-committee** — the rare, highest-altitude venue; always co-attended with the CAIO.

**Entrance criteria.**

- Stage B is complete for every executive stakeholder who will speak. There are no surprises in the room.
- The coalition tracker (§2) is at a *majority alignment* on the specific ask — you know how the room will vote before you walk in. A room where you do not know the outcome is a room you entered under-sequenced.
- The room's chair (the CTO, the CAIO, the review-body chair) knows what the ask is and has agreed to the agenda. Chapter 3 § *never surprise your peer* is the practice at the room level.

**Exit criteria.**

- The ratified decision is *stated in the room*, in a form the chair repeats and everyone hears. A decision that never surfaces as a chair-repeated sentence is a decision that will not survive the week.
- The specific commits are *named* — capacity, headcount, review touchpoints, seam co-authorship — with named owners and named dates.
- The room log (mod-503 chapter 7 § *written outputs*) or the equivalent for the venue is authored within 48 hours and circulated to the coalition tracker's full stakeholder list.

**Discipline.**

- **The chair carries the ratification, not the principal.** The chair (usually the CTO, CAIO, or SVP) is the person whose voice carries the org-wide weight. The principal is the *technical author* of the ratified direction; the chair is the ratifier. A principal who takes over the chair's role in the room has misread the seat.
- **The pre-briefing is not optional.** The chair reads the artifact before the room. If the chair is walking in cold, the principal has failed stage A for the chair.
- **Nothing new introduced in the room.** A stakeholder who hears a new claim, a new number, or a new ask for the first time in the room is going to (correctly) block on it. If it did not survive stage B's 1:1s, it does not go in the room.
- **The room is short.** 15–30 minutes of floor time, with most of it Q&A. A room that runs 60 minutes on a single ratification is a room whose stage B was under-done.

### Stage D — Follow-up commitment tracking

**Purpose.** The stage most under-practiced by first-cycle principals. After the room, the ratified commits are *tracked* to closure. Capacity commits show up as headcount plans in the following cycle. Review touchpoints appear on the calendar. Seam co-authorships produce documents. Version-bumps ship. The coalition tracker is *the artifact this stage lives in*.

Without this stage, ratification is banked, execution is not tracked, and the direction ratified in stage C does not become the *"executable roadmap"* Twilio's framing demands.

**Entrance criteria.** Stage C's decision-room log is written and circulated. The commits are enumerated.

**Exit criteria.**

- Every commit from stage C has a *tracking status* on the coalition tracker — *pending*, *in-progress*, *closed*, *slipping*, *broken*.
- Slipping commits are surfaced *early*, not at the next quarterly. The tracker is a leading indicator, not a lagging one.
- Broken commits are *escalated back* into the coalition sequence — a 1:1 with the peer executive whose commit broke, a possible re-ratification in the next decision-room, or (chapter 6) an escalation to the CAIO / CFO.

**Discipline.**

- **The tracker is refreshed on the standing 1:1 cadence.** The bi-weekly 1:1 with the CAIO (chapter 3) walks the tracker. Slipping commits get discussed live; the tracker becomes the shared instrument.
- **Closure is the definition of success.** A ratification stage C that never closes commits is a ratification stage C that did not deliver *"executable roadmap"*. Chapter 6 § *dead scope discipline* is what happens when a commit cannot close.
- **Commitment velocity is a signal.** A coalition where 80% of commits close within 90 days is a coalition that is holding. A coalition where 40% close is a coalition where the underlying partnership contracts (chapter 3) are eroding.

## §2 — The coalition tracker

The tracker is the artifact that makes the sequence engineering-legible. It is a single document — a spreadsheet, a table in a canonical docs page, a checklist in Backstage, whatever the org's tooling supports — with a bounded schema. Exercise-03 has you author it for a specific bet.

### Schema

One row per named stakeholder. Columns:

| Column | What it holds |
| ------ | ------------- |
| **Stakeholder** | Name, title, org affiliation (ML function, platform, product-area X, governance, finance, CISO). |
| **Role in this bet** | *Executive-branch peer*, *voting VP*, *reviewing VP*, *ratifying staff engineer*, *informed stakeholder*, *chair*. |
| **Pre-read status** | *Distributed on YYYY-MM-DD*; *acknowledged on YYYY-MM-DD*; *read on YYYY-MM-DD*; *comments returned on YYYY-MM-DD*. |
| **1:1 status** | *Scheduled for YYYY-MM-DD*; *held on YYYY-MM-DD*; *position: aligned / aligned-with-condition / not-aligned*. |
| **Position** | Their current position on the specific ask. Verbatim if possible. |
| **Conditions** | Any specific conditions attached to their alignment. Verbatim. |
| **Shift signals** | What would move them from *not-aligned* to *aligned*. This column is chapter 6's fuel; the shift signals are the escalation-and-deferral inputs. |
| **Commit** | The specific commit they carried out of the decision-room (or "n/a" for informed stakeholders). |
| **Commit status** | *Pending / in-progress / closed / slipping / broken*. |
| **Last touched** | Date. Rows untouched for >30 days are staleness indicators. |

### Discipline

- **The tracker is one document.** Not one per stage. Not one per bet direction. The whole coalition for the current-cycle bet lives in one table.
- **The tracker is *shared* with the peer executives** (per the partnership contracts, chapter 3). The CAIO, the Head of AI Governance, the CFO, and the CISO can read the tracker. Their teams cannot always read it (some conditions are sensitive) — but the four peer executives can.
- **The tracker is refreshed on the 1:1 cadence.** The bi-weekly 1:1 with the CAIO includes a five-minute look at the tracker. The monthly 1:1 with the CFO includes a look at the *cost-related* commits.
- **The tracker persists across bets.** Stakeholders who appeared in the FY24 tracker will re-appear in the FY26 tracker with a longer history. The history is signal; a stakeholder who broke a commit two cycles ago is a stakeholder who needs a different sequencing this cycle.

### What the tracker is *not*

- **Not a Gantt chart.** The tracker is not the roadmap; the roadmap is the deep-dive companion (mod-502 chapter 7). The tracker is the *coalition state*, not the *execution plan*.
- **Not a status report.** The tracker is a working document; it is not what you send to the CTO. What you send to the CTO is a curated view — the escalation summary from chapter 6, or the coalition-position summary in the pre-read.
- **Not a permanent surveillance state.** Stakeholders whose commit closed and whose role is *informed* on future bets fall off the tracker. It is a working document, not a personnel file.

## §3 — Three named failure modes

Three failure modes recur in first-cycle principal coalitions. Each has a specific hygiene.

### Failure mode 1 — Surprise-in-the-room

**Symptom.** In the decision-room (stage C), a stakeholder raises an objection nobody else in the room had anticipated. The room derails; the chair delays the ratification; the principal is asked to "come back with a revised proposal". The bet slips a cycle.

**Root cause.** Stage B was under-done for that stakeholder. Either the 1:1 was not held, or the 1:1 was held but the principal did not surface the objection they had, or the objection is new *(reasonable and unforeseen)* — but "reasonable and unforeseen" is a rare and diagnosable outcome, not the modal one.

**Hygiene.**

- **Every stakeholder who will speak in the room has had a 1:1.** No exceptions for "we're friendly" or "they always agree". The 1:1 exists so that the *speaker* in the room repeats what they said in the 1:1, in front of witnesses.
- **The FAQ (chapter 5) is drafted from stage B objections.** Every objection heard in a 1:1 goes into the FAQ; the FAQ becomes the pre-read appendix that inoculates the room.
- **The chair pre-briefs on the possible outcomes.** The chair walks in knowing what a *"ratified as proposed"*, *"ratified with the addition of X"*, or *"deferred pending Y"* outcome would look like. If the chair does not have the vocabulary, they cannot land the ratification.

### Failure mode 2 — Coalition-of-one

**Symptom.** The principal is doing all four stages alone — writing the artifact, walking every 1:1, running the decision-room, tracking every commit. The coalition rides on the principal's calendar; when the principal is out for a week the coalition freezes.

**Root cause.** The partnership contracts (chapter 3) are being under-used. The peer executive branch is treating the principal as the *distribution channel*, not as the *co-author*. The staff-plus engineers whose ratification the coalition depends on are not being brought into the sequence early.

**Hygiene.**

- **The four peer executives carry the artifact into rooms the principal is not in.** The CAIO walks the strategy one-pager to the board sub-committee; the Head of AI Governance walks the policy-to-contract mapping to the risk committee; the CFO walks the capacity envelope to the CFO's own peer set. This is chapter 3 § *the peer's authority is what you borrow*.
- **Staff-plus engineers own the deep-dive sections for their portfolios.** The Ranking-team staff engineer owns the deep-dive's row-3 subsection; the Gen-AI-integration staff engineer owns the row-4 subsection. Their ratification is what makes the room's staff-scope voice consistent with the room's principal-scope voice.
- **The coalition tracker has multiple maintainers.** If only the principal edits the tracker, the tracker is a personal notebook. Chapter 3 § *artifact flow* extends here — the peer executives can annotate their rows.

### Failure mode 3 — No commitment-tracking

**Symptom.** The room ratifies. Six months later, the capacity that was committed is unaccounted for; the review touchpoint the CAIO agreed to never appeared on calendars; the seam co-authorship the peer platform-side principal committed to did not produce a document. The direction ratified in stage C did not become executable.

**Root cause.** Stage D is under-practiced. The tracker exists at stage C; it is not refreshed at stage D. The principal treats the ratification as the outcome; the executive branch (correctly) sees that no follow-through is being tracked, and the credibility of the next ratification erodes.

**Hygiene.**

- **The bi-weekly 1:1 with the CAIO walks the tracker.** Not the whole tracker — the current-quarter commits. A five-minute standing item.
- **Slipping commits are flagged before they miss.** The tracker's *last touched* column and *commit status* column together are the leading indicator. A commit that was *pending* three cycles ago is a commit that has silently died.
- **Escalate broken commits early.** A commit that the responsible peer executive can no longer keep should go into the escalation log (chapter 6) *at the moment it breaks*, not at the next quarterly review. The escalation is the corrective action; the delay is the credibility erosion.

## §4 — Reading the practice against Twilio's framing

Twilio's *"lead cross-functional engineering efforts, breaking down complex initiatives into executable roadmaps"* is the anchor sentence for this chapter. Read each phrase now that the four stages are in view.

- ***Lead*** — the principal is the coalition's *technical author*. The four stages are the leadership practice; without them, "leading" is being copied on emails.
- ***Cross-functional*** — the coalition includes the four peer executives, the peer platform-side principals, the peer VPs, the peer staff engineers. Every stage of the sequence involves all four populations.
- ***Engineering efforts*** — the sequence, the tracker, the FAQ, the escalation log are *artifacts* the practice produces. Chapter 1 § *not "just be very persuasive"* is the corrective; the artifacts are what makes the practice repeatable.
- ***Breaking down*** — the mod-502 bet portfolio decomposes into per-row asks; each per-row ask decomposes into per-stakeholder commits; each commit decomposes into a follow-up. The decomposition is what the tracker instruments.
- ***Executable roadmaps*** — the exit criterion. Stage D closes commits; commits close on named calendars; calendars produce the executable roadmap. Twilio's sentence has three words load-bearing on stage D: *executable*, *roadmap*, and the imperative that these be the *output*, not a byproduct.

A principal who cannot point at their tracker after reading this section is a principal who is running an ad-hoc practice. The tracker is the code; the sequence is the compiler; the roadmap is the binary.

## Summary

- Coalition-building at principal altitude is an *engineering discipline*, not a soft skill. Twilio's *"executable roadmaps"* framing is the acceptance test. The soft-skills inputs (empathy, executive presence, active listening) are necessary but not sufficient.
- The four-stage sequence is pre-read → one-on-one prep → decision-room → follow-up commitment tracking. Every stage has entrance and exit criteria. Every stage is where a first-cycle principal usually fails.
- The *coalition tracker* is the artifact that makes the sequence engineering-legible. A bounded schema per stakeholder — role, pre-read status, 1:1 status, position, conditions, shift signals, commit, commit status, last touched. Shared with the four peer executives.
- Three named failure modes: surprise-in-the-room (stage B under-done), coalition-of-one (chapter 3 partnership contracts under-used), no-commitment-tracking (stage D missing). Each has a specific hygiene.
- The room is where ratification is *announced*; the 1:1 is where ratification is *set*; the commit-tracking is where ratification becomes *executable*. Chapter 5 walks the artifact craft the coalition consumes; chapter 6 walks the escalation and deferral protocol that runs through the tracker's *shift signals* column.
