# The Staff-Scope Portfolio Roadmap Versus the Principal-Scope North Star

> Chapter 5 of mod-502. Prerequisite: chapters 1–4 in this module; mod-501 chapter 6 (hand-off contracts). Downstream: chapters 6 and 7 assume this seam is settled.

## Why this chapter has to exist

Every principal-scope learner coming out of a strong staff-scope background has already authored — often more than once — a multi-quarter portfolio roadmap for the ML function. The roadmap goes to the VP, decomposes into per-team quarterly plans, and is the artifact leadership committed to before the current fiscal year began. It is a serious, high-quality artifact. It is also — critically — not a multi-year org-scope North Star.

The most common failure mode when a staff engineer starts drafting at principal altitude is that the North Star comes out as a longer, glossier portfolio roadmap. The bets are dated to specific fiscal quarters. The metrics are the current fiscal year's OKR metrics. The audience is the VP the writer already reports to. The horizon is 18 months. Each of those choices *is a slip* from the principal-scope altitude down to the staff-scope altitude. Mod-501 chapter 6 named this failure mode as *re-doing staff scope*. This chapter draws the specific seam between the two artifacts so you can spot the slip in your own draft.

## The two artifacts, side by side

| Dimension | Staff-scope portfolio roadmap | Principal-scope North Star |
|---|---|---|
| Primary audience | VP (typically the ML function's VP) | CEO / CTO / SVP; board of directors indirectly |
| Horizon | Multi-quarter — typically 4 to 6 quarters | Multi-year — 3 to 5 years |
| Unit of commitment | Quarter | Bet |
| Scope | The ML function's *portfolio* (3–5 production ML systems) | The ML function *across all product areas* |
| Load-bearing content | Delivery milestones on the fiscal calendar; team owners; per-quarter dependencies | Bet portfolio with non-goals and sunset criteria; industry-signal tracker; direction leadership can quote |
| Falsifiability shape | Milestones slip; teams re-plan | Bets sunset; industry signal fires |
| Refresh cadence | Quarterly | Twice a year, plus emergency refresh on falsification-signal trigger |
| Author | Staff engineer(s); ratified by VP | Principal engineer; ratified by CTO / SVP |
| Owned in this ecosystem by | `staff-ml-engineer-learning` mod-410 (portfolio-scope roadmap authoring) | `principal-ml-engineer-learning` mod-502 (this) |

Every row is load-bearing. Miss one, and the two artifacts blur.

## The seam — how the two artifacts fit

The portfolio roadmap does not disagree with the North Star. It **decomposes into it**. Every commitment on the roadmap is traceable to a bet on the North Star; every bet on the North Star is decomposable into commitments across one or more roadmaps.

Concretely, the seam looks like this:

- The North Star has five bet rows (chapter 2). Two or three are year-1 bets (chapter 3). Each of those has non-goals and sunset criteria (chapter 4).
- The portfolio roadmap for the ML function's current fiscal year names, per team, the quarterly deliveries that advance one or more of the year-1 bets. It also names any load-bearing operational work — reliability, cost, migration — that does not advance a specific bet but keeps the function running.
- A staff engineer looking at the portfolio roadmap can trace every non-operational commitment back to a specific North Star bet. If a commitment does not trace back, either the commitment shouldn't be there or the North Star is missing a row.
- A principal engineer looking at the North Star can look at the current portfolio roadmap and ask: *does this roadmap decompose the year-1 bets accurately, given what the function's staff engineers know about the systems today?* If it doesn't, either the roadmap is off or the year-1 bet was set at the wrong altitude.

The two artifacts are in continuous conversation. Neither replaces the other. The rules of the conversation matter: the North Star does not tell the roadmap which quarter a specific delivery happens; the roadmap does not tell the North Star which direction to bet on. Each stays in lane, cites the other, and the seam holds.

## What lifts and what does not

For a learner making the transition, the useful move is to look at your last strong portfolio roadmap and ask, section by section, *what lifts to a North Star and what stays in the roadmap*.

### The multi-quarter delivery calendar does not lift

Fiscal-quarter delivery dates belong in the roadmap. They do not belong in the North Star. A quarterly commitment date on a North Star bet is a category error: the North Star names the direction; the roadmap names the schedule.

If your North Star draft has fiscal-quarter dates on the bets, cut them and move the underlying work to the roadmap.

### The team-and-owner assignment does not lift

Team assignments belong in the roadmap. A named principal or staff owner belongs in the North Star, but only at the level of *who ratifies the bet* — not per-team delivery ownership.

If your North Star draft has team names next to bets, cut them; the roadmap owns team assignments.

### The current-year OKR metric set does not lift

OKR metrics belong in the roadmap and in the OKR document, not in the North Star. The North Star names *directional commitments*: what capability, what posture, what boundary. A specific numeric target ("engagement +6%") for the current year is roadmap-scope.

If your North Star draft has percentage targets on bets, cut them; the metric *commitment* (e.g., "engagement + long-term-retention composite, not click-through") lifts, but the *numeric target* stays in the roadmap.

### The bet framing does lift

A row of the roadmap that reads *"invest in shared feature substrate across ranking teams"* becomes a bet on the North Star at higher altitude: *"converge feed / search / notifications retrieval + reranking onto a shared substrate"* — with the sunset criterion, the non-goal for ads-ranking federation, and the timeliness argument (chapter 3) attached.

### The industry-signal watch does lift, expanded

A roadmap that already tracks a small number of external signals ("watch for the next Llama release", "watch for the next EU AI Act delegated act") already has the seed of a chapter-6 falsification tracker. On the North Star it becomes a formal tracker with defined signal categories, decision cadence, and named signals per bet. Chapter 6 handles this.

### The horizon extends

A roadmap covers 4–6 quarters. A North Star covers 3–5 years. Everything in the roadmap between quarter 4 and quarter 6 is speculative and the roadmap is honest about that; the North Star's year-4 and year-5 rows are also speculative and the deep-dive companion doc is honest about that. Both artifacts respect the horizon at which they can commit.

## The specific hand-off contract, restated

Mod-501 chapter 6 named the hand-off contract at general level. Here is the version specifically for the portfolio-roadmap-vs-North-Star seam.

**Staff owns.**

- The multi-quarter portfolio roadmap for the current and next fiscal year.
- The quarterly delivery milestones per team, per product area.
- The OKR metric decomposition.
- The team-scope architecture RFC that grounds each portfolio row.
- The delivery-risk register and the mitigation plan.

Ratified by the VP; feeds inputs into the North Star refresh cycle.

**Principal owns.**

- The multi-year North Star document.
- The bet portfolio (chapter 2), sequenced (chapter 3), with non-goals and sunset criteria (chapter 4).
- The industry-and-internal falsification signal tracker (chapter 6).
- The one-pager and deep-dive companion doc (chapter 7).

Ratified by the CTO / SVP; feeds the shape of the roadmap that staff authors.

**Jointly owned.**

- The North Star refresh cadence (twice a year plus emergency triggers). Principal calls the cadence; staff supplies the ground truth from the roadmap.
- The non-goal list. Principal writes it; staff pressure-tests it against roadmap reality ("this non-goal implies we cut a commitment we already made").
- The reverse-check on year-1 bet decomposition. Principal sets the year-1 bet; staff answers whether the roadmap can decompose it *this* fiscal year vs. next.

**Escalation.**

- Staff disagrees with a year-1 bet's decomposability: staff surfaces in the pre-refresh review; principal weighs. If unresolved, principal escalates to VP with the specific decomposition disagreement; VP either commits capacity or asks the principal to move the bet to year 2.
- Principal disagrees with a roadmap commitment that appears to advance a non-goal: principal surfaces in the roadmap review; VP weighs. If unresolved, principal escalates to CTO / SVP with the non-goal citation. Staff does not have to defend the commitment; the VP does.

That escalation path is what keeps the two artifacts in productive tension rather than in silent parallel drift.

## When the seam has broken

You can diagnose a broken seam quickly from either side.

**From the roadmap side.** Look at the top ten commitments on the current roadmap. For each, can you name the specific North Star bet it decomposes? If more than two commitments have no North Star bet behind them, the North Star is missing rows *or* the roadmap has drifted into non-strategic operational load. Both are worth surfacing to the ratifying VP.

**From the North Star side.** Look at each year-1 bet. Can you name the specific roadmap commitments — teams, quarters, deliverables — that advance the bet in the current fiscal year? If any year-1 bet has no roadmap decomposition, the bet was set but the org is not moving on it. The bet either needs to be moved to year 2 (be honest) or the roadmap has to update in the next refresh cycle.

Both diagnoses are useful working artifacts on their own — the exercise-05 assignment is essentially the North-Star-side diagnosis run against a real roadmap you or a peer has authored.

## Common failure modes at the seam

- **The North Star is a longer roadmap.** Symptoms in chapter 5's earlier section. Fix: strip the calendar, team owners, and numeric OKR targets; commit to bets, non-goals, and sunsets.
- **The roadmap ignores the North Star.** Symptoms: the roadmap advances directions the North Star quietly closed off; the North Star is a wall decoration nobody references at planning. Fix: enforce the "every non-operational roadmap commitment traces to a bet" rule at the next planning cycle; refresh the North Star if the drift indicates the North Star was already stale.
- **Both artifacts have the same author.** In small orgs, the principal and the top staff engineer are the same person. The seam still exists — you switch hats between artifacts. The load-bearing discipline is to keep two documents, not one, and to be explicit about which artifact you are writing in at any moment. Merging them into one document is the same as not having the North Star.
- **The North Star updates on the roadmap's cadence.** If the North Star refreshes every quarter, it is a longer roadmap. If it refreshes once every 18 months, it is a museum piece. Twice a year plus emergency refresh (chapter 6 handles emergencies) is the sample-supported cadence.

## Summary

- The portfolio roadmap and the North Star are different artifacts with different audiences (VP vs CTO / SVP), horizons (4–6 quarters vs 3–5 years), units of commitment (quarter vs bet), and falsification shapes (milestone slip vs sunset trigger).
- The two artifacts are in continuous conversation. The roadmap decomposes the North Star; the North Star shapes the roadmap.
- Certain things lift from roadmap to North Star (bet framing, industry-signal watch); certain things stay in the roadmap (fiscal calendar, team owners, OKR percentage targets).
- The hand-off contract has specific rows for staff-owned, principal-owned, jointly-owned, and escalation. Write it down and revisit at each refresh cycle.
- Diagnose a broken seam from either side by tracing commitments to bets; act on the diagnosis at the next refresh.
