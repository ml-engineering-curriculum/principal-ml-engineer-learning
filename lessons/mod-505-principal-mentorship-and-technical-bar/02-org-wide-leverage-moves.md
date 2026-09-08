# Org-Wide Leverage Moves — The Small Set That Lifts the Whole ML Org

> Chapter 2 of mod-505. Prerequisite: chapter 1 (staff-engineer growth conversation) and mod-501 chapter 5 § *Theme 4* (the *multiply the effectiveness of every ML team* framing). Downstream: chapter 3 (hiring-loop calibration) and chapter 4 (review bar) are two of the four leverage-move classes this chapter names.

## Why "leverage" is the load-bearing word

The Upstart *Staff / Principal ML Engineer* posting states the target sentence for this chapter almost verbatim: *"multiply the effectiveness of every ML team in the org."* The verb is *multiply*. The object is *every ML team*. Both matter.

- *Multiply*, not *add*. The principal is not the tenth engineer on a team; they are the change that makes the ten engineers on ten teams each do their work slightly (or noticeably) better. If a principal's contribution can be described as *"they did the work of two staff engineers this quarter"*, they are producing *additive* value at the wrong altitude. The mod-501 chapter 5 § *Theme 4* framing collapses.
- *Every ML team*, not *the team the principal happens to sit near*. A leverage move that lifts one team is a staff-scope contribution — legitimate, but owned by the level below (`staff-ml-engineer-learning` mod-407 § portfolio-scope work). A leverage move that lifts every team lands the principal's *coach* verb at the object mod-501 chapter 5 § *Theme 4* named.

DAT Freight & Analytics states the same idea from the other angle: *"delivering solutions whose impact scales across teams and the broader organization."* Coupang: *"exceptional ability to influence technical direction across multiple teams and organizations."* The verb varies (multiply, scale, influence); the object is consistent. This chapter is about picking the small number of moves that carry that verb at that object.

The small-number part is not decorative. A principal chasing every possible leverage move ends up with none of them landing — chapter 6 § *the "chasing every bet at once" drift* is the failure mode. This chapter names the four canonical leverage-move *classes* and the discipline for selecting among them.

## What a leverage move *is*

A leverage move is a specific artifact, standard, or ritual you author (or materially revise) that, once in place, changes how *every* team in the ML org does the work — without you being in the room when they do it.

Three properties are load-bearing.

- **Once-authored, repeatedly-used.** The move is a written artifact or a durable ritual, not a one-off intervention. The design review you attended last Thursday is not a leverage move; the design-review *rubric* every team's reviews are now run against is. The eval you built for the RecSys team is not a leverage move; the *shared eval standard* every ML launch must clear is.
- **Absent-you effective.** Once in place, the move keeps working when you are on vacation, when you rotate onto a different bet, when you leave the org. The move that only works because *you personally* show up to enforce it is a staff-scope move at principal-scope opportunity cost.
- **Org-scope reach, not team-scope reach.** A canonical eval standard is a leverage move; that team's eval harness is not. The reference-architecture revision every team's next re-platform will build against is a leverage move; the re-platform of one team's system is not.

The three properties, taken together, are why the leverage frame maps to the mod-502 (strategy) / mod-503 (architecture) / mod-505 (technical bar) trinity: strategy and architecture are two leverage-move classes; the four moves this chapter names are the *rest*.

## The four canonical leverage-move classes

Every org has different starting conditions and different pain, but the *classes* of move that lift the whole ML org are stable. Four cover the space; every leverage move you make lands in one of them. If you have a *fifth* candidate that does not fit, that is a signal to re-examine whether it is really a leverage move or a staff-scope contribution.

### Class A — the canonical review pattern

**What it is.** A written *how-we-review* rubric that every team's design reviews, RFC reviews, and launch reviews are calibrated against. Named review categories, per-category checklist, per-category authority to *block*, and the escalation path when a review reveals a bar-crossing question the local reviewer cannot resolve. Chapter 4 is the reference for the *content* of the bar; this class is the *ritual* around it.

**Why it lifts every team.** Every ML team already runs some kind of review. The absence of a canonical rubric means each team's reviews drift toward whatever the loudest voice on that team happens to care about — one team over-indexes on p50 latency, one team over-indexes on offline metrics, one team stops running launch reviews entirely because they *"slow shipping."* A canonical rubric normalises the surface every team is looking at without prescribing how they solve for it.

