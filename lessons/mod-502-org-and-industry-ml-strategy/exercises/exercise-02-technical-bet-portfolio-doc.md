# exercise-02: Technical Bet Portfolio Doc

**Estimated effort:** 3 hours

## Objective

Produce the five-row technical bet portfolio at bet altitude for the org you are writing for. This is the *content* of section 3 of the deep-dive companion doc (chapter 7) and the substrate that exercise-03 sequences into a multi-year roadmap. The output is a five-page artifact — one page per row — with each row written at bet altitude and citing (not duplicating) the specialist-track and staff-track material underneath.

## Prerequisites

- Chapter 2 read and internalised — the five-row shape, the bet-vs-implementation altitude distinction, the hand-off contracts per row.
- Chapter 5 skimmed so you can enforce the roadmap-vs-North-Star seam while drafting.
- Mod-501 chapter 6 read — the hand-off contracts to staff scope. Every row you write cites these.
- The same org context you chose for exercise-01 (or, if you are doing exercise-02 first, an org context you can defend).
- Familiarity with the peer specialist-track scopes named in chapter 2 (`fine-tuning-engineer-learning`, `training-pipeline-engineer-learning`, `agentic-ai-engineer-learning`, `rag-engineer-learning`, `ai-infra-ml-platform-learning`, etc.) — enough to name them accurately in each row's hand-off list.

## Problem statement

You are drafting the deep-dive companion's bet-portfolio section for the org's ML North Star. Every row has to be written at bet altitude — the altitude a CTO / SVP can ratify and a staff engineer can build a fiscal-year roadmap from — without slipping into the implementation depth the specialist tracks own.

Each row has a specific job:

- Name the bet at principal altitude, not team-scope.
- Attach non-goals that make the bet a decision rather than an aspiration (chapter 4).
- Attach sunset criteria with a triggering condition, a review cadence, and a defined exit action.
- Name the specialist and staff tracks the row hands off to for implementation depth. Cite; do not duplicate.
- Distinguish itself from the peer platform-side principal's mod-505 platform-bet portfolio: when a row depends on a platform bet, name the dependency; when a row *is* a platform bet, note that it is not in scope for this document.

## Requirements

Produce a single markdown file, `exercise-02-bet-portfolio.md`, in a personal workspace (do not commit into this curriculum repo). Structure it as follows.

- **A single H1 title** naming the artifact ("<Org> ML Bet Portfolio (FY26–FY30) — Deep-Dive Section").
- **A one-paragraph header** naming the org, the horizon, and the parent document (the exercise-01 one-pager or the eventual deep-dive companion). No more than five sentences.
- **Five H2 sections**, in the chapter-2 row order:
  1. Row 1 — Gen-AI direction
  2. Row 2 — RecSys / personalization direction
  3. Row 3 — Agentic-AI direction
  4. Row 4 — Foundation-model program / large-scale fine-tune direction
  5. Row 5 — MLOps as org contract
- **Each H2 has the same six subsections**, in order:
  1. **Bet framing.** One paragraph at bet altitude. What the org is committing to, over what horizon, at what scope. Cite the chapter-2 shape.
  2. **Rationale.** Two to four sentences. Why this bet, this org, this window. Include at least one specific piece of org-relevant context (workload mix, product-area shape, regulatory posture, customer segment) that shapes the choice.
  3. **Non-goals.** Three to five bullets. Concrete refusals with named consequences. Time-boxed to the window.
  4. **Sunset criteria.** One to two named criteria. Each with a triggering condition, a review cadence, and a defined exit action (chapter 4).
  5. **Hand-off contracts.** A short list naming the peer specialist tracks and the staff-scope modules this row cites for implementation depth. Cite each with track slug and — where you can — the specific module.
  6. **Interlock with the peer platform-side principal's mod-505.** One or two sentences naming the platform bet(s) this row depends on, or noting that this row is modelling-only with no platform interlock.
- **Two page-scale constraints.** Each row is approximately one page long — no less than half a page, no more than a page and a half. If a row overflows, you have slipped into implementation altitude; if a row underflows, you have not written enough non-goals or sunsets.

