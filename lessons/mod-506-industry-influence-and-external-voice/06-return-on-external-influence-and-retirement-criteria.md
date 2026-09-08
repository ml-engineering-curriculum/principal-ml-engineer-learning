# Return on External-Influence Investment — The Three Signals and the Retirement Criteria

> Chapter 6 of mod-506. Prerequisite: chapters 1–5. Downstream: exercise-01's artifact plan includes the tracking-and-retirement dashboard this chapter defines. Interacts with mod-502 chapter 6 (signal-tracking cycle) and mod-505 chapter 6 (personal-cadence artifact) — both are the parent disciplines this chapter lifts to the external-influence-portfolio surface.

## Why the ROI question is load-bearing

External-influence work has a cost the principal pays in *the currency that matters most at principal altitude* — authoring time on artifacts other people cite. Chapter 2 § *the internal-first ratio* named the annual budget (roughly 30% of authoring hours). Chapters 3, 4, and 5 walked how each individual artifact is produced.

None of that answers the question that ultimately settles the portfolio: *is the external-influence work returning enough signal to justify continuing at the current level?* Without an answer, the principal ends up in one of two failure modes.

- **Over-investment.** The keynote-only drift (chapter 1 failure mode 6; mod-505 chapter 6 § *keynote-only drift*). The principal keeps saying yes to external work because it feels productive and gets validating feedback in the room. The internal substrate erodes. Two cycles later the external work has degraded because the internal substrate is thin.
- **Under-investment.** The principal drops external work after a few unsuccessful bets and accepts that industry-influence is *"not for me"*. The Capital One preferred qualification quietly sits unaddressed. Recruiting funnel narrows. The peer principals at other orgs stop citing your work because there is nothing to cite. The peer-principal exchange (mod-505 chapter 6) has fewer counterparties.

Both failure modes are cheaper to detect if the principal tracks the return signal explicitly. This chapter fixes the three signals and the retirement criteria.

## The three return signals

The Capital One preferred-qualification framing enumerates the *venues* (papers, presentations, blog posts, open source). It does not enumerate the *return*. But the return signals converge on three axes across principal-scope postings and role definitions.

### Signal 1 — the recruiting signal

**What it is.** Staff-plus candidates in the org's hiring funnel who cite an external artifact of yours as a reason for interviewing or as evidence they read before the loop. Modal forms: *"I read your KDD paper on the eval program"*, *"I watched your QCon keynote on the foundation-model bet framing"*, *"I have been contributing to the open-source project your team released."*

**Why it matters at principal altitude.** The principal seat is (per mod-505 chapters 3 and 5) the staff-plus hiring-loop calibrator. A recruiting funnel that surfaces candidates who *already know* the org's principal-scope work is a funnel with materially higher signal-per-hour spent in loops. Every candidate who arrives having read your artifact is a candidate the loop starts with a common vocabulary, a shared architectural context, and evidence of independent alignment with the org's technical direction.

**How to measure.** The org's recruiter or hiring-manager can tag inbound applicants and offered candidates with a *"cited principal-scope artifact"* flag. Track the count per quarter per artifact. A useful denominator is the total staff-plus applicant count in the same window; a useful qualitative pointer is the specific candidates whose citations were most substantive (a candidate quoting the artifact's non-goals is a stronger signal than one who read the abstract).

**What good looks like.** A single influential artifact will surface 5–20 candidates per quarter across staff-plus roles at a mid-sized ML org after 6–18 months of publication. Portfolio-wide, an active principal producing 4–8 external artifacts per year sees a steady 15–50 candidates per quarter citing at least one across the funnel. The absolute number is org-specific; the useful measure is the *trend* per artifact and the *staff-plus offer rate* on candidates who arrived through citation.

**What decay looks like.** An artifact's citation count in the recruiting funnel peaks 3–6 months after publication and decays over 12–24 months. A durable artifact (a widely-cited paper, a foundational open-source release) can sustain non-trivial citation for 3+ years; most keynotes decay to near-zero within 24 months.

