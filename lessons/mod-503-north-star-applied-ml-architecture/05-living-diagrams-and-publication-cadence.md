# Living Diagrams and the Publication Cadence

> Chapter 5 of mod-503. Prerequisite: chapters 1–4. Downstream: chapter 6 walks the version-bump triggers a refresh cycle acts on; chapter 7 walks the review body that ratifies each refresh.

## Why "living" is the load-bearing word

The Capital One target framing — *"north star platform architecture, continuously publishing and refining living diagrams and canonical APIs"* — puts the discipline before the artifact. The verb chain is *continuously publishing and refining*. The adjective is *living*. Every failure mode this chapter is trying to prevent lives in the gap between an artifact that exists once and an artifact that stays honest across years.

Three specific ways an architecture stops being living, all common enough to name:

1. **Snapshot-in-Confluence.** The artifact was written for a launch, was excellent, has not been touched since, and now describes a shape the org has drifted away from. A new engineer reads it and starts working against a fiction.
2. **Everywhere-and-nowhere.** The artifact exists as PowerPoint files, Miro boards, Google Docs, and Notion pages, each authored by a different team, each partly correct. There is no single URL a reader can be handed. Convergence quietly failed at the artifact level.
3. **Reactive-only-refresh.** The artifact is refreshed *when someone complains*. That means the artifact is always a quarter behind the state of the org, and the org's ML function is always negotiating with a shape it already outgrew.

A living architecture solves each of the three with a discipline: a **single canonical location** (chapter 5 §1), a **publication cadence** with named triggers (§2), a **versioning discipline** across all four contracts and the diagram set (§3), and a **diagram-authoring discipline** that keeps the diagrams accurate to what they claim to model (§4).

## §1 — The single canonical location

Every reference architecture needs one URL you can point at. Not a folder, not a Slack thread, not a Confluence space: one page (or a small, indexed set of pages behind one root URL) that carries the *current* diagrams and the *current* contract versions, and links to every prior version under version discipline.

Two properties matter:

- **Discoverable.** A new engineer joining the ML function should learn the URL on their first day, either through onboarding or through an org-wide bookmark. If a random member of a product team cannot find the URL in under two minutes, the artifact is not doing its job.
- **Trustworthy.** The URL is the source of truth. If somebody has a differing version somewhere else, the URL wins by construction — this is a social contract the principal enforces at the review body (chapter 7) and defends with the CTO (mod-504).

The location itself is not the point — an internal docs site, a GitHub / GitLab / Gerrit repo published to an internal pages site, a Backstage catalog entry — any of these work. What matters is that there is *exactly one*.

A useful checklist for the location:

- [ ] One root URL, memorable enough to be quoted in a meeting.
- [ ] Current version banner at the top: *"v3.2, refreshed 2026-04-14"*.
- [ ] Table of contents mirroring the six-plane shape (chapter 3) and the four contracts (chapter 4).
- [ ] Link to the current major of each contract's schema (`v1.4` feature, `v2.1` registry, `v1.3` eval, `v3.2` gateway) and to prior majors still in the support window.
- [ ] Link to the changelog and the version-bump triggers (chapter 6).
- [ ] Link to the review-body queue and the recent-decisions log (chapter 7).
- [ ] Link to the peer platform-side principal's substrate contracts (chapter 8).
- [ ] Link to the mod-502 strategy documents the architecture pairs with.
- [ ] A "how to consume this artifact" section for the two audiences (staff engineer / product engineer / partner principal).

The last one is often skipped and it should not be. The consumers of the artifact are three different audiences: staff engineers building blueprints against it, product engineers building integrations against the contracts, and peer principals negotiating seams. A short paragraph per audience saves multiple hours per week across the org.

## §2 — The publication cadence

The cadence has three named refreshes and two named triggers.

### The three named refreshes

- **Quarterly minor refresh.** Diagrams, cross-links, changelog updated. Contract minor version bumps applied. Chapter 7's recent-decisions log rolls forward. Cadence: end of each fiscal quarter. Owner: the principal, with substrate updates from the peer platform-side principal.
- **Semi-annual major review.** Full re-read of the six-plane shape and the four contract surfaces against the state of the org and the state of the industry. Contract major version bumps considered. Evolution plan (chapter 6) updated to name the plug-in points for the current-half bets. Cadence: aligned with the mod-502 strategy refresh cadence. Owner: the principal, chaired at the org-wide architecture-review body (chapter 7).
- **Annual grand refresh.** A larger cycle that revisits the shape itself — e.g. is the six-plane decomposition still the right one? Do we still need four contracts and not five? Should observability be promoted from a slice to a plane? Cadence: annually, aligned with the fiscal year. Owner: the principal, ratified with the CTO / peer principals.

### The two named emergency triggers

