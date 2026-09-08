# Internal-Community Thought Leadership — The Substrate External Voice Rests On

> Chapter 2 of mod-506. Prerequisite: chapter 1 (venue-audience-artifact discipline). Downstream: chapters 3–5 each depend on the internal-first ratio and the canonical-reference-doc discipline this chapter fixes. Interacts closely with mod-505 chapter 5 § *community rituals* — this chapter picks up where that section leaves off and lifts the community-ritual craft from *within-team* to *within-org* altitude.

## Why internal precedes external

Ibotta's role definition is explicit: *"act as a leading contributor, voice, and thought leader in a growing community of machine learning practitioners"*. The clause does not say *external* community. The most defensible reading is *the internal community first*, with the external community as a follow-on the internal signal supports — and this chapter argues that reading is not a comfort framing but a load-bearing one.

Two independent reasons make the ordering non-negotiable at principal altitude.

**Reason 1 — the external artifact's credibility comes from internal-first evidence.** A keynote whose lessons trace to a live production system the principal's own org runs is a keynote the audience treats as evidence. A keynote whose lessons trace to a system the principal *heard about at another org* is a keynote the audience (correctly) discounts. The internal-first ordering is what makes the principal a *witness* rather than a *reporter* — and the witness's talk is what carries the industry-influence effect chapter 6 tracks.

**Reason 2 — the external voice's opportunity cost is the internal voice.** The principal has, roughly, one paired-artifact cycle per quarter that can absorb external-influence work (chapter 6 § *the calendar-shape check* is where this budget lands). Every hour spent on an external talk is an hour not spent on the internal tech-radar entry, the internal reference document, or the internal design-review write-up. If the internal artifacts are underweight, the principal has *converted the substrate* into external voice — and the next external artifact will read thin, because the internal system has stopped generating novel lessons.

The ordering is what mod-505 chapter 6 § *keynote-only drift* names as a failure mode. This chapter is the positive form of that failure-mode discipline: the *practice* that keeps the internal artifact stream running while the external work happens.

## What internal-community thought leadership looks like at principal altitude

Mod-505 chapter 5 walked the four canonical community rituals from the internal-culture-elevation seat: the architecture-review study group, the internal ML engineering-blog, the applied-relevance reading discussion, and the cross-team rotation. Those rituals *run the community*. This chapter is about the *authored artifacts* the principal produces *within* that community — the artifacts that a staff-plus engineer at your org opens, reads, and pattern-matches their own work against.

Three artifact classes carry most of the load.

### Artifact class A — the internal talk

**What it is.** A 30–45 minute recorded talk at an internal engineering forum — the ML-org all-hands, the engineering-wide tech talk series, the applied-ML office hours, a new-hire onboarding week deep-dive, the CTO's staff-plus community-of-practice. The talk's audience is 30–500 internal engineers.

**What it is not.** A 15-minute status update at a team's sprint review (that is standard team communication, not thought leadership). A team-scoped teach-back after a specific launch (that is the launch owner's craft, one rung below principal). A keynote at an external conference (that is chapter 4).

**Content shape at principal altitude.** The internal talk is where the principal *first* frames a lesson before it reaches any external audience. It carries the same through-line discipline chapter 4 will apply to keynotes, but the take-away artifact is *internal* — a decision framework the ML org can immediately reuse, a reference architecture diagram published to the org's canonical location (mod-503 chapter 5), an eval-standard proposal that will subsequently ratify through the org-wide architecture-review body (mod-503 chapter 7).

**Cadence at principal altitude.** Roughly 3–5 per year. One per major artifact refresh (semi-annual mod-502 north-star refresh, annual mod-503 architecture revision), plus one or two topic-driven ones (a foundation-model program readout, a canonical-eval standard proposal, a portfolio-scope retro on a bet that was retired). Chapter 6 § *the internal-vs-external ratio* returns to the numeric target.

### Artifact class B — the tech-radar entry

