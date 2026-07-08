# Hand-Off Contracts to Staff-Plus IC Scope

> Chapter 6 of mod-501. Prerequisite: chapters 1–5, plus the [`../../PREREQUISITES.md`](../../PREREQUISITES.md) staff-scope foundation from `staff-ml-engineer-learning`. This chapter closes the loop: the principal lifts staff scope; the principal does not re-do it.

## The lift-vs-redo distinction

A common failure mode when a staff engineer starts operating at principal altitude is that they keep authoring the staff-scope artifact instead of the principal-scope artifact. The multi-team blueprint gets scoped harder. The portfolio TCO gets re-defended. The staff-plus hiring loop gets calibrated one more time by the same engineer. None of that is wrong, but it does not lift the ML org's altitude — it just does the previous level's job better.

The principal-scope move is to *lift* the staff-scope artifact: point it at the org- and industry-wide direction, use it as input to a north-star artifact one altitude higher, and delegate the staff-scope authoring itself to the staff engineers you now coach and calibrate. The principal-scope North Star cites the staff-scope multi-team blueprint. The principal-scope north-star architecture composes the staff-scope multi-system RFCs. The principal-scope technical bar reads the staff-scope hiring calibration and adjudicates.

Two failure modes to avoid:

- **Re-doing staff scope.** The most common failure — the newly-titled principal keeps the staff-scope work they were already good at and never lifts. Result: the ML org's altitude never rises, the staff engineers under the principal never get to author their own artifacts because the principal keeps doing it for them, and the principal never learns what mod-502 through mod-505 teach.
- **Skipping staff scope.** The rarer failure — the newly-titled principal treats staff scope as beneath them and asks for a portfolio blueprint from someone else so they can start on the North Star. This does not survive interview. The North Star's credibility depends on being able to cite specific staff-scope work the principal actually did or coached. Skip the ladder rung and the ladder above it will not hold.

The right move is lift-not-redo. This chapter draws the seam for every dimension the staff track owns.

## Hand-off contracts, dimension by dimension

Each subsection: what the staff track owns, what the principal lifts to, and what the seam looks like as an artifact.

### Multi-team ML architecture / blueprint

**Staff owns** (`staff-ml-engineer-learning` mod-401 through mod-404): the multi-team blueprint for a portfolio of 3–5 production ML systems. The multi-system RFC that argues merge / split / share of a substrate across teams. The migration cost defence.

**Principal lifts to** (mod-503 in this track): the north-star applied-ML architecture the whole ML org converges on. Living diagrams. Canonical APIs — feature store, model registry, eval platform, inference gateway, training platform contract. Reference architecture that a new bet plugs into without a rewrite.

**Seam artifact.** The north-star architecture *cites* the multi-team blueprints — one per product area, each authored by the responsible staff engineer — as its concrete underlayers. The blueprints stay authored by staff. The north-star architecture is authored by the principal and evolves as new blueprints come in. When a new bet is scoped (chapter mod-502), the north-star architecture is what tells the staff engineer scoping the bet where the canonical seams are and which contracts to preserve.

Rule of thumb: if you are drawing the boxes for a single portfolio, you are doing staff scope. If you are drawing the boxes that all portfolios must fit into, you are doing principal scope.

### Foundation-model program

**Staff owns** (`staff-ml-engineer-learning` mod-403): the foundation-model pretraining or large-scale fine-tune program. Chinchilla-style compute-optimal framing. Data mixture, ablation sequencing, capability-vs-safety post-training investment. The failure-mode budget.

**Principal lifts to** (mod-502 in this track): whether the ML org should run a foundation-model program *at all* in the multi-year window — the bet-portfolio decision — and, if yes, what its role is inside the org direction. Not the pretraining recipe; the strategic bet.

**Seam artifact.** The multi-year North Star document has a foundation-model program row. The row's *description* is a principal-scope framing (why the org invests, what non-goals fall out of the investment, what sunset criteria trigger a stop). The row's *implementation* is a staff-scope RFC (Chinchilla framing, MFU estimate, cluster and cost plan). Principal authors the row; staff authors the RFC. Both artifacts cite each other.