- **Bet-portfolio change.** If mod-502's strategy portfolio changes materially between refreshes — a bet is sunset, a new bet is committed, a foundation-model program is approved — the architecture publishes an interim refresh naming the plug-points. Chapter 6 walks the trigger discipline.
- **Regulatory or incident trigger.** A regulatory shift with a compliance deadline (EU AI Act obligation activation, ISO/IEC 42001 audit finding), or a post-incident review with an architecture-level finding, triggers an interim refresh. The specific plane / contract carrying the change is named; a full-artifact refresh does not wait for the next cadence.

The specific dates and owners for the current cycle live on the canonical location. The purpose of writing the cadence in this chapter is that a new principal picking up the artifact knows *what pattern to expect*.

## §3 — Version discipline across the four contracts and the diagram set

The reference architecture has *two* versioning axes:

- **Per-contract semver.** Each of the four canonical APIs (chapter 4) carries an independent major/minor/patch. Contracts evolve at their own paces.
- **Whole-artifact version.** The reference architecture as a whole carries a version — `v3.2`, `v3.3`, `v4.0` — that a reader can pin against. Whole-artifact bumps are less frequent than any single contract's bumps.

The interaction:

- A patch or minor bump on a single contract *does not* bump the whole-artifact version. Example: `feature/v1.4 → feature/v1.5` adds an optional field; the artifact goes from `v3.2` to `v3.3` at the next quarterly refresh with an update to that section, but not sooner and not sitting on the whole artifact.
- A major bump on any single contract bumps the whole-artifact minor. Example: `registry/v2 → registry/v3` requires the artifact to bump `v3.2 → v3.3` at a minimum, with a callout on the changelog.
- A major bump on multiple contracts or a change to the six-plane shape bumps the whole-artifact major. Example: promoting observability from slice to plane is a whole-artifact major.

Version discipline notes:

- **Contract majors are supported N-and-N-1 concurrently.** The ML org runs both versions long enough for product teams to migrate. The migration horizon is documented (typically two quarters after the new major ships). Chapter 4 §"Stability vs. versioning tension" is the reference.
- **Deprecations carry an end-of-life date.** The date is a commitment; sliding it silently is the failure the discipline exists to prevent. The review body (chapter 7) is where dates get held or renegotiated in the open.
- **Contract-version stamping on every response.** Every response returned by the substrate implementations of the four contracts carries `contract_version`. Product teams' observability data now includes which contract versions their integrations exercise, and the ML org can see support-window drift in dashboards, not in incidents.
- **Whole-artifact version pinning is a valid request.** A product team building an integration can say *"we build against reference architecture v3.2, contract set (feature v1.4, registry v2.1, eval v1.3, gateway v3.2)"* and the ML org honors it under the support window. This is what makes the artifact usable to product teams.

## §4 — Diagram-authoring discipline

Diagrams are the most-cited and most-drifted artifact in any architecture document. Four disciplines make them stay living.

### Discipline 1 — Diagram-as-code

Every diagram is generated from a text source in the canonical location's repo. When the diagram source is a `.puml` (PlantUML), `.mmd` (Mermaid), `.d2` (D2), or `.dot` (Graphviz) file — or their peers — the version history is visible in the git log, the diff on a diagram change is reviewable, and no one can "just update the picture" without leaving a trace. Diagram-as-code is not fashion; it is what makes the "living" property enforceable at the review body.

The specific tool is a per-org choice — PlantUML, Mermaid, D2, and Structurizr (the C4-native tool) are all reasonable. What is not reasonable at this altitude is a `.pptx` or a Google Slides file as the source of truth.

### Discipline 2 — A small, fixed diagram set

The canonical location holds a *fixed set* of diagrams, always at the same names. Adding a new diagram to the fixed set is a review-body decision; deleting one is likewise. The set typically includes:

