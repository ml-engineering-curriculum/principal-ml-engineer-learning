# exercise-03: Multi-Year Roadmap With Non-Goals and Sunset Criteria

**Estimated effort:** 3 hours

## Objective

Sequence the five-row bet portfolio from exercise-02 into a defensible multi-year roadmap using the chapter-3 grid (bet / hedge / option / not-in-window) and attach the full chapter-4 non-goals-and-sunset-criteria layer to each row. The output is the sequencing + non-goals + sunsets sections of the deep-dive companion doc (chapter 7 sections 4 and 10, plus the sunset-criteria half of section 3).

Together with exercise-01 (one-pager) and exercise-02 (bet-portfolio content), this exercise produces the substantive core of the paired North Star artifacts.

## Prerequisites

- Chapters 3 and 4 read and internalised.
- Chapter 5 read — the sequencing has to respect the roadmap-vs-North-Star seam.
- Exercise-02 complete, or a working bet-portfolio draft you can sequence against. This exercise assumes the five rows exist.
- Familiarity with the peer platform-side principal's mod-505 shape (see [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning)); you don't need to have written that portfolio, but you have to be able to name at least a couple of platform-side dependencies each of your rows would carry.

## Problem statement

The bet portfolio names five directions. The sequencing turns those five directions into a defensible plan: which are year-1 bets, which are hedges with a decision date, which are options preserved through architectural discipline, and which are explicitly not-in-window with revisit conditions. The non-goals-and-sunset layer turns the sequencing into an *enforceable* plan: a bet without a non-goal is an aspiration; a bet without a sunset criterion is a perpetual bet.

Your task is to produce (a) the 5×3 sequencing grid, (b) the timeliness / flip / revisit arguments per state, and (c) the full non-goal register and sunset-criteria set — such that a staff engineer reading only this document could build the current fiscal year's portfolio roadmap in a single session.

## Requirements

Produce a single markdown file, `exercise-03-sequencing-and-sunsets.md`, in a personal workspace (do not commit into this curriculum repo). Structure it as follows.

