# The SVP / CTO-Audience Narrative Craft — One-Pager, Deep-Dive, and FAQ

> Chapter 5 of mod-504. Prerequisite: chapter 1 (working definition), chapter 2 (audience boundary), chapter 3 (partnership contracts), chapter 4 (coalition sequence). Downstream: exercise-01 authors the three-artifact set for a bet from the learner's mod-502 portfolio.

## Why three artifacts, not two

Mod-502 chapter 7 fixed a paired-artifact discipline: an *executive-audience one-pager* for the CTO / SVP and a *deep-dive companion* for the staff engineer. That pair was designed for the SoundCloud / Capital One / Pinterest style of principal-scope strategy work — a directional artifact plus its substrate.

Chapter 5 of this module extends the pair to a *triplet*. The third artifact is the **FAQ**. The FAQ carries the specific objections the CTO / CFO / CISO / peer VP will raise in the room, drafted before the room, and used as a coalition tool in the 1:1s that lead up to the room. Chapter 4 named the FAQ as the artifact the *stage B objections* funnel into. This chapter walks its craft.

Three reasons the FAQ is a first-class artifact and not a deep-dive appendix.

**Reason 1 — the executive audience does not read the deep-dive under time pressure.** Mod-502 chapter 7 § *reading mode* fixed the CTO / SVP as a five-minute-one-pager reader. The deep-dive gets referenced by their staff, not by them. Their live back-and-forth objections in the room draw on the FAQ, not the deep-dive.

**Reason 2 — the FAQ is what circulates in the pre-read.** The FAQ ships in the pre-read package (chapter 4 stage A) alongside the one-pager. A CTO reading the pre-read sees the direction (one-pager) and the objections-already-anticipated (FAQ), in that order. This inoculates the room: the CTO who reads the FAQ sees the principal has already thought through their peer VPs' likely objections. The room's tone shifts from *"pressure-test the direction"* to *"ratify the direction and clarify any remaining ambiguity"*.

**Reason 3 — the FAQ is a coalition tool.** Chapter 4 § *stage B* is where objections surface in 1:1s. The FAQ collects them. In the 1:1 with the CFO, the principal walks the CFO's specific FAQ section (the cost objections); in the 1:1 with the CISO, the principal walks the security section. Each executive sees their concerns already framed and answered. Chapter 3's *never surprise your peer* discipline is the direct antecedent.

The composite target framing for this chapter carries two postings, both from the 2026-Q2 sample.

- **Twilio (Principal ML Engineer):** *"Lead cross-functional engineering efforts, breaking down complex initiatives into executable roadmaps."* The one-pager and the deep-dive are what carry the "breakdown"; the FAQ is what unblocks the "executable".
- **Wiser Solutions (Principal ML Engineer):** *"Define and evolve the AI and data science technical strategy in partnership with product and business leadership."* The partnership frame extends to the artifact — the deep-dive and the FAQ are the surfaces where the CAIO, CFO, and product leadership become co-authors, not just readers.

Chapter 2 established that the artifacts *lift* the mod-410 staff-scope RFC portfolio; this chapter walks the craft of the lift for each of the three tiers.

## The one-pager — lifted to SVP / CTO / CEO audience

Mod-502 chapter 7 § *the executive-audience one-pager* is the reference. This section adds the SVP / CTO / CEO-audience discipline on top.

### What lifts and what does not

The six-section shape (direction, bet portfolio, non-goals, signal watch, what we ask of leadership, refresh cadence) is unchanged. The audience-matched discipline (chapter 2 axes) is where the lift lands.

**What lifts:**

- **The direction sentence.** From a portfolio-scope framing to a multi-year direction framing (chapter 2 axis 1). Model: *"Over the next four years the ML function converges its production ML onto a shared paved-road substrate, invests in Gen-AI as an integration bet with a targeted post-training program on the enterprise side, and holds foundation-model pretraining out-of-window absent named revisit signals."* The sentence is the whole document in miniature; if it does not survive the CTO's five-minute read, the rest of the page cannot save it. Mod-502 chapter 7 § *the direction sentence* is the reference.
- **The bet portfolio.** Rows carry the same shape as mod-502 chapter 7, but the *posture* and *current-year state* clauses are pitched at the multi-year altitude. No specific team names inline; no quarter-level milestones; no OKR references.
- **What we ask of leadership.** This section becomes the *SVP / CTO commit list*. Not *"commit two Platform engineers for the migration in Q3"* (staff-scope) but *"underwrite the FY26–FY29 ML capacity envelope in the range X–Y engineers; commit to the quarterly governance-council touchpoint with the Head of AI Governance; carry the board-facing narrative for the ranking-substrate consolidation"* (principal-scope). Chapter 2 axis 4 is the reference.

