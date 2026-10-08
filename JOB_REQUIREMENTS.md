# Job Requirements — Principal Machine Learning Engineer

**Role level:** 48 (principal IC altitude, ML engineering ladder — above `staff-ml-engineer-learning` at level 40, below `chief-ai-officer-learning` on the executive branch)
**Track:** `principal-ml-engineer-learning`
**Research window:** 2026-07-08 → 2026-10-08 (last 90 days)
**Today:** 2026-10-08
**Postings analyzed:** 30 (25 high-confidence + 5 medium/low-confidence)
**Machine-readable source:** [`.aicg/job-requirements.json`](.aicg/job-requirements.json)
**Proposed delta this cycle:** [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json) — **zero additions**

## Headline

Third research cycle for this track. The first cycle (2026-04-08 → 2026-07-08) bootstrapped the module + project plan. The second cycle (2026-06-08 → 2026-09-08) re-validated themes against a fresh 26-posting sample and concluded zero additions. This third cycle is a 30-day roll-forward of the same methodology against the 2026-07-08 → 2026-10-08 window.

**Sample construction:** 23 of the prior 26 postings remain live and within the strict new window and are carried forward with `date_observed` updated to 2026-10-08. 3 fall outside the strict window and are retained at medium or low confidence for segment coverage (Autodesk Platform 2026-05-06, SoundCloud 2026-04-01, Palo Alto Networks 2026-04-02 — the Palo Alto original was superseded by a live 2026-09-23 variant surfaced this cycle, so it was promoted back to high). 4 net-new postings were surfaced via spot-check WebSearch and added: Zillow Agentic AI Principal ML (2026-09-03; a Workday-SPA fetch that failed in the prior cycle now renders), Amgen Principal ML Engineer (2026-09-25), Ecolab Principal AI Engineer — ML/MLOps Platform Architect (2026-09-21), and Verizon Distinguished Engineer — AI/ML Engineering (2026-09-14; distinct from the already-sampled Verizon Applied AI Solutions posting). Net sample size: **30 postings** — above the ≥ 25 threshold with room to spare.

**The four principal-owned requirement themes remain stable and are all covered by the authored curriculum:**

1. **Applied-ML architecture at portfolio-and-industry altitude** — 26/30 postings, 0.87 (up 0.02 vs. prior cycle; effectively flat at the ceiling). Covered by [`mod-503-north-star-applied-ml-architecture`](lessons/mod-503-north-star-applied-ml-architecture/) and [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/).
2. **Cross-org influence without authority** — 17/30 postings, 0.57 (up 0.03 vs. prior cycle; stable). Covered by [`mod-504-cross-org-influence-without-authority`](lessons/mod-504-cross-org-influence-without-authority/) and [`project-502`](projects/project-502-cross-org-influence-and-technical-bar-simulation/).
3. **Principal mentorship + technical-bar calibration for the ML org** — 11/30 postings, 0.37 (up 0.02 vs. prior cycle; stable at threshold). Covered by [`mod-505-principal-mentorship-and-technical-bar`](lessons/mod-505-principal-mentorship-and-technical-bar/) and [`project-502`](projects/project-502-cross-org-influence-and-technical-bar-simulation/).
4. **Industry influence via publications, keynotes, open source** — 9/30 postings, 0.30 (down 0.01 vs. prior cycle; **SUSTAINED AT THRESHOLD for a second consecutive cycle**). Covered by [`mod-506-industry-influence-and-external-voice`](lessons/mod-506-industry-influence-and-external-voice/) and [`project-503`](projects/project-503-industry-influence-artifact-portfolio/). The two-cycle average is 0.305 — clears the material floor but has not strengthened. Hold `mod-506` at current scope.

Also principal-owned per role definition:

5. **Org- and industry-wide ML technical strategy** — 7/30 postings, 0.23 under this cycle's strict tagging convention (now the published default — resolves the methodology reconciliation flagged in 2026-09). Under broader tagging the figure would be 0.43–0.47. Covered by [`mod-501-principal-ml-role-scope`](lessons/mod-501-principal-ml-role-scope/) and [`mod-502-org-and-industry-ml-strategy`](lessons/mod-502-org-and-industry-ml-strategy/).

**Verdict: zero curriculum additions warranted this cycle.** The mature curriculum absorbs every material-threshold requirement, the one theme that newly crossed threshold in the prior cycle (industry influence) has sustained at the floor rather than strengthened, and none of the sub-threshold watch-list signals from 2026-09 escalated: req-tco-cost stabilized at 0.23 rather than continuing its 5× climb, MCP as a named skill did not appear in any new postings, the alignment/RLHF signal remained flat. See [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json).

## Requirement themes → curriculum ownership

**Freq** is the fraction of the 30-posting sample that cited the theme; only ≥ 0.30 is treated as material.

