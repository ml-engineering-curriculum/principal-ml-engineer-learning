# External Industry Influence as an Engineering Discipline — Venue, Audience, Artifact

> Chapter 1 of mod-506. Prerequisite: mod-501 chapter 5 § *four principal-scope themes* (this module owns the fifth, principal-defining, below-threshold theme), mod-504 chapter 2 (audience boundary) and chapter 5 (SVP / CTO-audience narrative craft). Downstream: every subsequent chapter treats one venue class (chapter 3 paper / blog, chapter 4 keynote, chapter 5 open-source contribution) and reuses the venue-audience-artifact matching this chapter fixes.

## Why external influence is engineering work, not marketing

Two role definitions frame the target for the whole module and this chapter in particular.

- **Capital One (Sr. Distinguished AI Engineer, preferred qualification):** *"ML industry impact through conference presentations, papers, blog posts, or open source contributions."* The verb is *impact*, the objects enumerate exactly four venue classes. The clause is a preferred qualification, not a required qualification — the module is deliberately smaller (10h) than the mandatory-theme modules, and every artifact this module authors carries the same *evidence, not aspiration* discipline the rest of the track uses.
- **Ibotta (Principal ML Engineer):** *"Act as a leading contributor, voice, and thought leader in a growing community of machine learning practitioners."* The Ibotta framing is broader than Capital One's — the *community* need not be external; the internal ML org counts, and chapter 2 argues it counts *first*.

Together the two framings scope what this module owns: **the principal's external voice, in the four venue classes Capital One names, grounded in the internal-community credibility Ibotta names**. The rest of the module walks each venue class as a specific craft; this chapter fixes the venue-selection discipline that comes before any of the individual crafts.

External influence is engineering work because it has an *artifact*, an *audience*, a *cadence*, and a *review body* — the same four properties every principal artifact has (mod-503 chapter 1 § *what a living architecture is and is not*, mod-504 chapter 5 § *the FAQ as a first-class artifact*). It is not marketing (which optimises the artifact for reach), and it is not personal-brand work (which optimises the artifact for the author). It optimises for the *reference the industry adopts* and the *problem class the community makes progress on* — the same targets the mod-503 north-star architecture optimises for internally.

Three consequences of treating the practice as engineering work fall out immediately.

**Consequence 1 — venue choice is a design decision.** A talk that would have landed as a QCon industry-track session and instead gets pushed to a NeurIPS submission fails not because the content was wrong but because the audience-artifact match was wrong. Chapter 4 walks the venue-vs-artifact map; this chapter fixes the underlying discipline.

**Consequence 2 — the artifact has to be defensible after the room.** The paper, blog post, keynote, or open-source release the principal ships is *cited* by other principals — often years later. A claim that survived the 45-minute keynote but does not survive an independent staff-plus reader six months on is a defect. Chapter 3 § *writing discipline* and chapter 5 § *maintainership contract* both cash out this point.

