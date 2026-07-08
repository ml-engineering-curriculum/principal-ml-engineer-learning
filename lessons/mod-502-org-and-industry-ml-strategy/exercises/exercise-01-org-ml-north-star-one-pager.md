# exercise-01: Org ML North Star One-Pager

**Estimated effort:** 3 hours

## Objective

Author the executive-audience one-pager for an ML function's multi-year technical North Star, following the shape in chapter 7. The one-pager pairs with the deep-dive companion doc (exercise-03 builds the sequencing / non-goals / sunsets layer of the deep-dive; this exercise's output is the single-page executive artifact and, together with exercise-03, forms the pair a CTO / SVP would ratify).

## Prerequisites

- Chapters 1 and 2 read; the working definition of a North Star and the five-row bet portfolio are already familiar.
- Chapter 7 skimmed for the one-pager's six-section shape and the writing discipline.
- A working editor (any). No code required.
- An org context to write against — either your current employer or a public reference org whose ML function you know well enough to construct a defensible portfolio (Pinterest, SoundCloud, Instacart, Upstart, DoorDash, Ibotta, Capital One, Bumble, Airbnb, and the peer platform-side sample orgs are all fine choices; pick one you can defend concrete claims about).

## Problem statement

You have been asked by the CTO of the org you are writing for to author the one-page ML technical North Star for the next 3-to-5 years. The CTO plans to circulate the page to the SVPs of Product and Engineering, to the peer VP of AI Infrastructure, and to the Head of AI Governance for ratification. Later this quarter they will quote it verbatim in a board meeting.

The one-pager is *not* the whole North Star document — it is the executive-audience half of a paired artifact (chapter 7). It has to stand alone on its own page and be quotable in five minutes. Everything that does not fit lives in the deep-dive companion doc (exercises 02, 03, and 04 populate that companion's key sections).

## Requirements

Produce a single markdown file, `exercise-01-one-pager.md`, in a personal workspace (do not commit into this curriculum repo — this is a per-learner artifact). Structure it exactly as follows.

- **A single H1 title** naming the artifact ("<Org> ML Technical North Star (FY26–FY30) — Executive One-Pager" or similar).
- **A named target org.** Real (your employer or a public reference org) or a *plausibly-real synthesis* clearly labelled as such; not fictional. Your one-pager should be one that a real CTO of that org could conceivably ratify.
- **The six named sections from chapter 7**, in order and named:
  1. Direction (2–3 sentences).
  2. Bet portfolio (5 bullets — one per chapter-2 row, in order: Gen-AI direction; RecSys / personalization direction; agentic-AI direction; foundation-model program direction; MLOps as org contract).
  3. Non-goals (3–5 bullets).
  4. Signal watch (2–3 bullets).
  5. What we ask of leadership (3 bullets).
  6. Refresh cadence (1 sentence).
- **A one-page hard cap.** If you were to render your markdown as printed A4 / US-letter with reasonable font, it would fit on one page. Cut, don't shrink font.
- **A five-minute-readability self-test.** After drafting, walk away for at least 15 minutes, come back, and time yourself reading it aloud. If you cannot read it aloud with comprehension in five minutes, revise until you can.
- **A quotable direction sentence.** The first sentence of the Direction section should be quotable on its own, without loss of meaning, and short enough to fit in a board-meeting quote. Rewrite this sentence more than any other.

## Starter guidance

- Draft the *direction sentence* first, and rewrite it until it survives a peer's reading unassisted. Everything else on the page defends that sentence. If the sentence is not right, no amount of polish on the other sections will save the page.
- For the bet portfolio bullets, use the shape *"Bet name — one-clause posture — one-clause year-1 state (bet / hedge / option / not-in-window)."* Nothing more per bullet on the one-pager. If a bullet needs a supporting clause, that clause belongs in the deep-dive.
- For the non-goals, select 3–5 across the portfolio — don't try to enumerate the full non-goal set from chapter 4. Choose the ones the CTO most needs in mind when defending the direction to their peers.
- For the signal watch, pick 2–3 material shifts from chapter 6's categories — one is often a regulatory / EU AI Act obligation, one is often a cost / compute-generation shift, one is often a frontier-lab publication. Choose the ones most likely to matter in the next six months.
- For what-we-ask-of-leadership, be concrete. "Alignment" and "support" are not asks; a capacity envelope, a hiring shape, a partnership commitment, a review touchpoint are asks.
- Do not use numeric OKR-style percentage targets on the one-pager. They read as false precision to an executive and belong in the deep-dive companion doc.
- Do not use ML-engineering jargon a CTO would not know without asking. If a term needs a definition, either define it in-line or replace it with plainer language.
- Watch for the drift from *direction* to *summary of the year-1 roadmap*. The one-pager commits leadership to multi-year direction, not to the current fiscal year's execution. Chapter 5 is the reference for the seam.
- If you find yourself writing per-team named commitments, cut them. Team assignments belong in the portfolio roadmap, which staff owns.

## Acceptance criteria

Your document is done when it can pass all of the following:

- [ ] The document is one page under reasonable print rendering.
- [ ] All six named sections present, in order, correctly labelled.
- [ ] The direction sentence is quotable on its own; a peer can read it aloud and it makes sense without the rest of the page.
- [ ] The bet portfolio has exactly five bullets, in the chapter-2 row order, each with a named posture and a named year-1 state (bet / hedge / option / not-in-window).
- [ ] The non-goals section names 3–5 concrete refusals with named consequences, not vibes.
- [ ] The signal watch section names 2–3 specific signals across at least two of chapter 6's four categories.
- [ ] The what-we-ask-of-leadership section names three concrete asks — envelope, shape, or commitment — not "alignment" or "support".
- [ ] The refresh cadence is stated in one sentence, including the emergency-refresh trigger.
- [ ] Nowhere on the page do fiscal-quarter delivery dates, per-team owners, or numeric OKR percentage targets appear.
- [ ] The document reads aloud in five minutes with comprehension.

## Stretch goals

- **Adversarial CTO review.** Ask a peer to play the ratifying CTO and ask three challenge questions: (1) *"Which non-goal are you most likely to relax under pressure?"* (2) *"Which bet do you privately think is a hedge that you have written as a bet?"* (3) *"Which signal in your watch section would actually shift you in the next six months?"* Revise the one-pager based on the pressure test.
- **Two-org comparison.** Author a *second* one-pager for a materially different org (a consumer-recommendations-heavy shape vs an enterprise-fintech shape — chapter 3's two worked example grids are a starting point). Compare the two direction sentences and non-goal sets. What survives across the two, and what is the org-specific bet in each?
- **Pair with an exercise-03 draft.** Draft the sequencing / non-goals / sunsets layer (exercise-03) and pressure-test the one-pager against it: does the one-pager's five-bullet portfolio match the exercise-03 sequencing? Does every non-goal on the one-pager appear in the deep-dive's full non-goal register?

## Deliverable location

Local workspace. Do not commit into this curriculum repo — this is a per-learner artifact. When exercise-03 is complete, pair the one-pager with the deep-dive draft; the pair is the deliverable exercise-01 and exercise-03 combine to.