- **Six-plane band diagram** (chapter 3's mental picture, cleaned up). The top-of-page view.
- **Contract surface diagram**: the four canonical APIs (chapter 4), the actors on each side, the version pins.
- **Registry state-machine diagram**: `registered → eval-passed → canary → blessed → deprecated → retired`, with the transitions and signatures required for each.
- **Serving-routing diagram**: how the gateway resolves aliases → registry → model URIs → serving pool, with canary / A-B / shadow lanes.
- **Governance-slice diagram**: which plane carries which sign-off; where policy documents ([`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning)) attach.
- **Substrate seams diagram**: where the ML architecture meets [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) and [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) (chapter 8).
- **Evolution plug-in diagram**: current-cycle bets and their plug-in points (chapter 6).

Seven diagrams. Every one has a fixed name, a fixed slot in the canonical location, and a fixed audience-labeling convention. Adding one is a proposal; removing one is a version-bump event.

### Discipline 3 — Notation coherence with the industry

The [C4 model](https://c4model.com/) is the modal notation for system architecture in 2026, and reading its four levels (Context / Container / Component / Code) as an *outside-in* zoom is what most engineers arrive already knowing. The reference architecture is a *Context / Container* altitude document, occasionally reaching to *Component* when a contract's substrate is being discussed. Below *Component* is blueprint (staff) or implementation (build teams).

You do not have to use C4 notation. But if you use a different notation, cite the choice explicitly in a "notation guide" section on the canonical location. Every reader has a background from somewhere; naming the notation reduces the cognitive load of the read by an order of magnitude.

### Discipline 4 — Every diagram cites the contract it depicts

A diagram of the serving plane cites *inference-gateway contract v3.2*. A diagram of the registry state machine cites *registry contract v2.1*. A diagram of the training plane cites *training-pipeline substrate contract vX.Y from the peer platform-side principal's artifact*. If a diagram cannot cite its underlying contract, the diagram is decorative rather than load-bearing, and it either needs a contract or does not belong in the canonical set.

## The tooling stack — a pragmatic default

Different orgs settle differently, but a pragmatic default that has worked across the case-study literature is:

- **Repository.** A single git repo (`org/ml-north-star-architecture`) that publishes to an internal pages site under a stable URL.
- **Diagram source.** PlantUML, Mermaid, or D2 files under `diagrams/`. Rendered to SVG and PNG at publication time.
- **Contract sources.** OpenAPI / protobuf / GraphQL / Thrift files under `contracts/{feature,registry,eval,gateway}/vN.M/`. Linted, versioned, and published to the ML function's SDK repos on merge.
- **Changelog.** `CHANGELOG.md` in the repo, one entry per whole-artifact version bump, cross-referencing per-contract bumps. A patch is a paragraph; a major review is a page.
- **Review body records.** `review-log/` with one dated entry per architecture-review-body session — attendees, decisions, defer/block/nudge/escalate outcomes (chapter 7).
- **Docs site.** A generator (Docusaurus, Backstage TechDocs, mdBook, MkDocs) rendering the repo to the canonical URL. The docs generator is not the artifact — the repo is — but the site is what most consumers see.

This is one reasonable stack. Two other reasonable stacks are Backstage TechDocs plus its Software Catalog (if the org already runs Backstage) and Confluence with strict version discipline via a plugin (if the org's Confluence hygiene is unusually strong). Do not run all three simultaneously; that is the "everywhere and nowhere" failure mode.

## Publication as a communication act

The publication cadence is a communication act as much as a hygiene one. Every publication event is an opportunity to:

- Announce what changed and why (to the ML org, to the peer platform-side principal, to product-team leadership).
- Name deprecation timelines to keep them live in consumers' planning.
- Cite the strategy documents from mod-502 the refresh aligns with.
- Refer specific new decisions to the review body's next session (chapter 7) rather than piling them into the refresh.

The bad shape is a publication that reads as *"here is the new v3.3, please read it in your own time"*. The good shape is a short summary email or channel post — *"v3.3 changes X, Y, Z; deprecates A with EOL 2026-Q4; upcoming review-body item is B"* — with the docs link. The mod-504 material on cross-org influence is the reference for the communication craft; the takeaway for this chapter is that the publication *event* matters, not just the *content*.

## Common failure modes for the publication discipline

- **Refresh becomes a compliance ritual.** The cycle happens; nobody reads the diffs. Fix: use the review-body (chapter 7) as the forcing function; require a five-minute walk-through of the diff at every session.
- **Refresh becomes an author-only-refresh.** The principal updates the artifact solo; product teams and platform teams are not consulted. The artifact drifts from what the org actually converges on. Fix: chapter 7's review-body membership includes the two audience-representatives.
- **Version discipline is aspirational.** The changelog says the semver rules, but breaking changes ship without a major bump. Fix: contract-version stamping in responses (§3) makes drift visible in observability data; the review body enforces the semver discipline at the moment of merge, not after.
- **Diagram sprawl.** A dozen new diagrams show up over three refreshes; none of them replaces an existing one. The fixed-set discipline (§4 discipline 2) is the corrective.
- **Support-window silently slides.** A major version is nominally deprecated but nobody in the ML function actually retires it because two product teams have not migrated. The migration horizon becomes de-facto infinite. Fix: cross-hold with product-team leadership at the review body; escalate to peer VPs of product before the horizon slides silently.

## Summary

- "Living" means the artifact has a single canonical location, a published cadence, a version discipline, and an authoring discipline that keeps its diagrams honest to the org's current state.
- One URL. One canonical location. Discoverable in under two minutes; trustworthy by construction; carrying the current versions and the changelog.
- Cadence: quarterly minor refresh, semi-annual major review, annual grand refresh, plus two named emergency triggers (bet-portfolio change and regulatory / incident trigger).
- Two versioning axes: per-contract semver (each contract at its own pace, with N-and-N-1 concurrent support and named deprecation EOL) and whole-artifact version (bumped by any contract major or any shape change).
- Diagram-authoring disciplines: diagram-as-code; a small, fixed diagram set; notation coherence (C4 is the modal choice; whatever you use, cite it); every diagram cites the contract it depicts.
- Treat every publication as a communication act. The bad shape is silent; the good shape is a short summary that names what changed, what's deprecated, and what's coming to the review body.
- Watch the five publication-discipline failure modes: compliance-only refresh, author-only refresh, aspirational versioning, diagram sprawl, silent support-window slide. Chapter 7's review body is the corrective for most.
