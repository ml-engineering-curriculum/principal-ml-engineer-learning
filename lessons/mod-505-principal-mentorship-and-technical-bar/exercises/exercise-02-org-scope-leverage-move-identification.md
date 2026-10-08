# exercise-02: Pick the Two Leverage Moves You Commit to Next Fiscal Year

**Estimated effort:** 3 hours

## Objective

Run the friction-count sensing pass from chapter 2 § *selection discipline — test 1*, apply the three-test discipline (friction-count, class-diversification, named co-authors), and produce the fiscal-year leverage-move commitment artifact for the principal seat you hold (or are preparing to hold). The commitment names *two* leverage moves — one per canonical class — with co-authors, drafted / review / published cadence, and the specific *"how you know it landed"* criteria from chapter 2 § classes A–D.

The deliverable is the single artifact you would carry into the next 1:1 with your line manager, your peer executive counterparts (mod-504 chapter 3), and the two or three staff engineers whose co-authorship each move depends on. It is also the artifact chapter 6 § *quarterly review item 3* and § *committed-leverage-move check* audit against.

## Prerequisites

- **Chapter 2 read end-to-end.** Especially the three load-bearing properties (once-authored / repeatedly-used, absent-you effective, org-scope reach), the four canonical classes (A canonical review pattern, B north-star architectural revision, C bar-raising interview change, D shared eval standard), the three selection tests, and the six failure modes.
- **Chapter 6 § *the "chasing every bet at once" drift*.** Two moves per fiscal year is the modal number; three is the ceiling; four is drift. This exercise is where that discipline shows up as artifact.
- **Mod-502 chapter 3 (sequencing bets, hedges, options).** The same portfolio discipline applied one altitude down. The exercise's selection logic reads directly from this.
- **Mod-503 chapter 6 (evolution plan and version-bump triggers).** If one of your two moves is a Class B north-star architectural revision, mod-503 chapter 6 is the parent discipline — your move cites it, it does not re-derive it.
- **Optional but recommended: a current org posture.** You cannot run test 1 (friction-count) on an org you do not know. If you are doing this exercise on a hypothetical or past org, be explicit in the artifact — a composite org is fine, but it must have one named top-3 bet set, one named ML org structure, and one named set of load-bearing teams.

## Problem statement

Produce the FY-next *leverage-move commitment artifact*: the two moves the principal is committing to for the next fiscal year, each in a different canonical class, each with named co-authors, each with the landing-criteria pre-registered. Also produce the private *option list* — the moves that passed test 1 but did not make the cut — so the quarterly review (chapter 6) has an explicit tracked set to return to when a committed move lands, slips, or is retired.

The deliverable is three artifacts.

- **The friction-count sensing log.** Private. The five staff engineers you talked to this quarter (or the five you would talk to), the specific friction each named, and the aggregated friction tally. The log is the substrate for test 1.
- **The commitment memo.** Public-to-the-ML-org. The two committed moves, each with one page: class, working title, co-authors, draft / review / publish cadence, landing criteria, and the *"what this is not"* section (chapter 2 § *what is not a leverage move*) that fends off scope creep.
- **The option list.** Semi-private (shared with your line manager and peer executive counterparts, not with the whole org). The 3–6 moves that passed test 1 but did not make the two-slot cut, each with one paragraph on why they did not, and the sensing threshold that would move them into the committed slot next cycle.

Together these three artifacts are the exercise deliverable. They are also the baseline the quarterly review audits against — the FY cadence this exercise sets up is what chapter 6 instantiates.

## Requirements

Populate a workspace directory `exercise-02-leverage-move-commitment/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-02-leverage-move-commitment/
├── README.md                    # index; FY cycle; current state of the two moves
├── friction-count-log.md        # test 1 substrate; 5 staff-engineer sampling
├── commitment-memo.md           # the two committed moves (public-to-org)
├── option-list.md               # moves that did not make the cut (semi-private)
└── appendices/
    ├── class-coverage-check.md  # test 2 — class diversification against org history
    └── co-author-briefs.md      # test 3 — the two or three co-authors per move
```

### `friction-count-log.md` — the test 1 substrate

Chapter 2 § *selection discipline — test 1* is the reference. The log is the input that makes test 1 defensible rather than impressionistic. 1–2 pages.