### Signal 2 — the industry-standard adoption signal

**What it is.** Peer companies citing the principal's reference architecture, adopting the open-source release, extending the benchmark, or building on the pattern the paper or blog described. Modal forms: a peer org's principal-scope blog citing your paper; a peer org's public architecture diagram mirroring your reference architecture's shape; a peer org's open-source release building on your benchmark or eval harness; a standards body incorporating your invariant into an emerging standard.

**Why it matters at principal altitude.** This is the *industry impact* the Capital One framing names. It is the load-bearing signal for the *external influence bet's* justification. A paper that no peer principal has cited within 18 months is a paper the industry has not adopted; a keynote that no peer principal has referenced in a subsequent talk or blog is a keynote whose direction did not land beyond the room.

**How to measure.** Multiple channels, each low-cost individually.

- **Citation graph (papers).** Google Scholar or Semantic Scholar citation count. Filter for *industry-cited* citations specifically — a paper cited only by academic papers has landed as an academic paper, not as an industry-track paper. Track quarterly.
- **Repository-adoption graph (open source).** GitHub Insights (stars, forks, dependent-repository count) plus *depended-on-by* signal from ecosystem package managers (PyPI, npm, Maven Central) — total downloads and quarterly download trend. Filter for *organisational* adopters, not individual downloads.
- **Reference-architecture citation (papers and blogs).** Manual monitoring of peer companies' engineering-blog series, industry-track programmes, and standards bodies. A quarterly search on the specific terms the artifact introduced or the specific patterns it named. This is manual work — 30–60 minutes per quarter per artifact; delegated to the org's engineering-brand or applied-ML lead.
- **Standards-body adoption.** Tracking whether the artifact's contribution has been proposed, referenced, or incorporated in an emerging standard (MLCommons, ONNX, OpenTelemetry-ML, CNCF ML SIG). This surfaces on a longer horizon (12–36 months post-publication).

**What good looks like.** Industry citation is inherently longer-horizon than recruiting-funnel citation. A useful bar for a single artifact: 3–10 peer-company citations within 18 months for a paper or blog; 100–1,000 GitHub stars and 5–20 organisational dependents within 12 months for an open-source release; 1–3 peer keynotes referencing the through-line within 12 months for a talk. These bars are order-of-magnitude, not thresholds; the trend and the *substance* of the citations matter more than the count.

**What decay looks like.** Industry adoption typically peaks 12–24 months after publication for papers and blogs, 24–36 months for open-source releases, and can persist near-peak for 5+ years for foundational artifacts. Artifacts that fail to gain adoption in the first 12 months rarely recover; the signal is either the direction did not resonate or the venue-audience-artifact match (chapter 1) was wrong.

### Signal 3 — the internal-leverage signal

**What it is.** The internal effect of the external artifact — junior staff at the org building on the principal's canonical write-up, internal design reviews citing the artifact as substrate, new-hire onboarding using the external artifact as the entry point to the org's technical direction. Also: the open-source release lowering internal maintenance cost because internal consumers converge on the public API rather than a fork.

**Why it matters at principal altitude.** This is where the internal-first ratio (chapter 2) closes the loop. An external artifact whose *internal* effect is high is doing double duty — it advances the industry *and* it lifts the org's junior staff onto the artifact's substrate faster than an internal-only artifact would. An external artifact whose internal effect is zero has effectively been *paid for* by internal-substrate work but returns only external signal; the ratio has been externalised.

**How to measure.**

