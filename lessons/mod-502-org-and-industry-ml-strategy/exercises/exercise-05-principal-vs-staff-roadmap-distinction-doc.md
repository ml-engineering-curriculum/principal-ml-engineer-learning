# exercise-05: Principal-Scope North Star vs. Staff-Scope Portfolio Roadmap — Distinction Doc

**Estimated effort:** 3 hours

## Objective

Diagnose the seam between the principal-scope multi-year North Star and the staff-scope portfolio roadmap (chapter 5, and mod-501 chapter 6) against a real (or realistic) portfolio roadmap. The output is a short distinction doc that (a) traces every non-operational roadmap commitment back to a specific North Star bet, (b) surfaces the seams that are broken in either direction, and (c) proposes concrete refinements to either artifact so the seam holds.

## Prerequisites

- Chapter 5 read and internalised — the two-artifact comparison table, the seam mechanics, the hand-off contract.
- Mod-501 chapter 6 read — the general hand-off pattern from principal to staff scope.
- Exercise-02 and exercise-03 complete — you have a working bet portfolio and sequencing to trace against.
- A portfolio roadmap to trace against — either (a) your team or org's real current-fiscal-year ML portfolio roadmap (with any sensitive detail redacted before you write in the personal workspace), or (b) a synthetic-but-realistic portfolio roadmap you construct as the staff-scope counterpart to your exercises 02+03 for the same org. Option (b) is fine, but the roadmap must be realistic enough to actually pressure-test the seam.

## Problem statement

Chapter 5's argument is that the two artifacts are in continuous conversation: the roadmap decomposes the North Star; the North Star shapes the roadmap. That conversation breaks in two directions.

- **Roadmap side breaks the seam.** A commitment on the roadmap has no North Star bet behind it. Two possibilities: the North Star is missing a row, or the commitment is non-strategic operational load that should not be in the roadmap's strategic section.
- **North Star side breaks the seam.** A year-1 bet on the North Star has no corresponding roadmap decomposition. Two possibilities: the bet is set but the org is not moving on it (be honest and move the bet to year 2), or the roadmap is stale and needs to update.

Your task is to run the two diagnoses on a real (or realistic) pair, produce the trace, name the broken seams, and propose the refinements.

## Requirements

Produce a single markdown file, `exercise-05-distinction-doc.md`, in a personal workspace (do not commit into this curriculum repo). Structure it as follows.

- **A single H1 title.** ("<Org> ML North Star ↔ Portfolio Roadmap Distinction Doc — <YYYY-MM-DD>".)
- **Section 1: Source artifacts.** Name the two artifacts you are tracing against: the North Star (your exercises 01–04, or a real one), and the portfolio roadmap (real or realistic-synthetic). One paragraph each.
- **Section 2: The two-artifact table.** Reproduce the chapter-5 comparison table (audience, horizon, unit of commitment, scope, load-bearing content, falsifiability shape, refresh cadence, author, ecosystem owner), filled in for *your* org's actual pair. Note where either artifact deviates from the reference row and whether the deviation is a real difference or a bug.
- **Section 3: Roadmap-to-North-Star trace.** For each strategic commitment on the roadmap (list at least ten, or the full list if fewer), name the specific North Star bet it decomposes. Format:

  ```
  | Roadmap commitment | North Star bet | Row | Year-1 state | Notes |
  |---|---|---|---|---|
  | ... | ... | 2 | bet | ... |
  ```

  Flag each commitment as: `traces cleanly`, `traces but weakly`, or `no North Star trace`. Include a count summary at the bottom.
- **Section 4: North-Star-to-roadmap trace.** For each year-1 bet on the North Star, name the specific roadmap commitments — teams, quarters, deliverables — that advance the bet in the current fiscal year. Flag each bet as: `decomposes clearly`, `decomposes weakly`, or `no roadmap decomposition`. Include a count summary at the bottom.
- **Section 5: Diagnosed broken seams.** For every commitment flagged `no North Star trace` in section 3 and every bet flagged `no roadmap decomposition` in section 4, name which of the four failure modes from chapter 5 fits, and what the fix is:
  - Roadmap commitment with no North Star trace → missing North Star row *or* non-strategic operational load in the roadmap's strategic section.
  - North Star bet with no roadmap decomposition → bet set but org not moving *or* stale roadmap.
