# exercise-04: Author the Review-Bar Charter and Walk One Escalation End-to-End

**Estimated effort:** 3 hours

## Objective

Instantiate chapter 4's practice: author the tiered review-bar charter (chapter 4 § *the portfolio-scope RFC bar* and § *the north-star-scope revision bar*), author the escalation-and-anti-escalation criteria (chapter 4 § *the escalation path*), and walk one specific escalation end-to-end through the four triggers, the artifact shape, and the four possible principal responses. Three artifacts, each sitting on a different seam of chapter 4's tiered bar.

The charter is the principal's public contribution to the ML org's canonical review pattern (chapter 2 § *Class A* is the leverage-move class this exercise most often feeds); the escalation walkthrough is the private sanity-check that the triggers and anti-triggers are concrete enough to apply under real-cycle pressure.

## Prerequisites

- **Chapter 4 read end-to-end.** The two altitudes (portfolio-scope RFC vs. north-star-scope revision), the eight axes for the portfolio-scope RFC plus the four principal-specific reads, the seven-check north-star review checklist, the four decision modes (block / nudge / escalate / defer per mod-503 chapter 7), the four escalation triggers, the four anti-triggers, the escalation-artifact shape, and the six failure modes.
- **Chapter 2 § *Class A — the canonical review pattern*.** This exercise's charter is a Class A artifact in draft form. Chapter 2's co-author discipline and landing-criteria discipline both apply.
- **Mod-503 chapter 7 (running the org-wide architecture-review body).** The parent forum for the north-star-scope half of the charter. The charter cites it; it does not re-derive it.
- **Mod-503 chapter 6 (evolution plan and version-bump triggers).** The version-bump trigger table is the substrate for the north-star-scope review's seven-check item 2 and for escalation-trigger 1.
- **Mod-504 chapter 3 (peer-executive partnership contracts) and mod-504 chapter 6 (deferred-decision artifact).** The escalation path hooks into both. Chapter 4's escalation-trigger 2 (governance) and 3 (cross-org) route into mod-504 chapter 3 counterparts; the escalation-artifact *named decision date* shape mirrors mod-504 chapter 6.
- **[`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-02.** The staff-scope executive-audience RFC that the portfolio-scope bar reads against. Reading an mod-410 exercise-02 artifact (yours or a peer's) before authoring the portfolio-scope-RFC half of the charter is what grounds the eight axes in substrate.

## Problem statement

Produce three artifacts.

- **The review-bar charter.** Public-to-the-ML-org. Two-tier structure: portfolio-scope RFC rigor (eight axes + four principal-specific reads) and north-star-scope revision rigor (seven-check checklist + chair responsibilities). Explicit: *which tier applies to which artifact*, and the *tier-naming* ritual that runs at the top of every review.
- **The escalation charter.** Public-to-the-ML-org. The four triggers (with specific examples from this org), the four anti-triggers (also with specific examples), the escalation-artifact shape (trigger / local-state / specific-question / named-decision-date), the four principal responses (ratify / send back / convene / return to local scope), and the forum map (local team / portfolio / org-wide architecture-review / responsible-AI / hiring committee) that names which escalations cross which forums.
- **The walked escalation.** Private-to-this-exercise. One specific escalation — real or composite — walked end-to-end: the local review state, the trigger that fires, the escalation artifact as it would be written by the staff engineer, the principal's response written out in full, and the follow-up (the local reviewer coaching moment, the version-bump entry if any, the next-review date).

The charter is the Class A leverage-move artifact; the walkthrough is the sanity-check that the charter is operable under real pressure.

## Requirements

Populate a workspace directory `exercise-04-review-bar-charter/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-04-review-bar-charter/
├── README.md                        # index; FY cycle; charter version
├── review-bar-charter.md            # two-tier charter (public artifact)
├── escalation-charter.md            # triggers, anti-triggers, forum map (public artifact)
├── walked-escalation.md             # end-to-end walkthrough (private)
└── appendices/
    ├── forum-map.md                 # the five review-body forums and their scopes
    ├── decision-mode-worked-examples.md  # block / nudge / escalate / defer
    └── anti-trigger-worked-examples.md   # the four anti-triggers in action
```

### `review-bar-charter.md` — the two-tier charter

Chapter 4 § *the portfolio-scope RFC bar* and § *the north-star-scope revision bar* are the content. The charter is the published artifact every staff engineer and loop reviewer in the ML org reads before running or sitting in a review. 3–4 pages.

- **Preamble — half a page.** The charter's purpose (set the tiered review bar; name the escalation path to principal weight), the fiscal year and version, the co-authors (chapter 2 § *Class A how to author it* — co-authored with two or three of the org's most-trusted staff engineers; the published version carries their names), and the ratification cadence (quarterly review per chapter 2 § *Class A how you know it landed*).
- **The tier-naming ritual.** Half a page. Every review opens by naming its tier (portfolio-scope or north-star-scope). The tier-naming is what prevents the chapter 4 § *failure mode: running every review at north-star rigor* collapse. The ritual is one line: *"this review is at the <portfolio-scope / north-star-scope> tier; the rigor level is <eight axes / seven-check>."* Named at the top of every review's agenda.
- **The portfolio-scope RFC tier — 1 to 1.5 pages.**
  - **The eight axes.** Reproduce chapter 4 § *the eight axes the review has to touch*, specialised to this org's artifact names. For each axis: one-sentence summary of what the review reads for, one-sentence summary of what *absence* on this axis signals (either revision needed, reviewer missed it, or legitimate deferral documented).
  - **The four principal-specific reads.** Reproduce chapter 4 § *the principal's specific reads*: organisational-context, precedent, altitude, escalation-trigger. For each: a one-paragraph description specialised to this org.
  - **What the principal is *not* doing** (chapter 4 § *what the principal is not doing*). One paragraph: not re-authoring, not adding a ninth axis, not running the review. These are the discipline that keeps the tier calibrator-level, not shadow-chair.
- **The north-star-scope revision tier — 1 to 1.5 pages.**
  - **The seven-check checklist.** Reproduce chapter 4 § *the seven-check north-star review checklist*: paired-artifact discipline, version-bump justification, additive-by-default, peer-platform co-authorship, governance posture, migration plan with named owners and dates, rollback plan. For each: one-sentence summary of what the check reads for.
  - **The review meeting ritual.** Chapter 4 § *the review meeting itself*: pre-read is required and enforced; the four decision modes are named; the *"what is not on the agenda"* section; the rationale is captured, not just the decision. One paragraph per element.
  - **The chair's responsibilities.** Chapter 4 § *the principal's specific responsibilities as chair*: set the agenda in advance, keep the room at altitude, force the resolution, write the meeting note. The chair is the principal (or an explicit named delegate during principal unavailability — chapter 4 § *failure mode: never chairing the north-star review* is the parent anti-pattern).
- **Interaction with the escalation charter.** Half a page. The pointer to `escalation-charter.md` and the explicit statement that the tiered bar and the escalation path are *companion* mechanisms — one does not work without the other.

Constraint: the charter is written to be read, not to impress. If a staff engineer who has never sat on an ML org review cannot read the charter in 15 minutes and know what tier their review is at, the charter is overwritten.

### `escalation-charter.md` — the escalation-and-anti-escalation path

Chapter 4 § *the escalation path* is the content. 2–3 pages.

- **Preamble — 2–3 sentences.** The escalation charter's job: lift a lower-level review to principal weight *only* when one of the four triggers fires. Not before; not for reasons that are not on the list.
- **The four triggers — one paragraph each.** Reproduce chapter 4 § *the four escalation triggers*:
  1. The direction requires a north-star architecture revision.
  2. The direction crosses a governance obligation the staff engineer cannot commit to.
  3. The direction has cross-org consequences that require executive-branch partnership.
  4. The direction is stuck on a technical judgment the local reviewers are split on.
  Each paragraph grounds the trigger in a *specific example from this org or a composite org*. The example is what makes the trigger operable; a generic restatement of the chapter is not sufficient.
- **The four anti-triggers — one paragraph each.** Reproduce chapter 4 § *the four escalation anti-triggers*:
  1. "The team wants a principal to sign off."
  2. "The decision is important."
  3. "The principal has opinions."
  4. "The team wants to move faster than the local review body."
  Each paragraph grounds the anti-trigger in a *specific example*. If you cannot produce a concrete example, the anti-trigger is not yet operable in the org and will not fend off escalations in practice.
- **The escalation artifact shape.** Chapter 4 § *the escalation artifact*. The four parts: the trigger (one paragraph), the local review's state (one paragraph), the specific question for the principal (one page), the named decision date. Reproduce the shape verbatim; this is what the staff engineers in the org will author against. Include a one-page *template* at the end of this section — not just the description. The template is what the staff engineer fills in, and its specificity is what makes escalations well-shaped.
- **The four principal responses.** Chapter 4 § *the principal's response*: ratify, send back with specific asks, convene the north-star review body, return to local scope. One paragraph each, specialised to this org — including the convention that each response is *written and posted in the canonical location* (not verbal; verbal responses lose the teaching).
- **The forum map pointer.** The forum map (`appendices/forum-map.md`) is where the forums are enumerated. The charter cites the map and makes the convention explicit: escalations name the forum they are heading *to* and the forum they are *not* going to. Chapter 4 § *interaction with the review body forums* is the reference.
- **The coaching convention.** One paragraph. When the principal returns an escalation to local scope (response 4), the response is also a *coaching moment* for the local reviewer. Chapter 4 § *failure mode: coaching through the review's outcome, not its process* is the parent anti-pattern; the charter names the convention explicitly so local reviewers know a *return to local scope* is coaching, not dismissal.

Constraint: the charter is specific. A charter that reads *"escalate when it is important"* has not fended off anti-trigger 2; a charter that reads *"the principal's response is to review and get back to you"* has not instantiated the four-response discipline. If the charter could apply to a non-ML org without rewriting, it is not grounded.

### `walked-escalation.md` — the end-to-end walkthrough

Private. 2 pages. One specific escalation, walked through the charter.

- **The scenario — 3–5 sentences.** The specific review that produced the escalation (team, scope, artifact kind), the specific trigger that fires (one of the four), the specific local-review state.
- **The escalation artifact as written.** Fill in the escalation-charter template verbatim: the trigger (one paragraph), the local review's state (one paragraph), the specific question (one page), the named decision date. Written as the staff engineer would write it, not as the principal would want them to write it — the walkthrough tests whether the template is operable, so authoring in staff voice is deliberate.
- **The principal's response — written in full.** Pick one of the four responses (ratify / send back / convene / return to local scope). Write the response as a markdown message that would be posted in the canonical location. Include the specific technical reasoning, the specific coaching note (if return-to-local-scope), the specific next-review date (if send-back), the specific version-bump entry (if ratify-at-principal-weight).
- **The follow-up.** 2–3 bullets. What the local reviewer does next; what the principal does next; which forum the artifact proceeds to (if any); what the review-body meeting note (chapter 4 § *the principal's specific responsibilities as chair*) says if the escalation convened the north-star review body.
- **The sanity-check reflection.** Half a page. Did the trigger fire cleanly? Did any anti-trigger also apply (and did the charter help disambiguate)? Was the escalation artifact well-shaped (did the template collect the right information)? Did the principal's response transfer the teaching to the local reviewer (chapter 4 § *response shape teaches local review bodies*)? If any answer is "not really," the charter has a gap — name it and loop back into `review-bar-charter.md` or `escalation-charter.md` for the fix.

Constraint: this walkthrough is specific. A generic scenario does not test the charter. If the scenario reads *"a team wanted to launch something and needed principal review,"* it is not grounded; rewrite with the specific team, the specific artifact kind, the specific trigger.

### `appendices/forum-map.md` — the five review-body forums

Chapter 4 § *interaction with the review body forums* is the reference. Half a page to one page. A simple table (forum, scope, owner, cites-up-to, cites-down-to) with the five forums:

- Local team review body.
- Portfolio review body.
- The org-wide architecture-review body (mod-503 chapter 7).
- The responsible-AI review body (`head-of-ai-governance-learning` peer track).
- The hiring committee (chapter 3).

For each forum: one line on scope, one line on owner, one line on the forum *above* (where escalations route up), one line on the forum *below* (where escalations route down). The map is what makes escalations well-targeted.

### `appendices/decision-mode-worked-examples.md` — the four decision modes

Mod-503 chapter 7 § *four decision modes* is the parent reference; chapter 4 cites it. Half to one page. Four short examples (one paragraph each) showing one *block*, one *nudge*, one *escalate*, and one *defer* decision from this org's recent reviews (or composite). Each example names the artifact, the material point, the specific decision mode invoked, and the one-sentence rationale captured in the meeting note.

Constraint: the examples are specific and distinguish the four modes. If the *block* example and the *nudge* example read interchangeably, the examples are not calibrated.

### `appendices/anti-trigger-worked-examples.md` — the four anti-triggers

Half to one page. Four short examples (one paragraph each) showing an escalation that *looked* like it should fire a trigger but was actually one of the four anti-triggers in disguise. Each example names: the triggering ask the staff engineer or team made, the anti-trigger that actually applied, and the principal's response that returned the decision to local scope with a coaching note.

The appendix is what makes anti-trigger discipline tangible. Without it, anti-triggers are abstract and never fire; with it, local reviewers see the pattern and self-regulate.

## Starter guidance

- **Author the north-star-scope tier first; it is the shorter and more constrained half.** The seven-check checklist is tight; the eight axes plus four principal reads are the longer prose. Starting with the shorter half gives the longer half a shape to lean against.
- **The *what the principal is not doing* section is load-bearing.** The modal failure of a review-bar charter is turning the principal into a shadow re-author or a ninth-axis-adder. Chapter 4 § *what the principal is not doing* names the discipline; the charter is where that discipline becomes org-wide.
- **The escalation template is more useful than the escalation description.** A one-page template that the staff engineer can copy-paste and fill in is 10x more useful than a two-paragraph description of what the escalation should contain. Author the template.
- **Draft the walked-escalation last, not first.** The walkthrough tests the charter; if the charter is unstable, the walkthrough drifts. Lock the charter first; let the walkthrough surface the gaps; return to the charter for the fix.
- **The forum map is what makes multi-forum escalations well-shaped.** Chapter 4 § *interaction with the review body forums* names the governance-loop-hop pattern; the forum map is the artifact that fends it off. Treat it as a first-class appendix, not an afterthought.
- **Co-author the charter.** Chapter 2 § *Class A how to author it* is explicit: co-authored with two or three of the org's most-trusted staff engineers. Even in an exercise, name the co-authors (real or composite); the authorship convention is the leverage. If you cannot name a co-author, the charter is *your* document, not the org's — and the chapter 2 § *failure mode: the leverage move authored alone* applies.
- **Interact with exercise-02 explicitly.** If one of exercise-02's committed moves is Class A, this exercise's `review-bar-charter.md` is where its substance lives — same artifact, different workspace. Cross-reference. If not, the charter here is a candidate for exercise-02's option list with a specific threshold criterion.
- **Interact with exercise-03 explicitly.** If exercise-03's `class-c-change-proposal.md` surfaces a loop-level calibration gap that depends on a review-bar change (e.g., the portfolio-deep-dive rubric change requires the review-bar charter to formalise the altitude-check), the two artifacts cite each other.
- **Time-box each artifact.** Review-bar charter: 60 minutes. Escalation charter: 45 minutes. Walked-escalation: 45 minutes. Forum map: 10 minutes. Decision-mode worked examples: 15 minutes. Anti-trigger worked examples: 15 minutes. Total: roughly 3 hours. If you exceed 4 hours, you are over-authoring one of the artifacts.

## Acceptance criteria

The exercise is done when:

- [ ] `review-bar-charter.md` names two tiers (portfolio-scope and north-star-scope) explicitly and includes the tier-naming ritual as a one-line opening for every review.
- [ ] The portfolio-scope tier reproduces all eight axes (chapter 4 § *the eight axes the review has to touch*) and all four principal-specific reads (chapter 4 § *the principal's specific reads*).
- [ ] The portfolio-scope tier includes a *what the principal is not doing* section that names at least three disciplines (not re-authoring, not adding a ninth axis, not running the review).
- [ ] The north-star-scope tier reproduces all seven checks (chapter 4 § *the seven-check north-star review checklist*).
- [ ] The north-star-scope tier includes the review-meeting ritual (pre-read required, four decision modes named, *what is not on the agenda*, rationale captured) and the chair's four responsibilities.
- [ ] The charter is co-authored with 2–3 named co-authors (chapter 2 § *Class A how to author it*). The co-authors are named, not anonymous.
- [ ] `escalation-charter.md` names all four triggers and all four anti-triggers, each grounded in a specific example from this org or composite.
- [ ] The escalation artifact shape is reproduced *with a one-page template* that staff engineers can copy and fill in.
- [ ] The four principal responses are described explicitly and the convention that each response is *written and posted in the canonical location* is named.
- [ ] The forum-map pointer and the coaching convention (return-to-local-scope is coaching, not dismissal) are both present.
- [ ] `walked-escalation.md` is a specific scenario (named team, named artifact kind, named trigger), not generic.
- [ ] The walkthrough fills in the escalation template verbatim and writes the principal's response as a markdown message that could be posted in the canonical location.
- [ ] The walkthrough's sanity-check reflection names at least one gap in the charter that the walkthrough surfaced (or honestly states no gaps were found and why).
- [ ] `appendices/forum-map.md` names all five forums with scope, owner, cites-up-to, and cites-down-to.
- [ ] `appendices/decision-mode-worked-examples.md` has one example per decision mode (block / nudge / escalate / defer) that distinguishes them from each other.
- [ ] `appendices/anti-trigger-worked-examples.md` has one example per anti-trigger showing the triggering ask, the anti-trigger that applied, and the principal's response.
- [ ] The exercise passes the *tier-naming test*: picking a random RFC from this org (or composite), you can name its tier in one sentence without ambiguity.
- [ ] The exercise passes the *escalation-template operability test*: a staff engineer unfamiliar with the charter could read the template and fill it in to produce a well-shaped escalation. If they could not, the template is under-specified.
- [ ] The exercise passes the *drift-mode check*: none of chapter 4's six failure modes are visible in the charter (tier-collapse, never-chairing north-star, escalating-on-opinion, refusing-to-escalate, reviewing-without-rationale, outcome-feedback-not-process-coaching).

## Stretch goals

- **Share the charter with one peer platform-side principal.** Chapter 2 § *Class B — the north-star architectural revision* names the co-authorship convention with the peer platform-side principal; the review-bar charter has the same seam. If the charter cannot be read and understood by the peer platform-side principal in 15 minutes, re-write it.
- **Draft the escalation retrospective for one real (or composite) escalation that was mis-shaped.** One page. What was the mis-shape (anti-trigger-fired-but-called-trigger; trigger-fired-but-escalated-to-wrong-forum; template-filled-but-decision-date-missing); what did the principal's response correct; what does the charter need to change to prevent the same mis-shape next cycle. The retrospective is the input the quarterly chapter 2 § *Class A how you know it landed* audit reads against.
- **Author the *review-pattern training* companion.** If staff engineers in the org have never seen a well-run north-star-scope review, the charter does not land on its own. One page: a short training doc that walks a staff engineer through what to expect, what to pre-read, how to participate, and how to escalate if the review surfaces a trigger. Chapter 2 § *Class A how it looks in practice* names the supporting handbook — this is the ground-level version.
- **Compose with exercise-02 (leverage-move commitment).** If this exercise's `review-bar-charter.md` is one of exercise-02's two committed moves (Class A), the exercise-02 commitment memo cites this exercise and this exercise cites exercise-02's cadence and co-authors. The two artifacts should be internally consistent across workspaces.
- **Compose with exercise-03 (hiring-loop calibration).** If exercise-03's `class-c-change-proposal.md` surfaces a review-bar implication (e.g., the portfolio-deep-dive rubric change requires the review-bar charter to formalise the altitude-check for portfolio artifacts), author the cross-reference explicitly.
- **Author the version-bump playbook.** The review-bar charter will version-bump as the org evolves (chapter 2 § *failure mode: the leverage move that never sunsets* is the anti-pattern if it does not). One page: when the charter version-bumps, what triggers the bump (new tier needed? new axis consolidation? forum map changed?), who co-authors the bump, what the migration is for in-flight reviews. The playbook is what keeps the charter *living* rather than frozen.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-04-review-bar-charter/` is what you extend across quarters: the review-bar charter is the baseline chapter 6 § *committed-leverage-move check* audits against if Class A is in your committed move set; the escalation walkthrough stacks across cycles to produce the escalation-retrospective substrate (stretch goal 2); the forum map and the two worked-example appendices are referenced by exercise-03's debrief-protocol escalation path and by future exercise-04 instances across fiscal years.