- **Internal citation count.** How often the external artifact is cited in the org's internal design reviews, internal one-pagers, internal onboarding materials, and internal tech-radar entries. Track per artifact quarterly. Two entry points: pull-request / merge-request grep for the artifact's URL or title; internal-doc-registry grep for the same.
- **Junior-staff progression signal.** How often junior staff (L20 / L30) reference the external artifact as an *"I built this after reading your paper"* attribution. Surfaces in mod-505 chapter 5 § *community rituals* — the applied-relevance reading discussion is where the attribution surfaces most cleanly.
- **New-hire onboarding usage.** Whether the external artifact appears in the ML org's new-hire onboarding curriculum. A useful cross-check: ask three recent new-hires which external artifacts they read as part of onboarding; if the artifact you produced does not surface, the internal-leverage signal is under-realised.
- **Maintenance-cost delta (open source only).** Whether the open-source release has lowered or raised internal maintenance cost since release. This is the chapter 5 § *the two-implementations trap* audit; measure quarterly during the release's first two years and annually after.

**What good looks like.** An internal-leverage-positive artifact is cited 5–20 times per quarter in internal design reviews, appears in the new-hire onboarding curriculum within 6 months of publication, and (for open-source releases) has flat or declining internal maintenance cost. The specific numbers vary; the useful measure is the *directionality* — is the artifact's internal effect increasing, plateauing, or decaying?

**What decay looks like.** Internal-leverage signal decays *faster* than industry-adoption signal because internal audiences move on to newer artifacts. A 12-month decay-to-half is the modal shape for a keynote; a 24-month decay-to-half for a paper; open-source releases can sustain internal-leverage indefinitely if the release remains the canonical internal consumer.

## The tracking dashboard

The three signals combine into a single tracking dashboard the principal reviews quarterly. Shape: one row per external artifact, one column per signal per quarter, an overall status column (green / yellow / red / retired), and a *next-action* column.

Practical shape (table columns):

- **Artifact ID and title.** With publication date.
- **Venue class.** Paper / blog / keynote / open-source (chapter 1 taxonomy).
- **Recruiting signal (last 4 quarters).** Citations in funnel; qualitative note on standout candidates.
- **Industry-adoption signal (last 4 quarters).** Citation count / adoption metric; qualitative note on standout adopters.
- **Internal-leverage signal (last 4 quarters).** Internal citation count; onboarding-usage flag; maintenance-cost note (for OSS).
- **Status.** Green (all three signals healthy or on-plan), yellow (one signal decaying), red (two or three signals decaying), retired (out of active portfolio).
- **Next action.** Continue / refresh / retire / escalate to hand-off.

The dashboard is reviewed in the mod-505 chapter 6 quarterly cadence artifact. It is *not* published externally; it is the principal's private (or principal-plus-manager) tracking tool.

## The calendar-shape check

Chapter 2 § *the internal-first ratio* named the 70/30 target hours split. The calendar-shape check is the quarterly audit that keeps the ratio honest.

Three checks.

- **Check 1 — hours authored.** From the principal's calendar, roughly bucket authoring hours across internal (chapter 2 artifact classes A/B/C plus the mod-503 chapter 5 canonical docs plus mod-504 chapter 5 one-pagers / deep-dives / FAQs) and external (chapter 3–5 artifacts). Confirm the ratio is within 60/40–80/20 of internal-to-external. Sustained inversion is a rebalancing signal.
- **Check 2 — artifact-slate freshness.** For each of chapter 2's three internal artifact classes, confirm at least one artifact has been authored or revised in the last 6 months. If any class has gone 12+ months untouched, that class is decaying and needs rebalancing regardless of what the external slate looks like.
- **Check 3 — the peer-principal exchange.** Mod-505 chapter 6 § *the peer-principal exchange* is the closest analogue to an external audit. Confirm at least one recent (last 6 months) exchange with a peer principal at another org where the external-influence portfolio was substantively discussed. If the peer's read of your external presence differs materially from your own (they cite artifacts you had forgotten about; they do not cite artifacts you thought were load-bearing), the external portfolio's self-assessment is drifting from ground-truth.

## Retirement criteria — when to sunset an external-influence bet

Mod-502 chapter 4 § *sunset criteria* established the discipline: every bet carries pre-committed criteria that would end it. The external-influence portfolio holds the same discipline. Four retirement triggers.