- **A single H1 title.** ("<Org> ML North Star — Sequencing, Non-Goals, and Sunset Criteria (FY26–FY30)".)
- **Section 1: The 5×3 sequencing grid.** A markdown table with five rows (in chapter-2 order) and three year columns (Year 1, Year 2, Year 3). Each cell contains one of `bet` / `hedge` / `option` / `not-in-window`. Include a paragraph beneath the table naming the total year-1 bet count and confirming it is ≤3.
- **Section 2: Timeliness arguments.** One short paragraph per year-1 bet. Each paragraph answers the defense-1 question from chapter 3: *"Why is this a year-1 bet instead of a year-2 bet?"* The argument is a timeliness argument (cost of not investing rises faster than cost of investing), not a readiness argument.
- **Section 3: Flip conditions and decision dates.** One entry per hedge in the grid. Each entry names the specific signal (from chapter 6's category vocabulary) that would flip the hedge to a bet, plus the decision date the hedge resolves on.
- **Section 4: Preserved-option costs.** One entry per option in the grid. Each entry names the architectural discipline in the north-star architecture (mod-503) that preserves the option and the concrete substrate cost. A one-liner is fine; the discipline is what matters.
- **Section 5: Revisit conditions.** One entry per not-in-window row. Each entry names the falsification signal (from chapter 6) that would bring the row back into the window and — importantly — clarifies that the revisit is a review, not an automatic activation.
- **Section 6: Cross-check with the peer platform-side grid.** One paragraph noting the platform-side dependencies each year-1 bet carries and any place where your grid's coherence with a plausible platform-side grid is uncertain. If you know the peer principal's actual grid, cite it; otherwise, sketch what you would ask them to confirm.
- **Section 7: The non-goal register.** A per-row list of the full non-goal set for that row's current state. Each non-goal is a concrete refusal, with a named consequence, time-boxed to the window. Chapter 4's discipline strictly applied. Aim for three to five non-goals per row.
- **Section 8: The sunset criteria set.** A per-row list of the sunset criteria for that row. Each criterion has all three parts named — triggering condition, review cadence, defined exit action. Chapter 4's discipline strictly applied. Aim for one to two criteria per row.

## Starter guidance

- **Draft the grid first, then argue the sequence.** Do not start by writing the timeliness argument for a year-1 bet you have not yet committed to. Commit the grid, then defend the cells.
- **Enforce the year-1 bet cap.** Three year-1 bets is the healthy shape; four is over-committed. If you find yourself with four bets in year 1, pick the weakest and move it to year 2 as a hedge with a flip signal.
- **Every hedge must have a decision date and a flip signal, both concrete.** An indefinite hedge is not a hedge; it is a bet at low scale you have not admitted to. Chapter 3's discipline applies.
- **Every not-in-window row must have a revisit condition.** Even the honest *"this direction is closed for the full window"* answer needs a criterion that would bring it back. Chapter 3's defense 3.
- **The non-goal register is not the one-pager's non-goals section.** The one-pager has 3–5 non-goals across the entire portfolio. Section 7 of this exercise has 3–5 *per row*, for a total of 15–25. This is the *full* register.
- **Each sunset criterion needs all three parts.** Chapter 4's three parts are non-negotiable. If any part is missing, the criterion is decoration.
- **Cite chapter numbers as you go.** Same as exercise-02.
- **When the peer platform-side dependency is uncertain, say so.** The mod-504 material handles the cross-org conversation; for this exercise, an honest *"pending cross-check with the platform principal on X"* is a real note, not a gap.

## Acceptance criteria

Your document is done when it can pass all of the following:

- [ ] The 5×3 grid is filled in, in chapter-2 row order and year order, with one of `bet` / `hedge` / `option` / `not-in-window` in every cell.
- [ ] Year-1 bet count is between 1 and 3, inclusive; the count is stated explicitly.
- [ ] Every year-1 bet has a timeliness paragraph naming why the bet is year 1, not year 2, on a rising-cost-of-delay argument.
- [ ] Every hedge has a named flip signal and a named decision date, both in the current fiscal window or the next.
- [ ] Every option has a named preserved-substrate cost, referring to specific architectural discipline in the north-star architecture (mod-503).
- [ ] Every not-in-window row has a named revisit condition, framed as a review not an activation.
- [ ] The peer-platform-side cross-check paragraph names each year-1 bet's platform dependencies or explicitly notes uncertainty.
- [ ] The non-goal register has 3–5 concrete refusals per row, each with a named consequence and time-boxed to the window; total 15–25 non-goals.
- [ ] Every row's sunset criteria are named, and each has all three parts — triggering condition, review cadence, defined exit action.
- [ ] Nowhere in the document do fiscal-quarter delivery dates, per-team owners, or numeric OKR percentage targets appear.

## Stretch goals

- **Adversarial staff-engineer readback.** Have a peer play a staff engineer on one of the affected teams. Give them section 1 (the grid), the relevant row's non-goals, and the row's sunset criteria. Ask them to draft one paragraph of their next-quarter plan. If they can do it, section 3 works; if not, revise until they can.
- **Second-shape grid.** Author a *second* grid for the same org where you change exactly one year-1 bet from `bet` to `hedge` (or from `hedge` to `bet`). Argue the second sequence against the first. Which is more defensible, and why?
- **Sunset-execution simulation.** Pick one row's sunset criterion, imagine the triggering condition just fired, and write the two-paragraph exit-action narrative you would post to the org's docs. Does the exit action as written actually resolve unambiguously, or are there gaps? Refine.
- **Pair-test with the one-pager.** Compare exercise-01's non-goals section (3–5 bullets) against section 7's non-goal register (15–25 bullets). Are the one-pager's non-goals the correct *most-important* subset? Refine either artifact until the two are consistent.

## Deliverable location

Local workspace. This is one of the two substantive halves of the deep-dive companion doc; the other is exercise-02. When both are complete, they combine into the deep-dive's sections 3, 4, 10, and the sequencing table for section 4 of chapter 7.