**What it looks like in practice.** A one-page rubric (5–8 review categories: data quality, eval bar, load / capacity, monitoring / SLO, cost / TCO, governance / risk, model-registry / provenance, launch gates), a supporting how-we-review handbook (10–20 pages of examples and worked-through prior reviews), and a *quarterly ratification* ritual where the rubric itself is reviewed by the ML org's staff-plus tech leads. Mod-503 chapter 7 (running the org-wide architecture-review body) is the parent ritual; this class is the *review-pattern layer* underneath it.

**How you know it landed.** Six months after publication: the rubric is cited by name in individual team's design docs. Twelve months after publication: a staff engineer on a team you do not sit near uses the rubric to *block* a launch, and the block is respected without your involvement. That is *absent-you* effective.

**How to author it.** Do not draft it in a room by yourself. Draft it with two or three of the org's most-trusted staff engineers, each of whom will co-sign the published version — that is what makes it *the org's* rubric rather than *your* rubric. Chapter 5 § *co-authorship for technical culture* is the practice.

### Class B — the north-star architectural revision

**What it is.** A material revision to the north-star architecture (mod-503) — a new plane, a new canonical API contract, a version-bump on an existing contract that unblocks multiple teams' bets — that changes the shape every team's next-cycle work builds against. Mod-503 chapter 6 (evolution plan and version-bump triggers) is the reference; this class is the *rhythm* of authoring the version bumps.

**Why it lifts every team.** Every ML team plugs into the reference architecture (mod-503 chapter 1 § *the paired-artifact frame*). A revision that removes a shared friction — the eval-harness contract that every team is currently working around, the feature contract that every team's real-time features are struggling to fit — unblocks every team simultaneously. One revision, N teams' friction removed.

**What it looks like in practice.** Not a rewrite. The evolution-plan discipline from mod-503 chapter 6 is explicit: additive-by-default, deprecation-with-timeline, version-bumps only when the trigger table justifies them. A well-scoped revision is 10–30 pages of RFC-shaped writing, one 60-minute review body session, and a 3–6 month migration window during which the new version and the old version coexist.

**How you know it landed.** Six months after publication: at least two teams have migrated to the new version and reported it removed a friction they had been carrying. Twelve months after publication: the old version is deprecated on schedule; no team has requested an extension. Chapter 4 § *escalation path* is the mechanism if the deprecation is contested; the leverage is *absent-you* only if the deprecation holds without your personal enforcement.

**How to author it.** Draft with the peer platform-side principal (mod-503 chapter 8 § *co-authored interfaces*) and with the two or three staff engineers whose teams the revision unblocks. The co-authorship is what makes the revision *land*; a revision authored by the principal alone tends to be treated as *the principal's ask* rather than *the org's next step*.

### Class C — the bar-raising interview change

**What it is.** A specific, named change to the ML org's hiring loops — a new interview kind (e.g., a systems-and-tradeoffs interview at the staff-plus level), a new rubric on an existing interview (e.g., an eval-thinking rubric on the design interview), a change to the loop chair's decision protocol (chapter 3 is the reference), or a change to the debrief protocol that closes a repeated calibration gap. Chapter 3 walks the loop-level calibration practice; this class is one of the artifacts that comes out of it.

**Why it lifts every team.** Every team hires. Every new hire has to pattern-match to the ML org's technical bar. A bar-raising change made in the loop is a change that compounds — every next hire is closer to (or further from) the bar you want the org to hold. One rubric change lifts the bar for every hire in the following year.

**What it looks like in practice.** A written change proposal — one page: current state, proposed state, evidence (from calibration debriefs, from actual outcomes), migration plan (who trains on the new rubric, when it goes live, when it is re-reviewed). A trial run on 2–3 loops. A ratification session with the hiring committee. A change to the shared interview-question and rubric bank. Amazon's *Bar Raiser* program is the canonical inspiration for the *authority* half; the change-proposal shape is generic.

