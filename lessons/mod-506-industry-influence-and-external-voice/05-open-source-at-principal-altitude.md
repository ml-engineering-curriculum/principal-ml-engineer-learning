# Open Source at Principal Altitude — Release-Level Decisions, the Maintenance Contract, and Alignment With the North Star

> Chapter 5 of mod-506. Prerequisite: chapter 1 (venue-audience-artifact discipline), chapter 2 (internal-first substrate), and mod-503 chapter 4 (canonical API contract surface). Downstream: exercise-04 authors the release-level plan for one open-source contribution. Interacts with the peer specialist tracks (`senior-ml-engineer-learning`, `training-pipeline-engineer-learning`, `ai-infra-ml-platform-learning`) which own the day-to-day commit-level maintainership craft this chapter deliberately does *not* re-teach.

## What the principal owns and does not own in open source

The peer specialist tracks own the *commit-level* open-source craft — writing the PR, reviewing the peer's PR, running the CI, cutting the release, publishing the changelog, running the community Discord. Those are load-bearing crafts and specific tracks teach them at depth. See in particular [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) for the individual-maintainer craft and [`ai-infra-ml-platform-learning`](https://github.com/ai-infra-curriculum/ai-infra-ml-platform-learning) for the platform-side maintainer craft.

The principal owns the *release-level* decisions that sit above those crafts. Four decision classes.

- **The what-to-open-source-vs-keep-proprietary decision.** Which internal system or component gets released, which stays internal, and why. This is a strategy decision, not a code decision.
- **The maintenance-contract decision.** What the org commits to on the maintenance burden — cadence of releases, security-patch SLA, breaking-change policy, deprecation horizon, community-response SLA. This is a resource-commitment decision the CFO and the engineering director need to underwrite.
- **The north-star-alignment decision.** Whether the open-source release mirrors the internal reference architecture (mod-503 chapter 3), extends it, or diverges from it — and the implications for internal maintenance if the two drift.
- **The exit / hand-off decision.** How the release ends — whether it graduates to a foundation, gets donated to a standards body, gets archived, or continues indefinitely.

These four decisions are all made *before* the release ships. The rest of this chapter walks each.

## Decision 1 — what to open source vs. keep proprietary

The default posture is *keep proprietary*. Not because open source is bad but because the open-source release is a *multi-year commitment* the org has to underwrite, and most internal ML systems are not the right shape for that commitment. The principal's job is to identify the specific subset that is.

Six shapes tend to be right for open-sourcing.

- **Shape A — the paved-road interface, not the implementation.** The API contract the org's ML platform exposes internally is a candidate; the implementation behind it usually is not. The public artifact is the *interface* other orgs can implement against; the private artifact is the specific implementation that competes on operational excellence. Mod-503 chapter 4 § *the canonical API contract surface* is the internal substrate — the surface that maps well to a public release is the surface that has stabilised across multiple internal consumers.
- **Shape B — the evaluation harness, not the evaluation data.** A cross-team eval program (mod-505 chapter 2 § *Class D*) often produces an eval harness that generalises across orgs. Releasing the harness (the framework, the metric definitions, the test-runner) makes the industry more productive. The specific eval *data* (the labelled sets, the proprietary regression suite) usually stays internal.
- **Shape C — the benchmark, not the benchmark's private extension.** A benchmark the org has built and validated for its internal use often generalises: MLPerf-style throughput benchmarks, HELM-style evaluation suites, MTEB-style embedding benchmarks, MLCommons submissions. The public benchmark is what the industry converges on; the org's private extensions (proprietary tasks, customer-specific test sets) stay internal.
- **Shape D — the reference implementation of an internal invariant.** When the internal north-star architecture has ratified a non-negotiable invariant (e.g., three-tier data-tier discipline, per mod-503 chapter 4), releasing a reference implementation of that invariant helps the industry adopt it and — a load-bearing second-order effect — makes it easier for the org to hire staff-plus engineers who already understand the invariant.
- **Shape E — the tool that is not the org's competitive edge.** Utilities the org built to support its ML work but that are orthogonal to what makes the org competitive: data-labelling tooling, feature-quality dashboards, model-serving edge-case handlers, migration utilities. The tool works well enough for the org's use; releasing it lowers the industry's floor without giving away the ceiling.
- **Shape F — the graduated experiment.** A project the org built and used successfully and no longer needs to be the primary maintainer of. The org donates the project to a foundation (CNCF, Linux Foundation, Apache) and continues as a contributor rather than the maintainer. This is chapter 5 § *decision 4 — exit / hand-off* landing at the initial release.

Six shapes tend to be wrong for open-sourcing.

