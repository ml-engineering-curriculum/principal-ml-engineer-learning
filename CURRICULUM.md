# Principal Machine Learning Engineer Curriculum

<!-- aicg:orientation:start -->
> **Start here:** [Module 00: Your Relationship to the Model](lessons/00-your-relationship-to-the-model/README.md). Where this role sits relative to the model, what it owns, and who it works with across the five curricula.
<!-- aicg:orientation:end -->

**Role level:** 48 (principal IC altitude, ML engineering ladder — above `staff-ml-engineer-learning` at level 40, below the peer executive branch owned by `chief-ai-officer-learning` / `head-of-ai-governance-learning`)
**Status:** planned — modules and projects below are the planned scope authored from [`.aicg/curriculum-plan.json`](.aicg/curriculum-plan.json). Lessons and projects will be drafted by subsequent autonomous content cycles.

## Overview

This track lifts a level-40 Staff ML Engineer to level-48 principal IC altitude. It does **not** re-teach the multi-team, portfolio-scope, single-team, or build-altitude scope that lower-level tracks own — the [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) (L40) multi-team ML architecture / foundation-model programs / distributed-training strategy / ML platform strategy / cross-team eval / GPU capacity & TCO / portfolio-scope reliability / portfolio-scope responsible-AI / staff-plus tech-leadership curriculum is a prerequisite, as is [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) (L30) beneath that and [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) (L20) beneath that. Instead the track adds the **delta between "portfolio-scope multi-team leader" and "org- and industry-wide leader of the ML function"**: org- and industry-wide ML technical strategy, applied-ML architecture at portfolio-and-industry altitude (living diagrams, canonical APIs), cross-org influence up to the SVP / CTO level without direct authority, principal-level mentorship and technical-bar calibration for the ML org, and the external-voice / industry-influence facet the role definition names as principal-defining.

Total planned commitment: **70 hours** across 6 modules + **75 hours** across 3 projects = **~145 hours**.

The principal-owned surface is deliberately small — four themes at ≥ 0.60 frequency in the 26-posting in-window sample, plus one principal-defining below-threshold theme grounded in role definition rather than in-window frequency. See [`JOB_REQUIREMENTS.md`](JOB_REQUIREMENTS.md) for the requirements-to-coverage map and cited references, and [`.aicg/job-requirements.json`](.aicg/job-requirements.json) for the machine-readable posting evidence.

## Ownership rule

Following the project-wide ownership rule, this curriculum:

- **Inherits** from `staff-ml-engineer-learning` (level 40), `senior-ml-engineer-learning` (level 30), and `ml-engineer-learning` (level 20). Multi-team, portfolio-scope, single-team, and build-altitude scope are prerequisites, not modules — do not start here without them in hand.
- **Owns** org- and industry-wide ML technical strategy (`req-org-industry-strategy`, freq 0.92), applied-ML architecture at portfolio-and-industry altitude (`req-applied-ml-architecture`, 0.85), cross-org influence up to SVP / CTO without authority (`req-cross-org-influence`, 0.69), principal mentorship and technical-bar calibration for the ML org (`req-principal-mentorship-and-bar`, 0.65), and — grounded in role definition rather than in-window frequency — the external-voice / industry-influence facet (`req-industry-influence`, 0.15 in-window; principal-defining per role def).
- **Defers sideways to peer specialist tracks** for all Gen-AI / multimodal / RecSys / MLOps / agentic / RAG / distributed-training / fine-tuning / evaluation implementation depth — `senior-ml-engineer`, `staff-ml-engineer`, `fine-tuning-engineer`, `nlp-engineer`, `training-pipeline-engineer`, `model-evaluation-engineer`, `ai-eval-engineer`, `rag-engineer`, `llm-application-developer`, `applied-ai-engineer`, `agentic-ai-engineer`, `senior-agentic-ai-engineer`, `agentic-systems-architect`.
- **Defers sideways to peer platform tracks** — `ai-infra-ml-platform-learning`, `ai-infra-mlops-learning`, `ai-infra-performance-learning` own the paved-road build; this track owns the org-scope consumer contract at north-star altitude.
- **Defers sideways to peer principal tracks** — [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) and [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) own the platform-side principal scope. The two sides converge at the ML-org-to-platform-org contract, not at re-teaching each other's scope.
- **Defers sideways to peer executive branch** — [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning) and [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) own the executive path (direct reports, headcount, budget, board reporting). This track is the IC-principal counterpart — no direct reports, no P&L, no board-reporting duties.
- **Partners with** `ai-infra-security-learning` (L35) for ML/AI security depth and with `ai-governance-analyst` / `head-of-ai-governance` for governance depth.

