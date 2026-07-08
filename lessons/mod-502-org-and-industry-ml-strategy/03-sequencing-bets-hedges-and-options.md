# Sequencing Bets, Hedges, and Options Across the Multi-Year Window

> Chapter 3 of mod-502. Prerequisite: chapter 2 — the five-row bet portfolio. Downstream: chapter 4 attaches non-goals and sunset criteria to each row; chapter 6 handles the signal that would move a bet from *hedge* to *bet* or from *bet* to *sunset*.

## Why sequencing is the load-bearing move

A North Star with five rows and no sequencing is a wishlist. It says *"we will invest in Gen-AI, RecSys, agentic AI, MLOps discipline, and (maybe) a foundation-model program"* — and, absent a sequence, the reader has no way to tell what leadership is actually committed to next year, what is on hold for year two, or what is being reserved as an option. Every one of the five rows can plausibly be a year-one bet; not all five can be, because the org has a finite headcount, a finite capital budget, and a finite executive attention span.

Sequencing is the discipline that turns the five-row portfolio into a defensible multi-year plan. The output of this chapter is a small vocabulary for what each row *is* in a given year — a **bet**, a **hedge**, an **option**, or a **not-in-window** — and a rubric for defending the assignment.

## Vocabulary

Each row in each year of the 3-to-5-year window is one of four states.

### Bet

**Definition.** The org is actively investing. Named funded team(s), a named principal / staff owner, a multi-quarter delivery commitment inside the year, and a place on the executive-review cadence. The bet is expected to move the org's technical position by year-end.

**Signals it is a bet, not a hedge.** Delivery milestones are on the fiscal calendar. Staff-scope roadmaps for the ML function decompose to it. The peer platform-side principal track's roadmap (`ai-infra-principal-engineer-learning`) knows about it. The CFO's capacity model knows about it. The Head of AI Governance's review-body agenda knows about it.

**Number.** Two to three of the five rows should be bets in year 1 for a healthy portfolio. Four bets is over-committed; five bets is a wishlist. Zero or one bet is undercommitted; the North Star was written but the org is not actually moving on it.

### Hedge

**Definition.** The org is investing at exploratory scale — one team, or one small cross-team effort, or one bounded experiment — with an *explicit intent to upgrade the hedge to a bet if a specific signal fires* (chapter 6). A hedge is not the same as a bet at low scale; a hedge is a decision to *preserve optionality* against a future acceleration signal.

**Signals it is a hedge, not a bet.** No multi-quarter delivery commitment tied to the fiscal calendar for the org-scope direction; instead, a small delivery commitment inside a bounded experiment. The row's sunset criterion (chapter 4) includes a decision date on which the hedge either upgrades to a bet or retires.

**Number.** One to two hedges per year is typical. More than two, and the org is spreading executive attention too thin across not-yet-decided directions.

### Option

**Definition.** The org is *not* investing in the direction, but is *preserving the ability to invest later*. Concretely, that means keeping the substrate the direction would rely on healthy (canonical APIs from mod-503 still compose against it; the platform-side track has not walled it off; no organisational commitment to a competing direction pre-empts a future reversal). No engineering effort is scheduled against the option; the cost is discipline in the substrate.

**Signals it is an option, not a hedge.** No team is assigned. No experiment budget is allocated. But the north-star architecture (mod-503) explicitly *does not* foreclose the direction, and the North Star deep-dive companion doc names the conditions under which the option would be exercised.

**Number.** Zero to two options per year, on rows that would be too costly to hedge but too consequential to close off.

### Not-in-window

**Definition.** The org has considered the direction and is explicitly *not* pursuing it in the 3-to-5-year window. The row is written into the North Star with a one-sentence *why not, and what would change it*. This is a bet — a bet *against* the direction.

**Signals it is a genuine decision, not an omission.** The row appears in both the one-pager and the deep-dive. The decision has a defensible rationale a peer VP could disagree with substantively. The falsification signal chapter 6 tracks for this row is real, not perfunctory.

**Number.** Zero to two rows in this state is normal; the foundation-model program row (row 4) is often here for orgs that are not AI labs.

## Assigning states across a five-row × three-year grid

