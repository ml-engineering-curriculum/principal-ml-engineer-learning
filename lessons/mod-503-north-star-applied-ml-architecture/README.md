# mod-503-north-star-applied-ml-architecture: North-Star Applied-ML Architecture — Living Diagrams, Canonical APIs, and Org-Scope Reference Architecture

**Estimated effort:** 14 hours

This module owns the *paired* artifact to mod-502's multi-year strategy: the **north-star applied-ML architecture** the whole ML org converges on. The target framing is Capital One's *"north star platform architecture, continuously publishing and refining living diagrams and canonical APIs"* — read as a paired set of *living diagrams* and *canonical APIs*, maintained on a cadence rather than shipped as a one-shot RFC.

Read the chapters in order. Each one sharpens one clause of chapter 1's working definition: chapter 2 fixes the altitude; chapter 3 fixes the shape; chapter 4 fixes the four canonical APIs; chapter 5 fixes what "living" means in practice; chapter 6 fixes evolution and version-bump discipline; chapter 7 fixes the org-wide review body; chapter 8 fixes the seam contracts with peer platform-side principals and the governance branch.

## Learning objectives

- Publish and continuously refine a north-star ML architecture the whole org converges on — living diagrams, canonical APIs, contracts between the ML org, the platform teams, and the product teams — using Capital One's *'north star platform architecture, continuously publishing and refining living diagrams and canonical APIs'* as the target artifact. The output is not one RFC; it is a maintained artifact.
- Reason about applied-ML architecture at portfolio-and-industry altitude: not the multi-team blueprint (staff scope — owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-402) but the reference architecture that spans multiple product areas, sets the shape the ML org converges on, and stays usable for years. Ground the shape in Chip Huyen (*Designing Machine Learning Systems*), Google's *Rules of ML*, and the canonical Meta / Airbnb / Uber applied-ML architecture case studies.
- Set the canonical API surface — feature contract, model-registry contract, eval-harness contract, inference-gateway contract — the ML org publishes to product teams; make it stable enough that product teams build against it and versionable enough that the ML org can evolve it.
- Author the reference architecture's evolution plan: how a new bet (Gen-AI, agentic, RecSys re-platform, foundation-model program) plugs into the north-star architecture without forcing a rewrite, and what triggers a version-bump.
- Run the org-wide architecture-review body: what the principal blocks, what they nudge back with feedback, what they escalate to peer platform principals or to the executive branch — and where they defer to the staff-scope multi-team blueprint owner rather than duplicating the review.
- Set the hand-off contract to the peer platform-side principal tracks ([`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning), [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning)) for platform-side scope, and to the peer executive branch ([`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning)) for policy and governance scope.

## Chapters

1. [`01-what-a-north-star-architecture-is-and-is-not.md`](01-what-a-north-star-architecture-is-and-is-not.md) — the working definition, the Capital One target framing unpacked, and the five defensibility tests (convergence, contract stability, evolution discipline, ownership legibility, publication cadence). What the artifact is *not* — multi-team blueprint, RFC/ADR log, deployment-state snapshot, org chart, manifesto.
2. [`02-portfolio-and-industry-altitude.md`](02-portfolio-and-industry-altitude.md) — the two altitudes (staff multi-team blueprint vs. principal reference architecture), the three-literature canon (Chip Huyen; Google *Rules of ML*; Meta / Airbnb / Uber / Netflix / LinkedIn / Pinterest engineering blogs), and the two altitude-slip failure modes (downward into blueprint, upward into manifesto).
3. [`03-canonical-shape-of-the-org-scope-reference-architecture.md`](03-canonical-shape-of-the-org-scope-reference-architecture.md) — the six planes (data, feature, training, registry, evaluation, serving), the two cross-cutting slices (observability, governance / responsible AI), the two cited substrates (compute, corporate). Per-plane load-bearing elements, failure modes, and hand-offs.
4. [`04-canonical-api-contract-surface.md`](04-canonical-api-contract-surface.md) — the four canonical APIs: feature contract, model-registry contract, eval-harness contract, inference-gateway contract. The eight required elements per contract (purpose, versioning, schema, invariants, SLOs, failure modes, ownership, evolution rules). The stability-vs-versioning tension.
5. [`05-living-diagrams-and-publication-cadence.md`](05-living-diagrams-and-publication-cadence.md) — the single canonical location, the three-refresh cadence (quarterly / semi-annual / annual) plus two emergency triggers, per-contract semver plus whole-artifact version, diagram-as-code discipline, and the pragmatic tooling stack.
6. [`06-evolution-plan-and-version-bump-triggers.md`](06-evolution-plan-and-version-bump-triggers.md) — the four bet classes (capability, substrate, portfolio, governance), the version-bump trigger table, and the fixed shape of the evolution-plan section.
7. [`07-running-the-org-wide-architecture-review-body.md`](07-running-the-org-wide-architecture-review-body.md) — the standing charter, the five-population membership, the cadence, and the four decision modes (**block**, **nudge**, **escalate**, **defer**). The "defer to the multi-team blueprint owner" case walked explicitly.
8. [`08-hand-off-contracts-to-platform-principals-and-governance.md`](08-hand-off-contracts-to-platform-principals-and-governance.md) — the four substrate seams and the co-authored interfaces with peer platform-side principals; the three governance seam contracts (policy-to-contract mapping, risk-tier definition, documentation conventions). When to escalate above both seams to the executive branch.

