# exercise-03: Conference Keynote Through-Line, Take-Away, FAQ, and Section-Level Outline

**Estimated effort:** 3 hours

## Objective

Author the full three-part keynote artifact per chapter 4 for one specific keynote slot named in `exercise-01-industry-influence-artifact-plan/fiscal-year-artifact-bets.md`: the *through-line*, the *take-away artifact*, the *room's FAQ*, and the section-level outline the slide deck will be built against. Rehearse to time; capture the pre-flight readout and the hallway-track plan.

The exercise instantiates chapter 4 — the venue map, the three-part artifact, the mod-504 chapter 5 reuse map, the hallway-track discipline, the six-step authoring discipline, and the eight failure modes. It is the second of the three per-artifact exercises (02 for paper / blog, this one for the keynote, 04 for open-source) and often lifts its substrate directly from exercise-02's draft (chapter 4 § *the reuse from mod-504 chapter 5* names the deep-dive-to-paper mapping).

The 3-hour effort target reflects the *outline-plus-FAQ-plus-pre-flight* scope, not the full-rehearsed-deck scope. A fully rehearsed and recorded keynote is typically 30–60 hours of authoring plus 3–5 timed rehearsals; this exercise gets you the authored artifact that the deck is subsequently built against.

## Prerequisites

- **Chapter 4 read end-to-end.** Especially the venue map, the three-part artifact (through-line / take-away / FAQ), the mod-504 chapter 5 reuse map, the hallway-track practice, the six-step talk-authoring discipline, the panel variant, and the eight failure modes.
- **Chapter 1 skim.** The venue-audience-artifact matching discipline underpins the keynote venue choice.
- **Chapter 2 skim.** Specifically § *co-authorship* and § *the internal talk* — the keynote often extends an internal talk that has already road-tested the through-line.
- **Chapter 3 skim (if the keynote references a paper or blog).** The paper or blog is the keynote's deep-dive substrate per chapter 4 § *the deep-dive → the paper or blog*. If exercise-02's draft exists for the same lesson, open it alongside this exercise.
- **Mod-504 chapter 5 read end-to-end.** The SVP / CTO-audience narrative craft (one-pager, deep-dive, FAQ) is the direct antecedent chapter 4 *lifts* to the industry audience. If mod-504 chapter 5 is unfamiliar, the reuse map in this exercise will not land.
- **Mod-504 chapter 4 skim.** The coalition-sequencing discipline is what chapter 4 § *the hallway track* lifts to the conference venue.
- **Exercise-01 completed.** The keynote slot you draft is the one in your `fiscal-year-artifact-bets.md`. If exercise-01 is not yet done, do it first — this exercise's venue, lesson, co-authors, and target return signals all live in that plan.
- **Optional: an existing internal talk recording.** If you have given an internal talk on the lesson (chapter 2 artifact class A), have it open. The through-line pre-flight (chapter 4 § *through-line pre-flight*) is more efficient against a prior internal recording than from a cold start.

## Problem statement

Pick one fiscal-year bet from `exercise-01-industry-influence-artifact-plan/fiscal-year-artifact-bets.md` whose venue class is a conference keynote or industry-track talk. Draft the full three-part keynote artifact per chapter 4's shape plus the section-level outline the deck will be built against plus the hallway-track plan the trip executes against.

Three constraints on the choice.

- The lesson must be *directional* — a bet-framing, an architecture stance, a program-design philosophy — rather than a system-and-data deep-dive (which belongs in a paper, exercise-02) or a reusable-interface release (which belongs in open source, exercise-04). Chapter 4 § *when the venue-artifact match is right* is the test.
- The venue is picked specifically — not *"a conference talk"* but *"QCon AI 2027 track keynote"* or *"KDD 2027 industry day plenary"* or *"MLSys 2027 industry-track talk"*. Chapter 4 § *the venue map* is the reference.
- The internal substrate must exist (or be sketched enough that the exercise can proceed). Chapter 2 § *the internal talk* is the modal substrate; if the through-line has not been road-tested internally at least once, the pre-flight will fail (chapter 4 § *through-line pre-flight*).

Produce the keynote outline, the through-line, the take-away artifact specification, the room's FAQ, the hallway-track plan, and the pre-flight readout as a bundled first-draft artifact.

## Requirements