See [`JOB_REQUIREMENTS.md`](JOB_REQUIREMENTS.md) for the full requirements catalogue and the cited public references the plan is grounded in.

## Module plan

| Module | Title | Hours | Status |
|---|---|---|---|
| mod-501-principal-ml-role-scope | The Principal ML Engineer Role: IC-Principal Altitude, Titles, and the Distinguished-vs-Principal Boundary | 8 | planned |
| mod-502-org-and-industry-ml-strategy | Org- and Industry-Wide ML Technical Strategy — The Multi-Year North Star and the Technical Bet Portfolio | 14 | planned |
| mod-503-north-star-applied-ml-architecture | North-Star Applied-ML Architecture — Living Diagrams, Canonical APIs, and Org-Scope Reference Architecture | 14 | planned |
| mod-504-cross-org-influence-without-authority | Cross-Org Influence Without Authority — SVP/CTO-Level Consensus and Executive-Branch Partnership | 12 | planned |
| mod-505-principal-mentorship-and-technical-bar | Principal Mentorship & Technical-Bar Calibration for the ML Org | 12 | planned |
| mod-506-industry-influence-and-external-voice | Industry Influence & External Voice — Publications, Keynotes, Open Source, and the References Others Cite | 10 | planned |

## Project plan

| Project | Title | Hours | Status |
|---|---|---|---|
| project-501-org-ml-north-star-and-reference-architecture | Org-Scope ML North Star & Reference Architecture — The Living Artifact | 30 | planned |
| project-502-cross-org-influence-and-technical-bar-simulation | Cross-Org Influence & Technical-Bar Simulation | 25 | planned |
| project-503-industry-influence-artifact-portfolio | Industry Influence & External Voice Artifact Portfolio | 20 | planned |

## Module summaries

