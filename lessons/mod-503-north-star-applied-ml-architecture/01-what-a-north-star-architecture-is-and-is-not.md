# What a North-Star Applied-ML Architecture Is — and Is Not

> Chapter 1 of mod-503. Prerequisite: mod-501 chapters 1 and 6 (verb-and-object vocabulary, hand-off contracts) and mod-502 chapter 1 (definition of a North Star as a *strategy* artifact). Downstream: every chapter here refines one clause of the definition this chapter fixes.

## Why start with the definition

Mod-502 already fixed what a *strategy* North Star is: a single, standing, executive-audience document that names the 3-to-5-year technical direction as a small portfolio of bets. This module owns a *paired* artifact — the **north-star applied-ML architecture** — that the strategy cites and that the whole ML org is expected to converge on. It is the shape the bets plug into.

The two artifacts are not the same. The strategy answers *what are we betting on, why, and what would make us stop?* The architecture answers *what is the shape our production ML systems converge on, and where does each new component plug in?* Both are principal-scope. Both are living. Neither replaces the other.

The Capital One Distinguished / Sr. Distinguished ML Engineer sample framing names the object of this module cleanly:

> "North star platform architecture, continuously publishing and refining living diagrams and canonical APIs."

Read that sentence with the same discipline mod-502 chapter 1 used on the SoundCloud framing. Object: *north star platform architecture*. Modifier that carries the entire discipline: *continuously publishing and refining*. Instrument that makes it usable: *living diagrams and canonical APIs*. Every phrase is load-bearing, and every subsequent chapter of this module refines one of them.

## Working definition

A **north-star applied-ML architecture** for an org is:

> A single, versioned, continuously refined reference architecture — expressed as living diagrams plus a small set of canonical APIs — that names the shape the whole ML org converges on across product areas, sets the seams between the ML org, the platform teams, and the product teams, and stays stable enough that product teams can build against it for years while the ML org evolves it under version discipline.

Read the sentence twice. Every clause is load-bearing.

- **single, versioned, continuously refined** — one artifact under one owner (the principal, adjudicated), on an explicit refresh cadence, with a version discipline that lets consumers pin against a version rather than a snapshot. Chapter 5 owns the cadence and versioning. If your org has three competing "north-star architecture" decks, the coordination job the artifact exists to do has not started yet.
- **reference architecture** — the shape the org converges on, not the deployed topology of any single system. Reference architectures constrain by naming; they do not deploy code. Chapter 3 walks the canonical shape.
- **living diagrams plus a small set of canonical APIs** — the diagrams are the shape; the canonical APIs are the *contracts* the shape makes concrete enough that product teams can build against it. Diagrams alone are wallpaper; contracts alone are a REST catalog. The pair is what the artifact is. Chapters 4 (contracts) and 5 (diagrams) own the pair.
- **the shape the whole ML org converges on across product areas** — the altitude is portfolio-and-industry, not multi-team blueprint. Chapter 2 draws that boundary against the staff-scope multi-team blueprint owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-401 / mod-402.
- **the seams between the ML org, the platform teams, and the product teams** — the artifact's primary purpose is not to draw boxes inside the ML org, it is to name the interfaces *between* the ML org and its two closest partners. The interfaces upward (product teams building against the ML function) and downward (the ML function building on the platform substrate) are the load-bearing seams.
- **stays stable enough that product teams can build against it for years while the ML org evolves it under version discipline** — the two acceptance tests. Contracts stable enough to build against and evolution disciplined enough that stability does not become stagnation. Chapter 6 owns evolution and version-bumps.

Every subsequent chapter in this module sharpens one of those clauses.

## The Capital One framing, unpacked

The Capital One sample framing is the cleanest single-sentence statement of the artifact in the 2026-Q2 sample. Three phrases carry most of the load, and every one of them cuts a common failure mode.

**"North star platform architecture."** *Platform*, in Capital One's usage in the posting sample, is not the ML platform team's substrate. It is the org-scope architecture the platform-and-product teams share — the shape the whole ML function converges on. Reading *platform* as *the ML platform team's stack* is the most common misread of this sentence in practice, and it collapses the artifact from principal altitude down into staff-scope platform blueprint. Chapter 2 makes the altitude distinction concrete.

**"Continuously publishing and refining."** This is not an RFC and it is not an ADR log. RFCs are proposals; ADRs record a decision at a point in time. Neither is *living*. The Capital One framing insists that the artifact is refreshed on a cadence, published to a known location the org can point at, and refined against consumer signal. Chapter 5 walks the cadence and publication discipline; chapter 6 walks refinement.

**"Living diagrams and canonical APIs."** The pair. Living diagrams — the shape, kept current under version discipline. Canonical APIs — the contracts the shape makes concrete: feature, model-registry, eval-harness, inference-gateway. Chapter 4 walks the four contracts; chapter 5 walks what makes a diagram *living* rather than a snapshot.

