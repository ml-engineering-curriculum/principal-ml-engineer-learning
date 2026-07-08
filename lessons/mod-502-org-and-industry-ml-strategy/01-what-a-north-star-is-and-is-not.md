# What a Multi-Year ML Technical North Star Is — and Is Not

> Chapter 1 of mod-502. Prerequisite: mod-501 chapters 1 and 6 — the verb-object vocabulary and the hand-off contracts. Downstream: every subsequent chapter in this module presupposes the definition this chapter fixes.

## Why start with the definition

"North Star" is the most abused phrase in ML strategy writing. It gets stapled onto quarterly roadmaps, OKR decks, architecture RFCs, launch write-ups, and half-serious internal-community manifestos. Every one of those is a real artifact and useful in its place, but none of them is what the principal-scope postings — SoundCloud (*"define the technical North Star for ML across engineering"*), Pinterest (*"unified technical architecture and defining a roadmap for industry-leading methodology"*), Instacart (*"define & own the Ads Quality technical strategy and roadmap, balancing between both short-term needs and long-term sustainability"*), Capital One (*"drive organization-wide platform innovation"*) — mean by the phrase.

Before the module authors a North Star, the module needs a definition sharp enough that you can look at your own draft and say *this is a North Star* or *this is one of the other artifacts wearing the label*. That is what this chapter does.

## Working definition

A multi-year ML technical North Star for an org is:

> A single, standing document that names the 3-to-5-year technical direction the ML function commits to across product areas, sequenced as a small portfolio of bets with explicit non-goals and sunset criteria, defensible to the CEO / CTO / SVP audience, and stable enough that the org's quarterly roadmaps roll up into it rather than around it.

Read the sentence twice. Every clause is load-bearing.

- **single, standing document** — one artifact, not a folder. Refreshed on a cadence (typically twice a year, plus an emergency refresh when a falsification signal fires — chapter 6); not re-authored from scratch every quarter. If your org has three competing "ML North Star" decks in flight, you don't have a North Star yet; you have a coordination problem the North Star is meant to solve.
- **3-to-5-year** — long enough that the specific model architectures, cloud SKUs, and framework versions in circulation *today* are largely irrelevant to whether the direction is right. Short enough that a first-year MBA on the CFO's staff can still be around to see the outcome. Any horizon shorter than three years is portfolio-roadmap territory (chapter 5); any horizon longer than five is a manifesto.
- **technical direction the ML function commits to** — not the product's OKRs, not the executive branch's headcount plan. Direction that only a technical leader in the ML function can author, and that binds the ML function's engineering decisions.
- **across product areas** — the scope is the whole ML org, not the ranking team, not the Gen-AI team, not the RecSys stack. Across three-to-five product areas' worth of ML systems and the platforms they share.
- **small portfolio of bets** — the North Star is not one thing; it is a shape the bets form. Chapter 2 gives the five-row shape the sample supports. "Small" is important — three to five bets, not fifteen. If everything is a bet, nothing is.
- **explicit non-goals and sunset criteria** — the discipline that distinguishes a North Star from a manifesto (chapter 4). Every bet named on the positive side of the ledger has to have a matching non-goal on the negative side, and every bet has to have a criterion that would end it.
- **defensible to the CEO / CTO / SVP audience** — the audience is unambiguously executive. Not "someone above the VP" — the CEO, CTO, or the SVP the CTO defers to on ML direction. If the SoundCloud sentence *"define the technical North Star for ML across engineering"* were about a VP-audience roadmap, it would have said VP.
- **quarterly roadmaps roll up into it** — the seam mod-501 chapter 6 named. The staff-scope portfolio roadmap does not disagree with the North Star; it decomposes into it. Chapter 5 in this module works through the seam.

Every subsequent chapter in this module refines one of those clauses.

## The SoundCloud framing as a template

SoundCloud's Senior Principal ML posting names the artifact explicitly and — importantly — does not scope it to one product area:

