# Non-Goals and Sunset Criteria — The Discipline That Makes the North Star Defensible

> Chapter 4 of mod-502. Prerequisite: chapters 2 (the five-row bet portfolio) and 3 (sequencing). Downstream: chapter 6 handles the signal that would fire a sunset criterion; chapter 7 packages non-goals and sunsets into the one-pager and the deep-dive.

## Why non-goals and sunset criteria are the whole game

Chapter 1's test for whether a document is a *North Star* rather than a *manifesto* was falsifiability. This chapter is where that test is operationalised. A bet portfolio without explicit non-goals reads as *"we like these five things"*; the same portfolio with explicit non-goals reads as *"we chose these five things, and we chose them over these seven other things, and here is the criterion under which we would reverse the choice"*.

The discipline has two halves.

- **Non-goals** attach to a bet at the moment the bet is committed. They name what the bet is *not*, and what the org will *not* fund, hire for, or optimise for as a consequence of committing the bet. They are the negative-space definition of the bet.
- **Sunset criteria** attach to a bet across its lifetime. They name the observable event that would end the bet — not because it failed, but because the environment changed in a way that made the bet the wrong bet. They are the exit protocol for the bet.

Both are unusual to write at first because they force a real *decision*, not an aspiration. The rest of this chapter walks through how to write each half well.

## Non-goals — the negative-space definition of a bet

A well-written bet has a matched set of non-goals that discipline it. Concretely, that means: for every affirmative claim the bet row makes, there is a corresponding claim on the *opposite* side that the org is choosing not to make.

Take the Gen-AI bet row from chapter 2's worked example (adopt frontier APIs for two consumer surfaces; post-train mid-tier open-weights model on one enterprise surface; do not train from scratch). The affirmative side is three specific commitments. The non-goal side, written well, would name at least four things:

- We will **not** fund a foundation-model pretraining program in this window. Rationale: economics do not clear against workload volume; see the row 4 not-in-window explanation.
- We will **not** invest in a per-workload custom prompt-template DSL. Rationale: locks the org into a single provider's abstraction; conflicts with the row's flexibility premise.
- We will **not** allow ad-hoc per-team supplier evaluations. Rationale: fragments the org's frontier-API position; the mod-503 canonical API for the inference gateway is the one place suppliers are evaluated.
- We will **not** treat data-residency-constrained workloads as candidates for API adoption; they go to the post-training track. Rationale: the whole reason the mid-tier post-training program exists.

Each of these non-goals *does* something in the document. They pre-empt requests for exceptions ("can our team spin up its own Gemini eval?"), they prevent silent scope creep (the day-two request to fund a DSL), they draw the seam clearly enough that a staff engineer building the quarterly roadmap knows what is out.

### Writing non-goals well

Three properties every well-written non-goal has.

**Concrete refusal.** A non-goal names a specific action or investment the org is not making, not a general disposition. *"We don't invest in speculative research"* is not a non-goal; it's a vibe. *"We do not fund a foundation-model pretraining program in this window"* is a non-goal.

**Named consequence.** A non-goal that has no downstream implication is decorative. Each non-goal should be traceable to *something the org would otherwise do* — an RFC that would otherwise get approved, a hire that would otherwise get made, a budget line that would otherwise get funded, an experiment that would otherwise get run.

**Time-boxed to the window.** Non-goals apply to the 3-to-5-year window, not forever. Say the window explicitly. This matters because a *"we do not do X"* without a window is a manifesto claim; a *"we do not do X in the FY26–FY30 window"* is a bet.

### The non-goal set as a coherence check

A helpful check: read the non-goals as a *set*, ignoring the affirmative bet rows. Do they cohere? Does the picture of "what the ML org is not doing" hang together into a defensible org identity?

If the non-goal set includes both *"we do not fund a foundation-model pretraining program"* and *"we do not adopt frontier APIs for the enterprise product area"*, the reader is left with a coherent picture of the org's Gen-AI posture (invest in adopted-and-post-trained mid-tier, on the enterprise side; invest in frontier APIs on the consumer side). If the non-goal set includes both *"we do not fund a foundation-model pretraining program"* and *"we do not adopt any external Gen-AI capability"*, the reader is left with an incoherent picture, and the North Star has an internal contradiction.

## Sunset criteria — the exit protocol for a bet

Every bet in the North Star has a natural life. Some end because they succeed and the direction stabilises into a run-rate. Others end because the environment shifted, the falsification signal fired, or a better direction opened up. Sunset criteria are how the North Star pre-commits to *how the bet ends* — including the second case, the harder one.

A sunset criterion has three parts.

- **A triggering condition.** Specific and observable. *"If frontier API price per million tokens rises by ≥3x on the two-year forward curve"* is a triggering condition. *"If the environment changes materially"* is not.
- **A review cadence.** How often the triggering condition gets evaluated. Typical: at each half-year North Star refresh, plus an emergency evaluation if a chapter-6 signal fires between refreshes.
- **A defined exit action.** What the org does when the condition fires. Freeze new investment, wind down existing investment on a named schedule, migrate consumers of the underlying substrate, ratify the exit with the peer platform-side principal and Head of AI Governance.

Without all three parts, a sunset criterion is decoration. With all three, it is a governance artifact.

### The specific hardnesses of sunset writing

**The hard case is not "the bet failed".** A bet that fails has an obvious exit — you kill it. The hard case is a bet that is *working* but the environment shifted such that continuing to fund it is the wrong org-scope call. That is the case sunset criteria are for. The Gen-AI row's sunset for the in-house post-training program on a workload where frontier API pricing has crossed under fully-loaded per-token cost of the in-house model — that is a working bet becoming the wrong bet. Writing the criterion is how you pre-commit to the exit before the sunk-cost pressure kicks in.

