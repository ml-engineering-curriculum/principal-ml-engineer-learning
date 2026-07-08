# exercise-01: Living North Star Architecture Artifact

**Estimated effort:** 4 hours

## Objective

Author the *first-cycle* version of a north-star applied-ML architecture — the shape (chapter 3), the four contract references (chapter 4), and the publication skeleton (chapter 5) — as one living artifact under version discipline. This is the exercise that establishes the artifact itself; exercises 02–05 build out its individual sections.

The output pairs with the mod-502 exercise-01 one-pager (the two artifacts cite each other — chapter 1 § *paired-artifact frame*).

## Prerequisites

- Chapters 1, 3, and 5 read; chapter 4 skimmed. The six-plane shape and the four canonical APIs should be familiar names.
- Mod-502 chapters 1 and 2 read — the strategy artifact the architecture pairs with.
- A working editor and a diagram-as-code tool (PlantUML, Mermaid, D2, or Structurizr). Any of these is fine; choose one and stick to it.
- An org context to write against — either your current employer or a public reference org whose ML function you can construct a defensible shape for (Pinterest, SoundCloud, Airbnb, Uber, DoorDash, Capital One, Bumble, Instacart, Netflix are all reasonable; pick one whose applied-ML shape you have some real grounding in).

## Problem statement

You have been asked by your CTO (or, for a public-reference-org exercise, the counterpart CTO) to publish the first cycle of the org-scope north-star applied-ML architecture. The Capital One framing is your target — *"north star platform architecture, continuously publishing and refining living diagrams and canonical APIs"*.

Your job on this exercise is *not* to author the whole artifact end-to-end. It is to author the **artifact skeleton and the first cycle's shape** — enough that a review-body session (exercise-04) could ratify it as v1.0 and the four contract-surface details (exercise-02) can plug in on top.

The artifact is a *living* one. That means it has to have a single canonical location, a publication cadence, a version, and a diagram set drawn from diagram-as-code sources — not a slide deck.

## Requirements

Produce the artifact as a small git repository (local; do not commit into this curriculum repo). Directory layout:

```
your-workspace/ml-north-star-architecture/
├── README.md                        # the canonical page
├── CHANGELOG.md
├── diagrams/
│   ├── 01-six-plane-band.<ext>      # source
│   ├── 02-contract-surface.<ext>    # source
│   └── (others as authored)
├── contracts/                       # stub only; exercise-02 fleshes out
│   ├── feature/README.md
│   ├── registry/README.md
│   ├── eval/README.md
│   └── gateway/README.md
├── evolution-plan.md                # stub; exercise-03 fleshes out
├── review-log/                      # empty; exercise-04 populates
└── seams/                           # stub; exercise-05 fleshes out
    ├── platform-side.md
    └── governance.md
```

### The `README.md` canonical page (chapter 5 §1) — required content

- **Version banner** — `v1.0, published <YYYY-MM-DD>`.
- **A one-paragraph purpose statement** aligned with chapter 1's working definition and quoting the Capital One framing.
- **The six-plane shape** as a section, one paragraph per plane, at portfolio-and-industry altitude (chapter 3). Each paragraph names the plane's purpose, one to three load-bearing elements, and the specialist-track hand-off. Do *not* copy chapter-3 prose verbatim; rewrite for your specific org context.
- **The two cross-cutting slices** (observability, governance) as their own short section.
- **The two cited substrates** (compute substrate — platform-side principals; corporate substrate) named with pointer text, no ownership claim.
- **A "canonical API contract surface" section** naming the four contracts (feature / registry / eval-harness / inference-gateway) with a one-sentence purpose each and a link to `contracts/<name>/README.md`. The full contract detail is exercise-02.
- **A "publication cadence" section** (chapter 5 §2) naming the quarterly / semi-annual / annual refresh cycle and the two emergency triggers — with placeholder next dates.
- **A "how to consume this artifact" section** (chapter 5 § canonical-location checklist) with a short paragraph per audience: staff engineer, product engineer, peer principal.
- **A "review body" section** with the charter placeholder (exercise-04 fleshes it out) and a link to `review-log/`.
- **A "seams" section** with pointers to `seams/platform-side.md` and `seams/governance.md` (exercise-05 fleshes them out).
- **A pointer** to your mod-502 exercise-01 one-pager (real or fictional workspace path is fine — the purpose is to demonstrate the paired-artifact frame).

### The `CHANGELOG.md` — required

- One entry: `## v1.0 — <YYYY-MM-DD>` with a two-to-four bullet summary of what the artifact establishes.
- A "conventions" note at the bottom: patch / minor / major bump rules per chapter 5 §3.

### The `diagrams/` directory — required

- At minimum: `01-six-plane-band.<ext>` (source file in your chosen diagram-as-code tool), rendering as SVG or PNG, embedded in `README.md`. The diagram must be *generatable* from the source; a static image with no source is not a passing artifact.
- Optionally: `02-contract-surface.<ext>` if you want to include the second diagram now (exercise-02 will otherwise). One is required; two is fine.
- A note in the diagram file describing the notation you chose (C4, Mermaid flow, PlantUML classes, D2) — chapter 5 §4 discipline 3.

