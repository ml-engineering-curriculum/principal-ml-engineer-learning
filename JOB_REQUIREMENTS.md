# Job Requirements — Principal Machine Learning Engineer

**Role level:** 48 (principal IC altitude, ML engineering ladder — above `staff-ml-engineer-learning` at level 40, below `chief-ai-officer-learning` on the executive branch)
**Track:** `principal-ml-engineer-learning`
**Research window:** 2026-06-08 → 2026-09-08 (last 90 days)
**Today:** 2026-09-08
**Postings analyzed:** 26 (22 high-confidence + 4 medium-confidence)
**Machine-readable source:** [`.aicg/job-requirements.json`](.aicg/job-requirements.json)
**Proposed delta this cycle:** [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json) — **zero additions**

## Headline

Second research cycle for this track. The first cycle (2026-04-08 → 2026-07-08) produced the module + project plan; the mature curriculum was authored between cycles (commit `aac9283`). This cycle re-samples the same title population (`Principal`, `Sr. / Senior Principal`, `Distinguished`, `Sr. Distinguished` Machine Learning / AI Engineer; `Applied ML Architect`) and re-validates the requirement themes against a fresh 26-posting in-window sample.

**The four principal-owned requirement themes remain stable and are all covered by the authored curriculum:**

1. **Applied-ML architecture at portfolio-and-industry altitude** — 22/26 postings, 0.85 (identical to prior cycle). Covered by [`mod-503-north-star-applied-ml-architecture`](lessons/mod-503-north-star-applied-ml-architecture/) and [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/).
2. **Cross-org influence without authority** — 14/26 postings, 0.54 (down 0.15 vs. prior cycle, still comfortably material). Covered by [`mod-504-cross-org-influence-without-authority`](lessons/mod-504-cross-org-influence-without-authority/) and [`project-502`](projects/project-502-cross-org-influence-and-technical-bar-simulation/).
3. **Principal mentorship + technical-bar calibration for the ML org** — 9/26 postings, 0.35 (down 0.30 vs. prior cycle but still at threshold). Covered by [`mod-505-principal-mentorship-and-technical-bar`](lessons/mod-505-principal-mentorship-and-technical-bar/) and [`project-502`](projects/project-502-cross-org-influence-and-technical-bar-simulation/).
4. **Industry influence via publications, keynotes, open source** — 8/26 postings, 0.31 (**CROSSED the 0.30 material threshold this cycle**, up from 0.15). Covered by [`mod-506-industry-influence-and-external-voice`](lessons/mod-506-industry-influence-and-external-voice/) and [`project-503`](projects/project-503-industry-influence-artifact-portfolio/) — authored preemptively against role definition in the prior cycle, now validated by the market.

Also principal-owned per role definition:

5. **Org- and industry-wide ML technical strategy** — 6/26 postings, 0.23 under this cycle's stricter tagging (see [Methodology note on tagging reconciliation](#methodology-note-on-tagging-reconciliation) below). Under the prior cycle's broader tagging convention, this cycle's frequency would be 0.42–0.46. Either way, the theme remains principal-defining and is covered by [`mod-501-principal-ml-role-scope`](lessons/mod-501-principal-ml-role-scope/) and [`mod-502-org-and-industry-ml-strategy`](lessons/mod-502-org-and-industry-ml-strategy/).

**Verdict: zero curriculum additions warranted this cycle.** The mature curriculum absorbs every material-threshold requirement, and the one theme that crossed threshold this cycle (industry influence) was already preemptively covered. See [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json).

## Requirement themes → curriculum ownership

**Freq** is the fraction of the 26-posting sample that cited the theme; only ≥ 0.30 is treated as material.

