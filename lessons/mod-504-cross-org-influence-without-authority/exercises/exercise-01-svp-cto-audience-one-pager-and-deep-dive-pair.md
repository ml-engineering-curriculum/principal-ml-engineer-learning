# exercise-01: SVP / CTO-Audience One-Pager, Deep-Dive, and FAQ Triplet

**Estimated effort:** 3 hours

## Objective

Author the *SVP / CTO-audience narrative triplet* — the one-pager, the deep-dive companion, and the FAQ — for the ML technical direction you drafted in [`../../mod-502-org-and-industry-ml-strategy/exercises/exercise-01-org-ml-north-star-one-pager.md`](../../mod-502-org-and-industry-ml-strategy/exercises/exercise-01-org-ml-north-star-one-pager.md). The output is the *lift* (chapter 2) of that mod-502 pair from *VP / staff-engineer* audience to *SVP / CTO / CEO* audience, plus the third artifact (the FAQ, chapter 5) that inoculates the decision-room.

This is not a re-authoring exercise. It is a *lift-vs-replace* exercise (chapter 2 § *the lift-vs-replace rule*). The mod-502 artifact is your substrate; the deliverable is the audience-lifted triplet.

The triplet ships as one package. It is what circulates in the pre-read distribution (chapter 4 stage A) and grounds the 1:1s (chapter 4 stage B) leading into the decision-room (chapter 4 stage C).

## Prerequisites