**Consequence 3 — an influence bet is a bet.** It takes principal-scope time (chapter 2's internal-first discipline sets the priority ordering), returns signal on a lagging horizon (chapter 6 § *return on external-influence investment*), and can decay (chapter 6 § *retirement criteria*). The four venue classes are not a checklist; they are a *portfolio* the principal deliberately allocates against, and mod-502 chapter 6's signal-tracking cycle is the closest analogue for how it is managed.

## The four venue classes and what each is for

Capital One's list enumerates four venue classes. Each does specific work on specific audiences with specific artifacts. Confusing them is the modal first-cycle failure.

### Venue class 1 — Industry-track paper (peer research-adjacent)

**Canonical venues.** KDD industry track, RecSys industry track, WSDM industry track, MLSys, NeurIPS / ICML workshops with industry-track submission windows (e.g., ML for Systems, ML in the Physical World), the applied-ML tracks at SIGIR / WWW / CIKM. Sometimes a peer-reviewed venue with an industry-outcomes preference (Deployable ML, Applied Data Science tracks).

**Audience.** Staff-plus applied-ML engineers, principal-track engineers at peer companies, applied-research scientists whose research programs intersect the paper's problem class. Second-order audience: hiring managers at peer orgs whose staff-plus candidates cite the paper; university faculty whose PhD students look for industry programs to apply to.

**Artifact.** A paper — typically 4–8 pages for a workshop, 8–12 pages for a full industry-track submission — with the applied-ML *system* as the artifact under study. Not a *model paper* (that is the peer research-principal track's craft — [`ai-research-scientist-learning`](https://github.com/ml-engineering-curriculum/ai-research-scientist-learning) owns the peer-reviewed academic publication discipline). An industry-track paper's contribution is *the design and the data on the system as it ran in production*: the architecture decision, the evaluation program that ratified it, the failure mode the org retired, the abstraction that generalised.

**When the venue-artifact match is right.** The lesson generalises across companies, the production system has enough scale that the numbers are load-bearing (throughput, latency, coverage, ratifications-per-cycle), and the org will approve external publication of the specifics. The lesson is the *system design and the data*, not the *proprietary edge*.

**When it is wrong.** The lesson is a *point solution* to one company's product surface (blog is better — venue class 2). The lesson is *directional and hortatory* rather than measurable (keynote is better — venue class 3). The lesson is a *reusable library or interface* (open source is better — venue class 4).

### Venue class 2 — Blog post (applied-ML engineering blog series)

**Canonical venues.** Company-owned engineering blogs — Meta Engineering, Airbnb Tech Blog, Uber Engineering, Pinterest Engineering, LinkedIn Engineering, Netflix TechBlog, DoorDash Engineering, Instacart Tech, Stripe Blog, and the equivalents at peer orgs. Independent applied-ML publications and newsletters that syndicate or original-publish long-form applied work (Papers With Code newsletter, The Sequence, Import AI, and topic-specific newsletters in RecSys / MLOps / eval). The principal's own long-form on a platform the principal maintains sits here too, but should be treated as *third-priority* — see chapter 6 § *the platform-of-one failure mode*.

**Audience.** Staff and staff-plus engineers actively looking for applied patterns to reuse (search-driven readers, months to years after publication). Second-order: hiring pipeline for staff-plus roles; peer principals doing landscape scans.

**Artifact.** A long-form post — typically 2,000–6,000 words with diagrams and, where possible, a code snippet or a reference implementation link. The post's contribution is the *pattern* extracted from the production system: the mistake the org learned from, the invariant that held up across three iterations, the trade-off matrix that emerged, the metric that turned out to matter. Not a *release announcement* (product marketing owns that surface) and not a *tutorial* (that is a build-altitude craft owned by [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) and [`ml-engineer-learning`](https://github.com/ml-engineering-curriculum/ml-engineer-learning)).

**When the venue-artifact match is right.** The lesson is generalisable but requires more product-and-org context than a paper's abstract allows, the numbers may be less rigorous than a peer-reviewed submission would require, and the org values a broader reach than a paper's citation-driven audience. The applied-ML engineering blog series pattern (see references at end of chapter) is the modal shape — a canonical piece per production system, authored by the staff-plus / principal engineer who ran the system, edited to a house standard.

**When it is wrong.** The lesson is a *product announcement* (marketing surface). The lesson is a *one-off write-up* that will not be updated across the system's evolution (a paper is more honest about the "as of writing" contract). The lesson is a *reference architecture the whole org should converge on* (that is the internal north-star artifact — mod-503 — and the external version follows the internal one, not the other way around).

### Venue class 3 — Conference keynote or industry-track talk

**Canonical venues.** O'Reilly AI, QCon (AI track), Strata Data & AI, MLOps World, LinkedIn's community-hosted principal-scope meetups, Ray Summit / KubeCon AI Day / MLSys workshop keynotes, PyData / SciPy plenaries, the industry-day plenaries at KDD / RecSys / NeurIPS. An internal-first keynote (a company-hosted principal-scope conference — Meta's @Scale, Google I/O side stages, AWS re:Invent's ML deep-dives) fits here too if it is externally-attended, though its audience skews toward the hosting company's user base.

**Audience.** A room of 100–2,000 staff-plus engineers and engineering leaders. Second-order: the recorded talk on YouTube / conference archive, watched asynchronously by 3–20× the room size over 12–36 months.

**Artifact.** A 30–45 minute presentation, an accompanying slide deck, and — chapter 4 will argue this loudly — a *take-away artifact* the audience can walk out with (a reference diagram, a decision framework, a checklist, an open-source repo). The presentation's contribution is *the through-line*: one sentence the audience remembers, backed by 3–5 concrete illustrations they can pattern-match against. Not a *survey talk* (a survey belongs in a paper or a written landscape review), not a *tutorial* (tutorial-track sessions are a build-altitude craft), and not a *pitch deck* (that is marketing and the audience will read it as such).

**When the venue-artifact match is right.** The lesson is *directional* — a bet-framing, an architecture stance, a program-design philosophy — where the emotional weight of the presentation matters as much as the technical content. The audience is *decision-influenced* rather than *information-completed*: a staff-plus engineer leaves the room with a decision framework and applies it back at their own org, whereas a reader of a paper leaves with data they can cite. Chapter 4 walks the executive-audience-narrative reuse from mod-504 chapter 5.

**When it is wrong.** The lesson is a *system deep-dive that needs 20 pages to defend* (paper). The lesson is a *pattern reference that people will search for later* (blog). The lesson is a *reusable interface* (open source). A talk pretending to do any of these will read as thin.

### Venue class 4 — Open-source contribution at principal altitude

**Canonical venues.** A new open-source project (the org releases a library, a benchmark, a reference implementation), a substantial upstream contribution to an existing project (a feature-tier addition to Ray, PyTorch, JAX, MLflow, Kubeflow, Feast, TFX, Weights & Biases OSS, LangChain, Airflow, DBT, etc.), a benchmark / eval suite the community adopts (BIG-bench, HELM, MTEB, MLPerf-style benchmark submissions), a standards-body contribution (an ONNX operator, a MLCommons benchmark, an OpenTelemetry ML-metrics extension, a CNCF-adjacent ML project).

**Audience.** Downstream users of the code (staff-plus engineers integrating the library into their own systems), the project's maintainer community (other principals whose orgs contribute to the same codebase), and — critically — *your own future teams* who will encounter the release as an external dependency.

**Artifact.** A release, a substantive PR series, a maintainership commit, or a benchmark submission — plus the *release-level decisions* that surround it: the licence, the API stability contract, the maintenance-burden estimate, the alignment (or divergence) between the OSS release and the internal reference architecture. Chapter 5 walks the release-level decision surface in detail; the day-to-day commits are the peer specialist tracks' craft (`senior-ml-engineer-learning` and the platform-side principal tracks own that scope).

**When the venue-artifact match is right.** The lesson is a *reusable interface or implementation* the community can adopt, the org has committed to the multi-year maintenance burden, and the release aligns with the internal north-star architecture such that maintaining it publicly *lowers* rather than *raises* internal maintenance cost.

**When it is wrong.** The lesson is a *pattern description* (blog). The lesson is a *point-in-time snapshot* the org will not maintain (open-sourcing an unmaintained codebase harms the community and the org's own credibility). The release is a *marketing thin wrapper* on top of proprietary depth (the community reads through this in one week).

## The venue-audience-artifact matching discipline

The four venue classes are not equivalent surfaces. The principal's first move on any external-influence bet is to match the *lesson* to the *venue* to the *audience*. The matching discipline has four steps.

**Step 1 — name the lesson in one sentence.** Before picking the venue, write the lesson as if it were the direction sentence of a mod-504 chapter 5 one-pager: one sentence, roughly 30–60 words, no proper nouns unless load-bearing, ending with what the audience should take away. The sentence is what the venue-audience-artifact match tests against. If you cannot write it, the bet is not yet ready for any venue.

**Step 2 — classify the lesson.** Which of four shapes does it take? (a) *System-and-data* → paper; (b) *pattern-with-context* → blog; (c) *directional-with-through-line* → keynote; (d) *reusable-interface* → open source. Some lessons take multiple shapes; a single bet may fan out into a paper, a blog, and a talk on the same production system (chapter 3 walks the paper-blog split as a common fan-out; chapter 4 walks the paper-and-keynote pairing). Do not, however, ship the same content in multiple venues without shaping it for each — the same 45-minute talk turned into a blog post reads as a transcript; the same paper turned into a keynote reads as a survey.

**Step 3 — audit the audience-artifact fit.** For the venue class you have picked, name the specific reader you are writing for. A KDD industry-track paper's reader is not the same as an O'Reilly AI keynote's audience is not the same as the Meta Engineering blog's reader. If you cannot name the specific reader in one sentence (title band, current problem, why they are searching for or listening to this), the artifact will drift toward "someone who cares about the topic in general" — which is *no reader*.

**Step 4 — validate against the reviewer.** Every principal-scope external artifact has a *reviewer*. For a paper, the venue's programme committee. For a blog, the org's engineering-blog editor (Meta Engineering, Uber Engineering, and Airbnb Tech Blog all run explicit editorial review). For a keynote, the conference's programme chair. For an open-source release, the project's maintainer community and — critically — the org's legal and IP counsel. If you cannot name the reviewer and the criteria they will apply, the artifact will fail the venue's bar. This step is the closest analogue to mod-505 chapter 4 § *the review bar* at the external surface.

## The venue-selection failure modes

Six failure modes recur across principal-scope venue selection. Each is a specific class of match-failure between the lesson and the venue.

- **Failure mode 1 — the wrong-venue paper.** A pattern-with-context lesson (blog shape) submitted as a paper. The paper reads as under-evaluated because the numbers are not paper-rigorous, and the industry-track PC (correctly) desks it. The fix: shape the lesson as a blog first, and then — if the numbers hold — extract a paper from the blog's substrate later.

- **Failure mode 2 — the venue-chase.** The principal picks the venue for its prestige (a NeurIPS submission where the KDD industry track was the actual home; a keynote at O'Reilly AI when a blog would have reached the same staff-plus audience with 5% of the effort). The venue's audience does not match the lesson's target reader; the artifact underperforms; the principal's next bet defensively over-invests to compensate. The fix: name the target reader before naming the venue.

- **Failure mode 3 — the surveyed-in-a-keynote pattern.** The principal has three years of production-system work and tries to compress it into a 45-minute keynote as a "here is everything we learned" survey. The audience leaves without a through-line, cannot summarise the talk to a colleague, and the recording under-performs on the archive. The fix: pick the one through-line that generalises and cut the other 60% of the material.

- **Failure mode 4 — the promotional blog masquerading as engineering content.** The blog is written by the principal but edited by marketing to remove the *hard parts* — the failure mode the org learned from, the non-goal the org explicitly ratified, the sunset criterion the direction now carries. The remaining artifact is a promotional post the staff-plus reader (correctly) discounts. Chapter 3 § *the honest-failure discipline* is the reference. The fix: agree upfront with the engineering-blog editor that the hard parts are load-bearing; if they must be cut, the artifact is not ready.

- **Failure mode 5 — the open-source dump.** The principal open-sources a codebase the org will not maintain — internal-tools code released "for the community" that gets no PRs, no releases, and no security patches after the launch quarter. Chapter 5 § *the multi-year maintenance commitment* is the reference; the fix is to refuse the release if the maintenance commitment is not underwritten.

- **Failure mode 6 — the venue-inflation over time.** The principal ships one keynote, gets positive signal, and treats every subsequent bet as a keynote-shape opportunity. Six quarters later the internal-community credibility (chapter 2's substrate) has decayed because the internal-first ratio has inverted. Chapter 2 § *the internal-first ratio* is the ratio; chapter 6 § *the recruiting-signal decay curve* is the observable outcome. The fix: audit the venue portfolio annually and rebalance.

## The prerequisite chapter 2 will unpack

Two things are true about principal-scope external influence.

**External influence is a preferred qualification, not a mandatory qualification, in the current-cycle sample.** Capital One's language is explicit and the module's 10-hour size reflects it. A principal who has never spoken externally can still hold the seat; a principal who has *only* spoken externally cannot. Chapter 2 walks the *why* — the internal-community-first discipline that must come before any external voice for the external voice to carry the credibility of a principal rather than the credibility of a keynote personality.

**Internal thought leadership is Ibotta's framing and is the substrate for everything the rest of the module covers.** The next chapter argues that the internal-community craft — the internal talk series, the tech-radar authorship, the canonical org-wide reference doc series — must not just precede external work chronologically but must *continue to run in parallel* with it. The external artifact is legible in the industry only because the internal artifact is legible in the org.

## Summary

- External industry influence is engineering work, not marketing. It has an artifact, an audience, a cadence, and a review body — the same four properties every principal artifact has. It optimises for the reference the industry adopts, not for reach or personal brand.
- Capital One's preferred-qualification framing enumerates four venue classes: industry-track paper, blog post, conference keynote, open-source contribution. Each has a distinct audience, artifact shape, and reviewer.
- The venue-audience-artifact matching discipline is four steps: name the lesson in one sentence, classify the lesson's shape, audit the audience-artifact fit, validate against the reviewer. The first step is the leverage step; if the lesson-sentence is not writable, no venue will save the bet.
- Six failure modes: wrong-venue paper, venue-chase, surveyed-in-a-keynote, promotional-blog-masquerade, open-source-dump, venue-inflation. Each is a specific match-failure between the lesson's shape and the venue's discipline.
- External influence is a *preferred* qualification in the current-cycle sample, and the module is deliberately sized to reflect that. The principal-defining substrate is the *internal* thought-leadership work Ibotta's role framing names — which chapter 2 argues must both precede and run in parallel with any external voice.
- Chapter 2 walks the internal-community discipline. Chapters 3–5 walk each venue class in depth. Chapter 6 walks the return-on-external-influence tracking that decides which bets to renew, which to retire, and which to escalate to the next altitude.