Rule of thumb: if you are deciding whether the org should train from scratch versus fine-tune versus adopt a frontier model, you are doing principal scope. If you are deciding the recipe once the org has committed to train from scratch, you are doing staff scope.

### Distributed-training strategy

**Staff owns** (`staff-ml-engineer-learning` mod-403 and mod-404): the parallelism recipe (FSDP / tensor-parallel / pipeline-parallel / 3D-parallel). The MFU estimate and cluster utilisation model. The kernel-level failure-mode budget. Peer platform track `training-pipeline-engineer-learning` owns the build.

**Principal lifts to** (mod-502): the industry-scope framing of distributed-training bets — should the org run its own training platform, or adopt one; what capacity portfolio (reserved / on-demand / spot / multi-cloud / self-hosted) fits the org's multi-year direction; whether frontier-scale training is even in scope for this org.

**Seam artifact.** The North Star document has a training-platform bet row. Principal decides "own vs adopt vs partner"; staff scopes the "how" if own is chosen. The peer platform tracks scope the platform build. No principal-scope module in this track re-teaches parallelism recipes; those live at staff and infra tracks.

Rule of thumb: if you are picking between FSDP and 3D-parallel for a specific training run, you are doing staff / infra scope. If you are picking between owning and adopting a training platform for the ML org over multiple years, you are doing principal scope.

### Portfolio TCO and GPU capacity

**Staff owns** (`staff-ml-engineer-learning` mod-407): the portfolio-scope GPU capacity forecast, the capacity-portfolio mix, the FinOps discipline, the CFO-readable TCO model.

**Principal lifts to** (mod-502 and mod-504): the multi-year capacity investment as a bet in the North Star, the CFO-partnership contract on how the ML org's spend fits the org's overall AI investment, and the escalation path when a bet demands a step-change in capacity.

**Seam artifact.** The North Star document has a capacity row. Principal frames the multi-year investment case for the CFO / CTO audience; staff authors the TCO model that grounds the number. The CFO reads the principal-scope framing; the CFO's team pressure-tests the staff-scope TCO. Both artifacts stay in sync.

Rule of thumb: if you are proving out a spot / reserved mix for the ranking portfolio next fiscal year, you are doing staff scope. If you are arguing the multi-year AI-capacity trajectory for the CFO and CTO to commit to, you are doing principal scope.

### Portfolio-scope responsible AI

**Staff owns** (`staff-ml-engineer-learning` mod-409): the portfolio-scope AI risk register (NIST AI RMF + Gen-AI profile), EU AI Act tiering across the portfolio, standardised model cards and datasheets, the pre-launch review gate.

**Principal lifts to** (mod-502): the org- and industry-scope framing of responsible AI as a strategic bet. The North Star row on responsible AI as an org contract. Partnership with `head-of-ai-governance-learning` on which policy authoring is jointly owned. The `head-of-ai-governance` peer track authors the policy; the principal ensures the ML org converges on it.

**Seam artifact.** The North Star has a responsible-AI row that names the org-scope contract, the partnership with governance, and the escalation path for a high-tier system. Staff authors the register. Governance authors the policy. Principal frames how the two artifacts fit the multi-year direction.

Rule of thumb: if you are tiering a specific system under EU AI Act, you are doing staff / governance scope. If you are framing the ML function's multi-year responsible-AI trajectory for the CTO and Head of AI Governance, you are doing principal scope.

### Staff-plus technical leadership (coaching and hiring calibration)

**Staff owns** (`staff-ml-engineer-learning` mod-410): the exec-audience RFC (VP-level), staff-plus hiring loop as an *interviewer* + first-round calibrator, coaching L30 senior tech leads through single-team scope, the multi-quarter roadmap leadership commits to.

**Principal lifts to** (mod-504 and mod-505): the SVP / CTO-level audience (not VP), staff-plus hiring loop as a *loop-level* calibrator (not interviewer), coaching L40 staff engineers through their staff-scope work, and the multi-year North Star (not multi-quarter roadmap).

**Seam artifact.** The mod-410 executive-audience RFC portfolio at staff altitude *feeds* the mod-504 SVP / CTO narrative practice at principal altitude — the principal cites, reframes, and elevates the staff-scope RFCs. The mod-505 loop-level calibration reads and adjudicates the mod-410 interviewer-level calibration.