- **Sampling frame — 2–3 sentences.** Which 5 staff engineers you selected and why (stratified: 2 teams shipping well, 2 teams stuck, 1 team you do not know well). Not your friends; a stratified sample.
- **The prompt you ran — one line, verbatim.** The exact wording of the question you asked each staff engineer. *"What is the friction you are carrying that is not yours to fix but is slowing every launch your team ships?"* is the chapter 2 canonical phrasing; adjust only if the org's vocabulary demands it.
- **The five responses — one paragraph each.** Named engineer, named team, named friction. Verbatim quote where available; summary otherwise. Explicit about *frequency* ("hit this twice last quarter") and *scope* ("blocks every launch, not just the current cycle").
- **The friction tally.** A simple table: friction description, number of mentions, class candidates (A / B / C / D) that would address it, est. landing cycle (6 / 12 / 18 months per class discipline).
- **The two frictions above the test 1 threshold.** The frictions that showed up on three or more lists. These are the sanctioned candidates for the two-slot commitment. If fewer than two frictions crossed the threshold, name the gap honestly — you are either not close enough to the teams (chapter 5 § *technical-culture leverage* is the sensing fix) or the org is in a state where no org-wide friction is top-of-mind, in which case the smaller-batch leverage class is probably the right call.

Constraint: the log is honest, not persuasive. If three of your five staff engineers named the same friction and it is a friction *you had not previously prioritized*, say so in the log — that is the discovery test 1 is for.

### `commitment-memo.md` — the public artifact

One page per committed move, two pages total (plus a half-page preamble). This is the artifact every staff engineer in the ML org, your peer platform-side principal, your line manager, and your peer executive counterparts should be able to read and understand what you have committed to and when.

- **Preamble — half a page.** Fiscal year, the number of moves committed (two, by discipline), the three selection tests and how each move passed them, the retirement candidates from last fiscal year (if applicable), and the pointer to the option list.
- **Move 1 — one page.**
  - **Class (A / B / C / D).** Named explicitly. If you had to force the move into a class, re-examine whether it is really a leverage move.
  - **Working title.** 10–15 words. *"Shared eval standard v1 for Gen-AI launches, co-authored with the ML platform team and the Gen-AI-Product staff engineer."* Not *"improve eval."*
  - **Co-authors.** Two or three named engineers (or peer principal, or hiring-committee chair, depending on class). The co-authorship is what makes the move land, per chapter 2 § *selection test 3*. If no co-authors are named, do not publish the memo.
  - **The friction this move removes.** Grounded in the friction-count log. Which of the five staff engineers named the friction; which teams it affects; the scope of the lift.
  - **The cadence — draft, review, publish, first-landing-report dates.** Explicit day-level dates. Chapter 2 § *selection discipline* names the modal shape: drafted by month 3, reviewed by month 4, published by month 5, first landing report by month 11.
  - **Landing criteria — the "how you know it landed" set.** Reproduce the criteria from chapter 2 §§ *A how you know it landed*, *B how you know it landed*, *C how you know it landed*, or *D how you know it landed* for the move's class, specialised to this move's specific scope. These are what the FY+1 review will audit against.
  - **What this is not.** Explicit scope boundary. The move is not a rewrite; not a mandate; not a tool. Chapter 2 § *what is not a leverage move* is the pattern reference. Half a paragraph.
- **Move 2 — one page.** Same shape as Move 1, in a *different* class (test 2). If both moves are in the same class, redo test 2 and pick a different second move.

Constraint: two pages total for the two moves. If a move cannot fit on one page, it is not yet scoped as a leverage move — it is scoped as a program.

### `option-list.md` — the moves that did not make the cut

The option list is where the frictions that passed test 1 but did not make the two-slot commit live. It is semi-private (shared with your line manager and peer executive counterparts). 1–2 pages.

- **The 3–6 options.** For each: friction (one line), class candidate (A / B / C / D), reason it did not make the current cut (test 2 class-collision, test 3 no co-author, cadence overload, dependency on another in-flight move, etc.), threshold criterion that would move it into the committed slot (*"if the eval-standard move lands by month 6 instead of month 11, this moves into the slot"* or *"if the hiring-committee chair rotates to someone who can co-author, this becomes viable"*).
- **Retirement candidates.** From your current fiscal year's committed set, which moves are approaching retirement — the three-year-old rubric nobody cites, the standard that has not been version-bumped in 18 months. Chapter 2 § *failure mode: the leverage move that never sunsets* is the parent reference. Name each with the retirement cadence.

