# The Two Paired Artifacts — The Executive One-Pager and the Deep-Dive Companion Doc

> Chapter 7 of mod-502. Prerequisite: chapters 1–6. Downstream: exercises 01 (one-pager) and 03 (multi-year roadmap with non-goals and sunsets) apply this chapter directly; project-501 defends the pair in front of a simulated SVP / CTO panel.

## Why two artifacts, not one

A North Star has two audiences and two very different reading modes. A CTO / SVP reads for direction, boundary, and defensibility — five minutes, one focused reading, followed by a Q&A session. A staff engineer reads for enough decomposition to build the current fiscal year's roadmap — 30 to 60 minutes, referenced repeatedly across the quarter. A single document cannot serve both readings well without one of two failure modes: either it is too dense for the CTO reading and gets abandoned three paragraphs in, or it is too shallow for the staff-engineering reading and the roadmap gets built off vibes and hallway lore.

The paired artifact is the resolution. **The one-pager** is the executive-audience artifact — one page, five minutes, quotable. **The deep-dive companion doc** is the staff-engineer-audience artifact — fifteen to twenty-five pages, hyperlinked to the tracker (chapter 6), the sunset criteria (chapter 4), the hand-off contracts (mod-501 chapter 6), and the north-star architecture (mod-503).

Both artifacts are always shipped as a pair. Neither replaces the other. Neither can be read in isolation and produce the intended reader response.

## The executive-audience one-pager

### Purpose

A single page a CTO / SVP can:

- read in five minutes on their own time,
- summarise back accurately in a board meeting or a peer-review conversation,
- and cite as the source of the ML function's technical direction for the next 3-to-5 years.

If any one of those three readings fails, the one-pager needs a rewrite. This is the acceptance bar.

### Shape

An effective one-pager has six named sections. Each is short.

1. **Direction (2–3 sentences).** The one-sentence answer to "where is the ML function going?", followed by a one-sentence *why now*. Nothing more. The sentence a CTO can quote is here.
2. **Bet portfolio (5 bullet rows, one per chapter-2 row).** Per bullet: bet name, one-clause posture, one-clause current-year state (bet / hedge / option / not-in-window from chapter 3). Nothing more.
3. **Non-goals (3–5 bullets).** The single most important non-goals across the portfolio. Not the full non-goal set — that lives in the deep-dive. The ones a CTO needs to have in mind to defend the direction to their peers.
4. **Signal watch (2–3 bullets).** The most material industry / regulatory / cost signals from the tracker (chapter 6) that could shift a bet in the next six months. Not the full tracker.
5. **What we ask of leadership (3 bullets).** The specific asks the CTO / SVP is committing to when they ratify the North Star. Typically: a capacity envelope, a hiring shape, a partnership commitment (e.g., "quarterly review touchpoint with Head of AI Governance").
6. **Refresh cadence (1 sentence).** When the North Star is next refreshed and what would trigger an emergency refresh.

That is the entire one-pager. Nothing else fits on a page that also has to be quotable in five minutes.

### Writing discipline

Three specific discipline notes.

**The direction sentence is the whole document in miniature.** If the one sentence at the top does not make sense on its own, the rest of the page cannot save it. Draft this sentence early and rewrite it more than any other sentence in either artifact. Model: *"Over the next four years the ML function converges its production ML onto a shared paved-road substrate, invests in Gen-AI as an integration bet with a targeted post-training program on the enterprise side, and holds foundation-model pretraining out-of-window absent named revisit signals."* That one sentence carries most of the load; the rest of the page defends it.

**No numbers on the one-pager unless the number is load-bearing.** Percentage targets, cost figures, headcount numbers, and dates below the year-1 / year-2 / year-3 granularity belong in the deep-dive. On the one-pager, they read as false precision to an executive audience and invite the wrong kind of Q&A.

**No jargon that a CTO would not know without an ML engineering background.** The audience is executive, and while a CTO usually has a strong technical foundation, they are not in the ML weeds day-to-day. Terms like *Chinchilla-optimal*, *MFU*, *FSDP*, *reranker*, and *MoE ranker* belong in the deep-dive. Terms like *foundation-model pretraining*, *frontier-API adoption*, *paved-road substrate*, and *sunset criterion* belong on the one-pager and are worth spending one line to make sure a reader has the working definition.

