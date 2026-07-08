# The ML Bet Portfolio — Five Rows at Principal Altitude

> Chapter 2 of mod-502. Prerequisite: chapter 1 — the working definition of a North Star. Downstream: chapter 3 sequences these bets into a multi-year roadmap; chapter 4 attaches non-goals and sunset criteria; chapter 7 packages them into the one-pager and the deep-dive.

## Why five rows

Chapter 1 fixed the North Star as *a small portfolio of bets*. This chapter names the specific shape the sample supports for the modelling-side principal — five rows, one per bet class, at bet altitude, not implementation altitude:

1. **Gen-AI direction** — integration vs. build-vs-buy of foundation models across the ML function.
2. **RecSys / personalization direction** — the org-scope ranking, retrieval, and personalization stack and metrics.
3. **Agentic-AI direction** — bet size, time horizon, and boundary against RAG-only or classical-pipeline approaches.
4. **Foundation-model / large-scale fine-tune program direction** — whether and how the org invests in owning training-scale artifacts.
5. **MLOps discipline as an org contract** — the platform-and-process bet the whole ML org converges on.

The five rows are load-bearing, not arbitrary. Every principal-scope theme in the 2026-Q2 sample that names a *technology direction* (not a process, not an audience, not a mentorship practice) maps into one of these five. If your North Star has a sixth row, it either belongs to one of the five (in which case merge) or belongs in the peer platform-side principal track's mod-505 (in which case cite, don't duplicate).