Constraint: the option list is honest about what did not fit, not a wish-list. If a move is on the option list because *you* are not sure, say so; if it is on the option list because the *org* is not ready, say so; if it is on the option list because *no co-author* exists yet, say so.

### `appendices/class-coverage-check.md` — the test 2 substrate

Half to one page. A simple 2x4 table: rows are the four classes (A, B, C, D); columns are *"funded in the last fiscal year"* and *"funded in the fiscal year before that"*. For each cell, note the specific leverage move the org funded in that class (or *—* if none). Then one paragraph on which class is the strongest candidate for the next move, grounded in the table.

The table makes test 2 (class-diversification) legible rather than impressionistic. Chapter 2 § *selection test 2* is the reference.

### `appendices/co-author-briefs.md` — the test 3 substrate

One paragraph per co-author, grouped by move. For each named co-author:

- **Who they are.** Name, current scope (team, role, L-band).
- **Why they are the right co-author for this move.** The specific capability or legitimacy they bring (deep RecSys authorship for Move 1; chair of the hiring committee for Move 2; peer platform-side principal because the move touches substrate).
- **Whether they have agreed.** If yes, by what date and in what forum. If no, by what date you will have the conversation and what the fallback is if they decline.
- **How credit will be transferred.** Chapter 5 § *co-authorship as the technical-culture practice* names the three properties; this appendix is the per-co-author instantiation.

Constraint: one paragraph per co-author, named explicitly. If you cannot name a co-author with specificity, test 3 fails and the move should not be in the commitment memo.

## Starter guidance

- **Do test 1 first, before you touch the memo.** The friction-count log is the input the memo rests on; if you draft the memo first and run test 1 after, you will unconsciously bias the sensing toward the moves you have already committed to. Chapter 2 § *selection discipline* is explicit on the ordering.
- **The 5 staff-engineer sample is stratified.** The modal failure of test 1 is sampling only the engineers you already talk to regularly — who are usually the ones who already share your model of the org's friction. Chapter 2 § *selection test 1* is explicit on the stratification: 2 shipping-well, 2 stuck, 1 you do not know well. If your five are all in the first category, redo the sample.
- **Do not fund both moves in the same class.** Even if friction-count surfaced two frictions that fall into Class D (shared eval standard), fund one via Class D and the other via a different class (A, B, or C) that addresses the same frictions from a different angle. Class-diversification is what keeps the portfolio balanced across the four surfaces chapter 2 names.
- **Co-authors are a precondition, not a nice-to-have.** The modal reason a leverage move does not land is that it was authored alone and treated as *the principal's* move rather than *the org's*. Chapter 2 § *failure mode: the leverage move authored alone* is the reference. If you cannot name co-authors for one of your two moves, the move is not ready — move it to the option list, pick a different candidate from the option list, and re-run test 3.
- **The commitment memo is the artifact your successor could read in year 3.** The memo is dated at the FY start; your successor (or you, 24 months from now) should be able to read it, see what you committed to, see the landing criteria, and audit whether the moves landed. If the memo reads only to this quarter's audience and loses meaning in 12 months, re-write it with the longer horizon in mind.
- **Keep the option list live.** Chapter 6 § *quarterly review item 3* presumes the option list exists and is current. The quarterly audit returns to the list to decide whether to swap a committed move with an option — the list is not a decoration.
- **Time-box each artifact.** Friction-count log: 45 minutes (plus the actual 5 staff-engineer conversations if they are not already in your calendar). Commitment memo: 60 minutes. Option list: 30 minutes. Class-coverage appendix: 20 minutes. Co-author briefs: 30 minutes. Total: roughly 3 hours of writing; the 5 conversations are additional. If the writing exceeds 4 hours, you are over-authoring one of the artifacts.

## Acceptance criteria

The exercise is done when:

