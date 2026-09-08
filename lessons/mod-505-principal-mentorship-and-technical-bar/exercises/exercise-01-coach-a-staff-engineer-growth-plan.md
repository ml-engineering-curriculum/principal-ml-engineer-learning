# exercise-01: Coach a Staff Engineer's Growth Plan End-to-End

**Estimated effort:** 3 hours

## Objective

Run the L40→? growth conversation (chapter 1) end-to-end for one specific staff engineer and produce the three artifacts the conversation converges on: (i) the *placement notes* the principal keeps in their own quarterly file (chapter 6 § *quarterly review*, item 4); (ii) the *endorsement-criteria addendum* the mentee will use to build the signal you named you would need to see; (iii) the *mentee-owned growth plan* — the document the mentee walks out with and that the next 1:1 revises.

This exercise instantiates chapter 1's practice. The mentee can be real or a composite; if composite, be explicit about that in the notes (a composite mentee should still be internally consistent — one energy pattern, one portfolio shape, one path-lean signal, not a Frankenstein of every mentee you have ever coached).

## Prerequisites

- **Chapter 1 read end-to-end.** Especially the three paths as they operate at L48+, the four evidence axes, the four endorsement-criteria clusters, and the conversation shape.
- **Mod-501 chapters 4 and 5 read end-to-end.** The three-role-families boundary and the verb-object placement are the substrate for the endorsement-criteria discipline.
- **Mod-501 chapter 6 (hand-off contracts).** The seam with mod-410 exercise-04 (L30 coaching) is what keeps the exercise from drifting into staff-scope work.
- **Optional: mod-410 exercise-02 (staff-scope exec-audience RFC portfolio).** If your candidate mentee already has a mod-410 exercise-02 portfolio (or work-equivalent), it is the strongest signal substrate for the *portfolio evidence* axis.
- **Optional: [`staff-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/staff-ml-engineer-learning) mod-410 exercise-04** — the L30 coaching exercise the mentee already runs. Reading it lets you position your L40 coaching *above* the mentee's L30 practice.
- **Not a prerequisite: [`ai-infra-team-lead-learning`](https://github.com/ai-infra-curriculum/ai-infra-team-lead-learning).** But skimming its scope helps you name the EM path with fidelity when you describe it to the mentee.

## Problem statement

Pick a staff engineer (real or composite) who is at the *path-selection* moment described in chapter 1: 3+ years at L40, considering their next step but not yet committed to a specific path. Run the two- or three-session conversation arc chapter 1 § *the shape of the conversation* describes. Produce three artifacts.

- **Placement notes** — the principal's private read on the mentee. Not shared with the mentee; not shared with the mentee's line manager; kept in the principal's quarterly file per chapter 6.
- **Endorsement-criteria addendum** — the specific signal you named you would need to see before endorsing the mentee for the path they are leaning toward. This IS shared with the mentee, verbatim, so they can go build the signal.
- **Mentee-owned growth plan** — the mentee's document, drafted by them (or by you on their behalf in this exercise, since you are playing both seats) after the second conversation. The document the next 1:1 revises.

The three artifacts together are the exercise deliverable. The private notes plus the two mentee-facing artifacts is the shape you will use for every future L40 coaching relationship.

## Requirements

Populate a workspace directory `exercise-01-l40-growth-coaching/` (local — not committed to this curriculum repo). Suggested layout:

```
exercise-01-l40-growth-coaching/
├── README.md                      # index; mentee profile summary; conversation cadence
├── placement-notes.md             # principal's private read (chapter 6 § quarterly item 4 shape)
├── endorsement-criteria.md        # shared with mentee; chapter 1 § endorsement-criteria per path
├── mentee-growth-plan.md          # mentee's document; chapter 1 § conversation step 6
└── appendices/
    ├── conversation-log.md        # what happened in each session; brief and factual
    └── path-comparison-table.md   # the three paths side-by-side, from mentee's perspective
```

### `placement-notes.md` — private principal-side read

Chapter 1 § *a worked micro-example* is the reference shape; chapter 6 § *quarterly review* item 4 is where the file will live in production. One page, structured.

- **Mentee profile — 3–5 lines.** Years at L40, current technical scope, current line-EM, most recent shipped artifact at portfolio scope.
- **Energy pattern read.** What charges them, what drains them. Grounded in specific observations (a specific meeting after which they came back energised, a specific artifact they resisted finishing). Not adjectives.
- **Portfolio evidence read.** What is on their portfolio at the three altitudes chapter 1 names — IC-signal artifacts (paired-artifact instincts), EM-signal artifacts (people-growth stories), specialist-signal artifacts (depth artifacts cited elsewhere).
- **Bar-calibration behaviour read.** From the reviews you have observed them in, which of the three question shapes do they favour (shape-shifting, plan-shifting, growth-of-author, depth-of-approach)?
- **Response to the ambiguous-decision read.** Their first-instinct response to the org-scope prompt you gave them. First-artifact, first-meeting, or first-depth-analysis?
- **Placement read — one paragraph.** Which path is the strongest lean; where is the honest ambiguity; what is your placement hypothesis.
- **Endorsement-criteria set — one paragraph.** For the leaning path, the specific signal you have set as the criterion.
- **Alternative-path check — 2–3 lines.** Which peer track / role family you have pointed the mentee at to sanity-check the alternative(s).
- **Next-conversation date and objective.** Chapter 1 § *conversation step 7* cadence — 6 weeks for path-leaning, 3 months once path is chosen.

Constraint: one page. If it overflows onto page two, you have written characterisation, not observation.

### `endorsement-criteria.md` — shared with the mentee

This document IS the endorsement criteria you named in chapter 1 § *endorsement criteria per path*, written for the mentee to read. One page.

- **Opening — 2–3 sentences.** Restate the path the mentee is leaning toward and the fact that the criteria below are the specific signal you would need to see to endorse them for it. Endorsement means: *I would speak to your candidacy for the next altitude*, *I would sponsor you to the room that ratifies the promo*, *I would name you as a co-author on a leverage-move artifact*.
- **The criteria — 3–5 bullets.** Each bullet is a specific, observable, time-bounded signal. *"Ship one paired-artifact — one-pager plus deep-dive — for your next RFC by end of Q1 FY27; revise the shape at least once across the cycle in response to review comments."* Not *"demonstrate strategic thinking."*
- **What I am not looking for — 2–3 bullets.** Explicit negative criteria that guard against common false-signal shapes. *"I am not looking for you to attend more cross-team meetings; presence does not substitute for artifacts."*
- **How this connects to the alternative paths — 2–3 sentences.** If the mentee is leaning IC and you have a real specialist alternative for them, name it briefly and name the alternative endorsement criteria. Do not force the choice; keep the alternative visible.
- **Cadence and re-review date.** Six weeks to next path check-in; three months once path is chosen. Which artifacts the next 1:1 will review.

Constraint: one page, plain language, verbatim-shareable. If you would be uncomfortable if the mentee's line-EM saw this document, either the criteria are wrong or your relationship with the mentee needs a separate conversation.

### `mentee-growth-plan.md` — the mentee's document

In production this is authored by the mentee; in this exercise you draft it on their behalf. Chapter 1 § *conversation step 6* is the reference. 2–3 pages.

- **The path being invested toward.** One paragraph. Which path, why (in the mentee's voice), what the mentee sees themselves doing at the next altitude that they are not doing now.
- **The next-fiscal-year artifact set.** The 3–5 artifacts (RFCs, cross-team ratifications, leverage-move co-authorships, hiring-loop participation, community-ritual contribution) the mentee will produce or contribute to over the next fiscal year. Each artifact is *specific* (name, scope, delivery date) and maps to one of the endorsement criteria (`endorsement-criteria.md`).
- **The current-quarter commit.** The 1–2 artifacts landing this quarter. Explicit named-day commitments.
- **The check-in cadence.** With the mentee's line-EM, with you (the principal), with any peers named as reviewers or co-authors.
- **Alternative-path check — one paragraph.** What the mentee is doing to sanity-check the alternative paths (e.g., a shadow-week with a peer EM at another team, a coffee with a specialist-track principal at another org, a reading of the peer-EM track's onboarding material).
- **Risks to the plan.** 2–3 named risks — a specific bet that might sunset before the artifact lands; a specific dependency on a peer team; a specific life-shaped constraint the mentee is comfortable naming.

Constraint: 2–3 pages. The plan is a *working document*, not a manifesto — it will be revised at every subsequent 1:1.

### `appendices/conversation-log.md`

One page per conversation session. Date, duration, agenda covered (per chapter 1 § *conversation shape* steps 1–7), what came up that the placement notes now reflect, what the mentee committed to before the next session. Not verbatim; factual and brief.

### `appendices/path-comparison-table.md`

A single table with 3 columns (principal-IC, EM, specialist) and rows for the day-shape, the reward function, the artifact type, the audience, the promotion criteria at L48+, and the personal-life trade-offs. Filled in from chapter 1 § *the three paths as they operate at L48+*. This is a mentee-facing supporting document — you are giving the mentee the shape you have carried in your head so they can pattern-match against it.

## Starter guidance

- **Pick a real mentee if you can.** Even a low-fidelity read of a real person surfaces more signal than a composite; if you must use a composite, keep the composition internally consistent.
- **Do the observation before the conversation.** Chapter 1 § *the four evidence axes* is an *observation* discipline, not a *questionnaire*. If you have not been in enough of the mentee's meetings, reviews, or 1:1s to have first-hand observation, the placement notes will be low-fidelity — spend a week catching up on their portfolio and sitting in on their reviews before you run the conversation.
- **Draft the placement notes *before* the second conversation, not after.** The private read is what makes the second conversation legible — it is what lets you say *"when you describe X, you are describing the IC signal"* with specificity. If the placement notes come after the conversation, you are documenting what you said rather than *preparing* what you will say.
- **Name the endorsement criteria out loud in the conversation.** The mentee should not have to infer them. Chapter 1 § *conversation step 5* is explicit; the endorsement-criteria document is what remains after.
- **Do not resolve the mentee's ambiguity for them.** Chapter 1 § *conversation step 4* is a *make-visible* step, not a *decide-for-them* step. If the mentee is genuinely split, the document supports both paths with the corresponding endorsement criteria and gives them 6 weeks to move signal on the path they lean toward.
- **Cite the peer tracks explicitly.** If you endorse the EM path, cite [`ai-infra-team-lead-learning`](https://github.com/ai-infra-curriculum/ai-infra-team-lead-learning) as the track to point them at. If you endorse the specialist path, cite the specific specialist track (e.g., [`senior-ml-engineer-learning`](https://github.com/ml-engineering-curriculum/senior-ml-engineer-learning) mod-306 for RecSys, [`training-pipeline-engineer-learning`](https://github.com/ml-engineering-curriculum/training-pipeline-engineer-learning) for distributed-training depth). The citation is what makes the endorsement actionable.
- **Time-box each artifact.** Placement notes: 30 minutes to draft. Endorsement criteria: 45 minutes (this is the most-worked artifact). Growth plan: 60–90 minutes (or handed to the mentee to draft). Total roughly 3 hours; if you exceed 4, you are over-authoring one of the artifacts.

## Acceptance criteria

The exercise is done when:

- [ ] `placement-notes.md` fits on one page and has all nine sub-sections from the shape above.
- [ ] The energy-pattern, portfolio, bar-calibration, and ambiguous-decision reads are each grounded in a *specific observation*, not an adjective.
- [ ] The placement read states a hypothesis, not a diagnosis. Ambiguity is preserved where it is genuine.
- [ ] `endorsement-criteria.md` fits on one page and is verbatim-shareable with the mentee (i.e., you would be comfortable if their line-EM read it).
- [ ] Each endorsement-criteria bullet is specific, observable, and time-bounded. No *"demonstrate strategic thinking"* bullets.
- [ ] The document names the alternative-path criteria briefly, so the mentee is not forced into a false binary.
- [ ] `mentee-growth-plan.md` is 2–3 pages and has all six sub-sections from the shape above.
- [ ] The artifact set is *specific* — each artifact has a name, scope, and delivery date, and maps to at least one endorsement criterion.
- [ ] The current-quarter commit names 1–2 specific artifacts with day-level dates.
- [ ] The alternative-path check names a specific sanity-check activity (a shadow week, a coffee, a reading).
- [ ] `conversation-log.md` has one entry per conversation (minimum 2), each factual and brief.
- [ ] `path-comparison-table.md` has all three paths in columns and at least six rows populated from chapter 1's descriptions.
- [ ] The exercise passes the *hand-off test*: another principal reading the three artifacts (placement notes, endorsement criteria, growth plan) can hold the next 1:1 with the mentee without your presence. If they cannot, the artifacts are under-specified.
- [ ] The exercise passes the *drift-mode check*: none of the six failure modes from chapter 1 § *failure modes* are visible in the artifacts (coaching L30 not L40, coaching favorites, coaching toward decided answer, sponsorship-as-service substitution, sliding into first-line EM work, endorsing IC because it flatters you).

## Stretch goals

- **Run the second conversation with a real peer.** If your mentee is a composite, ask a peer (a staff engineer, a peer principal) to play the mentee and give you the second conversation for real. Their pushback on the endorsement criteria will surface where the criteria are vague vs. concrete.
- **Author a *"what happens if you pick the other path"* scenario for the mentee.** One page, first-person, from the mentee's perspective, describing their day-shape 24 months from now on the alternative path they are not leaning toward. This is a *pattern-match* aid for the mentee, not a persuasion tool.
- **Extend the exercise to two mentees on different paths.** One mentee leaning principal-IC, one leaning EM or specialist. The comparison surfaces which of your instincts generalise across paths and which are path-specific. Chapter 1 § *failure mode 2 (coaching your favorites)* is what this exercise stretches into.
- **Draft the *sponsorship letter* the mentee's next promo case (or next reference call) would attach.** One page, factual, names 2–3 specific accomplishments and the endorsement. Chapter 5 § *line 6 (no writing the promo case)* is the boundary; the sponsorship letter is the principal-side artifact that supports promo without owning it.
- **Author the *coach-the-coach* companion document.** If the mentee has an L30 direct on their team that the mentee is themselves coaching, draft the one-page brief on how the mentee should run *that* coaching (mod-410 exercise-04). This is the *chain*: the principal coaches the L40; the L40 coaches the L30.

## Deliverable location

Local workspace / personal git repo. Do not commit into this curriculum repo. The workspace directory `exercise-01-l40-growth-coaching/` is what you extend across the module: exercise-02 builds the leverage-move working titles that the mentee-growth-plan's artifact set may map onto; exercise-04's escalation charter includes the *coach the local reviewer* discipline that the growth-plan supports; chapter 6's quarterly cadence archives this exercise's placement notes as the seed of the mentee-portfolio-check section.
