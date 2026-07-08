# Prerequisites — Principal Machine Learning Engineer Track

**Role level:** 48 (principal IC altitude, ML engineering ladder)

This track is a **level-up** curriculum on top of the entire staff-plus IC ladder. It assumes the full level-40 [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) curriculum, the level-30 [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) curriculum beneath it, and the level-20 [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) foundation beneath that, in hand. It does not re-teach any of it. Do not start here without the prerequisites below.

## Assumed foundation (level 40 — Staff Machine Learning Engineer)

Owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning). You should already be able to:

- Blueprint 3–5 production ML systems as one portfolio; author a multi-system RFC that argues for merge / split / share of a substrate across teams and defends the migration cost.
- Scope a foundation-model pretraining or large-scale fine-tune program (Chinchilla-style compute-optimal trade-off, data mixture, ablation sequencing, capability-vs-safety post-training investment), pick the parallelism recipe (FSDP / tensor-parallel / pipeline-parallel / 3D-parallel) and defend it, estimate MFU, and set the failure-mode budget.
- Make org-scope build-vs-adopt calls on the ML platform substrate (feature store, model registry, eval platform, training platform, inference gateway); author the paved-road consumer contract with the peer platform teams and the multi-team gap / contribute-back RFCs.
- Standardise the offline eval harness across ML teams, own the LLM-as-judge policy at org scope, set the shadow / canary / progressive-rollout contract every team follows.
- Build a portfolio-level GPU capacity forecast; choose the capacity portfolio (reserved / on-demand / spot / multi-cloud / self-hosted); apply FinOps discipline; author a CFO-readable TCO model.
- Standardise ML-specific SLI / SLO vocabulary across a portfolio; run multi-team incident command using the Google SRE structure adapted to ML failure classes; author the org-standard postmortem template.
- Author a portfolio-scope AI risk register (NIST AI RMF + Gen-AI profile), classify each system against EU AI Act tiers, standardise model cards and datasheets, set the pre-launch review gate.
- Author a multi-quarter ML program roadmap leadership commits to; write executive-audience one-pagers and RFCs; run staff-plus hiring loops and calibrate senior ML engineers; coach senior tech leads and partner with the EM peer; sustain the technical bar without sliding into IC-only or management-only work.

## Assumed foundation (level 30 — Senior Machine Learning Engineer)

Owned by [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning). Single-team tech-lead scope — single-system architecture RFC, single-team eval harness, single-team ML SLOs, single-team responsible-AI review, coaching mid-level engineers, rubric-based interview authoring.

## Assumed foundation (level 20 — Machine Learning Engineer)

Owned by [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning). Build-altitude fundamentals — problem framing, data ingest / cleaning / features, classical modelling, PyTorch training loops, MLflow experiment tracking, FastAPI + Docker serving, drift monitoring, ML system design at working-level altitude.

If any of the above is shaky, complete the corresponding track first. **This track will assume — and lift each of those dimensions to org- and industry-wide scope — but will not re-teach them.**

## Assumed lived experience

The principal IC role is defined at least as much by the situations the engineer has been in as by the skills they hold. Before this track lands, you should have shipped at least one staff-scope ML portfolio program (per `staff-ml-engineer-learning` project-401 / 402 / 403 or the field equivalent) and have accumulated:

- Authored and defended at least one portfolio-scope multi-system RFC that another staff engineer or a director pushed back on.
- Led a staff-scope ML program — foundation-model training program, RecSys re-platform, cross-team eval overhaul, or an org-scope MLOps or platform-strategy shift — through leadership commit and into delivery.
- Sat in staff-plus hiring loops as a calibrator (not just an interviewer) and given hire / no-hire / staff-vs-senior signals with rubric evidence.
- Written at least one executive-audience RFC or one-pager that a VP or SVP acted on (approved, deferred, or amended).
- Coached at least one senior tech lead (L30) through a design review, a launch, or an incident postmortem.
- Partnered with a peer platform team (level-40 architect or team lead) as a paved-road consumer and negotiated a contract that outlived the specific system that motivated it.

Without these lived experiences, the principal-scope modules (mod-502 org-and-industry ML strategy, mod-503 north-star applied-ML architecture, mod-504 cross-org influence, mod-505 principal mentorship & bar) and the project-501 / 502 capstones will feel abstract. If any of the above is missing, extend `staff-ml-engineer-learning` project-403 (staff-plus-tech-leadership-simulation) or find a field opportunity that closes the gap before starting here.

## Recommended reading before you start