Rule of thumb: if you are the interviewer providing rubric evidence on a candidate, you are doing staff scope. If you are the calibrator adjudicating whether the loop overall reached hire / no-hire / staff-vs-senior, you are doing principal scope.

### Cross-team eval program

**Staff owns** (`staff-ml-engineer-learning` mod-405 and mod-406): the cross-team eval harness standard, LLM-as-judge policy at portfolio scope, shadow / canary / progressive-rollout contract every team follows.

**Principal lifts to** (mod-503): the eval canonical API as part of the north-star architecture. Not the harness itself; the seam the harness exposes to every ML team in the org. The `model-evaluation-engineer-learning` and `ai-eval-engineer-learning` peer tracks own the eval-platform build.

**Seam artifact.** The north-star architecture has an eval canonical API contract. Staff authors the org's harness against that contract. Peer eval-engineer tracks author the platform behind the contract. Principal ensures the contract is durable across bets.

## The re-do trap, by module

For each downstream module in this track, note the staff-scope artifact you might feel tempted to re-author instead of lifting:

- **mod-502 (org-industry strategy)** — do not re-write the portfolio roadmap. Do write the multi-year North Star that the portfolio roadmaps roll up into.
- **mod-503 (north-star architecture)** — do not re-draw the multi-team blueprint diagrams. Do draw the north-star diagram that the multi-team blueprints slot into, and do author the canonical API contracts.
- **mod-504 (cross-org influence)** — do not re-author the VP-level RFC. Do build the SVP / CTO narrative that the VP-level RFC feeds into.
- **mod-505 (mentorship + technical bar)** — do not interview one more senior candidate. Do calibrate the loop, adjudicate the interviewer split, and set the bar the interviewer cohort calibrates against.
- **mod-506 (industry influence)** — do not blog about one more ranking-team production incident. Do author the piece the org's staff engineers will cite in their own blog posts about the same incident class.

Every one of these traps is a lateral move from staff-scope competence to staff-scope-in-principal-clothing. Chapter 6's job is to name them explicitly so you can spot the pull toward them and refuse it.

## A working hand-off contract, once you have a Family 1 role

Once you actually hold a Family 1 role, an explicit contract with the staff engineers underneath you is a helpful working artifact. A shape that has worked for the StaffEng.com Distinguished / Fellow interviews (see [`resources.md`](resources.md)):

- **Staff-owned artifacts** (list): the multi-team blueprint per product area, the portfolio TCO, the exec-audience RFC at VP altitude, the portfolio-scope risk register, the cross-team eval harness, the multi-quarter roadmap. The principal does not co-author; the principal reviews and adjudicates.
- **Principal-owned artifacts** (list): the North Star document, the north-star architecture with canonical APIs, the SVP / CTO narrative, the technical bar, the industry-influence pieces. The staff engineers do not co-author; they contribute inputs.
- **Jointly-owned artifacts** (short list): the technical-bar rubric for staff-plus hiring loops (principal sets the bar; staff engineers apply it), and the sunset-criteria list for retired bets (principal decides; staff engineers execute).
- **Escalation path** for disagreement: staff engineer surfaces disagreement in the design review; if unresolved, principal calls a decision; if the staff engineer still disagrees, path escalates to the VP (not to skip the principal). No side channels around the principal.

Write this contract down. Revisit it every six months. It saves both the staff engineers below you and you from lift-vs-redo confusion.

## Summary

- The principal lifts staff scope; the principal does not re-do it.
- Every downstream module in this track (mod-502 through mod-506) has a specific re-do trap — the staff-scope artifact you'll feel tempted to re-author. Name the trap so you can refuse it.
- The hand-off contract is a working artifact with three lists: staff-owned, principal-owned, jointly-owned — plus an escalation path.
- The prerequisites [`../../PREREQUISITES.md`](../../PREREQUISITES.md) file names the specific staff-scope competencies this chapter presumes. If any are shaky, close the gap in `staff-ml-engineer-learning` before starting mod-502.
- Chapter 6 is the last chapter of mod-501. Exercise-04 asks you to produce the self-assessment; exercise-03 asks you to classify a batch of postings against the three role families from chapter 4; exercises 01 and 02 apply the vocabulary from chapters 1–3.