Read the Pinterest posting sentence alongside it — *"unified technical architecture and defining a roadmap for industry-leading methodology"* — and you see the same artifact viewed from the RecSys / personalization-heavy angle. Object: *unified technical architecture*. The unification is what makes it a north-star artifact rather than a per-product-area diagram. Both framings point at the same object; the Capital One framing carries the cadence and API discipline more explicitly, which is why this module treats it as the target.

## What a north-star architecture is *not*

Each of the following is a real, useful artifact. None of them is a north-star architecture. Naming them explicitly is how you keep your own draft honest.

### Not a multi-team blueprint (staff scope)

The multi-team blueprint owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-401 / mod-402 is the design for *the specific ML systems being built now across a small set of teams* — the ranking-team-plus-serving-team-plus-eval-team blueprint that ships this fiscal year. Its audience is a director; its horizon is a year or two; its scope is a bounded portfolio; its acceptance criterion is that the named teams can build against it in the current planning cycle.

A north-star architecture's audience is the CTO / SVP peer set plus every ML team in the org; its horizon is 3-to-5 years; its scope is the whole ML function across product areas; its acceptance criterion is that a new product area launching in year 3 can plug into the architecture without renegotiating the seams.

Signs your draft is a multi-team blueprint in north-star clothing: the diagrams name specific team owners inline ("Ranking Team's Redis-backed retrieval cluster"); the contracts embed a specific vendor or model architecture; the version cadence is quarterly and matches an OKR cycle. None of that belongs in the north-star architecture.

Chapter 2 draws the altitude boundary in detail. Chapter 7 owns the review-body practice of deferring to the blueprint owner rather than duplicating their review.

### Not an RFC or an ADR log

An RFC (request-for-comments) proposes a decision. An ADR (architecture decision record) logs one. Both are point-in-time artifacts, both are valuable, and neither is living. The north-star architecture cites RFCs and ADRs, and their outcomes shape it — but the artifact itself is *the current shape*, not *the history of how we got here*.

Signs your draft is an RFC in north-star clothing: it opens with a proposal ("we propose to adopt X"); it has an author-and-date at the top; it presumes a specific reviewer will approve or reject it. RFCs live in a `/rfc` directory, not in the north-star artifact.

### Not a systems context / C4 diagram set of the current deployment

The C4 model, ArchiMate, and their kin are useful notations. They are not, on their own, a north-star architecture. A C4 model of *what is currently deployed* is a snapshot of implementation state; it is what the SRE team looks at during an incident. A north-star architecture is the shape the org is *converging on*, not what is deployed at 2:00 AM today.

Signs your draft is a deployment-state snapshot in north-star clothing: it names specific hostnames, EC2 instance types, k8s namespaces, or DAG names; it is generated (or generatable) from infrastructure-as-code. Deployment state belongs in the SRE runbook; the north-star architecture references it, does not contain it.

### Not a set of team-boundary org charts

An org chart names who reports to whom. A responsibility map (RACI or similar) names who owns what. Both are people-artifacts, not architecture. The north-star architecture *does* name the seams between the ML org, the platform teams, and the product teams — but as *interfaces*, not as reporting lines. Chapter 8 owns the interface framing.

Signs your draft is an org chart in north-star clothing: the primary decomposition is by team; the diagrams have team names in the boxes instead of capabilities and contracts; the artifact would need to be re-drawn every time a team splits or merges.

### Not a manifesto or a set of principles

*"We invest in paved roads. We prefer standard interfaces. We build for observability by default."* These are principles. They are useful — mod-505 in this track handles the ones that shape the technical bar — but principles do not make an architecture. Principles constrain choices; the architecture *is* the choice.

Signs your draft is a manifesto in north-star clothing: the load-bearing content is a bulleted list of aspirational values; the sections read as *"we believe"* rather than *"the shape is"*; there is nowhere in the document that a reader could disagree with a specific claim rather than a general value.

## The five properties of a defensible north-star architecture

A draft is defensible when it passes all five of these tests. Use them as a checklist alongside the mod-502 chapter 1 list for the strategy.

1. **Convergence.** The artifact names one shape the org converges on, not a menu of options. A reader can point to a diagram and a contract and say *"this is the shape"* without hedging. The Capital One framing's *"north star"* is doing this work: a north star names direction, singular.
2. **Contract stability.** Product teams can build against the canonical APIs (chapter 4) with a documented version horizon. If the ML org has to change the shape of `GET /features/{entity}` next quarter, they must do it under a version bump, not a silent break.
3. **Evolution discipline.** A new bet — Gen-AI capability, agentic pattern, RecSys re-platform, foundation-model program — plugs into the architecture without forcing a rewrite. Chapter 6 owns the plug-points and the version-bump triggers.
4. **Ownership legibility.** For every plane in the architecture, the principal owner is named, the staff-scope blueprint owner is named, and the platform-side counterpart is named. Nobody has to guess which of the three level-48+ role families (mod-501 chapter 4) owns each seam.
5. **Publication cadence.** The artifact has a known location, a known refresh cadence, and a version number. Chapter 5 walks the discipline. A brilliant document that lives in a dead Confluence page is not a north-star architecture.