**What it is.** An entry in the org's tech-radar — the internal document that classifies technologies, patterns, and architectural stances into a small set of tiers (Adopt / Trial / Assess / Hold is the canonical ThoughtWorks-radar taxonomy; many orgs use variants). Each entry is a short authored piece — typically 200–800 words — with a specific position, the evidence supporting it, and the boundaries the position applies within.

**What it is not.** A tool-selection RFC (that is a staff-scope RFC and belongs in the mod-410 exercise-02 RFC portfolio). A team-scope build-vs-buy decision (that is the team's tech-lead's craft, one rung below principal). A vendor endorsement (that is a procurement decision and belongs with the CFO / procurement seat).

**Why principal-authored radar entries matter.** The org's tech radar is the *canonical short-form* the whole ML org converges on for technology and pattern positions. A radar entry authored by the principal — with the specific evidence and the specific boundaries — sets the position that a hundred subsequent design reviews will reference. A radar entry that is *not* authored by the principal, or where the principal has abdicated to a lower-altitude author, means those hundred design reviews will surface the position ad-hoc, with less rigor and more churn.

**Cadence at principal altitude.** Roughly 4–8 per year — one per quarter for the "hot" positions (which foundation-model providers are Adopt, which eval methodologies are Trial, which agentic framework patterns are Hold-and-why), plus two or three per year for the "structural" positions (which architectural stances the ML org has ratified, which non-negotiable invariants the reference architecture enforces).

### Artifact class C — the canonical org-wide reference doc

**What it is.** A long-form authored document that becomes the *single canonical reference* the org points at for a specific topic — the *why we do it this way* document. Examples: the ML org's *bet-lifecycle document* (how a bet moves from proposal to trial to adopted to sunset), the *cross-team eval program specification* (the eval standard mod-505 chapter 2 § *Class D* names), the *foundation-model program economics document* (mod-502 chapter 4 § *the FM program* is the internal artifact this externalises), the *reference architecture narrative* (mod-503 chapter 5 § *the north-star document*).

**What it is not.** A blog post (that is external). A spec (specs live at the API-contract layer, mod-503 chapter 4). A one-pager (one-pagers are executive-audience — mod-504 chapter 5). A wiki article (wikis are collaborative and low-authorship-signal; a canonical reference doc is single-authored and revised in place).

**Content shape at principal altitude.** The doc has an *audience* (the whole ML org, plus the peer platform-side principal, plus new-hire staff-plus engineers), an *artifact shape* (5–20 pages, sectioned, versioned in-place), a *cadence* (annual major revision plus quarterly minor revisions), and a *review body* (the org-wide architecture-review body from mod-503 chapter 7). Every principal-altitude reference doc is co-authored with named collaborators — chapter 2 § *co-authorship* below explains why.

**Cadence at principal altitude.** Roughly 2–4 authored or substantially co-authored per year, plus 6–10 minor revisions per year on the existing corpus. The reference-doc set persists across years; the principal's job is to keep it *canonical* (single source of truth), *accurate* (revised when the underlying system evolves), and *cited* (referenced from every downstream artifact — the internal talk, the tech-radar entry, the exec-audience one-pager, the paper's related-work section).

## The internal-first ratio

There is a numeric discipline the principal can hold themselves to on the internal-vs-external balance. It is not a hard rule; it is a rebalancing signal.

**The 70/30 ratio (roughly).** Across a fiscal year, the principal's *authored artifact hours* should split roughly 70% internal and 30% external. The 70% covers the three artifact classes above plus the routine paired-artifact work mod-503 and mod-504 name (living diagrams, canonical APIs, one-pagers, deep-dives). The 30% covers everything in chapters 3, 4, and 5 of this module — papers, blogs, keynotes, open-source releases.

Two caveats:

- **The ratio is *hours of authoring*, not *count of artifacts*.** A single external paper can absorb 60–120 hours across a year; three internal tech-radar entries might be 12–20 hours in total. Counting artifacts inverts the ratio.
- **The ratio is fiscal-year, not monthly.** External artifact work clusters — a paper is drafted in a two-month push, a keynote is prepared over 4–6 weeks. The ratio balances over the full year, not any given month.

