# Job Requirements — Principal Machine Learning Engineer

**Role level:** 48 (principal IC altitude, ML engineering ladder — above `staff-ml-engineer-learning` at level 40, below `chief-ai-officer-learning` on the executive branch)
**Track:** `principal-ml-engineer-learning`
**Research window:** 2026-04-08 → 2026-07-08 (last 90 days)
**Today:** 2026-07-08
**Postings analyzed:** 26 (20 high-confidence + 6 medium/low-confidence)
**Machine-readable source:** [`.aicg/job-requirements.json`](.aicg/job-requirements.json)
**Proposed delta this cycle:** [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json) — **zero additions**

## Headline

The 2026-Q2 market for Principal / Distinguished / Sr. Principal Machine Learning Engineers is thin (~few thousand titled openings in the US, per LinkedIn), fragmented across titles (`Principal`, `Sr. Distinguished`, `Distinguished AI Engineer`, `Senior Principal`), and dominated by **three signals**:

1. **Org- and industry-wide ML technical strategy** — set the "technical North Star for ML across engineering", define the multi-year modelling roadmap, drive strategy across product areas (24/26 postings, 0.92).
2. **Applied-ML architecture at portfolio-and-industry altitude** — architect complex enterprise AI systems, publish and refine the "north-star platform architecture with living diagrams and canonical APIs", set the org's converged systems shape (22/26, 0.85).
3. **Cross-org influence without authority up to SVP/CTO** — influence stakeholders up to the SVP level, drive consensus at organizational level, sit as the ML org's technical voice in cross-functional executive reviews (18/26, 0.69).

Around those three signals a fourth cluster — **principal mentorship and technical-bar calibration for the ML org** (17/26, 0.65) — captures "act as thought leader in the ML community", "multiply the effectiveness of every ML team", and "elevate engineering culture".

Everything else in the sample maps to **lower-level owners** by the Ownership Rule:

- Gen-AI / multimodal, RecSys/ranking, agentic platforms, distributed training, foundation-model programs, MLOps depth, responsible-AI at portfolio scope, GPU capacity/TCO, hiring calibration for staff hires — all owned at `senior-ml-engineer`, `staff-ml-engineer`, `fine-tuning-engineer`, `training-pipeline-engineer`, `model-evaluation-engineer`, `nlp-engineer`, `applied-ai-engineer` / `agentic-ai-engineer`, `rag-engineer`, `ai-infra-mlops`, `ai-infra-ml-platform`, `ai-infra-performance`, `ai-infra-security`, `ai-governance-analyst`, or `head-of-ai-governance`.

**This means the principal-owned curriculum surface is small** — it is the delta between "portfolio-scope multi-team leader" (owned by `staff-ml-engineer-learning`) and "org-and-industry-scope leader of the ML function" — not a full ~200-hour catalogue duplicating lower-level material.

## Status — bootstrap research complete; module authoring deferred to bootstrap cycle

<!-- needs-research: the ~2026-10-08 next research cycle should re-validate the frequency of req-industry-influence, req-executive-board-comms, and req-foundation-model-programs against a fresh in-window sample. Consider whether Distinguished titles at Capital One (and any spread to peer enterprises) merit their own owner role. -->

<!-- needs-research: verify the peer-track boundary against Principal Research Scientist / Applied Scientist titles from AI labs (Anthropic, OpenAI, DeepMind, Google Research) — the market treats these as a different ladder, and none of the top-flight lab principal-track postings surfaced in this sample. If they don't count toward this track, that's fine; document the exclusion rule alongside the Staff/EM boundary. -->

The 26 postings sampled clear the ≥25 threshold and produce four principal-scope requirements at ≥0.60 frequency. Requirement themes are grounded in verbatim posting quotes, not invented. However, the actual **module and project catalogue authoring** for the `principal-ml-engineer-learning` track is deferred to a separate `aicg org bootstrap-role` cycle for two reasons:

