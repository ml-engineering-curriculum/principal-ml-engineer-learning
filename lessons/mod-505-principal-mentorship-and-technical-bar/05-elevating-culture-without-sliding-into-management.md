# Elevating Technical Culture Without Sliding Into People-Management Scope

> Chapter 5 of mod-505. Prerequisite: chapters 1 (staff-engineer coaching), 2 (leverage moves), 3 (hiring calibration), 4 (review bar), and mod-501 chapter 4 (three role families boundary). Downstream: chapter 6 (sustained principal signal) uses the *management-drift* failure mode this chapter names as one of its four drift patterns.

## Why this chapter exists

Two posting sentences carry the load for this module's culture-side scope and are worth reading together.

- **Bumble (Principal ML Engineer, Matching and Recommendations):** *"Operate as a senior individual contributor, influencing technical strategy and decision-making without direct authority."* — the boundary sentence. *IC-principal, without direct authority.*
- **Ibotta (Principal ML Engineer):** *"Act as a leading contributor, voice, and thought leader in a growing community of machine learning practitioners."* — the community sentence. *Internal community of ML practitioners*, not external evangelism (that is mod-506).

Between the two sentences sits a specific principal contribution that is easy to name and hard to actually make: **the principal owns the technical-culture leverage of the ML org — the practices, the rituals, the shared standards, the internal-community shape — without ever staffing the seat that would give them direct authority to enforce it.** The chapter is about how to make that contribution and how to *not* slide into the peer-EM scope that would give the same contribution a different (and inappropriate for this track) shape.

The two adjacent seats have to be named clearly, because the modal principal-culture failure is one of them:

