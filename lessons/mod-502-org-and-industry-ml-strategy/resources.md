# Resources for mod-502-org-and-industry-ml-strategy

Curated primary references for the chapters and exercises in this module. Every entry below is a primary source (official publication, standards body, engineering blog, or the paired evidence catalogue) or a canonical secondary source (textbook, staff-plus IC ladder text). Nothing here is invented.

## The evidence catalogue for this module

- [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) — the 26-posting 2026-Q2 sample and the requirement-to-coverage map. Theme 1 (org- and industry-wide ML technical strategy) at 0.92 frequency is this module's ground truth. Every principal-scope posting quoted in the chapters (SoundCloud, Pinterest, Capital One, Instacart, Ibotta, Upstart, Bumble) is sourced from this catalogue.
- [`../../.aicg/job-requirements.json`](../../.aicg/job-requirements.json) — machine-readable posting evidence with per-posting URL, requirement citations, and confidence classification.
- [`../../.aicg/curriculum-plan.json`](../../.aicg/curriculum-plan.json) — the module and project plan the track is scoped against.

## Sibling modules in this track

The North Star this module authors is one of a paired set. These sibling modules matter directly:

- [`../mod-501-principal-ml-role-scope/`](../mod-501-principal-ml-role-scope/) — the vocabulary and hand-off contracts every chapter in this module presupposes. Chapters 1 and 6 of mod-501 are the immediate prerequisites.
- [`../mod-503-north-star-applied-ml-architecture/`](../mod-503-north-star-applied-ml-architecture/) — the north-star applied-ML architecture (living diagrams, canonical APIs) the North Star pairs with. Chapter 2 (row-2 RecSys/personalization) and chapter 7 (deep-dive companion) both cite this module.
- [`../mod-504-cross-org-influence-without-authority/`](../mod-504-cross-org-influence-without-authority/) — the material that turns the mod-502 pair of artifacts into an SVP / CTO ratification. Chapter 7 hands the artifacts to mod-504 for defense.
- [`../mod-505-principal-mentorship-and-technical-bar/`](../mod-505-principal-mentorship-and-technical-bar/) — the review-bar discipline that ensures the org's day-to-day ML engineering practice converges on the North Star row 5 (MLOps as org contract).
- [`../../projects/project-501-org-ml-north-star-and-reference-architecture/`](../../projects/project-501-org-ml-north-star-and-reference-architecture/) — the capstone that integrates mod-501 through mod-504 into a defended North Star + reference architecture pair.

## Peer principal-scope tracks — the closest structural parallel

The North Star's bet portfolio (chapter 2) sits next to the peer platform-side principal's platform-bet portfolio; the two are best read side by side.

- [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) — level-50 platform-side principal path. Mod-505 (long-term technical bets) is the closest structural parallel to mod-502 in this track — platform bets sequenced across the same 3-to-5-year horizon. Chapters 2, 3, and 6 of this module cross-reference.
- [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) — level-50 platform-architecture principal path.

## Staff-plus IC prerequisites — the material the North Star lifts

The North Star cites but does not duplicate the following staff-scope material. If any of these dimensions is shaky, the mod-502 hand-off contracts (chapter 2 and chapter 5) will feel abstract:

