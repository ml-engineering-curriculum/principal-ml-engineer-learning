# exercise-02: Industry-Track Paper or Applied-ML Engineering Blog — Full First Draft

**Estimated effort:** 3 hours

## Objective

Author a full first draft of one industry-track paper *or* one applied-ML engineering blog post — the specific artifact whose bet you named in `exercise-01-industry-influence-artifact-plan/fiscal-year-artifact-bets.md`. Apply chapter 3's lesson-extraction discipline, the writing discipline, and the pre-publication legal-review checklist end-to-end.

The exercise instantiates chapter 3. It is the load-bearing exercise for exercises 02-04 because the paper or blog is the *substrate* many principal-scope keynotes (exercise-03) and OSS releases (exercise-04) reference.

The 3-hour effort target reflects the *first-draft* scope, not the *submission-ready* scope. A submission-ready paper is typically 40–120 hours of authoring plus co-author revision cycles; this exercise gets you the first draft that the co-authors respond to.

## Prerequisites

- **Chapter 3 read end-to-end.** Especially the four principal-scope lesson shapes, the three paper-vs-blog signals, the four lesson-extraction steps, the shape sections, and the six failure modes.
- **Chapter 1 skim.** The venue-audience-artifact matching discipline underpins the paper-vs-blog choice.
- **Chapter 2 skim.** The internal substrate (chapter 2 § *canonical org-wide reference doc*) is what the lesson extracts from.
- **Exercise-01 completed.** The paper or blog you draft is the one in your `fiscal-year-artifact-bets.md`. If exercise-01 is not yet done, do it first — this exercise's substrate depends on it.
- **Optional: an existing internal reference doc.** If you have an internal reference doc (mod-503 chapter 5, mod-505 chapter 2 § *Class D*, mod-502 chapter 7-shape one-pager plus deep-dive) that is the substrate for the paper or blog, have it open. If you do not, either use a composite reference doc (be explicit about that) or extract from a public case study whose substrate you can cite.

## Problem statement

Pick one fiscal-year bet from `exercise-01-industry-influence-artifact-plan/fiscal-year-artifact-bets.md` whose venue class is paper *or* blog *or* paper-plus-blog. Draft the full first version of the artifact per chapter 3's shape. If your bet is a paper-plus-blog fan-out, pick *one* side to draft here (the other becomes a follow-up exercise).

Two constraints on the choice:

- The lesson must fit one of chapter 3's four principal-scope lesson shapes (architecture / cross-team eval / bet framing / FM economics). If your fiscal-year bet's lesson does not fit, either lift the lesson to fit or defer the bet.
- The internal substrate must exist (or be sketched enough that the exercise can proceed). Chapter 3's *lesson-with-no-substrate paper* failure mode is what this constraint guards against.

Produce the paper or blog as a full first-draft document, plus the pre-publication artifact bundle (author list, submission cover letter, legal-review checklist).

## Requirements

Populate a workspace directory `exercise-02-paper-or-blog/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-02-paper-or-blog/
├── README.md                    # index; which bet from exercise-01; venue and lesson
├── draft.md                     # the full paper or blog first draft
├── lesson-extraction.md         # the chapter 3 step 1–4 worked out explicitly
├── co-author-plan.md            # named co-authors, section ownership, review cycles
├── legal-review-checklist.md    # chapter 3's three checks; per-check current status
├── submission-cover-letter.md   # (paper only) the venue-specific cover letter
└── appendices/
    ├── figures-and-diagrams.md  # figure list; source (typically mod-503 chapter 5 diagrams)
    └── references-worked.md     # bibliography, industry-first
```

### `README.md` — index

Half a page. States:

- Which bet from exercise-01 this exercise instantiates. Reference `fiscal-year-artifact-bets.md` bet ID.
- The venue (specific — KDD industry track 2027, Meta Engineering blog, RecSys industry track 2027, etc.).
- The lesson in one sentence.
- Paper vs. blog (or paper-plus-blog with which side drafted here).
- The internal substrate the draft extracts from (reference to the internal doc; composite is fine, be explicit).
- The co-authors and their section ownership.

### `lesson-extraction.md` — the chapter 3 discipline worked

One page. Chapter 3 § *the lesson-extraction discipline* has four steps; this document walks each explicitly.

- **Step 1 — pick the internal artifact the lesson extracts from.** Name the internal doc; describe its current state (stable, evolving, to-be-authored).
- **Step 2 — decompose into what generalises and what does not.** Two lists: generalisable material (patterns, invariants, trade-offs, sunset criteria, numeric envelopes), and non-generalisable material (specific team names, product surfaces, proprietary edges). The generalisable list is the paper or blog's substrate; the non-generalisable list is what gets aggregated, anonymised, or cut.
- **Step 3 — reframe as venue contribution.** The paper's contribution sentence or the blog's take-away sentence. One sentence. Compressed. This is the direct source of the paper's abstract or the blog's lead paragraph.
- **Step 4 — pick the one honest failure.** Which of chapter 3 § *the honest-failure discipline* three ways (retired bet, invariant that broke, eval program that leaked). Name the failure specifically; sketch the 200–400 word treatment it gets in the draft.