The exercise is simple in shape: for each of the five rows, and for each of years 1, 2, and 3 in the 3-to-5-year window, assign one of `bet`, `hedge`, `option`, `not-in-window`. That produces a 5×3 grid. Years 4 and 5 remain in the deep-dive companion but do not appear as commitments in the one-pager — they are signal, not commitment.

A defensible grid has the following properties.

**Sum of bets across all rows in year 1 ≤ 3.** More than three concurrent org-scope bets exceeds executive attention. If your draft has four year-1 bets, one of them is a hedge or a bet you have not yet clarified.

**No row is a `bet` in year 1 if the substrate it needs is a `not-in-window` on the peer platform-side track.** This is the coherence check with the peer principal's portfolio. If your Gen-AI row is a year-1 bet on adopting frontier APIs but the platform-side principal has *not-in-window* their inference-gateway build, one of you is wrong. The North Star is where you catch it.

**Every row that is a `hedge` in year N should have a decision date in year N or N+1 that resolves it to `bet` or retirement.** A hedge that runs indefinitely is a bet at low scale in disguise; call it what it is.

**Every row that is an `option` in year N should have the substrate cost of preserving the option named in the north-star architecture (mod-503) chapter on canonical APIs.** Options are cheap in headcount and expensive in architectural discipline; the discipline has to appear somewhere concrete.

## Defensibility — how to argue the sequence

The North Star is going to face a CTO / SVP audience in mod-504's material and in the project-501 capstone. The sequence is where they will push hardest, because the sequence is where the visible cost of the direction lives.

Three defenses land. Anticipate each one in the draft.

### Defense 1 — "Why is this a year-1 bet instead of a year-2 bet?"

The load-bearing answer is a *timeliness* argument, not a *readiness* argument. A capability the ML function *could* deliver in year 1 is not the same as a bet that *has* to happen in year 1. The bet is year 1 if the cost of *not* investing rises faster than the cost of *investing* — the direction gets harder to enter later, competitors gain compounding advantage, a substrate lock-in window closes, or the falsification signal for the alternative has already fired.

Write the two-sentence timeliness argument into every year-1 bet. If the argument reduces to "we are ready" or "we want to", the bet is not a year-1 bet; it is a year-2 bet you have not yet argued.

### Defense 2 — "Why is this a hedge instead of a bet?"

The load-bearing answer is *falsifiability* — the specific signal that would flip the hedge to a bet, and the decision date the hedge resolves on. If the answer to "why is this a hedge?" is "we're not sure yet", the hedge is a bet-in-waiting; write the signal that would sharpen the decision, and put a date on it. Chapter 6 handles the signal side; chapter 4 handles the decision-criterion side.

Write the flip-condition and the decision date into every hedge. If neither exists, the hedge is either a bet you have not committed to or an option you have overscoped.

### Defense 3 — "Why is this not in the window at all?"

The load-bearing answer is the *falsification signal* that would *bring it into* the window. A row in `not-in-window` state without a falsification signal reads as a shrug; a row with an explicit falsification signal reads as a bet against the direction with a named revisit condition. Chapter 6's tracker is where the signals live; the North Star row cites them.

Write the revisit condition into every `not-in-window` row. Foundation-model program (row 4) is the most common home for this defense; do it well there.

## Two worked example grids

For grounding — the same five-row portfolio, sequenced two different ways for two different orgs. Both are defensible; each one is defensible *for its org*.

### Example A — a consumer-recommendations-heavy org (Pinterest-shape, Snap-shape, Ibotta-shape)

|              | Year 1 | Year 2 | Year 3 |
|---|---|---|---|
| Gen-AI direction | **bet** — API-integration for two consumer-facing surfaces | **bet** — extend to a third surface; post-training experiment on the enterprise-adjacent surface | **bet** — post-training experiment upgrades to a program if signal fires |
| RecSys / personalization | **bet** — converged retrieval + reranking substrate across feed / search / notifications | **bet** — Gen-AI query-understanding upgrade; ads stays federated | **bet** — evaluate consolidation of ads if attribution model changes |
| Agentic-AI | **hedge** — two internal-tooling agents with shared eval harness; decision date end of year 1 | option or bet contingent on year-1 hedge outcome | contingent |
| Foundation-model program | **not-in-window** — API adoption breakeven does not clear at any scenario in the plan | not-in-window unless signal fires | not-in-window |
| MLOps as org contract | **bet** — establish paved-road contract; two named exceptions | **bet** — extend contract to responsible-AI review gate | **bet** — evolve contract for EU AI Act tier-2 systems |