### Common failure modes

- **The one-pager overflows to two pages.** Almost always because the bet portfolio has drifted into per-bet paragraphs. Cut back to bullet rows; move the paragraphs to the deep-dive.
- **The one-pager reads as an executive summary of the deep-dive.** It should read as its own artifact, produced *before* the deep-dive existed, that would still make sense on its own. If the one-pager only makes sense to someone who has read the deep-dive, the deep-dive has swallowed the one-pager.
- **The one-pager treats the CTO as the target reader for justification.** The CTO is the target reader for *direction and commitment*. Justification lives in the deep-dive. The CTO reads the one-pager to know what they are agreeing to and to be able to quote it accurately. The deep-dive is where they go if they need to defend a specific decision — but almost always, they will send the deep-dive to a peer or a staff engineer for that.

## The deep-dive companion doc

### Purpose

A 15-to-25 page artifact a staff engineer can:

- read in 30–60 minutes,
- build a fiscal-year portfolio roadmap from,
- reference across the quarter as directional truth,
- and use as the source when their team asks whether a given proposed effort is on-strategy or off.

The staff engineer's roadmap-authoring session, if the deep-dive is doing its job, ends with confidence about the year-1 bets, the non-goals to respect, and the sunset criteria to be alert to.

### Shape

Twelve named sections. Each has a purpose; none are optional.

1. **Direction and audience.** Restate the one-pager's direction sentence, and name the audiences (CTO / SVP; staff engineers building against the North Star). One page.
2. **Context and history.** What the org's previous multi-year direction was (if one existed), what changed, and why the refresh cycle produced this document now. Two to three pages. Grounds the reader in the *why now* answer at more depth than the one-pager could.
3. **The five bet rows.** One page per row: bet framing (chapter 2), current-year state (chapter 3), non-goals (chapter 4), sunset criteria with all three parts (chapter 4), specialist-track hand-off (mod-501 chapter 6). Five pages total.
4. **Sequencing across the 3-to-5-year window.** The chapter-3 grid at full detail: what is a bet / hedge / option / not-in-window in each year, timeliness arguments per year-1 bet, flip signals per hedge, revisit conditions per not-in-window row. Two pages.
5. **Coherence with the peer platform-side principal's mod-505 grid.** Explicit cross-references to the platform bets. Where the modelling bets depend on platform bets; where the platform bets are already committed vs. still uncertain. One to two pages.
6. **The seam with the portfolio roadmap.** The chapter-5 hand-off contract, made specific to the current fiscal year. Which staff engineers are the counterpart owners; which artifacts flow which direction; the escalation path. One page.
7. **Signal tracker snapshot.** The chapter-6 tracker in its current-refresh state — per bet, the signals being watched, the current values, the decision log for the previous refresh cycle. Two to three pages.
8. **Refresh cadence and emergency triggers.** The formal cadence and the specific emergency-refresh triggers for this refresh cycle. Half a page.
9. **The what-we-ask-of-leadership section, expanded.** The one-pager's asks made concrete: named capacity envelope, named hiring shape, named partnership commitments, named review touchpoints. Two pages.
10. **The non-goal register.** The full set of non-goals across all bet rows, indexed by row and by named consequence. Two pages.
11. **Open questions and known unknowns.** The specific decisions the principal has *not yet made* and expects to make at the next refresh, along with the signal or the input that will make the decision possible. One page.
12. **Appendices.** Pointers to the north-star architecture (mod-503), the responsible-AI review process, the hiring calibration (mod-505 in this track), the tracker's raw source list, and the previous refresh cycle's decision log. Two to three pages.

Total: 15–25 pages depending on how much history, how much detail on the tracker, and how many bets are in play.

### Writing discipline

**Every claim traces to a chapter or a peer artifact.** The deep-dive is not the place for freestanding claims; every substantive claim cites the chapter that produced the framework (chapter 2 for bet framing, chapter 4 for sunsets, chapter 6 for signals) or a peer artifact (`staff-ml-engineer-learning` mod-407 for cost, `head-of-ai-governance-learning` for regulatory, `ai-infra-principal-engineer-learning` mod-505 for platform bets). This is what lets the deep-dive stay small: it does not re-argue anything from scratch.

