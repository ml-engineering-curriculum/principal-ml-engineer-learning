# Resources for mod-506-industry-influence-and-external-voice

Curated primary references for the chapters and exercises in this module. Every entry below is a primary source (the venue's own CFP page, the publisher's own documentation, the standards body's own page, the engineering blog itself) or a canonical secondary source. Nothing here is invented; when a chapter cites *"the Meta Engineering blog"*, *"the KDD industry track"*, *"the Apache 2.0 licence"*, or *"the Contributor Covenant"*, the primary pointer is below.

## The evidence catalogue for this module

- [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) — the 26-posting evidence catalogue. The Capital One Sr. Distinguished AI Engineer *"ML industry impact through conference presentations, papers, blog posts, or open source contributions"* clause and the Ibotta Principal ML Engineer *"act as a leading contributor, voice, and thought leader in a growing community of machine learning practitioners"* clause are both sourced here.
- [`../../.aicg/job-requirements.json`](../../.aicg/job-requirements.json) — machine-readable posting evidence with per-posting URL and requirement citations.
- [`../../.aicg/curriculum-plan.json`](../../.aicg/curriculum-plan.json) — the module and project plan the track is scoped against. The `req-industry-influence` requirement entry carries the below-threshold-but-principal-defining classification that justifies this module's 10-hour size.

## Prior sibling modules — the substrate chapters 1–6 lift from

The practice this module walks is parasitic on the artifacts and vocabulary the prior modules produce. If any of these is unfamiliar, chapter 1's venue-selection discipline will not land and chapter 2's internal-first substrate will have nothing to point at.

- [`../mod-501-principal-ml-role-scope/`](../mod-501-principal-ml-role-scope/) — the four principal-scope themes (chapter 5) plus the *fifth, principal-defining, below-threshold* theme this module owns. The verb-and-object vocabulary (chapter 1) is the substrate the venue-audience-artifact matching discipline (chapter 1 of this module) builds on.
- [`../mod-502-org-and-industry-ml-strategy/`](../mod-502-org-and-industry-ml-strategy/) — the bet-framing substrate chapter 3 (paper / blog) extracts *org-wide bet framing* lessons from. Chapter 6 § *sunset criteria* is the parent retirement-criteria discipline. Chapter 7's paired-artifact frame is what mod-504 chapter 5 lifts and this module's chapter 4 reuses for the keynote craft.
- [`../mod-503-north-star-applied-ml-architecture/`](../mod-503-north-star-applied-ml-architecture/) — the canonical reference architecture chapter 3 (paper / blog) extracts *architecture at portfolio-and-industry altitude* lessons from, chapter 4 (keynote) uses as the source of the take-away diagram, and chapter 5 (open source) aligns the release against. Chapter 4 § *the canonical API contract surface* is the surface shape A (paved-road interface) releases are extracted from.
- [`../mod-504-cross-org-influence-without-authority/`](../mod-504-cross-org-influence-without-authority/) — the SVP / CTO-audience narrative craft (chapter 5) that chapter 4 of this module *lifts* to industry audience. The coalition-sequencing discipline (chapter 4 there) becomes the hallway-track discipline in chapter 4 here.
- [`../mod-505-principal-mentorship-and-technical-bar/`](../mod-505-principal-mentorship-and-technical-bar/) — the internal-community rituals (chapter 5) that this module's chapter 2 lifts to authored-artifact altitude. The keynote-only drift failure mode (chapter 6) that chapters 1, 2, and 6 of this module recurrently guard against. The personal-cadence artifact (chapter 6) whose portfolio-check section carries this module's tracking dashboard.

## Peer tracks — commit-level open-source maintainership

Chapter 5 explicitly cedes the day-to-day open-source commit craft to the peer specialist tracks. The maintainership contract (chapter 5 § *the maintainership contract with the peer specialist tracks*) is the seam.

- [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) — the L30 senior-IC track that often supplies the maintainer bench.
- [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning), [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning), [`rag-engineer-learning`](https://github.com/ml-engineering-curriculum/rag-engineer-learning), [`agentic-systems-architect-learning`](https://github.com/ml-engineering-curriculum/agentic-systems-architect-learning) — specialist tracks whose maintainers staff the bench for domain-specific releases.
- [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning), [`ai-infra-performance-learning`](https://github.com/ai-infra-curriculum/ai-infra-performance-learning), [`ai-infra-security-learning`](https://github.com/ai-infra-curriculum/ai-infra-security-learning) — infrastructure-side peer tracks whose maintainers staff the bench for platform-adjacent releases.
- [`ai-research-scientist-learning`](https://github.com/ml-engineering-curriculum/ai-research-scientist-learning) — the peer research-principal track that owns the academic peer-reviewed publication discipline chapter 3 explicitly cedes to.
- [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning), [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) — executive-branch peer tracks whose seats hold the ratification signatures chapter 5 § *decision 2* and § *decision 3* require.

## Industry-track venues — chapter 1 and chapter 3 canon

Chapter 1 enumerates the canonical industry-track and workshop venues; chapter 3 specifies the paper's shape against those venues' expectations. The primary sources are each venue's own CFP and programme pages.

### Core applied-ML industry tracks

- **KDD** (ACM SIGKDD Conference on Knowledge Discovery and Data Mining). The *Applied Data Science Track* is the industry venue. Programme pages at [`kdd.org`](https://kdd.org/). The track's charter prioritises deployed-system papers over methodological novelty.
- **RecSys** (ACM Conference on Recommender Systems). *Industry Session* and the applied-track submissions. Primary source: [`recsys.acm.org`](https://recsys.acm.org/). The industry sessions reliably publish applied-ML principal-scope lessons.
- **WSDM** (ACM International Conference on Web Search and Data Mining). *Industry Day*. Primary source: [`www.wsdm-conference.org`](https://www.wsdm-conference.org/).
- **SIGIR** (ACM SIGIR Conference on Research and Development in Information Retrieval). *Industry Track*. Primary source: [`sigir.org`](https://sigir.org/).
- **WWW / The Web Conference** (ACM Web Conference). *Industry Track*. Primary source: [`www2026.thewebconf.org`](https://www2026.thewebconf.org/) (annual URL changes with the hosting year; the stable landing is [`www.iw3c2.org`](https://www.iw3c2.org/)).
- **CIKM** (ACM International Conference on Information and Knowledge Management). *Applied Research Track*. Primary source: [`cikm.org`](https://cikm.org/) (annual URL shifts).
- **MLSys** (Conference on Machine Learning and Systems). The applied-ML-and-systems-crossover venue; industry-adjacent track strong on deployed systems. Primary source: [`mlsys.org`](https://mlsys.org/).
- **NeurIPS / ICML workshops** — the ML-for-Systems, ML-in-the-Physical-World, Deployable-ML, and related industry-adjacent workshops at NeurIPS ([`neurips.cc`](https://neurips.cc/)) and ICML ([`icml.cc`](https://icml.cc/)). Industry-track submissions typically route through these workshops rather than the main-track CFP.

### Industry-adjacent engineering and MLOps conferences

- **O'Reilly AI Conference / AI Superstream** — the practitioner-oriented plenary venue chapter 4 § *the venue map* names as a canonical plenary setting. Primary source: [`www.oreilly.com/online-learning/ai-superstream.html`](https://www.oreilly.com/) (O'Reilly periodically rebrands the series). <!-- needs-research: O'Reilly's AI conference branding has shifted across years (OSCON AI, AI Conference, AI Superstream); confirm current canonical series name and URL. -->
- **QCon** (InfoQ). *AI/ML Track*. Primary source: [`qconferences.com`](https://qconferences.com/) and [`www.infoq.com`](https://www.infoq.com/). QCon's track structure gives applied-ML principal-scope talks a well-defined 40-minute slot.
- **Strata Data & AI Conference** (O'Reilly). Primary source: [`www.oreilly.com`](https://www.oreilly.com/) — note that Strata's live-conference branding has shifted across years. <!-- needs-research: confirm whether Strata is currently running as a standalone event, a Superstream, or has been folded into another O'Reilly series. -->
- **MLOps World** — the ML-operations-focused conference venue chapter 4 § *the venue map* names as a canonical FM-economics-adjacent audience. Primary source: [`mlopsworld.com`](https://mlopsworld.com/).
- **Ray Summit** — the Anyscale-hosted applied-ML plenary venue. Primary source: [`raysummit.anyscale.com`](https://www.anyscale.com/ray-summit) (Anyscale rotates the URL annually).
- **KubeCon + CloudNativeCon** — the CNCF conference where the *AI Day* and *ML Day* co-located events live. Primary source: [`www.cncf.io/kubecon-cloudnativecon-events/`](https://www.cncf.io/kubecon-cloudnativecon-events/).
- **PyData / SciPy** — the Python-ecosystem conferences where applied-ML plenary-adjacent talks live. Primary sources: [`pydata.org`](https://pydata.org/) and [`conference.scipy.org`](https://conference.scipy.org/).
- **LeadDev / LeadDev StaffPlus** — the practitioner-conference series for staff-plus engineers. Primary source: [`leaddev.com`](https://leaddev.com/) and the StaffPlus series at [`leaddev.com/staffplus-new-york`](https://leaddev.com/staffplus-new-york). Chapter 4 § *the venue map* cites this as the staff-plus-adjacent venue option.

### Company-hosted principal-scope conferences

Chapter 4 § *the venue map* notes that internally-hosted but externally-attended company conferences fit the industry-track-talk shape when the hosting company's user base skews staff-plus.

- **Meta @Scale** — Meta's engineering conference series. Primary source: [`atscaleconference.com`](https://atscaleconference.com/).
- **AWS re:Invent** — Amazon Web Services' annual conference, with substantial ML deep-dive sessions. Primary source: [`reinvent.awsevents.com`](https://reinvent.awsevents.com/).
- **Google Cloud Next** and **Google I/O** — Google's cloud and developer conferences with ML tracks. Primary sources: [`cloud.withgoogle.com/next`](https://cloud.withgoogle.com/next/) and [`io.google`](https://io.google/).
- **Microsoft Build** and **Ignite** — Microsoft's developer and IT-professional conferences with AI tracks. Primary sources: [`build.microsoft.com`](https://build.microsoft.com/) and [`ignite.microsoft.com`](https://ignite.microsoft.com/).

## Applied-ML engineering blog canon — chapter 2 § Class B and chapter 3 canon

The applied-ML engineering blog series pattern that chapter 1, chapter 2, and chapter 3 all cite. These are the primary engineering-blog surfaces where principal-scope applied-ML artifacts land.

### The canonical applied-ML engineering blog series

- **Meta Engineering** — [`engineering.fb.com`](https://engineering.fb.com/). The applied-ML, infrastructure, and systems series. Chapter 3 § *shape of the applied-ML engineering blog post* cites the Meta Engineering editorial standard as part of the modal shape.
- **Airbnb Tech Blog** — [`medium.com/airbnb-engineering`](https://medium.com/airbnb-engineering) (official blog hosted on Medium). The applied-ML and data-platform series.
- **Uber Engineering** — [`www.uber.com/en/blog/engineering/`](https://www.uber.com/blog/engineering/). The applied-ML, data-platform, and ML infrastructure series. Uber's Michelangelo ML platform blog series is a canonical chapter 3 § *architecture at portfolio-and-industry altitude* reference.
- **Pinterest Engineering** — [`medium.com/pinterest-engineering`](https://medium.com/pinterest-engineering). The recommender-system and applied-ML series.
- **LinkedIn Engineering** — [`www.linkedin.com/blog/engineering`](https://www.linkedin.com/blog/engineering). The applied-ML, recommender-system, and infrastructure series.
- **Netflix TechBlog** — [`netflixtechblog.com`](https://netflixtechblog.com/). The applied-ML, infrastructure, and personalisation series. The Netflix recommendation-system blog series is a canonical chapter 3 § *cross-team eval program discipline* and § *architecture at portfolio-and-industry altitude* reference.
- **DoorDash Engineering** — [`doordash.engineering/blog/`](https://doordash.engineering/blog/).
- **Instacart Tech** — [`tech.instacart.com`](https://tech.instacart.com/).
- **Stripe Blog** — [`stripe.com/blog/engineering`](https://stripe.com/blog) (ML content lives in the broader engineering category).
- **Shopify Engineering** — [`shopify.engineering`](https://shopify.engineering/).
- **Spotify Engineering** — [`engineering.atspotify.com`](https://engineering.atspotify.com/).
- **Twitter / X Engineering** — [`blog.twitter.com/engineering/en_us`](https://blog.x.com/engineering/en_us) (URL has shifted under rebranding; the stable landing is at [`blog.x.com`](https://blog.x.com/)). <!-- needs-research: X's engineering-blog URL and publication cadence have been inconsistent post-rebranding; confirm the current canonical publication path. -->

### Independent applied-ML newsletters and syndication surfaces

- **Papers with Code** — [`paperswithcode.com`](https://paperswithcode.com/). The applied-ML newsletter and code-paired-paper surface chapter 1 § *venue class 2 — blog post* names as the independent-publication canonical.
- **The Sequence** — [`thesequence.substack.com`](https://thesequence.substack.com/). The industry-focused AI/ML newsletter.
- **Import AI** by Jack Clark — [`jack-clark.net`](https://jack-clark.net/). The weekly AI-industry roundup newsletter cited across the applied-ML practitioner community.
- **The Batch** (DeepLearning.AI) — [`www.deeplearning.ai/the-batch/`](https://www.deeplearning.ai/the-batch/).
- **The Gradient** — [`thegradient.pub`](https://thegradient.pub/). Long-form applied-ML and research commentary.
- **Chip Huyen's blog** — [`huyenchip.com`](https://huyenchip.com/). Principal-scope applied-ML practitioner writing, canonical secondary source for ML-systems-design patterns.
- **Eugene Yan's blog** — [`eugeneyan.com`](https://eugeneyan.com/). Applied-ML and ML-systems-design practitioner writing with explicit applied-ML blog editorial standards.

## Open-source governance canon — chapter 5 canon

Chapter 5's release-level decisions depend on the broader open-source governance literature being named. These are the primary standards and documents.

### Open-source licence primary sources

Chapter 5 § *section 9 — the community-governance model* names the licence as a decision requiring a one-sentence justification. The canonical licence texts:

- **Apache License 2.0** — [`www.apache.org/licenses/LICENSE-2.0`](https://www.apache.org/licenses/LICENSE-2.0). The modal choice for corporate-stewarded ML projects (includes a patent grant that MIT does not).
- **MIT License** — [`opensource.org/license/mit`](https://opensource.org/license/mit/). The modal choice for permissive licensing without patent-grant implications.
- **BSD 3-Clause License** — [`opensource.org/license/bsd-3-clause`](https://opensource.org/license/bsd-3-clause/).
- **Mozilla Public License 2.0** — [`www.mozilla.org/en-US/MPL/2.0/`](https://www.mozilla.org/en-US/MPL/2.0/). File-level weak-copyleft choice.
- **GNU LGPL 2.1 and 3.0** — [`www.gnu.org/licenses/lgpl-2.1.html`](https://www.gnu.org/licenses/lgpl-2.1.html) and [`www.gnu.org/licenses/lgpl-3.0.html`](https://www.gnu.org/licenses/lgpl-3.0.html). Weak-copyleft at the library layer.
- **GNU GPL 2.0 and 3.0** — [`www.gnu.org/licenses/gpl-2.0.html`](https://www.gnu.org/licenses/gpl-2.0.html) and [`www.gnu.org/licenses/gpl-3.0.html`](https://www.gnu.org/licenses/gpl-3.0.html). Strong-copyleft; typically unsuitable for corporate ML stewardship because of the downstream-propagation obligations.
- **OSI Open Source Definition** — [`opensource.org/osd`](https://opensource.org/osd/). The 10-point definition that constrains which licences qualify as *open source* for the purposes of chapter 5's governance taxonomy.

### Model-and-weights licensing (shape α territory)

Chapter 5 § *shape α* names model-weights releases as a non-default decision. For orgs that do release model weights, the modal licence surface:

- **OpenRAIL** family of licences — [`www.licenses.ai`](https://www.licenses.ai/) and the Responsible AI Licenses initiative pages. The BigScience OpenRAIL-M licence is the canonical weights-release template cited in the ML-industry foundation-model release cadence.
- **Llama Community License** (Meta's community-model licence family) — [`www.llama.com/license/`](https://www.llama.com/license/) — the canonical community-model licence for Llama family releases. <!-- needs-research: Meta periodically revises the specific Llama community licence (Llama 2 community licence, Llama 3 community licence, etc.); verify the current revision applicable to the specific model generation. -->
- **CreativeML Open RAIL-M** — the Stable Diffusion family licence. Primary source: [`huggingface.co/spaces/CompVis/stable-diffusion-license`](https://huggingface.co/spaces/CompVis/stable-diffusion-license).

### Contribution-process documents

Chapter 5 § *section 9* names the CLA / DCO decision. The canonical templates:

- **Developer Certificate of Origin (DCO)** — [`developercertificate.org`](https://developercertificate.org/). The Linux-kernel-style in-commit sign-off alternative to a CLA.
- **Apache Software Foundation Individual CLA** — [`www.apache.org/licenses/contributor-agreements.html`](https://www.apache.org/licenses/contributor-agreements.html). The canonical CLA template for Apache-licensed projects.
- **Contributor Covenant** — [`www.contributor-covenant.org`](https://www.contributor-covenant.org/). The modal community-code-of-conduct template chapter 5 § *section 9* names.

### Standards bodies for shape-C and shape-D exits

Chapter 5 § *exit B — donation to a standards body* lists the standards bodies the modal exit targets. The primary sources:

- **MLCommons** — [`mlcommons.org`](https://mlcommons.org/). The ML-benchmark standards body; the MLPerf benchmark suite is the canonical shape-C donation target.
- **ONNX** (Open Neural Network Exchange) — [`onnx.ai`](https://onnx.ai/). The neural-network interchange standard; shape-C and shape-D donations route through the ONNX operator-submission process.
- **OpenTelemetry** — [`opentelemetry.io`](https://opentelemetry.io/). The observability-standards body with an ML-metrics extension track; chapter 1 § *venue class 4* names it as an ML-standards-body contribution venue.
- **CNCF (Cloud Native Computing Foundation)** — [`www.cncf.io`](https://www.cncf.io/). The CNCF Sandbox / Incubation / Graduation path is the modal chapter 5 § *exit A — graduation to a foundation* target.
- **Apache Software Foundation Incubator** — [`incubator.apache.org`](https://incubator.apache.org/). The ASF project-graduation path.
- **Linux Foundation projects** — [`www.linuxfoundation.org/projects`](https://www.linuxfoundation.org/projects). The LF project-hosting-and-graduation path; the LF AI & Data sub-foundation ([`lfaidata.foundation`](https://lfaidata.foundation/)) is the ML-specific target.

### Open-source project governance patterns

- **The Apache Way** — [`www.apache.org/theapacheway/index.html`](https://www.apache.org/theapacheway/index.html). The canonical treatment of consensus-based open-source governance.
- **OSS Capacity Planning** by Nadia Eghbal / Asparouhova in *Working in Public: The Making and Maintenance of Open Source Software* (Stripe Press, 2020). The canonical treatment of open-source maintenance economics; chapter 5 § *decision 2 — the maintenance-contract decision* is a specialisation of this book's framing. Book site at [`press.stripe.com/working-in-public`](https://press.stripe.com/working-in-public).
- **Producing Open Source Software** by Karl Fogel. Full text at [`producingoss.com`](https://producingoss.com/). The canonical practical treatment of running open-source projects at scale.
- **GitHub's Open Source Guides** — [`opensource.guide`](https://opensource.guide/). GitHub-hosted practitioner-facing guides on building communities, legal, maintenance, and leadership.

## Reference ML open-source projects — chapter 5 ground truth

Chapter 5 § *decision 2 — the maintenance-contract decision* describes seven commitments. The following projects are the canonical reference implementations of those commitments in production.

- **PyTorch** — [`pytorch.org`](https://pytorch.org/) and the governance documentation at [`github.com/pytorch/pytorch/blob/main/GOVERNANCE.md`](https://github.com/pytorch/pytorch/blob/main/GOVERNANCE.md). The modal large-scale ML framework governance model; now stewarded by the PyTorch Foundation under the Linux Foundation.
- **TensorFlow** — [`www.tensorflow.org`](https://www.tensorflow.org/) and the governance documentation in the [`tensorflow/community`](https://github.com/tensorflow/community) repository. Google-stewarded; the SIG-structure is a canonical shape-D (reference-implementation) governance reference.
- **JAX** — [`jax.readthedocs.io`](https://jax.readthedocs.io/) and the project repository at [`github.com/jax-ml/jax`](https://github.com/jax-ml/jax). Google-stewarded; the JAX governance evolution is a canonical shape-A (paved-road-interface) and shape-D reference.
- **Ray** — [`www.ray.io`](https://www.ray.io/) and the project repository at [`github.com/ray-project/ray`](https://github.com/ray-project/ray). Anyscale-stewarded; the chapter 5 shape-A (paved-road-interface) reference for distributed-compute primitives.
- **MLflow** — [`mlflow.org`](https://mlflow.org/) and the project repository at [`github.com/mlflow/mlflow`](https://github.com/mlflow/mlflow). Databricks-stewarded; now part of the LF AI & Data foundation. The chapter 5 shape-D (reference-implementation-of-invariant) reference for experiment-tracking.
- **Kubeflow** — [`www.kubeflow.org`](https://www.kubeflow.org/). CNCF-stewarded; the canonical ML-on-Kubernetes shape-D reference.
- **TFX (TensorFlow Extended)** — [`www.tensorflow.org/tfx`](https://www.tensorflow.org/tfx). Google-stewarded ML-pipeline framework.
- **Feast** — [`feast.dev`](https://feast.dev/). Linux Foundation-stewarded feature-store framework; shape-A (paved-road-interface) reference.
- **LangChain** — [`www.langchain.com`](https://www.langchain.com/) and the project repository at [`github.com/langchain-ai/langchain`](https://github.com/langchain-ai/langchain). Agentic-and-LLM-orchestration framework; a canonical shape-A (paved-road-interface) reference for the LLM-application layer.
- **Hugging Face Transformers** — [`huggingface.co/docs/transformers`](https://huggingface.co/docs/transformers) and the project repository at [`github.com/huggingface/transformers`](https://github.com/huggingface/transformers). Hugging Face-stewarded; the canonical shape-A reference for the transformer-model-loading-and-inference layer.
- **Weights & Biases Weave** — [`github.com/wandb/weave`](https://github.com/wandb/weave). The Weights & Biases OSS core.
- **Apache Airflow** — [`airflow.apache.org`](https://airflow.apache.org/). ASF-stewarded workflow orchestration; a canonical shape-F (graduated experiment) reference — originally Airbnb-built and now ASF-governed.
- **DBT (data build tool)** — [`www.getdbt.com/product/what-is-dbt/`](https://www.getdbt.com/product/what-is-dbt/) and the project repository at [`github.com/dbt-labs/dbt-core`](https://github.com/dbt-labs/dbt-core).

## Benchmark and eval-standard canon — chapter 5 shape C ground truth

Chapter 5 § *shape C — the benchmark, not the benchmark's private extension* names benchmarks as a canonical release shape. The reference benchmarks:

- **MLPerf** — [`mlcommons.org/en/`](https://mlcommons.org/) (MLCommons-stewarded). The canonical training-and-inference performance benchmark suite.
- **HELM** (Holistic Evaluation of Language Models) — [`crfm.stanford.edu/helm/`](https://crfm.stanford.edu/helm/). Stanford CRFM-stewarded LLM-evaluation framework.
- **MTEB** (Massive Text Embedding Benchmark) — [`huggingface.co/spaces/mteb/leaderboard`](https://huggingface.co/spaces/mteb/leaderboard) and the project repository at [`github.com/embeddings-benchmark/mteb`](https://github.com/embeddings-benchmark/mteb). The canonical embedding-model benchmark.
- **BIG-bench** (Beyond the Imitation Game Benchmark) — [`github.com/google/BIG-bench`](https://github.com/google/BIG-bench). Google-and-community-stewarded LLM-capability benchmark.
- **lm-evaluation-harness** — [`github.com/EleutherAI/lm-evaluation-harness`](https://github.com/EleutherAI/lm-evaluation-harness). EleutherAI-stewarded LLM-evaluation harness; a canonical shape-B (eval harness not eval data) reference.
- **HumanEval and MBPP** — the canonical code-generation benchmarks. Primary source: Chen et al., [*Evaluating Large Language Models Trained on Code*](https://arxiv.org/abs/2107.03374) (OpenAI, 2021) for HumanEval; Austin et al., [*Program Synthesis with Large Language Models*](https://arxiv.org/abs/2108.07732) (Google, 2021) for MBPP.
- **SWE-bench** — [`www.swebench.com`](https://www.swebench.com/) and the project repository at [`github.com/princeton-nlp/SWE-bench`](https://github.com/princeton-nlp/SWE-bench). Princeton-stewarded software-engineering-task benchmark.

## Keynote and executive-audience talk craft — chapter 4 canon

Chapter 4 § *the keynote is an executive-audience artifact* lifts from the mod-504 chapter 5 SVP / CTO-audience narrative craft. The broader keynote-and-talk-craft canon:

- **Chris Anderson, *TED Talks: The Official TED Guide to Public Speaking*** (Houghton Mifflin Harcourt, 2016). The canonical treatment of the plenary-keynote through-line discipline chapter 4 § *the through-line* lifts. The *through-line* term itself is Anderson's.
- **Nancy Duarte, *Resonate: Present Visual Stories That Transform Audiences*** (Wiley, 2010). The canonical treatment of presentation structure that chapter 4 § *the talk arc* draws from. [Book site](https://www.duarte.com/books/resonate/).
- **Nancy Duarte, *slide:ology: The Art and Science of Creating Great Presentations*** (O'Reilly, 2008). The companion deck-authoring reference.
- **Carmine Gallo, *Talk Like TED: The 9 Public-Speaking Secrets of the World's Top Minds*** (St. Martin's Press, 2014). Secondary-source treatment of the TED-style keynote.
- **Garr Reynolds, *Presentation Zen: Simple Ideas on Presentation Design and Delivery*** (New Riders, 3rd edition 2019). The minimalist-slide-design reference.
- **Jeff Bezos's 2017 shareholder letter** — [`www.aboutamazon.com/news/company-news/2017-letter-to-shareholders`](https://www.aboutamazon.com/news/company-news/2017-letter-to-shareholders). The *high-standards* writing-culture framing that chapter 4 § *the FAQ the room brings* is a parallel practice of; the Amazon narrative-first culture is the parent discipline mod-504 chapter 5 inherited.
- **Colin Bryar and Bill Carr, *Working Backwards: Insights, Stories, and Secrets from Inside Amazon*** (St. Martin's Press, 2021). The six-pager, PR/FAQ, and working-backwards process chapters are the canonical reference for the FAQ-as-first-class-artifact discipline chapter 4 lifts.

## Academic publishing craft (for the boundary chapter 3 draws) — peer-track reference

Chapter 3 explicitly cedes the academic-publishing craft to the peer research-principal track ([`ai-research-scientist-learning`](https://github.com/ml-engineering-curriculum/ai-research-scientist-learning)). The reference texts on academic ML publishing — cited here only to make the boundary legible, not as this module's primary craft:

- **Zachary Lipton and Jacob Steinhardt, [*Troubling Trends in Machine Learning Scholarship*](https://arxiv.org/abs/1807.03341)** (ICML 2018 Machine Learning Debates). The canonical treatment of what *not* to do in ML publishing; chapter 3 § *the honest-failure discipline* and § *writing discipline* lift the don't-oversell-the-method guidance from this piece.
- **ML Reproducibility Checklist** (NeurIPS) — [`www.cs.mcgill.ca/~jpineau/ReproducibilityChecklist.pdf`](https://www.cs.mcgill.ca/~jpineau/ReproducibilityChecklist.pdf). Joelle Pineau's reproducibility checklist adopted by NeurIPS. Chapter 3 § *evaluation methodology* lifts the methodology-section-rigor discipline from this.
- **Peer-reviewed ML academic venues** — NeurIPS ([`neurips.cc`](https://neurips.cc/)), ICML ([`icml.cc`](https://icml.cc/)), ICLR ([`iclr.cc`](https://iclr.cc/)). These are the venues the peer research-principal track owns the publication craft for; chapter 3 of this module uses the industry-track-adjacent workshops at these venues rather than the main tracks.

## Return-signal measurement — chapter 6 canon

Chapter 6 § *the three return signals* and § *the tracking dashboard* draw from the broader portfolio-tracking and signal-measurement canon. The primary tools and sources:

- **Google Scholar** — [`scholar.google.com`](https://scholar.google.com/). The canonical citation-graph surface for papers.
- **Semantic Scholar** — [`www.semanticscholar.org`](https://www.semanticscholar.org/) (Allen Institute). The applied-ML-aware alternative to Google Scholar with better industry-citation surfacing.
- **GitHub Insights** — [`docs.github.com/en/repositories/viewing-activity-and-data-for-your-repository`](https://docs.github.com/en/repositories/viewing-activity-and-data-for-your-repository/). The canonical repository-adoption signal surface for open-source releases.
- **PyPI download statistics** — [`pypistats.org`](https://pypistats.org/) and the official [BigQuery PyPI dataset](https://docs.pypi.org/api/bigquery/). The canonical Python-package download signal.
- **npm download statistics** — [`www.npmjs.com`](https://www.npmjs.com/) (per-package download tabs).
- **Internet Archive / Wayback Machine** — [`web.archive.org`](https://web.archive.org/). The archival surface the retirement-criteria discipline (chapter 6 § *retirement is explicit, not passive*) relies on for *"what was the state of this release when we retired it"*.

## Target posting corpus — the specific framings this module operates against

The composite target framings quoted throughout the chapters are these postings. Full text and URLs are in [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md).

- **Capital One** — Senior Distinguished AI Engineer. Load-bearing clause (chapter 1, chapter 3, chapter 4, chapter 5): *"ML industry impact through conference presentations, papers, blog posts, or open source contributions."* The four-venue-class enumeration this module is organised around.
- **Ibotta** — Principal ML Engineer. Load-bearing clause (chapter 2): *"act as a leading contributor, voice, and thought leader in a growing community of machine learning practitioners."* The internal-community-first framing chapter 2 is scoped against.

## Track-level companion material

- [`../../CURRICULUM.md`](../../CURRICULUM.md) — the six-module arc and where mod-506 sits in it. The `req-industry-influence` requirement entry's below-threshold-in-window evidence that justifies the 10-hour module size.
- [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) — the 26-posting evidence catalogue the Capital One and Ibotta target framings are sourced from.
- [`../../PREREQUISITES.md`](../../PREREQUISITES.md) — the assumed staff-plus IC foundation. If the staff-plus IC leadership canon (Larson, Reilly, Fournier) and the applied-ML blog editorial standard are unfamiliar, chapter 2's internal-first substrate and chapter 3's writing discipline will be hard to operate against.
- [`../../projects/project-503-industry-influence-artifact-portfolio/`](../../projects/project-503-industry-influence-artifact-portfolio/) — the capstone project that integrates this module into a shipped multi-venue artifact portfolio.