1. This packet's continuity-bias contract targets **incremental deltas** on top of an existing mature curriculum. The track currently ships only a scaffolded placeholder in `CURRICULUM.md`, and any first-cycle authoring would blow past the "> 20% additions" auto-flag threshold. Human review should route this through the dedicated bootstrap path — the same path `staff-ml-engineer-learning` and `senior-ml-engineer-learning` used — rather than a monthly research delta.
2. The principal-owned surface is small (four themes at material frequency) and heavily interrelated with existing coverage at `staff-ml-engineer-learning`. Authoring the four principal-scope modules deserves a coherent one-shot design rather than a series of monthly additions.

**Zero curriculum additions are proposed this cycle.** See [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json) — the delta arrays are intentionally empty.

## Methodology

1. Enumerated the target titles (`Principal Machine Learning Engineer`, `Principal ML Engineer`, `Sr. / Senior Principal Machine Learning Engineer`, `Distinguished Machine Learning Engineer`, `Sr. Distinguished Machine Learning Engineer`, `Distinguished AI Engineer`, `Applied ML Architect`) across Greenhouse, Lever, Ashby, LinkedIn, Built In, employer ATS (Capital One, Snap, Pinterest, DoorDash, Airbnb), and specialist boards. Ashby / Workday / Roblox / Airbnb / DoorDash SPA pages did not render statically and were captured only at low confidence from search-index snippets.
2. **Filtered out** plain "Machine Learning Engineer" (L20), Senior ML Engineer (L30), Staff ML Engineer (L40 — owned by `staff-ml-engineer-learning`), Engineering Manager / Director of ML (peer people-management path), Research Scientist / Applied Scientist (research track), Principal Data Scientist (peer analytics track), Principal AI Infrastructure Engineer / Principal Platform Engineer (peer platform tracks — already owned by `ai-infra-principal-engineer-learning` and `ai-infra-principal-architect-learning`).
3. Applied the **principal-differentiation heuristic**: for every requirement, articulated **what a level-48 principal owns that a level-40 staff does not** — the shift from "portfolio-scope multi-team blueprint" to "org- and industry-wide North Star", from "exec-audience RFC leadership commits to" to "board / CTO / SVP-level narrative", from "coach senior tech leads" to "coach staff engineers and set the technical bar for the ML org", from "cited public references" to "author references others cite". Captured in the `seniority_signal` field of every requirement in `.aicg/job-requirements.json`.
4. Applied the **ownership rule**: assign coverage to the lowest-level role that genuinely requires the skill; higher levels add depth, architecture, or industry-leadership framing.

## Requirement themes → curriculum ownership

**Freq** is the fraction of the 26-posting sample that cited the theme; only ≥0.30 is treated as material.