- **Shape α — the model weights themselves.** Unless the release is a strategic-differentiation move (a *"we open-source our foundation model"* bet with explicit board and CFO sign-off), the model weights are the proprietary artifact. Frontier-model orgs have specific stances on this; the modal principal-scope decision is *no*.
- **Shape β — the internal-tools codebase.** Code written for internal-use with internal-only conventions, internal-only assumptions, and internal-only test coverage. Releasing it produces a maintenance nightmare — external users file issues about internal-only behaviours; the org's engineers spend time defending internal-only design decisions to external users. Named as *the open-source dump* in chapter 1 failure mode 5.
- **Shape γ — the customer-data-touching code.** Code paths that touch customer data or that assume specific customer-data schemas. The privacy and contractual-encumbrance surface is too large; the release fails legal review.
- **Shape δ — the proprietary edge.** The specific algorithm, model architecture, or system optimisation that is *the reason* the org competes on this axis. Releasing it hands the differentiator to competitors for no compensating industry benefit.
- **Shape ε — the pre-stable API.** An interface that has not yet stabilised internally across multiple consumers. Releasing it means every internal breaking change is now a public breaking change; the maintenance cost multiplies.
- **Shape ζ — the "just for the community" release with no internal use case.** Code the org built specifically to open-source and does not itself use in production. Signal-quality decays because the org has no vested interest in maintenance; the release ends up as chapter 1 § *the open-source dump*.

The what-to-release decision is captured in a *release proposal* the principal authors and the engineering director and CFO ratify. Exercise-04 walks the shape.

## Decision 2 — the maintenance-contract decision

Every open-source release is a *multi-year commitment*. The maintenance contract is the specific commitment.

**Commitment 1 — cadence of releases.** The org commits to a release cadence: point-release cadence (monthly, quarterly), minor-release cadence (quarterly, semi-annually), major-release cadence (annually, biennially). The cadence is what downstream users plan against.

**Commitment 2 — security-patch SLA.** When a security vulnerability is reported (privately, through a security disclosure channel the release publishes), the org commits to a fix and release timeline. Modal: 90 days from private disclosure to public patch for standard-severity; 30 days for critical-severity. The SLA is enforced by the org's security team and cannot be missed without material community trust cost.

**Commitment 3 — breaking-change policy.** The rules for API breaking changes: deprecation-and-then-removal cycles (typically 6–12 months of deprecation warning before removal), semantic-versioning discipline, migration-guide obligation. A breaking change without a deprecation cycle is a community-trust incident.

**Commitment 4 — deprecation horizon.** How long a feature marked deprecated persists before removal, and the notice pathway (release notes, in-code warnings, blog post). Two release cycles of deprecation before removal is a reasonable floor; more for foundational APIs.

**Commitment 5 — community-response SLA.** How long an issue or a PR waits for a maintainer's first response. Modal: 1–2 weeks for an issue's triage response, 2–4 weeks for a PR's first review comment. Not resolution — just response. A repo with month-plus first-response times signals abandonment even when the maintainers are technically active.

**Commitment 6 — the maintainer bench.** How many *named* maintainers the org commits to, at what altitude, at what cadence. Two maintainers minimum (one is a bus-factor risk); three-plus is a healthy bench. The principal is not one of the maintainers — the principal's role is to sponsor the maintainer bench, not to run the day-to-day work.

**Commitment 7 — the sunset criteria.** The signals that would cause the org to reduce commitment or exit maintenance. Mod-502 chapter 4 § *sunset criteria* applies at the OSS release layer too. The sunset is *pre-committed*; when the criteria fire, the exit executes per decision 4 below rather than through a slow-fade abandonment.

The maintenance contract is authored by the principal, sponsored by the engineering director (who commits the headcount), and — critically — ratified by the CFO (who commits the multi-year budget). Without CFO ratification the maintenance contract is aspiration; the sunset criteria fire on schedule (the promising release from three years ago that now has no maintainers) rather than on merit.

## Decision 3 — north-star-alignment decision

The open-source release either mirrors the internal north-star architecture (mod-503 chapter 3), extends it, or diverges from it. Each choice has an implication for internal maintenance cost.

- **Mirroring.** The open-source release is the same shape as the internal system. Internal consumers use the OSS release as-is or as-a-thin-wrapper. Maintenance cost stays low because there is one implementation. This is the modal principal-scope pattern for shape A (paved-road interface) and shape D (reference implementation of invariant).
- **Extending.** The open-source release is a superset of the internal system — the internal system uses a subset of the public API, and the public API supports additional cases the org's internal system does not. Maintenance cost is moderate because the org tests the internal-use subset thoroughly but relies on community reports for the extended cases. This is the modal pattern for shape B (eval harness) and shape C (benchmark).
- **Diverging.** The open-source release has drifted from the internal system — new features are added publicly that the internal system does not consume, or the internal system has added features that the public release does not have. Maintenance cost is *high*: two implementations to keep coherent, two test surfaces, two documentation surfaces. Chapter 5 § *the two-implementations trap* below is the pattern to avoid.