**How you know it landed.** Six months after publication: interviewers cite the change by name in debriefs. Twelve months after publication: at least one hiring decision has *flipped* because the new rubric caught something the old rubric would have missed — and the hiring committee ratified the flip without your involvement. Twenty-four months after publication: the new hires on the far side of the change are visibly stronger on the axis the change targeted. This class has the longest confirmation horizon; that is inherent, not a bug.

**How to author it.** Draft with the hiring committee chair and one or two loop chairs who have run enough loops to see the current calibration gap first-hand. The change should not be *your* opinion about what the bar should be; it should be a *ratified* change the loop chairs run. Chapter 3 § *coaching the loop chair* is the sponsorship half.

### Class D — the shared eval standard

**What it is.** The ML org's canonical eval bar — the specific eval categories every ML launch clears, the shared benchmark suite the org calibrates against, the LLM-as-judge protocol the Gen-AI teams share, the offline-online reconciliation discipline the RecSys teams share. Mod-503 chapter 3 § *plane 5 (evaluation)* is the reference for where the standard sits in the architecture; this class is the *authoring* of the standard.

**Why it lifts every team.** Eval is the single most repeatedly-underinvested-in surface across ML teams. Every team invents their own; the invention costs weeks of engineering per team; the results are not comparable across teams; a launch that clears one team's bar would fail another team's bar. A canonical standard removes the reinvention, makes results comparable, and gives the review pattern (Class A) something concrete to enforce against.

**What it looks like in practice.** A canonical eval spec (5–10 pages): eval categories, dataset conventions, statistical significance conventions, reporting shape, launch-gate thresholds by category. A shared eval harness — either a real codebase (`ml-org/eval-toolkit`) or a canonical contract every team's harness must satisfy. A reference eval report for each named launch category (RecSys launch, Gen-AI launch, foundation-model fine-tune launch). A quarterly review of the standard against the actual launches that happened. Google's *ML Test Score* rubric (Breck et al., 2017 — see resources.md) is a canonical inspiration for the *rubric* half; NIST AI RMF and the *Generative AI Profile* overlay are the parent frameworks for the categories at Gen-AI altitude.

**How you know it landed.** Six months after publication: at least half the teams have run at least one launch through the standard. Twelve months after publication: a launch is *blocked* on the standard's threshold and the block is respected. Eighteen months after publication: the standard has been version-bumped at least once in response to a real gap surfaced by the actual launches — the standard is *living*, not frozen.

**How to author it.** With the two or three teams whose launches the standard first covers, plus the eval-platform team (owned by the peer platform-side principal). Mod-503 chapter 4 § *eval-harness contract* is the contract-shape reference; the *content* of the standard is what this class authors.

## Selection discipline — the small number is small

Four classes. The temptation is to run all four in parallel. Do not. Two moves in parallel is the modal number a principal can carry over a fiscal year at defensible depth. Three is the ceiling; four is chasing every bet.

The selection discipline has three tests.

- **Test 1 — which move removes the friction the most teams are currently carrying?** Talk to five staff engineers in the ML org this quarter (not friends — a stratified sample: two teams that are shipping well, two teams that are stuck, one team you do not know well). Ask each: *"what's the friction you're carrying that is not yours to fix but is slowing every launch?"* Count the answers. The friction that shows up on three or more lists is the friction the next leverage move should target. If nothing shows up on three lists, you are not close enough to the teams' work; chapter 5 § *technical-culture leverage* returns to the sensing practice.
- **Test 2 — does the move land in the *class* the org has not funded before?** An org whose review pattern is strong and whose eval standard is weak should not fund another review-pattern refresh; it should fund the eval standard. An org whose north-star architecture is being aggressively revised every quarter should not fund another revision; that org is more likely to need a review-pattern refresh that consolidates the revisions into a runnable bar. Diversify across classes; do not run two moves in the same class simultaneously.
- **Test 3 — do you have a co-author?** Every leverage move needs a co-author. If you cannot name the two or three staff engineers (or the peer platform-side principal, or the hiring committee chair) who would co-sign the published version, the move will not land. The absence of co-authors is often a sign that the move is not the org's next step; it is *your* next step. Reconsider before committing.

A leverage move that passes all three tests gets a working title, a named co-author set, and a *published cadence* (drafted by month 3, reviewed by month 4, published by month 5, first landing report by month 11). Chapter 6 § *personal-cadence artifact* is where the working titles land on the quarterly review.