> "Define the technical North Star for ML across engineering."

Object: `the technical North Star for ML across engineering`. Scope: the entire engineering org's ML function — SoundCloud's recommendation stack, its search stack, its ads stack, its content-understanding stack, and its shared platforms all fall under it. The verb `define` is the classical principal-scope framing: not "propose", not "align on", but `define`. The person named in the posting *sets* what the direction is, then argues it up (chapter 6 in this module — falsification signal; mod-504 — the SVP / CTO consensus practice).

This framing is the template because it is the cleanest single-sentence load-bearing statement of the object in the sample. Every North Star this module walks you through authoring is a variant of it — same verb, same altitude of object, different specific org.

## The Pinterest framing as the architecture-adjacent variant

Pinterest's Principal ML Engineer, Content Recommendations posting names the same class of artifact but from an architecture-facing angle:

> "Unified technical architecture and defining a roadmap for industry-leading methodology."

Object A: `unified technical architecture` — this belongs to mod-503, the north-star applied-ML architecture. Object B: `roadmap for industry-leading methodology` — this belongs here. The Pinterest phrasing is a useful reminder that the North Star and the north-star architecture are paired artifacts: the strategy names the bets; the architecture names the seams the bets plug into. Mod-503 chapter 1 handles the pairing from the architecture side.

For a learner coming out of a staff-scope background, the Pinterest framing is often the easier on-ramp: you already know how to argue architecture; the North Star is *"the architecture argument, plus the bets that shape it, plus the sequencing, plus the sunset criteria, at 3-to-5-year horizon, for an executive audience"*.

## What a North Star is not

Each of these is a real, useful artifact. None of them is a North Star. Naming them explicitly is how you keep your own draft honest.

### Not a portfolio roadmap

The staff-scope portfolio roadmap (owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410) commits leadership to multi-quarter delivery on 3–5 production ML systems. Its audience is the VP; its horizon is the fiscal year; its scope is the portfolio; its unit of commitment is the quarter. The North Star's audience is the CTO / SVP / board; its horizon is 3-to-5 years; its scope is the whole ML function; its unit of commitment is the bet. Chapter 5 in this module works through the seam.

Signs your draft is a portfolio roadmap in North Star clothing: the milestones are dated to specific fiscal quarters; the metrics are the current fiscal year's OKR metrics; the risks are project-execution risks (staffing, dependencies, delivery date). None of those belong in a North Star.

### Not a set of OKRs

OKRs commit the ML function to *measurable outcomes* in a specific time window. A North Star commits the ML function to a *direction* over multiple time windows. The two artifacts can be consistent — every OKR the ML function commits to should be traceable back to a North Star bet — but they are not the same artifact.

Signs your draft is an OKR sheet in North Star clothing: it reads as a bullet list of KRs; every bet has a percentage-target metric attached; there is no place in the document where non-goals or sunset criteria appear. Chapter 4 handles the last of those.

### Not an architecture document

The north-star applied-ML architecture (mod-503) is the *converged systems shape* the whole ML org points at. It has diagrams. It has canonical APIs. It is the answer to "where does this new component fit?" A North Star is the answer to "what are we betting on, why, and what would make us stop?" The two documents cite each other but are not each other.

Signs your draft is an architecture document in North Star clothing: the load-bearing artifacts are diagrams; the audience is engineers, not executives; the failure mode of the document is "we drew the boxes wrong", not "we bet on the wrong direction".

### Not a manifesto

A manifesto is a values statement. It commits the ML function to a way of working ("we default to rigorous eval before launch", "we prefer paved roads over per-team stacks"). Values statements are useful — mod-505 in this track handles the ones that shape the technical bar — but they are not a North Star. A North Star has decisions in it. A manifesto has aspirations.

Signs your draft is a manifesto in North Star clothing: every bet reads as a value ("we invest in Gen-AI"); no bet has a rejected alternative named next to it; there is nowhere in the document that a reader could disagree with a specific claim rather than a general aspiration.