The rebalancing signals fire when the ratio inverts for two consecutive quarters. Signal 1: the internal talk slate has been empty for six months and the last two authored artifacts were external. Signal 2: the tech-radar has three or more positions the principal has *not* authored and none the principal *has*. Signal 3: a canonical reference doc has gone 12+ months without revision while an external paper is in its third revision cycle. Any two of the three firing simultaneously is the rebalancing trigger; chapter 6 § *the calendar-shape check* returns to this.

## Co-authorship as internal-community leverage

Every principal-altitude internal artifact is *co-authored*, not solo-authored. This is a deliberate discipline for three reasons.

**Reason 1 — leverage.** Mod-505 chapter 2 § *class B leverage moves* named a canonical property of principal work: *once-authored, repeatedly-used*. Co-authorship extends the leverage by making the artifact *once-authored, repeatedly-used, and co-owned across a peer set*. A tech-radar entry co-authored with the staff engineer whose team runs the eval standard is a tech-radar entry the team will defend, extend, and cite.

**Reason 2 — succession.** The principal is not permanent. The canonical reference doc co-authored with two staff engineers today is the reference doc one of those staff engineers can revise autonomously in 18 months when the principal has moved to the next altitude or the next org. Sole-authored artifacts age poorly the moment the author's context shifts.

**Reason 3 — the mentorship seam.** Mod-505 chapter 5 § *co-authorship as the culture-writing practice* is where this discipline compounds with the mentorship craft. The staff engineer who co-authors the tech-radar entry is *practising the artifact shape* they will need to author solo at principal altitude. The internal-community thought-leadership work is where the principal builds the *next* principal-altitude authors.

Practical shape: for every internal artifact class listed above, the principal names 1–2 co-authors before the artifact is drafted. The co-authors are not thanked-in-the-acknowledgements; they are named on the byline, they contribute at least 20% of the drafting, and they hold the responsibility for a specific section. Chapter 3 § *co-authorship in external artifacts* extends the same discipline to papers and blogs.

## Distinguishing internal from external community

The internal community is *the ML org itself and the immediate platform-and-product neighbours it works with*. The external community is *everyone else*: peer companies, peer principals, the industry-wide audience Capital One's preferred-qualification enumerates.

Four practical distinctions matter.