- **The peer engineering-manager seat.** Owned by [`ai-infra-team-lead-learning`](https://github.com/ai-infra-curriculum/ai-infra-team-lead-learning) at the first-line rung. Direct reports, 1:1s, performance reviews, comp, headcount, hiring plan, promo decisions.
- **The IC-principal seat.** Owned by this track. No direct reports. Technical direction, north-star architecture, cross-org influence, technical bar, technical-community leadership.

Both seats *influence culture*. The peer-EM shapes culture through the specific engineers on their team; the IC-principal shapes culture through the artifacts, standards, and community rituals every team's engineers pattern-match to. The two contributions compose; they do not substitute for each other.

## What "technical-culture leverage" actually is

Culture is not the principal's speeches at the all-hands. Culture is *what the bar rewards*, *what the review pattern normalises*, and *how the community of practitioners in the org compares work against each other*. Four of the eight surfaces where principal-scope culture-shaping actually happens are already owned by earlier chapters and by earlier modules; this chapter names the remaining four.

- **The bar itself.** What the review pattern rewards (chapter 4). What the hiring loop rewards (chapter 3). What the shared eval standard rewards (chapter 2 § Class D). Every rubric change is a culture change; the culture-writing is done by chapters 2–4.
- **The visible artifact.** The North Star (mod-502), the north-star architecture (mod-503), the paired one-pagers, the FAQ triplet (mod-504 chapter 5). What the principal *writes* signals what the org *reads*. Culture-writing through writing.
- **The visible review.** The north-star review body sessions (mod-503 chapter 7), the escalation dispositions (chapter 4 § *escalation response*), the way the principal handles disagreement in the room. Culture-writing through demonstration.
- **The visible community.** The internal ML practitioner community that Ibotta names — the guild, the reading group, the internal architecture-review study group, the shared engineering-blog voice. Culture-writing through the community's rituals.

The first three of the four are covered by chapters 2–4 and by mods 502–504. This chapter walks the fourth in depth: the internal ML practitioner community and the specific rituals that lift it, and — the load-bearing boundary — how to do so without sliding into peer-EM scope.

## The internal ML practitioner community — the four canonical rituals

The four rituals are common; not every org runs all four. Pick the one or two that fit the org's stage and run them well rather than running all four at half-depth. The four:

### Ritual A — the ML architecture-review study group

**What it is.** A monthly (or bi-weekly) session where the ML org's staff-plus engineers walk through *one* live artifact — a north-star revision draft, a portfolio-scope RFC, a public engineering-blog reference architecture from a peer org (see mod-503 resources.md for the case-study literature) — and *practise* the review rigor. Not a decision-making body; a *skill-building* body.

**Why it lifts the culture.** Skill in review is unevenly distributed across an ML org; a study group makes the good reviews *legible* so reviewers can learn from each other. Over 4–6 months, the *shape* of reviews in the org's actual decision-making bodies (chapter 4) improves without a top-down enforcement action.

**The principal's role.** Convene it; chair the first 2–3 sessions to establish the shape; hand the chairing to a rotating set of staff engineers (chapter 3 § *coach the loop chair* is the same coaching arc, applied to review skill rather than hiring skill). Attend regularly; do not chair it forever. The absent-you effectiveness test from chapter 2 applies.

**What to avoid.** Turning it into a decision-making body. Once the study group is deciding, it is either duplicating the real review body (chapter 4) or overriding it. Keep the *study* label load-bearing.

### Ritual B — the internal ML engineering-blog cadence

**What it is.** An internal blog — often on the corporate intranet, the internal-tooling docs site, or a private Confluence — where the ML org's engineers publish worked write-ups: how the RecSys team debugged an offline / online skew, how the Gen-AI team's eval harness caught a regression, how the platform team's serving-gateway version-bump landed. Weekly or bi-weekly cadence; 800–2000 words per post; standard shape.

**Why it lifts the culture.** Writing forces the author to make their reasoning legible; reading forces the audience to pattern-match against reasoning they did not do themselves. Over 6–12 months, the *shared vocabulary* of the ML org converges — teams start using the same terms for the same phenomena, and cross-team debugging gets faster.

**The principal's role.** Publish 4–6 posts per year at the *shape* the org's engineers should aspire to (not the *depth* of a keynote — that is mod-506). Curate the calendar for the first cycle; hand the curation to a rotating editor after two cycles. Read every post; leave one substantive comment on each — that comment is often what turns a good post into a great one for the author's growth.

**What to avoid.** Making it the principal's soapbox. Four principal posts in a quarter is a signal that the principal is monopolising the surface; the practice inverts. Fix: cap your own posting cadence at 4–6 posts per year and prompt other engineers.

### Ritual C — the reading / research-scan discussion

**What it is.** A monthly session where the group reads one paper (or one engineering-blog post, one industry report) that is relevant to the ML org's current bets, and discusses it. Not a paper-reading club in the research-track sense — an *applied-relevance* reading, oriented on *what this changes for the bets we are currently running*.

**Why it lifts the culture.** Every ML org has to stay current, and the modal alternative — every engineer reads what they happen to read — creates radically uneven internal knowledge. A shared reading makes the org's current-tech-context *singular* and gives cross-team conversations a common substrate. Ibotta's *"thought leader in a growing community"* framing lands directly here.

**The principal's role.** Select the reading for the first cycle to model the *applied-relevance* selection criterion (a Chip Huyen chapter, a Rules-of-ML rule, an Uber Michelangelo evolution post, a NIST AI RMF section — see mod-503 resources.md); hand the selection to a rotating slate. Facilitate the first 2–3 sessions; step back.

**What to avoid.** Confusing this ritual with the research-track *paper-reading club*. If the discussions are about *is this SOTA?* the ritual has drifted into research-track territory (owned by Family 3 in mod-501 chapter 4). Applied-relevance is the discriminator.

### Ritual D — the internal cross-team ML-community rotation

**What it is.** A structured way for engineers on one ML team to spend 4–8 weeks *embedded* on an adjacent ML team — the RecSys engineer sits with the Gen-AI team for a sprint; the fine-tuning engineer sits with the platform team for a rotation. Not a full transfer; a structured secondment.

**Why it lifts the culture.** Cross-team fluency is one of the surfaces the principal cannot manufacture on their own; the rotations produce it as a side-effect. Six months of well-run rotations produces engineers who *pattern-match across teams* — which is precisely the substrate the leverage moves (chapter 2) need to land against.

**The principal's role.** Author the rotation framework — the goals, the shape, the how-to-be-a-good-host and how-to-be-a-good-guest checklists, the debrief protocol. Chair the first 2–3 rotations' debriefs. Hand the framework to a rotating owner. The peer EMs (`ai-infra-team-lead-learning`) are the *staffing decision-makers* — they decide who rotates and when — but the principal owns the *shape* of the rotation and the ritual around it.

**What to avoid.** Rotating engineers *at* the principal's discretion. The principal does not have direct authority; the framework the principal authors sets the shape, but the peer EMs staff. Reaching into staffing is the *sliding-into-EM-scope* pattern named later in the chapter.

## Co-authorship as the technical-culture practice

The single most repeatable culture-lift the IC-principal can produce is *co-authorship*. Every artifact this module and the sibling modules produce — north-star architecture, paired one-pagers, review pattern, eval standard, hiring rubric change — has a co-author or a co-signer named on the byline. That authorship convention is itself culture. Three properties.

- **The co-author is a peer or a mentee at L40, not a delegate.** Co-authorship with a staff engineer who was actually *the author of the underlying analysis* legitimises the artifact in a way the principal-authored version cannot. If the co-authored artifact reads as *"the principal wrote this and put a co-author's name on it,"* the practice has failed.
- **The co-author gets the credit publicly.** In the review body, in the meeting note, at the internal all-hands. Not the principal's line manager giving the credit; the principal giving the credit in the room. The transfer of credit is what makes the co-authorship *real*.
- **The co-authoring is repeated across cycles, not one-off.** A different co-author on each artifact over 4–6 cycles produces a durable culture of *the principal writes with the staff engineers*. The one-time gesture does not.

Bumble's *without direct authority* clause is what makes co-authorship the practice. The principal cannot compel a staff engineer to co-author; the principal *invites* — and the invitation lands only because the coaching, the review bar, and the visible artifact craft have been legitimate. Co-authorship is the accumulation of the practice; it is not a shortcut.

## The boundary with the peer EM track — six specific lines

The peer-EM branch — [`ai-infra-team-lead-learning`](https://github.com/ai-infra-curriculum/ai-infra-team-lead-learning) at the first-line rung and the second-line / director tracks above — owns the scope that shares half the culture surface with the principal. The boundary between the two must be drawn precisely, or the principal drifts into shadow-EM work and the peer EMs push back (correctly). Six specific lines, each of which is a common sliding surface.

### Line 1 — the principal does not run 1:1s with someone else's report

A staff engineer's directs — the L20 and L30 engineers on that staff engineer's team — are not the principal's mentees. The staff engineer's own line-EM is the direct-report EM; the staff engineer is the technical lead. The principal running 1:1s with a staff engineer's directs *without* the staff engineer or the EM present is sliding into shadow-EM work.

**The clean pattern.** The principal's 1:1 cadence is with L40 mentees (chapter 1). If an L30 engineer needs coaching, the principal coaches the L40 mentee on *how* to coach them (mod-410 exercise-04 is the L40 mentee's practice; the principal's role is coach-the-coach).

### Line 2 — the principal does not sit in on performance-review calibration

Performance-review calibration is a peer-EM ritual: EMs of one org meet to normalise their reports' calibration against a common bar. The principal — with no direct reports — is not a peer in the room. The principal's presence in the room, even as an "advisor," distorts the ritual: EMs use the principal's read as a proxy for the direct-line performance signal that only they have.

**The clean pattern.** The principal contributes to the technical bar the calibration is *against* (chapter 3 § *rubric-based principal-track interview* is one such contribution; chapter 4 § *review bar* is another) but does not sit in the calibration meeting. If asked, decline and explain the boundary.

### Line 3 — the principal does not adjudicate compensation

Compensation calls — hire comp, promo comp, off-cycle comp — sit inside the org's HR framework and are owned by the reporting line and the People / HR partner. The principal is asked their opinion sometimes, especially on staff-plus hires (chapter 3); the principal's opinion is *"was this a staff hire, or a principal hire?"* — not *"should this candidate be offered X or Y?"*. The dollar figure is not the principal's call.

**The clean pattern.** The principal's calibration on level and technical bar is inputs to comp; the comp math is HR + hiring manager. Do not blur the two.

### Line 4 — the principal does not staff their peer EMs' teams

The composition of an EM's team — who is on it, who leaves, who transfers in — is the EM's decision (subject to the EM's own management chain). A principal who reaches into staffing *because they have opinions about which engineers should be where* is doing shadow-EM work and creating unhealthy dependency dynamics between engineers and the principal.

**The clean pattern.** The principal shapes *the technical direction* the teams work against (mod-502, mod-503) and *the standards* they work to (chapters 2–4 of this module); the staffing decisions are made by the EMs against those directions and standards. If a specific staffing move is a critical unblock for a bet, the principal escalates the *unblock*, not the *staffing move*.

### Line 5 — the principal does not mediate people conflicts

A conflict between two engineers, or between an engineer and their EM, is a people-management issue owned by the reporting-line and the People / HR partner. A principal who mediates the conflict directly is doing peer-EM work; a principal who tries to *technically arbitrate* the conflict (deciding that engineer A is right because their code is better) is doing *both* peer-EM work and misusing the technical bar as a HR proxy.

**The clean pattern.** If a technical *disagreement* is fuelling a people-work conflict, the principal can arbitrate the technical disagreement (chapter 4 § *escalation path* is the mechanism, if trigger 4 fires). The technical arbitration is often what defuses the people-work conflict; the principal does not touch the people-work half.

### Line 6 — the principal does not carry the promo case

Writing an engineer's promo case is a specific work product — the packet, the peer-feedback synthesis, the multi-quarter growth narrative — owned by the EM (with input from peer engineers). A principal writing a mentee's promo case is doing EM work at principal-scope opportunity cost, and is often symptomatic of the mentee's EM not writing the case well (which is a peer-EM growth issue for a different EM to coach into their EM).

**The clean pattern.** The principal writes *sponsorship letters* (short, factual, name a specific accomplishment or two, name the endorsement) that the mentee's EM includes in the promo packet. The packet is the EM's; the sponsorship is the principal's. Two artifacts, two owners.

## The two rituals whose ownership can be ambiguous, and how to resolve them

Two rituals repeatedly show up on the boundary and cause ownership questions. Resolve them explicitly.

- **The staff-plus tech-lead onboarding.** When a new staff engineer joins the ML org, who owns their onboarding — the peer EM (who hired them), or the principal (as the org's staff-plus technical coach)? **Answer: peer EM owns the *job* onboarding; the principal owns the *technical-culture* onboarding.** Concretely: the peer EM covers the team's rituals, the org's operational rhythms, the direct-report cadence. The principal (in a scheduled 30–45 minute session in week 2 or 3) walks the new staff engineer through the North Star, the north-star architecture, the review pattern, the leverage-move portfolio, and their expected place in the community rituals. Two owners, two conversations.
- **The internal ML-community charter itself.** Who owns the charter for the internal community — the shape of the guild, the rituals, the how-to-be-a-good-community-member norms? **Answer: co-authored by the principal and the *senior peer EM* (usually the ML org's Director or VP of Engineering).** The principal writes the technical-community half (the reading discipline, the review rigor, the co-authorship convention); the senior peer EM writes the people-community half (the psychological-safety norms, the promotion pathway from the community back to the teams, the resourcing model). One charter, two authors, two signatures.

Ambiguity resolved in advance is easier than ambiguity litigated in the moment. If a third ritual surfaces in your org whose ownership is unclear, negotiate it *before* running it — with the senior peer EM directly.

## The four community-side failure modes

- **The principal-as-community-lead identity.** The principal starts to identify as *the leader of the ML community* rather than *one of its senior contributors*. Symptoms: the principal opens every community session; the principal's voice is the loudest voice in every reading; other engineers stop volunteering as chairs or curators. This is the *become-the-EM-in-a-different-hat* failure. Fix: hand chair / curator / facilitator roles to rotating staff engineers within 2–3 cycles; measure your own speaking time in community sessions and cap it.
- **Community rituals substituting for the technical bar.** The org has a strong reading group and a lively internal blog but the review pattern is weak. This is the *culture-without-bar* failure — the community becomes a place where quality *is discussed* but is not *held*. Fix: the community rituals lift the bar; they do not substitute for it. If the review body (chapter 4) is not being run, no reading discussion recovers that.
- **The community rituals as recruiting theatre.** The rituals are optimised for what candidates see when they interview — the reading list gets flashy but is not applied-relevance-selected, the internal blog features leadership posts more than practitioner posts. Fix: audit the ritual against its stated purpose annually; if the audit reveals recruiting-optimisation drift, name it and re-anchor.
- **The community rituals expanding without sunset discipline.** New rituals get started; old rituals never end; the engineers' calendars fill with community-scope obligations. Fix: apply chapter 2 § *retirement candidates* discipline to community rituals as well as to leverage moves. Every ritual has a retirement criterion; a ritual that no longer serves the culture is retired, not preserved for its own sake.

## Interaction with mod-506 (industry influence and external voice)

Mod-506 owns the *external* voice — publications, keynotes, open-source at principal altitude, conference talks. This chapter owns the *internal* community. The two are related but distinct.

- **The internal ML engineering-blog (Ritual B) is not the same as the corporate engineering blog.** The internal blog is a practitioner-to-practitioner surface; the corporate blog (Meta Engineering, Uber Engineering, Airbnb Engineering per mod-503 resources.md) is an external-audience surface owned by mod-506. Cross-posting from one to the other is not automatic; it is a per-post editorial decision.
- **A post that lands well internally may not be an external post.** A worked case study of the RecSys team's offline / online skew debug is deeply valuable to the internal community and may be too specific or too proprietary to publish externally. Do not force every internal artifact to become external content; the two audiences want different things.
- **Community leadership is not external evangelism.** Ibotta's framing — *"leading contributor, voice, and thought leader in a growing community of ML practitioners"* — is explicit that the *community* is the ML function's own practitioners. External thought leadership is a different scope. The principal who spends 60% of their community time on external evangelism has drifted into mod-506's scope and out of chapter 5's.

## A worked micro-example

For grounding, here is what the *culture-side summary paragraph* on a principal's practice reads like at defensible altitude.

> **Technical-culture practice (FY26-YTD, v1.2).** Community rituals in flight: ML architecture-review study group (Ritual A, launched FY25-Q3, currently chaired by a rotating slate of 4 staff engineers — I have not chaired since Q1); internal ML engineering-blog (Ritual B, curated by two rotating staff editors, my own posting cadence 3 posts YTD against a 4–6/year budget); cross-team rotation framework (Ritual D, v1 published FY26-Q1, 4 rotations completed, framework owner handed to peer platform-side principal). Reading discussion (Ritual C) not run — piloted in Q2, low attendance, retired per chapter 5 § *sunset discipline*. Co-authorship: 3 artifacts published this year, each with 1–2 co-authored staff engineers named on the byline (v3.4 architecture revision, launch-review rubric v2, systems-and-tradeoffs interview rubric update). Boundary with peer EM branch: 1:1s with peer EMs (`ai-infra-team-lead-learning` seat holders) at monthly cadence to keep the technical-direction / staffing / promo boundary clean; no shadow-EM work identified in Q3 audit. Retirement candidate: the *"principal office hours"* Ritual (from FY25) has drifted into de-facto 1:1 slots with directs; sunsetting Q4 per chapter 5 § *community-side failure modes*.

Notice the shape: named rituals, ownership handed to rotating chairs, co-authorship named, boundary-audit line, retirement discipline. Not "improved culture this quarter."

## Summary

- Bumble names the boundary — *IC-principal, without direct authority*. Ibotta names the community — *leading contributor and voice in the ML practitioner community*. The chapter is about lifting technical culture inside those two constraints without drifting into peer-EM scope.
- Technical culture is what the bar rewards. The first three culture surfaces — the review pattern, the visible artifact, the visible review — are covered by chapters 2–4 and by mods 502–504. This chapter walks the fourth: the internal ML practitioner community.
- Four canonical community rituals: (A) ML architecture-review study group, (B) internal ML engineering-blog, (C) applied-relevance reading discussion, (D) cross-team ML-community rotation. Run one or two well; do not run all four half-heartedly.
- Co-authorship is the load-bearing technical-culture practice: every artifact carries a co-author who was actually the author, credit is transferred publicly, the pattern is repeated cycle over cycle. Bumble's *without direct authority* clause is what makes the co-authorship legitimate rather than transactional.
- Six specific boundary lines with the peer-EM branch: no 1:1s with someone else's report, no performance-review calibration attendance, no compensation adjudication, no staffing peer teams, no people-conflict mediation, no writing the promo case. Sponsorship letters — one-page and factual — are the principal-side artifact that supports promo without owning it.
- Two rituals whose ownership was previously ambiguous — staff-plus onboarding and the internal ML-community charter — are resolved: peer-EM owns *job onboarding* and *people-community norms*; principal owns *technical-culture onboarding* and *technical-community norms*; the community charter is co-authored.
- Four community-side failure modes: principal-as-community-lead identity, community substituting for the bar, community as recruiting theatre, ritual expansion without sunset. Each has a specific fix.
- Chapter 6 walks the four drift modes at the principal-signal altitude — including the *management-drift* pattern this chapter's boundary lines are meant to prevent.
