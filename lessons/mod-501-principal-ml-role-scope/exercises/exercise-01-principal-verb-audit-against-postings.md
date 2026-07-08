# exercise-01: Principal Verb Audit Against Postings

**Estimated effort:** 2 hours

## Objective

Apply the verb-and-object vocabulary from chapter 1 and the reading protocol from chapter 2 to a small batch of real principal-scope postings, and produce a per-posting *verb audit* that separates the principal-defining sentences from the staff-scope leftover and the executive-branch leakage. The output is a short markdown document you carry forward and cite in exercise-04 and in the mod-504 executive-audience work later.

## Prerequisites

- Chapters 1 and 2 of this module read.
- Familiarity with the 26-posting sample in [`../../../JOB_REQUIREMENTS.md`](../../../JOB_REQUIREMENTS.md).
- A working editor (any). No code required.

## Problem statement

Compensation committees and hiring managers don't read a Principal / Distinguished ML posting the way a candidate does. They read the load-bearing sentences and let the rest wash over them. You are going to practice doing the same on real postings, then produce an artifact that shows you can:

1. Extract the 3–6 load-bearing sentences per posting.
2. Attribute each load-bearing sentence to a specific principal-scope theme (theme 1 org-industry strategy, theme 2 north-star architecture, theme 3 cross-org influence, theme 4 mentorship + technical bar, or theme 5 industry influence).
3. Flag staff-scope leftover (bullets that describe genuine ML-engineering work at portfolio scope, owned by `staff-ml-engineer-learning`).
4. Flag executive-branch leakage or research-track leakage (direct reports, budget, headcount, first-author publications, state-of-the-art benchmarks).
5. Reach a per-posting classification: **clean principal-scope**, **hybrid** (with the direction of the hybrid noted), or **mismarketed** (staff or exec dressed as principal).

## Requirements

Produce a single markdown file, `exercise-01-verb-audit.md`, in a personal workspace (do not commit into this curriculum repo). Structure it as follows.

- **At least 5 postings audited.** Pick them from the sample in [`../../../JOB_REQUIREMENTS.md`](../../../JOB_REQUIREMENTS.md), spread across the four segments (fintech / distinguished, consumer / recsys, enterprise / SaaS, AI-native). At least one posting must be a Capital One Distinguished- or Sr.-Distinguished-titled role so you exercise the Distinguished-stack vocabulary from chapter 3. At least one posting must be a Family-1-adjacent hybrid — one that mixes IC-principal signals with a hint of executive-branch signals (Bumble's *"without direct authority"* sentence is a helpful reference for what a *clean* IC-principal posting reads like; look for a posting that is less clean).
- **Per posting, produce five sections:**
  1. **Load-bearing sentences** — 3 to 6 verbatim quotes from the posting. Reject adjectives-only sentences. Keep sentences with verbs and objects.
  2. **Theme attribution** — for each load-bearing sentence, name the theme from chapter 5 (theme 1–5). If a sentence spans two themes, name both and note which is dominant.
  3. **Staff-scope leftover** — bullets that describe portfolio-scope work owned by `staff-ml-engineer-learning`. Verbatim quotes. Note which staff-scope module owns each (see [`../../mod-501-principal-ml-role-scope/06-handoff-contracts-to-staff-scope.md`](../06-handoff-contracts-to-staff-scope.md) for the seam map, or cross-check with `staff-ml-engineer-learning`'s module list).
  4. **Executive / research-track leakage** — bullets with direct-reports, budget, headcount, first-author publication, or state-of-the-art benchmark signals. Verbatim quotes. Name which peer track owns them (chapter 4).
  5. **Verdict** — one paragraph. Which of `clean principal-scope`, `hybrid Family-1/Family-2`, `hybrid Family-1/Family-3`, `mismarketed staff`, `mismarketed executive`, `mismarketed research` best fits, and why. Cite the verb-and-object altitudes from chapter 1 as your reasoning.
- **A cross-posting summary section at the end.** Which principal-scope themes appear most often in your batch? Which appear least often? Does the pattern match the ≥0.60 in-window frequencies from [`../../../JOB_REQUIREMENTS.md`](../../../JOB_REQUIREMENTS.md)? If your batch skews away from the sample-level frequencies (small-N noise is normal), name that.

## Starter guidance

- Start with the SoundCloud posting — it has the cleanest single load-bearing sentence in the sample (chapter 2 walks through it) and gives you a template.
- For the Capital One Distinguished pick, decide up front whether you want a `Distinguished` or a `Sr. Distinguished` posting. The two rungs surface different load-bearing sentences and are worth compare-and-contrasting.
- Do not audit more than 8 postings in this pass. The goal is *sharpness on a small batch*, not exhaustiveness. Diminishing returns hit fast; exercise-02 and exercise-04 revisit the sample.
- If a posting has already been de-linked or moved off the employer's careers page, use the description captured in the sample metadata (`.aicg/job-requirements.json`) if available. Do not audit a posting you cannot read.
- Refuse to include a bullet in the load-bearing set unless it has a *verb* and an *object at principal altitude*. Adjective-heavy sentences ("strategic", "innovative", "cutting-edge") without a concrete object are noise.
- Watch for the case where the load-bearing sentences and the surrounding bullets disagree in altitude — that is a data point about the posting (chapter 2's failure modes), not a flaw in your reading.

## Acceptance criteria

Your document is done when it can pass all of the following:

- [ ] At least 5 postings audited, spread across at least three of the four sample segments.
- [ ] At least one Capital One Distinguished- or Sr.-Distinguished-titled posting included.
- [ ] Every load-bearing sentence is a verbatim quote (or a very tight paraphrase with the original noted alongside).
- [ ] Every load-bearing sentence is attributed to at least one of the five principal-scope themes.
- [ ] Every posting has at least one staff-scope leftover bullet or is explicitly noted as having none.
- [ ] Every posting has at least one executive / research leakage bullet or is explicitly noted as having none.
- [ ] Every posting has a verdict paragraph that cites the verb-and-object altitude, not the adjective density.
- [ ] The cross-posting summary compares your batch's theme distribution to the ≥0.60 sample-level frequencies.

## Stretch goals

- **Second-pass compare.** Have a peer, mentor, or the paired solutions repo audit the same postings; compare load-bearing-sentence extraction. Do you and they identify the same sentences? If not, whose reading is closer to the verb-and-object altitude?
- **Employer-family aggregation.** Aggregate the load-bearing sentences across all five (or more) postings you audited into a single table by theme. Which theme has the most variety across employers? Which is the most stereotyped?
- **Extend to a non-sample posting.** Find a currently-live Principal / Distinguished ML posting *outside* the 2026-Q2 sample window and audit it the same way. Which theme frequencies survive the extension? Which don't? Note whether the pattern seems stable — this is the exact input the `2026-10-08` re-sample cycle uses.

## Deliverable location

Local workspace. Do not commit into this curriculum repo — this is a per-learner artifact. Cite the file when you produce the exercise-04 self-assessment; the two artifacts pair.