- Will Larson, *[Staff Engineer: Leadership beyond the management track](https://staffeng.com/book)* (Stripe Press, 2021) — the canonical staff-plus IC ladder text. This principal track lifts what Larson calls the Fellow / Distinguished IC archetype; the book still applies.
- [StaffEng.com Distinguished / Fellow interviews](https://staffeng.com/stories/) — real IC-principal engineer stories from Slack, Stripe, Google, Netflix, Fastly, and others.
- Chip Huyen, *Designing Machine Learning Systems* (O'Reilly, 2022) — grounding for the mod-503 north-star applied-ML architecture module.
- The Google ML [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml) — grounding for the ML-org-scope architectural discipline mod-503 sets.
- The applied-ML engineering blog series from Meta ([Applied Machine Learning at Facebook](https://engineering.fb.com/2018/05/09/core-infra/applied-machine-learning-at-facebook-a-datacenter-infrastructure-perspective/) and follow-ups), Airbnb ([Bighead / Zipline](https://medium.com/airbnb-engineering/tagged/machine-learning)), Uber ([Michelangelo](https://www.uber.com/en-JP/blog/michelangelo-machine-learning-platform/)), Pinterest ([content-recommendation and ads-quality series](https://medium.com/pinterest-engineering)) — mod-502 and mod-503 use these as case studies.
- [NIST AI Risk Management Framework 1.0](https://www.nist.gov/itl/ai-risk-management-framework) and the [Gen-AI Profile overlay](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) — the responsible-AI grounding the principal-scope North Star (mod-502) refers to, even though portfolio-scope authoring is owned at `staff-ml-engineer-learning` mod-409.
- Papers you should have opinions on for the mod-502 bet portfolio: [Chinchilla](https://arxiv.org/abs/2203.15556) for compute-optimal framing, the [Meta Llama 3 technical report](https://ai.meta.com/research/publications/the-llama-3-herd-of-models/) for foundation-model program economics, the [DeepSeek-V3 technical report](https://arxiv.org/abs/2412.19437) for capacity-vs-quality tradeoff at frontier scale.
- For mod-504 (cross-org influence): the *Staff Engineer* interviews on coalition-building; internal-to-a-tech-company case studies of paved-road adoption (Netflix, Stripe, Airbnb engineering blogs) — the sequencing pattern the module teaches is grounded in these.
- For mod-506 (industry influence): the industry-track submission guides for [ICML](https://icml.cc/), [NeurIPS](https://neurips.cc/), and [KDD](https://kdd.org/kdd2025/); the *Papers With Code* newsletter pattern for productive dissemination; the [O'Reilly AI Conference](https://www.oreilly.com/conferences/) and [QCon](https://qconferences.com/) speaker-craft guides.

## Recommended tooling access

You do not need production-scale compute to run this curriculum — the principal-scope artifacts are documents, contracts, and reviews, not training runs. That said:

- Access to the tooling stack from the staff track — MLflow, PyTorch, an LLM API key or local inference stack, a small cluster or multi-GPU node — is still assumed for grounding examples.
- A diagramming environment for the mod-503 living-architecture artifact (Excalidraw, Structurizr, Mermaid, or the equivalent). Whatever the team already uses is fine; the point is that the artifact stays maintainable.
- A shared-document environment (Google Docs, Notion, Confluence, or a versioned Markdown repo) for the mod-502 North Star one-pager and deep-dive companion.

## Peer specialist and peer platform tracks worth knowing exist

The principal ML engineer routinely defers to and coordinates with these owners. You should be able to read the shape of their contract and set one:

- `training-pipeline-engineer-learning`, `ai-infra-performance-learning` — distributed-training implementation and cluster tuning.
- `fine-tuning-engineer-learning`, `nlp-engineer-learning`, `rag-engineer-learning`, `llm-application-developer-learning`, `applied-ai-engineer-learning` — LLM and applied-ML specialisations.
- `agentic-ai-engineer-learning`, `senior-agentic-ai-engineer-learning`, `agentic-systems-architect-learning` — agentic-AI ladder that the principal treats as a bet, not an implementation project.
- `model-evaluation-engineer-learning`, `ai-eval-engineer-learning` — evaluation-platform depth.
- `ai-infra-ml-platform-learning`, `ai-infra-mlops-learning` — the paved-road ML platforms this principal track sets the org contract for at north-star altitude.
- `ai-infra-security-learning`, `ai-governance-analyst-learning`, `head-of-ai-governance-learning` — the security and governance counterparts. The principal partners with them; they own policy authoring.

## Peer level-48+ tracks worth understanding

The IC-principal ladder is one of several level-48+ paths. Understand which one you are on:

- **This track** — Principal ML Engineer (IC-principal, ML engineering ladder). No direct reports.
- [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning) — peer executive path (direct reports, headcount, budget, board reporting). If a posting reads as executive scope (P&L, headcount ownership, board reporting), the fit is with that track rather than this one.
- [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) — peer executive-branch path centred on AI governance.
- [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) — peer platform-side principal path (level 50). Complementary scope: platform vs. modelling. This track's mod-505 references it as the peer principal owner for the platform side.
- [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) — peer platform-architecture principal path (level 50).
- **Principal Research Scientist / Distinguished Applied Scientist** — peer research-principal path at AI labs (Anthropic / OpenAI / DeepMind / Google Research / Meta AI). No owner in this ecosystem yet; documented in `JOB_REQUIREMENTS.md`. Postings whose primary verbs are research verbs ("publish state-of-the-art", "invent new pretraining objectives") belong to this path, not this one.