| # | Theme | Freq | Δ vs. prior | Owner role (lowest-level) | Coverage |
|---|---|---:|---:|---|---|
| 1 | Applied-ML architecture at portfolio-and-industry altitude | 0.85 | 0.00 | **`principal-ml-engineer` (this)** | [`mod-503`](lessons/mod-503-north-star-applied-ml-architecture/), [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/) |
| 2 | MLOps / production ML lifecycle depth | 0.73 | +0.38 | `ai-infra-mlops`, `ai-infra-ml-platform`, `senior-ml-engineer`, `ml-engineer` | [`ai-infra-mlops-learning`](https://github.com/ai-infra-curriculum/ai-infra-mlops-learning), [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning), [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-307, [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) mod-108, mod-109. Principal-side slice = application of theme 5. |
| 3 | Cross-org influence without authority (up to VP/SVP/CTO) | 0.54 | −0.15 | **`principal-ml-engineer` (this)** | [`mod-504`](lessons/mod-504-cross-org-influence-without-authority/), [`project-502`](projects/project-502-cross-org-influence-and-technical-bar-simulation/) |
| 4 | Agentic AI platform strategic leadership (LangChain / CrewAI / AutoGen / MCP / RAG at production scale) | 0.42 | +0.07 | `agentic-ai-engineer`, `senior-agentic-ai-engineer`, `agentic-systems-architect`, `rag-engineer`, `llm-application-developer` | [`agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/agentic-ai-engineer-learning), [`senior-agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-agentic-ai-engineer-learning), [`agentic-systems-architect-learning`](https://github.com/ml-engineering-curriculum/agentic-systems-architect-learning), [`rag-engineer-learning`](https://github.com/ml-engineering-curriculum/rag-engineer-learning), [`llm-application-developer-learning`](https://github.com/ml-engineering-curriculum/llm-application-developer-learning). Principal-side slice = application of theme 5. |
| 5 | Org- and industry-wide ML technical strategy | 0.23<sup>*</sup> | −0.69<sup>*</sup> | **`principal-ml-engineer` (this)** | [`mod-501`](lessons/mod-501-principal-ml-role-scope/), [`mod-502`](lessons/mod-502-org-and-industry-ml-strategy/), [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/) |
| 6 | Principal mentorship + technical-bar calibration for the ML org | 0.35 | −0.30 | **`principal-ml-engineer` (this)** | [`mod-505`](lessons/mod-505-principal-mentorship-and-technical-bar/), [`project-502`](projects/project-502-cross-org-influence-and-technical-bar-simulation/) |
| 7 | Gen-AI / multimodal ML strategic leadership | 0.35 | −0.07 | `senior-ml-engineer`, `fine-tuning-engineer`, `nlp-engineer`, `training-pipeline-engineer` | [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-303, mod-304; [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning); [`nlp-engineer-learning`](https://github.com/ml-engineering-curriculum/nlp-engineer-learning); [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning). Principal-side slice = application of theme 5. |
| 8 | Industry influence — publications, keynotes, open source | **0.31** | **+0.16** | **`principal-ml-engineer` (this)** | [`mod-506`](lessons/mod-506-industry-influence-and-external-voice/), [`project-503`](projects/project-503-industry-influence-artifact-portfolio/). **Crossed 0.30 this cycle; existing preemptive coverage absorbs it.** |
| 9 | Responsible AI at org and industry scope | 0.23 | 0.00 | `staff-ml-engineer` (portfolio), `senior-ml-engineer` (system), `head-of-ai-governance`, `ai-governance-analyst`, `ai-infra-security` | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-409; [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-309; [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning); [`ai-governance-analyst-learning`](https://github.com/ml-engineering-curriculum/ai-governance-analyst-learning); [`security-learning`](https://github.com/ai-infra-curriculum/security-learning) |
| 10 | GPU / ML capacity cost and TCO at org scope | 0.23 | +0.19 | `staff-ml-engineer` mod-407 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-407. **Watch:** 5× jump this cycle; if crosses 0.30 next cycle add an exercise to `mod-502` rather than a new module. |
| 11 | Recommendation / ranking / personalization at scale | 0.15 | −0.23 | `senior-ml-engineer` (architecture), `ml-engineer` (build), `training-pipeline-engineer`, `ai-infra-ml-platform` | [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) mod-110; [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-302, mod-303, mod-306. |
| 12 | Distributed training strategy at scale (FSDP / DeepSpeed / Megatron / tensor parallelism) | 0.12 | −0.07 | `training-pipeline-engineer` (build), `staff-ml-engineer` (program), `ai-infra-performance` (kernel) | [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning); [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403, mod-404; [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning) |
| 13 | Alignment / RLHF / preference-optimization strategy | 0.12 | +0.04 | `fine-tuning-engineer` | [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning) |
| 14 | Executive- and board-level communication | 0.08 | −0.07 | `staff-ml-engineer`; principal-side included in [`mod-504`](lessons/mod-504-cross-org-influence-without-authority/) | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-02 |
| 15 | Foundation-model / large-scale training program leadership | 0.08 | −0.04 | `staff-ml-engineer` mod-403 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403 |
| 16 | Hiring calibration for staff+ ML hires | 0.08 | +0.04 | `staff-ml-engineer` mod-410 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-03; principal-side bar-calibration for staff+ loops is a `mod-505` topic |
| 17 | ML practitioner workflow foundations | n/a | — | `ml-engineer` (level 20) | Prerequisite. [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) |
| 18 | Single-team ML tech-lead scope | n/a | — | `senior-ml-engineer` (level 30) | Prerequisite. [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) |
| 19 | Multi-team ML portfolio scope | n/a | — | `staff-ml-engineer` (level 40) | Prerequisite. [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) |
| 20 | Direct people management | n/a | — | Peer people-leader branch (executive tracks) | Not in scope. This track is the IC-principal counterpart. |

<sup>*</sup> Theme 5 (org-and-industry-wide strategy) shows a nominal 0.69 drop but this is a **tagging convention shift, not a market signal**. Under the prior cycle's broader convention this cycle's frequency would be 0.42–0.46. See [Methodology note on tagging reconciliation](#methodology-note-on-tagging-reconciliation).

## Methodology

1. Enumerated the target titles (`Principal Machine Learning Engineer`, `Principal ML Engineer`, `Sr. / Senior Principal Machine Learning Engineer`, `Distinguished Machine Learning Engineer`, `Sr. Distinguished Machine Learning Engineer`, `Distinguished AI Engineer`, `Distinguished Software Engineer (ML / AI scope)`, `Applied ML Architect`) across Greenhouse, Lever, Ashby, Built In, LinkedIn snippets, employer ATS (Capital One, Coupang, Walmart, Twilio, ServiceNow, Verizon, Cisco, Autodesk), and specialist boards.
2. **Filtered out** plain Machine Learning Engineer (L20), Senior ML Engineer (L30), Staff ML Engineer (L40 — owned by `staff-ml-engineer-learning`), Engineering Manager / Director of ML (peer people-management path), Research Scientist / Applied Scientist (research track), Principal Data Scientist (peer analytics track), Principal AI Infrastructure Engineer / Principal Platform Engineer (peer platform tracks — already owned by `ai-infra-principal-engineer-learning` / `ai-infra-principal-architect-learning`).
3. Applied the **principal-differentiation heuristic**: for every requirement, articulated what a level-48 principal owns that a level-40 staff does not — the shift from "portfolio-scope multi-team blueprint" to "org- and industry-wide North Star", from "exec-audience RFC leadership commits to" to "board / CTO / SVP-level narrative", from "coach senior tech leads" to "coach staff engineers and set the technical bar for the ML org", from "cited public references" to "author references others cite". Captured in the `seniority_signal` field of every requirement in [`.aicg/job-requirements.json`](.aicg/job-requirements.json).
4. Applied the **ownership rule**: assign coverage to the lowest-level role that genuinely requires the skill; higher levels add depth, architecture, or industry-leadership framing.

### Methodology note on tagging reconciliation

The current cycle applied a **stricter tagging convention for `req-org-industry-strategy`** than the prior cycle. The prior cycle tagged 24/26 postings (0.92) on any principal-scope "define / set / drive technical direction" verb; the current cycle only tagged postings with EXPLICIT organizational-scope strategy language ("define technical strategy at organizational level", "act as technical thought leader on Gen AI adoption across the organization", "shape roadmaps and visions", "guide enterprise AI/ML strategies"). Under the strict tagging, the cycle-over-cycle frequency drops 0.92 → 0.23; under a broader tagging convention aligned with the prior cycle, it would be 0.42–0.46.

**The underlying reality has not changed** — Principal ML Engineer postings still center on strategic scope. Interpret the drop as a methodology reconciliation, not a market shift. Both cycles owned this theme at `principal-ml-engineer`; both cycles produced identical curriculum coverage; no curriculum action follows from the tagging shift.

A definitive tagging rule will be published in the ownership documentation before the next cycle to prevent cycle-to-cycle whiplash on this signal.

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

Verbatim posting evidence for this shift, drawn from the 2026-09 sample:

- **Capital One (Sr. Distinguished AI Engineer)**: "Demonstrated ability to lead and mentor an engineering organization and influence cross-functional stakeholders up to the SVP level"
- **Capital One (Sr. Distinguished AI Engineer, Agentic AI Platform)**: "Demonstrated ability to lead and mentor multiple engineering teams and influence cross-functional stakeholders up to the VP level"
- **Coupang (Principal Engineer, ML)**: "Exceptional ability to influence technical direction across multiple teams and organizations without direct authority"
- **DAT Freight & Analytics (Principal ML)**: "Ability to operate at Principal scope, setting technical direction, identifying and retiring platform risk, mentoring engineers, and delivering solutions whose impact scales across teams and the broader organization"
- **Cisco (Distinguished Software Engineer, Security Platform)**: "Serve as a recognized internal and external thought leader, influencing industry direction"
- **Cisco / ThousandEyes (Distinguished Engineer, ML)**: "As a technical leader, you'll excel in making critical technical decisions, shaping roadmaps and visions that drive the success of transformative machine learning projects"
- **ServiceNow (Principal ML)**: "Set the architectural patterns the group works from. Own the hard design calls, run the design reviews, and raise the bar on agentic design"
- **SoundCloud (Senior Principal, ML)**: "This role reports directly to the Chief Technology Officer and will work in lockstep with the Music Intelligence, Content, and Recommendations teams"
- **Cogniify (Principal AI/ML)**: "Proven track record of driving technical strategy and influencing engineering direction at an organizational level"
- **Twilio (Principal ML)**: "spearhead ML/AI focused research projects within Twilio's Emerging Technology & Innovation (ETI) organization"
- **Walmart (Distinguished, AI/ML)**: "Proven record as a senior individual contributor influencing architecture and driving technical excellence across large organizations"

Postings whose primary verbs are executive verbs ("own the P&L", "own budget", "report to CEO", "manage VP-level headcount") belong to the executive track and were excluded from this sample. Postings whose primary verbs are research verbs ("publish state-of-the-art", "lead the research direction", "invent new pretraining objectives") belong to the research track and were excluded.

### Principal IC vs. Executive vs. Research Principal at level 48+

Three distinct level-48+ role families coexist in ML orgs:

- **Principal Machine Learning Engineer** (this track) — IC-principal engineering path. Owns the ML org's technical direction, architecture, and technical bar. No direct reports.
- **Head of AI / VP of ML / Chief AI Officer** — executive path. Owned by [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning), [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning). Direct reports, headcount, budget, board reporting.
- **Principal Research Scientist / Distinguished Applied Scientist** — research-principal path. No owner in this ecosystem yet; the market draws a hard line between engineering-track Principals (this role) and research-track Principals.

## Delta from prior cycle (2026-07 → 2026-09)

The prior cycle window (2026-04-08 → 2026-07-08) and the current cycle window (2026-06-08 → 2026-09-08) overlap by one month. Both samples are size 26. Key observations:

**Employers carried forward with same URL (7 postings):**
Capital One Sr. Distinguished AI Engineer (Remote Eligible), Capital One Sr. Distinguished AI Engineer (Agentic AI Platform), Twilio Principal ML & Data Engineer, Airbnb Principal ML Engineer LLM Fine-tuning, Pinterest Principal ML Engineer Content Recs, Upstart Staff/Principal ML Engineer, SoundCloud Senior Principal (out-of-window but still open, kept at medium confidence), Palo Alto Networks Principal ML Engineer (out-of-window but still open, kept at medium confidence).

**New employers this cycle (11 net-new segments):**
Coupang (ads serving + ML platform), Walmart (2 Distinguished agentic postings), Rula (health-tech personalization), Cisco / ThousandEyes (Distinguished ML), Cisco / Security Platform (Distinguished SWE), Verizon (Distinguished Engineer, Applied AI Solutions), Autodesk (Senior Principal Foundation Model Systems + Principal ML Platform), DAT Freight & Analytics (real-time marketplace ML platform), Block (Staff/Principal ML Engineer, Credit), LexisNexis (Principal ML Engineer I), ConnectWise (Principal ML Engineer, alignment / post-training), Cogniify (Principal AI/ML), ServiceNow (Principal ML), Raft (Principal ML with MCP).

**Requirement cluster shifts:**

- **`req-agentic-platforms-strategy` UP 0.07 (0.35 → 0.42)** — hardened from "preferred" to "required" across multiple postings. MCP appears for the first time as an explicit named skill (Raft, Cogniify, ServiceNow). Still owned by peer agentic tracks per the ownership rule.
- **`req-mlops-production-lifecycle` UP 0.38 (0.35 → 0.73)** — MLOps / LLMOps have become table-stakes across Principal ML Engineer postings. Still owned by `ai-infra-mlops` and lower-level practitioner tracks per the ownership rule.
- **`req-industry-influence` UP 0.16 (0.15 → 0.31) — CROSSED THE 0.30 MATERIAL THRESHOLD.** Validates the preemptive authoring of [`mod-506`](lessons/mod-506-industry-influence-and-external-voice/) against role definition in the prior cycle. Existing coverage absorbs the shift — no new module needed.
- **`req-tco-cost` UP 0.19 (0.04 → 0.23)** — GPU inference / training cost trade-offs being named at posting-level specificity. Still sub-threshold; watch on next cycle.
- **`req-alignment-rlhf` UP 0.04 (0.08 → 0.12)** — DPO / RFT / LoRA / QLoRA being named as posting-level required qualifications. Still sub-threshold; owned by `fine-tuning-engineer`.
- **`req-cross-org-influence` DOWN 0.15 (0.69 → 0.54)** — within normal cycle-to-cycle variance, still comfortably material.
- **`req-principal-mentorship-and-bar` DOWN 0.30 (0.65 → 0.35)** — still at threshold. Some drop reflects more diverse employer mix this cycle (fewer thought-leader-explicit postings, more platform-engineering Principal roles).
- **`req-recsys-ranking-scale` DOWN 0.23 (0.38 → 0.15)** — RecSys-heavy Principal role mix was lighter this quarter; theme still material at lower-owner levels.
- **`req-org-industry-strategy` DOWN 0.69 (0.92 → 0.23) NOMINAL** — methodology reconciliation, not a market shift (see [Methodology note on tagging reconciliation](#methodology-note-on-tagging-reconciliation)).

**Verdict:** No material market shift warrants curriculum change. Every material-threshold theme is already covered by the authored curriculum ([`mod-501`](lessons/mod-501-principal-ml-role-scope/) through [`mod-506`](lessons/mod-506-industry-influence-and-external-voice/), [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/) through [`project-503`](projects/project-503-industry-influence-artifact-portfolio/)). The one theme that crossed threshold this cycle (`req-industry-influence`, 0.15 → 0.31) is already covered by mod-506, authored preemptively against role definition in the prior cycle. **Delta is zero additions.**

## Posting evidence

The 26 postings in the sample, with URLs and the requirement themes each cites, are stored verbatim in [`.aicg/job-requirements.json`](.aicg/job-requirements.json). Highlights, grouped by segment:

### Fintech / distinguished-title segment (5 postings — Capital One dominates)

- **Capital One** — Distinguished Machine Learning Engineer (2026-07-13, Plano/McLean). "ML industry impact through conference presentations, papers, blog posts, or open source contributions" remains an explicit preferred qualification. Salary top: $307K McLean. [URL](https://www.capitalonecareers.com/job/plano/distinguished-machine-learning-engineer/1732/97747878720)
- **Capital One** — Sr. Distinguished AI Engineer, Remote-Eligible (2026-07-01). "Demonstrated ability to lead and mentor an engineering organization and influence cross-functional stakeholders up to the SVP level." Salary top: $392K SF/NYC/San Jose. [URL](https://www.capitalonecareers.com/job/san-francisco/sr-distinguished-ai-engineer-remote-eligible/1732/97191343504)
- **Capital One** — Sr. Distinguished AI Engineer, Agentic AI Platform (2026-06-24). LangChain / CrewAI / Semantic Kernel / AutoGen and LLMOps (Vertex AI, SageMaker, Azure ML) as preferred requirements. [URL](https://www.capitalonecareers.com/job/san-francisco/senior-distinguished-ai-engineer-agentic-ai-platform/1732/96890760608)
- **Block** — Staff/Principal Machine Learning Engineer (Modeling), Credit. "Proficiency with AI-native development workflows. You use LLMs, agentic coding tools, and AI-assisted automation as a regular part of how you build and ship." [URL](https://builtin.com/job/staff-principal-machine-learning-engineer-modeling-credit/8472833)
- **Upstart** — Staff/Principal ML Engineer. "This is a high influence role suited for those who enjoy combining science innovation, with cross functional collaboration and advisory." [URL](https://careers.upstart.com/jobs/principal-machine-learning-engineer)

### Consumer / recsys / adtech / retail segment (7 postings)

- **Coupang** — Principal Engineer, ML (Ads Serving & ML Platform), Seattle (2026-09-08). "Exceptional ability to influence technical direction across multiple teams and organizations without direct authority." Salary top: $386K. [URL](https://boards.greenhouse.io/coupang/jobs/8175850)
- **Walmart** — Distinguished Software Engineer, AI/ML — Agentic Systems, Sunnyvale. Salary top: $338K. [URL](https://careers.walmart.com/us/en/jobs/R-2451270)
- **Walmart** — Distinguished Software Engineer, AI/ML — Agentic Systems & SRE, Sunnyvale. Two Distinguished agentic postings in the same segment — noteworthy for `req-agentic-platforms-strategy` hardening. [URL](https://careers.walmart.com/us/en/jobs/R-2533229)
- **Pinterest** — Principal ML Engineer, Content Recommendations. "Act as the ultimate 'customer representative' for engineers on Trust including representing needs to leadership." Salary top: $480K. [URL](https://builtin.com/job/principal-machine-learning-engineer-content-recommendations/7731228)
- **Rula** — Principal AI Engineer, Personalization and Recommendation, Remote (2026-08-26). Health-tech with HIPAA / GDPR compliance and vector search. "Demonstrated ability to define technical strategy and guide the broader AI/ML infrastructure ecosystem." [URL](https://careers.wing.vc/companies/rula/jobs/91149411-principal-ai-engineer-personalization-and-recommendation-remote)
- **DAT Freight & Analytics** — Principal ML Engineer, Seattle (Hybrid). "Ability to operate at Principal scope, setting technical direction, identifying and retiring platform risk, mentoring engineers, and delivering solutions whose impact scales across teams and the broader organization." Salary top: $320K. [URL](https://builtin.com/job/principal-machine-learning-engineer/7934886)
- **SoundCloud** — Senior Principal Engineer, Machine Learning, Remote NY (2026-04-01, out-of-window but still open; medium confidence). "This role reports directly to the Chief Technology Officer." [URL](https://jobgether.com/offer/69cd2c2e5bd3b40540a4bd53-senior-principal-engineer-machine-learning)

### Enterprise / SaaS / cybersecurity segment (7 postings)

- **Twilio** — Principal Machine Learning Engineer, Remote US. "Spearhead ML/AI focused research projects within Twilio's Emerging Technology & Innovation (ETI) organization." Preferred: "you have previously shared your ideas in public forums through blog posts, meetup presentations, or speaking at conferences." Salary top: $239K. [URL](https://boards.greenhouse.io/twilio/jobs/3535517)
- **Twilio** — Principal ML & Data Engineer, Remote US. MLOps stack named at requirement-level (MLflow, Kubeflow, SageMaker, Vertex AI). Salary top: $271K. [URL](https://builtin.com/job/machine-learning-data-engineer-p5/6844774)
- **ServiceNow** — Principal Machine Learning Engineer. "Hands-on depth designing, shipping, and operating agentic systems in production — multi-agent orchestration, tool calling, planning loops, memory, and failure recovery. Not prototypes." Salary top: $420K. [URL](https://jobs.smartrecruiters.com/ServiceNow/744000145376219-principal-machine-learning-engineer)
- **Verizon** — Distinguished Engineer, Applied AI Solutions, Irving/Alpharetta/Basking Ridge. "Act as a technical thought leader on Gen AI adoption across the organization." Requires security guardrails against prompt injection / data leakage / model abuse. Salary top: $263K. [URL](https://mycareer.verizon.com/jobs/r-1100363/distinguished-engineer-applied-ai-solutions/)
- **LexisNexis** — Principal Machine Learning Engineer I, Raleigh NC. "Provide architectural direction and code-level guidance." Salary top: $253K. [URL](https://builtin.com/job/principal-machine-learning-engineer-i/9690092)
- **ConnectWise** — Principal Machine Learning Engineer, Remote (IND). Names supervised fine-tuning, DPO, RFT, LoRA/QLoRA, BERT/ModernBERT, LLM-as-judge as required — most explicit alignment / post-training toolchain in the sample. [URL](https://job-boards.greenhouse.io/connectwise/jobs/4707883005)
- **Palo Alto Networks** — Principal ML Engineer (Internet Security LLMs, NLP, Deep Learning), Santa Clara (2026-04-02, out-of-window but still open; medium confidence). [URL](https://www.themuse.com/jobs/paloaltonetworks/principal-machine-learning-engineer-internet-security-llms-nlp-deep-learning/)

### Distinguished-title enterprise segment (Cisco, 2 postings)

- **Cisco (ThousandEyes)** — Distinguished Engineer, Machine Learning (Modeling and Tuning), SF Hybrid. "Shaping roadmaps and visions that drive the success of transformative machine learning projects." Salary top: $372K. 15+ years required. [URL](https://www.builtinsf.com/job/distinguished-engineer-aiops-hybrid/2162086)
- **Cisco (Security and Policy Platform)** — Distinguished Software Engineer, Remote US (2026-08-16). "Serve as a recognized internal and external thought leader, influencing industry direction." 15+ years required. Salary top: $407K. [URL](https://remote100k.com/remote-job/cisco-distinguished-software-engineer)

### AI-native / scientific / applied-ML architecture segment (3 postings)

- **Autodesk** — Senior Principal ML Engineer (Foundation Model Systems), Remote US/CA. Names the full frontier training stack (FSDP, DeepSpeed, Megatron-LM, DDP, tensor parallelism, pipeline parallelism) plus RLHF at requirement-level specificity. Salary top: $296K. [URL](https://builtin.com/job/senior-principal-machine-learning-engineer/8958113)
- **Autodesk** — Principal ML Engineer, ML Platform and Systems Architecture, Remote US/CA (2026-05-06, borderline within-window). "This is a senior technical leadership role for an engineer who excels at system architecture." Salary top: $272K. [URL](https://jobs.aihub.masstech.org/companies/autodesk/jobs/77521901-principal-ml-engineer-machine-learning-platform-and-systems-architecture)
- **Airbnb** — Principal ML Engineer, LLM Fine-tuning and Optimization, Remote US. Preferred: "Publications at peer-reviewed AI conferences (e.g., NeurIPS, CVPR, ICML, ICLR, ICCV, and ACL)." Salary top: $365K. [URL](https://careers.airbnb.com/positions/7955579/)

### AI consulting / defense segment (2 postings)

- **Raft** — Principal Machine Learning Engineer, Remote US. Requires "agentic workflows with tool calling, Model Context Protocol (MCP) implementations, and multi-step reasoning systems" + Top Secret clearance. [URL](https://job-boards.greenhouse.io/raft/jobs/5739876004)
- **Cogniify** — Principal AI/ML Engineer, US East/West Coast + US Remote (2026-09-03). "Serve as the senior technical authority on ML system design, providing guidance on architecture, tooling, and engineering standards across the organization." Names MCP / SOC2 / HIPAA / GDPR at preferred level. [URL](https://builtin.com/job/principal-ai-ml-engineer-usa/9752057)

Full failed-fetch list (SPAs and 404s) is captured in [`.aicg/job-requirements.json → failed_fetches`](.aicg/job-requirements.json).

## What we did NOT propose (and why)

| Tempting addition | Why we rejected it |
|-------------------|--------------------|
| A module or scope-up specifically for MCP (Model Context Protocol) named skill | MCP appears in only 3/26 postings (Raft, Cogniify, ServiceNow) — well below the 0.30 material threshold. Implementation belongs to the agentic peer tracks ([`agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/agentic-ai-engineer-learning), [`agentic-systems-architect-learning`](https://github.com/ml-engineering-curriculum/agentic-systems-architect-learning)); principal-side slice is "evaluate MCP as an agentic-platform bet" — an application of the existing `mod-502` bet-portfolio framing. Flag for cross-repo review on next cycle. |
| A module on FSDP / DeepSpeed / Megatron / tensor parallelism at principal altitude | Named in only 2/26 postings (Autodesk Foundation Model Systems, Airbnb). Below threshold and duplicative of [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) + [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403 / mod-404. Principal-side slice remains "org-scope bet framing" — application of `req-org-industry-strategy` covered in `mod-502`. |
| A capacity / cost / TCO module at principal altitude | Jumped 5× this cycle (0.04 → 0.23) but still sub-threshold. If it crosses 0.30 next cycle, add an exercise inside `mod-502` (org-wide capacity-cost bet framing) rather than a new module. |
| A responsible AI at org scope module at principal altitude | Stable at 0.23 — below threshold. Portfolio-scope responsible AI is owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-409; principal-side slice would be industry-standards contribution — not called out at material frequency. |
| A scope-up of `mod-506` (industry influence) now that it crossed threshold | Frequency crossed at 0.31 — just barely above threshold. The module was already scoped correctly at 10 hours + a 20-hour project. Wait for two consecutive cycles at ≥ 0.30 before scoping up; then add an exercise on standards-body contribution or a keynote-slide portfolio, not new modules. |
| A rewrite of `mod-502` (org-industry strategy) because its frequency "dropped" this cycle | The drop is a tagging convention reconciliation, not a market shift. See [Methodology note on tagging reconciliation](#methodology-note-on-tagging-reconciliation). |
| Direct people-management coverage | Peer executive track ([`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning), [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning)) owns this. This track is the IC-principal counterpart. |

## External resources for out-of-scope topics

These resources cover topics that are NOT principal-ML-engineer ownership (per the Ownership Rule) but that Principal ML Engineers are commonly expected to reason about at the strategy / bet altitude. They are linked here so principal-track learners can ground their bets without the principal curriculum duplicating implementation-level material owned in lower-level tracks.

- **Applied-ML architecture at industry altitude:** Chip Huyen, *Designing Machine Learning Systems* (O'Reilly, 2022) — canonical text; Google Machine Learning Rules (rules-of-ml); Meta's *Applied Machine Learning at Facebook* engineering blog; Airbnb Engineering blog series on Bighead / Zipline; Uber Engineering blog on Michelangelo.
- **Staff-plus IC leadership progression to principal:** Will Larson, *Staff Engineer: Leadership beyond the management track* (Stripe Press, 2021); StaffEng.com Distinguished / Fellow interviews; Engineering Ladders principal-rung criteria (https://www.engineeringladders.com/); progression.fyi collected frameworks.
- **Foundation-model / large-scale training programs:** Chinchilla scaling-laws paper (Hoffmann et al. 2022); NVIDIA Megatron-LM; Microsoft DeepSpeed / ZeRO; PyTorch FSDP2 documentation; Meta Llama 3 technical report — used as principal-side worked examples, implementation lives at [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) and [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403 / mod-404.
- **Agentic AI platforms:** LangGraph docs (https://langchain-ai.github.io/langgraph/); OpenAI Assistants API / Anthropic tool-use documentation; Semantic Kernel and AutoGen; Model Context Protocol spec (https://modelcontextprotocol.io) — new in this cycle; production-agentic engineering blog series (Pinterest, Salesforce, ServiceNow) — implementation lives at agentic peer tracks.
- **Responsible AI at org scope:** NIST AI Risk Management Framework 1.0 + Generative AI Profile; EU AI Act (Regulation 2024/1689); Google Model Cards paper; Datasheets for Datasets paper — depth lives at [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-409 and governance tracks.
- **Industry influence / keynote craft:** ICML / NeurIPS / KDD industry-track submission guides; O'Reilly AI Conference speaker guidance; QCon Engineering Culture track; the *Papers With Code* newsletter pattern for productive dissemination.

## Ownership map — quick reference

- **Principal ML Engineer (this track, level 48)** owns org- and industry-wide ML technical strategy, applied-ML architecture at portfolio-and-industry altitude, cross-org influence up to SVP/CTO, principal-level mentorship + technical-bar calibration for the ML org, and the external-voice / industry-influence facet (validated by market crossing to ≥ 0.30 this cycle). Everything below the level-40 staff scope is inherited, not re-taught.
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

<!-- needs-research: re-run 2026-12-08 with the same sampling method. Watch for: (a) whether req-industry-influence sustains >= 0.30 for a second consecutive cycle (if yes, consider a modest scope-up of mod-506 with an exercise on standards-body contribution or a keynote-slide portfolio); (b) whether req-tco-cost crosses 0.30 (if yes, add an exercise inside mod-502 for org-wide capacity-cost bet framing); (c) whether MCP appears in >= 8 postings (if yes, coordinate cross-repo with agentic peer tracks); (d) whether the Foundation Model Systems posting signal (currently 2/26) sustains or expands. Also: publish a definitive tagging rule for req-org-industry-strategy to prevent cycle-to-cycle whiplash. -->

The 26 in-window postings sampled clear the ≥ 25 threshold. Four principal-scope requirements sit at or above the 0.30 material threshold (applied-ML architecture 0.85, cross-org influence 0.54, principal mentorship 0.35, industry influence 0.31 — newly crossed) and belong at this level. Two other principal-owned themes sit just below or at threshold under this cycle's stricter tagging discipline (org-and-industry strategy 0.23 strict / 0.42–0.46 broad; the drop is methodology, not market). All other requirements at material frequency (≥ 0.30) are owned by lower-level tracks under the Ownership Rule — this packet catalogues them and does not duplicate their coverage.

The authored curriculum ([`mod-501`](lessons/mod-501-principal-ml-role-scope/) through [`mod-506`](lessons/mod-506-industry-influence-and-external-voice/), [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/) through [`project-503`](projects/project-503-industry-influence-artifact-portfolio/)) absorbs every material-threshold requirement. The one theme that crossed threshold this cycle (`req-industry-influence`, 0.15 → 0.31) is already covered by `mod-506`, authored preemptively against role definition in the prior cycle. The proposed delta this cycle is **zero additions**, per [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json).