### Not a market map or industry survey

A market map ("here is who is doing what in Gen-AI / RecSys / agentic-AI") is an *input* to the North Star. It is not the North Star. If your draft reads as a summary of what the AI labs and platform vendors are shipping, you have written the input, not the artifact. Chapter 6 handles the discipline of tracking industry signal as an input.

## The five properties of a defensible North Star

A North Star draft is defensible when it passes all five of these tests. Use them as a checklist:

1. **Cohesion.** The bets fit together. Investing in bet A does not silently un-invest bet B. A reader can trace a coherent story across the portfolio.
2. **Non-triviality.** The bets are *choices*. A different, competent principal at a peer org could plausibly have named a different portfolio; you can argue why yours is right and theirs is wrong for this org.
3. **Falsifiability.** The bets can be shown to be wrong. Chapter 6 works through the industry and internal signals that would falsify a specific bet. A North Star that cannot be falsified is a manifesto.
4. **Ownership legibility.** For every bet in the portfolio, the principal-scope owner is named (typically the principal author of the North Star, adjudicated), and the staff-scope owner of the underlying implementation is named (see the hand-off contracts in mod-501 chapter 6). Nobody has to guess who is holding which end.
5. **Executive readability.** A CTO or SVP can read the one-pager in five minutes and quote the top-line bet portfolio back accurately. Chapter 7 in this module walks through the one-pager craft.

If a draft fails any one of these, the fix is usually earlier in the document than the fix appears. Cohesion failures come from bad sequencing (chapter 3); falsifiability failures come from missing sunset criteria (chapter 4) or missing signal tracking (chapter 6); executive readability failures come from confusing the one-pager audience with the deep-dive audience (chapter 7).

## A worked micro-example

For grounding, here is what a *single row* of a North Star (Gen-AI direction) reads like at principal altitude. The full portfolio is chapter 2's job.

> **Gen-AI direction (3-to-5-year, org-wide).** Adopt frontier foundation models via API for user-facing text and multimodal features. Post-train a single mid-tier open-weights model in-house for the two workloads where the API economics or the data-residency posture do not clear the bar (defined below). Do *not* build a foundation-model pretraining program in this window. Sunset the in-house post-training program if frontier API pricing per million tokens falls below the fully-loaded per-token cost of the in-house model at expected FY-end volume; sunset the API-adoption bet if a supplier's terms materially degrade against the org's data-residency contract with our largest regulated customer segment.

Notice what is *not* in that paragraph: parallelism recipes (`ai-infra-performance-learning`), specific model choices (staff, per-bet RFC), quarterly milestones (staff portfolio roadmap), OKR percentage targets. What *is* in it: the direction, the boundary the direction implies (non-goal: don't build a pretraining program), the specific criterion that would end each side of the bet.

A staff engineer reading this row can build a quarterly roadmap from it. A CTO reading this row can quote the bet portfolio back accurately in a board meeting. That is the standard the North Star has to hit.

## Summary

- A multi-year ML technical North Star is a single, standing document naming the 3-to-5-year direction across product areas, sequenced as a small portfolio of bets with explicit non-goals and sunset criteria, defensible to CEO / CTO / SVP.
- SoundCloud's *"define the technical North Star for ML across engineering"* is the cleanest single-sentence framing in the sample. Pinterest's *"unified technical architecture and defining a roadmap for industry-leading methodology"* is the architecture-adjacent variant.
- A North Star is *not* a portfolio roadmap, an OKR sheet, an architecture doc, a manifesto, or a market map. Each of those is a real artifact; each rides in a different lane.
- Five defensibility tests — cohesion, non-triviality, falsifiability, ownership legibility, executive readability — every draft has to pass.
- Every subsequent chapter of the module sharpens one clause of the working definition. Chapter 2 hands you the five-row bet portfolio shape.