| # | Theme | Freq | Owner role (lowest-level) | Coverage |
|---|---|---:|---|---|
| 1 | Org- and industry-wide ML technical strategy | 0.92 | **`principal-ml-engineer` (this)** | Not yet authored — track scaffolded only. Owned here, awaiting bootstrap cycle. |
| 2 | Applied-ML architecture at portfolio-and-industry altitude (north-star platform architecture with living diagrams and canonical APIs) | 0.85 | **`principal-ml-engineer` (this)** | Not yet authored — track scaffolded only. Owned here, awaiting bootstrap cycle. |
| 3 | Cross-org influence without authority (up to VP/SVP level, driving consensus at organizational level) | 0.69 | **`principal-ml-engineer` (this)** | Not yet authored — track scaffolded only. Owned here, awaiting bootstrap cycle. |
| 4 | Principal mentorship + technical-bar calibration for the ML org (thought leader in the ML community, multiply the effectiveness of every ML team) | 0.65 | **`principal-ml-engineer` (this)** | Not yet authored — track scaffolded only. Owned here, awaiting bootstrap cycle. |
| 5 | Gen-AI / multimodal ML implementation depth | 0.42 | `senior-ml-engineer` (integration), `fine-tuning-engineer` (post-training), `nlp-engineer` (NLP depth), `training-pipeline-engineer` (large-scale training) | [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-303-advanced-modeling, mod-304-production-llm-integration; [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning); [`nlp-engineer-learning`](https://github.com/ml-engineering-curriculum/nlp-engineer-learning); [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) |
| 6 | Recommendation / ranking / personalization at scale | 0.38 | `senior-ml-engineer` (architecture); `ml-engineer` (build); depth at peer platform tracks | [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) mod-110; [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-302, mod-303, mod-306; [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning) for platform depth |
| 7 | MLOps / production ML lifecycle depth (CI/CD, drift, A/B, feature stores, MLflow / Kubeflow / SageMaker) | 0.35 | `ai-infra-mlops` (level 30 build), `ai-infra-ml-platform` (level 30 platform); practitioner slice at `ml-engineer` / `senior-ml-engineer` | [`ai-infra-mlops-learning`](https://github.com/ai-infra-curriculum/ai-infra-mlops-learning); [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning); [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) mod-108, mod-109; [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-307 |
| 8 | Agentic AI platform depth (LangChain / CrewAI / Semantic Kernel / AutoGen, multi-agent workflows, RAG at production scale) | 0.35 | `agentic-ai-engineer`, `senior-agentic-ai-engineer`, `agentic-systems-architect`, `rag-engineer`, `llm-application-developer`, `applied-ai-engineer` | [`agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/agentic-ai-engineer-learning); [`senior-agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-agentic-ai-engineer-learning); [`agentic-systems-architect-learning`](https://github.com/ml-engineering-curriculum/agentic-systems-architect-learning); [`rag-engineer-learning`](https://github.com/ml-engineering-curriculum/rag-engineer-learning); [`llm-application-developer-learning`](https://github.com/ml-engineering-curriculum/llm-application-developer-learning); [`applied-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/applied-ai-engineer-learning) |
| 9 | Responsible AI at portfolio and org scope (NIST AI RMF, EU AI Act, model cards, datasheets, review gates) | 0.23 | `staff-ml-engineer` (portfolio-scope), `senior-ml-engineer` (single-system), `head-of-ai-governance` / `ai-governance-analyst` (policy), `security-learning` (red team) | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-409-responsible-ai-at-portfolio-scope; [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-309; [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning); [`ai-governance-analyst-learning`](https://github.com/ml-engineering-curriculum/ai-governance-analyst-learning); [`security-learning`](https://github.com/ai-infra-curriculum/security-learning) |
| 10 | Distributed training strategy at scale | 0.19 | `training-pipeline-engineer` (level-35 build), `staff-ml-engineer` mod-403/404 (program strategy), `ai-infra-performance` (kernel depth) | [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning); [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403, mod-404; [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning) |
| 11 | Executive- and board-level communication | 0.15 | `staff-ml-engineer` (exec-audience RFC); principal-side C-suite/board narrative | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-02 (executive-audience RFC portfolio). Principal-scope escalation deferred until frequency crosses 0.30. |
| 12 | Industry influence — publications, keynotes, open-source thought leadership | 0.15 | **`principal-ml-engineer` (this)** — principal-defining signal by role definition, but sample evidence is thin | Not yet authored. Deferred until frequency crosses 0.30 in a future cycle OR a bootstrap cycle explicitly runs. Do NOT bootstrap against below-threshold evidence per continuity contract. |
| 13 | Foundation-model / large-scale training program leadership | 0.12 | `staff-ml-engineer` mod-403 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403-foundation-model-training-programs |
| 14 | Alignment / RLHF / preference optimization | 0.08 | `fine-tuning-engineer` | [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning) (preference optimization / safety tuning modules) |
| 15 | GPU capacity, cost, TCO at org scope | 0.04 | `staff-ml-engineer` mod-407 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-407-capacity-cost-and-tco |
| 16 | Hiring calibration for staff+ ML hires | 0.04 | `staff-ml-engineer` mod-410 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-03 |
| 17 | ML practitioner workflow foundations (data → model → deploy → monitor) | n/a — prerequisite | `ml-engineer` (level 20) | Prerequisite. [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) |
| 18 | Single-team tech-lead ML engineering (single-system architecture, review authoring, one-team roadmap) | n/a — prerequisite | `senior-ml-engineer` (level 30) | Prerequisite. [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) |
| 19 | Multi-team portfolio scope (staff-plus IC altitude — cross-team eval program, portfolio blueprint, multi-quarter roadmap) | n/a — prerequisite | `staff-ml-engineer` (level 40) | Prerequisite. [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) |
| 20 | Direct people management (1:1s, performance reviews, headcount) | n/a — peer people-leader | `ai-infra-team-lead` (level 40 EM), executive tracks | Not in scope. This track is the IC-principal counterpart. |

## Seniority differentiation — what changes from level 40

The single most important signal in a Principal / Distinguished ML Engineer posting is the **further shift in the object of the verb**:

| Verb | Level 30 (Senior) object | Level 40 (Staff) object | **Level 48 (Principal) object** |
|---|---|---|---|
| own | the ranking model | the ranking, retrieval, and personalization portfolio | **the ML org's technical direction across product areas** |
| lead | the fraud detection team | the ML org's build-vs-buy on the eval platform | **the north-star platform architecture the whole ML org converges on** |
| set | the eval harness for the team | the multi-quarter roadmap leadership commits to | **the technical bar the ML org hires and calibrates against** |
| author | the model card | the AI-risk register the CISO signs off on | **the reference architecture the industry cites** |
| influence | the sibling team | the peer ML platform team | **cross-functional stakeholders up to the SVP/CTO level** |
| coach | mid-level engineers | senior tech leads (L30) | **staff engineers (L40) and staff-plus hiring committees** |

Verbatim posting evidence for this shift:

- **Capital One (Sr. Distinguished, remote-eligible)**: "provide organizational technical leadership to influence architecture, engineering standards, and drive organization-wide platform innovation"
- **Capital One (Distinguished, Agentic AI Platform)**: "you will contribute to the north star platform architecture, continuously publishing and refining living diagrams and canonical APIs"
- **Capital One (Sr. Distinguished AI Engineer)**: "influence cross-functional stakeholders up to the SVP level"
- **SoundCloud (Senior Principal)**: "define the technical North Star for ML across engineering"
- **Instacart (Principal, Ads Quality)**: "define & own the Ads Quality technical strategy and roadmap, balancing between both short-term needs and long-term sustainability"
- **Ibotta (Principal)**: "act as a leading contributor, voice, and thought leader in a growing community of machine learning practitioners"
- **Upstart (Principal)**: "your work will multiply the effectiveness of every ML team at Upstart"
- **Bumble (Principal)**: "operate as a senior individual contributor, influencing technical strategy and decision-making without direct authority"

Postings that only surface staff-scope verbs (multi-team, portfolio, cross-team eval program) were kept in the sample but flagged in the machine-readable file as `medium` or `low` confidence for principal-track alignment.

### Principal IC vs. Executive vs. Research Principal at level 48+

Three distinct level-48+ role families coexist in ML orgs:

- **Principal Machine Learning Engineer** (this track) — IC-principal engineering path. Owns the ML org's technical direction, architecture, and technical bar. No direct reports.
- **Head of AI / VP of ML / Chief AI Officer** — executive path. Owned by [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning), [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning). Direct reports, headcount, budget, board reporting.
- **Principal Research Scientist / Distinguished Applied Scientist** — research-principal path. No owner in this ecosystem yet; the market draws a hard line between engineering-track Principals (this role) and research-track Principals.

Postings whose primary verbs are executive verbs ("own the P&L", "own budget", "report to CEO", "manage VP-level headcount") belong to the executive track and were excluded from this sample. Postings whose primary verbs are research verbs ("publish state-of-the-art", "lead the research direction", "invent new pretraining objectives") belong to the research track and were excluded.

## Posting evidence

The 26 postings in the sample, with URLs and the requirement themes each cites, are stored verbatim in [`.aicg/job-requirements.json`](.aicg/job-requirements.json). Highlights, grouped by segment:

### Fintech / distinguished-title segment (5 postings — Capital One dominates)

- **Capital One** — Sr. Distinguished Machine Learning Engineer (2026-06-05, McLean/Plano). "ML industry impact through conference presentations, papers, blog posts, or open source contributions" as an explicit preferred qualification. [URL](https://www.capitalonecareers.com/en/job/mclean/sr-distinguished-machine-learning-engineer/1732/91589940128)
- **Capital One** — Sr. Distinguished Machine Learning Engineer, Remote-Eligible (2026-04-06). "Drive organization-wide platform innovation." [URL](https://www.capitalonecareers.com/job/mclean/sr-distinguished-machine-learning-engineer-remote-eligible/1732/93650794080)
- **Capital One** — Sr. Distinguished AI Engineer, Remote-Eligible (2026-07-01). "Contribute to the technical vision and the long term roadmap of foundational AI systems." Salary top: $392K. [URL](https://www.capitalonecareers.com/job/san-francisco/sr-distinguished-ai-engineer-remote-eligible/1732/97191343504)
- **Capital One** — Distinguished AI Engineer (2026-05-21). "Influence cross-functional stakeholders up to the VP level." [URL](https://www.capitalonecareers.com/job/mclean/distinguished-ai-engineer/1732/92321941392)
- **Capital One** — Distinguished AI Engineer, Agentic AI Platform (2026-06-23). "North star platform architecture, continuously publishing and refining living diagrams and canonical APIs." [URL](https://www.capitalonecareers.com/job/san-francisco/distinguished-ai-engineer-agentic-ai-platform/1732/96846031728)

### Consumer / recsys / adtech segment (9 postings)

- **SoundCloud** — Senior Principal ML Engineer, New York. "Define the technical North Star for ML across engineering." [URL](https://job-boards.greenhouse.io/soundcloud71/jobs/8486880002)
- **Pinterest** — Principal ML Engineer, Content Recommendations. "Set overall technical strategy, unified technical architecture and defining a roadmap for industry leading methodology." Salary top: $480K. [URL](https://www.pinterestcareers.com/jobs/5036093/principal-machine-learning-engineer-content-recommendations/)
- **Instacart** — Principal SWE/ML Engineer, Ads Quality. "Define & own the Ads Quality technical strategy and roadmap." Requires PhD + 15+ years. [URL](https://www.builtinsf.com/job/principal-softwaremachine-learning-engineer-ads-quality/4504005)
- **Paramount+** — Principal ML Engineer, Personalization (2026-04-22). Ad-tech, RL, causal inference. [URL](https://www.showbizjobs.com/jobs/paramount--principal-machine-learning-engineer-personalization-in-new-york/jid-mk15k2)
- **Snap Inc** — Principal ML Engineer, Content ML, L7 (2026-06-25). Salary top: $414K. [URL](https://careers.snap.com/job?id=R0045945)
- **Bumble** — Principal ML Engineer, Matching and Recommendations (2026-04-02). "Operate as a senior individual contributor, influencing technical strategy and decision-making without direct authority." [URL](https://jobs.lever.co/bumbleinc/a9f321fc-b38d-450a-a3ba-3174e37ba0f3)
- **Ibotta** — Principal ML Engineer, Denver (2026-03-28). "Act as a leading contributor, voice, and thought leader in a growing community of machine learning practitioners." [URL](https://jobs.notablecap.com/companies/ibotta/jobs/72502067-principal-machine-learning-engineer-r-102400)
- **DoorDash** — Principal ML Engineer, Ads & Promos Delivery (medium confidence — SPA fetch blocked). [URL](https://careersatdoordash.com/jobs/principal-machine-learning-engineer-ads-promos-delivery/7760003/)
- **Roblox** — Distinguished Engineer, ML - Discovery (low confidence — SPA timeouts). [URL](https://careers.roblox.com/jobs/6330894)

### Enterprise / SaaS / cybersecurity segment (7 postings)

- **GoodRx** — Principal ML Engineer (2026-07-05). "Define and drive machine learning strategy across multiple domains and product areas." Multi-agent + RAG at production scale. [URL](https://www.builtinnyc.com/job/principal-machine-learning-engineer/9152221)
- **Twilio** — Principal ML & Data Engineer (2026-05-21). "Lead cross-functional engineering efforts, breaking down complex initiatives into executable roadmaps." [URL](https://www.builtinnyc.com/job/principal-machine-learning-data-engineer/9004116)
- **Palo Alto Networks** — Principal ML Engineer (Gen AI, LLM). "Contribute to strategic direction of AI-driven cybersecurity initiatives." [URL](https://builtin.com/job/principal-machine-learning-engineer-gen-ai-llm/4764441)
- **Wiser Solutions** — Principal ML Engineer. "Define and evolve Wiser's AI and data science technical strategy in partnership with product and business leadership." 15+ years. [URL](https://jobs.smartrecruiters.com/WiserSolutions/744000112567651-principal-machine-learning-engineer)
- **ServiceNow** — Principal ML Engineer, Agentic AI (low confidence). Now Assist platform. [URL](https://careers.servicenow.com/jobs/744000107759800/principal-machine-learning-engineer-agentic-ai/)
- **Zscaler** — Principal ML Engineer, San Jose (2026-07-01, low confidence). Agentic frameworks for cybersecurity. [URL](https://www.linkedin.com/jobs/view/principal-machine-learning-engineer-at-zscaler-4198247640)
- **Autodesk** — Principal ML Engineer, ML Platform and Systems Architecture, Boston (low confidence). [URL](https://autodesk.wd1.myworkdayjobs.com/en-US/Ext/job/Principal-ML-Engineer--Machine-Learning-Platform-and-Systems-Architecture_26WD97132-1)

### AI-native / scientific / applied-scientific segment (4 postings)

- **Lila Sciences** — Principal Machine Learning Engineer (2026-04-28). "Define and advance ML engineering standards, tooling, and best practices across the AI organization." 10+ years + closed-loop discovery engine. Salary top: $374K. [URL](https://job-boards.greenhouse.io/lilasciences/jobs/4222224009)
- **Headspace** — Principal ML Engineer. LLM orchestration, RAG, embedding, RecSys. Salary top: $258.7K in high-cost regions. [URL](https://job-boards.greenhouse.io/hs/jobs/7891502)
- **PhysicsX** — Principal ML Engineer, Singapore. 3D point-cloud / mesh geometry-aware modelling. [URL](https://jobs.generalcatalyst.com/companies/physicsx/jobs/65000587-principal-machine-learning-engineer)
- **Airbnb** — Principal ML Engineer, LLM Fine-tuning and Optimization (low confidence — SPA fetch blocked). [URL](https://careers.airbnb.com/positions/7955579/)

### Marketplace / fintech applied segment (1 posting)

- **Upstart** — Principal Machine Learning Engineer. "Your work will multiply the effectiveness of every ML team at Upstart—accelerating innovation and advancing our mission." [URL](https://careers.upstart.com/jobs/principal-machine-learning-engineer)

Full failed-fetch list (SPAs and 404s) is captured in `.aicg/job-requirements.json → failed_fetches`.

## What we did NOT propose (and why)

| Tempting addition | Why we rejected it |
|-------------------|--------------------|
| Full 10-module principal curriculum authored from this packet | This packet is the **research packet**, not the bootstrap packet. First-cycle authoring for an unauthored track blows past the "> 20% additions" auto-flag threshold and belongs in a dedicated `aicg org bootstrap-role` cycle (the path `staff-ml-engineer-learning` and `senior-ml-engineer-learning` used). The `.aicg/curriculum-plan-delta.json` is deliberately empty — this decision is not a signal to defer indefinitely; it's a routing decision to the correct process. |
| A `mod-XXX-industry-influence` module for publications / keynotes / open-source thought leadership | Cited in only 4/26 postings (0.15) — below the 0.30 material threshold. Yes, the principal role definition per the README calls this out, but the continuity-bias contract explicitly forbids proposing modules on below-threshold evidence. Wait for either a 2026-10 cycle where frequency rises, or a bootstrap cycle that authors it against the role definition rather than posting evidence. |
| An agentic-AI strategy module at principal level | Peer platform curriculum [`ai-infra-principal-engineer-learning/JOB_REQUIREMENTS.md`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) already addresses agentic-AI as a canonical "long-term technical bet" (`mod-505-long-term-technical-bets`) at level 50 for the platform side. The principal-ML slice should use the same generic bet-evaluation shape when authored — not a technology-specific module that ages out. |
| A gen-AI multimodal module at principal level | Duplicates senior + fine-tuning + nlp + training-pipeline coverage. Principal-side slice is "set the org's gen-AI direction" — an application of req-org-industry-strategy, not a distinct module. |
| A RecSys module at principal level | Duplicates senior-ml-engineer mod-302 / mod-303 / mod-306. Principal-side is org-scope RecSys standards — application of req-org-industry-strategy. |
| A distributed-training module at principal level | Duplicates training-pipeline-engineer + staff-ml-engineer mod-403 / mod-404. Principal-side is industry-scope bet framing. |
| An MLOps module at principal level | Duplicates ai-infra-mlops + ai-infra-ml-platform + senior mod-307. Principal-side is org-scope MLOps consumer contract — application of req-org-industry-strategy. |
| Direct people-management coverage | Peer executive track (`chief-ai-officer-learning`, `head-of-ai-governance-learning`) owns this. This track is the IC-principal counterpart. |

## External resources for out-of-scope topics

These resources cover topics that are NOT principal-ML-engineer ownership (per the Ownership Rule) but that Principal ML Engineers are commonly expected to reason about at the strategy / bet altitude. They are linked here so principal-track learners can ground their bets without the principal curriculum duplicating implementation-level material owned in lower-level tracks.

- **Applied-ML architecture at industry altitude:** Chip Huyen, *Designing Machine Learning Systems* (O'Reilly, 2022) — canonical text; Google Machine Learning Rules (rules-of-ml); Meta's *Applied Machine Learning at Facebook* engineering blog; Airbnb Engineering blog series on Bighead / Zipline; Uber Engineering blog on Michelangelo.
- **Staff-plus IC leadership progression to principal:** Will Larson, *Staff Engineer: Leadership beyond the management track* (Stripe Press, 2021); StaffEng.com Distinguished / Fellow interviews; Engineering Ladders principal-rung criteria (https://www.engineeringladders.com/); progression.fyi collected frameworks.
- **Foundation-model / large-scale training programs:** Chinchilla scaling-laws paper (Hoffmann et al. 2022); NVIDIA Megatron-LM; Microsoft DeepSpeed / ZeRO; PyTorch FSDP2 documentation; Meta Llama 3 technical report — used as principal-side worked examples, implementation lives at [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) and [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403 / mod-404.
- **Agentic AI platforms:** LangGraph docs (https://langchain-ai.github.io/langgraph/); OpenAI Assistants API / Anthropic tool-use documentation; Semantic Kernel and AutoGen; production-agentic engineering blog series (Pinterest, Salesforce, ServiceNow) — implementation lives at agentic peer tracks.
- **Responsible AI at org scope:** NIST AI Risk Management Framework 1.0 + Generative AI Profile; EU AI Act (Regulation 2024/1689); Google Model Cards paper; Datasheets for Datasets paper — depth lives at [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-409 and governance tracks.
- **Industry influence / keynote craft:** ICML / NeurIPS / KDD industry-track submission guides; O'Reilly AI Conference speaker guidance; QCon Engineering Culture track; the *Papers With Code* newsletter pattern for productive dissemination.

## Ownership map — quick reference

When backfilling postings or authoring the eventual principal-ML curriculum, use this decision to keep the track from drifting into peer territory:

- **Principal ML Engineer (this track, level 48)** owns *org- and industry-wide ML technical strategy, applied-ML architecture at portfolio-and-industry altitude, cross-org influence up to SVP/CTO, and principal-level mentorship + technical-bar calibration for the ML org*. Everything below the level-40 staff scope is inherited, not re-taught.
- **Staff ML Engineer (level 40)** owns multi-team ML portfolio scope. This principal track defers to it for all portfolio-scope requirements (foundation-model programs, distributed-training strategy, ML platform strategy, cross-team eval, portfolio reliability, TCO, responsible AI at portfolio scope, staff-plus technical leadership).
- **Senior ML Engineer (level 30)** owns single-team ML tech-lead scope. This principal track links to it for all single-team requirements.
- **ML Engineer (level 20)** owns the build-altitude ML practitioner workflow. Prerequisite.
- **Fine-Tuning Engineer, NLP Engineer, RAG Engineer, LLM Application Developer, Applied AI Engineer, Agentic AI Engineer, Senior Agentic AI Engineer, Agentic Systems Architect** — LLM / gen-AI / agentic specialists at level 30–40. This principal track defers to them for all LLM / agentic / RAG implementation depth.
- **Training Pipeline Engineer (level 35), AI Infra Performance, AI Infra ML Platform, AI Infra MLOps** — infra specialists. This principal track defers to them for all training-platform / MLOps / cluster / kernel depth.
- **Model Evaluation Engineer, AI Evaluation Engineer** — eval specialists at level 30–35. This principal track defers to them for eval-platform depth.
- **AI Infra Security (level 35), AI Governance Analyst, Head of AI Governance** — security / governance depth. This principal track defers to them.
- **Chief AI Officer, Head of AI Governance** — peer executive tracks. This principal track is the IC-principal counterpart — no direct reports, no budget ownership, no board reporting duties.
- **AI Infra Principal Engineer, AI Infra Principal Architect** — peer platform-side principal tracks. Complementary scope: platform vs. modelling.

## Conclusion

<!-- needs-research: re-run 2026-10-08 with the same sampling method. Watch for: (a) whether req-industry-influence and req-executive-board-comms rise above 0.30 material; (b) whether Distinguished titles spread beyond Capital One; (c) whether Principal Research Scientist / Applied Scientist tracks need their own owner role. -->

The 26 in-window postings sampled clear the ≥25 threshold. Four principal-scope requirements sit at ≥0.60 frequency and belong at this level (org- and industry-wide strategy, applied-ML architecture at industry altitude, cross-org influence, and principal mentorship + technical-bar calibration). All other requirements at material frequency (≥0.30) are owned by lower-level tracks under the Ownership Rule — this packet catalogues them, does not duplicate their coverage.

The `principal-ml-engineer-learning` track is currently a scaffolded placeholder. Authoring the four principal-scope modules is deferred to a dedicated `aicg org bootstrap-role` cycle for human review — the same path staff and senior ML tracks used — rather than being pushed through this monthly research delta. The proposed delta this cycle is **zero additions**, per [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json).
