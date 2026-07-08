# Tracking Industry and Internal Signal That Would Falsify or Accelerate the North Star

> Chapter 6 of mod-502. Prerequisite: chapter 3 (sequencing) and chapter 4 (non-goals and sunset criteria). Downstream: chapter 7 packages the tracker's outputs into the deep-dive companion doc; the exercise-04 assignment implements a signal tracker end-to-end.

## Why signal tracking is a principal-scope artifact

A North Star with sunset criteria (chapter 4) but no signal tracker is unfalsifiable in practice: the sunset triggers exist on paper, but nobody is watching for them, and by the time the trigger has fired in a way that leadership can no longer ignore, the org has spent one to two extra years compounding on the wrong direction. The signal tracker is the operational discipline that closes the gap between "the criterion exists" and "the criterion is watched".

The tracker is also *not* a governance-review board (owned by the peer executive branch, [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning)) and *not* a market-research subscription (owned by product / strategy). It is a small, principal-owned artifact that names the specific signals per bet, the source that would surface each signal, the review cadence, and the decision protocol when a signal materially fires. Read the difference:

- A **market map** ("Anthropic released Sonnet 5.5; DeepSeek released V4") is an *input*.
- A **signal** ("Sonnet 5.5's per-token pricing at expected FY-end volume moves the Gen-AI row 1 sunset criterion by X") is what the tracker *produces* from inputs.
- A **decision** ("we are refreshing the North Star's Gen-AI row two quarters early because the signal materially fires") is what the tracker *escalates to*.

The tracker's job is the second bullet.

## The four signal categories

Every signal the tracker follows belongs to one of four categories. The categories are load-bearing because the *source*, the *cadence*, and the *decision-quality* differ for each.

### Category 1 — AI lab and applied-ML industry publications

**What it is.** Published technical output from the frontier labs (Anthropic, OpenAI, Google DeepMind, Meta AI Research, xAI, Mistral AI, DeepSeek, Alibaba, Qwen, and comparable), from major hyperscaler research groups (Google Research, Microsoft Research), and from the applied-ML industry-track venues (KDD applied track, RecSys, industry-track submissions at NeurIPS / ICML, engineering blogs from Airbnb, Uber, Netflix, Meta, Pinterest, LinkedIn, DoorDash, and their peers).