The alignment decision is not a one-time choice; it is a continuous discipline. The internal system evolves; the public release evolves; the two need active alignment work. Mod-503 chapter 6 § *evolution plan and version-bump triggers* is the internal-substrate cadence the public release aligns against.

### The two-implementations trap

Six months after release, the internal system has added three features the public release does not have (marketing-visible internal wins the org has not been ready to release publicly). The public release has added four features the internal system does not consume (community PRs the org accepted without a matching internal use case). The two are now diverged.

The trap tightens on the next major version. The public release plans a v2.0 breaking-change cycle that will require the internal consumers to migrate too — but the internal system has been building against the diverged v1.x line, and the migration cost is now real internal work.

The fix is *upfront alignment discipline*: the internal system consumes the public release as-a-dependency, not as-a-fork; the community PRs the org accepts have to have an internal use case that will exercise them; the release's cadence is coupled to the internal system's evolution cadence, not decoupled from it. This is expensive and the temptation to fork is real; the temptation is the failure mode.

## Decision 4 — exit / hand-off

Every release has an exit. Four modal exit shapes.

- **Exit A — graduation to a foundation.** The project matures to the point where it is genuinely community-owned (multiple committer orgs, a diverse committer base, an independent governance body). The org donates the project to a foundation (CNCF, Linux Foundation, Apache Software Foundation) and continues as a contributor rather than the sole steward. This is the modal *successful* exit.
- **Exit B — donation to a standards body.** For releases that are inherently standards-shaped (a benchmark, a protocol, an API contract), the exit is to a standards body (MLCommons for benchmarks, W3C for web-adjacent standards, IETF for protocols). The org continues to contribute to the standard but no longer owns the implementation.
- **Exit C — archival.** The project has fulfilled its purpose and no longer justifies maintenance. The org marks the repository as archived, publishes a *"why we archived"* post, and points users to the successor or the alternative. Named archival is more trustworthy than slow-fade abandonment.
- **Exit D — continuous stewardship.** The project is genuinely load-bearing for the org's internal use and the community depends on the org's continued maintenance. The exit is *not-yet*; the release continues indefinitely. This is a legitimate posture but should be re-audited annually per chapter 6 § *retirement criteria*.

The exit is planned at the release proposal, not after two years of drift. Every release proposal names the expected exit shape and the criteria that would move the release toward it. The release without a named exit becomes chapter 1 failure mode 5's open-source dump slowly, over years.

## The maintainership contract with the peer specialist tracks

The principal does not maintain the release day-to-day. The peer specialist tracks do. The interface between the two is a *maintainership contract*.

**What the principal brings.**

- The release proposal (decisions 1–4 above).
- Sponsorship of the maintainer bench (headcount commitment from the engineering director; budget commitment from the CFO).
- Alignment with the internal north-star architecture (mod-503 chapter 3).
- Escalation authority when the release is under threat (a departing maintainer, a security incident, a breaking-change dispute the community cannot resolve).
- Retirement authority (the exit decision per decision 4).

**What the peer specialist maintainers bring.**

- Day-to-day PR review, issue triage, and release cutting.
- Community engagement (Discord / Slack, community calls, contributor onboarding).
- Security response coordination.
- Documentation and tutorial authorship.
- Migration-guide authorship on breaking changes.

**The contract's cadence.** Modal: monthly or quarterly principal-to-maintainer 1:1 focused on the release-level questions (is the maintenance contract holding, are the alignment invariants intact, are the sunset criteria approaching); annual release-level review focused on decision 4 (should the exit be revisited).

**The escalation seam.** When a decision the maintainers cannot make individually surfaces (major architectural change, breaking-change with contested community response, security-response gone sideways, a fork threat), the maintainers escalate to the principal within days. The escalation is not adversarial; it is the contract's normal mode. Mod-505 chapter 4 § *the escalation path* is the internal-review-body analogue.

## The release-proposal artifact

Every open-source release from a principal-scope decision produces a release proposal — the single canonical document that ratifies decisions 1–4. Shape:

