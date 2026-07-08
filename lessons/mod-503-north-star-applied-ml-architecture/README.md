# mod-503-north-star-applied-ml-architecture: North-Star Applied-ML Architecture — Living Diagrams, Canonical APIs, and Org-Scope Reference Architecture

> Scaffolded by `aicg org execute-plan`. Lecture chapters and exercise content are authored on subsequent autonomous cycles.

**Estimated effort:** 14 hours

## Learning objectives

- Publish and continuously refine a north-star ML architecture the whole org converges on — living diagrams, canonical APIs, contracts between the ML org, the platform teams, and the product teams — using Capital One's 'north star platform architecture, continuously publishing and refining living diagrams and canonical APIs' as the target artifact. The output is not one RFC; it is a maintained artifact.
- Reason about applied-ML architecture at portfolio-and-industry altitude: not the multi-team blueprint (staff scope — owned by `staff-ml-engineer-learning` mod-402) but the reference architecture that spans multiple product areas, sets the shape the ML org converges on, and stays usable for years. Ground the shape in Chip Huyen (Designing Machine Learning Systems), Google Rules of ML, and the canonical Meta / Airbnb / Uber applied-ML architecture case studies.
- Set the canonical API surface — feature contract, model-registry contract, eval-harness contract, inference-gateway contract — the ML org publishes to product teams; make it stable enough that product teams build against it and versionable enough that the ML org can evolve it
- Author the reference architecture's evolution plan: how a new bet (Gen-AI, agentic, RecSys re-platform, foundation-model program) plugs into the north-star architecture without forcing a rewrite, and what triggers a version-bump
- Run the org-wide architecture-review body: what the principal blocks, what they nudge back with feedback, what they escalate to peer platform principals or to the executive branch — and where they defer to the staff-scope multi-team blueprint owner rather than duplicating the review
- Set the hand-off contract to the peer platform-side principal tracks (`ai-infra-principal-engineer-learning`, `ai-infra-principal-architect-learning`) for platform-side scope, and to the peer executive branch for policy and governance scope

## Structure

- `01-…md` … `0N-…md`: lecture chapters.
- `exercises/`: per-exercise prompts.
- `labs/`: long-form hands-on labs.
- `quizzes/`: knowledge checks.
- `resources.md`: external references.