**Sections stand alone.** A staff engineer building the ranking-team's roadmap needs to be able to read only the sequencing section, the row-2 bet paragraph, and the seam-with-roadmap section, and get their job done. Force yourself to write sections that are self-contained.

**No hidden decisions in the appendix.** The appendix is for pointers, not for load-bearing decisions the CTO's staff engineer might miss. If a decision matters, it is in one of sections 3, 4, 6, 7, or 9.

**Version control and stable slugs.** The deep-dive gets referenced by URL / anchor in future roadmap RFCs. Every section header has a stable slug that survives the next refresh. This is boring hygiene and pays back over multi-year use.

### Common failure modes

- **The deep-dive is a long one-pager.** Symptoms: the tracker snapshot is missing; the hand-off contract with the roadmap is a paragraph, not a page. Fix: build sections 5, 6, 7, and 9 out; they are the ones a staff engineer will spend the most time in.
- **The deep-dive re-argues the bet from scratch.** Symptoms: the row 4 (foundation-model program) not-in-window section spends four pages defending the choice. Fix: the argument is chapter 4's; the deep-dive cites it. Save the space for the specific *this org, this year* details.
- **The deep-dive has an audience-of-one problem.** The document is written for the principal's own re-reading, not for the staff engineers who will actually use it. Fix: get a real staff engineer to walk through the document and try to build a fake roadmap from it. Refine.

## How the pair ships together

Practical logistics.

- **Both artifacts refresh together.** The one-pager cannot be updated without a corresponding deep-dive refresh, even if the deep-dive change is small. Version them jointly.
- **The one-pager is what circulates upward.** Board decks, CTO briefings, SVP escalations — the one-pager is what gets sent. The deep-dive is available on request; it is not the artifact that leadership consumes on the review cadence.
- **The deep-dive is what circulates downward.** VPs, staff engineers, the peer platform-side principal, Head of AI Governance, CFO's team on the capacity envelope — they read the deep-dive. They will *also* have seen the one-pager, but the deep-dive is where their work is anchored.
- **The pair goes into the org's canonical docs repository.** Not a private folder. Not the principal's own inbox. In a place the whole ML org can find, cite, and consult — the same place the mod-503 north-star architecture ships. If the org has no canonical docs home, chapter 6 of mod-503 handles the pattern.
- **The pair is tied to the North Star's refresh cadence** — twice a year plus emergency refresh. Old versions stay in place with a *superseded on YYYY-MM-DD by vN+1* header so peers can see the history.

## The interview / defense session

Once the pair exists, the principal's job in mod-504 (cross-org influence) picks up: defending the pair to a live CTO / SVP audience, walking a peer VP or Head of AI Governance through the seams, and running the ratification conversation. The mod-504 material is where that practice lives; this chapter's job is only to ensure the artifacts are ready.

Two lightweight self-tests before mod-504:

1. **The five-minute test.** Give the one-pager to a peer who has never seen the document. After five minutes, ask them to summarise the direction and the bet portfolio. If they can do it, the one-pager works; if not, cut and rewrite until they can.
2. **The staff-engineer test.** Give the deep-dive to a staff engineer who owns one of the affected teams. After 45 minutes, ask them to draft one paragraph of their team's next-quarter plan. If the paragraph is coherent with the North Star, the deep-dive works; if not, the section that failed them needs a rewrite.

## Summary

- The North Star ships as two paired artifacts: the executive-audience one-pager and the deep-dive companion doc. Neither replaces the other; both refresh together.
- The one-pager is a single page with six named sections — direction, bet portfolio, non-goals, signal watch, what-we-ask-of-leadership, refresh cadence. Quotable in five minutes.
- The deep-dive companion is a 15-to-25 page document with twelve named sections — from context through open questions to appendices. Buildable-from in 30–60 minutes for a staff engineer.
- The one-pager surfaces the material shifts; the deep-dive carries the full detail. The one-pager is not an executive summary of the deep-dive.
- The pair ships to the canonical docs home, is versioned together, refreshes twice a year plus emergency, and is what mod-504 defends to the executive audience.
