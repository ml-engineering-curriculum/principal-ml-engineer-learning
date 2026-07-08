# Resources for mod-501-principal-ml-role-scope

Curated references for the chapters, exercises, and self-assessment work in this module. Every entry below is a primary source or a canonical secondary source; nothing here is invented. When a chapter references an artifact ("StaffEng.com Distinguished interviews", "*Designing Machine Learning Systems*"), this file is the pointer.

## The evidence catalogue for this module

The 26 principal / distinguished ML engineer postings this module draws on:

- [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) — the requirements catalogue with cited references, requirement-to-coverage map, and the verb-and-object shift table (level 30 → 40 → 48). Every posting quoted in chapters 1–5 is sourced here.
- [`../../.aicg/job-requirements.json`](../../.aicg/job-requirements.json) — machine-readable posting evidence with per-posting URL, requirement citations, and confidence classification.
- [`../../.aicg/curriculum-plan.json`](../../.aicg/curriculum-plan.json) — the module and project plan the track is scoped against.

## Staff-plus IC ladder and the Principal / Distinguished / Fellow archetype

- Will Larson, *[Staff Engineer: Leadership beyond the management track](https://staffeng.com/book)* (Stripe Press, 2021) — the canonical staff-plus IC ladder text. Larson's Fellow / Distinguished IC archetype is the closest shared vocabulary for what this track lifts you to. The book still applies at level 48; chapter 4 of this module cites its trajectory framing.
- [StaffEng.com Distinguished / Fellow interviews](https://staffeng.com/stories/) — real IC-principal engineer stories from Slack, Stripe, Google, Netflix, Fastly, and others. Chapter 3's title map cross-references this shape of role; chapter 6's hand-off contract shape draws from it.
- [Engineering Ladders framework](https://www.engineeringladders.com/) — a public engineering-ladder reference the market often anchors internal ladders against. Useful for pattern-matching cross-employer, but note it does not model the Distinguished stack cleanly.
- [progression.fyi](https://www.progression.fyi/) — collected engineering-career frameworks. Employer patterns for principal-level rungs vary; this repository catalogues many of them.

## Applied-ML architecture at industry altitude

Grounding for chapter 1's verb-object table (row `lead` at the L48 object `north-star platform architecture`), for chapter 6's architecture hand-off contract, and for mod-503 downstream.

- Chip Huyen, *Designing Machine Learning Systems* (O'Reilly, 2022) — canonical text for applied-ML system architecture at the altitude this module presumes.
- Google, [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml) — the applied-ML engineering discipline reference. Grounding for the review bar mod-505 sets and the north-star architecture mod-503 authors.
- Meta engineering blog, [Applied Machine Learning at Facebook — A Datacenter Infrastructure Perspective](https://engineering.fb.com/2018/05/09/core-infra/applied-machine-learning-at-facebook-a-datacenter-infrastructure-perspective/). Older, but structurally the shape of a north-star applied-ML architecture piece.
- Airbnb engineering blog: the [machine-learning tagged series](https://medium.com/airbnb-engineering/tagged/machine-learning) — Bighead, Zipline, and successor architectures. Case-study material for what a north-star architecture looks like when it has been maintained for years.
- Uber engineering blog: [Michelangelo](https://www.uber.com/blog/michelangelo-machine-learning-platform/) and successor platform posts.
- Pinterest engineering blog: [Content-recommendation and ads-quality series](https://medium.com/pinterest-engineering). Pinterest's Principal ML Engineer, Content Recommendations posting explicitly references *"unified technical architecture and defining a roadmap for industry-leading methodology"* — the Pinterest blog is the primary source for what that architecture already looks like there.

## Cross-org influence and coalition-building at IC-principal altitude

Grounding for chapter 5 theme 3 and for mod-504.

- Will Larson, *Staff Engineer* — chapters on influence, staff-plus writing, and coalition-building. Cited above; the same book is the primary reference here.
- The [Netflix Tech Blog](https://netflixtechblog.com/), the [Stripe Engineering blog](https://stripe.com/blog/engineering), the [Airbnb Engineering blog series on migration and paved roads](https://medium.com/airbnb-engineering) — public case studies of paved-road adoption and cross-org sequencing. Chapter 6's hand-off contract draws on the same pattern.

## Foundation-model programs and long-term technical bets

Cited in chapter 6's foundation-model hand-off contract row and in mod-502's bet-portfolio work. Implementation lives at `training-pipeline-engineer-learning` and `staff-ml-engineer-learning` mod-403 / mod-404; this track uses these papers and reports as principal-side worked examples, not implementation curricula.

- Hoffmann et al., [*Training Compute-Optimal Large Language Models*](https://arxiv.org/abs/2203.15556) (Chinchilla, 2022) — the compute-optimal framing.
- Meta AI, [*The Llama 3 Herd of Models*](https://ai.meta.com/research/publications/the-llama-3-herd-of-models/) technical report — foundation-model program economics at frontier scale.
- DeepSeek AI, [*DeepSeek-V3 Technical Report*](https://arxiv.org/abs/2412.19437) — capacity-vs-quality tradeoff at frontier scale, useful for the bet-portfolio framing in mod-502.
- NVIDIA, [Megatron-LM](https://github.com/NVIDIA/Megatron-LM). Microsoft, [DeepSpeed / ZeRO](https://www.deepspeed.ai/). PyTorch, [FSDP2 documentation](https://pytorch.org/docs/stable/fsdp.html). Parallelism-recipe primary sources. Implementation curriculum lives at `training-pipeline-engineer-learning` and `ai-infra-performance-learning`.

## Responsible AI at org scope

Cited in chapter 6's responsible-AI hand-off contract row and in mod-502's bet-portfolio framing. Depth lives at `staff-ml-engineer-learning` mod-409 and at the governance tracks; this track uses the frameworks as principal-side vocabulary.

- NIST, [AI Risk Management Framework 1.0](https://www.nist.gov/itl/ai-risk-management-framework), plus the [Generative AI Profile overlay](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf).
- European Union, [AI Act (Regulation 2024/1689)](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:L_202401689) — official journal text.
- Mitchell et al., [Model Cards for Model Reporting](https://arxiv.org/abs/1810.03677).
- Gebru et al., [Datasheets for Datasets](https://arxiv.org/abs/1803.09010).

## Peer executive-branch tracks (Family 2)

Referenced in chapter 4's three-family classification and chapter 6's escalation-path shape.

- [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning) — peer executive path (CAIO, direct reports, P&L, board reporting).
- [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) — peer executive-branch path centred on AI governance.

## Peer research-principal path (Family 3) — no owner in this ecosystem yet

Referenced in chapter 4. Public postings from the AI labs are the primary source for what a Family-3 posting looks like.

- Anthropic careers page ([Principal Research Scientist / Distinguished Applied Scientist rungs surface periodically](https://www.anthropic.com/careers))
- OpenAI careers page ([research and research-engineer principal rungs](https://openai.com/careers/search))
- Google DeepMind careers page ([research-scientist principal rungs](https://deepmind.google/about/careers/))
- Meta AI research careers page ([research-scientist principal rungs](https://www.metacareers.com/jobs/))

## Peer platform-side principal tracks (adjacent — same altitude, different scope)

- [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) — level-50 platform-side principal path. The mod-505 (long-term technical bets) shape in that track is the closest structural parallel to mod-502 in this track.
- [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) — level-50 platform-architecture principal path.

## Prerequisite staff-plus IC coverage this module presumes

Chapter 6's hand-off contracts point back to these. If any dimension in chapter 6 is unfamiliar, read the corresponding module in `staff-ml-engineer-learning` first.

- [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) — level-40 curriculum. Multi-team ML architecture (mod-401 / mod-402), foundation-model programs (mod-403), distributed-training strategy (mod-404), cross-team eval (mod-405 / mod-406), portfolio TCO (mod-407), portfolio reliability, portfolio-scope responsible AI (mod-409), staff-plus tech leadership (mod-410).

## For industry influence and external voice (mod-506 companion)

- ICML — [industry track / applied-ML track submission guidance](https://icml.cc/).
- NeurIPS — [submission and industry-track pointers](https://neurips.cc/).
- KDD — [submission guide, especially the applied-track](https://kdd.org/).
- O'Reilly AI Conference — [speaker guidance](https://www.oreilly.com/conferences/).
- QCon — [Engineering Culture track](https://qconferences.com/) — case studies of principal-scope engineering-culture change.
- [Papers With Code](https://paperswithcode.com/) newsletter pattern — a productive dissemination cadence for applied-ML thought leadership.

## An honest note on the below-threshold theme

Mod-506 (industry influence and external voice) and its supporting references are held at a smaller module size because the 2026-Q2 in-window evidence is thin (0.15 frequency, 4/26 postings). The role definition names this facet as principal-defining, but the sample does not corroborate at material frequency. The [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) `needs-research` flags re-visit this on the 2026-10-08 re-sample. If the theme rises above the 0.30 material threshold in that cycle, expect this file to grow.
