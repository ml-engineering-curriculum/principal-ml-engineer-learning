# The Principal-Scope Executive Audience vs. the Staff-Scope Executive Audience

> Chapter 2 of mod-504. Prerequisite: chapter 1 (working definition of influence without authority). Downstream: chapter 5 lifts the mod-502 chapter 7 paired artifact to the audience this chapter fixes; exercise-01 is where the lift is performed.

## Why the audience boundary matters

The single most common failure in a first-cycle principal draft is *artifact-audience mismatch* — a document written to the principal's own comfort altitude rather than to the executive who is actually going to ratify the bet. The failure comes in two directions. Aim too low (SVP-audience artifact written for a Director) and the document over-explains, over-defends, over-hedges, and drowns the direction in caveats. Aim too high (Director-audience artifact walked to an SVP) and the document assumes context the SVP does not have, uses ML-function-internal jargon the SVP has not internalised, and never gets to the *"what am I agreeing to"* question the SVP needs answered.

Chapter 1 named the audience ceiling — *SVP* (Capital One, Sr. Distinguished) versus *VP* (Capital One, Distinguished). This chapter draws the ceiling as an operating boundary: who reads what, what the reading mode is, and how the artifact changes across the boundary.

The chapter is anchored to the staff-scope executive-audience RFC portfolio owned by [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-02. That portfolio *is not thrown away when a level-40 staff engineer promotes to level-48 principal*. It becomes the base the principal *lifts* to a higher audience. The lift-vs-replace distinction is the load-bearing craft of this chapter.

## The two audiences, named

### The staff-scope executive audience

**Who they are.** The audience owned by `staff-ml-engineer-learning` mod-410. In modal ML orgs this is:

- **The staff engineer's own VP or Director** — the people-management chain above their team-of-teams.
- **The peer VP of the adjacent function** whose team the staff engineer's portfolio depends on — a Director of Product for the same product area, a VP of Platform whose substrate the ML systems stand on, a Director of Data whose pipelines feed the features.
- **The functional review body's chair** — the ML-function launch-review chair, the responsible-AI review body's chair at *committee* altitude, the platform launch council's chair.

The audience ceiling for staff-scope work is typically the VP directly above the staff engineer's Director, plus the peer VPs on adjacent functions. A staff engineer occasionally has a document walked to an SVP by *their* VP; the artifact was staff-authored but the ratification is at the VP's altitude, not the staff engineer's.

**What they read for.** The staff-scope executive audience reads a mod-410-style exec-audience RFC for:

- The portfolio-scope decision the VP has to commit against — capacity, roadmap, cross-team dependency.
- The specific inter-team seams the RFC is renegotiating.
- The commit the VP is being asked to make on behalf of their engineering organisation.
- The horizon — typically a fiscal year, sometimes two.

**Reading mode.** The staff-scope executive audience typically has 20–45 minutes for a substantive read plus a 30-minute review meeting. The document can run to 10–20 pages if the reading is single-cycle; the review conversation is where the substance lands.

### The principal-scope executive audience

**Who they are.** The audience owned by *this* module. In modal ML orgs this is:

- **The SVP of Engineering** or **SVP of Product** or **SVP of AI / Data** whose portfolio the ML function sits inside. The person who reports directly to the CTO or the CEO.
- **The CTO.** The chief technology executive — the person the CEO holds accountable for the technical direction across all engineering functions.
- **The CEO.** For the largest bets — a foundation-model program, a shared-substrate re-platform, a full org-wide capability shift — the CEO becomes the ratification altitude when the decision affects P&L allocation.
- **A board sub-committee.** For the largest bets in regulated industries (financial services, healthcare, sectoral AI regulation), the board's technology sub-committee or the audit committee ratifies. This is the highest audience ceiling this module walks; it is rare and always co-authored with the CAIO / Head of AI Governance / CFO.
- **The peer executive branch.** The CAIO / Head of AI, the Head of AI Governance, the CISO, the CFO. These are peers at the ratification table, not audience-of-one — chapter 3 owns the partnership contract with each.

**What they read for.** The principal-scope executive audience reads for:

- The *direction* — what the ML function is committing to for the next 3–5 years, in one paragraph they can quote.
- The *boundary* — what the ML function is *not* doing (the non-goals from mod-502 chapter 4), and what would make them stop (the sunset criteria).
- The *ask* — the capacity envelope, the headcount shape, the partnership commitments, the board mandate the SVP / CTO / CEO is being asked to underwrite.
- The *defensibility* — one paragraph they can use in front of *their* peers (fellow SVPs, the CFO, the board) to justify having ratified this direction.

**Reading mode.** The principal-scope executive audience reads for five minutes on their own time, followed by a 15-to-30-minute review conversation in which they will summarise the direction back to the room to test their own comprehension. This is the audience mod-502 chapter 7 § *the executive-audience one-pager* fixed the shape for. The reading mode is what forces the one-page ceiling and the *quotable-in-five-minutes* discipline.

## The five axes of difference

The two audiences differ along five axes. Every axis has an artifact-level consequence.

### Axis 1 — Altitude of the argument

**Staff-scope audience:** the argument is *at the portfolio-scope decision level*. "*We are re-platforming the ranking stack onto the shared serving substrate this fiscal year, which requires <VP-partner> to commit <specific team capacity> for the migration and accept <specific downtime window> during the cutover.*" The argument is anchored in a specific portfolio, a specific fiscal year, a specific set of teams.

**Principal-scope audience:** the argument is *at the multi-year direction level*. "*Over the next four years the ML function converges its production ML onto a shared paved-road substrate, invests in Gen-AI as an integration bet with a targeted post-training program on the enterprise side, and holds foundation-model pretraining out-of-window absent named revisit signals.*" The argument is anchored in a direction, a bet portfolio, and a horizon that spans multiple fiscal years. It does not name specific teams; it names the shape.

The consequence for the artifact: an SVP-audience document that names specific teams and specific quarter-by-quarter milestones has *descended into staff altitude*. It will read as a portfolio roadmap to the SVP, and the SVP will (correctly) route it back down to the VP for portfolio-scope discussion. The lift has failed.

### Axis 2 — Horizon

**Staff-scope audience:** one fiscal year, occasionally two. The mod-410 exec-audience RFC is anchored to the current planning cycle plus the next.

**Principal-scope audience:** three to five years. Mod-502 chapter 3's sequencing grid — bet / hedge / option / not-in-window — spans a window this long. The principal-scope audience reads for direction over that horizon.

The consequence for the artifact: a document that talks about *next quarter's launch* to an SVP is at the wrong altitude. A document that talks about *the four-year direction, with this fiscal year's first-move* is at the right altitude.

### Axis 3 — Vocabulary

**Staff-scope audience:** engineering-technical vocabulary is safe. A VP of Engineering understands *feature-store contract*, *canary rollout*, *A/B test power*, *training / serving skew*. A Director of Product understands *retrieval quality*, *ranking depth*, *personalisation cold-start*.

**Principal-scope audience:** engineering-technical vocabulary is dangerous. A CTO understands the vocabulary — most CTOs at ML-heavy orgs have a strong technical foundation — but they are not in the ML weeds daily, and vocabulary that would land with a VP of Engineering reads as ML-function-internal jargon that has escaped its container. Mod-502 chapter 7's discipline (*"no jargon that a CTO would not know without an ML engineering background"*) is the reference. Terms like *foundation-model pretraining*, *paved-road substrate*, *frontier-API adoption*, *sunset criterion* belong on the one-pager. Terms like *Chinchilla-optimal*, *MFU*, *FSDP*, *reranker*, *MoE ranker* belong in the deep-dive.

The consequence for the artifact: a one-pager sent to a CTO that reads as a technical brief has aimed at the wrong audience. The rewrite is at the *vocabulary* layer more often than at the *content* layer.

### Axis 4 — What the audience is being asked to commit

**Staff-scope audience:** a portfolio-scope commit. Capacity for a fiscal year, a cross-team dependency, an OKR co-owned by the VP, an inter-team review touchpoint.

**Principal-scope audience:** a directional commit — the SVP / CTO ratifies the ML function's multi-year direction, underwrites the capacity envelope (usually stated as a range, not a headcount number), commits to a governance partnership cadence, and takes on the board-facing narrative for the ML function. The commit is *directional and structural*, not *item-level*.

The consequence for the artifact: the *what we ask of leadership* section (mod-502 chapter 7 § *what we ask of leadership*) reads differently at the two altitudes. At staff altitude it is *"commit two Platform engineers for the migration in Q3"*; at principal altitude it is *"underwrite the FY26 capacity envelope of X-to-Y engineers on the ML function, commit to the quarterly governance-council touchpoint with the Head of AI Governance, and take the board-facing narrative for the RecSys re-platform bet"*.

### Axis 5 — Meeting-room dynamics

**Staff-scope audience:** the review meeting is 30 minutes. The staff engineer walks through the RFC, fields questions, and leaves with commits. The VP is the target reader; the peer VPs are co-attendees.

**Principal-scope audience:** the review is embedded in a broader session — a CTO's monthly technical council, an SVP's quarterly investment review, a board technology sub-committee meeting. The principal has 15–30 minutes of *floor time*, most of which is spent on Q&A rather than on presentation. The one-pager is what the room has read in advance; the walk-through is 5–10 slides at most; the substance lands in the executive's back-and-forth with their peers in the room.

The consequence for the artifact: a document that assumes a walk-through slot longer than 15 minutes has misjudged the room. Chapter 4 § *the room the decision is actually made in* is the reference; the SVP / CTO decision-room is often a pre-ratification session, and the actual commitment is finalised in the one-on-one that follows.

## The lift-vs-replace rule

The staff-scope RFC portfolio (`staff-ml-engineer-learning` mod-410 exercise-02) is *not thrown away when the principal audience is different*. It becomes:

1. **The primary source of substance** for the principal-scope artifact. The evidence, the technical arguments, the risk enumeration all originate in the staff-scope RFC portfolio.
2. **The deep-dive companion** to the principal-scope one-pager, in modified form. Mod-502 chapter 7 § *the deep-dive companion doc* absorbs a large fraction of what a staff-scope exec-audience RFC would contain — restructured around bet-portfolio row and cited from the one-pager.
3. **The route the direction executes through**. The staff engineers who authored the mod-410 RFCs are the same engineers whose teams execute the principal-ratified direction. Their RFCs are the plumbing.

The rule is *lift, don't replace*.

**Lift** means: take the staff-scope RFC portfolio, restructure it around the principal-scope bet portfolio (mod-502 chapter 2), cut the portfolio-scope specifics that do not belong at the principal altitude (specific team names, quarter-level milestones, feature-flag rollout plans), abstract the specific technical arguments to the pattern the SVP / CTO needs to grasp, and generate the SVP / CTO-audience artifact from it. The one-pager comes out short. The deep-dive comes out at 15–25 pages (mod-502 chapter 7 § *shape*). The staff-scope RFCs remain the substrate.

**Replace** means: write the SVP / CTO-audience artifact from scratch without reference to the staff-scope RFC portfolio. This is the modal failure of a first-cycle principal. The consequence is that the SVP / CTO artifact and the staff-scope RFCs drift, and the direction ratified at the SVP altitude does not connect to the plumbing that would execute it. Twilio's *"executable roadmaps"* framing fails.

Practical lift discipline:

- **Every principal-scope claim traces to a staff-scope RFC or a peer artifact.** The deep-dive companion cites the mod-410 exec-audience RFC that carries the underlying substance. Nothing is invented at the principal altitude that is not already grounded at the staff altitude.
- **Every staff-scope RFC that carries a bet in the mod-502 portfolio is enumerated in the deep-dive's appendix.** The SVP / CTO does not read them; a staff engineer reading the deep-dive uses the appendix as the reference to their own team's roadmap RFCs.
- **The staff-scope RFCs are refreshed when the principal-scope direction shifts.** A principal-ratified direction change flows *back down* into the staff-scope RFC portfolio; the mod-410-owner staff engineer refreshes their RFC to match. Without this flow, the two artifact tiers drift.

## Three lift-vs-replace failure modes

Named the way mod-502 chapter 4 names non-goal failure modes.

### Failure 1 — "The staff RFC in a suit"

**Symptom.** The principal-scope one-pager is the staff-scope RFC compressed into two pages. The vocabulary is engineering-technical, the horizon is a fiscal year, the ask names specific teams. The document reads as *"my portfolio-scope RFC, but shorter"*.

**Fix.** Rewrite the *direction sentence* (mod-502 chapter 7 § *the direction sentence*) at the multi-year altitude first. Then rewrite the bet portfolio at the *portfolio-of-bets* altitude (mod-502 chapter 2's row shape). Then rewrite the ask at the *directional and structural* altitude (axis 4 above). The pieces below the one-pager can inherit from the staff-scope RFC portfolio; the one-pager itself cannot.

**Root cause.** The principal has not internalised axis 1 (altitude of the argument). The rewrite is not at the vocabulary layer; it is at the *what the document is arguing about* layer.

### Failure 2 — "The manifesto with no substrate"

**Symptom.** The principal-scope one-pager is at the right altitude — direction, boundary, ask — but the deep-dive companion cannot be traced to any staff-scope RFC portfolio. The direction is asserted; the substrate that would execute it does not exist as documents. The SVP asks *"how would we actually do this?"* and the answer is a talk-track, not a set of cited RFCs.

**Fix.** Author or refresh the underlying mod-410 staff-scope exec-audience RFC portfolio first. The deep-dive is the *directional restructure* of that portfolio; without the portfolio, the deep-dive is aspiration.

**Root cause.** The principal has jumped straight to principal-scope artifacts without maintaining the staff-scope substrate. This is often paired with the mentorship failure — the principal has stopped investing in the staff engineers whose RFCs would carry the substrate — which is why mod-505 (technical bar and mentorship) is a peer module to this one.

### Failure 3 — "The two artifacts drift"

**Symptom.** The SVP ratifies the principal-scope direction. The staff-scope RFC portfolio does not refresh. Six months later the two disagree: the staff-scope RFC still names an obsolete direction, the principal-scope one-pager names the new one, and the executing teams are operating from the staff RFC because that is the document their VP reads.

**Fix.** Every principal-scope direction change triggers a *staff-scope RFC refresh cycle* — the staff-plus engineers on the affected portfolios refresh their mod-410 RFCs within the next planning window. This refresh is the plumbing chapter 4 § *follow-up commitment tracking* enforces. Without it, the principal has ratified paper.

**Root cause.** The commitment-tracking discipline in chapter 4 is not being run. The ratification is banked; the execution is not tracked.

## A worked micro-example — the same bet at two altitudes

To ground the difference, here is the *RecSys re-platform bet* at both altitudes.

**Staff-scope executive-audience RFC (`staff-ml-engineer-learning` mod-410 exercise-02 shape, roughly).** Title: *Re-platforming the Ranking Stack onto the Shared Serving Substrate, FY26 Plan*. Audience: VP of Engineering (ML), VP of Platform, Director of Product (Ranking). Length: 12–18 pages. Substance:

> The Ranking Team will migrate its current bespoke serving stack onto the shared serving substrate over FY26, starting with the low-risk shadow-traffic tier in Q1, adding the co-primary tier in Q2, and cutting over in Q3 with a two-week rollback window. The migration requires two Platform engineers full-time for Q1–Q2 and one for Q3, plus Ranking Team capacity per the plan below. Expected wins: <named cost delta>, <named latency delta>, <named canary-experiment cycle-time delta>. Risks: <named list>. Roll-back plan: <named steps>. VP-level ratification asks: (a) VP Platform commits the two-plus-one engineers per the migration plan; (b) VP Engineering (ML) commits the Ranking-Team capacity; (c) Director of Product (Ranking) accepts the two-week freeze on ranking-quality launches during Q3 cutover; (d) launch-review chair pre-approves the migration-time deviation from the standard canary bar.

**Principal-scope executive-audience one-pager (mod-502 chapter 7 shape, lifted from the staff RFCs of this and adjacent portfolios).** Title: *ML Technical North Star FY26–FY29 — one-pager*. Audience: SVP of Engineering, CTO. Length: one page. Substance:

> **Direction.** Over the next four years the ML function converges its production ML onto a shared paved-road substrate, invests in Gen-AI as an integration bet with a targeted post-training program on the enterprise side, and holds foundation-model pretraining out-of-window absent named revisit signals.
> **Bet portfolio.** *Row 3 — RecSys / personalisation.* Bet posture: converge the ranking-and-recommendation substrate onto the paved road; consolidate ranking, search, and ads-ranking onto a single serving substrate over the four-year window; retire two bespoke stacks. Current-year state: *bet* (year 1 of the convergence).
> **Non-goals.** <named>. **Signal watch.** <named>. **What we ask of leadership.** Underwrite the FY26–FY29 ML capacity envelope in the range X–Y engineers; commit to the quarterly governance-council touchpoint with the Head of AI Governance; carry the board-facing narrative for the ranking-substrate consolidation. **Refresh cadence.** Semi-annually + emergency refresh triggers per the chapter-6 evolution plan.

Read the two together. The staff-scope RFC is *the plumbing that carries the bet*; the principal-scope one-pager is *the direction the bet plugs into*. Row 3 of the one-pager cites the staff-scope RFC portfolio in the deep-dive companion. The two are aligned; neither replaces the other. The lift is complete.

## Summary

- The principal-scope executive audience (SVP / CTO / CEO / board sub-committee, plus the peer executive branch) is distinct from the staff-scope executive audience (VP / Director of Product / peer platform VP). Chapter 1's audience ceiling is the operating boundary this chapter fixes.
- Five axes of difference — altitude of the argument, horizon, vocabulary, what is being committed, meeting-room dynamics — carry the artifact-level consequences. A first-cycle principal draft usually fails on axis 1 (altitude) and axis 3 (vocabulary).
- The staff-scope RFC portfolio owned by `staff-ml-engineer-learning` mod-410 is not replaced when the audience shifts. It is *lifted* — the principal-scope one-pager and deep-dive are structural restructures of the staff-scope portfolio at a higher altitude. The lift rule is the load-bearing craft of this chapter and of exercise-01.
- Three lift-vs-replace failure modes to watch: the staff RFC in a suit (fails axis 1), the manifesto with no substrate (fails the lift rule), and the two artifacts drift (fails the follow-up commitment tracking chapter 4 owns).
- Read this chapter alongside mod-502 chapter 7 (the paired one-pager / deep-dive). Chapter 5 in this module lifts that pair to SVP / CTO audience and adds the FAQ; exercise-01 is where the lift is performed.