- **Trigger 1 — signal decay across all three axes.** The artifact's recruiting signal has decayed to near-zero, the industry-adoption signal has plateaued below the useful bar or is declining, and the internal-leverage signal is not compensating. The artifact has run its useful life; retiring it means not investing further in refreshes, follow-on talks, or updates.
- **Trigger 2 — the substrate has evolved past the artifact.** The internal system the artifact was extracted from has been sunset, re-architected, or fundamentally shifted. The artifact is now describing a system the org no longer runs. The artifact is retired to *"archived, superseded by [next artifact]"* status.
- **Trigger 3 — the direction the artifact defended has been retired.** For bet-framing artifacts (mod-502-shape), the underlying bet has sunset per its own sunset criteria. The artifact retires with the bet — and the *retirement itself* often becomes a chapter 3 § *the honest-failure discipline* substrate for the next artifact.
- **Trigger 4 — the maintenance cost has exceeded the return.** For open-source releases specifically, the chapter 5 § *decision 4 — exit / hand-off* criteria have fired. The release moves to one of the four named exit shapes; the maintenance-cost delta stops accruing to the org.

Retirement is *explicit*, not passive. A retired artifact is marked retired in the tracking dashboard; a retired open-source release is moved to its named exit shape; a retired paper or blog is superseded by a follow-up artifact that cites the retirement. This is what distinguishes *retired* from *dead*, in the mod-504 chapter 6 § *the discipline that separates deferred from dead* sense.

## Interaction with the mod-505 personal-cadence artifact

The external-influence tracking dashboard is one of the sections of the principal's quarterly personal-cadence artifact (mod-505 chapter 6 § *quarterly review*). Specifically, the mod-505 quarterly artifact's *portfolio-check* section carries a subsection on external-influence:

- The tracking dashboard's status row for the quarter.
- The calendar-shape check outcome.
- Any retirement triggers that fired this quarter (per the four triggers above).
- Any rebalancing signals that fired (per chapter 2 § *the internal-first ratio*).
- Named commitments for the next quarter (which artifact refresh, which retirement, which new bet, which internal rebalance).

The mod-505 chapter 6 § *yearly review* extends this to the annual re-audit: which artifacts landed in the top decile on which signals, which venues over- and under-performed for the year, whether the venue portfolio itself needs rebalancing (fewer keynotes, more open-source; more papers, fewer blogs; etc.).

## Failure modes

- **The vanity-metric trap.** Tracking absolute counts (papers submitted, blog posts published, keynote invitations accepted) instead of return signal. A quarter with three keynotes and zero recruiting-funnel citations is a *worse* quarter than one keynote with fifteen substantive citations. The fix: never track venue-side counts as the return metric; always ask *what came back?*

- **The signal-of-one trap.** Tracking only one signal (usually the industry-adoption signal, because it is the most externally-visible and ego-flattering). A paper with 500 academic citations and zero recruiting-signal or internal-leverage is a paper that has landed as academic work, not as principal-scope external influence. The fix: all three signals or none; the tracking dashboard's status column is *conjunctive*, not disjunctive.

- **The lagging-only measurement.** Only reading signals at 18-month or 24-month horizons. By then, the rebalancing decision is 12+ months late. The fix: quarterly review of all three signals with explicit near-term (3-6 month) and horizon (12-24 month) tracking columns.

- **The self-assessment drift.** The principal reads their own external-influence portfolio as more influential than it is (or, occasionally, less). No external audit surfaces the drift. The fix: the peer-principal exchange every 6 months, with an explicit *"how are you reading my external presence"* prompt.

- **The retirement-avoidance pattern.** The principal knows the artifact should be retired but keeps it in active status because retiring feels like admitting failure. The tracking dashboard rows for the artifact stay yellow for four consecutive quarters. The fix: pre-commit the retirement criteria (four triggers above); when any triggers fire, execute the retirement per chapter 6 § *retirement criteria*.