Populate a workspace directory `exercise-03-keynote-outline-and-faq/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-03-keynote-outline-and-faq/
├── README.md                        # index; which bet from exercise-01; venue and slot
├── through-line.md                  # the one-sentence through-line + pre-flight readout
├── take-away-artifact.md            # the concrete thing the audience walks out with
├── room-faq.md                      # 8–12 anticipated questions with voiced answers
├── outline.md                       # 5–8 section outline matched to time budget
├── hallway-track-plan.md            # pre-conference outreach list + conversation guides
├── pre-flight-readout.md            # the 5-peer convergence check + what shifted
└── appendices/
    ├── mod-504-reuse-map.md         # the explicit lift from mod-504 chapter 5 artifacts
    └── panel-variant-notes.md       # (optional) if the talk may convert to a panel
```

### `README.md` — index

Half a page. States:

- Which bet from exercise-01 this exercise instantiates. Reference `fiscal-year-artifact-bets.md` bet ID.
- The specific venue and slot (QCon AI 2027 plenary, KDD 2027 industry day, MLSys 2027 industry-track talk — the specific conference, year, track, and time slot or placeholder).
- The talk shape per chapter 4 § *the venue map* (plenary / industry-track / invited / workshop / panel) and the time budget (30 / 45 / 60 minutes).
- The lesson in one sentence (pre-through-line form — pulled from `fiscal-year-artifact-bets.md` and refined here).
- Which of the four chapter 3 principal-scope lesson shapes it fits (architecture / cross-team eval / bet framing / FM economics).
- The internal substrate the talk extracts from (internal talk, canonical reference doc, paired paper or blog — reference exercise-02's draft if applicable).
- The co-authors or named collaborators whose work the talk cites — not everyone named on the slides is a co-author, but the talk's substrate owners are acknowledged on at least one slide and in the FAQ.

### `through-line.md` — the one-sentence through-line

Chapter 4 § *part 1 — the through-line* is the content. 1 page.

- **The through-line.** One sentence, 20–40 words. Two-part shape: (1) what changed or what the industry should adopt, (2) the specific evidence horizon (e.g., *"we ran this program for 18 months across three product areas with 11 model teams"*). No proper nouns unless load-bearing. Written at the top of the file in a dedicated bold line.
- **Why the title is the through-line.** Chapter 4 § *the through-line is the talk's title*. State the talk's working title and confirm that reading the title alone communicates the through-line to a staff-plus engineer glancing at the conference programme. If the title requires interpretation to reveal the through-line, rewrite one of them.
- **Rejected candidate through-lines.** 2–4 earlier drafts that did not survive. For each, one sentence on *why* it was rejected (two-part shape missing, too many proper nouns, no evidence horizon, horizon too generic, through-line too long to hold in memory, lesson not actually directional). The rejected candidates are what makes the discipline visible.
- **The compression chain.** How the through-line compresses from the chapter 2 § *internal talk* framing (if applicable), from the exercise-02 paper abstract or blog lead paragraph (if applicable), and from the mod-504 chapter 5 direction sentence (if the talk also exists in SVP / CTO-audience form). Chapter 3 § *the lesson survives compression* is the discipline — one lesson, four shapes.

### `take-away-artifact.md` — the audience's Monday-morning artifact

Chapter 4 § *part 2 — the take-away artifact* is the content. Half a page to 1 page.

- **The take-away shape.** One of chapter 4's four modal shapes: *reference diagram*, *decision framework*, *open-source release or reference repo*, *follow-on written artifact*. Named explicitly.
- **The artifact itself.** The actual thing the audience will download or clone or save:
  - *Reference diagram*: a one-page diagram (sketched here in markdown or linked to the mod-503 chapter 5 living diagram source, with the proprietary-specifics redaction pass applied per chapter 3 § *the pre-publication legal review*).
  - *Decision framework*: the actual decision tree, matrix, or checklist in markdown.
  - *Open-source release*: a reference to the exercise-04 release proposal (if applicable) or to an existing OSS release; chapter 5 § *the maintenance contract* must be ratified before the keynote commits to it as the take-away.
  - *Follow-on written artifact*: a reference to the exercise-02 paper or blog draft (if applicable) or to an existing published artifact.
- **The distribution channel.** How the audience actually gets the artifact — a conference-published slide deck URL, a repo link read aloud during the talk, a QR code on a slide, a landing page the audience visits. Named specifically.
- **The persistence budget.** How long the artifact will remain accessible — 12 months minimum; longer for a reference diagram or decision framework; indefinite for an open-source release. If the artifact's persistence is less than 12 months, the keynote's return-signal horizon (chapter 6 § *what decay looks like*) is already compromised at launch.
- **Why this shape and not another.** One paragraph justifying the chosen shape against the lesson. A directional architecture-stance keynote with a *follow-on paper* as the take-away is different from the same lesson with a *reference diagram* as the take-away — the choice shapes what the audience does on Monday.

### `room-faq.md` — the audience's anticipated questions

Chapter 4 § *part 3 — the FAQ the room brings* is the content. 1–1.5 pages. 8–12 questions.

Structure as a Q&A block. Each entry has:

- **The question — in the audience's voice.** Not strawmen; the actual question a mid-level staff engineer in the audience would ask if given the microphone. One sentence; two if truly needed.
- **The answer — in the speaker's voice.** 2–4 sentences. Long enough to answer, short enough to speak in 30 seconds. Each answer cites either the internal substrate, the paper / blog, or a specific chapter / section the speaker has prepared.

The 8–12 questions must cover the full chapter 4 § *modal question categories* list (name each category at least once — generalisation, scale, failure-mode, cost, team-shape, vendor / dependency, migration, industry-shift). If one category has no concrete question for your lesson, name why; the absence is itself a signal.

In addition:

- **The questions that the talk itself must address.** Mark each question with one of: *addressed in main talk* (the talk's main line directly addresses the question — the FAQ answer is a 30-second reinforcement of what the talk already covered), *addressed in FAQ only* (the question is tangential to the main line but the audience will still ask it), or *unaddressed-and-honest* (the honest answer is *"I have not thought about that; let me follow up in the hallway"* — chapter 4 § *the Q&A-defensive answer* failure mode is what this guards against).
- **The *follow-up-in-hallway* questions.** Mark 2–3 of the FAQ entries as questions you will *actively steer into hallway conversations* post-talk. These are the chapter 4 § *the hallway track* seed questions — they are what you ask the peer principals in the pre-conference outreach to react to.

### `outline.md` — the 5–8 section outline

Chapter 4 § *the talk-authoring discipline* step 4 is the content. 1 page.

Structure as a sequence of 5–8 top-level sections, each anchored to a slide or a small run of slides. Each section entry has:

- **Section name.**
- **Time budget.** In minutes. The sum of all sections' time budgets equals the talk's slot length minus the Q&A reserve (10–15 minutes at plenary, 5–10 at industry-track).
- **Section purpose.** One sentence. What this section does for the audience and for the through-line.
- **The through-line thread.** One sentence stating how this section advances or illustrates the through-line. If a section does not advance the through-line, it does not belong — cut it to the take-away artifact or to the FAQ.
- **The slide-count estimate.** Rough — not final — but a 7-minute section with 25 slides is text-heavy (chapter 4 failure mode: *the under-rehearsed talk*); a 7-minute section with 3 slides is diagram-heavy.
- **The illustration or diagram.** If the section carries a diagram or a concrete illustration, name it. The 3–5 illustrations of the through-line (chapter 4 § *the talk arc*) carry the talk; most live in sections 2–5.

The talk arc is: framing (2–3 minutes), the through-line stated (1 minute), 3–5 illustrations of the through-line in production (25–30 minutes), the honest failure and its lesson (3–5 minutes), the take-away (2–3 minutes), Q&A (10–15 minutes at plenary, 5–10 at industry-track). If your outline deviates from this arc, state why.

The honest-failure section is a non-optional entry. Chapter 4 § *the keynote with no honest failure* failure mode is one of the eight; the section-level outline enforces it structurally.

### `hallway-track-plan.md` — the conference's stage B

Chapter 4 § *the hallway track* is the content. 1 page.

- **The peer-principal outreach list.** 5–15 named (or role-and-org composite) peer principals you intend to engage before the talk. For each: name / role, org, why them specifically (which of their artifacts, which prior conversation, which shared problem class), and the specific through-line question you want their react to.
- **The pre-conference outreach messages.** 1–2 example drafts (not sent — this is an exercise). Each message is personalised: references the peer's own work, states the through-line in one sentence, proposes a specific 20–30 minute conversation slot at the conference. Not a broadcast; each message is written for one peer.
- **The in-conference schedule.** The 2–4 days of the conference, roughly blocked for: pre-conference outreach completion (travel day, day before), 1:1 conversations (3–8 slots across the main conference days), the talk itself (1 slot), post-talk hallway (immediately after + the next morning), the plenary / dinner social surfaces (evenings). Chapter 4 § *the hallway-track skipped* failure mode is what this plan guards against.
- **The conversation agendas.** For each 1:1 conversation slot, name the one question you will put to the peer. The question is drawn from the FAQ (chapter 4 § *the FAQ shapes the talk*) — the pre-talk conversation surfaces whether the peer's answer matches or diverges from yours, and the divergence is what shapes the talk's framing in the days before delivery.
- **The post-talk follow-up list.** 3–5 commitments you intend to make in the 2–4 days after the talk. Each is a specific follow-up with a named person — a link sent, an introduction made, a joint-work proposal floated. Chapter 6 § *signal 1 (recruiting)* and § *signal 3 (internal leverage)* both improve dramatically when the post-talk follow-up is intentional.

### `pre-flight-readout.md` — the 5-peer convergence check

Chapter 4 § *through-line pre-flight* is the content. Half a page.

- **The five peers consulted.** 5 named (or role-composite) staff-plus peers *who are not attending the talk*. For each: name / role, how long they looked at the through-line (modal: 2–5 minutes), their one-sentence summary of what they understood the talk to argue.
- **The convergence check.** Compare the five summaries. If they converge on a single argument, the through-line is landing. If they diverge, the through-line is not yet the right sentence — name the divergence pattern (two peers heard a *bet-framing* argument, three heard an *architecture* argument; the through-line is unclear which).
- **What shifted after the pre-flight.** The specific revisions the through-line underwent after reading the five summaries. If nothing shifted, either the first through-line was unusually sharp or the pre-flight was cursory; be honest about which.
- **The second-round pre-flight (if the first round did not converge).** If the first-round summaries diverged, revise the through-line and re-run with 3 of the 5 peers. Document the second-round summaries.

The pre-flight is the *before-the-talk-is-written* leverage step. Running it after the deck is drafted is too late — the through-line has already shaped the deck, and the peer summaries will converge on the deck's argument rather than on the through-line itself.

### `appendices/mod-504-reuse-map.md` — the lift from the SVP / CTO craft

Chapter 4 § *the reuse from mod-504 chapter 5* is the content. Half a page.

A short mapping table, five rows:

| mod-504 chapter 5 artifact | mod-506 chapter 4 keynote analogue | What is the same | What shifts |
|-|-|-|-|
| The one-pager | The through-line | Same compression discipline; one sentence that carries the direction | Spoken, not read; 20–40 words to hold in memory |
| The deep-dive | The paper or blog (chapter 3) | Same substrate role; the artifact the audience consults for the numbers | External venue; longer feedback horizon |
| The FAQ | The FAQ | One-to-one lift; same voiced-objection discipline | Audience is the room, not named executive stakeholders |
| The pre-read distribution | The pre-talk publicity | Same artifact-ahead-of-the-room discipline | Public channel (conference programme) not private channel (slack / email) |
| The 1:1 prep | The hallway track | Same coalition-sequencing discipline; the room does not decide, the pre-work does | Peer principals instead of executive stakeholders |

For each row, add a one-paragraph note on what this reuse looked like for *your* specific keynote (e.g., *"my mod-504 chapter 5 one-pager on the FM program was authored 9 months ago; the keynote through-line is the direct compression of that direction sentence"*). The reuse map is what makes the lift from executive-audience craft to industry-audience craft explicit — chapter 4 § *the keynote is an executive-audience artifact* is grounded, not asserted.

### `appendices/panel-variant-notes.md` — if the talk may convert to a panel

Chapter 4 § *the panel variant* is the content. Half a page. Optional — only populate if there is a non-trivial chance the keynote slot converts to a panel seat.

- **The through-line held across the panel.** Same through-line; the panel format tempts spreading across positions. State the one position you will hold across the full 45–60 minute discussion.
- **The take-away as a quote.** Draft the specific 15–30 word sentence you want the audience to quote in the follow-up hallway. Draft it; rehearse it; deliver it in response to the moderator's opening prompt.
- **The panel-shape FAQ.** The moderator's likely questions and the co-panelists' likely positions. 3–5 entries. Each with the 30-second response you intend to deliver.

## Starter guidance

- **Write the through-line first; before any slide, before the outline, before the FAQ.** Chapter 4 § *the talk-authoring discipline* step 1 is non-negotiable. If the through-line is not stable, every subsequent artifact in this exercise will shift under you.
- **Run the 5-peer pre-flight *before* the outline, not after.** The pre-flight is the leverage step; running it after the deck is drafted will produce false convergence because the peers' summaries will track the deck's argument. The pre-flight is cheap (30 minutes per peer, async DMs are fine) and the ROI on cutting a weak through-line early is extremely high.
- **Choose the take-away before the outline.** The take-away shapes what the talk is *for*. A talk with the take-away retrofitted will have an outline that does not naturally hand off to the take-away in its final 2–3 minutes.
- **Draft the FAQ before the outline, not after.** The FAQ surfaces the objections the talk's main line must address. Objections surfaced in the FAQ that are not addressed in the main line are either (a) moved into the main line (modal) or (b) left to the FAQ with a strong voiced answer. Discovering an unaddressed objection *after* the outline is drafted means an expensive restructuring.
- **The honest-failure section is in the outline, not an afterthought.** Chapter 3 § *the honest-failure discipline* lifted to the spoken venue — one honest failure, 3–5 minutes, that the audience can pattern-match against their own missteps. Chapter 4 failure mode: *the keynote with no honest failure* is modal; cut if the honest failure cannot be named.
- **Build the hallway-track plan early — not the week of the conference.** 2–4 weeks of outreach before the conference is the chapter 4 standard. The ROI on the talk is dominated by the hallway, not the room; a plan built the week of the trip skips most of the leverage.
- **Co-authors are *named*, not implied.** Chapter 2 § *co-authorship* is the leverage discipline, lifted into the keynote: the staff engineers whose work the talk cites are named on at least one slide and acknowledged in the FAQ. Solo-presented keynotes drawn from team work read as glory work and the peer principals in the audience will (correctly) discount them.
- **Rehearse to time, but only after the outline is locked.** 3–5 full rehearsals (chapter 4 § *the talk-authoring discipline* step 6) is the standard; this exercise's time budget covers only the first rehearsal. The remaining 2–4 happen between this exercise and the actual delivery.
- **Time-box each artifact.** README: 10 minutes. Through-line: 30 minutes (then pause for pre-flight). Pre-flight readout: 20 minutes (plus the peers' async turnaround, which happens outside the time-box). Take-away: 15 minutes. FAQ: 40 minutes (this is the load-bearing section). Outline: 30 minutes. Hallway-track plan: 20 minutes. Reuse-map appendix: 10 minutes. Panel variant: 15 minutes (optional). Total ~3 hours.

## Acceptance criteria

The exercise is done when:

- [ ] `README.md` names the exercise-01 bet, the specific venue + slot (not generic), the talk shape and time budget, and the chapter 3 lesson shape the talk fits.
- [ ] `through-line.md` contains the through-line as a bold one-sentence line of 20–40 words with the two-part shape (direction + evidence horizon).
- [ ] The through-line has no gratuitous proper nouns; any proper noun present is load-bearing (information the audience needs).
- [ ] The talk's working title is the through-line or one sentence away from it. If not, one of the two is rewritten.
- [ ] 2–4 rejected candidate through-lines are documented with the specific reason each was rejected.
- [ ] The compression chain is traced from the internal talk (chapter 2) and / or the paper / blog (chapter 3) and / or the mod-504 chapter 5 direction sentence.
- [ ] `take-away-artifact.md` names the shape (reference diagram / decision framework / open-source release / follow-on written artifact), the actual artifact (sketched or linked), the distribution channel, and the persistence budget (12 months minimum).
- [ ] `room-faq.md` contains 8–12 questions covering all chapter 4 § *modal question categories* (generalisation, scale, failure-mode, cost, team-shape, vendor / dependency, migration, industry-shift). Any missing category is explicitly justified.
- [ ] Each FAQ answer is 2–4 sentences and would speak in 30 seconds at pace.
- [ ] Each FAQ entry is marked as *addressed in main talk*, *addressed in FAQ only*, or *unaddressed-and-honest*. No *"I have no answer"* entries that are not framed as honest handoffs to the hallway.
- [ ] 2–3 FAQ entries are marked as *follow-up-in-hallway* seed questions.
- [ ] `outline.md` names 5–8 top-level sections with time budgets that sum to the talk's slot length minus the Q&A reserve.
- [ ] Each section has a one-sentence purpose and a one-sentence through-line thread. Sections that do not advance the through-line have been cut or moved to the take-away or the FAQ.
- [ ] The outline includes an honest-failure section with 3–5 minutes of time budget.
- [ ] The outline matches the chapter 4 talk-arc shape (framing, through-line stated, 3–5 illustrations, honest failure, take-away, Q&A) or explicitly justifies deviation.
- [ ] `hallway-track-plan.md` names 5–15 peer principals with the specific through-line question for each, 1–2 example outreach messages, the in-conference schedule block, the conversation agendas, and the post-talk follow-up commitments.
- [ ] `pre-flight-readout.md` documents the 5-peer convergence check with each peer's one-sentence summary, the convergence or divergence analysis, and the specific revisions the through-line underwent as a result.
- [ ] `appendices/mod-504-reuse-map.md` includes the five-row table with per-row notes specialised to this specific keynote.
- [ ] `appendices/panel-variant-notes.md` is populated (if applicable) with the held through-line, the drafted quote, and the panel-shape FAQ.
- [ ] The exercise passes the *through-line convergence test*: if a sixth peer who was not in the pre-flight reads only the through-line and the talk title, they can summarise what the talk argues in one sentence that matches the four prior pre-flight summaries.
- [ ] The exercise passes the *take-away durability test*: a staff-plus engineer who was not in the audience could, 6 months later, read the take-away artifact and apply the lesson at their own org without the keynote present.
- [ ] The exercise passes the *chapter-4-failure-mode audit*: none of the eight failure modes (no through-line, no take-away, surveyed keynote, no honest failure, keynote-only calendar, under-rehearsed talk, Q&A-defensive answer, hallway-track skipped) are visible in the artifact bundle.

## Stretch goals

- **Record the first full rehearsal.** Chapter 4 § *rehearse to time* step 6. Record (audio or video), self-review, and capture a one-page `rehearsal-notes.md` with: time delta per section, places where the through-line thread wavered, slides that are text-heavy and need re-authoring, Q&A questions that stumbled. The rehearsal is what turns the outline into the deck.
- **Run the full hallway-track outreach dry-run.** Draft the full set of 5–15 personalised outreach messages (not just the 1–2 examples). Even unsent, drafting the full set surfaces the hallway-track's shape: whether 15 is the right number, whether each message is actually personalised, whether the through-line question is specific enough to each peer. This is the chapter 4 § *the hallway track* practice at full scope.
- **Author the companion take-away artifact end-to-end.** If the take-away is a reference diagram or a decision framework, draft the final version (not a sketch). Push it through the chapter 3 § *the pre-publication legal review* checks. This often becomes the single most-shared asset from the talk.
- **Draft the post-talk retrospective — before the talk.** 1 page. Imagine the talk has been delivered; write the retrospective you would wish to have written. What landed, what did not, what the hallway said, what you would cut, what you would add. Writing the retrospective in advance is a form of pre-mortem — it surfaces where you are still unsure about the talk's shape.
- **Compose with exercise-02.** If exercise-02's draft is the paper or blog that provides the keynote's deep-dive substrate (chapter 4 § *the deep-dive → the paper or blog*), add explicit cross-links: the keynote's `outline.md` cites specific sections of exercise-02's `draft.md`; exercise-02's `draft.md` closing cites this keynote as the directional sibling artifact. The cross-linking is the chapter 3 § *the paper-plus-blog fan-out* pattern lifted to paper-plus-keynote.
- **Compose with exercise-04.** If the take-away artifact is the open-source release from exercise-04, confirm that chapter 5's maintenance contract (exercise-04's release proposal) is ratified before the keynote commits to the release as the take-away. Chapter 5 failure mode: *the open-source dump* is what unratified take-aways produce.
- **Draft the panel-conversion plan.** Even if the slot is a plenary keynote today, state the plan if the organisers downgrade it to a panel (which happens). The panel-variant appendix is where this plan lives; the stretch is to make it fully operable.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-03-keynote-outline-and-faq/` is what you extend across quarters: the through-line and the FAQ carry forward into the actual slide deck authoring (outside this exercise); the hallway-track plan is executed at the conference and retroactively annotated with what actually happened; the pre-flight readout stacks across rehearsal cycles as additional peer summaries land. The take-away artifact (if a reference diagram or decision framework) often becomes a canonical mod-503 chapter 5 living diagram once redacted; cross-reference accordingly.
