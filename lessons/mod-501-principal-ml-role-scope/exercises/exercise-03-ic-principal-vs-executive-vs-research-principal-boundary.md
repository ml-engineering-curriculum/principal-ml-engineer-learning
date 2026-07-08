# exercise-03: IC-Principal vs Executive vs Research-Principal Boundary

**Estimated effort:** 2 hours

## Objective

Practice the three-family classification from chapter 4 on a mixed batch of postings — Family 1 (IC-principal, this track), Family 2 (executive branch, peer tracks `chief-ai-officer-learning` / `head-of-ai-governance-learning`), and Family 3 (research-principal, no owner in this ecosystem). The output is a classification table and a short reflection on the two hybrids from the batch.

## Prerequisites

- Chapter 4 read.
- Chapters 1 and 2 already worked through in exercise-01.
- Access to careers pages beyond the 26-posting sample — because the sample is Family-1 by construction, this exercise deliberately pulls postings from all three families.

## Problem statement

A learner at Family 1 needs to hold the boundary from both sides. From the inside: recognise when a posting titled "Principal ML Engineer" is actually asking for Family 2 (executive) or Family 3 (research). From the outside: recognise when a posting titled "Head of AI" or "Principal Research Scientist" is on a neighbouring ladder and *not* the target for this track. The chapter-4 three-step classification is how you decide.

You are going to run the classification on 9 postings — 3 from each family — and document your classification with the specific signals from chapter 4's steps. At least two of the 9 must be hybrids where the classification isn't clean; you'll write those up separately.

## Requirements

Produce a single markdown file, `exercise-03-family-classification.md`, in a personal workspace. Structure it as follows.

- **Batch composition — 9 postings total, minimum:**
  - **3 Family-1 postings** — IC-principal ML engineer. Any 3 from the 2026-Q2 sample in [`../../../JOB_REQUIREMENTS.md`](../../../JOB_REQUIREMENTS.md) that you did *not* audit in exercise-01. (Pick fresh so you're re-exercising the classification, not the specific vocabulary you already have.)
  - **3 Family-2 postings** — executive-branch. Titles like `Head of AI`, `VP of ML`, `VP of AI Engineering`, `Chief AI Officer`, `Chief ML Officer`, `SVP of AI`. Any 3 you can find live on Greenhouse / Lever / Ashby / LinkedIn or on the employer's careers page. At least one must be a Head-of-AI / CAIO title. If any are difficult to find live, use the peer tracks' evidence files (`chief-ai-officer-learning/JOB_REQUIREMENTS.md`, `head-of-ai-governance-learning/JOB_REQUIREMENTS.md`) as your source; note whichever source you used.
  - **3 Family-3 postings** — research-principal. Titles like `Principal Research Scientist`, `Distinguished Applied Scientist`, `Principal Applied Scientist`, `Senior Research Scientist`. Any 3 from Anthropic, OpenAI, DeepMind, Google Research, Google DeepMind, Meta AI, Microsoft Research, Apple ML Research, or an AI lab careers page.
- **Per posting, produce five sections:**
  1. **Title, employer, date pulled, and source.**
  2. **Step-1 tally** — count direct-reports / budget / headcount / board-reporting signals. Quote the specific bullets. Report 0, 1–2, or 3+ (using chapter 4's brackets).
  3. **Step-2 tally** — count state-of-the-art / publication / research-agenda signals. Quote the specific bullets. Report 0, 1–2, or 3+.
  4. **Step-3 verification** — if steps 1 and 2 both fail (both zero or near-zero), run the chapter-2 principal-scope theme scan on the top 5–10 bullets and report which themes are cited.
  5. **Classification** — Family 1, Family 2, Family 3, or `hybrid Family-N/Family-M` (name the dominant one). One-sentence reasoning citing the tallies.
- **Two hybrid write-ups.** At least two of your 9 postings should end up classified as hybrids or be non-obvious cases. For each, write a two-paragraph note:
  - First paragraph: why the classification isn't clean. Which family's signals dominate, which are secondary. Where the tie could plausibly break.
  - Second paragraph: which track this learner (you) would layer *if* pursuing this posting. E.g., if it's a Family-1 posting that grew a small team (chapter 4's Hybrid A), the answer might be "still this track, but partner with `chief-ai-officer-learning` for the small-team management basics".

## Starter guidance

- The signal-density brackets from chapter 4 (0 / 1–2 / 3+) are approximations, not laws. Trust the tally when the counts are extreme; use judgement when they're close to the bracket lines.
- For Family-3 postings, watch for the *"PhD required"* qualifier — necessary but not sufficient (Instacart Principal ML Engineer also requires a PhD and is Family 1). The clearer Family-3 tell is the research-agenda verbs.
- For Family-2 postings that read technical (a technical VP hiring for their own successor, or a Head-of-AI who came from an IC-principal background), watch chapter 4's Hybrid-B — the technical bullets are usually aspirational; the actual role scope is Family 2.
- Do not classify based on the compensation number. A Family-3 Principal Research Scientist at a frontier lab may out-earn a Family-1 Distinguished Engineer at Capital One; the number is a corroborating signal only.
- If you cannot fetch a Family-2 or Family-3 posting live, you may draw from the *`JOB_REQUIREMENTS.md`* files in the peer tracks (`chief-ai-officer-learning`, `head-of-ai-governance-learning`) as your source, provided you cite it. The classification exercise is what matters, not the freshness of the posting.

## Acceptance criteria

Your document is done when it can pass all of the following:

- [ ] 9 postings total, 3 per family.
- [ ] Every posting has a source (URL, employer name, and date pulled — or a citation to a peer-track evidence file if live-fetch was blocked).
- [ ] Every posting has step-1 and step-2 tallies with quoted bullets.
- [ ] Every posting has a classification and one-sentence reasoning.
- [ ] At least two hybrid write-ups completed, each two paragraphs.
- [ ] The 3 Family-1 postings are distinct from the ones audited in exercise-01.
- [ ] At least one of the 3 Family-2 postings is titled `Head of AI` or `Chief AI Officer` (Vice Presidents of ML also count if the reporting chain reads as executive).
- [ ] The Family-3 postings are drawn from at least two different AI labs.

## Stretch goals

- **Trajectory annotation.** For each Family-1 posting in the batch, name the plausible trajectory chapter 4 identifies (`stay Family 1 / slide Family 2 / slide platform-side principal / slide Family 3`). Which trajectory does the posting itself seem to bend toward (based on the surrounding responsibilities and preferred qualifications)?
- **Employer overlap.** Pick one employer that runs postings in more than one of the three families (Meta, Google, and Apple all do this — plus some AI labs run separate engineering and research ladders). For that employer, sketch the level-48+ landscape as a single small diagram or table: which titles map to which families, which ladders are marketed as promotable-into-each-other, where the boundary is enforced.
- **Family-3 sampling for the ecosystem.** If you have time, note down the shape of the 3 Family-3 postings — verbs, objects, publication expectations, tenure floors, PhD scaffolding. The ecosystem's `JOB_REQUIREMENTS.md` for this track has an open `needs-research` flag on whether Principal Research Scientist / Applied Scientist needs its own owner role; a small structured sample is helpful evidence.

## Deliverable location

Local workspace. Do not commit into this curriculum repo. Keep the artifact alongside exercise-01 and exercise-02 as your growing "how I read a posting" reference.
