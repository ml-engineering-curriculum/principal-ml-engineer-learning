# exercise-02: Distinguished vs Principal vs Senior Principal Title Map

**Estimated effort:** 2 hours

## Objective

Build a personal, employer-by-employer title map that tells you which title stack a given employer runs and which posted rung sits at which scope. The map is a working reference you consult every time you consider or triage a Principal / Distinguished ML posting. It also feeds mod-505's target-employer research for hiring-loop calibration later.

## Prerequisites

- Chapter 3 (`03-title-map-distinguished-principal-senior-principal.md`) read.
- Some familiarity with the 26-posting sample and the ability to browse employer careers pages for adjacent titled rungs.

## Problem statement

Employers use one of (at least) three title stacks: single-rung Principal, two-rung Principal → Sr. Principal, or Distinguished → Sr. Distinguished. The word on the door does not carry the level; the object of the load-bearing verbs does. You are going to build the employer-by-employer map that lets you spot the stack on sight.

Concretely:

1. For at least 8 employers from the 2026-Q2 sample (see [`../../../JOB_REQUIREMENTS.md`](../../../JOB_REQUIREMENTS.md)), identify which title stack the employer runs.
2. For each rung the employer posts (Staff, Principal, Sr. Principal, Distinguished, Sr. Distinguished, or whatever the employer uses), name the load-bearing verb-object altitude of a representative posting.
3. Cross-employer, note where the same word (e.g., "Principal") points at different scopes and where different words (e.g., "Distinguished" at Capital One vs. "Senior Principal" at SoundCloud) point at the same scope.

## Requirements

Produce a single markdown file, `exercise-02-title-map.md`, in a personal workspace. Structure it as follows.

- **At least 8 employers.** Include:
  - At least one employer running the single-rung stack (Pinterest, Bumble, Upstart, Ibotta, GoodRx are all fine picks).
  - At least one employer running the two-rung stack (SoundCloud is the clearest 2026-Q2 example).
  - Capital One (the Distinguished stack — audit at least two Capital One postings from the sample, spread across `Distinguished` and `Sr. Distinguished`).
  - At least one AI-native or scientific employer (Lila Sciences, Headspace, PhysicsX).
  - At least one enterprise / SaaS employer (Twilio, Wiser Solutions, Palo Alto Networks).
- **Per employer, produce four fields:**
  1. **Stack** — `single-rung`, `two-rung`, `Distinguished`, or `other` (explain).
  2. **Rungs posted** — the actual title stack visible on the employer's careers page or in the sample. Include Staff if visible, so you have the level-40 anchor.
  3. **Rung-to-scope table** — a mini table of `rung -> load-bearing verb-object altitude`. Use the vocabulary from chapter 1. Cite one representative sentence per rung.
  4. **Compensation top-of-band (if published)** — corroborating datapoint. Sample-level pubs: Pinterest $480K, Snap $414K, Capital One Sr. Distinguished (Remote-Eligible) $392K, Lila Sciences $374K, Headspace $258.7K (high-cost region). If the employer does not publish, mark as `unpublished`.
- **A cross-employer comparison section at the end** answering three questions:
  1. Which employers use the same word ("Principal") to name meaningfully different scopes? Give the pair-wise contrast in one sentence each.
  2. Which employers use different words to name the same scope? Give the pair-wise contrast in one sentence each.
  3. If you had to advise a candidate on "am I ready for the `Principal` rung at Employer A vs the `Sr. Distinguished` rung at Capital One?", which chapter-1 verb-object altitudes would you use to answer? Sketch the answer in a paragraph.

## Starter guidance

- Start with Capital One. Their Distinguished-title program is well-defined and the five Capital One postings in the sample collectively run the whole principal-scope playbook.
- For each employer, look for at least one *adjacent* rung on the employer's careers page — the Staff rung beneath and, if it exists, the Fellow rung above. The adjacent rungs anchor the map. If you can't find them, note the absence.
- The word "Senior" is treacherous. `Senior Principal` at SoundCloud names a new rung; `Sr. Machine Learning Engineer` at many employers just names a `Senior` (L30) engineer at the top of their time-in-rung band. Read the load-bearing sentences, not the title.
- If an employer has no public JD for a rung but you know the rung exists (from employees on the engineering blog, from talks, from public promotions posts), you can still put the rung in the table — mark it as `internal-only rung` and note your source.
- Do not try to force employers into a single ranked table. The stacks are not directly comparable across employers — Snap L7 is not the same as Capital One Distinguished which is not the same as SoundCloud Senior Principal. Use the objects, not the numbers or the words.

## Acceptance criteria

Your document is done when it can pass all of the following:

- [ ] At least 8 employers, spread across at least three of the four sample segments (fintech/distinguished, consumer/recsys, enterprise/SaaS, AI-native/scientific).
- [ ] Capital One included with at least one `Distinguished` and one `Sr. Distinguished` posting audited.
- [ ] At least one two-rung-stack employer included (SoundCloud fine).
- [ ] Every employer has a stack classification, a rungs-posted list, and a rung-to-scope table.
- [ ] Every rung-to-scope table cites at least one verbatim load-bearing sentence per rung.
- [ ] Published compensation top-of-band recorded where available; unpublished marked.
- [ ] The cross-employer comparison section answers the three questions.
- [ ] Where the same title word (`Principal`) points at different scopes across employers, the contrast is stated as a verb-object altitude difference, not as an adjective preference.

## Stretch goals

- **Add a Fellow-rung row.** For any employer whose engineering ladder is publicly documented (Snap, Meta, Google, Stripe, LinkedIn, Netflix), fill in the Fellow / Senior Fellow rung the sample does not cover. Mark it as `above this track's altitude` and note the closest reference (Larson's *Staff Engineer*, StaffEng.com).
- **Add an executive-branch row per employer.** For each of your 8 employers, if you can find the peer executive title (Head of AI, VP of ML, CAIO), name it and note the scope difference from the same employer's Principal / Distinguished rung. This is the boundary chapter 4 draws — applying it employer-by-employer sharpens the classification.
- **Second-source the compensation top-of-band.** For at least three employers, corroborate the sample's published top-of-band from a public secondary source (levels.fyi, published state-mandated ranges, employer JD text) and note discrepancies. This is not the focus of the exercise; treat it as a nice-to-have.

## Deliverable location

Local workspace. Do not commit into this curriculum repo. Cite the file when you produce the exercise-04 self-assessment, and re-consult it every time you're considering a specific Principal / Distinguished ML posting.