**What signal it carries.** Capability frontier shift (a new pretraining recipe closes a capability gap; a new alignment recipe drops the residual harm on a class of models); economics shift (a new architecture drops the compute cost of a capability by an order of magnitude); reference-architecture shift (a well-cited applied-ML system publishes a substrate that the org's row 5 might adopt or need to compete with).

**How it fires signal for each bet row.**

- Row 1 (Gen-AI): frontier lab publications, model-family release notes, pricing announcements. The Chinchilla paper is a canonical historical example of a lab publication that reshaped the compute-optimal framing every foundation-model bet inherited. Present-day equivalents include the Llama-3 herd technical report, the DeepSeek-V3 technical report, and any follow-on frontier release.
- Row 2 (RecSys): applied-ML industry-track papers, engineering blogs, RecSys conference proceedings.
- Row 3 (Agentic-AI): capability-benchmarking releases, agent-eval-harness releases, tool-use / function-calling reliability studies.
- Row 4 (Foundation-model program): compute-optimal training recipe evolution, MFU improvements, cluster-scale kernel work.
- Row 5 (MLOps as contract): applied-ML paved-road publications, org-scope architecture retrospectives.

**Cadence.** Weekly light scan; quarterly deep review.

**Failure mode.** Confusing "the paper is exciting" with "the paper fires a signal for our specific North Star row". The tracker's job is to filter to the second category. A useful heuristic: for each shortlisted paper, name which specific sunset or accelerator criterion in your North Star it moves, and by how much. If neither, drop.

### Category 2 — Cost and compute-generation shifts

**What it is.** Frontier API price changes, hyperscaler GPU capacity availability shifts, hardware-generation transitions (the current transition to the next major GPU class shipping in volume), and the resulting shift in per-token / per-training-run economics.

**What signal it carries.** The economics side of every sunset criterion in chapter 4. Row 1's *"if frontier API pricing falls below fully-loaded per-token cost of the in-house model at expected volume"* is a cost signal. Row 4's *"if frontier API pricing rises by ≥3x on the two-year forward curve"* is a cost signal. The MLOps row 5's cost side of contract exceptions is a cost signal.

**How it fires signal.**

- The two-year forward curve for frontier API pricing per million input and output tokens on the frontier suppliers your org actually uses. Track the announced price *and* the announced pricing tiers by volume; enterprise contracts often move differently than list price.
- The delivery calendar for the next GPU generation and the price/perf shift the org's capacity-planning peers expect. The `staff-ml-engineer-learning` mod-407 material and the peer platform-side principal track's mod-505 own the depth here; the tracker cites the projection, not the calculation.
- The cost of running the org's current in-house post-training program at expected FY-end volume, refreshed on the CFO / FP&A cadence and made comparable to the API alternative.

**Cadence.** Monthly for API-price watch; quarterly for the compute-generation transition; refreshed at each North Star refresh.

**Failure mode.** Reacting to a single API price cut without decoupling headline price from effective price at your org's actual volume and workload mix. Frontier suppliers announce tier changes, batch discounts, model-family price cuts, and pricing renegotiations at different cadences. The tracker projects the *effective* price, not the *announced* price.

### Category 3 — Regulatory and compliance-framework shifts

**What it is.** Formal regulatory frameworks and standards that materially change what the ML function can ship, when, or under what review — with a clear timeline and a clear obligation.

**What signal it carries.** Every bet has a regulatory posture; row 5 (MLOps as org contract) carries it explicitly. A shift in the regulatory frontier changes the boundary of what a bet can commit to.

**Named frameworks the tracker follows.**

- **EU AI Act (Regulation (EU) 2024/1689)** — official journal text is the source; the phased-obligation timeline (prohibitions first; GPAI obligations next; high-risk-system obligations following) is the tracker's calendar. The delegated acts and implementing acts issued by the European Commission and the AI Office are the source of ongoing signal. Track: (a) high-risk system tier definitions and how they map to the org's customer-facing model classes; (b) GPAI obligation thresholds; (c) transparency requirements for generated content; (d) any national competent authority guidance in the member states the org serves.
- **NIST AI Risk Management Framework 1.0 and the Generative AI Profile (NIST AI 600-1)** — voluntary in the US, but adopted as reference by many enterprise procurement processes. Track: framework revisions, generative-AI profile updates, sector-specific companion documents.
- **US Executive Orders and OMB memoranda on AI** — the executive-branch cadence carries shifts in the federal posture; track the relevant OMB memos on AI use and procurement.
- **ISO/IEC 42001** — the AI management system standard (2023, with revisions); track adoption by the org's enterprise customer segment.
- **Sector-specific frameworks** — for orgs in fintech, healthcare, education, hiring, or regulated consumer segments, the sector regulator's ML-specific guidance (e.g., US CFPB or OCC for fintech; US HHS OCR for healthcare; NYC Local Law 144 or comparable enactments for hiring). The `head-of-ai-governance-learning` peer track owns the depth; the tracker cites.
- **State-level enactments in the US and provincial enactments in other jurisdictions** — landscape shifts fast; the tracker watches the pipeline as well as the enacted list.

**How it fires signal.**

- A tier definition or obligation timeline change that reclassifies an org model class from tier N to tier N+1, materially raising the compliance cost.
- A GPAI obligation change that affects row 1's frontier-API adoption bet (transparency, data provenance, capability disclosure).
- A regulatory framework that lowers the effective cost of the in-house post-training program (e.g., data-residency hardening that lowers alternative options).

**Cadence.** Monthly light scan; quarterly deep review with `head-of-ai-governance` peer.

**Failure mode.** Chasing every proposed enactment without filtering to *material* obligations for the org's actual product surface. The `head-of-ai-governance` peer is the source of truth for what is material; the tracker cites.

### Category 4 — Internal early-warning metrics

**What it is.** A small number of internal metrics — not team-level OKRs, not per-system SLOs — that would surface trouble on a specific North Star bet earlier than a headline product metric would.

**What signal it carries.** The internal ground truth against which each bet's assumption stands or falls. Row 2's converged-substrate bet assumes the migration cost stays below a two-year benefit envelope; the internal metric is the incremental migration cost trajectory. Row 5's paved-road contract assumes adoption; the internal metric is the compliance rate against the contract and the exception count.

**Named metric types.**

- **Adoption** metrics: fraction of production models on the shared substrate; number of paved-road exceptions active; deviation-request cadence.
- **Cost** metrics: fully-loaded cost of a specific bet's underlying workload, tracked over quarters against the sunset threshold; compute utilisation on the training substrate if row 4 is not-in-window (a low-utilisation trajectory strengthens the not-in-window case).
- **Quality / capability** metrics: canonical eval-harness pass rates for the models produced under each bet; drift and safety monitor firing rates; incident count on customer-facing models under each bet's substrate.
- **Regulatory-readiness** metrics: fraction of tier-N-and-above models with the required review-gate artifacts; audit-finding count by category.
- **Coalition** metrics: whether the peer platform-side principal, the peer executive branch, and the CFO share the bet's story in their own artifacts. If the peer's roadmap silently un-invests the bet's dependency, that is a signal.

**Cadence.** Quarterly review at the North Star refresh; per-bet dashboards updated monthly.

**Failure mode.** Confusing internal early-warning metrics with product OKRs. The engagement / retention / revenue targets are OKRs; the tracker's job is one altitude up. If a metric shows up on the executive dashboard the CEO looks at, it is probably an OKR and not a tracker signal.

## The tracker as a working artifact

A serviceable tracker is a small standing document — a page or two — with the following shape.

```
Signal Tracker for the ML North Star (FY26 refresh)
---
Last full review: 2026-06-15
Next scheduled full review: 2026-12-15
Emergency-refresh triggers: any category-3 obligation shift; any category-2
  cost signal moving a sunset criterion by ≥25%; any category-1 publication
  that a peer track's principal has already flagged as material.

Per bet, three rows:
  [row] [signal] [current-value + trajectory + threshold + last-checked]

Bet 1 — Gen-AI direction
  1a category-2 API pricing at FY-end volume | trajectory: ↓12% YoY; threshold to
     fire sunset: crossing fully-loaded in-house per-token cost; last checked
     2026-06-15
  1b category-3 EU AI Act GPAI transparency obligations | trajectory: delegated
     act expected 2026-Q4; threshold: any obligation that changes the abstraction
     layer's supplier interchangeability; last checked 2026-06-15
  1c category-1 frontier lab release cadence | trajectory: 3 material releases
     in the last quarter; threshold: a release that closes the capability gap
     the enterprise post-training program depends on; last checked 2026-06-15

Bet 2 — RecSys / personalization
  ...

[continued per bet]

Decision log:
  2026-04-02: Signal 1a triggered a partial refresh; row 1 sunset criterion
     restated with FY26 volume basis. Ratified by CTO on 2026-04-10.
  2026-05-18: Signal 5b (regulatory) surfaced; no bet change; noted for the
     December review.
```

The tracker is intentionally small. If it becomes a comprehensive market-intelligence document, it has drifted out of its role and become someone else's artifact. If it becomes a compliance checklist, the same.

## The decision protocol

When a signal *materially fires* — as adjudicated by the principal, ratified through the review cadence — the tracker triggers one of four decisions.

1. **Note.** The signal is real but not yet material enough to move the bet. Log it and increase the cadence on that signal until the next scheduled review.
2. **Partial refresh.** The signal is material for one bet; refresh that bet's row (sunset criterion or sequencing) at the next scheduled emergency-refresh window (not the full North Star). Chapter 4's writing discipline applies to the refresh.
3. **Full refresh.** Multiple signals across multiple bets have moved; the North Star needs a full refresh out-of-cycle. Typically triggered when a category-3 regulatory shift compounds with a category-2 cost shift, or when the peer platform-side principal's mod-505 grid has moved.
4. **Sunset execution.** A sunset criterion (chapter 4) has fired unambiguously. Execute the exit action; ratify with peers; publish the wind-down in the next deep-dive companion refresh.

Every decision goes into the decision log at the bottom of the tracker. Over two years, the decision log becomes the durable record of how the North Star responded to signal — which is what a CTO or SVP will look at when they want to know whether the tracker is doing its job.

## Where the tracker lives in the ecosystem

The signal tracker is principal-owned but shares boundaries with three peer tracks.

- **`head-of-ai-governance-learning`** owns the depth of category 3 (regulatory). The tracker cites, does not duplicate.
- **`staff-ml-engineer-learning` mod-407** owns the depth of the capacity-and-cost side of category 2. The tracker cites, does not duplicate.
- **`ai-infra-principal-engineer-learning` mod-505** owns the platform-side falsification tracker for the platform bets. The two trackers cross-reference each other; when a platform-side signal materially moves a modelling bet's dependency, it is expected to surface in this tracker as an internal early-warning metric (category 4) even before the platform-side principal has decided their own move.

Cross-referencing keeps the principals honest and the org's overall AI direction coherent.

## Summary

- The signal tracker is the operational discipline that keeps the sunset criteria (chapter 4) enforceable. Without the tracker, the criteria are decoration.
- Four signal categories: AI lab and applied-ML publications; cost and compute-generation shifts; regulatory and compliance-framework shifts; internal early-warning metrics.
- Each signal has a source, a cadence, a threshold, and a decision protocol. Weekly / monthly light scan; quarterly deep review; emergency refresh on named triggers.
- The tracker is a small, standing artifact — one to two pages — with per-bet rows and a decision log. Not a market map; not a governance-review board.
- Regulatory framework depth (EU AI Act, NIST AI RMF, ISO/IEC 42001, sector regulators) lives at `head-of-ai-governance-learning`; the tracker cites. Cost-and-compute depth lives at `staff-ml-engineer-learning` mod-407 and the peer platform track; the tracker cites.
- Chapter 7 handles the packaging: the tracker's snapshot appears in the deep-dive companion doc; the one-pager surfaces only the *material shifts since last refresh*.