- [ ] `friction-count-log.md` names 5 stratified staff engineers (not all friends; not all one team).
- [ ] The log quotes or summarises each engineer's response with a named friction and a named scope ("blocks every launch", "slows the quarterly planning", etc.).
- [ ] The friction tally identifies at least one friction that was named by three or more engineers. If none, the log acknowledges this honestly rather than fabricating a cross-engineer pattern.
- [ ] `commitment-memo.md` fits on two pages (plus the half-page preamble) and names exactly two committed moves. Not three; not one.
- [ ] Each committed move is in a *different* canonical class (A / B / C / D). If both moves are in the same class, re-run test 2 before publishing.
- [ ] Each committed move has 2–3 named co-authors with specific roles (staff engineer M of the RecSys team, hiring committee chair J, peer platform-side principal P). *"Collaborate with the ML org"* is not a co-author.
- [ ] Each committed move has a draft / review / publish / first-landing-report cadence with day-level dates.
- [ ] Each committed move's landing criteria are reproduced from chapter 2 §§ A–D with specialisation to this move's scope. The criteria are *measurable* at the 6 / 12 / 18 month marks.
- [ ] Each committed move has a *"what this is not"* section that names at least one scope boundary (not a mandate; not a tool; not a rewrite).
- [ ] `option-list.md` has 3–6 options with specific class candidates, specific disqualifying reasons, and specific thresholds that would move them into the committed slot.
- [ ] The option list names at least one retirement candidate from the current fiscal year's committed set (unless this is the principal's first fiscal cycle in seat).
- [ ] `class-coverage-check.md` has the 2x4 table filled in with specific prior leverage moves (or honest *—* entries) and a one-paragraph recommendation for the current cycle's class pick.
- [ ] `co-author-briefs.md` has one paragraph per named co-author, including whether they have agreed to co-author.
- [ ] The exercise passes the *co-author verification test*: if you walked up to each named co-author today, they would recognise themselves as a co-author on the move. If not, the briefs are aspirational, not grounded.
- [ ] The exercise passes the *drift-mode check*: none of chapter 2's six failure modes are visible in the memo (one-per-week churn, authored-alone, measured-on-activity, never-sunsets, confused-with-strategy, displaces-staff-scope).

## Stretch goals

- **Share the commitment memo with one peer principal in another org.** The peer-principal exchange from chapter 6 § *interaction with the peer-principal community* is the closest thing to an external audit the IC-principal seat has. Ask the peer whether the two moves pass the three tests on independent reading; pressure-test the landing criteria.
- **Pre-draft the mid-year revision.** Six months into the fiscal cycle, the commitment memo gets a revision — one move may have landed early, another may have slipped. Pre-draft the revision shape (what you would need to see at month 6 to retire Move 1 early, swap in an option, or extend Move 2's cadence). This is where the option list becomes operationally useful.
- **Author the first draft of one of the two moves.** The commitment memo names the move; the move itself is a separate artifact — a rubric (Class A), an architecture revision (Class B), an interview-change proposal (Class C), or an eval standard (Class D). Draft one page of the first move's substantive artifact as a sanity check on scope. If the first page is 400 words and reads clearly, the move is scoped; if it balloons past 1500 words, the move is still a program.
- **Pair this exercise with exercise-04 (review-bar charter).** The two committed moves may each land Class A review-pattern work; exercise-04's charter is where the review-pattern substance lives. The exercises are companions, not duplicates — commit the moves here, author the charter there.
- **Compose with exercise-03 (hiring-loop calibration).** If one of the two committed moves is a Class C bar-raising interview change, exercise-03's output is where its substance lives. Keep the exercises distinct: this exercise commits the move at the portfolio level; exercise-03 authors the specific Class C artifact.
- **Author a *leverage-move retrospective* for one shipped move you have observed in prior roles (yours or a peer's).** One page. What class was the move; what friction did it remove; did it meet its landing criteria at 6 / 12 / 18 months; what was the retirement cadence; what would you do differently. This is a sanity-check on the landing-criteria discipline — if the retrospective is harder to write than the forward-looking commitment, the forward-looking landing criteria are probably not tight enough.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-02-leverage-move-commitment/` is what you extend across the module and across quarters: the commitment memo is the baseline chapter 6 § *committed-leverage-move check* audits against; the option list is where exercise-04's Class A rubric work and exercise-03's Class C work route if they are not already in the committed set; the friction-count log is the FY-cycle substrate the next fiscal year's sensing pass builds against.
