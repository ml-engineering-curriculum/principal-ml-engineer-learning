# Resources for mod-503-north-star-applied-ml-architecture

Curated references for the chapters and exercises in this module. Every entry is a primary source (a book, a technical report, a regulatory document, a canonical engineering-blog post) or a canonical secondary source (a widely-cited framework or standard). Nothing here is invented; when a chapter says "Chip Huyen names the plane decomposition" or "Rule 15 of the Rules of ML", the pointer is here.

## The three-literature canon (chapter 2)

The three bodies of work the reference architecture's shape is grounded in.

### Applied-ML system design vocabulary

- Chip Huyen, *[Designing Machine Learning Systems](https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/)* (O'Reilly, 2022) — the canonical vocabulary for the shape a north-star architecture names. Chapters 1–3 fix the definition and the lifecycle; 4–8 walk the offline planes; 9–11 walk the online planes. Chapter 10 (Infrastructure and Tooling for MLOps) is the closest direct match to chapter 3's plane decomposition in this module.
- Chip Huyen's [`chiphuyen/machine-learning-systems-design`](https://github.com/chiphuyen/machine-learning-systems-design) — a companion booklet with the interview-oriented framing; the plane decomposition is the same.

### Discipline / applied-ML engineering rules

- Martin Zinkevich (Google), *[Rules of Machine Learning: Best Practices for ML Engineering](https://developers.google.com/machine-learning/guides/rules-of-ml)* — the numbered rules that inform the invariants chapter 4 turns into contract-level enforcement. Rules 15 (every launch cites an eval report), 29 (training / serving skew), 32 (reuse feature extraction), 44+ (engineering-for-humans) are the load-bearing citations for this module.
- [Google's ML Test Score paper — *What's your ML Test Score? A rubric for ML production readiness and technical debt reduction*](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/45742.pdf) (Breck et al., 2017) — the discipline that becomes the eval-harness contract's *bar for launch* (chapter 3 plane 5).
- Sculley et al., *[Hidden Technical Debt in Machine Learning Systems](https://papers.nips.cc/paper/2015/hash/86df7dcfd896fcaf2674f757a2463eba-Abstract.html)* (NeurIPS, 2015) — the canonical statement of why the shape and the contracts matter at all.

### Case-study literature — engineering-blog reference architectures

- Meta / Facebook Engineering, *[Applied Machine Learning at Facebook — A Datacenter Infrastructure Perspective](https://engineering.fb.com/2018/05/09/core-infra/applied-machine-learning-at-facebook-a-datacenter-infrastructure-perspective/)* (Hazelwood et al., 2018). Older but structurally still the load-bearing plane decomposition at datacenter scale.
- Uber Engineering, *[Meet Michelangelo: Uber's Machine Learning Platform](https://www.uber.com/blog/michelangelo-machine-learning-platform/)* — the canonical case study of a paved-road MLOps substrate and a feature-store / model-store / training-template contract set. Chapter 4's canonical API framing owes the most to this.
- Uber Engineering, *[Continuous Integration and Deployment for Machine Learning Online Serving and Models](https://www.uber.com/blog/continuous-integration-testing-machine-learning-models/)* and *[Scaling Michelangelo](https://www.uber.com/blog/scaling-michelangelo/)* — the evolution posts that show how the platform contract survived multiple substrate re-platforms (chapter 6 § substrate bets).
- Airbnb Engineering, *[Bighead: Airbnb's End-to-End Machine Learning Platform](https://medium.com/airbnb-engineering/bighead-airbnbs-end-to-end-machine-learning-platform-a1c2b3e4d0e0)* and *[Zipline: Airbnb's Machine Learning Data Management Platform](https://medium.com/airbnb-engineering/zipline-airbnbs-machine-learning-data-management-platform-d0dc06e7a3c0)* — case studies for how a reference architecture *evolves* through multiple named bets. Chapter 6 § *evolution plan discipline* mirrors what these posts document over multiple years.
- Airbnb Engineering's [machine-learning tagged series](https://medium.com/airbnb-engineering/tagged/machine-learning) — the broader series where the evolution is visible.
- Netflix Tech Blog, *[Metaflow](https://netflixtechblog.com/tagged/metaflow)*, *[Personalization](https://netflixtechblog.com/tagged/personalization)*, and *[Experimentation](https://netflixtechblog.com/tagged/experimentation)* series — reference for developer-experience shape a canonical API surface has to hit, and for how the eval / experimentation program becomes an org-wide contract.
- LinkedIn Engineering, *[Open Sourcing Feathr — LinkedIn's Feature Store for Productive Machine Learning](https://engineering.linkedin.com/blog/2022/open-sourcing-feathr---linkedin-s-feature-store-for-productive-machine-)* — reference for a canonical feature-store contract, and for how an org publishes a feature contract externally.
- Pinterest Engineering blog — [content-recommendation and ads-quality series on Medium](https://medium.com/pinterest-engineering). Pinterest's Principal ML Engineer, Content Recommendations posting explicitly references *"unified technical architecture and defining a roadmap for industry-leading methodology"*; this blog is the primary source for what the unified architecture looks like in practice there.
- DoorDash Engineering, *[Building Riviera: A Declarative Real-Time Feature Engineering Framework](https://careers.doordash.com/blog/building-riviera-a-declarative-real-time-feature-engineering-framework/)* — recent (post-Michelangelo era) case study for feature-plane contract shape at a delivery-marketplace org.
- Instacart, *[Griffin: Instacart's Machine Learning Platform](https://tech.instacart.com/griffin-how-instacart-serves-100-millions-of-ml-predictions-a-day-15b6bcfcc865)* — a smaller-scale case study; useful for the "org-scope architecture at pre-frontier scale" framing.

## Contract-tooling and diagram-as-code (chapters 4–5)

Practical stacks for the four canonical APIs (exercise-02) and for the living diagrams (chapter 5, exercise-01).

### Contract / schema languages

- [OpenAPI Specification](https://spec.openapis.org/oas/latest.html) (3.1+) — the modal API schema for REST contracts. Chapter 4's example sketches are in an OpenAPI-adjacent shape.
- [Protocol Buffers](https://protobuf.dev/) — for higher-performance and IDL-first orgs.
- [GraphQL SDL](https://graphql.org/learn/schema/) — for federated / stitched contract surfaces.
- [Buf](https://buf.build/) — protobuf tooling (`buf lint`, `buf breaking`) that enforces additive-by-default evolution.
- [Spectral](https://stoplight.io/open-source/spectral) — OpenAPI linter for contract-level style and evolution rules.

### Diagram-as-code

- [C4 model](https://c4model.com/) (Simon Brown) — the modal system-architecture notation for 2026. Chapter 5 § *notation coherence with the industry* is the reference.
- [Structurizr](https://structurizr.com/) — C4-native tool with DSL and multiple render targets.
- [PlantUML](https://plantuml.com/) — text-based UML and C4 diagrams.
- [Mermaid](https://mermaid.js.org/) — text-based diagrams with strong GitHub / GitLab / MkDocs support.
- [D2](https://d2lang.com/) — modern text-based diagramming with clean syntax.
- [Graphviz](https://graphviz.org/) — the venerable `.dot` toolchain, still the best for large auto-laid-out graphs.

### Docs-site generators (canonical location publication)

- [Docusaurus](https://docusaurus.io/) — React-based, strong versioning support.
- [MkDocs](https://www.mkdocs.org/) with [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) — Python-based; simple to run in CI.
- [mdBook](https://rust-lang.github.io/mdBook/) — Rust-based, single-binary; good for internal book-shaped docs.
- [Backstage TechDocs](https://backstage.io/docs/features/techdocs/techdocs-overview) — integrates with the Backstage software catalog and is the modal internal-developer-portal target.

### Feature-store and registry substrates (chapter 3 planes 2 and 4)

- [Feast](https://feast.dev/) — open-source feature-store; useful for reference against LinkedIn's Feathr and Uber's Palette.
- [Tecton](https://www.tecton.ai/) — commercial feature-store; useful as a market pointer.
- [MLflow Model Registry](https://mlflow.org/docs/latest/model-registry.html) — the modal tool the chapter 4 registry contract sits above. *Tool, not contract* — chapter 4 § *the "tool is the contract" trap*.
- [Kubeflow](https://www.kubeflow.org/) — training-plane substrate reference.
- [Ray](https://www.ray.io/) — distributed-training substrate reference.
- [KServe](https://kserve.github.io/website/) — serving-plane substrate reference.

## Governance and responsible AI (chapters 3, 6, 8)

The policy frameworks that land as obligations on the reference architecture.

### Global regulatory frameworks

- European Union, *[AI Act (Regulation 2024/1689)](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:L_202401689)* — official journal text. High-risk-system tier, GPAI obligations, and post-market monitoring are all mapped to registry / eval / gateway obligations in chapter 6 §4 and chapter 8 § *contract 1*.
- NIST, *[AI Risk Management Framework 1.0](https://www.nist.gov/itl/ai-risk-management-framework)*, plus the *[Generative AI Profile overlay (NIST AI 600-1)](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf)*.
- ISO/IEC 42001:2023 — *Information technology — Artificial intelligence — Management system*. [ISO standard page](https://www.iso.org/standard/81230.html).
- OECD, *[AI Principles](https://oecd.ai/en/ai-principles)* — the international-baseline framing many other frameworks reference.

### Documentation frameworks

- Mitchell et al., *[Model Cards for Model Reporting](https://arxiv.org/abs/1810.03677)* (2018). Cited in chapter 3 § plane 4, chapter 4 § registry contract, chapter 7 § *examples of legitimate nudges*, and chapter 8 § *contract 3*.
- Gebru et al., *[Datasheets for Datasets](https://arxiv.org/abs/1803.09010)* (2018). Cited in chapter 3 § *governance / responsible AI* and chapter 8 § *contract 3*.
- Google, *[Data Cards Playbook](https://sites.research.google/datacardsplaybook/)* — the productized descendant of datasheets.

### Sectoral and regional rules (cited in exercise-05's policy-to-contract mapping)

- USA — [OMB M-24-10, *Advancing Governance, Innovation, and Risk Management for Agency Use of Artificial Intelligence*](https://www.whitehouse.gov/wp-content/uploads/2024/03/M-24-10-Advancing-Governance-Innovation-and-Risk-Management-for-Agency-Use-of-Artificial-Intelligence.pdf).
- USA — Consumer Financial Protection Bureau, [*Circular 2023-03 on Adverse Action Notices and AI*](https://www.consumerfinance.gov/compliance/circulars/circular-2023-03-adverse-action-notification-requirements-and-the-proper-use-of-the-cfpbs-sample-forms-provided-in-regulation-b/).
- USA / NYC — [Local Law 144 on Automated Employment Decision Tools](https://www.nyc.gov/site/dca/about/automated-employment-decision-tools.page).
- USA — Office of the Comptroller of the Currency, [*SR 11-7 / OCC Model Risk Management guidance*](https://www.federalreserve.gov/supervisionreg/srletters/sr1107.htm).

## Peer platform-side principal tracks (chapter 8)

Adjacent tracks the reference architecture holds seams with.

- [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) — Principal AI-Infrastructure Engineer. Owns the substrate the ML architecture stands on. Chapter 8 § *seam A–D* cite this track.
- [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) — Principal AI-Infrastructure Architect. Owns the platform-side reference architecture; co-authors the canonical types and SLO taxonomy above both artifacts. Chapter 8 § *co-authored interfaces*.
- [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning) — the platform-team practitioner track that *builds* the substrates (feature store, registry, serving gateway) the ML architecture cites. Chapter 3 hand-offs point here.
- [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning) — depth on inference latency and cost-per-inference; cited in chapter 3 plane 6 hand-offs and chapter 4 gateway SLOs.

## Peer executive branch (chapter 8 §2)

- [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) — the governance track that authors the policies the ML architecture converts into contract-level obligations.
- [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning) — the CAIO / VP-of-ML track that owns strategic direction, P&L, and board-facing framing. Cited when escalations rise above both peer seams (chapter 8 §3).

## Staff-scope multi-team blueprint owner (chapter 2, chapter 7)

- [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) — the level-40 track that owns the multi-team blueprint. Chapter 2 § *two altitudes* and chapter 7 § *the "defer to the multi-team blueprint owner" case, walked* are the reference. Modules mod-401 / mod-402 (multi-team blueprint), mod-405 / mod-406 (cross-team eval), and mod-410 (staff-plus tech leadership) are the most-cited hand-offs.

## Prior sibling modules in this track

- [`../mod-501-principal-ml-role-scope/`](../mod-501-principal-ml-role-scope/) — the verb-and-object vocabulary and the hand-off contracts back to staff scope. Chapter 1's *paired-artifact frame* presumes fluency with mod-501.
- [`../mod-502-org-and-industry-ml-strategy/`](../mod-502-org-and-industry-ml-strategy/) — the *paired* strategy artifact this architecture cites and is cited by. Every chapter here refers back to mod-502's bet portfolio.

## Downstream sibling modules

- [`../mod-504-cross-org-influence-without-authority/`](../mod-504-cross-org-influence-without-authority/) — the practice of holding the seams named in chapter 8.
- [`../mod-505-principal-mentorship-and-technical-bar/`](../mod-505-principal-mentorship-and-technical-bar/) — the review-bar side of chapter 7's *block* and *nudge* modes.
- [`../mod-506-industry-influence-and-external-voice/`](../mod-506-industry-influence-and-external-voice/) — dissemination cadence for the reference architecture's shape when published externally.

## Track-level companion material

- [`../../CURRICULUM.md`](../../CURRICULUM.md) — the six-module arc and the three capstones.
- [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) — the 26-posting evidence catalogue the Capital One and Pinterest target framings quoted throughout are sourced from.
- [`../../PREREQUISITES.md`](../../PREREQUISITES.md) — the assumed staff-plus IC foundation. If the multi-team blueprint work at staff scope is unfamiliar, mod-401 / mod-402 in the staff track are the pre-reads.
