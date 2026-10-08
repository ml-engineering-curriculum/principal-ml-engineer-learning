# exercise-04: Principal-Scope Open-Source Release Proposal

**Estimated effort:** 2 hours

## Objective

Author the full release-proposal artifact per chapter 5 for one candidate open-source release named in `exercise-01-industry-influence-artifact-plan/fiscal-year-artifact-bets.md`. Ratify (or self-simulate the ratification of) the four release-level decisions chapter 5 enumerates: *what to release vs. keep proprietary*, *the maintenance contract (seven commitments)*, *the north-star-alignment posture*, and *the exit / hand-off shape*. Produce the artifact in the shape chapter 5 § *the release-proposal artifact* names (10 sections, 5–15 pages).

The exercise instantiates chapter 5. It is the third of the three per-artifact exercises (02 for paper / blog, 03 for keynote, this one for open source) and sits deliberately at a shorter effort budget (2 hours) because the release proposal is a *decision document*, not a deeply authored narrative — the discipline is the four-decision clarity and the specificity of the seven maintenance commitments, not length.

The 2-hour effort target reflects the *first-draft proposal* scope, not the *ratified-and-launched* scope. A ratified open-source release is typically 2–4 months of pre-launch work (engineering, legal, security, docs, community), plus the multi-year maintenance commitment the proposal underwrites; this exercise gets you the proposal that the engineering director and CFO respond to.

## Prerequisites

- **Chapter 5 read end-to-end.** Especially the four release-level decisions, the six right-shape patterns and six wrong-shape patterns, the seven maintenance commitments, the north-star alignment stances (mirror / extend / diverge) with the two-implementations trap, the four exit shapes, the maintainership contract with peer specialist tracks, the 10-section release-proposal shape, and the eight failure modes.
- **Chapter 1 skim.** The venue-audience-artifact matching discipline underpins the open-source venue choice.
- **Chapter 2 skim.** Co-authorship discipline extends into the release proposal (the proposal is co-authored by the principal plus the designated maintainer bench).
- **Mod-503 chapter 3 and chapter 4.** The north-star architecture (chapter 3) is what the release aligns against; the canonical API contract (chapter 4) is often the surface that is a candidate for shape A (paved-road interface) release. If mod-503 chapters 3–4 are unfamiliar, the north-star-alignment decision will be hard to ground.
- **Mod-502 chapter 4 § *sunset criteria*.** The sunset-criteria discipline is lifted into chapter 5 § *commitment 7 (sunset criteria)* and § *decision 4 (exit / hand-off)*.
- **Peer specialist tracks skimmed.** Chapter 5 explicitly cedes commit-level maintainership craft to the peer tracks: [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning), [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning), [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning). The maintainer bench this proposal commits to is staffed from these tracks; skimming the maintainership chapters of at least one is enough to ground the maintainer-bench section.
- **Exercise-01 completed.** The release you draft is the one in your `fiscal-year-artifact-bets.md`. If exercise-01 is not yet done, do it first — this exercise's release scope and target return signals both live in that plan.
- **Optional: a candidate internal system identified.** If your fiscal-year bet points at a specific internal system or component as the release candidate, have the system's internal reference doc (mod-503 chapter 5) open. If not, use a composite system (the paved-road feature-registry, the cross-team eval harness, the FM-cost-sensitivity benchmark) and state the composite framing explicitly in `README.md`.

## Problem statement

Pick one fiscal-year bet from `exercise-01-industry-influence-artifact-plan/fiscal-year-artifact-bets.md` whose venue class is open source. Author the full release proposal per chapter 5's shape. The proposal is the single artifact the engineering director and CFO sign off on; without it (or without the ratifications it collects), the release does not ship — chapter 5 failure mode: *the unratified maintenance contract* is what un-proposed releases turn into.

Three constraints on the choice.