### mod-501 — Principal ML Role Scope
The IC-principal altitude vs. the peer executive branch vs. the peer research-principal path. The Distinguished / Sr. Distinguished / Senior Principal title map. The principal-defining verb shift (`set` the ranking model → the portfolio → **the ML org's technical direction across product areas**). Self-assessment against the four principal-scope themes and the hand-off contracts back to staff-plus IC scope. Grounded in the JOB_REQUIREMENTS.md verb-object table and the sampled Capital One / SoundCloud / Instacart / Ibotta / Bumble / Upstart / Snap / Pinterest / GoodRx postings.

### mod-502 — Org- and Industry-Wide ML Strategy
The multi-year ML technical North Star that leadership commits to — the 3-to-5-year direction across product areas — and the ML bet portfolio behind it (Gen-AI direction, RecSys / personalization direction, agentic-AI direction, foundation-model program direction, MLOps discipline as org contract). Sequencing, non-goals, sunset criteria. Distinguished from the staff-scope portfolio roadmap (owned by `staff-ml-engineer-learning` mod-410). Grounded in SoundCloud "define the technical North Star for ML across engineering", Pinterest "unified technical architecture and defining a roadmap for industry leading methodology", and the ai-infra-principal-engineer-learning mod-505 long-term-technical-bets shape.

### mod-503 — North-Star Applied-ML Architecture
The living north-star architecture artifact the whole ML org converges on: living diagrams, canonical APIs (feature, registry, eval, inference-gateway), contracts between the ML org, the platform teams, and the product teams. Evolution plan for how a new bet plugs in without a rewrite. Org-wide architecture-review body (block / nudge / escalate). Grounded in Capital One "north star platform architecture, continuously publishing and refining living diagrams and canonical APIs" and Chip Huyen's *Designing Machine Learning Systems*.

### mod-504 — Cross-Org Influence Without Authority
Influencing stakeholders up to the SVP / CTO / CEO level without direct authority. Distinguishing the principal-scope executive audience from the staff-scope executive audience (which is owned by `staff-ml-engineer-learning` mod-410 exercise-02). Partnership contract with the peer executive branch (Head of AI / CAIO / Head of AI Governance / CISO / CFO). Coalition-sequencing as an engineering discipline. Escalation-and-deferred-decision protocol. Grounded in Capital One "influence cross-functional stakeholders up to the SVP level", Bumble "operate as a senior individual contributor, influencing technical strategy and decision-making without direct authority", and Twilio "lead cross-functional engineering efforts".

### mod-505 — Principal Mentorship & Technical-Bar Calibration
Coach staff engineers (L40) — not senior tech leads. Multiply the effectiveness of every ML team (Upstart) via a small number of leverage moves. Sit on staff-plus hiring loops and calibrate loop-level, not just interview-level. Set the review bar the ML org calibrates against. Elevate engineering culture without sliding into people-management scope. Sustain the principal signal over years — quarterly / yearly personal-cadence artifacts. Grounded in Ibotta "act as a leading contributor, voice, and thought leader in a growing community", Upstart "multiply the effectiveness of every ML team", and Bumble "without direct authority".

### mod-506 — Industry Influence & External Voice
Publications (ICML / NeurIPS / KDD industry track, O'Reilly AI, applied-ML engineering blogs), keynotes, open-source contributions at principal altitude (release-level decisions, not day-to-day commits), and internal-community thought leadership. Return-on-external-influence tracking with retirement criteria. Grounded in Capital One "ML industry impact through conference presentations, papers, blog posts, or open source contributions" (explicit preferred qualification) and Ibotta "thought leader in a growing community of machine learning practitioners". Held at 10 hours — the smallest module in the plan — reflecting the modest in-window evidence (4/26 postings, freq 0.15, below the 0.30 material threshold); scoped up or trimmed on the 2026-10-08 re-sample per the `authoring_note` in `.aicg/curriculum-plan.json`.

## Project summaries

### project-501 — Org-Scope ML North Star & Reference Architecture
Author the multi-year North Star and the living north-star reference architecture for a 3–5-product-area ML org. Integrates mod-501, 502, 503, 504. Defended against a simulated SVP / CTO panel review.

### project-502 — Cross-Org Influence & Technical-Bar Simulation
Simulate driving an org-scope ML bet from the principal seat via coalition-building rather than direct authority. Integrates mod-504 and mod-505 with the mod-501 role-scope framing.

### project-503 — Industry Influence & External Voice Artifact Portfolio
Ship a portfolio of industry-influence artifacts extracting principal-scope lessons from staff+ production ML systems. Integrates mod-506. Smaller capstone reflecting the below-threshold in-window evidence for the underlying requirement.

## Assessment

Each module ships **1 quiz** plus the exercises and (where present) a lab listed in [`.aicg/curriculum-plan.json`](.aicg/curriculum-plan.json). Each project ships a portfolio-grade README and an explicit assessment rubric covering the principal signals — North Star defensibility, living-architecture artifact quality, canonical-API contract clarity, SVP/CTO-audience narrative craft, coalition-sequencing artifact quality, staff-plus hiring-loop calibration output, and (for project-503) the return-on-influence tracking.

## Where to go after this curriculum

The IC-principal ladder does not extend upward as a canonical ladder in the sampled market — a level-48 principal has, in practice, four progressions:

- **Stay principal, deepen** — the same track over years, with the north-star architecture and the North Star roadmap evolving through multiple bets. This is the modal outcome per Larson's *Staff Engineer* and the StaffEng.com Distinguished / Fellow interviews.
- **Peer executive branch** — [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning) or [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) if the learner takes on direct reports, headcount, and board reporting.
- **Peer platform-side principal** — [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) or [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) if the learner's centre of gravity migrates to platform.
- **Peer research-principal path** — Principal Research Scientist / Distinguished Applied Scientist at an AI lab (no owner in this ecosystem yet; documented in `JOB_REQUIREMENTS.md`).

<!-- needs-research: re-run 2026-10-08 with the same sampling method. Watch for (a) whether `req-industry-influence` and `req-executive-board-comms` rise above 0.30 material; (b) whether Distinguished titles spread beyond Capital One; (c) whether Principal Research Scientist / Applied Scientist tracks need their own owner role in this ecosystem. Re-scope mod-506 up or trim it to a mod-505 lab based on the outcome. -->