- [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) — level-40 curriculum. Especially:
  - mod-401 / mod-402 — multi-team ML architecture (the portfolio blueprint the north-star architecture composes).
  - mod-403 — foundation-model programs (the recipe layer of row 4).
  - mod-404 — distributed-training strategy (the parallelism-recipe layer under row 4).
  - mod-405 / mod-406 — cross-team eval program (the seam under row 5's canonical eval).
  - mod-407 — portfolio TCO / capacity (the cost-signal ground truth under chapter 6 category 2).
  - mod-409 — portfolio-scope responsible AI (the register and tiering the row-5 contract references).
  - mod-410 — staff-plus technical leadership, including the exec-audience RFC portfolio and the multi-quarter portfolio roadmap the mod-502 seam pairs with (chapter 5).

## Peer specialist tracks — the recipe layer for each bet row

Each row of chapter 2 cites one or more of these tracks. The North Star row commits to the strategic bet; the specialist track owns the recipe:

- **Row 1 (Gen-AI direction):**
  - [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-303, mod-304 — production Gen-AI integration.
  - [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning) — mid-tier post-training programs.
  - [`nlp-engineer-learning`](https://github.com/ml-engineering-curriculum/nlp-engineer-learning) — NLP-adjacent depth.
  - [`applied-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/applied-ai-engineer-learning) — application-layer Gen-AI engineering.
- **Row 2 (RecSys / personalization direction):**
  - [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) mod-110 — RecSys foundations.
  - [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-302, mod-303, mod-306 — production ranking / retrieval.
  - [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning) — feature store / registry / serving substrate.
- **Row 3 (Agentic-AI direction):**
  - [`agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/agentic-ai-engineer-learning) / [`senior-agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-agentic-ai-engineer-learning) — agent-pattern depth.
  - [`agentic-systems-architect-learning`](https://github.com/ml-engineering-curriculum/agentic-systems-architect-learning) — agent-system architecture.
  - [`rag-engineer-learning`](https://github.com/ml-engineering-curriculum/rag-engineer-learning) — RAG depth (the boundary partner in chapter 2 row 3).
  - [`llm-application-developer-learning`](https://github.com/ml-engineering-curriculum/llm-application-developer-learning) — application-layer LLM engineering.
- **Row 4 (Foundation-model program):**
  - [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) — training-pipeline recipe depth.
  - [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning) — kernel and parallelism depth.
- **Row 5 (MLOps as org contract):**
  - [`ai-infra-mlops-learning`](https://github.com/ai-infra-curriculum/ai-infra-mlops-learning) — MLOps build depth.
  - [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning) — paved-road platform build.
  - [`model-evaluation-engineer-learning`](https://github.com/ml-engineering-curriculum/model-evaluation-engineer-learning) / [`ai-eval-engineer-learning`](https://github.com/ml-engineering-curriculum/ai-eval-engineer-learning) — canonical eval platform depth.
  - [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) — policy authoring, sign-off partnership.

## Applied-ML system architecture and strategy — canonical texts

Foundational reading for the bet-altitude framing in chapters 1, 2, and 7.

- Chip Huyen, *Designing Machine Learning Systems* (O'Reilly, 2022). Grounds the vocabulary chapter 1 uses for "system", "portfolio", "org-scope architecture" and the ladder implied between them. Cited in chapter 1 and by mod-501.
- Google, [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml) — the applied-ML engineering discipline reference. Cited by mod-501 as the review-bar reference; useful here for the row-5 (MLOps as org contract) framing.
- Meta engineering blog, [Applied Machine Learning at Facebook — A Datacenter Infrastructure Perspective](https://engineering.fb.com/2018/05/09/core-infra/applied-machine-learning-at-facebook-a-datacenter-infrastructure-perspective/). Older but structurally the shape of a Gen-AI / RecSys / MLOps org-scope framing at a large employer.
- Uber engineering blog, [Michelangelo](https://www.uber.com/blog/michelangelo-machine-learning-platform/) and the follow-on platform posts. Reference for what a row-5 paved-road contract looks like in practice at scale.
- Airbnb engineering blog, [machine-learning tagged posts](https://medium.com/airbnb-engineering/tagged/machine-learning) — Bighead, Zipline, and their successors. Case study for a row-5 org contract that evolved through multiple bets.
- Pinterest engineering blog, [content recommendations and ads-quality posts](https://medium.com/pinterest-engineering). The org whose posting is the chapter-1 architecture-adjacent template ("unified technical architecture and defining a roadmap for industry-leading methodology"); its blog is the primary source for what that architecture looks like when it has been maintained for years.
- Netflix Tech Blog, [machine-learning posts](https://netflixtechblog.com/tagged/machine-learning). Case-study material for RecSys row 2 and MLOps row 5.
- LinkedIn Engineering, [Feathr feature store post](https://engineering.linkedin.com/blog/2022/open-sourcing-feathr---linkedin-s-feature-store-for-productive-machine-) and related platform-post series. Structural parallel for a row-5 canonical feature-substrate commitment.

## Foundation-model programs, compute economics, cost-signal grounding

Cited in chapter 2 row 4 and in chapter 6 category 2 (cost signals). Implementation depth lives at the specialist tracks named above; the module uses these as principal-side worked examples.

- Hoffmann et al., [*Training Compute-Optimal Large Language Models*](https://arxiv.org/abs/2203.15556) (Chinchilla, DeepMind, 2022) — the compute-optimal framing every foundation-model program bet inherits. The chapter-6 category-1 signal example.
- Meta AI, [*The Llama 3 Herd of Models*](https://ai.meta.com/research/publications/the-llama-3-herd-of-models/) technical report. Frontier-scale foundation-model program economics and post-training methodology. Chapter-6 category-1 signal example.
- DeepSeek AI, [*DeepSeek-V3 Technical Report*](https://arxiv.org/abs/2412.19437) — capacity-vs-quality tradeoff at frontier scale; a specific example of a category-1 signal that materially shifts row-1 economics conversations.
- NVIDIA, [Megatron-LM](https://github.com/NVIDIA/Megatron-LM). Microsoft, [DeepSpeed / ZeRO](https://www.deepspeed.ai/). PyTorch, [FSDP2 documentation](https://pytorch.org/docs/stable/fsdp.html). Parallelism-recipe primary sources; the row-4 recipe layer.
- OpenAI, [API pricing page](https://openai.com/api/pricing/). Anthropic, [API pricing page](https://www.anthropic.com/pricing). Google, [Vertex AI generative AI pricing](https://cloud.google.com/vertex-ai/generative-ai/pricing). Frontier-supplier pricing sources cited in chapter 6 category 2. Exercise-04 signal rows point at these.

## Regulatory and compliance frameworks — chapter 6 category 3

- **EU AI Act** — [Regulation (EU) 2024/1689](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:L_202401689), Official Journal of the European Union. The phased-obligation timeline, GPAI obligations, and high-risk-system tier definitions cited in chapters 2 (row 5), 4 (sunset criteria), and 6 (category 3).
- **European AI Office** — [European Commission's AI Office pages](https://digital-strategy.ec.europa.eu/en/policies/ai-office). Delegated acts, implementing acts, and guidance the tracker follows.
- **NIST AI Risk Management Framework 1.0** — [NIST AI RMF 1.0](https://www.nist.gov/itl/ai-risk-management-framework), plus the [Generative AI Profile overlay (NIST AI 600-1)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf). Cited in chapters 2 (row 5), 6 (category 3), and by the row-5 hand-off with `head-of-ai-governance-learning`.
- **ISO/IEC 42001** — [ISO/IEC 42001 AI management system standard](https://www.iso.org/standard/81230.html). Enterprise-procurement-adjacent standard; cited in chapter 6 category 3.
- **NIST Model Cards / Datasheets** — Mitchell et al., [Model Cards for Model Reporting](https://arxiv.org/abs/1810.03677); Gebru et al., [Datasheets for Datasets](https://arxiv.org/abs/1803.09010). Cited in mod-501 and referenced by row 5's org-scope documentation contract.
- **US Executive-branch AI guidance** — track the current OMB memoranda on federal AI use and procurement via the [OMB memoranda index](https://www.whitehouse.gov/omb/information-and-regulatory-affairs/) and the [NIST AI portal](https://www.nist.gov/artificial-intelligence). Referenced in chapter 6 category 3.
- **Sector regulators.** For US fintech: [CFPB](https://www.consumerfinance.gov/) and [OCC](https://www.occ.gov/) AI-adjacent guidance. For US healthcare: [HHS OCR AI health equity](https://www.hhs.gov/civil-rights/for-providers/laws-regulations-guidance/index.html) and the ONC HTI rules. For state-level enactments: [New York City Local Law 144](https://www.nyc.gov/site/dca/about/automated-employment-decision-tools.page) is the modal reference cited by many multi-jurisdiction employers. `head-of-ai-governance-learning` owns depth; this module cites.

## Staff-plus IC ladder and principal-scope leadership craft — Larson et al.

- Will Larson, *[Staff Engineer: Leadership beyond the management track](https://staffeng.com/book)* (Stripe Press, 2021) — the canonical staff-plus IC ladder text. Larson's Fellow / Distinguished IC archetype is the closest shared vocabulary for the audience-shape and coalition-shape work in chapter 7 and mod-504.
- [StaffEng.com Distinguished / Fellow interviews](https://staffeng.com/stories/) — real IC-principal engineer stories that illustrate the working-artifact discipline chapter 7 walks through. The hand-off contract shape in mod-501 chapter 6 draws from this same source.
- Will Larson, ["An Elegant Puzzle: Systems of Engineering Management"](https://press.stripe.com/an-elegant-puzzle) (Stripe Press, 2019). Reference for the executive-audience artifact craft (chapter 7's one-pager) and for the coalition-sequencing craft (mod-504).

## An honest note on cadence

The 2026-Q2 sample was captured 2026-04-08 → 2026-07-08. The next research cycle (~2026-10-08 per `../../JOB_REQUIREMENTS.md`) will re-validate whether the frequencies here still hold and whether new principal-scope posting patterns have emerged (foundation-model program frequency; industry-influence frequency; the Distinguished-title spread beyond Capital One). If any of the four ≥0.60 themes drops materially, the module's chapter emphases will re-scope on the same cadence.