- **The escalation-to-hand-off skipped.** For open-source releases specifically, the exit shape (chapter 5 § *decision 4*) is available but not executed even when the maintenance-cost delta has turned negative. The release lingers in *"active but under-maintained"* status. The fix: chapter 5's exit criteria are load-bearing; the tracking dashboard's *next-action* column names *escalate to hand-off* when the exit-shape criteria fire.

- **The internal-first ratio inversion goes undetected.** The calendar-shape check is done cursorily and the ratio drifts to 40/60 over two quarters without triggering rebalancing. The internal substrate erodes. Named as the keynote-only drift failure mode across chapters 1, 2, and 5. The fix: the calendar-shape check is a *disciplined* audit each quarter; the mod-505 quarterly artifact has a section for it.

## A worked micro-example — the tracking-row for one artifact

For grounding, here is what a single row of the tracking dashboard reads like at defensible fidelity, three quarters post-publication of a hypothetical industry-track paper on cross-team eval program discipline.

> **Artifact:** *A cross-team ML eval program at [org] — 11 teams, 18 months, three retired regressions*, KDD industry track, published Q2. **Venue class:** paper (with paired blog post published Q1). **Recruiting signal (last 4 quarters):** Q3 — 4 candidates cited (2 staff, 2 senior); Q4 — 11 candidates cited (5 staff, 4 senior, 2 principal-track); Q1-current — 8 candidates cited; Q2-current — 9 candidates cited. One offer accepted at staff level whose interview loop cited the paper's methodology section. **Industry-adoption signal:** 6 peer-company citations to date (2 in peer engineering blogs, 3 in follow-on industry-track submissions, 1 in MLCommons benchmark proposal); GitHub stars on the paired open-source eval-harness release: 340 (Q3 → Q2-current: 40 → 340). **Internal-leverage signal:** cited in 14 internal design reviews across 3 product areas (Q3 → Q2-current); appears in ML-org new-hire onboarding as required reading (added Q4); junior-staff attribution: 3 L30 engineers cite the paper as substrate for their next-cycle multi-team blueprints. **Status:** green. **Next action:** continue; plan Q4 refresh blog on the 24-month evolution; consider a QCon keynote (chapter 4) using the paper as substrate in the following cycle.

Notice what the row does *not* contain: the absolute submission-count, the "views" count on the blog post, the LinkedIn engagement metrics, the podcast interviews. All are vanity metrics. What the row does contain: the three signals, each with quarterly time-series and qualitative substance, and a next-action grounded in the trajectory.

## Summary

- External-influence work is a bet. Every bet carries pre-committed retirement criteria. This chapter fixes both the *return-signal tracking* and the *retirement discipline*.
- Three return signals: recruiting-funnel citation (near-term, decays 12–24 months), industry-standard adoption (long-horizon, peaks 12–36 months, foundational artifacts persist 5+ years), and internal leverage (junior-staff building on the write-up, onboarding usage, open-source-release maintenance-cost delta).
- The tracking dashboard is one row per artifact, one column per signal per quarter, an overall status (green / yellow / red / retired), and a next-action column. Reviewed quarterly in the mod-505 personal-cadence artifact.
- The calendar-shape check runs each quarter: hours authored (60/40–80/20 internal-to-external), artifact-slate freshness (each of chapter 2's three internal classes has been touched in 6 months), and the peer-principal exchange (external audit of the portfolio's self-read).
- Four retirement triggers: signal decay across all three axes, substrate evolved past the artifact, direction retired, maintenance cost exceeded return (for open-source). Retirement is explicit — marked in the dashboard, moved to a named exit shape (open-source), superseded by a follow-up artifact (papers and blogs).
- Seven failure modes: vanity-metric trap, signal-of-one trap, lagging-only measurement, self-assessment drift, retirement-avoidance pattern, escalation-to-hand-off skipped, internal-first ratio inversion undetected.
- The tracking dashboard closes the mod-506 loop: chapter 1's venue selection, chapter 2's internal-first substrate, chapters 3–5's per-venue craft, and this chapter's return-and-retirement discipline together are what turn external-influence work from a personal pursuit into a principal-scope engineering practice.