### `draft.md` — the full first draft

The load-bearing document. Length target: 8–12 pages for a paper draft; 2,000–5,000 words for a blog draft.

**For a paper draft**, populate all sections from chapter 3 § *shape of the industry-track paper*:

- Abstract (150–250 words)
- Introduction (1–1.5 pages)
- System overview (1.5–2.5 pages) — include at least one figure / diagram
- Evaluation methodology (1–1.5 pages)
- Results (1–1.5 pages) — include the negative-result section
- Discussion and limitations (0.5–1 page)
- Related work (0.5–1 page) — industry-first citation
- Conclusion (0.25–0.5 page)
- References

**For a blog draft**, populate all sections from chapter 3 § *shape of the applied-ML engineering blog post*:

- Title (7–12 words)
- Lead paragraph (100–200 words)
- Problem framing (300–500 words)
- System / approach (600–1,500 words) — include diagrams and code snippets where the API surface is concrete
- Evidence (400–800 words)
- The honest failure (200–400 words)
- What generalises and what does not (200–400 words)
- What comes next (100–200 words)
- Closing / call to action (50–150 words)

**Shared discipline** across both — chapter 3 § *writing discipline*:

- Every claim traces to a chapter, an internal doc, or a public source.
- The honest failure section is drafted.
- No proper nouns unless load-bearing.
- The lesson survives compression to abstract or lead-paragraph length.

### `co-author-plan.md` — chapter 2 co-authorship discipline applied

Half a page. Shape:

- **Named co-authors.** 1–3 named individuals (or roles if composite), by section ownership. Each co-author owns at least one section of the draft.
- **Review cycles.** The internal-review cycle (2–3 rounds), the co-author revision cycle (2–3 rounds), and the pre-submission full-draft review with a peer principal (1 round). Dates or milestones per round.
- **Byline order and attribution.** Who is first author, why. Chapter 2 § *co-authorship as internal-community leverage* is the reference; single-authored principal papers are a failure mode.
- **Section-level attributions.** Which co-author wrote or is primary reviewer on which section.

### `legal-review-checklist.md` — chapter 3 pre-publication

Half a page. Chapter 3 § *the pre-publication legal review* has three checks; this document runs each.

- **Trade-secret disclosure check.** Which specific paragraphs, figures, or numeric claims potentially disclose proprietary process. Current status: cleared / needs revision / needs escalation.
- **Customer-data disclosure check.** Which specific paragraphs, figures, or numeric claims potentially disclose customer data or customer-specific behaviour. Current status.
- **Contractual encumbrance check.** Which foundation-model provider contracts, vendor contracts, or partner contracts potentially constrain the draft's claims. Current status.

Plus:

- **Legal-review lead-time plan.** 2–4 weeks pre-submission (paper) or 2–4 weeks pre-publication (blog). Names the legal counsel or the review body.

### `submission-cover-letter.md` (paper only) — the venue-specific letter

Half a page. Some venues require it, some do not; even where not required, drafting the cover letter helps clarify the submission's fit with the venue. Shape:

- **Venue-fit statement.** Why this venue is the right home for this paper. Cites the venue's charter and the paper's contribution together.
- **Reviewers to exclude (if permitted).** Named individuals with a conflict of interest.
- **Related prior work by the same authors.** If any (including the paired blog post per chapter 3 § *the paper-plus-blog fan-out*).

### `appendices/figures-and-diagrams.md`

List of figures in the draft. For each figure: source (typically mod-503 chapter 5 living diagrams, redacted for proprietary specifics), caption, whether it is already publication-ready or requires redaction and re-authoring.

### `appendices/references-worked.md`

The draft's bibliography. Chapter 3 § *related work* names the discipline: industry-first citation. The bibliography should be roughly 60/40 industry-to-academic; if it inverts to 90% academic, the venue-audience-artifact match is wrong.

## Starter guidance