- **Section 6: Refinement proposals.** For each broken seam in section 5, propose a concrete refinement (add a row to the North Star; move a bet to year 2; add or remove a commitment from the roadmap; refresh either artifact) and name who ratifies the refinement (principal, staff engineer, VP).
- **Section 7: Escalation cases.** Name the two or three cases (if any) from your diagnosis where the fix requires the chapter-5 escalation path — up to the VP or up to the CTO / SVP — because principal and staff engineer cannot resolve locally. Cite the escalation-path shape from chapter 5.
- **Section 8: Meta-observation.** One paragraph on what the trace *as a whole* tells you about the health of the seam in the org you traced. Is the seam broadly holding, silently drifting, or actively broken? Cite specific numbers from your traces (e.g., "8 of 12 roadmap commitments trace cleanly; 2 fail; 2 trace weakly").

## Starter guidance

- **Do the roadmap-to-North-Star trace first.** It is usually the more productive direction — you have concrete commitments in front of you, and tracing them up forces you to notice where the North Star is thin.
- **A "trace weakly" flag is where the honest work lives.** A commitment that *sort of* advances a bet, but through a chain of two or three layers, is a trace-weakly. Treat these as flags for the North Star's row not being sharp enough, not for the roadmap being wrong.
- **Not every roadmap commitment is strategic.** Operational commitments — reliability improvements, migrations, incident-driven work — are legitimate roadmap entries that need not trace to a North Star bet. Section 3 is looking at *strategic* commitments; make the strategic-vs-operational cut before starting the trace. If your roadmap does not distinguish, treat all as strategic for the trace and note the ambiguity.
- **A high number of `no trace` findings on the roadmap side often means the North Star is missing rows.** Before proposing to cut roadmap commitments, ask whether the North Star should be broader.
- **A high number of `no decomposition` findings on the North Star side often means the year-1 bets are aspirational.** Chapter 3's discipline: name three year-1 bets, and the org has to actually be moving on them.
- **The escalation cases are usually the most valuable part of the doc.** If the diagnosis surfaces a seam that only a VP or SVP can close (e.g., "the North Star has a year-1 RecSys converged-substrate bet, but the platform-side principal's mod-505 has the underlying platform bet as year 2, so the roadmap literally cannot decompose the bet this year"), that is the case mod-504 is designed for. Note it here; carry it forward.
- **Do not use this exercise to blame the roadmap or the North Star.** Both artifacts are the output of good-faith work at different altitudes. The exercise's job is to make the seam legible, not to grade either artifact.

## Acceptance criteria

Your document is done when it can pass all of the following:

- [ ] Source artifacts section names the two artifacts being traced with enough detail that a reader can understand what the pair is.
- [ ] The two-artifact table is reproduced and filled in for the actual pair, with deviations from the reference row noted.
- [ ] Section 3 traces at least ten strategic commitments (or the full list if fewer) and includes the flag distribution count at the bottom.
- [ ] Section 4 traces every year-1 bet on the North Star and includes the flag distribution count.
- [ ] Every `no trace` / `no decomposition` finding in sections 3 and 4 is diagnosed in section 5 with a specific failure mode from chapter 5.
- [ ] Every broken seam in section 5 has a concrete refinement in section 6 with a named ratifier.
- [ ] Section 7 either names two or three escalation cases with the chapter-5 escalation path or explicitly notes there are none (with justification).
- [ ] Section 8 characterises the seam's health with specific counts drawn from the traces.
- [ ] Nowhere in the doc does the author confuse team-level operational work with a broken seam.
- [ ] If synthetic-realistic (not real) source artifacts were used, that is disclosed in section 1.

## Stretch goals

- **Cross-org roadmap trace.** Repeat the exercise for a different org whose portfolio roadmap you can access — perhaps a peer's, or a public post-mortem of an ML org's multi-year plan. Compare the seam health across the two orgs. What is the pattern of drift?
- **Backwards-tracing test.** For each North Star bet, ask a staff engineer on the affected team what artifact they would build the fiscal-year roadmap from. If they name a document other than the deep-dive companion (chapter 7), the deep-dive is not doing its job. Note the finding.
- **Escalation-case rehearsal.** For one of your section-7 escalation cases, draft the two-paragraph narrative you would use to bring the seam-broken case to the VP or CTO / SVP. Chapter 7 and mod-504 both feed the shape.
- **Pair with the mod-501 exercise-04 self-assessment.** How much of what mod-501 exercise-04 identified as level-up work on theme 1 (org-industry strategy) is on display in this exercise? Which of the seam failures you diagnosed would be easier to avoid after another cycle through the material?

## Deliverable location

Local workspace. This exercise is the seam-diagnosis practice that closes the mod-502 loop; the artifact is a working document you can return to at each North Star refresh cycle in the field.