- **Mod-502 chapters 1, 2, 4, 7 read end-to-end.** The paired-artifact frame from chapter 7 is the direct antecedent; every discipline in the mod-502 one-pager writing guide applies, doubled at the SVP / CTO altitude.
- **Mod-502 exercise-01 complete.** You need the *staff-scope* or *VP-scope* one-pager and deep-dive as the substrate to lift from. Without them, this exercise produces the "manifesto with no substrate" failure mode (chapter 2 § failure 2).
- **Mod-504 chapter 2 read end-to-end.** Especially § *the five axes of difference* and § *the lift-vs-replace rule*.
- **Mod-504 chapter 5 read end-to-end.** The three-artifact discipline, the FAQ shape by audience section, the writing discipline per artifact.
- **Optional but recommended: mod-502 exercise-03** (the multi-year roadmap with non-goals and sunsets), which populates the deep-dive's sections 3 and 4.
- **Mod-503 chapter 8 skimmed.** Chapter 5 § *the deep-dive* section 5 (coherence with the peer platform-side principal's grid) presumes the seam vocabulary.

## Problem statement

Your mod-502 pair was authored for the *VP of Engineering (ML)* audience — one rung below the audience ceiling this module walks. Chapter 2 § *the five axes of difference* named the boundary between that audience and the SVP / CTO / CEO audience. Your job on this exercise is to walk the mod-502 pair *through the boundary*: preserve the substrate, adjust the altitude, add the FAQ.

Specifically:

- The one-pager is rewritten so it survives a five-minute CTO read. The direction sentence is at the multi-year altitude. The bet portfolio drops team names and quarter-level milestones. The *what we ask of leadership* section becomes directional and structural, not item-level.
- The deep-dive companion is restructured so its readers now include both a staff engineer and the SVP / CTO's own delegated reader. Sections 5, 8, 9, and 12 are the primary sites of the lift.
- The FAQ is authored from scratch, voiced from the specific executive audiences the room will contain.

Chapter 5 § *how the three artifacts ship together* is the acceptance frame.

## Requirements

Populate a workspace directory `exercise-01-svp-cto-triplet/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-01-svp-cto-triplet/
├── README.md                     # index; audience calibration notes; refresh cadence
├── one-pager.md                  # the SVP / CTO / CEO-audience one page
├── deep-dive.md                  # the 15–25 page companion doc
├── faq.md                        # the FAQ, sectioned by audience
├── traceability.md               # per-claim trace from triplet to mod-502 / mod-410 sources
└── appendices/
    ├── mod-410-references.md    # pointers to underlying staff-scope RFCs
    └── refresh-log.md            # version log
```

### `one-pager.md` — the six-section shape at SVP / CTO / CEO altitude

Chapter 5 § *the one-pager* is the reference; mod-502 chapter 7 § *shape* is the six-section template.

- **Section 1 — Direction (2–3 sentences).** Includes the *direction sentence*: 40–60 words, three-part shape (horizon and direction; what we are betting on; what we are explicitly not doing this cycle). Rewritten at least five times. No proper nouns. No jargon a CTO would not recognise.
- **Section 2 — Bet portfolio (5 bullet rows).** Per row: bet name, one-clause posture, one-clause current-year state (bet / hedge / option / not-in-window). No team names inline. No quarter-level milestones. Chapter 2 axis 1 (altitude) is the discipline.
- **Section 3 — Non-goals (3–5 bullets).** The sharpest non-goals from mod-502 chapter 4. The ones a CTO uses to defend the direction to their SVP peers.
- **Section 4 — Signal watch (2–3 bullets).** The most material signals from the mod-502 chapter 6 tracker.
- **Section 5 — What we ask of leadership (3 bullets).** Directional and structural. Chapter 2 axis 4 is the discipline: not item-level, not team-level. *"Underwrite the FY26–FY29 ML capacity envelope in the range X–Y engineers"*, *"commit to the quarterly governance-council touchpoint with the Head of AI Governance"*, *"carry the board-facing narrative for the [named bet]"*.
- **Section 6 — Refresh cadence (1 sentence).** Semi-annually plus emergency-refresh triggers, per the mod-502 chapter 5 refresh cadence.

Constraint: the whole page must fit on *one printed page*. If it overflows, you have descended into the deep-dive.

### `deep-dive.md` — the twelve-section shape, lifted

Mod-502 chapter 7 § *the deep-dive companion* is the twelve-section template; chapter 5 § *the deep-dive* is the SVP / CTO lift discipline.

- **Sections 1–4 and 6–7 and 10–11** carry through from your mod-502 exercise-01 with minor edits (audience calibration, cross-references updated).
- **Section 5 (coherence with the peer platform-side principal's grid)** is expanded to a full one-to-two page treatment. Every mod-502 bet row cross-references the platform-side principal's corresponding roadmap row. Where the two directions cohere is called out; where they do not, an escalation-and-deferral log entry (chapter 6) is cited.
- **Section 8 (refresh cadence and emergency triggers)** is anchored to the four peer executives' calendars — CAIO board cycle, CFO investment cycle, Head of AI Governance regulatory-horizon scan, CISO threat-model refresh. Each is a candidate emergency-refresh trigger.
- **Section 9 (what-we-ask-of-leadership, expanded)** decomposes each of the three one-pager asks into (a) the named executive commit; (b) the cadence at which the ask is fulfilled; (c) the metric that would show the commit has closed. This is the underwriting spec the CFO's delegate will use in fiscal planning.
- **Section 12 (appendices)** cites the underlying `staff-ml-engineer-learning` mod-410 exercise-02 exec-audience RFCs verbatim. If your mod-410 portfolio does not yet exist, cite the mod-410 exercise-02 as the *pattern* your future RFCs will follow, and note the gap.

Constraint: 15–25 pages. Sections stand alone (a CFO's delegate reads section 9 in isolation and drafts the ask). Every claim traces to a chapter or a source artifact.

### `faq.md` — six sections, one per audience

Chapter 5 § *the FAQ* is the reference. Six sections:

1. **CTO objections.** 5–8 entries. Categories per chapter 5 § *shape*: differentiation, cost curve, direction-fragility, recruiting narrative, portfolio-consumption.
2. **CFO objections.** 5–8 entries. Categories: granular-cost, opportunity-cost, payback-horizon, vendor-dependency, peer-function allocation.
3. **CISO objections.** 4–6 entries. Categories: ML-specific threat surface per bet, contract-level enforcement, vendor-incident containment, threat-surface delta vs current-state.
4. **Head of AI Governance objections.** 4–6 entries. Categories: regulatory-obligation activation, responsible-AI review body touchpoint, risk-tier taxonomy shift, documentation surface evolution.
5. **Peer VP objections.** 3–5 entries. Categories: roadmap-touch, substrate-ask, capacity-consumption.
6. **Board / audit-committee objections (only if the org's structure warrants).** 3–5 entries. Categories: reported AI-risk posture, external-commitments alignment, foundation-model-provider exposure. Omit the whole section if your worked org does not have board-level ML review.

Per entry:

- The question is in the stakeholder's voice — the phrasing they would actually use.
- The answer is 2–4 sentences.
- The answer cites a specific deep-dive section, mod-503 chapter, mod-502 chapter, or peer artifact.
- At least three entries across the FAQ are *deferred* (chapter 6 § *the deferred-decision artifact*) — the honest answer is *"deferred pending <signal>, expected by <date>"*. Do not pretend to answer objections you cannot yet answer.

Constraint: 20–30 entries total across sections. Sectioned by audience, not by topic.

### `traceability.md` — the lift verification

Chapter 2 § *the lift-vs-replace rule* discipline. This document verifies you have lifted, not replaced.

- **Table 1 — one-pager claims to source claims.** For every substantive claim in the one-pager, name the source claim in your mod-502 chapter 2 rows or mod-410 exercise-02 RFCs. Rows that cannot be traced are candidates for the *"manifesto with no substrate"* failure (chapter 2 § failure 2); rewrite or drop.
- **Table 2 — deep-dive sections to source RFCs.** For each deep-dive section, list which mod-410 exercise-02 exec-audience RFC(s) it draws from. If your mod-410 portfolio is a placeholder, list the intended pattern.
- **Table 3 — FAQ objections to stage B origins.** For each FAQ objection, name where it came from: a real stage B 1:1 (if you have run any), a peer executive-branch counterpart's known concerns, or a class of objections you have observed at prior orgs. Objections purely from imagination are flagged and the count reported.

## Starter guidance

- **Lift, don't rewrite from scratch.** Open your mod-502 exercise-01 artifact in one window and this exercise's `one-pager.md` in another. Move claim by claim, adjusting altitude. If you are typing from a blank page, you are replacing, not lifting.
- **Draft the direction sentence first, and revise it more than any other sentence.** Mod-502 chapter 7 § *the direction sentence* is the reference; chapter 5 § *the direction sentence — writing discipline* is the SVP / CTO extension. Ten drafts is not excessive.
- **Draft the FAQ from your prior 1:1s, not from imagination.** Chapter 5 § *the FAQ — writing discipline* is explicit that a FAQ populated from imagination misses the actual objections. If you do not yet have a stage B history, use the *classes of objections* the chapter names and be honest about the source in `traceability.md`.
- **Voice the FAQ questions.** *"How does this differentiate from what our competitors are already doing on Gen-AI?"* is voiced. *"What is the competitive positioning of the Gen-AI bet?"* is a strawman. The stakeholder's phrasing matters.
- **Cite everything in the FAQ answer.** A FAQ answer that does not cite a deep-dive section, a mod-503 chapter, or a peer artifact is a FAQ answer the stakeholder will (correctly) treat as opinion.
- **Section-stands-alone in the deep-dive.** A CFO's delegate should be able to read section 9 in isolation and draft the FY26 investment ask. Force yourself to write for that.
- **The one-pager is not an executive summary of the deep-dive.** Mod-502 chapter 7 § *common failure modes* is the reference. The one-pager stands alone; it is its own artifact, produced *before* the deep-dive.
- **Store the FAQ's deferred entries in a placeholder escalation-and-deferral log (chapter 6).** Exercise-04 will populate the log for real; for now, note the entries so you do not lose them.
- **Test the five-minute test on someone.** Chapter 5 § *the self-test before the room* is the discipline. If you do not have a peer to test on, read the one-pager back to yourself after a 24-hour break and try to summarise the direction, the three non-goals, and the one commit.

## Acceptance criteria

Your triplet is done when it can pass all of the following:

- [ ] `one-pager.md` fits on one printed page. The six sections from chapter 5 § *the one-pager* / mod-502 chapter 7 § *shape* are all present.
- [ ] The direction sentence is 40–60 words, has the three-part shape (horizon and direction; what we are betting on; what we are explicitly not doing this cycle), contains no proper nouns, and uses no jargon that requires an ML engineering background.
- [ ] The bet portfolio has no team names inline, no quarter-level milestones, no OKR references, and no specific model architectures or vendor names.
- [ ] The *what we ask of leadership* section has exactly three bullets. Each bullet is *directional and structural* (chapter 2 axis 4) — none is item-level.
- [ ] `deep-dive.md` is 15–25 pages and has all twelve sections from mod-502 chapter 7 § *shape*.
- [ ] Sections 5, 8, 9, and 12 have been re-authored per chapter 5 § *the deep-dive — what lifts and what does not*. Section 5 is one-to-two pages; section 9 decomposes each ask into (executive commit, cadence, closure metric); section 8 anchors to the four peer executives' calendars; section 12 cites the underlying mod-410 exercise-02 RFCs or documents the gap.
- [ ] `faq.md` has 20–30 entries, sectioned into the six audience buckets from chapter 5 § *the FAQ — shape*.
- [ ] Every FAQ question is *voiced* — phrased as the stakeholder would phrase it. Every answer is 2–4 sentences and cites a specific deep-dive section, mod-503 chapter, mod-502 chapter, or peer artifact.
- [ ] At least three FAQ entries are *deferred* per chapter 6 § *the deferred-decision artifact* — the answer is *"deferred pending <signal>, expected by <date>"*, not a fabricated resolution.
- [ ] `traceability.md`'s Table 1 traces every substantive one-pager claim to a source in mod-502 or mod-410. Un-traceable claims are removed or rewritten.
- [ ] The triplet passes the *five-minute test* (chapter 5 § *the self-test before the room*): a peer who has not been in your 1:1s can summarise, after five minutes with the one-pager, the direction, the three non-goals, and the one commit they would be underwriting.
- [ ] The triplet passes the *objection-completeness test* (chapter 5): reading the FAQ, no obvious CTO / CFO / CISO / Head of AI Governance / peer VP objection is unaddressed.
- [ ] The triplet's `refresh-log.md` names the semi-annual refresh cadence and the emergency-refresh triggers from mod-502 chapter 5.

## Stretch goals

- **Run the five-minute test on a peer.** Give the one-pager to a peer executive or senior tech lead outside your ML function. After five minutes, ask them to summarise the direction, the three non-goals, and the one commit. Iterate until they can. If the iteration is more than three rounds, chapter 5 § *the direction sentence — writing discipline* has not yet landed.
- **Draft a two-slide walkthrough.** For the decision-room, chapter 4 § *stage C* names 5–10 slides at most. Draft the two-slide *opener* — one slide with the direction sentence and the bet portfolio table, one slide with the three asks. Chapter 5 § *how the three artifacts ship together* is the reference; the deck is the room's living version of the one-pager.
- **Author the CFO's board-facing narrative section.** Draft the specific two paragraphs the CFO would use, in the CFO's voice, to underwrite the *what we ask of leadership* section in a board technology sub-committee. Chapter 3 § *counterpart 4 — CFO / VP of Finance* is the reference. This is the "co-authored underwriting" artifact.
- **Draft the previous-cycle retrospective.** For each of the mod-502 bets in the portfolio, one paragraph on: what was ratified last cycle, what closed, what slipped, what was deferred, what is now dead scope. Chapter 6 § *dead-scope discipline* is the reference. If you do not yet have a previous cycle, sketch what the first cycle's retro will need to capture.
- **Author the *"what is not on the agenda"* section for the SVP / CTO review.** Per mod-503 chapter 7 § *session shape and agenda*, name explicitly what the room is *not* being asked to decide — items that belong at the VP altitude, items that belong at the responsible-AI review body, items that belong at the peer platform-side principal's review body. This is the discipline that keeps the room at the right altitude.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-01-svp-cto-triplet/` is what you extend across the next three exercises: exercise-02 authors the four partnership contracts that make the triplet ratifiable; exercise-03 authors the coalition tracker that the triplet's pre-read circulates through; exercise-04 authors the escalation-and-deferral log that the triplet's FAQ *deferred* entries populate.