## Exercises

Five exercises. The first establishes the artifact; the others populate its subtrees. Each builds directly on the artifact from exercise-01.

- [`exercises/exercise-01-living-north-star-architecture-artifact.md`](exercises/exercise-01-living-north-star-architecture-artifact.md) — 4h. Author the first-cycle artifact skeleton: canonical location, six-plane shape, four contract stubs, publication cadence, diagram set from diagram-as-code sources.
- [`exercises/exercise-02-canonical-api-contract-surface.md`](exercises/exercise-02-canonical-api-contract-surface.md) — 3h. Author the four canonical API contracts with the eight required elements each, plus the shared canonical-types document.
- [`exercises/exercise-03-reference-architecture-evolution-plan.md`](exercises/exercise-03-reference-architecture-evolution-plan.md) — 3h. Author the evolution-plan section — current-cycle bets by class, in-flight version bumps, currently-supported majors, deferred and out-of-scope items, plus the calibrated version-bump trigger table.
- [`exercises/exercise-04-org-wide-architecture-review-charter.md`](exercises/exercise-04-org-wide-architecture-review-charter.md) — 2h. Draft the review-body charter, membership, and the first session log — walking three items through the four decision modes.
- [`exercises/exercise-05-hand-off-contract-to-platform-principals.md`](exercises/exercise-05-hand-off-contract-to-platform-principals.md) — 2h. Author `seams/platform-side.md` (four substrate seams, four co-authored interfaces) and `seams/governance.md` (three governance seam contracts, policy-to-contract mapping table with real citable policies).

## Structure

- `01-…md` … `08-…md`: lecture chapters.
- `exercises/`: five hands-on exercises, one per major objective.
- `labs/`: reserved for optional long-form labs.
- `quizzes/`: knowledge check for the module.
- `resources.md`: cited external references — the applied-ML architecture canon, Rules of ML, the case-study literature, contract-tooling and diagram-as-code stacks, governance frameworks, peer principal tracks.

## Companion material

- [`../mod-502-org-and-industry-ml-strategy/`](../mod-502-org-and-industry-ml-strategy/) — the strategy artifact this architecture *pairs* with. Chapter 1 § *the paired-artifact frame* is the reference. The two artifacts cite each other.
- [`../mod-504-cross-org-influence-without-authority/`](../mod-504-cross-org-influence-without-authority/) — the *practice* of holding the seams named in chapter 8. Chapter 8 names the seam; mod-504 walks the room.
- [`../mod-505-principal-mentorship-and-technical-bar/`](../mod-505-principal-mentorship-and-technical-bar/) — the review-bar side of the review body's *block* and *nudge* modes.
- [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md) — the 26-posting evidence catalogue the module's target framings (Capital One, Pinterest, and their peers) draw from.
- [`../../CURRICULUM.md`](../../CURRICULUM.md) — where mod-503 sits in the six-module arc.
