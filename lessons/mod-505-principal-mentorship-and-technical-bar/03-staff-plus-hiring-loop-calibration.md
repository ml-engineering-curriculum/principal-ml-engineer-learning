# Staff-Plus Hiring Loop Calibration

> Chapter 3 of mod-505. Prerequisite: chapter 2 § *Class C — the bar-raising interview change* and mod-501 chapter 5 § *Theme 4* (the *"staff-plus hiring committees"* half of the *coach* verb's object). Downstream: chapter 4 (review bar) uses the same rubric-and-authority machinery; chapter 5 (technical culture) uses hiring as one of the two most visible culture-signaling surfaces.

## The seam this chapter sits on

Two adjacent tracks share the hiring-loop scope, and they carry different responsibilities. Read this seam before doing anything else, or you will duplicate work owned by the level below.

- [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) **mod-410 exercise-03** owns the *staff-scope hiring loop*: individual-interview design, individual-interview execution, individual-interviewer calibration. A staff engineer who has done that exercise can *interview well* on a staff-plus loop and can *design an interview* for a specific rubric axis.
- This chapter, **mod-505 chapter 3**, owns the *loop-level* calibration one step above: sitting on the loop as its calibrator, deciding hire / no-hire *at the loop level*, distinguishing *staff vs. principal* on the level call, and coaching the loop chair on running rubric-based principal-track loops.

The seam is the difference between *how a good interview happens* (mod-410) and *how a good loop reaches the right decision* (this chapter). A principal who reaches into individual-interview design is doing staff-scope work at principal-scope opportunity cost; a staff engineer who reaches into loop-level calibration is stretching outside their scope. Both are common; both erode the seam.

The *coach the loop chair* framing is the load-bearing verb: this chapter is not primarily about *your* seat in the loop; it is about the loop chair's seat, and the principal's job on it is to grow loop chairs who reach the right calls without needing the principal in the room. The absent-you effectiveness test from chapter 2 applies here too.

## What "the loop" is at staff-plus altitude

A staff-plus loop — the loop that hires a Senior Staff, Staff, Principal, Sr. Principal, or Distinguished ML Engineer — has structural differences from a senior-and-below loop. Naming them fixes what the principal is calibrating.

- **Five to seven interviews.** Not four. A staff-plus loop typically runs a coding / systems interview, a design / architecture interview, a portfolio deep-dive on prior work, a cross-functional-influence interview, a technical-leadership behavioural, and — for the principal-and-above bands — a *technical bar* interview whose specific job is to differentiate *staff-plus* from *principal*.
- **Multi-signal calibration.** No single interview carries the level decision. The loop's job is to triangulate a level *across* the interviews. A candidate who nails the coding and struggles with the cross-functional-influence is a signal about *level*, not about *hire*. A candidate who nails cross-functional-influence and fumbles the architecture depth is a *different* signal, also about level. Chapter 3's calibration is about reading the triangulation, not summing the ratings.
- **The loop chair holds the decision protocol.** The chair runs the debrief, adjudicates disagreement, drafts the recommendation to the hiring committee, and — in most orgs — either casts or facilitates the final hire / no-hire call. The principal's *coach the loop chair* work is largely about how the chair runs that hour and how the chair drafts that recommendation.
- **The hiring committee is a distinct body.** Most orgs above 500 engineers have a hiring committee that ratifies (or overturns) the loop's recommendation. The principal often sits on this committee at the staff-plus level; the chapter's calibration work is the input the principal brings to that seat.
- **The rubric is *level-specific*, not *role-specific*.** A staff-plus rubric asks *"is this a staff, a senior staff, or a principal?"* — not *"is this a good ML engineer?"* A principal loop that runs a generic *"ML engineer"* rubric will over-hire senior engineers into principal seats and mis-level almost every close call. Chapter 2 § *Class C* is the leverage-move class that fixes this at the rubric level.

Amazon's *Bar Raiser* program is a widely-cited version of the loop-calibrator seat; other orgs have named it differently (Google's *cross-functional hire committee reviewer*, Meta's *cross-team loop reviewer*, or an unnamed *senior calibrator* seat in leaner orgs). The specifics vary; the seat exists — and the principal is one of the small number of engineers who occupies it.

## The four calibration decisions

At the loop level, the principal has four decisions to make. Every debrief the principal chairs (or attends) is some combination of these.

### Decision 1 — hire / no-hire

**The question.** Would the loop's evidence, taken together, cross the bar the org has committed to hiring at?

**The signal you read.** Not the average of the ratings. The *shape* of the ratings: which interviews cleared the bar cleanly, which cleared it with a caveat, which failed to clear it, which produced a *no-decision* signal (an interview that ran short, an interviewer who did not push hard enough, an artifact the interviewer did not read). A loop with three strong-hire, two no-hire, and one no-decision is *not* a hire; it is a *do-not-know*, and the correct call is either an add-on interview or a no-hire with an explicit *reconsider-in-N-months* addendum. Chapter 3's discipline is refusing to average shape into a single number.

**The trap.** *"They interviewed well"* — where *well* means the candidate was pleasant in the room. A candidate who is pleasant and does not clear the technical bar is a no-hire; a candidate who was tense and did clear the bar is a hire. The pleasantness signal is not zero (chapter 5 § *technical culture* is where it lands) but it is not the hire signal. Loop chairs new to the seat over-index on pleasantness.

**The escalation path.** If the loop cannot converge on hire / no-hire — repeatedly deadlocked, splits along team lines, or the loop chair is not able to hold the room — the escalation is *to the hiring committee* with a written summary that names the split and the specific evidence each side is reading. Not to the recruiting VP; not to the hiring manager. The technical decision is a technical decision.

### Decision 2 — level (staff / senior staff / principal / sr. principal / distinguished)

**The question.** If hire, at what level?

**The signal you read.** Mod-501 chapter 1 (verb-and-object vocabulary) is the reference. The candidate's portfolio and the loop's evidence together should say: *at what altitude does this candidate's verb reliably land on the principal-scope objects?* A candidate whose *own* verb consistently lands on portfolio-scope objects (multi-team blueprint, portfolio TCO, exec-audience RFC) is staff-level; a candidate whose *own* verb consistently lands on org-and-industry-scope objects (org-wide North Star, north-star architecture, cross-org influence up to SVP / CTO, org-wide bar-raising leverage moves) is principal-level. The verb-object table is the calibration rubric; you should be able to point at specific interview evidence for each object.

**The trap.** *"Years of experience"* as a level proxy. Years correlate with level but do not cause it. A candidate with 15 years of staff-scope work is a staff hire, not a principal hire, at 15 years. The scope of *what they own* is the signal; the years are a downstream summary.

**The trap, again.** *"They'd stretch into principal"* — where the loop is being asked to hire below the level the requisition is written for and *hope* the candidate grows into it. This is a common failure mode when the loop is under recruiting pressure. The correct call is: hire at the level the evidence supports; open a separate promo path for the candidate once they are in seat. Hiring above the evidence produces the *senior in a principal seat* problem the leverage-move practice (chapter 2) then has to compensate for.

**The staff-vs-principal call, specifically.** This is the call the principal loop calibrator is most often being asked to make; it is also the hardest. The signal that most cleanly differentiates: does the candidate's portfolio contain an *org-and-industry-scope* artifact (a North Star document that survived a fiscal year, a north-star architecture that was consumed by peer platform teams, a cross-org bet that ratified above VP), or does it contain the *portfolio-scope* equivalent (a multi-team blueprint, an exec-audience RFC that leadership committed to, a portfolio TCO)? The former is principal; the latter is staff. Candidates who describe org-scope work in language that turns out, on probing, to be portfolio-scope work are the *senior-in-a-principal-seat* risk — mod-501 chapter 2 (reading a principal posting) has the same probing discipline in reverse.

### Decision 3 — the specific-role fit vs. bar-clear distinction

**The question.** The candidate cleared the bar; does the *specific role* on offer match what the candidate does well?

**The signal you read.** A candidate can clear the org's staff-plus bar and be wrong for the *specific* seat — a candidate whose portfolio is entirely RecSys architecture is a bar-clear-hire but the wrong hire for a Gen-AI-platform Principal seat. Chapter 3's discipline is to make this distinction explicit rather than collapsing role fit into bar clearance.

**The convention.** *Bar-clear* is a permanent status; *role fit* is a per-req question. A candidate who is bar-clear but wrong for the current req should be recommended for other reqs the org is running or expects to run, with the specific fit gap named. This is what turns hiring into an org-wide leverage move rather than a per-req grind.

**The trap.** *"They can learn the domain"* — where a bar-clear candidate is hired into a role whose domain they have never worked in and expected to ramp in the first six months. Sometimes this works; often it does not, and the mis-fit costs the org 12–18 months. The correct call is to name the fit gap explicitly and let the hiring manager decide with eyes open, not to smooth it over.

### Decision 4 — the loop-quality decision

**The question.** Did the *loop itself* produce the evidence a good decision needs?

**The signal you read.** Were all interviews conducted well — did each interviewer push at the depth their interview was designed to test? Did the interviews cover the rubric axes without gaps? Was the portfolio deep-dive substantive (interviewer had read the artifacts in advance, asked probing questions) or performative? Did the cross-functional-influence interview probe the *coaching* and *cross-org* verbs mod-501 chapter 1 named as principal-defining?

**The action.** If the loop produced weak evidence — a shallow deep-dive, a rushed design interview, an interviewer who did not push — the *right* action is usually to add an interview or re-run one, not to make the hire / no-hire call on incomplete evidence. This is where the loop chair's confidence is tested; the principal's coaching is often to steady the chair's willingness to say *the loop is not done yet*.

**The follow-up.** Loop-quality issues are inputs to the *coach the loop chair* practice and often surface Class C leverage-move candidates (chapter 2). A pattern of shallow portfolio deep-dives across three loops in a quarter is a signal that the portfolio-deep-dive rubric or the interviewer training on it needs work. That is a leverage-move-class-C prompt.

## Coaching the loop chair

The principal's most durable contribution to a hiring loop is not the calibration call on any single loop; it is the growth of the loop chairs who run the loops. The chair-coaching arc has four beats.

- **Beat 1 — pre-loop 1:1.** Before the loop runs, sit with the chair for 30 minutes. Walk the rubric together against the candidate's on-paper profile. Ask the chair to name what the loop is trying to *test* — which axes are load-bearing for this specific req, which are check-the-box. Ask the chair how they will handle the specific splits that seem most likely (a strong-coding / weak-design split, a strong-influence / weak-depth split, a strong-in-domain / weak-cross-domain split). If the chair cannot answer, coach them through it *before* the interviews start.
- **Beat 2 — you sit on the debrief; the chair runs it.** The principal's job is to be silent for the first 30 minutes. The chair runs the debrief; the interviewers vote; disagreements surface. The principal's job is to notice: does the chair let the loud voices dominate? Do they surface the quiet interviewer's read? Do they steer the debrief onto the rubric or onto the vibes? Do they force the level call as sharply as the hire call? Take notes silently.
- **Beat 3 — you speak, and only after the chair has held their own line.** If the loop reaches a defensible call without your intervention, do not intervene. Speak only if the loop is about to make an indefensible call or if the loop is deadlocked and the chair has clearly asked. This is the *absent-you effectiveness* test from chapter 2 applied to hiring: the chair should be able to reach the same call whether the principal is in the room or not.
- **Beat 4 — post-loop 1:1 with the chair.** Twenty to thirty minutes, within two working days. What went well in the debrief. What the chair would do differently. Which of the four calibration decisions (above) was hardest for them and why. Whether any pattern from this loop is Class C leverage-move-shaped. The post-loop conversation is where the chair grows; the debrief itself is where the loop's decision gets made.

Over enough cycles (roughly 4–6 loops), a chair grows from *the-principal-sits-on-my-loops* to *I-chair-loops-the-principal-does-not-need-to-attend*. That transition is the successful outcome. The principal's calendar frees up for the loops that most need the calibration; the org gets more well-run loops per unit principal time. This is the leverage.

## The rubric-based principal-track interview

The single interview whose design is most often the *coach the loop chair* topic is the *technical bar / principal-vs-staff differentiation* interview. Chapter 2 § *Class C* is the leverage-move class; this section is the anatomy of a defensible instance.

Common shapes:

- **The portfolio deep-dive at principal altitude.** 60–75 minutes on one artifact the candidate produced (an RFC, a strategy document, a reference architecture, a paired one-pager / deep-dive from mod-502 chapter 7). The rubric probes: *at what altitude did the candidate's verb land?* Mod-501 chapter 1's verb-object table is the rubric substrate. Interviewer reads the artifact end-to-end before the interview; opens by asking the candidate to walk it; probes deeper on the parts the artifact skims over; drills into the coaching / cross-org / bar-raising verbs.
- **The org-scope architecture-and-tradeoffs interview.** 45–60 minutes on a prompt sized at north-star altitude (mod-503) — *"design the reference architecture the ML org converges on for the next 3–5 years given <constraint>"*. Rubric probes: does the candidate reason at portfolio-and-industry altitude (mod-503 chapter 2), or at multi-team-blueprint altitude (staff scope, `staff-ml-engineer-learning` mod-402)? The altitude is the differentiator.
- **The cross-org-influence behavioural.** 45 minutes on 2–3 specific stories from the candidate's history where they had to ratify a technical direction with peers outside their line authority. Rubric probes: could the candidate name the artifact they used, the coalition they built, the escalation they navigated (mod-504 chapters 4 and 6 are the reference)? The presence of the *artifact-and-mechanism* answer, vs. a *charisma-narrative* answer, is the differentiator.

The rubric matters more than the exact set of interviews. A loop that runs three rubric-based principal-differentiation interviews with clear axes will produce more defensible level calls than a loop that runs five vaguely-shaped interviews without them.

## The five failure modes

- **Sitting on every loop.** Principals with hiring-committee seats sometimes attend every staff-plus loop in the ML org. This is the *become the chair, do not grow chairs* failure. Fix: define the criteria for which loops the principal attends (the highest-band loop each quarter; the first loop for a newly-appointed chair; any loop where the chair explicitly asks for principal presence) and refuse the rest.
- **Averaging ratings into a single number.** The loop debrief that becomes *"three strong-hires and two no-hires averages to hire"* is the *shape-erasure* failure. Fix: chair reads out the shape (which interviews cleared, which did not, and why) before any hire / no-hire discussion.
- **Confusing bar-clear with role-fit.** The bar-clear candidate hired into the wrong specific seat produces mid-tenure mis-fit that costs the org an EM's replanning cycle. Fix: make the *bar-clear / role-fit* distinction explicit in the debrief and in the written recommendation.
- **Deferring the level call.** *"Let's hire and let promo sort out the level in year one"* is the *defer-to-promo* failure. The candidate's comp band and the org's expectations are set at hire; adjusting them post-hire is much harder than getting the level right at hire time. Fix: force the level call in the debrief; if the loop cannot converge, escalate to the hiring committee with a written split, not a fudged level.
- **Coaching the chair to *your* debrief, not to *a good* debrief.** The chair adopts the principal's debrief style even where the chair's own style would land better with their specific interviewer set. This is the *become-me* failure. Fix: coach on the *decision quality* the chair reaches, not on the *procedural mimicry* of your style.

## Interaction with peer branches

- **The hiring manager.** The hiring manager (an EM) owns the req, the role definition, the offer. The principal on the loop is the *calibrator* of the technical bar and the level call; the hiring manager makes the final hire call, informed by the loop's recommendation. Do not usurp the hiring-manager seat; do not let the hiring-manager seat usurp the calibration seat. The two are peers.
- **Recruiting.** Recruiting owns pipeline, scheduling, comp negotiation. The principal on the loop is not the *sourcer* — a principal doing recruiting work is a staff-scope contribution at a much steeper opportunity cost than an actual sourcer. If recruiting is thin, the org has a different problem than the loop calibration.
- **The `ai-infra-team-lead-learning` peer track.** The first-line EM is often the hiring manager for staff hires; the principal is the calibrator. The two roles are described in *different* tracks precisely because the two contributions are distinct and must not be conflated. Chapter 5 § *boundary with the peer EM track* is the parent reference.
- **The staff engineer running the loop.** If a staff engineer is chairing the loop (common for the staff-hire loops), the principal's *coach the loop chair* practice is delegated to *coaching the staff engineer's chairing*. This is the L40 coaching (chapter 1) instantiated on the specific hiring artifact. Use it as a growth surface.

## A worked micro-example

For grounding, here is what a *loop-participation summary* on a principal's hiring calibration practice reads like at defensible altitude.

> **Hiring-loop calibration (FY26-YTD).** Sat on 6 staff-plus loops YTD. Chair-coached 4 loop chairs; two of the four now chair without my presence on lower-band loops. Called on the staff-vs-principal question in 3 loops: hired one at staff (bar-clear, evidence at portfolio scope), hired one at principal (evidence at org-and-industry scope, referenced their public RecSys architecture write-up cited by two peer orgs), escalated one to the hiring committee for a formal deferred re-interview (loop evidence conflicted; deep-dive was thin; asked for an add-on portfolio review, candidate declined). Flagged one Class C leverage-move candidate to the hiring committee: the portfolio-deep-dive rubric is currently drifting on the *coaching* verb (mod-501 chapter 1) — three of six deep-dives did not probe the *coach staff engineers* object. Drafting rubric update with hiring committee chair for FY26-Q4 ratification. Next loops booked: 2 in Q4 for Distinguished-band candidates; will attend both.

Notice the shape: number of loops, number of chairs coached, specific calls on the level question with the evidence that drove each, a Class C leverage-move flag, and the next commitments. Not "I interviewed strong candidates this quarter."

## Summary

- The seam: mod-410 exercise-03 (staff track) owns individual-interview design and interviewer calibration; this chapter owns the loop level above — sitting on the loop, deciding hire / no-hire and staff-vs-principal, and coaching the loop chair.
- The staff-plus loop is structurally different from a senior loop: 5–7 interviews, multi-signal calibration, a chair who holds the decision protocol, a hiring committee that ratifies, and a *level-specific* rubric.
- Four calibration decisions per loop: (1) hire / no-hire from the *shape* of ratings, (2) level from the object of the candidate's verb, (3) bar-clear vs. role-fit distinction, (4) loop-quality — did the loop produce evidence a good decision can rest on?
- The staff-vs-principal call is the hardest; the cleanest signal is whether the candidate's portfolio contains org-and-industry-scope artifacts (principal) or portfolio-scope artifacts (staff). *Years of experience* and *would stretch into principal* are common but weak proxies.
- The *coach the loop chair* practice runs across four beats: pre-loop rubric walk, silent debrief attendance, targeted intervention only when needed, post-loop chair 1:1. The success signal is chairs who reach defensible calls with the principal absent.
- The rubric-based principal-track interview kinds — portfolio deep-dive, org-scope architecture-and-tradeoffs, cross-org-influence behavioural — differentiate principal from staff. Mod-501 chapter 1's verb-object table is the rubric substrate.
- Five failure modes: attending every loop, averaging ratings, confusing bar-clear with role-fit, deferring the level call, coaching chairs into your style rather than a good debrief.
- Chapter 4 lifts the same rubric-and-authority machinery from hiring loops to design / RFC / launch reviews — the review bar the ML org calibrates against.