## What is *not* a leverage move

Naming the negatives sharpens the definition. Each of the following is often called a leverage move; none of them is one at the principal-IC altitude this module owns.

### An RFC you wrote for one team

The principal-authored RFC for one team's re-platform is a *contribution*, not a leverage move. It is the kind of contribution a staff engineer on that team should be authoring; the principal doing it is either *back-filling for absent staff capacity* (a staff-scope contribution, legitimate at low frequency but tracked as such) or *inadvertently displacing the staff engineer who should be growing into the authoring* (a coaching failure — chapter 1 § *sponsorship-as-service substitution* is the specific pattern).

The fix: pair with the staff engineer whose work this is. Co-author with them, credit them, and hand back the RFC after cycle one so the *next* cycle has them owning it end-to-end.

### A talk you gave at the internal all-hands

The talk that presents a leverage move is *dissemination*, not the move itself. Confusing the two is one of the more visible principal failure modes — a portfolio full of talks and no artifacts. Chapter 6 § *the "keynote-only" drift* is the parent failure mode; mod-506 (industry influence and external voice) is where the dissemination discipline lives, and it is explicit that dissemination without the underlying artifact is empty.

The fix: for every talk you give, the linked artifact should already exist. The talk points at the artifact; the artifact does the work.

### A senior engineer you mentored to promo