- **Access.** The internal artifact circulates on internal channels (Slack, the ML org's internal blog, the engineering wiki, the canonical-doc registry from mod-503 chapter 5). The external artifact circulates on public channels. A canonical reference doc mirrored to a public GitHub repo has become an external artifact — and needs the chapter 3 blog discipline or the chapter 5 open-source discipline applied to it.
- **Legal / IP surface.** Internal artifacts do not require legal review (with rare exceptions — a document referencing customer data may). Every external artifact requires legal review, and often a security review as well. Chapter 3 § *the pre-publication legal review* and chapter 5 § *release-level decisions* both walk this in more detail.
- **Reviewers.** Internal artifacts are reviewed by the org-wide architecture-review body (mod-503 chapter 7), the ML-org director, or a named principal peer. External artifacts are reviewed by the venue (PC, editor, programme chair) plus a marketing / comms partner plus legal. The reviewer surfaces are not the same, and the artifact must survive both.
- **Feedback horizon.** Internal artifacts get feedback in weeks (a tech-radar entry is challenged at the next design review). External artifacts get feedback in months to years (a paper's citation graph, a keynote's follow-on conversations). Chapter 6 § *return on external-influence investment* returns to the horizon-mismatch that makes external-only work risky.

## Failure modes

- **The keynote-only drift.** Named in mod-505 chapter 6; picked up here. The principal ships a keynote, gets validating feedback, and starts optimising for the next keynote. Six quarters later the internal tech-radar has gone stale, the reference-doc corpus is under-revised, and the principal's org-internal credibility has decayed. The fix is the internal-first ratio and the calendar-shape check chapter 6 walks.

- **The abdicated tech radar.** The principal treats the tech-radar as *someone else's document* — the platform director's, or a rotating committee's. Two years in, the radar carries positions the principal disagrees with (or agrees with by default), and design reviews across the org keep re-litigating those positions because the radar has no authored weight behind them. The fix: pick 3–5 radar positions per year the principal authors personally; refuse to delegate those.

- **The unwritten reference doc.** The principal *carries* the canonical framing (the bet-lifecycle, the eval-program spec, the foundation-model economics) in their head and in their 1:1s and in whiteboard sessions, but there is no single canonical document. Six months after the principal moves on, the framing has fragmented across seven Slack threads and three team wikis and no one can recover the original. The fix: write it down, canonicalise it, and revise it in place. Chapter 6 § *the durability signal* is the observable form.

- **The solo-authored reference doc.** The principal does write the reference doc but does not co-author. The doc is technically excellent, cited widely, and completely non-durable — because when the principal moves on, no other named author has the internal authority to revise it, and the doc calcifies. The fix: name co-authors before the first draft; give them section-level ownership.

- **The internal-blog-as-external-blog confusion.** The principal drafts a piece for the *internal* engineering blog but writes it as if for the external audience — hedged language, no company-specific detail, no numbers. The internal-community reader gets nothing they could not have found in a public blog, and the artifact fails the internal audience without benefiting from the external. The fix: pick one audience per artifact; the internal artifact is *for insiders* and should carry the specifics.

- **The Ibotta-quote-as-permission.** The principal invokes Ibotta's *thought leader in a growing community* framing as licence to broadcast opinions without evidence. Thought leadership at principal altitude is not opinion-volume; it is authored artifacts other people cite. The fix: return to chapter 1 § *external influence is engineering work* — the artifact, the audience, the cadence, the review body.

## The bridge to chapters 3–5

The three external venue classes chapters 3, 4, and 5 walk each depend on the internal-first substrate this chapter names. Specifically:

- **Chapter 3 (paper / blog).** The paper's *lesson* is extracted from the internal system whose reference doc the principal (co-)authored (artifact class C above). The blog's *pattern* is a pattern the internal talk (artifact class A) has already road-tested.
- **Chapter 4 (keynote).** The keynote's *through-line* has been through 2–3 internal talks first. Chapter 4 § *the through-line pre-flight* is the specific practice.
- **Chapter 5 (open source).** The open-source release's *contract* mirrors the internal north-star architecture's canonical API surface (mod-503 chapter 4). An open-source release that diverges from the internal reference architecture becomes the *worst* form of maintenance burden: two implementations to keep coherent.

An external artifact whose internal substrate is missing is an artifact the principal cannot defend under a good-faith staff-plus reader's questioning. The reader will ask, in effect, *"how does this actually run at your org?"* — and the principal has to be able to answer.

## Summary

- Ibotta's *"leading contributor, voice, and thought leader in a growing community of machine learning practitioners"* framing scopes to the internal community first, external as follow-on. The ordering is load-bearing: external-artifact credibility rests on internal-first evidence, and external-work opportunity cost is internal work.
- Three internal-authored artifact classes carry most of the principal's internal-community load: the internal talk (3–5/year), the tech-radar entry (4–8/year), and the canonical org-wide reference doc (2–4 authored plus 6–10 revisions/year).
- The internal-first ratio is roughly 70% internal authoring hours to 30% external across a fiscal year. Three rebalancing signals fire when the ratio inverts; any two together are the trigger to rebalance.
- Every principal-altitude internal artifact is co-authored, not solo-authored — for leverage, for succession, and for the mentorship seam (mod-505 chapter 5 § *co-authorship as the culture-writing practice*).
- Internal and external communities differ on access, legal/IP surface, reviewer set, and feedback horizon. A canonical internal reference doc mirrored publicly has become an external artifact and needs the chapter 3 or chapter 5 discipline applied.
- Six failure modes: keynote-only drift, abdicated tech radar, unwritten reference doc, solo-authored reference doc, internal-blog-as-external confusion, Ibotta-quote-as-permission.
- Chapters 3–5 each depend on this chapter's substrate. Chapter 6 returns to the internal-first ratio as the calendar-shape check.
