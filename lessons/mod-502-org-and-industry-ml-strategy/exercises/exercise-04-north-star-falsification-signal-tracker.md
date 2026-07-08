# exercise-04: North-Star Falsification Signal Tracker

**Estimated effort:** 2 hours

## Objective

Build the operational signal tracker described in chapter 6 for the org's ML North Star. The output is a small, standing tracker artifact — one to two pages — with per-bet signal rows across the four signal categories, a decision log, and a defined refresh cadence with emergency-refresh triggers. The tracker is what turns the exercise-03 sunset criteria into an enforceable exit protocol.

## Prerequisites

- Chapter 6 read and internalised — the four signal categories, the tracker shape, the decision protocol.
- Chapter 4 read — the sunset criteria this tracker watches for.
- Exercise-03 complete, or a working sequencing + sunsets draft the tracker can bind to.
- Working familiarity with the specific signal sources for the org you are writing against — the frontier suppliers whose price movements matter, the regulatory jurisdictions whose obligations bind the org, the applied-ML publication venues the org's ML function actually reads.

## Problem statement

Every sunset criterion in the North Star relies on a signal materially firing to become enforceable. A criterion nobody watches for is decoration. This exercise builds the tracker that makes the criteria real: named signals per bet, sources per signal, cadence per source, thresholds per bet, and a decision log that records how the tracker has acted over time.

The tracker is *not* a market map ("Anthropic released Sonnet 5.5"). It is not a compliance-review board ("we are ready for EU AI Act Article 50 obligations"). It is the small, principal-owned artifact that filters inputs into per-bet signals and escalates when a signal materially fires.

## Requirements

Produce a single markdown file, `exercise-04-signal-tracker.md`, in a personal workspace (do not commit into this curriculum repo). Structure it as follows.

- **A single H1 title.** ("<Org> ML North Star Signal Tracker — <YYYY-MM-DD refresh>".)
- **A header block** with:
  - Last full review date (use the current date or an appropriate date within the past six months).
  - Next scheduled full review date (six months out).
  - Emergency-refresh triggers, named specifically — chapter 6's shape is a good template.
- **Per bet, a subsection** (five subsections total, in chapter-2 row order) containing:
  - The bet's summary posture (one sentence, cite exercise-03).
  - A markdown table with columns: **signal ID** (e.g., 1a, 1b), **category** (1–4 from chapter 6), **description**, **source**, **cadence**, **current value / trajectory**, **threshold-to-fire-sunset-or-flip**, **last checked**.
  - At least three signal rows per bet, spanning at least two of the four signal categories.
  - For not-in-window rows, the tracker signals are the *revisit conditions* from exercise-03; treat them the same way.
- **A decision log section.** At least three plausible past decisions logged in the shape *"YYYY-MM-DD: signal X triggered a [note / partial refresh / full refresh / sunset execution]; consequence Y; ratified by Z."* The log demonstrates the decision protocol in operation; the entries can be plausible / synthetic for the purpose of the exercise, but they must show the protocol's four decision types across the log.
- **A category-coverage self-check.** A short paragraph naming which of chapter 6's four categories are underweighted in your tracker (if any) and what you would add on the next refresh.
- **A hand-off contract note.** One paragraph naming which signals cite `head-of-ai-governance-learning` for regulatory depth, which cite `staff-ml-engineer-learning` mod-407 for cost depth, and which cite `ai-infra-principal-engineer-learning` mod-505 for platform-side signal. The tracker cites; the tracker does not duplicate.

## Starter guidance

- **Every signal has an owner-of-source.** If you cannot name where the signal comes from — a specific supplier's pricing page, a specific standards body's official journal, a specific research venue's proceedings, a specific internal dashboard — the signal is not a signal yet; it is a wish for one.
- **Regulatory signals should point at real regulatory frameworks.** EU AI Act (Regulation (EU) 2024/1689), NIST AI Risk Management Framework 1.0 plus the Generative AI Profile (NIST AI 600-1), ISO/IEC 42001, and the sector-specific frameworks that bind your org. Do not invent regulations.
- **Cost signals should reference real supplier / capacity artifacts.** Supplier pricing pages, hyperscaler-published capacity plans, or the org's own FP&A forecasts. Do not fabricate price levels; the tracker's job is to make the *threshold* explicit even when the current value is not certain.
- **Category 1 signals should reference real venues.** Frontier lab technical reports (the Chinchilla paper, the Llama 3 herd technical report, the DeepSeek-V3 technical report, and their forward equivalents), KDD applied track, RecSys, NeurIPS / ICML industry-track, and the engineering blogs the org's peers publish on. Do not invent papers.
- **Category 4 signals are internal.** These should map to specific dashboards, monitoring systems, or metrics the org's ML function actually maintains. The point of category 4 is that it surfaces trouble on a bet *earlier* than the OKR metric would; if a category-4 signal is the same as an OKR, it is not doing the tracker's job.
- **Thresholds are load-bearing.** A signal without a threshold is a subscription. Every row needs the *"threshold to fire sunset or flip"* column filled in.
- **The decision log demonstrates the protocol.** Its job is to show that the tracker has all four decision types (note / partial refresh / full refresh / sunset execution) as live options, not just the safe *note* action. Include at least one *partial refresh* entry.
- **The tracker stays small.** One to two pages. If it exceeds two pages, it has drifted into being a market map or a compliance checklist. Cut back.

## Acceptance criteria

Your document is done when it can pass all of the following:

- [ ] Header block includes last-review date, next-review date, and specifically-named emergency-refresh triggers.
- [ ] Five per-bet subsections, in chapter-2 row order.
- [ ] Each subsection has a signal table with the eight required columns and at least three signal rows spanning at least two of the four chapter-6 categories.
- [ ] Every signal row names a specific, verifiable source (supplier pricing page, official journal, research venue, internal dashboard).
- [ ] Every signal row has a threshold-to-fire-sunset-or-flip populated.
- [ ] Regulatory signals reference at least one of EU AI Act (Regulation (EU) 2024/1689), NIST AI RMF 1.0, ISO/IEC 42001, or a real sector-specific framework.
- [ ] The decision log has at least three entries and demonstrates at least three of the four decision types (note / partial refresh / full refresh / sunset execution).
- [ ] The category-coverage self-check names which categories are underweighted and what would be added.
- [ ] The hand-off contract note cites `head-of-ai-governance-learning`, `staff-ml-engineer-learning` mod-407, and `ai-infra-principal-engineer-learning` mod-505 (or explicitly notes when a peer is not applicable to a given signal).
- [ ] The full document is one to two pages when rendered; not longer.
- [ ] No invented papers, invented regulations, invented supplier price levels, or invented benchmark results appear anywhere.

## Stretch goals

- **Second-refresh delta.** Fast-forward six months and produce a hypothetical *v2* of the tracker where two signals have shifted materially. Log the resulting decisions. What in the North Star changes? What in the roadmap changes? What in the mod-503 architecture changes?
- **Cross-check with a peer principal.** Take the peer platform-side principal track's mod-505 tracker shape and note which of your signals are also that principal's signals, and where the two would need to coordinate on the same threshold.
- **Signal-quality retrospective.** Pick three signals from your tracker and pressure-test them for the category-4 failure mode from chapter 6: is each signal really giving you earlier warning than the OKR would? If not, replace or drop.

## Deliverable location

Local workspace. When exercise-01, exercise-02, exercise-03, and exercise-04 are all complete, you have the substantive core of the paired North Star artifacts described in chapter 7 (one-pager + deep-dive). Exercise-05 stress-tests the seam with the staff-scope portfolio roadmap.