- **Do not skip the lesson-extraction pass.** The `lesson-extraction.md` document is not an afterthought; it is what makes the draft's discipline visible. A draft written without the extraction pass will drift back into the internal doc's specifics and will need to be rewritten anyway.
- **Draft the abstract or lead paragraph first.** The compressed form is the leverage point. If you cannot write it, the draft is not yet ready — the lesson is not stable, or the substrate is missing, or the honest failure is not yet named.
- **Include the honest failure in the first draft.** Not as a late edit. Chapter 3 § *the honest-failure discipline* is what separates principal-scope external content from promotional content; treat it as load-bearing from the first outline.
- **Cite industry work heavily.** The related-work section of a first-draft principal-scope paper should have at least 8–15 industry-scope citations (peer papers, peer blogs, peer OSS release docs, peer standards contributions) alongside the academic references. If your bibliography has 3 industry citations and 30 academic, you are drafting an academic paper; revisit chapter 1's venue selection.
- **Redact figures early.** The mod-503 chapter 5 living diagrams are proprietary in their internal form. Chapter 3 requires them to be redacted for proprietary specifics before external publication. Do the redaction pass on figures before showing the draft to co-authors — cleaner drafts get better reviews.
- **Do not exceed the length target.** A first-draft paper at 15 pages is a paper the PC will ask you to cut. A first-draft blog at 7,000 words is a paper in blog clothing (chapter 3 failure mode 3). Cut in the first draft; do not defer.
- **Name the co-authors before the first draft.** Chapter 2 § *co-authorship*. The co-authors are named at bet time (exercise-01); their section ownership is set at draft time (this exercise). Solo-authored drafts do not get co-authors added later.
- **Legal review lead-time is real.** Chapter 3 failure mode 6 (insufficient legal lead time) is the modal crunch. Even for this exercise's first-draft output, note the review calendar; a first draft submitted to legal 5 days before the venue deadline is a first draft that goes late.
- **Time-box each section.** README + lesson-extraction: 20 minutes. Draft: 90–120 minutes (the load-bearing section). Co-author plan: 10 minutes. Legal-review checklist: 10 minutes. Cover letter + appendices: 20 minutes. Total ~2.5–3 hours.

## Acceptance criteria

The exercise is done when:

- [ ] `README.md` names the exercise-01 bet, the specific venue, the one-sentence lesson, and the paper vs. blog choice.
- [ ] `lesson-extraction.md` walks all four chapter 3 steps explicitly, with the two decomposition lists (generalisable / non-generalisable) filled in.
- [ ] `draft.md` populates every section from the applicable shape (paper or blog).
- [ ] The abstract (paper) or lead paragraph (blog) is drafted and compresses the lesson to the target length.
- [ ] The draft includes an honest-failure section drafted at appropriate length (200–400 words), not a hedge or a promotional-tone qualifier.
- [ ] Every claim in the draft traces to a chapter, an internal doc, or a public source. No unattributed numeric claims.
- [ ] The draft has no gratuitous proper nouns. Product names and team names appear only where they carry information the reader needs.
- [ ] The draft's length is within the chapter 3 target range (8–12 pages for paper, 2,000–5,000 words for blog).
- [ ] `co-author-plan.md` names at least one co-author who is not the principal, with section ownership assigned. Not a solo-authored draft.
- [ ] `legal-review-checklist.md` runs all three chapter 3 checks with per-check current status.
- [ ] `submission-cover-letter.md` (if paper) states venue-fit in the venue's own charter language.
- [ ] The bibliography (`appendices/references-worked.md`) is at least 40% industry citations; not overwhelmingly academic.
- [ ] Figures are listed (`appendices/figures-and-diagrams.md`) with redaction status per figure.
- [ ] The draft passes the *chapter-3-failure-mode audit*: none of the six failure modes (lesson-with-no-substrate, promotional-blog masquerade, paper-in-blog-clothing, blog-in-paper-clothing, solo-authored artifact, insufficient-legal-lead-time crunch) are visible.
- [ ] The draft passes the *hand-off test*: a co-author reading `README.md`, `lesson-extraction.md`, and `draft.md` can hold the next revision cycle without your walkthrough.

## Stretch goals

- **Draft the paired artifact.** If your fiscal-year bet is paper-plus-blog fan-out, this exercise drafts one side. The stretch is to draft the second side (typically the blog if the paper was the primary, and vice-versa) using the same substrate. Cross-linking discipline (chapter 3 § *the paper-plus-blog fan-out*) applies.
- **Run the co-author round zero.** Send the first draft to one of the named co-authors and get feedback. Revise once. Add a `revision-notes.md` file capturing what the co-author flagged and what changed. The revision cycle is what turns first drafts into submission-ready drafts.
- **Run the pre-flight peer-principal review.** Send the draft to a peer principal at another org (real or composite) and get a 30-minute review conversation. Capture the peer's read of the lesson-sentence, the honest failure, and the generalisation-bounds. Note what shifted in the draft after the review.
- **Draft the *rejection* response.** If the paper draft is submitted and (as is common) desk-rejected or rejected on first review, draft the revision plan: which reviewer comment goes where in the next revision, which comments are declined and why. Rejections are part of the industry-track submission cycle; the revision discipline is what separates first-cycle from experienced authors.
- **Draft the accompanying *keynote through-line*.** Chapter 4 § *the through-line*. Take the paper's abstract or the blog's lead paragraph and compress it further into a 20–40 word through-line that could be delivered spoken. This is the *seed* for exercise-03 if the same substrate becomes a keynote.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-02-paper-or-blog/` extends across the module: exercise-03's keynote through-line can extract from this exercise's draft; exercise-04's release proposal can cite this exercise's paper as the accompanying published substrate; the tracking dashboard in exercise-01 gets a new row populated by this exercise's target return signals.