**What does not lift** — the six-section shape, the one-page ceiling, the *quotable-in-five-minutes* discipline, the *no jargon a CTO would not know* discipline. Those carry through unchanged.

### The direction sentence — writing discipline

The direction sentence is the whole document's leverage point. If a CTO / SVP repeats it back accurately at the next board meeting, the one-pager has worked. If they cannot, no other content on the page saves it.

Discipline notes specific to the SVP / CTO / CEO audience:

- **One sentence, ~40–60 words.** Longer and it becomes unquotable; shorter and it loses the bet-portfolio scaffolding.
- **Three-part shape.** *(1) horizon and direction; (2) what we are betting on; (3) what we are explicitly not doing this cycle.* All three in the same sentence. The negation is what a first-cycle draft usually omits; it is what makes the direction defensible in front of the CTO's peer set.
- **No proper nouns.** No specific team names, no specific product lines, no specific model architectures. The direction is at the ML-function-scope altitude. If a CTO reading it needs to know which team owns what to make sense of the sentence, the sentence has descended.
- **Rewrite the sentence more than any other line in the artifact.** Mod-502 chapter 7 § *the direction sentence* names this discipline; it is doubled at the SVP / CTO altitude. A ten-draft revision cycle on this one sentence is not excessive.

### What the SVP / CTO / CEO reads for, per section

Mod-502 chapter 7 established the six-section shape. Here is what each section is *doing* for the SVP / CTO / CEO reader specifically.

1. **Direction (2–3 sentences).** The CTO reads this to know what they will be quoted saying at the next board meeting. Every word is a candidate quote.
2. **Bet portfolio (5 bullet rows).** The CTO reads this to see the shape of the multi-year investment. Not the specifics; the shape. The peer VPs will read this to know which of their portfolios the direction touches. The CFO will read this to know the shape of the capacity envelope they are underwriting.
3. **Non-goals (3–5 bullets).** The CTO reads this to see the *sharp edges of the direction*. What the ML function has explicitly said no to. This section is what the CTO uses to defend the direction to their SVP peers — *"we are not doing X because Y"* is a stronger statement than *"we are doing A, B, C"*.
4. **Signal watch (2–3 bullets).** The CTO reads this to know what *would* change the direction. The signals are the CTO's *early-warning system* for whether the ML function is at risk of a costly pivot.
5. **What we ask of leadership (3 bullets).** The CTO reads this to see what they are being asked to underwrite. The list is short — three bullets — because a CTO asked to underwrite ten things underwrites none.
6. **Refresh cadence (1 sentence).** The CTO reads this to know when they next have to think about this artifact. Semi-annually plus emergency-refresh triggers is the modal cadence; state it in one sentence.

Every failure of an SVP / CTO one-pager traces to one of these six sections having been written for a different audience.

## The deep-dive companion — lifted to SVP / CTO / CEO backing

The deep-dive companion, at principal altitude, has *two audiences*, not one. Mod-502 chapter 7 § *the deep-dive companion doc* fixed the staff-engineer audience; this section adds the *SVP / CTO's own delegated reader* — usually a Chief of Staff, a Principal Program Manager, or the CTO's staff-plus technical advisor — who reads the deep-dive on the CTO's behalf when the CTO wants to defend a specific decision to a peer or to the board.

Both audiences read the same document, but for different questions.

**The staff engineer reads for** — how to build against the direction. What the row-3 bet actually decomposes into for their team. Which sunset criteria they should be alert to. Which seams (mod-503 chapter 8) their team's blueprint touches.

**The CTO's delegate reads for** — how to defend the direction. What specific evidence backs each bet. What the non-goals *cost* the org (opportunity cost, competitive posture). What the FY26 capacity envelope decomposes into. What the *"what we ask of leadership"* commits actually purchase the org, in language a CFO peer would find defensible.

### What lifts and what does not

