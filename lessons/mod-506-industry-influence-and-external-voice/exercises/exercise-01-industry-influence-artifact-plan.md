# exercise-01: Industry Influence Artifact Plan

**Estimated effort:** 2 hours

## Objective

Author the fiscal-year industry-influence artifact plan (chapter 1's venue-audience-artifact discipline, chapter 2's internal-first ratio, and chapter 6's tracking dashboard, in one document) for the next 12 months. This is the *plan* against which exercises 02, 03, and 04 produce specific artifacts. In a real principal seat this plan is authored, reviewed with the engineering director and CFO, and revised quarterly.

The exercise instantiates chapters 1, 2, and 6 together. It comes first in the module's exercise sequence because the plan is the *tracking substrate* the subsequent per-artifact exercises operate against.

## Prerequisites

- **Chapter 1 read end-to-end.** Especially the four venue classes, the venue-audience-artifact matching discipline (the four steps), and the six venue-selection failure modes.
- **Chapter 2 read end-to-end.** Especially the three internal artifact classes, the 70/30 internal-first ratio, and the co-authorship discipline.
- **Chapter 6 read end-to-end.** Especially the three return signals, the tracking-dashboard shape, the calendar-shape check, and the four retirement triggers.
- **Mod-505 chapter 6 § *quarterly review* skimmed.** The mod-505 personal-cadence artifact is the parent structure the plan's tracking dashboard slots into.
- **Optional: your org's actual current external presence.** If you have shipped external artifacts before (papers, blogs, keynotes, open-source releases), have the list handy. If not, use a composite based on a peer principal in your industry whose work you have followed.

## Problem statement

You are a principal ML engineer at an ML org of roughly 100–500 engineers with 3–5 product areas. It is Q4; the next fiscal year begins in ~10 weeks. Author the fiscal-year artifact plan that fixes:

- The *current-state* external-influence portfolio (baseline).
- The *fiscal-year* artifact bets (one plan per artifact — venue, lesson, co-authors, cadence, expected return signal).
- The *internal-first substrate* the fiscal-year external artifacts depend on (the internal talks, tech-radar entries, canonical reference docs that must precede or accompany each external artifact).
- The *quarterly tracking dashboard* the plan is measured against, pre-populated with baseline rows.
- The *retirement candidates* — external artifacts currently in the portfolio whose retirement criteria have fired or are about to fire.

The plan is a *working document*, not a manifesto. It should be revised at each quarterly review; the exercise's output is the initial version.

## Requirements

Populate a workspace directory `exercise-01-industry-influence-artifact-plan/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-01-industry-influence-artifact-plan/
├── README.md                             # index; principal context; fiscal-year framing
├── baseline-portfolio.md                 # current-state — what has shipped, what is active
├── fiscal-year-artifact-bets.md          # 4–8 fiscal-year bets, one per artifact
├── internal-first-substrate.md           # the internal artifacts required by the external bets
├── tracking-dashboard.md                 # chapter 6's dashboard, pre-populated
├── retirement-candidates.md              # current-portfolio artifacts to retire
└── appendices/
    ├── venue-map.md                      # the specific venues considered per bet
    └── calendar-shape-check.md           # this-quarter's ratio check + rebalancing signals
```

### `README.md` — index and principal context

Half a page. States:

- The principal's org context (rough size, product areas, technical stack at high level). One paragraph, composite is fine.
- The current fiscal quarter and the fiscal-year framing the plan covers.
- The principal's current external-influence baseline in one sentence (e.g., *"one paper published 18 months ago, two blog posts in the last year, no active open-source releases, three internal talks per year"*).
- The plan's top-line ask of the engineering director and CFO (e.g., *"approve one new open-source release, sponsor one KDD industry-track submission, protect ~30% of authoring hours for external work"*).

### `baseline-portfolio.md` — current state

One page. Shape:

- **Currently active artifacts.** One row per artifact, columns for: title, venue class, publication date, current status per chapter 6's dashboard (green / yellow / red), and any signal notes.
- **Current-year authored artifact hours split.** The rough hours-authored split across internal (chapter 2 classes A/B/C plus mod-503 living diagrams and mod-504 one-pagers) and external (chapters 3–5). Applied to the last 3 quarters (not necessarily perfectly measured — order-of-magnitude estimate).
- **The peer-principal exchange baseline.** Which peer principals at other orgs have engaged with the portfolio in the last 6 months. Names optional; roles and orgs (composite is fine) required.

### `fiscal-year-artifact-bets.md` — the plan itself

The load-bearing document. 2–4 pages. Shape: 4–8 fiscal-year bets, one per artifact the principal commits to authoring or co-authoring. Each bet is a bounded block with the following sections:

- **Bet title.** Working title (revised as the artifact is drafted). Not a manifesto title; a working one.
- **Venue class.** Which of the four chapter 1 classes (paper / blog / keynote / open source). If a paper-plus-blog fan-out (chapter 3 § *the paper-plus-blog fan-out*), name both.
- **The lesson — one sentence.** The chapter 1 step-1 lesson sentence. Compressed. If you cannot write it, this bet is not ready — either work the substrate longer or defer to a later fiscal year.
- **Which of chapter 3's four lesson shapes it fits.** Architecture / cross-team eval / bet framing / FM economics. If it does not fit, either lift the lesson to fit or drop the bet.
- **The internal substrate.** Which chapter 2 internal artifact(s) the external artifact extracts from. If the substrate does not yet exist, the bet is not ready — write the internal artifact first.
- **The co-authors.** Named (or roles if composite). At least one co-author who is not the principal.
- **The target venue.** The specific venue (KDD industry track, Meta Engineering blog, QCon AI track, Ray Summit keynote, a specific OSS project). Cite the venue's CFP window or publication cadence.
- **The publication timeline.** Draft milestones — internal-review draft (month X), legal-review draft (month Y), submission / publication (month Z). Includes legal-review lead time (chapter 3 § *the pre-publication legal review*).
- **The expected return-signal target.** For each of chapter 6's three signals, name the *near-term* (3–6 months post-publication) and *horizon* (12–24 months) target. Not vanity metrics; the three signals.
- **The retirement criteria.** Which of chapter 6's four triggers would retire the artifact. Named upfront so the retirement is not avoidance-blocked later.

Constraint: no more than 8 bets. If your plan has 10+, cut. The internal-first ratio (chapter 2) will not survive 10 external bets in one fiscal year at any tolerable internal-slate freshness. The modal principal ships 4–6 external artifacts per fiscal year across the four venue classes combined.

### `internal-first-substrate.md` — what must precede

One page. Shape:

- **The internal artifacts required by the fiscal-year external bets.** One row per internal artifact, columns for: title, chapter 2 class (A/B/C), current state (exists-and-stable / exists-and-evolving / to-be-authored), co-authors, cadence.
- **The internal-first ratio target.** The fiscal-year target hours-authored ratio (chapter 2 § *the internal-first ratio* recommends 70/30). Justified against the fiscal-year external bets — 8 external bets requires more external hours, which shifts the ratio; confirm the shift stays in the 60/40–80/20 band.
- **The rebalancing signals.** Chapter 2 § *the internal-first ratio* names three rebalancing signals. State how the plan tracks each per quarter; where the calendar-shape check (chapter 6) fits.

### `tracking-dashboard.md` — the operational surface

One page. A table with one row per artifact (baseline + fiscal-year-planned), columns per chapter 6 § *the tracking dashboard*:

- Artifact ID and title
- Venue class
- Recruiting signal (last 4 quarters — populate with baseline data where available; leave blank for fiscal-year-planned)
- Industry-adoption signal (last 4 quarters — same)
- Internal-leverage signal (last 4 quarters — same)
- Status (green / yellow / red / retired)
- Next action

Pre-populate the baseline rows; leave the fiscal-year-planned rows with the *target* signal values from `fiscal-year-artifact-bets.md`.

### `retirement-candidates.md` — the honest exit list

Half a page. Shape:

- **Baseline artifacts whose retirement criteria have fired.** One entry per artifact. Which of chapter 6's four triggers fired. What the *named exit* is (chapter 5 § *decision 4* for open-source; superseded-by-follow-up for papers / blogs; withdrawn-from-active-portfolio for keynotes).
- **Baseline artifacts approaching retirement.** One entry each, with which trigger is approaching and the projected fire quarter.

The exercise's honest-failure section: if `baseline-portfolio.md` shows artifacts in yellow or red status for 4+ quarters and `retirement-candidates.md` does not list them, you have hit the retirement-avoidance failure mode (chapter 6 failure mode 5). Revise.

### `appendices/venue-map.md`

Short table (half page). For each fiscal-year artifact bet, the 2–3 specific venues considered and the one selected, with a one-sentence justification per selection. This is where the chapter 1 § *the venue-selection failure modes* audit happens; each bet should show that it has considered alternate venues, not just picked the modal-prestige option.

### `appendices/calendar-shape-check.md`

Chapter 6 § *the calendar-shape check*, applied to the this-quarter baseline. Three checks (hours authored ratio, artifact-slate freshness for chapter 2's three classes, the peer-principal exchange). Each check has a one-paragraph readout: is it on-plan, is it drifting, is it triggering rebalancing?

## Starter guidance

- **Do the baseline honestly.** The exercise value comes from an accurate baseline, not an aspirational one. If your last external artifact was two years ago, name that. If you have never shipped an OSS release, name that. The plan lifts against reality, not against pretense.
- **Cap the number of bets.** 4–8 is the range; 8 is a stretch. A first-fiscal-year principal typically ships 3–5 external artifacts; a seasoned one ships 5–7. The plan-with-12-bets is a plan that will underperform on 8 of them.
- **Pick at most one bet per venue class per fiscal year.** One paper, one blog (or the paper-plus-blog fan-out counted as one bet), one keynote, one OSS release. Cross-venue portfolio diversity beats within-venue concentration; the chapter 1 venue-inflation failure mode is what within-venue concentration looks like.
- **Name the co-authors.** Chapter 2 § *co-authorship* is the leverage discipline. A bet without named co-authors is not a bet the plan should include; the succession and mentorship seams require named co-authors up front.
- **The internal substrate is prerequisite work, not parallel work.** If a fiscal-year external bet's internal substrate is *to-be-authored*, the external bet's timeline needs to allow 6+ months of internal-substrate work first. A draft plan that shows the paper submission 3 months after the internal reference doc is drafted has under-scoped the substrate.
- **Target the return signals, do not chase vanity metrics.** Chapter 6 failure mode 1 (the vanity-metric trap) is the modal first-cycle failure. The three-signal targeting is where the plan's discipline lives; without it, the plan is a wish-list.
- **Retirement criteria are named upfront.** Chapter 6 failure mode 5 (retirement-avoidance) is easier to guard against if the retirement criteria were pre-committed when the bet was ratified.
- **Time-box each section.** Baseline: 20 minutes. Fiscal-year bets: 40 minutes (this is the load-bearing section). Internal substrate: 20 minutes. Tracking dashboard: 15 minutes. Retirement candidates: 10 minutes. Appendices: 15 minutes. Total ~2 hours; if you go over 3, one of the sections is over-authored.

## Acceptance criteria

The exercise is done when:

- [ ] `README.md` states the principal context, fiscal-year framing, current baseline in one sentence, and the top-line ask of the engineering director and CFO.
- [ ] `baseline-portfolio.md` lists all currently active external artifacts with per-artifact status per chapter 6's dashboard, plus the current-year hours-authored split, plus the peer-principal exchange baseline.
- [ ] `fiscal-year-artifact-bets.md` contains 4–8 bets. Not 10+; not fewer than 3.
- [ ] Each bet has all 10 sections filled in (title, venue class, lesson sentence, chapter 3 shape, internal substrate, co-authors, target venue, publication timeline including legal review, return-signal targets, retirement criteria).
- [ ] Each bet's lesson sentence is *writable in one sentence* (chapter 1 step 1). If not, the bet is deferred, not included.
- [ ] Each bet has at least one *named* co-author who is not the principal.
- [ ] Each bet cites *one* specific target venue (not a list). Alternate venues considered live in `appendices/venue-map.md`.
- [ ] Each bet's target return signals are named for *all three* chapter 6 signals (recruiting, industry-adoption, internal-leverage), with near-term and horizon targets. No signal-of-one bets.
- [ ] `internal-first-substrate.md` names every internal artifact each fiscal-year external bet depends on. Every to-be-authored internal artifact is scheduled with sufficient lead time (6+ months) before the dependent external artifact.
- [ ] `internal-first-substrate.md`'s hours-authored ratio target is in the 60/40–80/20 internal-to-external band.
- [ ] `tracking-dashboard.md` pre-populates all baseline artifact rows with the last 4 quarters of signal data and all fiscal-year-planned rows with the target signal values.
- [ ] `retirement-candidates.md` names every baseline artifact in yellow or red status for 4+ quarters. No retirement-avoidance drift.
- [ ] The number of fiscal-year bets does not exceed 2 per venue class (paper, blog, keynote, OSS).
- [ ] `appendices/venue-map.md` shows 2–3 alternate venues considered per fiscal-year bet.
- [ ] `appendices/calendar-shape-check.md` runs the three-check audit and states whether rebalancing is triggered.
- [ ] The plan passes the *hand-off test*: another principal reading the six documents can hold the next quarterly review and know exactly what the plan commits to. If they cannot, the plan is under-specified.
- [ ] The plan passes the *chapter-1-failure-mode audit*: none of the six venue-selection failure modes (wrong-venue paper, venue-chase, surveyed-in-a-keynote, promotional-blog masquerade, open-source-dump, venue-inflation) are visible in the fiscal-year bets.

## Stretch goals

- **Draft the ratification memo to the engineering director and CFO.** One page. Frames the fiscal-year external-influence commitment, the CFO-side budget ask (multi-year for any OSS release), the headcount ask (co-author time, maintainer bench for OSS), and the escalation path when a bet needs to be pulled or added mid-year. This is where the plan converts from principal-authored to principal-plus-executive-ratified.
- **Extend the plan to a 3-year rolling horizon.** The single-year plan is the operational document; the 3-year rolling plan is the strategic one. Which artifacts persist across the horizon (foundational papers, open-source releases in continuous stewardship), which venue-classes are on-ramp (paper), which are steady-state (blog), which are outgoing (retired keynote series).
- **Draft the *peer-principal exchange invitation* for the next 6 months.** Chapter 6 § *the calendar-shape check* names the peer-principal exchange as the closest analogue to an external audit. Draft the invitation to 1–3 named peer principals: what you would ask them to read, what you would ask them to challenge, what specific artifact you want their read on.
- **Draft the *retirement post* for one baseline artifact whose criteria have fired.** One page. Names the artifact, the trigger that fired, the reason for retirement, and the follow-up artifact that supersedes it. The retirement post is what chapter 6's *explicit retirement* discipline looks like as a written artifact.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-01-industry-influence-artifact-plan/` is what you extend across the module: exercise-02 draws its paper or blog target from the fiscal-year-artifact-bets file; exercise-03 draws its keynote target from the same; exercise-04 draws its open-source-release proposal from the same. The plan is the *substrate* the other three exercises populate.
