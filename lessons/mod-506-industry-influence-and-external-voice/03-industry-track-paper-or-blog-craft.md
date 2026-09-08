# The Industry-Track Paper or Applied-ML Engineering Blog — Extracting a Principal-Scope Lesson From Production

> Chapter 3 of mod-506. Prerequisite: chapter 1 (venue-audience-artifact discipline) and chapter 2 (internal-first substrate). Downstream: exercise-02 authors a full first draft of one paper or blog. Interacts with mod-503 chapter 5 (the canonical reference doc the paper extracts from) and mod-505 chapter 2 § *Class D* (the cross-team eval program that often becomes the paper's evaluation section).

## What the venue asks of principal-altitude content

Chapter 1 fixed the venue classes. This chapter walks two of them together — the industry-track paper and the applied-ML engineering blog post — because they share more craft than the naming suggests. Both are *written* artifacts. Both extract a *lesson* from a real production ML system. Both are cited by staff-plus readers months to years after publication. The difference is in *evidence rigor* (the paper's PC and the blog's editorial review apply different bars), *audience shape* (the paper's reader is a peer researcher-or-principal doing citation-driven work; the blog's reader is a staff-plus engineer doing search-driven work), and *artifact durability* (a paper is a point-in-time snapshot with the "as of writing" contract; a blog is periodically updateable with an update log).

Both carry the productive-dissemination pattern this module is grounded in — the applied-ML engineering blog series that Meta, Airbnb, Uber, Pinterest, LinkedIn, Netflix, DoorDash, Instacart, and their peers run; the industry-track programme of KDD, RecSys, WSDM, SIGIR, WWW, CIKM, MLSys, and the applied-workshop programme at NeurIPS / ICML. This is *productive* dissemination in the sense that the artifact is designed to make the industry more productive, not to advance the author. The academic publishing craft — the peer-reviewed model paper whose contribution is a novel technique — belongs to the peer research-principal track ([`ai-research-scientist-learning`](https://github.com/ml-engineering-curriculum/ai-research-scientist-learning)); it is not this module's scope.

Four *principal-scope lessons* fit the paper-or-blog venue and this chapter's craft.

- **Architecture at portfolio-and-industry altitude.** The lesson about the *reference architecture* — the mod-503 north-star — that other orgs' principals should adopt or diverge from. Example lesson shape: *"our ML org converged on a feature-registry-and-inference-gateway substrate with three-tier data discipline; here is the API contract, here is the eval program that ratified it, here is the migration cost profile across three product areas."*
- **Cross-team eval program discipline.** The lesson about the *shared eval standard* (mod-505 chapter 2 § *Class D*) that lifted the whole ML org's release quality. Example lesson shape: *"we ran a cross-team eval program that unified 11 model teams onto a single ratification-and-launch protocol; here is the protocol, here is the effect on regression-rate and time-to-launch, here is the discipline that kept teams from drifting off it."*
- **Org-wide bet framing.** The lesson about the *mod-502 north-star* — the multi-year bet portfolio and its sunset criteria. Example lesson shape: *"we framed our foundation-model program as an integration bet with a targeted post-training program on the enterprise side; here are the sunset criteria we ratified with the CFO, here is the signal-tracking cycle, here is what shifted at the 18-month mark."*
- **Foundation-model program economics.** The lesson about the *TCO envelope* (mod-502 chapter 5's cost-and-capacity discipline) that other orgs' principals can pattern-match against. Example lesson shape: *"here is the FY26 cost profile for our Gen-AI integration; here is the sensitivity to frontier-provider pricing shifts; here is the vendor-risk model we ratified with the CISO."*

Anything narrower than one of these four shapes — a specific model-architecture win, a specific benchmark result on a specific dataset — is *not* a principal-scope lesson. It is a staff-scope or senior-scope contribution. Chapter 1 § *when the venue-artifact match is wrong* is the reference; those artifacts belong in a different venue with a different author (see [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) and [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) for the peer-scope publication craft).

## Paper vs. blog — when to pick which

Both venues can carry the same lesson. Three signals decide.

### Signal 1 — is the evaluation numerically load-bearing?

- **Numbers rigorous enough to defend at a PC.** If the lesson turns on numeric evidence — throughput, latency, coverage, statistical significance across a controlled comparison, a benchmark result under a fixed methodology — a paper is the honest venue. Papers force a discipline (methodology section, ablations, threats-to-validity) that a blog does not. A blog with the same numbers looks like it is skipping the discipline.
- **Numbers illustrative rather than load-bearing.** If the lesson is a *pattern* with numbers illustrating the shape (a rough throughput range, an approximate improvement, a *"we saw materially better"* claim without a controlled comparison), a blog is the honest venue. A paper submitted with illustrative numbers will (correctly) be desk-rejected.

### Signal 2 — is the lesson still evolving?

- **Snapshot lesson.** The system reached a stable state and the lesson is the *design that stabilised*. A paper is a natural fit; the *as-of-writing* contract matches the stability.
- **Evolving lesson.** The system is still evolving and the lesson will be revised over the next 12–24 months. A blog is a natural fit; the update log makes the evolution legible. A paper on an evolving lesson calcifies into a snapshot that the next reader has to check against the current state — often finding the paper obsolete.

### Signal 3 — what does the org's legal / IP posture allow?

- **Some organisations require peer-review venues.** Regulated industries and orgs with academic-partnership cultures may prefer or require peer-reviewed publication for any externally-published material. In that setting the paper is not a choice but a requirement.
- **Some organisations prefer engineering-blog surfaces.** Consumer-tech orgs with strong engineering-brand programmes typically prefer blog publication because it feeds the recruiting funnel more directly. In that setting the blog is the modal venue and the paper is the exception.
- **The org's legal review has veto power on both.** Chapter 3 § *the pre-publication legal review* below returns to this.

When the three signals conflict — the numbers are load-bearing (paper), the lesson is still evolving (blog), and the org prefers blog (blog) — the resolution is a *paper-plus-blog pair*: a paper that captures the snapshot and gets cited by the peer-research audience, plus a blog that carries the evolution and gets read by the search-driven audience. Chapter 3 § *the paper-plus-blog fan-out* walks the pair. Do not, however, ship the paper's content as the blog verbatim; each venue needs its own shape.

## The lesson-extraction discipline

Every principal-scope paper or blog begins with a *lesson-extraction pass* over the internal substrate. The pass is deliberate and has four steps.

**Step 1 — pick the internal artifact the lesson extracts from.** Chapter 2 § *canonical org-wide reference doc* (artifact class C) is the modal source. The paper on foundation-model program economics extracts from the internal FM-program economics reference doc. The paper on cross-team eval-program discipline extracts from the internal cross-team eval reference doc. If there is no internal reference doc, there is no paper — write the internal doc first, revise it for two quarters, and then extract the paper. Chapter 2's ordering discipline is what protects this.

**Step 2 — decompose the internal doc into what generalises and what does not.** An internal reference doc has org-specific and generalisable material interleaved. The lesson-extraction pass separates them. What generalises: the *pattern*, the *invariant*, the *trade-off*, the *sunset criterion*, the *numeric envelope*. What does not: the *specific team names*, the *specific product surface*, the *proprietary edge*. The generalisable material is the paper's substrate; the non-generalisable material either goes into the deep-dive appendix (paper) or gets cut (blog).

**Step 3 — reframe the generalisable material as the venue's contribution.** A paper's contribution section names *what is new*. A blog's opening frames *what the reader should take away*. Both surface the same lesson but in the venue's voice. If the reframing forces you to soften the claim ("this pattern *may* generalise" instead of "this pattern *did* generalise across the following three product areas"), the lesson is either not yet ready or the internal-first substrate has not carried enough evidence.

**Step 4 — pick the one honest failure.** Every principal-scope paper or blog carries *one honest failure*: the mistake the org learned from, the sunset that was executed, the invariant that turned out not to hold, the non-goal the team ratified after the second attempt. Chapter 3 § *the honest-failure discipline* below is the practice; the failure-mode section of this chapter names its absence as the modal failure mode.

## Shape of the industry-track paper

The industry-track paper's shape converges on a canonical structure across the venues (KDD, RecSys, SIGIR, WSDM, WWW, CIKM, MLSys). Details vary; the shape below is what an experienced PC would expect.

- **Abstract (150–250 words).** One paragraph. States the problem, the system, the contribution (in the venue's contribution vocabulary — "we present X and evaluate Y under Z"), and one headline result. The abstract is the artifact 90% of the audience reads; the rest is for the citation-driven reader.
- **Introduction (1–1.5 pages).** Why the problem matters in industry; what has been done; what this paper adds. Cites the *industry* related work as heavily as the *academic* related work — a paper without industry citations reads as a lifted thesis chapter.
- **System overview (1.5–2.5 pages).** The architecture, at portfolio-and-industry altitude. Diagrams (mod-503 chapter 5 § *living diagrams* is the source for the diagrams; strip proprietary specifics before including). The section is where the *reference architecture* lesson lives if the paper is on architecture; the *eval program* lesson lives if the paper is on eval; the *bet framing* lesson lives if the paper is on strategy.
- **Evaluation methodology (1–1.5 pages).** The industry-track paper's *hard section*. The controlled comparison, the metric, the data, the ablations, the threats-to-validity. A paper's disposition (accept / revise / reject) often turns on this section. Every claim in the results section must trace to this methodology.
- **Results (1–1.5 pages).** The numbers, honestly. Charts and tables. The honest failure lives here as a *negative result* section (the ablation that failed, the sunset that was executed, the invariant that broke). A paper without a negative-result section reads to a PC as promotional.
- **Discussion and limitations (0.5–1 page).** What the paper does not claim. Where the lesson does not generalise. What the reader should not extract. This is the paper's *non-goals* section (mod-502 chapter 4's non-goal discipline lifted to the paper artifact).
- **Related work (0.5–1 page).** Industry-first citation, academic second. If the related-work section has no industry papers or blogs, the paper has misread the venue's audience.
- **Conclusion (0.25–0.5 page).** The lesson, one paragraph. What the audience should adopt, adapt, or diverge from.
- **References.** Sane citation set. If the reference set is only academic papers, the paper's audience-match is wrong.
- **Appendix.** Optional. The extended methodology, the extra ablations, the reproducibility instructions. Reviewer 2's home.

Length target: 8–12 pages for a full industry-track submission; 4–8 pages for a workshop. Follow the venue's specific template.

## Shape of the applied-ML engineering blog post

The blog post's shape is looser than the paper's but the *discipline* is not. The modal shape is what the Meta / Airbnb / Uber / Pinterest engineering blog editorial teams enforce implicitly.

- **Title (7–12 words).** Names the *system* and the *lesson*. Not clickbait; not marketing. Model: *"How we ran a cross-team eval program that unified 11 model teams"*, not *"The one weird trick that lifted our launch quality by 40%"*.
- **Lead paragraph (100–200 words).** One paragraph. States the problem, the system, and the one lesson the reader should take away. The blog's five-second-scanner reads only this paragraph; every subsequent section is for the search-driven reader who is committing to the full read.
- **Problem framing (300–500 words).** Why the problem matters at scale; what the org was seeing before; what forced the intervention. Sets the *before* state.
- **System / approach (600–1,500 words).** What the org built or ratified. Diagrams (again lifted from mod-503 chapter 5). Code snippets where the API surface makes the pattern concrete. Cross-references to open-source projects if a chapter-5-shape release exists.
- **Evidence (400–800 words).** The numbers, illustrative or load-bearing. Honest about the methodology's rigor. If the numbers are load-bearing, the piece has drifted into paper shape and needs to become one.
- **The honest failure (200–400 words).** The mistake the org learned from, the sunset that was executed. This section is what separates a principal-scope blog from a promotional post; the failure-mode section returns to it.
- **What generalises and what does not (200–400 words).** The mod-502 chapter 4-shape *non-goal* discipline lifted to the blog. Where the pattern applies; where the reader should not apply it.
- **What comes next (100–200 words).** The next 12–24 months of the system's evolution. The update log the next revision of the post will land against.
- **Closing / call to action (50–150 words).** Where the reader can go for more (the open-source release, the paper, the internal team's contact, the follow-up post). Not marketing; not "sign up for our newsletter"; a genuine next surface.

Length target: 2,000–5,000 words; occasionally up to 6,000 for a genuinely comprehensive treatment. Anything longer is a paper in blog clothing.

## Writing discipline (paper and blog, shared)

- **Every claim traces to a chapter, an internal doc, or a public source.** Mod-504 chapter 5 § *writing discipline* is the antecedent; the discipline is doubled at the external-artifact bar because an unattributed claim in an external artifact is a permanent citation for the principal.
- **The honest failure is load-bearing.** Every principal-scope paper or blog carries one honest failure. If the artifact does not, it will read as promotional to a good-faith staff-plus reader and will not carry citation weight.
- **No proper nouns unless load-bearing.** Product names and team names appear only when they carry information the reader needs; otherwise the paper or blog is at *industry altitude* and the specifics are irrelevant. Mod-504 chapter 5 § *the direction sentence — no proper nouns* is the same discipline.
- **The lesson survives compression.** The paper's abstract, the blog's lead paragraph, and (chapter 4) the keynote's through-line all compress to the same one-sentence lesson. If the sentence changes shape across the compressions, the lesson is not yet stable.
- **Co-authorship is the default, not the exception.** Chapter 2 § *co-authorship as internal-community leverage* extends to the external artifact. Every principal-scope paper or blog names co-authors — the staff engineers who ran the system, the peer principals whose collaboration the lesson depended on, the eval-program owner whose work is cited in the methodology section. Single-authored external artifacts from a principal read as glory work and the peer principals at other orgs will (correctly) discount them.

## The paper-plus-blog fan-out

A single principal-scope lesson often produces both a paper and a blog. The two artifacts are not the same content in two shapes; they are two artifacts that share a substrate.

- **The paper carries the snapshot.** The controlled comparison, the methodology, the load-bearing numbers, the citation footprint. Audience: peer researchers-and-principals doing citation-driven work.
- **The blog carries the evolution.** The origin story, the honest failures across multiple attempts, the update log, the operational lessons that do not fit the paper's methodology section. Audience: staff-plus engineers doing search-driven work months later.
- **The two are cross-linked.** The paper's conclusion cites the blog; the blog's evidence section cites the paper. Each artifact is complete on its own but points to the other for the audience that would prefer that shape.
- **Publication cadence.** The paper's cycle is 6–18 months from lesson-stability to acceptance. The blog's cycle is 1–3 months from draft to publication. In practice the blog often lands *first*, and the paper follows once the numbers have hardened enough for PC scrutiny.

## The honest-failure discipline

Every principal-scope paper or blog carries one honest failure. Three ways the honest failure lands.

**Way 1 — the retired bet.** A bet the org ratified, ran, and sunset. The paper or blog documents the sunset criteria, the signal that fired, and the resulting decision. Mod-502 chapter 4 § *sunset criteria* is the internal substrate. Way 1 is the modal failure discipline for a *bet-framing* paper.

**Way 2 — the invariant that broke.** An architectural invariant the org held for 18 months that broke under a specific workload shift. The paper or blog documents the invariant, the workload shift, the recovery, and the revised invariant. Mod-503 chapter 6 § *version-bump triggers* is the internal substrate. Way 2 is the modal failure discipline for an *architecture* paper.

**Way 3 — the eval program that leaked.** An eval standard that missed a class of regression until a production incident surfaced it. The paper or blog documents the leak, the incident, and the eval-program revision. Mod-505 chapter 2 § *class D* is the internal substrate. Way 3 is the modal failure discipline for a *cross-team eval program* paper.

The honest failure is not a hedge or an excuse; it is the *most cited section* of a well-crafted principal-scope paper or blog, because it is what other orgs' principals will (correctly) pattern-match against their own similar decisions.

## The pre-publication legal review

Every external artifact goes through legal review before publication. The principal owns the review cycle, not marketing and not the co-authors. Three specific items always surface.

- **Trade-secret disclosure.** Does the artifact disclose a specific proprietary process, algorithm, or model that the org's IP posture protects? If so, either revise the artifact (the modal outcome) or withdraw it.
- **Customer-data disclosure.** Does the artifact reference specific customer data, specific product usage, or specific business metrics that the org's data-handling policy protects? If so, aggregate, anonymise, or withdraw.
- **Contractual encumbrance.** Does the artifact reference a vendor, partner, or acquired company in a way the contract with that party prohibits? If so, revise or withdraw. Foundation-model provider contracts frequently prohibit specific numeric comparisons or specific benchmark claims; the paper or blog needs to be checked against every applicable contract.

The legal review is not adversarial; it is a co-authoring step. The principal comes to legal with the draft and the target audience; legal comes to the principal with the specific paragraphs that need revision and why. Roughly 2–4 weeks of lead time on the review is the modal cadence; papers submitted to a venue with a tight deadline are the modal failure mode of insufficient lead time.

## Failure modes

- **The lesson-with-no-substrate paper.** The principal writes the paper before the internal reference doc exists. The paper's related-work section is thin (nothing to cite from the org's own artifact stream), the methodology section over-claims (no revised eval program to trace against), and the honest failure is missing (nothing was actually retired). The fix: chapter 2's ordering. Write the internal doc first, revise it twice, then extract the paper.

- **The promotional-blog masquerade.** The blog has no honest failure, no non-goals, no numbers-were-illustrative admission. It reads as marketing content and staff-plus readers discount it. Named as failure mode 4 in chapter 1; the fix is chapter 3 § *the honest-failure discipline* applied at draft time, not as a late edit.

- **The paper in blog clothing.** The blog runs 8,000 words with a full methodology section and load-bearing numbers. It is a paper the author has published as a blog to skip the PC. Readers who need the numbers cannot cite the blog with confidence (no venue peer review); readers who wanted a blog cannot skim it. The fix: split into two artifacts.

- **The blog in paper clothing.** The paper is 6 pages of narrative with a two-paragraph methodology section and no ablations. The PC (correctly) rejects it. The fix: submit as a blog, and only later extract a paper if the numbers harden.

- **The solo-authored artifact.** The paper's byline is the principal alone. The peer principals at other orgs discount it as glory work. The staff engineers who actually ran the system are unattributed. The fix: chapter 2 § *co-authorship* applied to external artifacts. Name the co-authors on the byline; give them section ownership.

- **The insufficient-legal-lead-time crunch.** The paper is drafted for a venue deadline in three weeks; legal review needs four. The principal ships anyway ("we'll accept the risk") and the org's IP team surfaces disclosures after publication. The fix: build legal review lead time into the artifact-plan schedule from the first draft; refuse to submit if the review has not completed.

## Summary

- The industry-track paper and the applied-ML engineering blog are two shapes of the same craft: extracting a principal-scope lesson from a real production ML system for a peer-industry audience. The academic-publishing craft (peer-reviewed model papers) belongs to the peer research-principal track, not this one.
- Four principal-scope lesson shapes fit the venue: architecture at portfolio-and-industry altitude, cross-team eval program discipline, org-wide bet framing, foundation-model program economics. Anything narrower is a peer-scope contribution.
- Three signals decide paper vs. blog: whether the numbers are load-bearing, whether the lesson is still evolving, and the org's legal / IP posture. When signals conflict, the paper-plus-blog fan-out is the resolution.
- The lesson-extraction discipline is four steps: pick the internal artifact, decompose into what generalises, reframe as venue contribution, pick the one honest failure. If there is no internal artifact, there is no external artifact.
- Paper shape: 8–12 pages with abstract, intro, system, evaluation methodology, results (including negative results), discussion and limitations, related work (industry-first), conclusion. Blog shape: 2,000–5,000 words with title, lead, problem framing, system, evidence, honest failure, generalisation-bounds, what comes next, closing.
- Writing discipline (shared): every claim traces, the honest failure is load-bearing, no gratuitous proper nouns, the lesson survives compression, co-authorship is the default.
- The paper-plus-blog fan-out ships one lesson in two shapes; each artifact stands alone and cross-links the other.
- The pre-publication legal review is non-negotiable — trade-secret, customer-data, and contractual encumbrance checks. Build 2–4 weeks of lead time in from the first draft.
- Six failure modes: lesson-with-no-substrate paper, promotional-blog masquerade, paper-in-blog-clothing, blog-in-paper-clothing, solo-authored artifact, insufficient-legal-lead-time crunch.
- Chapter 4 walks the keynote craft, which the paper or blog often precedes as a *published substrate* the keynote references.