1. **What is being released.** One paragraph. The system, the interface, the substrate.
2. **Which of the six *right-shape* patterns it fits.** Explicitly. If it does not cleanly fit one of the six, the release proposal has to defend the fit.
3. **What is deliberately not being released.** The proprietary edge, the customer-data-touching code, the internal-only conventions. Named.
4. **The maintenance contract.** All seven commitments from decision 2 above, filled in with specifics.
5. **The north-star alignment posture.** Mirror / extend / diverge. If extend or diverge, the specific alignment discipline (test surfaces, cadence coupling, PR-acceptance criteria) is named.
6. **The maintainer bench.** Names, altitudes, committed time-percentages. The engineering director's ratification signature.
7. **The budget line.** Multi-year (typically 3-year) commitment. The CFO's ratification signature.
8. **The exit shape.** Named upfront. The criteria that would move the release toward the named exit.
9. **The community-governance model.** Committer criteria, decision process, code-of-conduct posture, contribution licence (typically Apache-2.0, MIT, or BSD; project-specific).
10. **The legal review.** Trademark check, patent-encumbrance check, contributor-licence-agreement or developer-certificate-of-origin decision, third-party-code audit. Signed off by legal counsel.

The proposal is 5–15 pages, canonicalised in the mod-503 chapter 5 canonical-doc location, and revised annually per chapter 6 § *retirement criteria*.

## Failure modes

- **The open-source dump.** Named in chapter 1; called out here because it is the modal open-source failure mode. The org releases code with no maintenance contract, no CFO-ratified budget, and no named maintainer bench. Six months later the release has stale issues, no PRs merged, and a *"is this project abandoned?"* thread in the tracker. The fix: refuse the release without the ratified maintenance contract.

- **The two-implementations trap.** Named above. Six months after release the internal and public codebases have diverged; every subsequent internal change is doubled work. The fix: upfront alignment discipline; the internal system consumes the public release, not a fork.

- **The proprietary-edge leak.** The release includes the proprietary edge the org competes on. The competitor adopts the release and closes the differentiation gap within a cycle. The fix: chapter 5 § *shape δ* is not on the *right-shape* list; the release proposal names *what is deliberately not released* as its own section for this reason.

- **The principal-as-maintainer trap.** The principal writes the release proposal *and* takes on maintainership. Six months in the principal has become the release's primary reviewer, and the internal principal-scope work is under-served. The fix: the maintainer bench is the peer specialist tracks; the principal sponsors it but does not staff it.

- **The unratified maintenance contract.** The proposal names the maintenance contract but the CFO has not signed off on the multi-year budget. The release ships; the first budget cycle re-evaluates; the maintainer bench evaporates; the release fails. The fix: refuse the release without the CFO signature.

- **The no-exit release.** The release proposal has no named exit shape. Two years in the release is drifting — not obviously failing, not obviously succeeding — and no criterion exists to trigger a decision. The fix: every proposal names the exit shape; chapter 6 § *retirement criteria* is the annual re-audit.

- **The vanity release.** The release is the principal's personal side project positioned as an org-scope release, without an internal use case and without the maintainer bench. The internal ML org treats it as the principal's hobby; the community treats it as an under-supported project. The fix: no release without an internal use case that will exercise the code path in production.

- **The contribution-licence oversight.** The release is published without a clear contribution licence, or with a licence that conflicts with the org's IP posture, or without a CLA / DCO decision. Community PRs are accepted but the licence status is unclear; downstream users (correctly) refuse to depend on the release. The fix: legal review as decision-9 sign-off on the release proposal; no release without it.

## Summary

- The principal owns *release-level* open-source decisions (what to release, the maintenance contract, north-star alignment, exit shape). The peer specialist tracks own the *commit-level* maintainership craft. The maintainership contract is the seam.
- Six shapes are right for open-sourcing at principal altitude: paved-road interface (not implementation), eval harness (not eval data), benchmark (not private extension), reference implementation of an internal invariant, tool that is not the competitive edge, graduated experiment. Six shapes are wrong: model weights (usually), internal-tools codebase, customer-data-touching code, the proprietary edge, pre-stable API, "just for the community" release with no internal use case.
- The maintenance contract has seven commitments: release cadence, security-patch SLA, breaking-change policy, deprecation horizon, community-response SLA, maintainer bench, sunset criteria. Ratified by the engineering director (headcount) and the CFO (multi-year budget).
- North-star alignment is a continuous discipline: mirror, extend, or diverge. Divergence is the two-implementations trap; the fix is upfront alignment discipline and the internal system consuming the public release as a dependency, not a fork.
- Every release has a named exit shape at release: graduation to foundation, donation to standards body, archival, or continuous stewardship (re-audited annually).
- The release proposal is 5–15 pages ratifying all four decisions, canonicalised in the mod-503 chapter 5 location, revised annually.
- Eight failure modes: open-source dump, two-implementations trap, proprietary-edge leak, principal-as-maintainer trap, unratified maintenance contract, no-exit release, vanity release, contribution-licence oversight.
- Chapter 6 walks the return-on-external-influence tracking that the open-source release feeds into — the internal-leverage signal (does the release lower internal cost), the industry-adoption signal (is the release cited and adopted), and the exit trigger (should the release move to its named exit).