The peer platform-side principal track ([`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) mod-505 — long-term technical bets) frames its portfolio around *platform* bets: capacity substrate, training-platform build-vs-adopt, inference-serving substrate, developer-experience contracts, org-wide reliability discipline. Reading its shape alongside this chapter is useful for two reasons: it shows what the platform-side counterpart of a modelling bet portfolio looks like, and it names the seam where a modelling bet in this module's portfolio depends on a platform bet in that module's portfolio. Neither module owns both sides.

## Bet altitude versus implementation altitude

Before the rows: the discipline that keeps this chapter from re-doing staff-track work.

At **bet altitude**, a row answers: *should we do this, at what scale, over what horizon, and what would stop us?* One paragraph. One page at the outside. The reader is a CTO, a peer VP, a Head of AI Governance, a CFO who signs the multi-year capacity plan.

At **implementation altitude**, a row answers: *how do we do this, on what stack, with which recipe, at what latency, at what cost per token, on which schedule?* Multiple RFCs. Owned by staff engineers, specialist tracks, and platform teams. The reader is engineers building on the substrate.

The bet-altitude paragraph *cites* the implementation-altitude RFCs; it does not re-state them. If your North Star row starts to name specific model architectures, MFU targets, GPU SKUs, or per-quarter milestones, you have slipped down into staff scope. Lift the paragraph back up.

## Row 1 — Gen-AI direction

**Question the bet answers.** Where does the ML function integrate frontier foundation models via API, where does it adopt open-weights models and post-train them in-house, and where — if anywhere — does it invest in owning the pretraining artifact? Over the 3-to-5-year window, what is the trajectory?

**Load-bearing distinctions.**

- **Integrate** — the org calls a hosted frontier API (OpenAI, Anthropic, Google, hyperscaler-hosted) as the underlying capability. The bet is on the supplier and on the abstraction layer the ML function builds over the supplier.
- **Adopt-and-post-train** — the org runs an open-weights model (Llama 3-family, DeepSeek-V3-family, etc.) on its own infrastructure and post-trains for specific workloads. The bet is on the ability to close the capability gap between the mid-tier open-weights model and the frontier, at economics that beat the API for the workloads that matter.
- **Own the pretrain** — the org trains its own foundation model from scratch or from a public checkpoint at meaningful compute. The bet is on unique data, unique capability requirements, or unique cost structure that a frontier lab will not serve.

Most orgs' honest answer is a mix. The bet is which mix, over what horizon, and what would move the mix.

**Hand-offs.** Recipe for post-training belongs to [`fine-tuning-engineer-learning`](https://github.com/ml-engineering-curriculum/fine-tuning-engineer-learning). Recipe for pretraining belongs to [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) and [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-403. Integration engineering (RAG, tool-calling, prompt discipline) belongs to [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-304 and [`applied-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/applied-ai-engineer-learning). None of that recipe belongs in this row; the row *cites* it.

**Sample framing shape (illustrative, single row of a North Star).**

> Adopt frontier foundation models via API for the two consumer-facing product areas with the highest capability floor (X and Y). Post-train a single mid-tier open-weights model for the enterprise-facing product area (Z), where data-residency and per-token economics do not clear the API bar. Do not train a foundation model from scratch in this window; revisit at the FY29 planning cycle if API economics shift by >2x against our workload mix or if data-residency requirements harden further.

**Common failure modes.**

- Mixing the row with the RecSys row because the RecSys team also uses Gen-AI. RecSys is a *product area*, Gen-AI is a *capability class*. The RecSys row (row 2) names the org-scope ranking stack; the Gen-AI row names the capability strategy those product areas draw from.
- Naming a supplier commitment as the bet (*"we bet on Anthropic through FY29"*). The bet is the *strategy* (integrate frontier via API); the supplier is an implementation choice underneath it, adjudicated at a lower altitude and revisited more frequently.

## Row 2 — RecSys / personalization direction

**Question the bet answers.** What is the org-scope ranking, retrieval, and personalization stack the ML function converges on, what are the metrics leadership commits to for it over the multi-year horizon, and how does it evolve as Gen-AI capabilities intersect it?

**Load-bearing distinctions.**

- **Per-product-area stacks vs. a converged stack** — many orgs run several partially-independent RecSys stacks (feed, search, ads, notifications). The bet is whether the multi-year direction converges these onto a shared retrieval/ranking substrate, keeps them federated, or takes a hybrid path. Pinterest's *"unified technical architecture and defining a roadmap for industry-leading methodology"* is a converged framing; other orgs run federated by design.
- **Classical ranking vs. Gen-AI-augmented ranking** — where does the org invest in Gen-AI as a ranking-signal source, as a query-understanding upgrade, as an on-surface generation feature, or as a re-ranker? Which of those is a bet, and which is a hedge that becomes a bet only when a specific signal fires?
- **Metrics leadership commits to** — is the org's ranking success framed by engagement, quality, safety, revenue, or a composite? The metric is a strategic commitment, not a project-level KR.

**Hand-offs.** The build of the stack belongs to [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-302 / mod-303 / mod-306, [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning) mod-110, and [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning) for the underlying feature store, model registry, and serving substrate. The portfolio-scope architecture — Pinterest / Airbnb / Uber / DoorDash-style shared substrate — belongs to `staff-ml-engineer-learning` mod-401 / mod-402. This row cites, does not duplicate.

**Sample framing shape (illustrative).**

> Converge feed, search, and notifications ranking onto a shared retrieval + reranking substrate over the multi-year horizon; keep ads ranking federated for revenue-attribution reasons named in the non-goals. Invest in two-stage retrieval as the org-scope pattern; invest in Gen-AI-based query understanding as a hedge (year 1 experiment, year 2 or 3 bet upgrade contingent on the acceleration signal defined in the tracker). Metric commitment: engagement + long-term retention composite, not click-through.

**Common failure modes.**

- Writing the row as a single team's roadmap. This row is org-scope; if the reader thinks "this is the ranking team's plan", the altitude has slipped.
- Naming specific model architectures (two-tower, cross-encoder, MoE ranker). Architecture selection lives in the staff RFC. The bet is the substrate direction and the metric commitment.

## Row 3 — Agentic-AI direction

**Question the bet answers.** How big a bet is the org placing on agentic AI (multi-step tool-use, autonomous workflow completion) over the multi-year horizon, at what time horizon, and where is the boundary with the safer, better-understood RAG-and-classical-pipeline approach?

**Load-bearing distinctions.**

- **Size of bet** — is agentic AI a strategic differentiator the org is investing multi-year in, a supporting capability inside broader product-area work, or a hedge waiting on capability maturity? Different orgs land at all three; the honest answer for most is the middle.
- **Time horizon** — the agentic-AI capability frontier is moving fast enough that a 3-year bet is qualitatively different from a 5-year bet. Chapter 3 handles sequencing.
- **Boundary against RAG-only / classical-pipeline** — for each product area, what is the criterion that says "this workload should be a well-scoped agent" vs. "this workload should be a deterministic pipeline with an LLM step"? The North Star does not answer per-workload; it names the org-scope principle.

**Hand-offs.** Depth on agentic patterns, memory design, tool-use, and evaluation belongs to [`agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/agentic-ai-engineer-learning) / [`senior-agentic-ai-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-agentic-ai-engineer-learning) / [`agentic-systems-architect-learning`](https://github.com/ml-engineering-curriculum/agentic-systems-architect-learning). RAG depth belongs to [`rag-engineer-learning`](https://github.com/ml-engineering-curriculum/rag-engineer-learning). Application-layer engineering belongs to [`llm-application-developer-learning`](https://github.com/ml-engineering-curriculum/llm-application-developer-learning). This row cites those tracks by name; it does not repeat their material.

**Sample framing shape (illustrative).**

> Agentic AI is a hedge in year 1, a bet-upgrade candidate in year 2, contingent on the accelerator signals in the tracker (chapter 6). Bound investment in year 1 to two internal-tooling agents (developer productivity, customer support triage) with a shared eval harness. Do not stand up an autonomous customer-facing agent in this window; the safety and evaluation frontier will not be reliable at our SLA on that horizon.

**Common failure modes.**

- Writing the row as if agentic AI were a settled capability. It is not; the frontier moves. Chapter 6 handles the signal that would move the bet.
- Merging the row into Gen-AI (row 1). Agentic AI is a *usage pattern* built on top of foundation-model capability; the bet is qualitatively different, because it is about the org's willingness to accept the reliability profile of a multi-step system.

## Row 4 — Foundation-model program / large-scale fine-tune direction

**Question the bet answers.** Does the org invest in a foundation-model pretraining program or a large-scale fine-tune program in this window? If yes, at what scale, on what data, over what horizon? If no, what is the falsification signal that would make us revisit?

For the vast majority of orgs, the honest answer is *no in this window* — the capital investment, the data requirements, and the capability payoff make it uneconomic against frontier API adoption. The bet in that case is the *no* — with the reasoning and the falsification criteria named explicitly, so future you can defend the choice.

For the small number of orgs where the answer is *yes*, the row commits leadership to the scale, the horizon, and the boundary against alternatives.

**Hand-offs.** The pretraining recipe (Chinchilla-optimal framing, data-mixture ablations, parallelism strategy, MFU) belongs to `staff-ml-engineer-learning` mod-403 (foundation-model programs), mod-404 (distributed-training strategy), and to `training-pipeline-engineer-learning`. Capacity economics belong to `staff-ml-engineer-learning` mod-407. The peer platform-side track's mod-505 owns the platform decision (build the training platform vs. adopt). This row does *not* teach any of that — it commits leadership to the *strategic answer*.

**Sample framing shape (illustrative, "no" case).**

> No foundation-model pretraining program in the FY26–FY30 window. Rationale: fully-loaded per-model economics against expected internal workload volume do not clear a frontier-API adoption breakeven at any scenario in the capacity plan. Falsification: revisit at the FY29 planning cycle if (a) data-residency or contract-restriction signal makes API adoption infeasible for >=30% of workloads by revenue, or (b) frontier API pricing per million tokens rises by >=3x on the two-year forward curve, or (c) unique-data value in the enterprise product area rises to a scale that a mid-tier post-training program cannot capture.

**Common failure modes.**

- Treating this row as a technical opinion ("training is cool") rather than a leadership commitment. The *no* case is harder to write well than the *yes* case, because it has to defend against the Silicon-Valley default that everyone should train.
- Duplicating staff-scope pretraining depth. If your row is naming context lengths, tokenizer choices, or MFU targets, you have slipped altitude.

## Row 5 — MLOps discipline as an org contract

**Question the bet answers.** What is the org-scope contract every ML team follows — the paved-road platform, the eval / release / observability discipline, the responsible-AI review gate, the shared feature and registry substrate — that binds the ML function to a consistent way of shipping and running production ML?

This row is often mis-scoped as a purely platform row (in which case it belongs to the peer platform-side principal track's mod-505). It belongs *here*, at modelling-principal altitude, when the *contract* the platform enforces is a modelling-side commitment: *every production model is evaluated on the org's canonical harness before launch; every model class named as high-tier under EU AI Act runs through the responsible-AI review gate; every online model observes the same drift, freshness, and safety monitors.*

**Load-bearing distinctions.**

- **Contract vs. platform build.** The row commits leadership to the *contract* — the seam every ML team agrees to. The peer platform-side track's mod-505 commits leadership to the *build* — which team builds the paved road, on what substrate. Both bets have to be coherent; this row asserts the modelling-side commitment and cites the platform-side commitment.
- **Regulatory posture as a bet.** The org's stance on NIST AI RMF adherence, EU AI Act tiering, and forthcoming regulatory frameworks (US EO / OMB memos, upcoming state-level laws, ISO/IEC 42001) is a bet with strategic consequences for what the ML function can ship and when. This row names the posture and the escalation path when the regulatory landscape shifts (chapter 6).

**Hand-offs.** The portfolio-scope AI risk register, EU AI Act tiering, and standardised model cards belong to `staff-ml-engineer-learning` mod-409. The paved-road platform build belongs to `ai-infra-ml-platform-learning`, `ai-infra-mlops-learning`, and — at principal altitude on the platform side — `ai-infra-principal-engineer-learning` mod-505. The cross-team eval program belongs to `staff-ml-engineer-learning` mod-405 / mod-406, [`model-evaluation-engineer-learning`](https://github.com/ml-engineering-curriculum/model-evaluation-engineer-learning), and [`ai-eval-engineer-learning`](https://github.com/ml-engineering-curriculum/ai-eval-engineer-learning). Policy authoring belongs to [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning). This row cites all of those.

**Sample framing shape (illustrative).**

> The ML function operates a single paved-road contract: every production model registers in the org registry, evaluates on the canonical harness before launch, ships behind the shared inference gateway, and observes the shared drift + safety monitor set. Two named exceptions (adjudicated in the deep-dive companion doc): the ranking online-learning surface and the search retrieval-index rebuild loop, which each have documented deviations. The org's responsible-AI posture aligns to NIST AI RMF 1.0 with the Generative AI profile; EU AI Act tiering is applied to every customer-facing model class; the review gate is jointly owned with Head of AI Governance. Falsification signal for the shared contract: chapter 6.

**Common failure modes.**

- Turning the row into a checklist ("we do MLflow, we do model cards, we do canaries"). A checklist is not a bet.
- Naming a specific tool as the bet ("we bet on MLflow"). Tools are implementation choices under the contract; the bet is the contract.

## The five rows together

A principal-scope North Star has *these five rows and roughly no others*. It has row 1 (Gen-AI direction), row 2 (RecSys / personalization direction), row 3 (agentic-AI direction), row 4 (foundation-model program direction), row 5 (MLOps as org contract). It has a paragraph per row at bet altitude, and the paragraph cites — does not repeat — the specialist-track and staff-track material underneath.

When one of the five is genuinely not applicable to the org (a B2B enterprise SaaS org may not have a meaningful RecSys row; a consumer-social org may not have an agentic-AI row at material altitude), the row should still appear with a one-sentence *not-applicable-in-this-window* explanation. Silence on a row reads as an omission, not a decision.

Chapter 3 sequences the rows into a multi-year roadmap. Chapter 4 attaches non-goals and sunset criteria. Chapter 7 packages the whole into the one-pager and the deep-dive.

## Summary

- The bet portfolio has exactly five rows at modelling-principal altitude: Gen-AI direction, RecSys / personalization direction, agentic-AI direction, foundation-model program direction, MLOps as org contract.
- Each row is written at bet altitude — one paragraph, defensible to CTO / SVP — and cites the specialist and staff tracks that own the implementation depth.
- Hand-off contracts to the peer specialist tracks and the staff-plus tracks are named explicitly per row. Nothing in this chapter re-does that material.
- The peer platform-side principal track's mod-505 (long-term technical bets) is the closest structural parallel. Read the two portfolios side by side to see the platform bets and the modelling bets as a coherent whole.
- A missing row on your draft is a decision; a silent row is an omission. Write every row, even the ones that resolve to "not in this window".
