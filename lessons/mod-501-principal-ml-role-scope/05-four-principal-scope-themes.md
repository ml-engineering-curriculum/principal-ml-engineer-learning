# The Four Principal-Scope Themes and How to Self-Assess

> Chapter 5 of mod-501. Prerequisite: chapters 1–4. This chapter names the four principal-scope themes at ≥0.60 in-window frequency, plus the below-threshold industry-influence theme, and teaches you to place yourself against them.

## The four themes at material frequency

The 26-posting sample analysed in [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) surfaces exactly four principal-scope requirement themes above the 0.60 in-window frequency floor:

| # | Theme | Freq | Requirement ID (in curriculum plan) | Module owner |
|---|---|---:|---|---|
| 1 | Org- and industry-wide ML technical strategy | 0.92 | `req-org-industry-strategy` | mod-502 |
| 2 | Applied-ML architecture at portfolio-and-industry altitude (north-star platform architecture with living diagrams and canonical APIs) | 0.85 | `req-applied-ml-architecture` | mod-503 |
| 3 | Cross-org influence without authority (up to VP / SVP / CTO) | 0.69 | `req-cross-org-influence` | mod-504 |
| 4 | Principal mentorship + technical-bar calibration for the ML org | 0.65 | `req-principal-mentorship-and-bar` | mod-505 |

A fifth theme sits below the 0.30 material threshold in the 2026-Q2 sample but is called out in the role definition itself:

| 5 | Industry influence / external voice — publications, keynotes, open-source thought leadership | 0.15 | `req-industry-influence` | mod-506 |

Mod-506 is held at 10 hours precisely because the in-window evidence is thin; the module exists because the role definition names it, not because the sample demands it. The `authoring_note` in `.aicg/curriculum-plan.json` re-visits this on the 2026-10-08 re-sample.

Together, these five themes are the entire principal-owned surface of this track. Everything else in a real Principal / Distinguished ML posting maps back down to `staff-ml-engineer-learning` (portfolio scope), `senior-ml-engineer-learning` (single-team scope), or peer specialist tracks. Chapter 6 draws the specific hand-off contracts.

## Theme 1 — Org- and industry-wide ML technical strategy

**What you own.** The ML function's technical direction across product areas. The multi-year modelling roadmap the ML org commits to. The Gen-AI / RecSys / agentic-AI / foundation-model bets you sequence, and the non-goals / sunsets that fall out of that sequencing. The paragraph the CTO reads.

**What you do NOT own.** The multi-team portfolio roadmap for a single product area (owned by Staff, `staff-ml-engineer-learning` mod-410). The organisation's P&L or headcount plan (owned by Family 2). The research agenda (owned by Family 3).

**How to recognise the signal in your own history.** Have you ever authored the ML function's multi-year direction, defended it to executives above your VP, and had that document survive as a reference the next fiscal year's investment plan was scoped against? Have you had to publicly sunset a bet — not because it failed, but because it no longer fit the direction — and defended that call to product? If yes to both, this theme is lived experience. If you have only ever scoped a multi-quarter portfolio roadmap for one product area, this theme is level-up work.

**What mod-502 does to lift you.** It walks through the North Star document itself, the sequencing of bets across product areas, the CTO-audience narrative, the non-goals / sunset criteria, and the difference between the staff-scope portfolio roadmap and the principal-scope org direction.

## Theme 2 — Applied-ML architecture at portfolio-and-industry altitude

**What you own.** The living north-star architecture the whole ML org converges on — living diagrams, canonical APIs (feature store, model registry, eval, inference gateway, training platform contract), reference architecture that a new bet plugs into without a rewrite. Chip Huyen's *Designing Machine Learning Systems* is the closest shared vocabulary.

**What you do NOT own.** The build of the platform (owned by peer platform tracks `ai-infra-ml-platform-learning`, `ai-infra-mlops-learning`, `ai-infra-performance-learning`). The single-system architecture RFC for one production system (owned by Senior). The multi-system RFC for a portfolio (owned by Staff).

**How to recognise the signal in your own history.** Have you drawn — and maintained — a single canonical diagram that every ML team in the org points at when they need to argue where a new component fits? Do the paved-road platform teams use your architecture doc as the consumer contract they build to? Have you evolved the canonical APIs across multiple bets without rewriting from scratch? If yes, lived experience. If you have only ever authored a system-scope or portfolio-scope architecture RFC, level-up work.

**What mod-503 does to lift you.** It walks through the north-star architecture artifact itself, the canonical API contracts (feature, registry, eval, inference), the evolution plan across bets, and the org-wide architecture-review body that blocks / nudges / escalates.

## Theme 3 — Cross-org influence without authority up to SVP / CTO

**What you own.** Coalition-building across ML, platform, product, security, governance, finance, and legal. Consensus at the org level for a bet neither you nor your VP has line authority over. Escalation and deferred-decision protocols. Partnership contract with the peer executive branch — the Head of AI / CAIO / Head of AI Governance / CISO / CFO.

**What you do NOT own.** The exec-audience RFC as a portfolio-scope artifact (owned by Staff at `staff-ml-engineer-learning` mod-410 exercise-02). The line authority to force a decision. The mandate that comes with headcount.

**How to recognise the signal in your own history.** Have you driven a bet across the ML function that required a VP outside your reporting chain to agree, and got that agreement without a formal executive escalation? Have you sat in an SVP or CTO's review as the ML function's technical voice and had them defer to your framing? Have you built a coalition around a bet that outlasted the specific system that motivated it? If yes, lived experience. If you have only ever led portfolio-scope alignment with peer VPs inside your ML function, level-up work.

