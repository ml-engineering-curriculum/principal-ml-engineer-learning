# mod-502-org-and-industry-ml-strategy: Org- and Industry-Wide ML Technical Strategy — The Multi-Year North Star and the Technical Bet Portfolio

**Estimated effort:** 14 hours

Mod-501 established the vocabulary that separates level-48 principal scope from level-40 staff scope. This module authors the first — and highest-frequency — principal-scope artifact the sample points to: the ML function's **multi-year technical North Star** and the **bet portfolio** behind it. The theme was cited by 24 of 26 postings in the 2026-Q2 sample (0.92 frequency, the highest of any theme in the track) and is grounded in the SoundCloud *"define the technical North Star for ML across engineering"* and Pinterest *"unified technical architecture and defining a roadmap for industry-leading methodology"* framings.

The module is deliberately not an implementation curriculum for the underlying technologies. The peer specialist tracks (`fine-tuning-engineer-learning`, `training-pipeline-engineer-learning`, `agentic-ai-engineer-learning`, `ai-infra-ml-platform-learning`, `ai-infra-performance-learning`) own the *how* of each bet; `staff-ml-engineer-learning` mod-403 / mod-404 / mod-407 / mod-409 owns the portfolio-scope engineering. This module owns the *whether, when, for how long, and against what falsifier* — the strategic bet altitude, one rung above staff-scope portfolio roadmap.

Read the chapters in order. Chapters 1–2 set up what a North Star and a bet portfolio are; chapters 3–4 sequence the bets into a multi-year roadmap with non-goals and sunset criteria; chapter 5 draws the seam back to the staff-scope portfolio roadmap owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410; chapter 6 handles the industry-signal tracking that keeps the North Star honest; chapter 7 walks through the two writing artifacts a principal ships.

## Learning objectives

- Author the multi-year ML technical North Star for an org — the 3-to-5-year direction across product areas that leadership commits to — using the SoundCloud *"define the technical North Star for ML across engineering"* and Pinterest *"unified technical architecture and defining a roadmap for industry-leading methodology"* framings as templates.
- Frame the org's ML bet portfolio at the same altitude the peer platform-side principal track uses (see [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) mod-505-long-term-technical-bets) — but for the modelling side: Gen-AI direction (integration vs. build-vs-buy of foundation models), RecSys/personalization direction (org-scope stack and metrics), agentic-AI direction (bet size and time horizon), foundation-model / large-scale fine-tune program direction, MLOps discipline as an org contract. Do NOT duplicate the technology-specific implementation depth those bets rest on — the peer specialist tracks own that; the principal owns the bet.
- Sequence the North Star into a defensible multi-year roadmap: which bets get made in year 1, which are hedges, which are options to preserve — and articulate the non-goals and the sunset criteria for each bet.
- Reason about the difference between a portfolio roadmap (staff scope, owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410-staff-plus-technical-leadership) and a multi-year org-scope North Star (this scope): the former commits leadership to quarters, the latter commits leadership to a direction the CEO / CTO / board can quote.
- Track industry signal that would falsify or accelerate the North Star — publications from AI labs, cost/compute-generation shifts, regulatory shifts (EU AI Act obligations, NIST AI RMF updates), and the internal metrics that surface trouble early.
- Author the executive-audience North Star one-pager and the deep-dive companion doc — the pair a CTO / SVP can read in 5 minutes and a staff engineer can build a quarterly roadmap from.

## Chapters

1. [`01-what-a-north-star-is-and-is-not.md`](01-what-a-north-star-is-and-is-not.md) — What a multi-year ML technical North Star *is* (the 3-to-5-year direction leadership commits to and a CEO / CTO / board can quote) and what it *is not* (a portfolio roadmap, a set of OKRs, an architecture doc, a manifesto). Grounded in the SoundCloud and Pinterest framings.
2. [`02-the-ml-bet-portfolio-frame.md`](02-the-ml-bet-portfolio-frame.md) — The five-row bet portfolio at principal altitude: Gen-AI direction, RecSys/personalization direction, agentic-AI direction, foundation-model program direction, MLOps as org contract. The bet framing — not the recipe. Explicit hand-offs to the specialist tracks that own the recipe.
3. [`03-sequencing-bets-hedges-and-options.md`](03-sequencing-bets-hedges-and-options.md) — Sequencing the North Star into a multi-year roadmap: which bets get made in year 1, which are hedges, which are options preserved, and how to defend the sequence.
4. [`04-non-goals-and-sunset-criteria.md`](04-non-goals-and-sunset-criteria.md) — The non-goals and sunset criteria that turn the North Star from an aspiration into a defensible bet. When to *stop* a bet — not because it failed but because the sunset trigger fired.
5. [`05-portfolio-roadmap-vs-north-star.md`](05-portfolio-roadmap-vs-north-star.md) — The seam between the staff-scope portfolio roadmap (owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410) and the principal-scope multi-year North Star (this scope). Why the two artifacts are not substitutes for each other, and how the North Star lifts the roadmap.
6. [`06-tracking-industry-and-internal-falsification-signal.md`](06-tracking-industry-and-internal-falsification-signal.md) — Tracking the industry signal that would falsify or accelerate the North Star — AI lab publications, cost/compute-generation shifts, EU AI Act obligations, NIST AI RMF updates — and the internal metrics that surface trouble early.
7. [`07-authoring-the-one-pager-and-deep-dive.md`](07-authoring-the-one-pager-and-deep-dive.md) — The two paired writing artifacts: the executive-audience one-pager a CTO / SVP reads in five minutes, and the deep-dive companion doc a staff engineer builds a quarterly roadmap from.

## Structure

- `01-…md` … `07-…md`: lecture chapters.
- `exercises/`: five hands-on exercises, one per major objective.
- `labs/`: reserved for the North Star review-simulation lab (see the plan).
- `quizzes/`: knowledge check for the module.
- `resources.md`: cited external references.

## Companion material

- [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) — the 26-posting evidence catalogue. Theme 1 (org- and industry-wide ML technical strategy) at 0.92 frequency is this module's ground truth.
- [`../mod-501-principal-ml-role-scope/`](../mod-501-principal-ml-role-scope/) — the vocabulary and hand-off contracts every chapter here presupposes. Read mod-501 first.
- [`../mod-503-north-star-applied-ml-architecture/`](../mod-503-north-star-applied-ml-architecture/) — the immediately-downstream module. The North Star this module authors *cites* the north-star architecture that module authors; the two artifacts pair.
- [`../mod-504-cross-org-influence-without-authority/`](../mod-504-cross-org-influence-without-authority/) — the module that turns the artifacts here into an SVP / CTO-level decision.
- [`../../projects/project-501-org-ml-north-star-and-reference-architecture/`](../../projects/project-501-org-ml-north-star-and-reference-architecture/) — the capstone that integrates mod-501 through mod-504 into a defended North Star + reference architecture.