- The release must fit one of chapter 5's six right-shape patterns (paved-road interface not implementation, eval harness not eval data, benchmark not private extension, reference implementation of an internal invariant, tool that is not the competitive edge, graduated experiment). If it fits none, either reshape the release to fit or defer the bet. Chapter 5 § *decision 1 — what to open source vs. keep proprietary* is the test.
- The release must have a *named internal use case* that will exercise the code path in production. Chapter 5 § *shape ζ — the "just for the community" release with no internal use case* is a wrong-shape; releases without internal use are the modal path to chapter 5 failure mode: *the vanity release*.
- The maintenance contract must be ratifiable — meaning the headcount commitment (engineering director) and the multi-year budget (CFO) are plausible asks within the org's current fiscal picture. A proposal with an unratifiable contract fails at the first review; chapter 5 failure mode: *the unratified maintenance contract* is what unratified contracts turn into.

Produce the release proposal in the chapter 5 § *the release-proposal artifact* shape (10 sections), plus the maintainership-contract hand-off document, plus the exit-shape pre-commit.

## Requirements

Populate a workspace directory `exercise-04-release-proposal/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-04-release-proposal/
├── README.md                             # index; which bet from exercise-01; release scope
├── release-proposal.md                   # the 10-section canonical artifact
├── maintainership-handoff.md             # chapter 5 § *maintainership contract* detailed
├── exit-shape-pre-commit.md              # chapter 5 § *decision 4* detailed exit plan
├── north-star-alignment-audit.md         # chapter 5 § *decision 3* two-implementations check
└── appendices/
    ├── right-shape-vs-wrong-shape.md     # the shape audit (which pattern, why)
    ├── not-released-list.md              # chapter 5 § *what is deliberately not being released*
    └── legal-review-checklist.md         # trademark, patent, CLA / DCO, third-party audit
```

### `README.md` — index

Half a page. States:

- Which bet from exercise-01 this exercise instantiates. Reference `fiscal-year-artifact-bets.md` bet ID.
- The release's working name and one-sentence description.
- Which of chapter 5's six right-shape patterns it fits (named explicitly).
- The internal system or component the release is extracted from (reference the internal reference doc from mod-503 chapter 5; composite is fine, state that explicitly).
- The named internal use case that will exercise the code path in production (chapter 5 § *shape ζ* guard).
- The engineering director and CFO who would ratify the proposal (named; composite roles are fine).
- The target launch date and the current pre-launch work estimate (modal: 2–4 months of pre-launch engineering + legal + docs + community infrastructure).

### `release-proposal.md` — the 10-section canonical artifact

Chapter 5 § *the release-proposal artifact* is the content. 5–15 pages (chapter 5 target). Reproduce all 10 sections, each populated with specifics.

- **Section 1 — What is being released.** One paragraph. The system, the interface, the substrate. What a potential adopter would clone or install. State the modality (new standalone repo, upstream contribution to an existing project, benchmark submission, standards-body contribution).
- **Section 2 — Which of the six right-shape patterns it fits.** Explicitly named. One paragraph justifying the fit. If the release does not cleanly fit one of the six, the proposal must defend the fit against the six wrong-shapes.
- **Section 3 — What is deliberately not being released.** The proprietary edge, the customer-data-touching code, the internal-only conventions. Named explicitly. Chapter 5 § *decision 1* six wrong-shapes are the taxonomy; this section cross-references `appendices/not-released-list.md` where applicable.
- **Section 4 — The maintenance contract.** All seven commitments from chapter 5 § *decision 2* filled in with specifics:
  1. **Release cadence** (specific point / minor / major cadence, with dates or quarters).
  2. **Security-patch SLA** (specific days-from-disclosure for standard and critical severity).
  3. **Breaking-change policy** (specific deprecation-and-removal cycle length; semver stance; migration-guide obligation).
  4. **Deprecation horizon** (specific minimum deprecation duration before removal; notice pathway).
  5. **Community-response SLA** (specific first-response-time targets for issues and PRs).
  6. **Maintainer bench** (named maintainers — not just a headcount; chapter 5 § *commitment 6*).
  7. **Sunset criteria** (specific signals that would reduce commitment or trigger an exit per § *decision 4*).