**What mod-504 does to lift you.** It walks through the coalition-sequencing discipline, the executive-branch partnership contract, the SVP / CTO / CFO / CISO audience-shaping practice, the escalation and deferred-decision protocol, and the distinction between principal-scope executive audience and staff-scope executive audience.

## Theme 4 — Principal mentorship and technical-bar calibration for the ML org

**What you own.** Coaching staff engineers (L40) through their staff-plus work — the multi-team blueprint, the exec-audience RFC, the portfolio TCO defence. Sitting on staff-plus hiring loops as a calibrator, not just an interviewer, and setting the loop-level bar. Setting the review bar the ML org calibrates against — the design-review, RFC-review, launch-review standards every team follows. Multiplying the effectiveness of every ML team via a small number of leverage moves (Upstart: *"multiply the effectiveness of every ML team"*).

**What you do NOT own.** Coaching senior tech leads through single-team scope (owned by Staff at `staff-ml-engineer-learning` mod-410). Direct people management, 1:1s, performance reviews, headcount (owned by the peer EM path and Family 2). Interviewer-level calibration for senior hires (owned by Staff).

**How to recognise the signal in your own history.** Have you coached a staff engineer through leadership-commit on their portfolio-scope RFC and left them stronger for the next one? Have you sat on a staff-plus hiring loop as a calibrator, adjudicated an interviewer split, and had your call ratified by the hiring committee? Have you set the ML org's design-review standard — the rubric other teams use? If yes, lived experience. If you have only ever coached L20 / L30 engineers or interviewed at the individual-interviewer altitude, level-up work.

**What mod-505 does to lift you.** It walks through the small-leverage-move discipline, the staff-plus hiring loop calibration practice, the technical-bar authoring, the multiplier-not-manager identity, and the sustained-principal-signal cadence over years.

## Theme 5 — Industry influence and external voice (below-threshold)

**What you own.** Publications at the applied-ML industry-track venues (ICML / NeurIPS / KDD industry track, O'Reilly AI, applied-ML engineering blogs on your own employer's engineering blog). Conference keynotes and technical talks. Open-source contributions at principal altitude — release-level decisions on a widely used library, not day-to-day commits. Internal-community thought leadership on the ML function's direction. Return-on-external-influence tracking with retirement criteria for artifacts that stop paying rent.

**What you do NOT own.** First-author top-tier ML research submissions (owned by Family 3). Public representation of the org as its formal spokesperson (owned by Family 2 / marketing). Product marketing of specific ML features.

**How to recognise the signal in your own history.** Have you published a piece that another ML org's staff-plus engineer explicitly cited when scoping a comparable bet? Have you given a keynote at an applied-ML conference and had the artifact circulate internally at multiple orgs? Have you shepherded an open-source ML tooling release that another org's paved road adopted? If any of these, lived experience. If none, level-up work — and this is the module the smallest fraction of the sample corroborated (0.15 freq), so the level-up move is deliberate practice rather than urgent gap-closure.

**What mod-506 does to lift you.** It walks through the applied-ML industry-track submission craft, the keynote-craft discipline, the open-source-at-principal-altitude standard, and the return-on-external-influence tracking. Held at 10 hours because the evidence is thin.

## Placing yourself: a five-cell self-assessment

Take a working document — a private markdown file, a page in your engineering journal, whatever you already use — and, for each of the five themes above, fill in five cells:

1. **The theme statement in your own words.** One sentence. If you can't state it in your own words, chapter 5 hasn't landed yet — re-read this chapter's theme section.
2. **Lived experience — the strongest artifact you already have.** A specific document, deck, initiative, or outcome that carries this theme. Not a story about the theme; the artifact itself. If you can't name one, this is level-up work.
3. **The gap between where you are and the theme's principal-altitude object.** Concrete. Not "I need to think more strategically" — instead, "I have led portfolio-scope alignment across three teams but never SVP-level, so I have never had to shape the material my VP would use to bring an SVP along."
4. **The learning move.** Which module lifts you on this theme (see the table at the top of the chapter). Which project integrates it. And — critically — what field opportunity, current or upcoming, will let you actually practice at principal altitude, not just study.
5. **The retirement criterion.** How will you know you have lifted from level-up to lived-experience on this theme? Name a specific artifact or a specific outcome. If you cannot name a criterion, you cannot tell when you're done.

The five-by-five grid is the deliverable exercise-04 asks you to produce and defend.

## Where uneven placement is normal

Almost nobody starts this track with lived experience on all five themes. Most learners come in with strong lived experience on theme 4 (mentorship + bar — the natural extension of staff-scope work), reasonable lived experience on theme 1 (some form of multi-quarter roadmap authoring), and level-up work on themes 2, 3, and 5. That shape is normal.

The pattern that should give you pause is *"lived experience on all five themes already"*. If that is your read after the self-assessment, one of two things is true: either you are already operating at Family 1 altitude in the field and this track is a formalisation cycle (fine — treat it as a defensibility check), or the self-assessment was too generous (also common — read chapter 2 again and pressure-test each cell against the verb-object altitude, not the adjective density).

## Summary

- Four principal-scope themes sit at ≥0.60 in-window frequency: org-industry strategy, north-star architecture, cross-org influence, principal mentorship + technical bar. A fifth (industry influence) is below the material threshold but is called out in the role definition.
- Each theme has a scope-owned lower bound (what a staff engineer would author) and a scope-owned upper bound (what an executive would author). The principal-scope layer sits between them.
- Uneven placement is normal. Even placement is suspicious.
- The five-by-five self-assessment is exercise-04's deliverable and the working document you carry across the rest of the track.