**The hard case is not "one metric moved".** A sunset that fires on a single point-in-time metric is fragile. Sunsets are structured on *sustained shifts* or *step-changes* — the two-year forward curve, the compute-generation transition, the regulatory-framework release. Chapter 6 handles the signal-quality side.

**The hard case is the political case.** The sunset criterion for a bet the CEO announced at an all-hands is harder to write than the sunset criterion for a bet nobody personally owns. The way to write it anyway is to *frame the criterion at the time the bet is committed* — before there is a coalition around it. That is why the sunset criteria live in the North Star, not in the quarterly-review deck.

### Sunset criteria by row

Illustrative examples for each of chapter 2's five rows.

**Row 1 (Gen-AI).** Sunset the in-house post-training program on a specific workload if frontier API pricing per million tokens falls below fully-loaded per-token cost of the in-house model *at expected FY-end volume*, sustained over two consecutive quarters. Sunset the frontier-API adoption bet if a supplier's terms materially degrade against the org's data-residency contract with the top regulated-customer segment, or if a downstream competitor gains a compounding advantage the org's abstraction layer cannot close.

**Row 2 (RecSys / personalization).** Sunset the converged-substrate direction if the migration cost of any single product-area stack rises above the two-year benefit envelope, sustained across the next planning cycle; ratify with the platform-side principal. Sunset the Gen-AI-based query-understanding hedge if the eval signal after two consecutive quarters shows no meaningful engagement or quality lift, and if the compute cost of the eval-passing configuration exceeds the classical baseline by >2x.

**Row 3 (Agentic-AI).** Sunset the internal-tooling agent investment if, after the year-1 evaluation period, the agents do not clear the productivity or reliability bar set in the shared eval harness; retire the agents to the RAG-only or classical-pipeline substrate. Sunset the customer-facing-agentic option if the reliability profile at the org's SLA does not narrow over the year-2 window.

**Row 4 (Foundation-model program / not-in-window).** Trigger a revisit — not an activation — if (a) data-residency or contract-restriction signal makes API adoption infeasible for ≥30% of workloads by revenue, or (b) frontier API pricing per million tokens rises by ≥3x on the two-year forward curve, or (c) unique-data value in an enterprise product area rises to a scale that a mid-tier post-training program cannot capture. The revisit is a chapter-6 escalation, not an automatic bet upgrade.

**Row 5 (MLOps as org contract).** Sunset a named exception to the paved-road contract when the reason for the exception no longer holds (e.g., the online-learning ranking surface no longer requires the deviation); consumers of the exception migrate onto the shared substrate on a named schedule. Sunset the responsible-AI review gate's tier definitions when the regulatory framework changes materially (EU AI Act delegated act updates; NIST AI RMF revisions; state-level enactments) — chapter 6 tracks the shifts.

## The two rejected shapes: perpetual bet, ambiguous exit

Two anti-patterns dominate the shape of a first-draft North Star. Naming them explicitly helps you refuse them.

### The perpetual bet

A bet with no sunset criterion is a perpetual bet. The reader — and, worse, the staff engineers building against the bet in their quarterly roadmaps — is left with the impression that the direction is a permanent property of the org. That impression is what turns *"we invest in RecSys"* into *"we invest in RecSys forever"*, which is what makes it hard to reverse when the environment shifts.

The fix is to add the sunset criterion. Even the criterion *"this bet does not sunset in the 3-to-5-year window; revisit only under scenario X"* is a real sunset criterion — a null one, but written down and defensible.

### The ambiguous exit

A bet with a sunset criterion but no *exit action* is an ambiguous exit. The trigger fires; nobody knows what happens next. The org's coalition around the bet keeps funding it; the falsification signal was ignored; the exit protocol never activates.

The fix is to name the exit action — including who ratifies, on what cadence, and what the wind-down looks like. Mod-504 material walks through the coalition-side of executing a sunset; this chapter's job is to ensure the North Star has the pre-committed language the coalition can appeal to.

## How non-goals and sunset criteria live in the two artifacts

Chapter 7 walks through the one-pager and deep-dive companion artifacts in full. For now, the relevant discipline is:

- The **one-pager** carries the *non-goals* (as a short list under the bet portfolio) and a one-line signal per bet on the sunset criterion. It does not carry the exit-action detail. Executives read what the bet is *not* faster than they read what it *is*; the non-goals give them the shape.
- The **deep-dive companion** carries the full sunset criteria with all three parts (triggering condition, review cadence, exit action) per row. Staff engineers use the deep-dive to understand the exit protocol so their quarterly roadmaps do not commit to work that will be un-committed under a fireable trigger.

## Summary

- Non-goals are the negative-space definition of a bet. Every bet has a matched set of non-goals: concrete refusals with named consequences, time-boxed to the window.
- The non-goal set as a whole should cohere — read together, it should describe a defensible org identity.
- Sunset criteria are the exit protocol: a triggering condition, a review cadence, and a defined exit action. Without all three, a sunset is decoration.
- Sunset criteria are hardest to write for working bets in shifting environments; that is the case they exist for.
- The one-pager carries non-goals and sunset signals; the deep-dive carries full sunset criteria with exit actions. Chapter 7 packages the pair.
- Chapter 6 handles the signal that would fire a sunset criterion — the industry, regulatory, and internal signals the tracker watches.