A specific senior engineer promoted to staff is a *coaching outcome* (mod-410 exercise-04 owns L30 coaching; this module's chapter 1 owns L40 coaching). It is a legitimate outcome. It is not a leverage move; it did not lift *every* team, and it depends on your personal involvement (mod-410 exercise-04 style 1:1s).

The fix: if the coaching cascade *does* lift every team — because the L40 mentee now runs the review pattern, or now chairs a loop, or now co-authors the next architectural revision — the coaching-plus-sponsorship arc is the leverage. The individual mentorship is the seed, not the move.

### A cross-team meeting you now attend regularly

Attending the cross-team weekly sync is *presence*, not leverage. The move that would lift every team is authoring the artifact the sync converges on — the coordination doc, the shared roadmap alignment page, the escalation template. Presence without authored artifact is chapter 5 § *sliding into first-line EM work* dressed up as leverage.

The fix: exit the sync as a standing attendee. Author the artifact the sync would have needed, hand it to the sync's chair, and check in quarterly on how the artifact is aging.

### A tool you built and open-sourced

The tool is a *contribution*; the leverage question is *whether every ML team in the org uses it*. Many principal-authored internal tools do not land because their scope is not the org's next friction, only the principal's. Class D (shared eval standard) is a leverage move because eval friction is universal; a niche debugging library the principal is fond of is not.

The fix: run test 1 (friction-count) before you build the tool. If fewer than three staff engineers name the tool's absence as friction they are carrying, the tool is a contribution — legitimate — but not the org's next leverage move.

## Failure modes

- **"One leverage move per week."** Named on paper as a leverage move but actually a rolling series of tactical asks: a new review checklist item on Monday, a new eval convention on Wednesday, a new interview-rubric tweak on Friday. Every individual ask makes sense; the aggregate is churn. Teams stop being able to plan against the moves because the moves themselves keep moving. Fix: commit to two moves per fiscal year, publish the working titles, and refuse the tactical asks that do not fit.
- **The leverage move authored alone.** A rubric, revision, standard, or interview change with no co-authors. Ratification is thin ("the principal published this"); adoption is thinner ("the principal is the only one who cites it"). Fix: return to the selection-discipline test 3; if no co-author exists yet, the move is not ready.
- **The leverage move measured only on activity.** *"We rolled out the eval standard to 12 teams this quarter"* — with no data on whether any team's launch decisions changed. Activity metrics for leverage moves are proxies at best; the real signal is *did the org's work get better on the axis the move targeted?* Fix: publish the *landing criteria* alongside the move (the *"how you know it landed"* items above), and track against them at 6 / 12 / 18 months.
- **The leverage move that never sunsets.** A rubric from three years ago that no team consults, a shared eval standard that has not been version-bumped in 18 months, an interview change whose original rationale nobody remembers. Leverage moves have to be *maintained* or they become friction. Fix: the quarterly review (chapter 6) includes a *leverage-move health check* — for every move on your portfolio, is it still lifting the org, or is it now background noise?
- **The leverage move confused with the strategy.** Class B (north-star architectural revision) is a leverage move; mod-502 § the *bet portfolio* is the strategy. Confusing the two — treating a bet as a leverage move, or treating a leverage move as a bet — pulls the principal into strategy work when their week's committed leverage was a review-pattern refresh. Fix: use the mod-502 bet portfolio as the strategy substrate; use this chapter's four classes as the leverage substrate. They cite each other; they are not the same artifact.
- **The leverage move that displaces staff scope.** A canonical review pattern (Class A) that specifies design-review depth belongs at the org level; a *single team's* design-review checklist belongs to that team's staff engineer or line EM. Principal-authored artifacts that reach into staff-scope territory create ambiguity about who owns the local rubric. Fix: mod-501 chapter 6 (hand-off contracts) is the reference; the principal-authored artifact sets the *bar*, the staff-scope owner sets the *checklist*.

## A worked micro-example

For grounding, here is what the *portfolio-summary paragraph* on a principal's leverage-move practice reads like at defensible altitude.

> **Leverage-move portfolio (FY26 baseline, v2).** Two moves in flight, two moves shipped and in landing-report cycle. In flight: (i) *Shared eval standard v1 for Gen-AI launches* — Class D, co-authored with the ML platform team and the Gen-AI-Product team's staff engineer, published draft 2026-08-15, ratification session 2026-10-02, first landing report scheduled 2027-05-15; (ii) *North-star architecture v3.4 — real-time feature contract deprecation of v1* — Class B, co-authored with the peer platform-side principal per mod-503 chapter 8, draft 2026-09-30, migration window 2026-10 through 2027-03. Shipped and landing: (iii) *Canonical launch-review rubric v2* — Class A, published 2026-01, cited in 14 of 17 launches YTD, one launch blocked and un-blocked without my involvement (RecSys team, 2026-05); (iv) *Staff-plus interview: systems-and-tradeoffs rubric addition* — Class C, published 2026-03, first flipped hire decision 2026-07, hiring committee ratified. Selection tests: (i) friction-count of 4/5 for eval-standard, 3/5 for real-time feature contract; (ii) diversify — both moves in classes not currently funded; (iii) co-authors named for both. Retirement candidates: the FY24 *canonical monitoring dashboard template* is no longer cited by any team; retiring in FY26-Q4 per chapter 6 discipline.

Notice what is *not* in the paragraph: individual coaching wins, individual RFC-authoring wins, talks. Those live elsewhere (chapter 1 for coaching; chapter 4 for review authorship; mod-506 for talks). What *is* in it: the four classes, the co-authors, the landing criteria, the retirement candidates. That is the standard the practice has to hit.

## Summary

- The Upstart target sentence — *"multiply the effectiveness of every ML team"* — is the composite framing. *Multiply* rules out additive contributions; *every ML team* rules out team-scope contributions. This module's Theme 4 lives inside those two constraints.
- A leverage move has three properties: once-authored / repeatedly-used, absent-you effective, org-scope reach. Contributions that miss any of the three are legitimate but are not principal-altitude leverage moves.
- Four classes cover the space: (A) canonical review pattern, (B) north-star architectural revision, (C) bar-raising interview change, (D) shared eval standard. Chapters 3 and 4 walk classes C and A in depth; chapter 6 walks the class-selection cadence.
- Selection discipline runs three tests: friction-count from a stratified sample of staff engineers, class-diversification against what the org has not funded before, named co-authors. Ceiling is three moves in flight; two is modal; four is *chasing every bet* (chapter 6 § failure mode).
- The negatives — an RFC for one team, a talk, a mentored senior IC, standing-meeting attendance, a niche tool — are legitimate contributions that are commonly mislabelled as leverage moves. The mislabeling is what pulls a principal's calendar off leverage and onto contribution.
- Six failure modes: one-per-week churn, authored-alone, measured-on-activity, never-sunsets, confused-with-strategy, displaces-staff-scope. Each has a specific fix.
- Chapter 3 walks the loop-level calibration practice that turns Class C moves into ratified changes.