If a draft fails any one, the fix is usually earlier in the artifact than the fix appears. Convergence failures come from the altitude slipping down into blueprint (chapter 2); contract-stability failures come from the API surface not being carved right (chapter 4); evolution-discipline failures come from missing plug-points (chapter 6); ownership-legibility failures come from confusing the north-star architecture with the multi-team blueprint (chapters 2 and 7); publication failures come from treating the artifact as a one-shot RFC rather than as living (chapter 5).

## The paired-artifact frame

Read this chapter next to mod-502 chapter 1. The two definitions are deliberately parallel:

| Artifact                             | Owner scope        | Answers                                                             | Instrument                              | Refresh cadence                          |
| ------------------------------------ | ------------------ | ------------------------------------------------------------------- | --------------------------------------- | ---------------------------------------- |
| Multi-year ML technical North Star   | Principal (mod-502) | What are we betting on, why, and what would stop us?                | One-pager + deep-dive companion         | Semi-annually + emergency-refresh trigger |
| North-star applied-ML architecture   | Principal (this module) | What shape does the org converge on, and where does each thing plug in? | Living diagrams + canonical API contracts | Quarterly diagram refresh; APIs on semver |

The two artifacts cite each other. The strategy names bets; the architecture names the seams the bets plug into. Row 2 of the strategy (RecSys / personalization direction) cites the retrieval-and-ranking plane in the architecture. Row 4 (foundation-model program) cites the training-plane hand-off with `ai-infra-principal-engineer-learning`. Row 5 (MLOps as org contract) is largely *implemented by* the architecture's canonical APIs.

A CTO reading the strategy one-pager should be able to ask *"and what does that plug into?"* and be handed the architecture diagram. A staff engineer reading the architecture should be able to ask *"and why is this the shape?"* and be handed the strategy deep-dive. If either handoff feels forced, one of the artifacts has drifted.

## A worked micro-example

For grounding, here is what the *executive-summary paragraph* of a north-star architecture reads like at principal altitude. The full artifact is chapter 3's shape times chapter 4's contracts times chapter 5's diagram discipline.

> **Architecture (FY26 baseline, v3.2).** The ML function converges on a shared applied-ML substrate composed of six planes — data, feature, training, registry, eval, and serving — each fronted by a canonical API the product teams build against. The feature contract is the org-scope entry point for online and offline features (chapter 4). The model-registry contract is the source of truth for what is deployable, blessed, and retired. The eval-harness contract is the pre-launch bar every launch traces to. The inference-gateway contract is the sole ingress product teams call. Underneath, the platform teams own the substrate — Kubernetes, feature-store storage, model-registry storage, eval-orchestration runtime, gateway ingress — and their contracts (owned by [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning)) are cited in the seams doc (chapter 8). The architecture refreshes quarterly with a minor version bump and semi-annually with a major review; the current cycle's plug-points for the FY26 Gen-AI, agentic, and re-platform bets are listed in the evolution plan (chapter 6).

Notice what is *not* in that paragraph: specific Kubernetes namespaces, current inference latency numbers, per-team on-call rotations, current-quarter OKRs. What *is* in it: the shape, the four contracts, the seam ownership, the cadence, the plug-in strategy.

A product team engineer reading this paragraph can figure out which contract they build against. A staff engineer can figure out which plane their blueprint plugs into. A peer principal on the platform side can figure out where their contracts meet these. That is the standard the north-star architecture has to hit.

## Summary

- A north-star applied-ML architecture is a single, versioned, continuously refined reference architecture — living diagrams plus a small set of canonical APIs — that names the shape the ML org converges on across product areas, sets the seams with the platform teams and product teams, and stays stable enough for product teams to build against while evolving under version discipline.
- Capital One's *"north star platform architecture, continuously publishing and refining living diagrams and canonical APIs"* is the target framing. Every phrase is load-bearing: *platform* here means org-scope, not the ML platform team; *continuously publishing and refining* names the cadence; *living diagrams and canonical APIs* names the pair.
- A north-star architecture is *not* a multi-team blueprint, an RFC or ADR log, a deployment-state snapshot, an org chart, or a manifesto. Each of those is a real artifact; each rides in a different lane.
- Five defensibility tests — convergence, contract stability, evolution discipline, ownership legibility, publication cadence — every draft has to pass.
- Read this chapter alongside mod-502 chapter 1. The strategy and the architecture are paired artifacts; each cites the other. Chapter 2 draws the altitude boundary against the staff-scope multi-team blueprint.