The twelve-section shape from mod-502 chapter 7 § *shape* carries through. What changes:

- **Section 5 (coherence with the peer platform-side principal's grid) is expanded.** The SVP / CTO's delegate reads this section carefully — the CTO's peer SVP of Platform will have their own principal's roadmap, and the delegate is looking for whether the two directions cohere. A deep-dive that treats this section as a formality signals the two artifacts have drifted.
- **Section 8 (refresh cadence and emergency triggers) is anchored to the four peer executives' calendars.** The CAIO's board reporting cycle, the CFO's investment review cycle, the Head of AI Governance's regulatory-horizon scan, the CISO's threat-model refresh — each is a candidate emergency-refresh trigger for the ML function's strategy. This is chapter 3's partnership contracts landing as artifact discipline.
- **Section 9 (what-we-ask-of-leadership, expanded) becomes the underwriting spec.** Every ask decomposes into (a) the named executive commit, (b) the cadence at which the ask is fulfilled, (c) the metric that would show the commit has closed. This is what the CFO's delegate will use to negotiate the actual envelope during the fiscal planning cycle.
- **Section 12 (appendices) cites the mod-410 staff-scope RFCs verbatim.** Chapter 2's *lift, don't replace* discipline lands here — the deep-dive is the *directional restructure* of the underlying staff-scope portfolio; the appendix is where the reader can trace claim-to-RFC.

### Writing discipline

- **Every claim traces to a chapter or a peer artifact.** Same discipline as mod-502 chapter 7 § *writing discipline*, doubled at the SVP / CTO altitude. A CTO's delegate who cannot trace a claim to its source will (correctly) discount the claim.
- **Sections stand alone.** A CFO's delegate reading only section 9 needs to be able to draft the FY26 investment ask from that section. A CISO's delegate reading only section 6 (the seam with the roadmap) plus section 3 row 3 needs to be able to draft their threat model for the row.
- **No new bets in the deep-dive that are not in the one-pager.** The one-pager is the direction; the deep-dive is the substrate. A bet that appears in the deep-dive but not the one-pager is either a bet the principal is trying to smuggle in below the CTO's attention (a partnership-breaking move) or a bet that should be lifted onto the one-pager. Either way, fix.

## The FAQ — the third artifact

The FAQ is not an appendix and it is not a Q&A section at the end of the one-pager. It is a first-class artifact with its own audience, its own shape, and its own refresh cadence.

### Purpose

The FAQ collects, per pre-anticipated stakeholder, the objections the principal expects them to raise, drafted before the pre-read distribution. Each entry is a *question in the stakeholder's voice* and an *answer in the principal's voice*. The FAQ:

- **Ships in the pre-read package.** The CTO and every executive stakeholder receives the FAQ alongside the one-pager. The FAQ demonstrates that the principal has already anticipated the objections; it opens the ratification conversation from a position of *"here are the questions you were going to ask; here is what we have already thought"*.
- **Grounds the 1:1s (chapter 4 stage B).** Each executive's 1:1 walks their specific FAQ entries. The FAQ becomes the shared instrument.
- **Grounds the decision-room (chapter 4 stage C).** The room's Q&A returns to the FAQ; the objections have already been raised, and the room's job is to ratify the answers or add new ones. Chapter 4's *nothing new introduced in the room* discipline is enforceable because the FAQ is what defines *"not new"*.
- **Persists across cycles.** The FAQ from the previous strategy refresh is the input to the next FAQ. Objections that recur are the *load-bearing* objections; objections that appeared once and were resolved fall off the FAQ across refreshes.

### Shape

The FAQ is organised by audience, not by topic. Sections:

**Section 1 — CTO objections.** The five-to-eight objections a CTO in this org will raise. Modal categories, from experience across principal-scope postings:

- *"How does this differentiate from what our competitors are already doing?"* — the competitive-posture objection. Answer references the mod-502 signal-tracking cycle (chapter 6 there).
- *"What is the cost curve over the horizon?"* — the CFO-adjacent objection the CTO will raise on the CFO's behalf. Answer cites the deep-dive's section 9 and the CFO-co-authored capacity envelope.
- *"What happens if the industry shifts to X?"* — the direction-fragility objection. Answer cites the mod-502 sunset criteria and the *what would stop us* signal watch.
- *"How does this affect our recruiting narrative?"* — the CAIO-adjacent objection. Answer cites the co-authored strategy.
- *"How much of the ML function's capacity does this consume?"* — the portfolio-consumption objection. Answer decomposes the bet portfolio's per-row capacity ask.

**Section 2 — CFO objections.** The five-to-eight objections a CFO in this org will raise. Modal categories:

- *"What is the FY-year-N cost profile per bet?"* — the granular-cost objection. Answer cites the deep-dive's section 9.
- *"What is the cost of the non-goals (opportunity cost)?"* — the opportunity-cost objection. Answer cites the deep-dive's non-goal register (section 10).
- *"When does the bet start returning?"* — the payback-horizon objection. Answer decomposes per row.
- *"What is our sensitivity to vendor cost changes?"* — the vendor-dependency objection.
- *"How does this compare to the alternative allocation (across engineering functions)?"* — the peer-function allocation objection. Answer is honest about scope — this is co-decided with the CFO, not principal-decided.

**Section 3 — CISO objections.** The four-to-six objections a CISO in this org will raise:

- *"What is the ML-specific threat surface per bet?"* — cite chapter 3's joint threat-modelling artifact.
- *"How does the reference architecture enforce data-tier discipline at the contract layer?"* — cite mod-503 chapter 4's contract invariants.
- *"What happens in a foundation-model provider's incident that affects our production ML?"* — cite the incident-response runbook.
- *"How does this bet's threat surface compare to the current-state's?"* — cite the joint threat model.

**Section 4 — Head of AI Governance objections.** The four-to-six objections the Head of AI Governance will raise:

- *"Which of the current-cycle regulatory obligations does each bet trigger?"* — cite mod-503 chapter 8 § *contract 1* (policy-to-contract mapping).
- *"What is the responsible-AI review body's touchpoint per bet?"* — cite mod-503 chapter 7.
- *"How does the risk-tier taxonomy shift under this direction?"* — cite the co-authored risk-tier taxonomy.
- *"How does the documentation surface (Model Cards, Data Cards, datasheets) evolve under this direction?"* — cite the co-authored documentation framework.

**Section 5 — Peer VP objections.** The three-to-five objections the peer VPs (Platform, Product, Data) will raise:

- *"Which of our team's roadmaps does this touch and what is the coordination model?"* — cite mod-503 chapter 8 seams.
- *"What does the substrate ask of us over the horizon?"* — cite the seam contracts.
- *"How much of our capacity does the direction consume?"* — decompose per peer function.

**Section 6 — Board / audit-committee objections (for regulated industries and public-company orgs).** The three-to-five objections a board sub-committee raises:

- *"How does this direction affect our reported AI-risk posture?"* — cite the risk-tier taxonomy and the responsible-AI review body's audit trail.
- *"How does this direction align with our external commitments (public AI policy statements, ESG disclosures)?"* — cite the CAIO-owned external narrative.
- *"What is our exposure to a foundation-model provider's failure?"* — cite the vendor-risk model.

### Writing discipline

- **The FAQ is voiced.** Each question is in the stakeholder's voice — the phrasing they would actually use. If the question reads as a strawman ("*What if this doesn't work?*"), the FAQ has not landed.
- **Each answer is 2–4 sentences and cites a specific artifact section.** Answers longer than four sentences either belong in the deep-dive (with a pointer from the FAQ) or are trying to do too much work. Answers that do not cite are unanchored.
- **Objections come from stage B, not from imagination.** The FAQ that a first-cycle principal drafts from imagination is a FAQ that misses the actual objections. The FAQ that a defensible principal drafts is *populated from 1:1s* in the previous refresh cycle, augmented with objections drawn from the four peer executive counterparts' own team's likely reads. Chapter 4 § *shift signals* feeds the FAQ.
- **The FAQ is refreshed with every strategy refresh.** Objections that were resolved in the last cycle come off; new objections that surfaced in the last cycle's stage B go on. The FAQ is a *living* artifact on the same cadence as the one-pager.
- **The FAQ is short.** Twenty to thirty entries total across all sections. A FAQ with sixty entries has become the deep-dive; either move entries into the deep-dive or triage.
- **The FAQ is honest.** An objection the principal cannot yet answer is not *hidden*; it is listed with the current answer being *"deferred to the mod-502 chapter 6 signal-tracking cycle; the next data point that would resolve it is X, expected by Y"*. This is chapter 6's *deferred decision* discipline landing at the artifact layer. A FAQ that pretends to answer every objection is a FAQ the executive audience will (correctly) distrust.

### What the FAQ is *not*

- **Not a Q&A appendix.** The FAQ is a first-class artifact; it ships in the pre-read alongside the one-pager, not stapled to the back of the deep-dive.
- **Not a defense mechanism.** Every entry is *"here is the objection, here is the answer"*, not *"here is the objection, here is why the objection is wrong"*. Answers that dismiss objections are answers the stakeholder will (correctly) read as defensive.
- **Not a substitute for the deep-dive.** Answers cite the deep-dive; they do not replace it. The FAQ is the *executive-audience surface* on the deep-dive's substrate.

## How the three artifacts ship together

Practical logistics.

- **Ratification cycle.** The one-pager, the deep-dive, and the FAQ ship as a package on the semi-annual strategy-refresh cadence (mod-502 chapter 5 § *refresh cadence*). All three refresh together; a change to the one-pager triggers a review of the FAQ and the affected deep-dive sections.
- **Pre-read distribution (chapter 4 stage A).** The three-artifact package is what circulates before the decision-room. The one-pager goes to every stakeholder; the FAQ goes to every executive stakeholder; the deep-dive goes to every stakeholder who requests it (which is most of the executive-branch delegates and every staff engineer).
- **One-on-one prep (chapter 4 stage B).** Each 1:1 walks the FAQ section for that stakeholder. The 1:1's shift signals feed back into the FAQ before the room.
- **The room (chapter 4 stage C).** The one-pager is the working document; the FAQ is what the room's Q&A returns to; the deep-dive is on the table for reference. The chair's ratification points at the one-pager's direction sentence.
- **Follow-up (chapter 4 stage D).** The commits from the room are tracked on the coalition tracker (chapter 4 §2). The FAQ's *deferred* entries are tracked on the escalation-and-deferral log (chapter 6).
- **Canonical location.** All three ship to the same location the mod-502 strategy and the mod-503 architecture ship to (mod-503 chapter 5 § *the single canonical location*). Not a private folder. Not the principal's own inbox.

## A worked micro-example — the three artifacts for one bet

To ground the practice, here is what a single bet from the mod-502 portfolio looks like across the three artifacts. The bet: *the Gen-AI-as-integration bet with a targeted post-training program on the enterprise side*.

**One-pager — row 4 of the bet portfolio.**

> *Row 4 — Gen-AI.* Bet posture: integrate frontier-provider LLMs into the product surface via a paved-road inference gateway; invest in a targeted post-training program on the enterprise side for the two workflows where instruction-tuning has documented lift; hold foundation-model pretraining out-of-window absent named revisit signals. Current-year state: *bet* (year 2 of the integration; year 1 of the post-training program).

Two sentences. Zero jargon a CTO wouldn't know. No specific team names. No specific vendors.

**Deep-dive companion — the row-4 subsection.**

> *[Full one-page treatment.]* Bet framing (chapter 2): why the integration path is the current-year bet, why post-training is the year-2 addition, why pretraining is out-of-window. Current-year state (chapter 3): the specific targeted workflows and their expected lift horizons. Non-goals (chapter 4): explicitly-not-doing pretraining on our own data, explicitly-not-doing multi-vendor LLM orchestration this cycle, explicitly-not-doing consumer-facing agentic workflows this cycle. Sunset criteria (chapter 4, all three parts): the signals that would trigger a pivot on the integration path, the signals that would trigger a sunset of the post-training program, the signals that would trigger a re-open on the pretraining decision. Specialist-track hand-off (mod-501 chapter 6): the peer platform-side principal owns the inference-gateway substrate; the peer specialist track owns the post-training pipeline substrate.

**FAQ — the row-4 entries.**

- *CTO objection.* "How does this differentiate from what our competitors are already doing on Gen-AI?" *Answer (2–3 sentences).* The competitive posture is on *integration-and-post-training*, not on *frontier-model matching*; we are betting that the enterprise workflows we serve have specific instruction-tuning lift that competitors on general-purpose paved-road integration alone will not capture. Signal-tracking is continuous per mod-502 chapter 6; the signals that would change the posture are enumerated in the deep-dive section 7. If competitors ship a comparable post-training program before our year-2 mark, the sunset criterion 4c triggers.
- *CFO objection.* "What is the FY26 cost profile for the post-training program?" *Answer (2–3 sentences).* The FY26 envelope covers <X-Y> engineers plus <Z> post-training compute allocation, per the deep-dive section 9. The payback horizon is 18 months from FY26-Q1, and the sensitivity to frontier-provider pricing is documented in section 7. If pricing shifts materially, sunset criterion 4a triggers.
- *CISO objection.* "What is the threat surface of the frontier-provider integration path?" *Answer (2–3 sentences).* The joint threat model with the CISO (per chapter 3's partnership contract) covers vendor-lock, data-egress-through-generation, and prompt-injection surfaces. The inference-gateway contract (mod-503 chapter 4) enforces the data-tier discipline at the contract layer. Any new frontier-provider adoption goes through the CISO-authored vendor-risk review; the current provider's review is dated <YYYY-MM-DD>.
- *Head of AI Governance objection.* "Which regulatory obligations does the Gen-AI integration trigger?" *Answer (2–3 sentences).* Per the policy-to-contract mapping (mod-503 chapter 8 § *contract 1*), the integration path triggers EU AI Act GPAI-downstream-deployer obligations and the enterprise-workflow use-cases trigger high-risk-system tier obligations in the two specific product areas. The mapping cites both directly, and the responsible-AI review body has the current-cycle status. The post-training program's provenance discipline is co-authored with governance.
- *Peer VP objection (VP of Platform).* "How much of the platform-substrate roadmap does the inference gateway consume this cycle?" *Answer (2–3 sentences).* The inference-gateway contract lifts to v2.1 this cycle per the mod-503 chapter 6 evolution plan; the substrate ask is 30% of the platform-substrate roadmap for FY26-Q1 through FY26-Q3, per the co-authored seam document. The peer platform-side principal is co-author; the peer VP's specific portfolio impact is in the deep-dive section 5.

Notice how the FAQ *voices* the objections and *cites* the answers. A CTO reading the FAQ before the room understands the direction *and* the objections the direction has already survived. The room's job becomes ratification, not negotiation.

## The self-test before the room

Two lightweight self-tests before you take the three-artifact package into the decision-room (chapter 4 stage C).

1. **The five-minute test.** Give the one-pager to a peer executive who has *not* been in stage B. After five minutes, ask them to summarise the direction, the three key non-goals, and the one commit they would be underwriting. If they can, the one-pager works. If not, cut and rewrite until they can. Mod-502 chapter 7 § *the five-minute test* is the antecedent.
2. **The objection-completeness test.** Give the FAQ to your peer executive-branch counterparts *before* the room (this is what happens in the stage B 1:1s anyway). Ask each: *"is there an objection you or your peer would raise that is not in the FAQ?"* If yes, add it and answer it. The room where the CFO raises an objection not in the FAQ is a room whose stage B was under-done, and the coalition-tracker's *shift signals* column should have flagged it.

If both tests pass, the three-artifact package is at ratification bar.

## Summary

- The SVP / CTO-audience narrative for an ML bet is a *triplet* — one-pager, deep-dive, FAQ — not a pair. The FAQ is a first-class artifact that ships in the pre-read.
- The one-pager is the mod-502 chapter 7 shape lifted to SVP / CTO / CEO audience per chapter 2's five axes. The direction sentence, the bet portfolio at multi-year altitude, and the *what we ask of leadership* section are where the lift lands.
- The deep-dive is the same twelve-section shape as mod-502 chapter 7's, with two audiences: the staff engineer building against the direction and the SVP / CTO's delegate defending it to a peer. Sections 5, 8, 9, and 12 do the most work at the principal altitude.
- The FAQ carries the objections a CTO, CFO, CISO, Head of AI Governance, peer VP, and (in some orgs) a board sub-committee will raise. Objections are voiced; answers are 2–4 sentences with citations; the FAQ ships in the pre-read.
- The three artifacts ship together, refresh together, and feed the coalition sequence chapter 4 walks. Two self-tests before the room: the five-minute test and the objection-completeness test.
- Chapter 6 walks the escalation-and-deferral protocol that runs through the FAQ's *deferred* entries and the coalition tracker's *shift signals* column.