## Starter guidance

- **Row 5 (MLOps as org contract) is the most commonly miswritten row.** It slips easily into becoming a tooling checklist ("we do MLflow, we do model cards, we do canaries"). Refuse the checklist shape. Write the contract as a bet: what does the org commit to as an *invariant* every ML team abides by?
- **Row 4 (foundation-model program) is the row where the honest answer, for most orgs, is *not-in-window*.** If you write *not-in-window*, write it as a *decision* with the revisit conditions and the falsification signal that would bring the row back into the window. Chapter 4's non-goal-and-sunset discipline still applies to a not-in-window row.
- **Every row's rationale needs org-specific context, not general ML wisdom.** "We invest in Gen-AI because Gen-AI is important" is not a rationale. "We invest in a post-training program on mid-tier open-weights models for the enterprise-facing product area because 40% of contract-restricted workloads by revenue cannot be served by frontier APIs under our current data-residency posture" is a rationale. Force yourself to write the specific fact.
- **Every row's hand-off contracts need to be real track names, not aspirations.** If you cite `fine-tuning-engineer-learning` you should be able to point to the actual repo. If a needed peer track does not exist in the ecosystem yet, say so — that is a real note for the CTO to hear.
- **Every sunset criterion needs all three parts.** The chapter-4 discipline is strict. A criterion without an exit action is decoration.
- **Do not repeat implementation depth.** If you find yourself writing about MFU, parallelism recipes, retriever architectures, memory strategies for agents, or specific eval-harness engineering, you have slipped down. Delete and rewrite at bet altitude.
- **Cite chapter numbers as you go.** *"See chapter 2's bet framing for row 1"*, *"non-goal per chapter 4 discipline"*, *"sunset trigger tracked in chapter 6 category 2"*. It keeps the reader (and future you) grounded in which framework produced which claim.

## Acceptance criteria

Your document is done when it can pass all of the following:

- [ ] All five rows written, in chapter-2 order, each with the six named subsections.
- [ ] Each row is between half a page and a page and a half.
- [ ] Every row's bet framing sentence names the horizon and the scope; not just what, but for how long and across what portion of the org.
- [ ] Every row's rationale includes at least one org-specific fact (workload mix, product-area shape, regulatory posture, customer segment, or comparable) that a peer VP could disagree with substantively.
- [ ] Every row's non-goal set has at least three concrete refusals, each with a named consequence and time-boxed to the window.
- [ ] Every sunset criterion has all three parts — triggering condition, review cadence, defined exit action.
- [ ] Every row's hand-off contract cites real peer tracks (or explicitly names that a needed peer track does not yet exist).
- [ ] Every row's interlock section either names one to two specific platform-side dependencies or explicitly notes that the row has no platform interlock.
- [ ] Nowhere in the document do specific model architectures, MFU targets, parallelism recipes, retriever designs, or per-quarter delivery milestones appear.

## Stretch goals

- **Adversarial peer specialist review.** For each row, have (or role-play) a peer specialist-track engineer read *only their row* — a fine-tuning engineer for row 1's post-training piece, a RecSys senior engineer for row 2, an agentic-AI engineer for row 3, etc. Ask: *"Would you be able to build the fiscal-year roadmap from this row?"* Revise until each specialist can.
- **Row-4 defense.** If your row 4 is *not-in-window*, write a one-page counterfactual: what would the row look like if the answer *were* yes? This tests the defensibility of the *no* by making you argue the alternative.
- **Cross-org check.** Take a real Principal / Distinguished ML posting from the 2026-Q2 sample ([`../../../JOB_REQUIREMENTS.md`](../../../JOB_REQUIREMENTS.md)) whose org is *not* the one you wrote against and adjust the portfolio for that org: which rows change state? Which non-goals shift? This exercises the *this org, this window* discipline.

## Deliverable location

Local workspace. Pair with exercise-01 (one-pager) and exercise-03 (sequencing) to form the two paired artifacts described in chapter 7.