Three year-1 bets, one hedge, one not-in-window. The load-bearing timeliness argument: the shared substrate has to be adopted before the org's product-area count grows by 30% under the FY26 plan, or the migration cost compounds. The RecSys row is a year-1 bet, not a year-2 bet, on that basis.

### Example B — an enterprise-fintech org (Capital One-shape, Upstart-shape)

|              | Year 1 | Year 2 | Year 3 |
|---|---|---|---|
| Gen-AI direction | **bet** — post-training program on mid-tier open-weights model for data-residency-sensitive workloads; API adoption for lower-tier workloads | **bet** — extend post-training program to two more workloads | **bet** — evaluate frontier-parity of post-trained model against updated API baseline |
| RecSys / personalization | **hedge** — bounded investment on next-best-action ranking for retention; decision date end of year 2 | contingent | contingent |
| Agentic-AI | **bet** — customer-support triage agent as differentiator; strong guardrails and eval investment | **bet** — extend to underwriting-decision assistant with heavier review | **bet** — evaluate customer-facing agentic surfaces |
| Foundation-model program | **option** — preserve substrate ability to move to pretraining if data-residency landscape hardens further | option | option or bet contingent on signal |
| MLOps as org contract | **bet** — establish paved-road contract with EU AI Act tiering already applied; strong review gate | **bet** — extend contract to model-risk-management alignment | **bet** — evolve for state-level regulatory posture |

Three year-1 bets, one hedge, one option. Different shape than example A, because the org's regulatory posture and workload mix make the foundation-model program worth preserving as an option and make agentic AI worth committing to as a differentiator rather than hedging.

Both grids are legitimate outputs of this chapter. Neither is "the right answer"; each is *the right answer for its org and defensible against its specific counterargument*.

## The peer platform-side principal's grid

The North Star's sequence has to be *coherent with* the peer platform-side principal's mod-505 (long-term technical bets) grid. That module sequences platform bets (capacity substrate, training-platform build-vs-adopt, inference-serving substrate, developer-experience contracts, org-wide reliability discipline) on the same 3-to-5-year window. Every modelling bet in this chapter has a platform-substrate dependency in that chapter's grid, and vice versa.

The workable practice is: when the two principals draft the North Star and the platform bets in the same cycle, they cross-check the grids together, both defend to CTO / SVP together, and the seams are named in *both* documents. The mod-504 material (cross-org influence) walks through the practice.

## Common failure modes

- **Too many year-1 bets.** Four or five year-1 bets always mean the sequence has not been made. The org will de-prioritise on the fly, and the North Star will lose credibility mid-year. Cut to three.
- **Hedges without decision dates.** A hedge that runs indefinitely at exploratory scale is not a hedge; it is an underfunded bet the org is embarrassed about. Give the decision date and the flip signal.
- **Not-in-window without a revisit condition.** A `not-in-window` row without a falsification signal reads as neglect. Even if the revisit condition is *"this direction is closed for the full window, revisit only if the org's product portfolio changes shape"* — say that.
- **Coherence break with the peer platform-side grid.** The most costly failure is a modelling year-1 bet that the platform-side grid does not know about. Cross-check.
- **Sequencing that reads as a resource-allocation puzzle.** The audience is CEO / CTO / SVP; the sequence has to defensibly *shape the org's direction over years*, not merely fit the FY26 capacity plan. If the sequence is what an FP&A analyst would produce, the altitude is wrong.

## Summary

- Each of the five rows in each of the 3 near-term years takes one of four states: bet, hedge, option, not-in-window.
- Two to three year-1 bets is the healthy shape; one to two hedges; zero to two options; zero to two not-in-window rows.
- Every bet has a timeliness argument; every hedge has a flip signal and a decision date; every option has a preserved-substrate cost; every not-in-window row has a revisit condition.
- The grid is coherent with the peer platform-side principal's mod-505 grid — cross-check.
- Chapter 4 turns the sequence into the non-goals-and-sunset-criteria layer that keeps the sequence honest.