- **Section 5 — The north-star alignment posture.** Mirror / extend / diverge, named explicitly. If *extend* or *diverge*, the specific alignment discipline (test surfaces coupled, cadence coupling, PR-acceptance criteria that require internal use case). The two-implementations-trap guard is cross-referenced to `north-star-alignment-audit.md`.
- **Section 6 — The maintainer bench.** The named maintainers from the peer specialist tracks. For each: name (or role-composite), seniority altitude (L30 / L40 / L50), committed time-percentage (modal: 20–50% for a named maintainer; 100% is a product team, not a maintainer bench), and the engineering director's ratification signature line. 2 maintainers minimum, 3+ is a healthy bench. The principal's name does *not* appear here — chapter 5 § *the principal-as-maintainer trap* failure mode is what principal-as-maintainer looks like.
- **Section 7 — The budget line.** Multi-year commitment, typically 3 years. For each year: the headcount cost (maintainer time-percentage × loaded cost), the infrastructure cost (hosting the repo, running CI, hosting docs, running the community call), the community cost (conference travel, swag, contributor-event sponsorship). The CFO's ratification signature line. Chapter 5 § *the unratified maintenance contract* failure mode is what un-CFO-ratified budgets turn into.
- **Section 8 — The exit shape.** Named upfront per chapter 5 § *decision 4* (graduation to a foundation / donation to a standards body / archival / continuous stewardship). The specific criteria that would move the release toward the named exit are listed; cross-reference to `exit-shape-pre-commit.md`.
- **Section 9 — The community-governance model.** The committer criteria (how someone becomes a committer), the decision process (lazy consensus, BDFL-style single-maintainer veto, formal RFC process, voting rules — pick one and justify), the code-of-conduct posture (adopt Contributor Covenant or an equivalent; name it), the contribution licence (modal choices: Apache-2.0, MIT, BSD-3-Clause for permissive; or MPL-2.0, LGPL for weak-copyleft — pick one and justify against the org's IP posture), the CLA / DCO decision (which one; why).
- **Section 10 — The legal review.** Trademark check status, patent-encumbrance check status, CLA / DCO decision ratification, third-party-code audit status. Signed off by legal counsel (named — real or role-composite). Cross-reference to `appendices/legal-review-checklist.md` where the per-check status is maintained.

Each section is a *decision document*, not an exposition. The reviewer (engineering director / CFO / legal counsel) reads the section to confirm the specific commitment is defensible, not to be educated on open-source practice.

### `maintainership-handoff.md` — the contract with the peer specialist tracks

Chapter 5 § *the maintainership contract with the peer specialist tracks* is the content. 1 page.

The handoff document is the explicit contract between the principal (who owns the release-level decisions) and the maintainer bench (who owns the commit-level maintainership). Structure as two columns.

- **Column A — what the principal brings.** Chapter 5 § *the maintainership contract* enumerates five items: the release proposal, sponsorship of the maintainer bench (headcount + budget), alignment with the internal north-star architecture, escalation authority, retirement authority. Each item has a one-sentence operational cadence (e.g., *"escalation authority: available within 48 hours when any maintainer surfaces a chapter 5 § *the escalation seam* item"*).
- **Column B — what the peer specialist maintainers bring.** Chapter 5 § *the maintainership contract* enumerates five items: day-to-day PR review and release cutting, community engagement, security response coordination, documentation and tutorial authorship, migration-guide authorship. Each item has a one-sentence operational cadence.
- **The 1:1 cadence.** Modal: monthly or quarterly principal-to-maintainer 1:1 focused on the release-level questions (contract holding, alignment invariants intact, sunset criteria approaching). Named by date-pattern (e.g., *"first Tuesday of each quarter"*).
- **The annual review.** Chapter 5 § *the maintainership contract's cadence* annual release-level review focused on decision 4 (exit revisit). Named by date-pattern.
- **The escalation seam.** The specific list of items that *always* escalate to the principal within days: major architectural change, breaking-change with contested community response, security-response gone sideways, fork threat. For each: the principal's response SLA and the resolution forum.

### `exit-shape-pre-commit.md` — the named exit at launch

Chapter 5 § *decision 4 — exit / hand-off* is the content. Half a page to 1 page.

- **The named exit shape.** One of four: *graduation to a foundation* / *donation to a standards body* / *archival* / *continuous stewardship*. Named explicitly.
- **The criteria that trigger the exit.** For each criterion, a specific observable signal (e.g., *"when 3+ committer orgs contribute 20%+ of commits each over 2 consecutive quarters, graduation to CNCF is reviewed"* or *"when internal-use coverage drops below 50% of internal consumer teams for 2 quarters, archival is reviewed"*). The criteria map to chapter 6 § *retirement criteria — trigger 4 (maintenance cost exceeded return)* for the OSS-specific case.
- **The hand-off path.** If the exit is graduation or donation, the specific target (CNCF Incubation, Linux Foundation project, Apache Software Foundation Incubator, MLCommons working group, ONNX operator submission, OpenTelemetry ML extension). State the sponsor relationship if any.
- **The archival plan.** If the exit is archival, the plan for the *"why we archived"* post, the successor pointer or alternative project pointer, and the maintenance posture for critical security patches post-archive (modal: 12 months of security-only patches, then full archive).
- **The re-audit cadence for continuous stewardship.** If the exit is continuous stewardship (the legitimate "not yet" exit), the annual re-audit cadence per chapter 6 § *retirement criteria* trigger 4.

Named exits are what distinguish *retired* from *dead* — chapter 5 § *decision 4* and chapter 6 § *retirement criteria — explicit, not passive* are both the parent discipline.

### `north-star-alignment-audit.md` — the two-implementations-trap guard

Chapter 5 § *decision 3 — north-star-alignment decision* and § *the two-implementations trap* are the content. 1 page.

- **The alignment posture stated.** Mirror / extend / diverge. Match section 5 of `release-proposal.md`.
- **The internal consumer map.** List the internal teams or systems that will consume the public release as a dependency (not a fork). Each entry: team name (role-composite is fine), the API surface they use, the acceptance posture (consume-as-dependency / consume-as-forked-copy / to-be-migrated-to-consume-as-dependency). If any internal consumer is on the *forked-copy* line, the alignment posture is already drifting; the proposal states the specific migration plan to pull them onto the public release.
- **The cadence coupling.** State how the release's cadence is coupled to the internal system's evolution cadence (chapter 5 § *the two-implementations trap* fix: *"the release's cadence is coupled to the internal system's evolution cadence, not decoupled from it"*). If the internal system version-bumps on an 8-week cycle, the release's point-release cadence matches; if the internal system is on a quarterly cycle, so is the release.
- **The PR-acceptance criterion.** Chapter 5 § *the two-implementations trap* fix: *"community PRs the org accepts have to have an internal use case that will exercise them"*. State the specific criterion: a community PR is accepted only when there is an internal team that will adopt the new feature in the next 1-2 internal release cycles. The criterion is restrictive — most community PRs are rejected or deferred under it. The restriction is the point; chapter 5 § *the two-implementations trap* is what accepting unaligned PRs produces.
- **The audit cadence.** Quarterly audit of the alignment drift. State the specific signals (number of release features not consumed internally; number of internal features not released publicly; count of consumer teams on forked copies). The audit feeds chapter 6 § *the tracking dashboard* internal-leverage column for the OSS release.

### `appendices/right-shape-vs-wrong-shape.md` — the shape audit

Half a page. Chapter 5 § *decision 1* six right-shapes and six wrong-shapes are the taxonomy; this appendix walks the audit.

- **The right-shape fit.** Which of the six right-shapes the release fits (A paved-road interface / B eval harness / C benchmark / D reference implementation of invariant / E tool orthogonal to competitive edge / F graduated experiment). One paragraph justifying the fit, with the specific internal evidence that the pattern has stabilised across multiple internal consumers (shape A test), that the eval data stays internal (shape B test), that the proprietary extensions stay internal (shape C test), that the invariant is non-negotiable (shape D test), that the tool is orthogonal (shape E test), or that the project no longer needs org-primary maintainership (shape F test).
- **The wrong-shape audit.** For each of the six wrong-shapes (α model weights / β internal-tools codebase / γ customer-data-touching code / δ proprietary edge / ε pre-stable API / ζ "just for the community" release with no internal use case), state one sentence confirming the release is not one of them. If any wrong-shape is a plausible read of the release, the release proposal must defend why (e.g., *"the release includes model weights, but the strategic-differentiation move has explicit board + CFO sign-off per section 7"*).

### `appendices/not-released-list.md` — what stays proprietary

Half a page. Chapter 5 § *decision 1 — what is deliberately not being released* is the content.

An explicit list of what is deliberately *not* in the release, with the reason for each. Shapes:

- **The proprietary edge.** The specific algorithm, model architecture, or system optimisation that is *the reason* the org competes on this axis. Named.
- **The customer-data-touching paths.** Specific code paths that touch customer data or that assume specific customer-data schemas. Named.
- **The internal-only conventions.** Code written with internal-only assumptions, naming, dependencies, or testing. If the release pre-launch has done a *decoupling pass* on these, state what the pass removed; if not, the release is not yet ready (chapter 5 shape β failure).
- **The vendor / partner contractual encumbrances.** Specific vendor APIs, foundation-model provider interfaces, or partner-contracted code paths that cannot be released. Chapter 3 § *contractual encumbrance* legal review is the discipline.

The not-released-list is as load-bearing as the released-list. Chapter 5 § *the proprietary-edge leak* failure mode is what unauthored not-released-lists produce.

### `appendices/legal-review-checklist.md` — the pre-launch legal pass

Half a page. Chapter 5 § *section 10 — the legal review* content expanded.

- **Trademark check.** Is the release name legally clear (not infringing an existing trademark; the org has filed or does not need to file for the name)? Current status: cleared / needs filing / needs rename.
- **Patent-encumbrance check.** Does the release implement patented methods owned by the org (if so, the licence must include a patent grant — modal: Apache-2.0 provides this; MIT does not) or by third parties (if so, the release's dependency chain must be audited)? Current status.
- **CLA vs. DCO decision.** Contributor Licence Agreement (modal for corporate-stewarded projects — requires contributors to sign) or Developer Certificate of Origin (modal for Linux-kernel-style projects — in-commit sign-off; lower friction, less legal coverage). Pick one; state why.
- **Third-party-code audit.** Does the release vendor any third-party code? If so, the licences must be compatible with the release's licence; the attribution and NOTICE requirements must be met; copyleft code (GPL, LGPL under certain conditions) requires special handling.
- **Export-control check.** Does the release touch export-controlled technology (strong cryptography, certain ML models)? Status.
- **Legal-counsel sign-off.** Name of the legal counsel reviewing; sign-off date target; sign-off conditional on resolution of any open checks above.

## Starter guidance

- **Author the shape audit (`appendices/right-shape-vs-wrong-shape.md`) first.** If the release does not fit one of chapter 5's six right-shapes, the proposal has nothing to defend. Starting with the shape audit catches wrong-shape releases before the proposal effort is wasted.
- **The maintainer bench is named, not notional.** Chapter 5 § *the principal-as-maintainer trap* failure mode is modal. The bench is 2+ named maintainers from the peer specialist tracks, each with a committed time-percentage and the engineering director's name on the ratification line. Nameless benches are unratified; unratified benches evaporate at the first budget cycle.
- **The CFO signature is non-negotiable.** Chapter 5 § *the unratified maintenance contract* failure mode is what un-CFO-ratified budgets turn into. Even in the exercise, name the specific CFO or finance-partner role, state the multi-year budget ask in rough dollars (headcount + infra + community), and name the signature-pending status. A proposal that cannot be CFO-ratified is a proposal that should not ship.
- **The not-released-list is as load-bearing as the released-list.** The modal first-draft release proposal has an elaborate released-list and a cursory not-released-list. The reverse is better signal. The engineering director reading the proposal checks the not-released-list first to confirm the proprietary edge is protected.
- **Pick the alignment posture before the maintenance contract.** Chapter 5 § *decision 3* (alignment) shapes chapter 5 § *decision 2* (maintenance contract) — a diverge posture requires more maintainer time than a mirror posture, which inflates the budget line. Picking the alignment first makes the maintenance contract's size defensible.
- **The exit shape is named at launch, not later.** Chapter 5 § *the no-exit release* failure mode is what unauthored exits produce. Even a *continuous stewardship* exit is a named exit — it names the annual re-audit cadence that confirms it is still the right posture.
- **The two-implementations trap is upfront-preventable, not detectable-later.** The `north-star-alignment-audit.md` is the trap guard; the PR-acceptance criterion (community PRs require an internal use case) is restrictive by design. The pressure to relax the criterion is constant; the proposal's job is to make the relaxation visible.
- **The licence choice is not an afterthought.** Apache-2.0, MIT, BSD-3-Clause, MPL-2.0, LGPL — each has different implications for the org's IP posture, the community-contribution model, and the downstream users' ability to integrate. The chapter 5 § *section 9 — the community-governance model* names the licence as a decision requiring a one-sentence justification; the exercise authors that justification explicitly.
- **Time-box each section.** README: 10 minutes. Release proposal (10 sections): 60 minutes (this is the load-bearing section). Maintainership handoff: 15 minutes. Exit-shape pre-commit: 10 minutes. North-star-alignment audit: 15 minutes. Shape audit appendix: 5 minutes. Not-released-list appendix: 5 minutes. Legal-review checklist appendix: 5 minutes. Total ~2 hours; cut appendix depth before cutting proposal section depth.

## Acceptance criteria

The exercise is done when:

- [ ] `README.md` names the exercise-01 bet, the release working name, the right-shape pattern, the internal system, the named internal use case, and the engineering director + CFO ratifiers.
- [ ] `release-proposal.md` reproduces all 10 chapter 5 sections.
- [ ] Section 1 states what is being released as a one-paragraph description plus modality (new repo / upstream contribution / benchmark submission / standards contribution).
- [ ] Section 2 names which of the six right-shape patterns the release fits (A / B / C / D / E / F), with a one-paragraph justification.
- [ ] Section 3 names what is deliberately not being released. The not-released-list is non-trivial (not just *"everything proprietary"* — the specific proprietary edges, customer-data paths, and internal-only conventions are enumerated).
- [ ] Section 4 fills in all seven maintenance commitments with specific numeric or named values. No *"TBD"* placeholders.
- [ ] Section 5 names the alignment posture (mirror / extend / diverge). If extend or diverge, the alignment discipline is specified.
- [ ] Section 6 names 2+ specific maintainers (name or role-composite) with committed time-percentages and the engineering director's ratification signature line. The principal is not on the maintainer bench.
- [ ] Section 7 names the multi-year budget line (headcount + infrastructure + community costs) with the CFO's ratification signature line.
- [ ] Section 8 names one of the four exit shapes with specific trigger criteria.
- [ ] Section 9 names the committer criteria, the decision process, the code-of-conduct, the contribution licence, and the CLA / DCO decision — all with one-sentence justifications.
- [ ] Section 10 names the trademark, patent-encumbrance, third-party-code audit, and sign-off status.
- [ ] `maintainership-handoff.md` reproduces chapter 5 § *the maintainership contract* two-column shape (principal column + maintainers column), the 1:1 cadence, the annual-review cadence, and the escalation-seam enumerated list.
- [ ] `exit-shape-pre-commit.md` names the exit shape, the specific trigger criteria (each is an observable signal), and the hand-off path or archival plan or continuous-stewardship re-audit cadence.
- [ ] `north-star-alignment-audit.md` names the alignment posture, the internal-consumer map (with per-consumer posture: dependency / forked / to-be-migrated), the cadence coupling, the PR-acceptance criterion, and the audit cadence.
- [ ] `appendices/right-shape-vs-wrong-shape.md` audits all six right-shapes (naming the fit) and all six wrong-shapes (confirming the release is not one of them).
- [ ] `appendices/not-released-list.md` enumerates the specific proprietary edges, customer-data paths, internal-only conventions, and vendor / partner encumbrances deliberately kept proprietary.
- [ ] `appendices/legal-review-checklist.md` runs all five legal-review checks (trademark / patent / CLA-or-DCO / third-party / export-control) with per-check current status plus the legal-counsel sign-off line.
- [ ] The proposal passes the *CFO-ratifiability test*: a CFO reading section 7 can state the multi-year budget commitment and whether it is approvable within the current fiscal picture. If the budget is undefined or unapprovable, the proposal is not yet ready.
- [ ] The proposal passes the *engineering-director-ratifiability test*: an engineering director reading section 6 can state the headcount commitment and whether the maintainer bench is adequately staffed. If the bench is thin or notional, the proposal is not yet ready.
- [ ] The proposal passes the *chapter-5-failure-mode audit*: none of the eight failure modes (open-source dump, two-implementations trap, proprietary-edge leak, principal-as-maintainer trap, unratified maintenance contract, no-exit release, vanity release, contribution-licence oversight) are visible in the proposal.
- [ ] The proposal passes the *hand-off test*: a maintainer from one of the peer specialist tracks (senior-ml-engineer, ai-infra-ml-platform, training-pipeline-engineer, etc.) reading `maintainership-handoff.md` and `release-proposal.md` can start their maintainership role without further walkthrough.

## Stretch goals

- **Draft the launch blog post.** Chapter 3 § *shape of the applied-ML engineering blog post* applied to the launch announcement. 2,000–4,000 words. The launch blog is the chapter 4 § *the take-away artifact* that often pairs with the open-source release as a keynote's take-away (exercise-03 cross-links here if the fiscal-year bet pairs them).
- **Draft the one-year retro — in advance.** 1 page. Imagine the release has been live for 12 months; write the retro you would wish to have written. What landed, what did not, what the maintenance-cost delta is (chapter 5 § *the two-implementations trap* audit), whether the alignment posture is holding, whether the sunset criteria are approaching. Writing the retro in advance is a form of pre-mortem — it surfaces where the proposal is still unsure.
- **Draft the fork-threat response.** One of the chapter 5 § *the escalation seam* items. 1 page. The specific response to a credible fork threat: how the principal engages with the forkers, what concessions are on the table, what the alignment posture becomes if the fork succeeds. Fork threats are rare but material; the proposal's resilience to a fork is a signal of its upfront-alignment discipline.
- **Draft the first security-disclosure response.** Chapter 5 § *commitment 2 (security-patch SLA)* in action. 1 page. The specific protocol for the first critical-severity disclosure that will arrive: the private-disclosure channel, the triage SLA, the maintainer-bench escalation, the patch-and-release timeline, the public disclosure post. The protocol is what the SLA actually requires at operational level.
- **Compose with exercise-02.** If exercise-02's draft is a paper or blog that the release pairs with (the paper announces the release; the blog documents the pattern the release reifies), add explicit cross-links: `release-proposal.md` section 10 cites the paper / blog as the published substrate; exercise-02's `draft.md` references the release's canonical repo URL.
- **Compose with exercise-03.** If exercise-03's keynote has the release as its take-away artifact (chapter 4 § *the take-away artifact* shape *open-source release or reference repo*), confirm that this exercise's maintenance contract is ratified *before* exercise-03 commits to the release as the take-away. Chapter 5 § *the open-source dump* failure mode is what unratified take-aways produce.
- **Draft the standards-body-submission plan.** If the release is a benchmark (shape C), a protocol (adjacent to shape D), or a reference implementation of an invariant (shape D), state the specific standards body (MLCommons, ONNX, OpenTelemetry, CNCF ML SIG) and the submission path. Chapter 5 § *exit B — donation to a standards body* is often the right exit for shape-C and shape-D releases from the start.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-04-release-proposal/` is what you extend across the release's multi-year lifecycle: the release proposal is revised annually per chapter 5 § *canonicalised in the mod-503 chapter 5 canonical-doc location, revised annually per chapter 6 § *retirement criteria*; the maintainership-handoff is the standing contract the principal-to-maintainer 1:1 cadence operates against; the exit-shape pre-commit is the document chapter 6 § *retirement criteria trigger 4* reads against annually. The release's tracking-dashboard row (exercise-01) is populated quarterly from the alignment-audit's cadence.