### The stubs for exercises 02–05 — required

- `contracts/{feature,registry,eval,gateway}/README.md` — three-to-five-sentence stubs, each linking to chapter 4 as the current spec until exercise-02 fleshes them out.
- `evolution-plan.md` — a stub with the five fixed sections from chapter 6 § *the evolution plan section in the artifact* (current-cycle bets, in-flight bumps, current support windows, deferred items, out-of-scope items) with placeholder rows.
- `seams/platform-side.md` and `seams/governance.md` — short stubs referencing chapter 8, listing the four platform-side seams and the three governance contracts by name.

## Starter guidance

- **Convergence first.** Before you write a word, pick your org and hold the chapter-1 property of *convergence* against your draft. If your instinct is to author a menu of options, throw the draft out; the artifact is a *choice*. Practice the chapter-1 five-property test on your draft twice before shipping v1.0.
- **Reuse the canonical shape unless you can defend a deviation.** Chapter 2 § *the canonical applied-ML architecture in three literatures* is your reference. If your draft has seven planes, or six planes but a different top-level decomposition, you must argue why in your `README.md`. Otherwise, match the shape and gain the vocabulary for free.
- **Diagram-as-code from the first line.** Do not draft the diagrams in Miro / PowerPoint / whiteboard and then "move them into code later". Half of the discipline is that the source and the rendered image travel together. Chapter 5 §4 discipline 1.
- **Rewrite the plane paragraphs for your org.** Chapter 3's prose is example prose; do not copy-paste. Every plane's paragraph in your `README.md` should reflect your specific org's canonical entities, freshness-tier reality, and hand-off partners.
- **The stubs are load-bearing.** The purpose of the stubs is to force the *shape of the artifact* — the fixed section list, the fixed directory, the fixed diagram set — before individual content lands. A well-shaped stub the review body can iterate on beats a rich narrative document with no shape.
- **Write the "how to consume this" section for a real reader.** Imagine a new staff engineer picking up the artifact on their second day and needing to know where to start. That paragraph is the mirror of how much the artifact will get used across the org.
- **Version conventions on day one.** Chapter 5 §3 semver-and-support-window discipline is not something you add "when the artifact is mature". It goes into the changelog conventions from v1.0.

## Acceptance criteria

Your artifact is done when it can pass all of the following:

- [ ] The artifact is a small git repo with the directory layout above.
- [ ] `README.md` carries all the required sections in order.
- [ ] The six-plane shape section names all six planes (chapter 3) with distinct paragraphs — not repeated prose, not a bullet list.
- [ ] The four canonical API contracts are listed with a one-sentence purpose each and a link to the stub.
- [ ] The publication cadence section names quarterly / semi-annual / annual refresh plus the two emergency triggers.
- [ ] The "how to consume this artifact" section addresses the three audiences separately.
- [ ] At least one `diagrams/` file exists as source (`.puml`, `.mmd`, `.d2`, or `.dot`) and renders. The rendered image is embedded in `README.md`.
- [ ] `CHANGELOG.md` has a `v1.0` entry and a written conventions note.
- [ ] All four contract stubs exist. The `evolution-plan.md` stub has the five fixed sections. The two `seams/` stubs list the substrate contracts and governance contracts by name.
- [ ] Nowhere in the artifact does named team-owner text, specific quarterly milestones, per-model architecture, or cluster topology appear as content. (Chapter 2 § *watch two altitude-slip failure modes*.)
- [ ] The artifact would fail if `git rm -rf` were run on the diagram source and the artifact were re-rendered — i.e., diagrams are not living without their source.

## Stretch goals

- **Publish the artifact as a docs site.** Use Docusaurus, Backstage TechDocs, mdBook, or MkDocs to render the repo. Note the trade-off (chapter 5 § the tooling stack) between the git repo (source of truth) and the docs site (consumer surface).
- **Add a second diagram.** The registry state-machine diagram (chapter 5 §4 discipline 2) is often the most-cited by product teams; adding it now saves a review-body item later.
- **Cite three case studies as your shape's grounding.** Pick three of Meta's *Applied Machine Learning at Facebook*, Uber's *Meet Michelangelo*, Airbnb's *Bighead*, Netflix's *Metaflow*, LinkedIn's *Feathr*, Pinterest engineering, and cite what your shape borrows from each in a brief "grounding" section of `README.md`.
- **Draft the mod-502 exercise-01 one-pager alongside.** The two artifacts pair (chapter 1 § *paired-artifact frame*). A pair drafted together typically stays coherent longer than either drafted alone.
- **Set up diagram-as-code CI.** A simple GitHub Action (or GitLab equivalent) that re-renders the diagrams on push and fails if the rendered image is stale. This is chapter-5-§4-discipline-1 in enforcement.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo — this is a per-learner artifact. When exercises 02–05 are complete, they populate the stubs; the pair of `README.md` + fleshed-out subdirectories is the deliverable this exercise ends with.