| # | Theme | Freq | Δ vs. prior | Owner role (lowest-level) | Coverage |
|---|---|---:|---:|---|---|
| 1 | Applied-ML architecture at portfolio-and-industry altitude | 0.87 | +0.02 | **`principal-ml-engineer` (this)** | [`mod-503`](lessons/mod-503-north-star-applied-ml-architecture/), [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/) |
| 2 | MLOps / production ML lifecycle depth | 0.77 | +0.04 | `ai-infra-mlops`, `ai-infra-ml-platform`, `senior-ml-engineer`, `ml-engineer` | [`ai-infra-mlops-learning`](https://github.com/ai-infra-curriculum/ai-infra-mlops-learning), [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning), [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-307, [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) mod-108, mod-109. Principal-side slice = application of theme 5. |
| 3 | Cross-org influence without authority (up to VP/SVP/CTO) | 0.57 | +0.03 | **`principal-ml-engineer` (this)** | [`mod-504`](lessons/mod-504-cross-org-influence-without-authority/), [`project-502`](projects/project-502-cross-org-influence-and-technical-bar-simulation/) |
| 4 | Agentic AI platform strategic leadership (LangChain / CrewAI / AutoGen / MCP / RAG at production scale) | 0.50 | +0.08 | `agentic-ai-engineer`, `senior-agentic-ai-engineer`, `agentic-systems-architect`, `rag-engineer`, `llm-application-developer` | [`agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/agentic-ai-engineer-learning), [`senior-agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-agentic-ai-engineer-learning), [`agentic-systems-architect-learning`](https://github.com/ml-engineering-curriculum/agentic-systems-architect-learning), [`rag-engineer-learning`](https://github.com/ml-engineering-curriculum/rag-engineer-learning), [`llm-application-developer-learning`](https://github.com/ml-engineering-curriculum/llm-application-developer-learning). Principal-side slice = application of theme 5. |
| 5 | Gen-AI / multimodal ML strategic leadership | 0.43 | +0.08 | `senior-ml-engineer`, `fine-tuning-engineer`, `nlp-engineer`, `training-pipeline-engineer` | [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-303, mod-304; [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning); [`nlp-engineer-learning`](https://github.com/ml-engineering-curriculum/nlp-engineer-learning); [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning). Principal-side slice = application of theme 6. |
| 6 | Org- and industry-wide ML technical strategy | 0.23<sup>*</sup> | 0.00 | **`principal-ml-engineer` (this)** | [`mod-501`](lessons/mod-501-principal-ml-role-scope/), [`mod-502`](lessons/mod-502-org-and-industry-ml-strategy/), [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/) |
| 7 | Principal mentorship + technical-bar calibration for the ML org | 0.37 | +0.02 | **`principal-ml-engineer` (this)** | [`mod-505`](lessons/mod-505-principal-mentorship-and-technical-bar/), [`project-502`](projects/project-502-cross-org-influence-and-technical-bar-simulation/) |
| 8 | Industry influence — publications, keynotes, open source | **0.30** | **−0.01** | **`principal-ml-engineer` (this)** | [`mod-506`](lessons/mod-506-industry-influence-and-external-voice/), [`project-503`](projects/project-503-industry-influence-artifact-portfolio/). **Second consecutive cycle at ≥ 0.30; signal sustained but not strengthened. Hold current scope.** |
| 9 | GPU / ML capacity cost and TCO at org scope | 0.23 | 0.00 | `staff-ml-engineer` mod-407 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-407. **Watch:** did NOT continue climbing after the 2026-09 5× jump. If it crosses 0.30 across two consecutive cycles, add an exercise to `mod-502` (org-wide capacity-cost bet framing) or `mod-504` (TCO-vs-NPV executive framing). |
| 10 | Responsible AI at org and industry scope | 0.20 | −0.03 | `staff-ml-engineer` (portfolio), `senior-ml-engineer` (system), `head-of-ai-governance`, `ai-governance-analyst`, `ai-infra-security` | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-409; [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-309; [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning); [`ai-governance-analyst-learning`](https://github.com/ml-engineering-curriculum/ai-governance-analyst-learning); [`security-learning`](https://github.com/ai-infra-curriculum/security-learning) |
| 11 | Recommendation / ranking / personalization at scale | 0.13 | −0.02 | `senior-ml-engineer` (architecture), `ml-engineer` (build), `training-pipeline-engineer`, `ai-infra-ml-platform` | [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) mod-110; [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-302, mod-303, mod-306. |
| 12 | Distributed training strategy at scale (FSDP / DeepSpeed / Megatron / tensor parallelism) | 0.10 | −0.02 | `training-pipeline-engineer` (build), `staff-ml-engineer` (program), `ai-infra-performance` (kernel) | [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning); [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403, mod-404; [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning) |
| 13 | Alignment / RLHF / preference-optimization strategy | 0.10 | −0.02 | `fine-tuning-engineer` | [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning) |
| 14 | Executive- and board-level communication | 0.10 | +0.02 | `staff-ml-engineer`; principal-side included in [`mod-504`](lessons/mod-504-cross-org-influence-without-authority/) | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-02 |
| 15 | Foundation-model / large-scale training program leadership | 0.10 | +0.02 | `staff-ml-engineer` mod-403 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403 |
| 16 | Hiring calibration for staff+ ML hires | 0.07 | −0.01 | `staff-ml-engineer` mod-410 | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-03; principal-side bar-calibration for staff+ loops is a `mod-505` topic |
| 17 | ML practitioner workflow foundations | n/a | — | `ml-engineer` (level 20) | Prerequisite. [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) |
| 18 | Single-team ML tech-lead scope | n/a | — | `senior-ml-engineer` (level 30) | Prerequisite. [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) |
| 19 | Multi-team ML portfolio scope | n/a | — | `staff-ml-engineer` (level 40) | Prerequisite. [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) |
| 20 | Direct people management | n/a | — | Peer people-leader branch (executive tracks) | Not in scope. This track is the IC-principal counterpart. |

<sup>*</sup> Theme 6 (org-and-industry-wide strategy) is at 0.23 under the strict tagging rule that is now the published default (resolves the 2026-09 methodology reconciliation). Under the broader tagging convention of the first cycle, this cycle's frequency would be 0.43–0.47. Either way, the theme is principal-owned.

## Methodology

1. Enumerated the target titles (`Principal Machine Learning Engineer`, `Principal ML Engineer`, `Sr. / Senior Principal Machine Learning Engineer`, `Distinguished Machine Learning Engineer`, `Sr. Distinguished Machine Learning Engineer`, `Distinguished AI Engineer`, `Distinguished Software Engineer (ML / AI scope)`, `Applied ML Architect`) across Greenhouse, Lever, Ashby, Built In, LinkedIn snippets, employer ATS (Capital One, Coupang, Walmart, Twilio, ServiceNow, Verizon, Cisco, Autodesk, Amgen, Zillow, Ecolab), physicstoday.org / freehire.me / zapply.jobs aggregators, and specialist boards.
2. **Carried forward** the 26 postings from the 2026-09 cycle, re-observing on 2026-10-08. 23 remain within or at the new strict window at live or carried-forward confidence; 3 fall outside the strict window and were retained at medium or low confidence for segment coverage. Palo Alto Networks's original 2026-04-02 posting was superseded by a live 2026-09-23 variant surfaced this cycle, which was promoted to high confidence.
3. **Surfaced 4 net-new postings** via spot-check WebSearch: Zillow Agentic AI Principal ML (now rendering through the Workday external portal after prior-cycle SPA failure), Amgen Principal ML, Ecolab Principal AI Engineer — ML/MLOps Platform Architect, and Verizon Distinguished Engineer — AI/ML Engineering (distinct from the carried-forward Verizon Applied AI Solutions posting).
4. **Filtered out** plain Machine Learning Engineer (L20), Senior ML Engineer (L30), Staff ML Engineer (L40 — owned by `staff-ml-engineer-learning`), Engineering Manager / Director of ML (peer people-management path), Research Scientist / Applied Scientist (research track), Principal Data Scientist (peer analytics track), Principal AI Infrastructure Engineer / Principal Platform Engineer (peer platform tracks). The Amgen posting carries a 2-year direct-people-management floor and uses explicit "player-coach" framing; retained because the primary verbs remain IC-architecture ("Own enterprise AI/ML architecture, standards, APIs, and guardrails across cloud/on-prem") — analogous to SoundCloud (reports to CTO but IC-scope).
5. Applied the **principal-differentiation heuristic**: for every requirement, articulated what a level-48 principal owns that a level-40 staff does not — the shift from "portfolio-scope multi-team blueprint" to "org- and industry-wide North Star", from "exec-audience RFC leadership commits to" to "board / CTO / SVP-level narrative", from "coach senior tech leads" to "coach staff engineers and set the technical bar for the ML org", from "cited public references" to "author references others cite". Captured in the `seniority_signal` field of every requirement in [`.aicg/job-requirements.json`](.aicg/job-requirements.json).
6. Applied the **ownership rule**: assign coverage to the lowest-level role that genuinely requires the skill; higher levels add depth, architecture, or industry-leadership framing.

### Tagging-rule resolution (resolves 2026-09 open question)

The 2026-09 cycle's open-question #1 flagged that the `req-org-industry-strategy` tagging convention had shifted between the first and second cycles, producing a nominal 0.92 → 0.23 drop that was a methodology reconciliation rather than a market shift. The strict tagging rule — only explicit organizational-scope strategy language counts ("define technical strategy at organizational level", "technical thought leader on adoption across the organization", "guide enterprise AI/ML strategies", "shape roadmaps and visions", "own the enterprise strategy for foundation models") — is now the published default. Frequencies in this cycle hold at 0.23 strict vs. 0.23 strict last cycle. Under broader tagging the figure would be 0.43–0.47. Either way, the theme remains principal-owned at `principal-ml-engineer`; the strict rule removes the cycle-to-cycle whiplash and is the default for future cycles.

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

Verbatim posting evidence for this shift, drawn from the 2026-10 sample:

- **Capital One (Sr. Distinguished AI Engineer)**: "Demonstrated ability to lead and mentor an engineering organization and influence cross-functional stakeholders up to the SVP level"
- **Capital One (Sr. Distinguished AI Engineer, Agentic AI Platform)**: "Demonstrated ability to lead and mentor multiple engineering teams and influence cross-functional stakeholders up to the VP level"
- **Coupang (Principal Engineer, ML)**: "Exceptional ability to influence technical direction across multiple teams and organizations without direct authority"
- **DAT Freight & Analytics (Principal ML)**: "Ability to operate at Principal scope, setting technical direction, identifying and retiring platform risk, mentoring engineers, and delivering solutions whose impact scales across teams and the broader organization"
- **Cisco (Distinguished Software Engineer, Security Platform)**: "Serve as a recognized internal and external thought leader, influencing industry direction"
- **Cisco / ThousandEyes (Distinguished Engineer, ML)**: "shaping roadmaps and visions that drive the success of transformative machine learning projects"
- **ServiceNow (Principal ML)**: "Set the architectural patterns the group works from. Own the hard design calls, run the design reviews, and raise the bar on agentic design"
- **SoundCloud (Senior Principal, ML)**: "This role reports directly to the Chief Technology Officer and will work in lockstep with the Music Intelligence, Content, and Recommendations teams"
- **Ecolab (Principal AI Engineer, new 2026-10)**: "Own the enterprise strategy for foundation models, frontier models, and custom enterprise models"
- **Amgen (Principal ML Engineer, new 2026-10)**: "Own enterprise AI/ML architecture, standards, APIs, and guardrails across cloud/on-prem"
- **Zillow (Agentic AI, Principal ML, new 2026-10)**: "develop large-scale, fault-tolerant multimodal agentic experiences"
- **Verizon (Distinguished Engineer — AI/ML Engineering, new 2026-10)**: "architect and build device-side data telemetry, GenAI-powered agents, and predictive analytics platforms ... digital employees that transform raw device and network telemetry into real-time operational intelligence for Verizon's autonomous network vision"
- **Walmart (Distinguished, AI/ML)**: "Proven record as a senior individual contributor influencing architecture and driving technical excellence across large organizations"

Postings whose primary verbs are executive verbs ("own the P&L", "own budget", "report to CEO", "manage VP-level headcount") belong to the executive track and were excluded from this sample. Postings whose primary verbs are research verbs ("publish state-of-the-art", "lead the research direction", "invent new pretraining objectives") belong to the research track and were excluded.

### Principal IC vs. Executive vs. Research Principal at level 48+

Three distinct level-48+ role families coexist in ML orgs:

- **Principal Machine Learning Engineer** (this track) — IC-principal engineering path. Owns the ML org's technical direction, architecture, and technical bar. No direct reports (or a small people-management floor as a "player-coach" variant — see Amgen/SoundCloud boundary note below).
- **Head of AI / VP of ML / Chief AI Officer** — executive path. Owned by [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning), [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning). Direct reports, headcount, budget, board reporting.
- **Principal Research Scientist / Distinguished Applied Scientist** — research-principal path. No owner in this ecosystem yet; the market draws a hard line between engineering-track Principals (this role) and research-track Principals.

**Player-coach boundary note (new in 2026-10):** Amgen's 2026-09-25 posting carries a 2-year direct-people-management floor alongside IC-principal architecture language. SoundCloud's posting also reports to the CTO. If the player-coach / embedded-people-manager Principal pattern becomes more frequent (≥ 0.20 of the sample across two cycles), the methodology notes will need an explicit tagging-rule change for future cycles — not a curriculum change but a sample-boundary clarification. Currently 2/30 postings = 0.07, well below that bar.

## Delta from prior cycle (2026-09 → 2026-10)

This is a **30-day roll-forward re-sample**. The 2026-09 cycle finished with zero curriculum additions; this cycle shifts the window forward by 30 days to re-check whether anything material has moved. Both samples use the same methodology and the same strict tagging rule.

**Postings carried forward (23/26):** 20 of the 2026-09 postings fall within the new strict window with date_posted ≥ 2026-07-08 or still-live null date_posted; 3 are retained with carried-forward confidence (Capital One Sr. Distinguished Remote 2026-07-01, Capital One Sr. Distinguished Agentic 2026-06-24, Palo Alto Networks superseded by its 2026-09-23 variant).

**Postings dropped from the strict window:**

- **Autodesk Platform** (2026-05-06) — now > 150 days old. Posting is still live; demoted from high to medium for applied-ML-architecture segment coverage.
- **SoundCloud** (2026-04-01) — now > 180 days old. Still live. Demoted from medium to low; will drop next cycle unless re-posted.
- **Palo Alto Networks** (original 2026-04-02) — superseded by live 2026-09-23 variant (surfaced this cycle via zapply.jobs mirror) and PROMOTED to high confidence.

**New employers this cycle (4 net-new segments):**

- **Zillow** — Agentic AI, Principal Machine Learning Engineer, 2026-09-03. The Workday SPA that failed in the prior cycle now renders through the Workday external portal. First consumer / real-estate agentic principal in the sample. [URL](https://zillow.wd5.myworkdayjobs.com/en-US/Zillow_Group_External/job/Agentic-AI--Principal-Machine-Learning-Engineer_P751278-1)
- **Amgen** — Principal Machine Learning Engineer, Remote US, 2026-09-25. First biotech/pharma Principal in the sample. "Player-coach" IC-principal with a 2-year direct-people-management floor. "Own enterprise AI/ML architecture, standards, APIs, and guardrails across cloud/on-prem." Preferred: "Published thought-leadership or conference talks on enterprise GenAI adoption." Salary top: $253K. [URL](https://careers.amgen.com/en/job/washington/principal-machine-learning-engineer/87/101148956448)
- **Ecolab** — Principal AI Engineer — ML/MLOps Platform Architect, Bangalore, 2026-09-21. Industrial / cleantech enterprise AI Platform segment. "Own the enterprise strategy for foundation models, frontier models, and custom enterprise models." [URL](https://freehire.me/jobs/principal-ai-engineer-ml-mlops-platform-architect-ecolab-hulm3rav)
- **Verizon** — Distinguished Engineer, AI/ML Engineering, 2026-09-14. Second Verizon Distinguished posting in-sample (distinct from the Applied AI Solutions role). Telco autonomous-network vision segment. [URL](https://zapply.jobs/jobs/2e0c74ad-6fe5-43d8-9c70-6a9be064ae36/)

**Requirement cluster shifts (summary):**

- **Principal-owned themes are stable or essentially flat:** req-applied-ml-architecture +0.02 (0.87), req-cross-org-influence +0.03 (0.57), req-principal-mentorship-and-bar +0.02 (0.37), req-industry-influence −0.01 (0.30 — sustained at threshold), req-org-industry-strategy flat at 0.23 strict.
- **Lower-owner themes continue rising but stay out of scope:** req-mlops-production-lifecycle +0.04 (0.77), req-agentic-platforms-strategy +0.08 (0.50, now dominant non-architecture theme), req-gen-ai-multimodal-strategy +0.08 (0.43). All correctly linked to agentic / MLOps / gen-AI peer tracks under the ownership rule.
- **Sub-threshold watch-list did NOT escalate:** req-tco-cost stabilized at 0.23 (did not continue climbing after prior cycle's 5× jump); req-alignment-rlhf −0.02 (0.10); MCP as a named skill 0 new postings this cycle (held at 3/30 = 0.10); req-foundation-model-programs +0.02 (0.10) with Ecolab adding a lower-altitude evidence point.

**Verdict:** No material market shift warrants curriculum change. Every material-threshold theme is already covered by the authored curriculum ([`mod-501`](lessons/mod-501-principal-ml-role-scope/) through [`mod-506`](lessons/mod-506-industry-influence-and-external-voice/), [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/) through [`project-503`](projects/project-503-industry-influence-artifact-portfolio/)). The 30-day roll-forward confirms the 2026-09 cycle's finding. **Delta is zero additions.**

## Posting evidence

The 30 postings in the sample, with URLs and the requirement themes each cites, are stored verbatim in [`.aicg/job-requirements.json`](.aicg/job-requirements.json). Highlights by segment:

### Fintech / distinguished-title segment (5 postings — Capital One dominates)

- **Capital One** — Distinguished Machine Learning Engineer (date_posted 2026-07-13, Plano/McLean). "ML industry impact through conference presentations, papers, blog posts, or open source contributions" remains an explicit preferred qualification. Salary top: $307K McLean. [URL](https://www.capitalonecareers.com/job/plano/distinguished-machine-learning-engineer/1732/97747878720)
- **Capital One** — Sr. Distinguished AI Engineer, Remote-Eligible (2026-07-01). "Demonstrated ability to lead and mentor an engineering organization and influence cross-functional stakeholders up to the SVP level." Salary top: $392K SF/NYC/San Jose. [URL](https://www.capitalonecareers.com/job/san-francisco/sr-distinguished-ai-engineer-remote-eligible/1732/97191343504)
- **Capital One** — Sr. Distinguished AI Engineer, Agentic AI Platform (2026-06-24). LangChain / CrewAI / Semantic Kernel / AutoGen and LLMOps (Vertex AI, SageMaker, Azure ML) as preferred requirements. [URL](https://www.capitalonecareers.com/job/san-francisco/senior-distinguished-ai-engineer-agentic-ai-platform/1732/96890760608)
- **Block** — Staff/Principal Machine Learning Engineer (Modeling), Credit. "Proficiency with AI-native development workflows. You use LLMs, agentic coding tools, and AI-assisted automation as a regular part of how you build and ship." [URL](https://builtin.com/job/staff-principal-machine-learning-engineer-modeling-credit/8472833)
- **Upstart** — Staff/Principal ML Engineer. "This is a high influence role suited for those who enjoy combining science innovation, with cross functional collaboration and advisory." [URL](https://careers.upstart.com/jobs/principal-machine-learning-engineer)

### Consumer / recsys / adtech / retail segment (8 postings — Zillow new)

- **Zillow** — Agentic AI, Principal Machine Learning Engineer (2026-09-03, Remote-friendly). **New this cycle.** "develop large-scale, fault-tolerant multimodal agentic experiences ... Voice AI and Deep Research." Salary top: $310K + Equity. [URL](https://zillow.wd5.myworkdayjobs.com/en-US/Zillow_Group_External/job/Agentic-AI--Principal-Machine-Learning-Engineer_P751278-1)
- **Coupang** — Principal Engineer, ML (Ads Serving & ML Platform), Seattle (2026-09-08). "Exceptional ability to influence technical direction across multiple teams and organizations without direct authority." Salary top: $386K. [URL](https://boards.greenhouse.io/coupang/jobs/8175850)
- **Walmart** — Distinguished Software Engineer, AI/ML — Agentic Systems, Sunnyvale. Salary top: $338K. [URL](https://careers.walmart.com/us/en/jobs/R-2451270)
- **Walmart** — Distinguished Software Engineer, AI/ML — Agentic Systems & SRE, Sunnyvale. [URL](https://careers.walmart.com/us/en/jobs/R-2533229)
- **Pinterest** — Principal ML Engineer, Content Recommendations. Salary top: $480K. [URL](https://builtin.com/job/principal-machine-learning-engineer-content-recommendations/7731228)
- **Rula** — Principal AI Engineer, Personalization and Recommendation, Remote (2026-08-26). "Demonstrated ability to define technical strategy and guide the broader AI/ML infrastructure ecosystem." [URL](https://careers.wing.vc/companies/rula/jobs/91149411-principal-ai-engineer-personalization-and-recommendation-remote)
- **DAT Freight & Analytics** — Principal ML Engineer, Seattle (Hybrid). "Ability to operate at Principal scope, setting technical direction, identifying and retiring platform risk, mentoring engineers, and delivering solutions whose impact scales across teams and the broader organization." Salary top: $320K. [URL](https://builtin.com/job/principal-machine-learning-engineer/7934886)
- **SoundCloud** — Senior Principal Engineer, Machine Learning, Remote NY (2026-04-01, now low confidence). "This role reports directly to the Chief Technology Officer." [URL](https://jobgether.com/offer/69cd2c2e5bd3b40540a4bd53-senior-principal-engineer-machine-learning)

### Enterprise / SaaS / cybersecurity / telco segment (9 postings — Verizon AI/ML new)

- **Twilio** — Principal Machine Learning Engineer, Remote US. "Spearhead ML/AI focused research projects within Twilio's Emerging Technology & Innovation (ETI) organization." Preferred: "you have previously shared your ideas in public forums through blog posts, meetup presentations, or speaking at conferences." Salary top: $239K. [URL](https://boards.greenhouse.io/twilio/jobs/3535517)
- **Twilio** — Principal ML & Data Engineer, Remote US. MLOps stack named at requirement-level (MLflow, Kubeflow, SageMaker, Vertex AI). Salary top: $271K. [URL](https://builtin.com/job/machine-learning-data-engineer-p5/6844774)
- **ServiceNow** — Principal Machine Learning Engineer. "Hands-on depth designing, shipping, and operating agentic systems in production — multi-agent orchestration, tool calling, planning loops, memory, and failure recovery. Not prototypes." Salary top: $420K. [URL](https://jobs.smartrecruiters.com/ServiceNow/744000145376219-principal-machine-learning-engineer)
- **Verizon** — Distinguished Engineer, Applied AI Solutions, Irving/Alpharetta/Basking Ridge. "Act as a technical thought leader on Gen AI adoption across the organization." Salary top: $263K. [URL](https://mycareer.verizon.com/jobs/r-1100363/distinguished-engineer-applied-ai-solutions/)
- **Verizon** — Distinguished Engineer, AI/ML Engineering (2026-09-14). **New this cycle.** "architect and build device-side data telemetry, GenAI-powered agents, and predictive analytics platforms ... digital employees that transform raw device and network telemetry into real-time operational intelligence for Verizon's autonomous network vision." [URL](https://zapply.jobs/jobs/2e0c74ad-6fe5-43d8-9c70-6a9be064ae36/)
- **LexisNexis** — Principal Machine Learning Engineer I, Raleigh NC. "Provide architectural direction and code-level guidance." Salary top: $253K. [URL](https://builtin.com/job/principal-machine-learning-engineer-i/9690092)
- **ConnectWise** — Principal Machine Learning Engineer, Remote (IND). Names supervised fine-tuning, DPO, RFT, LoRA/QLoRA, BERT/ModernBERT, LLM-as-judge as required. [URL](https://job-boards.greenhouse.io/connectwise/jobs/4707883005)
- **Palo Alto Networks** — Principal ML Engineer, Santa Clara (2026-09-23 live variant — promoted this cycle to high confidence). [URL](https://zapply.jobs/jobs/42404cef-8ce9-49da-9234-6a24f0d60d11/)

### Industrial / biotech / platform segment (3 postings — all new this cycle)

- **Amgen** — Principal Machine Learning Engineer, Remote US (2026-09-25). **New this cycle.** "Own enterprise AI/ML architecture, standards, APIs, and guardrails across cloud/on-prem." Carries 2-year direct-people-management floor as a player-coach IC-principal. Preferred: "Published thought-leadership or conference talks on enterprise GenAI adoption." Salary top: $253K. [URL](https://careers.amgen.com/en/job/washington/principal-machine-learning-engineer/87/101148956448)
- **Ecolab** — Principal AI Engineer — ML/MLOps Platform Architect, Bangalore (2026-09-21). **New this cycle.** "Own the enterprise strategy for foundation models, frontier models, and custom enterprise models." [URL](https://freehire.me/jobs/principal-ai-engineer-ml-mlops-platform-architect-ecolab-hulm3rav)
- **Cogniify** — Principal AI/ML Engineer, US East/West Coast + US Remote (2026-09-03). Names MCP / SOC2 / HIPAA / GDPR at preferred level. [URL](https://builtin.com/job/principal-ai-ml-engineer-usa/9752057)

### Distinguished-title enterprise segment (Cisco, 2 postings)

- **Cisco (ThousandEyes)** — Distinguished Engineer, Machine Learning (Modeling and Tuning), SF Hybrid. "Shaping roadmaps and visions that drive the success of transformative machine learning projects." Salary top: $372K. 15+ years required. [URL](https://www.builtinsf.com/job/distinguished-engineer-aiops-hybrid/2162086)
- **Cisco (Security and Policy Platform)** — Distinguished Software Engineer, Remote US (2026-08-16). "Serve as a recognized internal and external thought leader, influencing industry direction." 15+ years required. Salary top: $407K. [URL](https://remote100k.com/remote-job/cisco-distinguished-software-engineer)

### AI-native / scientific / applied-ML architecture segment (3 postings)

- **Autodesk** — Senior Principal ML Engineer (Foundation Model Systems), Remote US/CA. Names the full frontier training stack (FSDP, DeepSpeed, Megatron-LM, DDP, tensor parallelism, pipeline parallelism) plus RLHF at requirement-level specificity. Salary top: $296K. [URL](https://builtin.com/job/senior-principal-machine-learning-engineer/8958113)
- **Autodesk** — Principal ML Engineer, ML Platform and Systems Architecture, Remote US/CA (2026-05-06, demoted to medium this cycle). "This is a senior technical leadership role for an engineer who excels at system architecture." Salary top: $272K. [URL](https://jobs.aihub.masstech.org/companies/autodesk/jobs/77521901-principal-ml-engineer-machine-learning-platform-and-systems-architecture)
- **Airbnb** — Principal ML Engineer, LLM Fine-tuning and Optimization, Remote US. Preferred: "Publications at peer-reviewed AI conferences (e.g., NeurIPS, CVPR, ICML, ICLR, ICCV, and ACL)." Salary top: $365K. [URL](https://careers.airbnb.com/positions/7955579/)

### AI consulting / defense segment (1 posting)

- **Raft** — Principal Machine Learning Engineer, Remote US. Requires "agentic workflows with tool calling, Model Context Protocol (MCP) implementations, and multi-step reasoning systems" + Top Secret clearance. [URL](https://job-boards.greenhouse.io/raft/jobs/5739876004)

Full failed-fetch list (SPAs and 404s) is captured in [`.aicg/job-requirements.json → failed_fetches`](.aicg/job-requirements.json).

## What we did NOT propose (and why)

| Tempting addition | Why we rejected it |
|-------------------|--------------------|
| A module or scope-up specifically for MCP (Model Context Protocol) named skill | MCP appears in only 3/30 postings (Raft, Cogniify, ServiceNow — all carried forward from the 2026-09 cycle). ZERO new postings this cycle name MCP, so the anticipated mainstreaming has not accelerated at principal altitude. Implementation belongs to the agentic peer tracks ([`agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/agentic-ai-engineer-learning), [`agentic-systems-architect-learning`](https://github.com/ml-engineering-curriculum/agentic-systems-architect-learning)); principal-side slice is "evaluate MCP as an agentic-platform bet" — an application of the existing `mod-502` bet-portfolio framing. |
| A module on FSDP / DeepSpeed / Megatron / tensor parallelism at principal altitude | Named in only 2/30 postings this cycle (Autodesk Foundation Model Systems, Airbnb). Below threshold and duplicative of [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) + [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403 / mod-404. |
| A capacity / cost / TCO module at principal altitude | STABILIZED this cycle at 0.23 (did not continue climbing after prior cycle's 5× jump). The predicted threshold crossing did not happen. Keep on watch list; if it crosses 0.30 across two consecutive cycles, add an exercise to `mod-502` (org-wide capacity-cost bet framing) or `mod-504` (TCO-vs-NPV executive framing, picking up the Amgen signal). |
| A responsible AI at org scope module at principal altitude | Stable at 0.20 (down 0.03) — below threshold. Portfolio-scope responsible AI is owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-409. |
| A scope-up of `mod-506` (industry influence) now that it has crossed threshold for a second consecutive cycle | Frequency sustained at 0.30 (down 0.01 from last cycle's 0.31). The signal is at the material floor but has not strengthened — the two-cycle average is 0.305. Wait for the next cycle; if freq rises above 0.35, add an exercise on standards-body contribution or a keynote-slide portfolio. If freq drops below 0.30 next cycle, hold at current scope. |
| A new module for the player-coach / embedded-people-manager Principal variant that Amgen exemplifies | Only 2/30 postings fit the pattern (Amgen, SoundCloud) = 0.07. Keep in boundary note; if the pattern reaches ≥ 0.20 across two consecutive cycles, revisit the sample-inclusion rule in the methodology — not the curriculum. |
| Direct people-management coverage | Peer executive track ([`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning), [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning)) owns this. |

## External resources for out-of-scope topics

These resources cover topics that are NOT principal-ML-engineer ownership (per the Ownership Rule) but that Principal ML Engineers are commonly expected to reason about at the strategy / bet altitude. They are linked here so principal-track learners can ground their bets without the principal curriculum duplicating implementation-level material owned in lower-level tracks.

- **Applied-ML architecture at industry altitude:** Chip Huyen, *Designing Machine Learning Systems* (O'Reilly, 2022) — canonical text; Google Machine Learning Rules (rules-of-ml); Meta's *Applied Machine Learning at Facebook* engineering blog; Airbnb Engineering blog series on Bighead / Zipline; Uber Engineering blog on Michelangelo.
- **Staff-plus IC leadership progression to principal:** Will Larson, *Staff Engineer: Leadership beyond the management track* (Stripe Press, 2021); StaffEng.com Distinguished / Fellow interviews; Engineering Ladders principal-rung criteria (https://www.engineeringladders.com/); progression.fyi collected frameworks.
- **Foundation-model / large-scale training programs:** Chinchilla scaling-laws paper (Hoffmann et al. 2022); NVIDIA Megatron-LM; Microsoft DeepSpeed / ZeRO; PyTorch FSDP2 documentation; Meta Llama 3 technical report — used as principal-side worked examples, implementation lives at [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) and [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403 / mod-404.
- **Agentic AI platforms:** LangGraph docs (https://langchain-ai.github.io/langgraph/); OpenAI Assistants API / Anthropic tool-use documentation; Semantic Kernel and AutoGen; Model Context Protocol spec (https://modelcontextprotocol.io); production-agentic engineering blog series (Pinterest, Salesforce, ServiceNow) — implementation lives at agentic peer tracks.
- **Responsible AI at org scope:** NIST AI Risk Management Framework 1.0 + Generative AI Profile; EU AI Act (Regulation 2024/1689); Google Model Cards paper; Datasheets for Datasets paper — depth lives at [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-409 and governance tracks.
- **Industry influence / keynote craft:** ICML / NeurIPS / KDD industry-track submission guides; O'Reilly AI Conference speaker guidance; QCon Engineering Culture track; the *Papers With Code* newsletter pattern for productive dissemination.

## Ownership map — quick reference

- **Principal ML Engineer (this track, level 48)** owns org- and industry-wide ML technical strategy, applied-ML architecture at portfolio-and-industry altitude, cross-org influence up to SVP/CTO, principal-level mentorship + technical-bar calibration for the ML org, and the external-voice / industry-influence facet (sustained at ≥ 0.30 for a second consecutive cycle this cycle). Everything below the level-40 staff scope is inherited, not re-taught.
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

<!-- needs-research: re-run 2027-01-08 with the same sampling method. Watch for: (a) whether req-industry-influence sustains >= 0.30 for a third consecutive cycle (if yes AND freq rises above 0.35, add an exercise on standards-body contribution or a keynote-slide portfolio to mod-506 — but NOT a new module; if freq drops below 0.30, hold mod-506 at current scope); (b) whether req-tco-cost crosses 0.30 after this cycle's stabilization at 0.23 (if yes across two consecutive cycles, add an exercise to mod-502 for capacity-cost bet framing OR mod-504 if the Amgen 'TCO vs. NPV' executive framing generalizes); (c) whether MCP breaks out of the 3-posting plateau (if 8+ postings, coordinate cross-repo with agentic peer tracks — still not this track's ownership); (d) whether the player-coach / embedded-people-manager Principal pattern (Amgen, SoundCloud) crosses 0.20 of the sample — not a curriculum action but a sample-inclusion methodology clarification. -->

The 30 in-window postings sampled clear the ≥ 25 threshold with room to spare. Four principal-scope requirements sit at or above the 0.30 material threshold (applied-ML architecture 0.87, cross-org influence 0.57, principal mentorship 0.37, industry influence 0.30 — sustained for a second consecutive cycle) and belong at this level. Org-and-industry-wide strategy sits at 0.23 under the strict tagging rule now serving as the default (0.43–0.47 under broader tagging — still principal-owned). All other requirements at material frequency (≥ 0.30) are owned by lower-level tracks under the Ownership Rule — this packet catalogues them and does not duplicate their coverage.

The authored curriculum ([`mod-501`](lessons/mod-501-principal-ml-role-scope/) through [`mod-506`](lessons/mod-506-industry-influence-and-external-voice/), [`project-501`](projects/project-501-org-ml-north-star-and-reference-architecture/) through [`project-503`](projects/project-503-industry-influence-artifact-portfolio/)) absorbs every material-threshold requirement. The one theme that newly crossed threshold in the prior cycle (`req-industry-influence`) has sustained at the floor without strengthening; mod-506 is correctly scoped at current size. The 30-day roll-forward confirms the 2026-09 cycle's finding that no material shift warrants curriculum change. The proposed delta this cycle is **zero additions**, per [`.aicg/curriculum-plan-delta.json`](.aicg/curriculum-plan-delta.json).
