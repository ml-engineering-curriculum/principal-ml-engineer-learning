# Portfolio-and-Industry Altitude — Reading the Applied-ML Architecture Canon

> Chapter 2 of mod-503. Prerequisite: chapter 1 (the working definition) and mod-501 chapter 6 (hand-off contracts). Downstream: chapter 3 fixes the canonical shape at this altitude; chapter 7 draws the review-body boundary against the multi-team blueprint owner.

## Two altitudes, one word

"Architecture" is used at many altitudes in ML engineering, and the level-40 staff and level-48 principal both do work called *architecture*. The staff owns the **multi-team blueprint** — the specific systems being built across a bounded portfolio of teams this fiscal year. The principal owns the **reference architecture** — the shape the ML org converges on across product areas over a 3-to-5-year horizon.

If those two altitudes are collapsed into one, one of two things happens. Either the principal descends into blueprint work (drawing box-and-line diagrams of the ranking team's current serving stack), or the staff ascends into reference-architecture work (writing 3-year vision docs the current fiscal year cannot execute). Both are common failure modes. Both waste the level's leverage. Both leave a seam open somewhere else that no one is minding.

This chapter fixes the two altitudes explicitly, walks the reference-architecture altitude the module owns, and grounds the shape in the canonical applied-ML architecture literature — Chip Huyen, Google's *Rules of ML*, and the Meta / Airbnb / Uber / Netflix engineering-blog case studies.

## The two altitudes

The clearest way to see the boundary is to line up what the two artifacts answer:

| Dimension                    | Multi-team blueprint (staff)                                     | Reference architecture (principal, this module)                                                   |
| ---------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Owner                        | Staff engineer(s) leading a bounded portfolio                    | Principal ML engineer, adjudicated                                                                |
| Horizon                      | 1–2 years, current planning cycle                                | 3–5 years                                                                                          |
| Scope                        | 3–5 named product-area teams and their platform counterparts     | The whole ML function across every product area                                                    |
| Audience                     | Director / VP + the named teams building against it              | CTO / SVP peer set + every ML team + every product team that consumes ML                          |
| Unit of commitment           | This-quarter builds; next-quarter builds                         | Contract stability + evolution plan                                                                |
| Failure mode if wrong        | This fiscal year misses; teams re-do work                        | Product teams cannot build against ML; org lacks a shape to converge on                            |
| Refresh cadence              | Per planning cycle (quarterly or half-yearly)                    | Semi-annual major, quarterly minor (chapter 5)                                                     |
| Canonical staff owner        | [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-401 / mod-402 | This module + peer platform-side principals ([`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning), [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning)) |

The two artifacts *cite* each other. The reference architecture is where the multi-team blueprint plugs in. The blueprint is where the reference architecture becomes concrete for a specific portfolio in a specific quarter. Neither is a substitute for the other; neither is a lift-and-shift of the other.

The seam is what chapter 7 walks: at the org-wide architecture review, the principal *defers* to the staff-scope blueprint owner on portfolio-level design decisions rather than duplicating the review. The principal's contribution is the seams — the contracts the blueprint has to meet, not the shape inside the blueprint.

## What "portfolio-and-industry altitude" actually means

At this altitude the reference architecture answers three questions no smaller-scope artifact answers well:

1. **Convergence.** Given N product areas (feed, search, ads, notifications, enterprise, personalization, safety, ...), what shape do they share? Where is the substrate common, where is the contract common, and where is per-product-area variation genuinely load-bearing?
2. **Seams with the platform and the product.** Where does the ML org draw the line with the platform substrate below it and with the product teams above it? Where are the canonical APIs that make those lines real?
3. **Evolution.** As bets change — foundation models come online, agentic patterns mature, a RecSys re-platform starts, a Gen-AI capability class emerges — how does the shape absorb them without a rewrite?

Everything else the ML function needs to design is at a lower altitude, and the answers depend on which portfolio, which team, which quarter. The reference architecture holds only what has to be true across all of them, and holds it for years.

A useful thought experiment: hold your draft against a *counterfactual* org three years from now. Is the shape still recognizable if the ranking team pivots to two-tower-plus-reranker, if the Gen-AI capability class rotates suppliers, if the eval program shifts from offline to online-first? If yes, you're at reference-architecture altitude. If no, you've drifted into blueprint.

## The canonical applied-ML architecture, in three literatures

You are not the first person to draw the shape. Three bodies of work carry most of the load; the reference architecture this module authors is a *specific-org synthesis* of them, not a novel invention.

### Chip Huyen — *Designing Machine Learning Systems*

Chip Huyen's *Designing Machine Learning Systems* (O'Reilly, 2022) is the closest thing the field has to a canonical vocabulary for the *shape* the principal north-star architecture names. Chapters 1–3 fix the definition of an ML system, its lifecycle, and the trade-off frame. Chapters 4–8 walk the offline planes — data, feature engineering, training, evaluation, model development. Chapters 9–11 walk the online planes — deployment, monitoring, continual learning. Chapters 10–11 in particular carry the framing this chapter borrows for the plane-by-plane decomposition (chapter 3).

For a principal writing a reference architecture, Huyen's book is doing two jobs. First, it fixes the *vocabulary* — *feature store*, *model registry*, *offline / online serving*, *training / serving skew*, *shadow deployment*, *continual learning*. Second, it draws the *default plane decomposition* — data → feature → training → eval → deploy → observe. That decomposition is not the only possible one, but it is what the field's readers will expect. Deviating from it puts a burden on your draft to explain why; matching it gets you readers primed with the vocabulary you need.

### Google — *Rules of Machine Learning*

Google's [Rules of Machine Learning](https://developers.google.com/machine-learning/guides/rules-of-ml) — Martin Zinkevich's numbered rules — is not an architecture document. It is a *discipline* document. Rules 1–13 (pre-ML, first pipeline, monitoring, launch) fix the engineering discipline the applied-ML pipeline has to hit. Rules 14–27 (ML phase I) walk the first-model-in-production shape. Rules 28–43 (ML phase II) walk the training / serving skew, the eval-metric alignment, and the online-vs-offline consistency the reference architecture has to enforce. Rules 44+ walk the engineering-for-humans discipline that maps directly onto the review-body practice in chapter 7.

For the principal writing the reference architecture, the *Rules* are the closest thing to a canonical statement of "here is what a rigorous applied-ML org actually enforces". They inform the *contracts* chapter 4 walks (feature contract, eval-harness contract) and the *review-body practices* chapter 7 walks (what to block, what to nudge). A north-star architecture that violates the Rules of ML is not defensible in front of a peer principal at Google, Meta, or any successor. Alignment with the Rules is baseline hygiene.

### The Meta / Airbnb / Uber / Netflix / LinkedIn case studies

The engineering-blog case studies are the third literature. Each is a specific org's specific-time snapshot of what the reference architecture looks like when it has been maintained for years. Reading them side by side is how you learn what stays constant across orgs and what is genuinely load-bearing per-org variation.

- **Meta — *[Applied Machine Learning at Facebook](https://engineering.fb.com/2018/05/09/core-infra/applied-machine-learning-at-facebook-a-datacenter-infrastructure-perspective/)*.** Older but structurally still the load-bearing paper. Shows the plane decomposition at datacenter scale, the substrate the product-area models share, and the seam between the ML org and the infrastructure org. The reference architecture this module walks is directly informed by the shape this paper drew.
- **Uber — *[Meet Michelangelo](https://www.uber.com/blog/michelangelo-machine-learning-platform/)*, and the follow-on posts.** The canonical case study of a paved-road MLOps substrate. Feature store, model store, training-pipeline templates, deployment substrate — the whole shape as a platform contract product teams build against. Chapter 4's canonical API framing owes the most to Michelangelo's example.
- **Airbnb — *[Bighead](https://medium.com/airbnb-engineering/bighead-airbnbs-end-to-end-machine-learning-platform-a1c2b3e4d0e0)*, *[Zipline](https://medium.com/airbnb-engineering/zipline-airbnbs-machine-learning-data-management-platform-d0dc06e7a3c0)*, and their successors.** Illustrative of how the reference architecture *evolves* through multiple named bets. Chapter 6's evolution-plan discipline mirrors what Airbnb's platform blog documents over multiple posts.
- **Netflix — *[Metaflow](https://netflixtechblog.com/tagged/metaflow)*, RecSys posts, and the eval-culture posts.** Reference for the developer-experience shape a canonical API surface has to hit; reference for how the eval program becomes an org-wide contract rather than a per-team practice.
- **LinkedIn — *[Feathr](https://engineering.linkedin.com/blog/2022/open-sourcing-feathr---linkedin-s-feature-store-for-productive-machine-)* and the platform posts.** Reference for a canonical feature-store contract, and for how an org publishes a feature contract externally without breaking internal consumers.
- **Pinterest** — the org whose posting is one of the module templates (*"unified technical architecture and defining a roadmap for industry-leading methodology"*); its [engineering blog](https://medium.com/pinterest-engineering) is the primary source for what its unified architecture looks like across content, ads, and search.

The right reading discipline is not to copy any one org's shape into your draft. It is to read three or four side by side, notice what is invariant (the plane decomposition is; the presence of a feature contract is; a model-registry contract is), and notice what is per-org load-bearing (Airbnb's temporal-data emphasis; Uber's driver-partner and ETA training; LinkedIn's professional-graph feature substrate; Netflix's per-title RecSys shape). Then argue *your* org's version.

## What the reference architecture does not own

Reference-architecture altitude means the artifact does not own several categories of work. Explicit non-ownership is how you keep it small enough to stay alive.

- **Model architecture selection.** Whether the ranking model is a two-tower + reranker, an MoE ranker, or a graph-based recommender is not a north-star decision. It is a staff RFC decision, revisited more frequently than the reference architecture is refreshed. The reference architecture names the *shape* the ranking model plugs into (retrieval → ranking → reranking → serving), not the model architecture.
- **Framework selection.** PyTorch vs. JAX, Ray vs. Kubeflow, Kubernetes vs. hyperscaler-native — these are staff-scope choices with quarterly-to-yearly refresh cycles. The reference architecture names the *interfaces* (canonical API contracts, chapter 4), and expects those interfaces to be honored across framework choices.
- **Cloud / vendor selection.** *"We run on AWS"* is a corporate decision above the ML function; *"the training platform uses Ray"* is a platform-team decision. The reference architecture cites both and does not re-decide them.
- **Deployment topology.** Number of clusters, region topology, on-call rotation shape, autoscaling policy — these are SRE-and-platform work. The reference architecture names the *guarantees* the topology has to hit (latency SLO tier, availability tier), not the topology.
- **Per-quarter roadmaps.** The reference architecture has an evolution plan (chapter 6); it does not have quarterly milestones. Quarterly milestones live in the staff portfolio roadmap and the multi-team blueprint.
- **Team-level design reviews.** The reference architecture is cited by team-level design reviews; it is not their author. Chapter 7 walks the review-body practice.

## Two altitude-slip failure modes to watch

**Downward slip.** The draft names specific team owners, current-quarter roadmaps, per-model architecture choices, or cluster-topology decisions. The draft could be dropped into a staff portfolio blueprint and read fine. Fix: replace the specific with the class ("Ranking team's PyTorch reranker" → "the ranking substrate"); replace the current-quarter milestone with the evolution triggers (chapter 6); replace the team owner with the plane owner + the seam contract (chapter 8).

**Upward slip.** The draft reads as a manifesto or a market map. Nothing in it commits the org to a specific shape; every claim is *"and we may do X or Y depending on"*. A CTO cannot quote a shape from it because there is no shape. Fix: force convergence (chapter 1 property 1). The reference architecture is the *choice*, not the enumeration of options.

## A cross-org read-around exercise

To calibrate your own draft at portfolio-and-industry altitude, read the following four artifacts side by side and note what each names as its top-level plane decomposition and its top-level canonical contract:

1. Huyen, *Designing Machine Learning Systems*, chapter 10 (Infrastructure and Tooling for MLOps). What are the top-level planes she names, and what does she call the interfaces?
2. Uber's *Meet Michelangelo* (and one of its follow-ons — the *[Continuous Delivery for ML](https://www.uber.com/blog/continuous-integration-testing-machine-learning-models/)* post or the *[Michelangelo's Machine Learning Model Serving](https://www.uber.com/blog/scaling-michelangelo/)* post). What is the canonical API surface product teams build against?
3. LinkedIn's Feathr post (or Meta's Feature Store post). What is the feature contract?
4. One of Airbnb's Bighead-era posts. What is the evolution story from Bighead to the successors?

The four together give you a spread of "what a mature applied-ML reference architecture actually looks like when someone else did it and wrote it up." Your draft should read as one *specific-org synthesis* of the same class.

## Summary

- Applied-ML "architecture" is used at two altitudes: the staff multi-team blueprint (bounded portfolio, this-year) and the principal reference architecture (whole ML function, 3-to-5 years). This module owns the second altitude only.
- Portfolio-and-industry altitude means the reference architecture answers three questions the smaller altitudes cannot: what shape the org converges on across product areas, where the seams with the platform and the product teams sit, and how the shape absorbs new bets without a rewrite.
- Ground the shape in the applied-ML architecture canon: Chip Huyen's *Designing Machine Learning Systems* (vocabulary and plane decomposition), Google's *Rules of Machine Learning* (discipline and contract enforcement), and the Meta / Uber / Airbnb / Netflix / LinkedIn / Pinterest engineering-blog case studies (specific-org syntheses to read side by side).
- The reference architecture does *not* own model architecture, framework choice, cloud vendor, deployment topology, quarterly roadmaps, or team-level design reviews. Each of those has an explicit owner; the reference architecture cites, does not duplicate.
- Watch both altitude-slip failure modes: downward into blueprint (specific teams / quarters / models) and upward into manifesto (no convergence, no shape). The corrective in each case is chapter 1's convergence property.
- Chapter 3 walks the canonical shape at this altitude. Chapter 4 walks the canonical API contract surface that makes the shape usable to product teams.
