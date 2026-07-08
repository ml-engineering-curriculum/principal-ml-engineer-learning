# The Verb-and-Object Vocabulary

> Chapter 1 of mod-501. Prerequisite: none — this is where the module starts. Downstream: every subsequent chapter uses the vocabulary this chapter defines.

## Why start with verbs and objects?

A Principal ML Engineer posting looks, on a first read, like a Staff ML Engineer posting with fancier adjectives ("multi-year", "org-wide", "north-star"). Recruiters and hiring managers themselves conflate the two levels often enough that the postings do it too. If the only tool you have for reading the levels is *how impressive the sentence sounds*, you will make the wrong classification about a third of the time and you will build the wrong track for yourself, because staff-plus IC scope and IC-principal scope share a lot of surface adjectives and diverge only on a few load-bearing verbs and objects.

The reliable move is to strip each responsibility down to a **verb** and its **object**, then ask what altitude that object sits at. `set` is the same verb whether the object is a ranking model, a portfolio, or the ML org's technical direction across product areas. The verb doesn't move; the object does. The altitude of the object *is* the level.

This chapter establishes the vocabulary that the rest of the module — and the rest of this track — uses.

## The verb-and-object table

The core reference:

| Verb | Level 30 (Senior) object | Level 40 (Staff) object | **Level 48 (Principal) object** |
|---|---|---|---|
| own | the ranking model | the ranking, retrieval, and personalization portfolio | **the ML org's technical direction across product areas** |
| lead | the fraud detection team | the ML org's build-vs-buy on the eval platform | **the north-star platform architecture the whole ML org converges on** |
| set | the eval harness for the team | the multi-quarter roadmap leadership commits to | **the technical bar the ML org hires and calibrates against** |
| author | the model card | the AI-risk register the CISO signs off on | **the reference architecture the industry cites** |
| influence | the sibling team | the peer ML platform team | **cross-functional stakeholders up to the SVP / CTO level** |
| coach | mid-level engineers | senior tech leads (L30) | **staff engineers (L40) and staff-plus hiring committees** |

Source: [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md), consolidated from the 26-posting sample. Every level-48 object in the right-hand column is a verbatim or minor-paraphrase quote from one of the postings named there.

The pattern in every row is the same three-step lift:

1. Level 30 owns *a system* (single-team scope — one model, one team, one harness, one card).
2. Level 40 owns *a portfolio of systems, plus one org-scope contract* (multi-team scope — the platform strategy, the roadmap, the risk register, the paved-road contract).
3. Level 48 owns *the org- and industry-wide direction of the ML function* (org- and industry-scope — the direction across product areas, the north-star architecture, the technical bar, the reference other orgs cite).

Everything else — the number of stakeholders, the calendar horizon, the salary top-of-band — follows from this. The object is the load-bearing piece.

## Two examples, worked

Take the sentence "we need someone who can set the ML strategy". By itself, at any level. What determines the altitude?

**Case A — SoundCloud, Senior Principal ML Engineer (New York).** Verbatim: *"Define the technical North Star for ML across engineering."* Verb: `set` (via `define`). Object: `the technical North Star for ML across engineering`. That object spans the entire engineering org's ML function, not one team's roadmap. Right-hand column of the verb-object table. This is a Principal-scope responsibility.

**Case B — a Staff ML Engineer posting for the ranking team on the same product.** Wording tends to be *"Set the ranking team's multi-quarter roadmap."* Same verb (`set`). Object: `the ranking team's multi-quarter roadmap`. Middle column. Staff-scope. Owned by `staff-ml-engineer-learning` mod-410, not this track.

Both sentences use the same verb. Only the object tells you which track authors the material.

For a third contrast, note that the *executive* form of `set` in the ML function reads more like *"Own the P&L for ML"* or *"Set the ML function's headcount and budget for FY27."* Verb — `own` / `set`. Object — `the P&L`, `headcount and budget`. Executive branch, owned by `chief-ai-officer-learning`. Not this track either.

## Objects that only appear at principal altitude

Some phrases in the right-hand column of the verb-object table simply do not appear in a well-written Staff posting. Watch for these — they are principal-defining:

- **"the technical North Star for ML"** — SoundCloud. Direction of the ML function itself. A staff engineer sets *a roadmap*; a principal sets *the North Star the roadmap serves*.
- **"the north-star platform architecture"** with **"living diagrams and canonical APIs"** — Capital One, Agentic AI Platform Distinguished. The whole ML org's architecture converges on it. A staff engineer authors *the multi-system RFC*; a principal authors *the north-star architecture the multi-system RFCs must fit inside*.
- **"organization-wide platform innovation"** — Capital One, Sr. Distinguished Remote-Eligible. The scope is `organization`, not `portfolio`.
- **"multiply the effectiveness of every ML team"** — Upstart. The scope is *every* ML team, not the assigned team or the sibling teams.
- **"influence cross-functional stakeholders up to the SVP level"** — Capital One, Sr. Distinguished AI Engineer. Staff-scope influence tops out at the VP; principal-scope influence goes SVP / CTO.
- **"thought leader in a growing community of machine learning practitioners"** — Ibotta. The audience is the *community*, not the org.
- **"strategic direction of AI-driven cybersecurity initiatives"** — Palo Alto Networks. The verb `contribute to` softens it, but the object is `strategic direction`. Principal-scope.

If none of these principal-scope objects — or their close paraphrases — appear in a posting, then no matter how impressive the adjective density is, the role is being *marketed* as principal but *scoped* as staff. Chapter 2 spends time on how to catch that.

## Objects that never appear at principal IC altitude

Conversely, some objects belong on the executive-branch or research branches and should raise a flag when they appear in a "Principal ML Engineer" posting:

- **"own the P&L"**, **"own the ML org's budget"**, **"set headcount"**, **"perform manager-of-managers reviews"** — executive scope. These belong to Head of AI / VP of ML / CAIO. The IC-principal path has no direct reports.
- **"report to the CEO"**, **"present to the board of directors quarterly"** — executive scope. The IC-principal presents to executives; the IC-principal does not sit on their governance cadence.
- **"invent new pretraining objectives"**, **"publish state-of-the-art results on <benchmark>"**, **"lead the research direction"** — research-principal scope. Principal Research Scientist / Distinguished Applied Scientist at an AI lab. Not this track.

When a posting mixes principal-IC objects with executive objects or research objects, chapter 4 handles the classification.

## Why the object shift lives in the object, not the verb

A common trap is to hunt for principal-flavoured *verbs*: "set", "define", "lead", "influence". Those verbs occur at every level. Staff engineers `set` roadmaps. Senior engineers `set` team eval harnesses. Junior engineers `set` PR review conventions for the repo. The verb doesn't discriminate — its object does.

A second common trap is to hunt for principal-flavoured *adjectives*: "strategic", "north-star", "long-term", "cross-functional". These modifiers get slapped onto staff-scope responsibilities all the time because the recruiter, the hiring manager, or the JD-copier before them wanted the posting to *sound* senior. Adjective density is not the level signal. The object is the level signal.

Read every principal-scope sentence twice. First read, ask *what verb*. Second read, ask *what object, at what altitude*. If the altitude is `the ML org's direction across product areas`, `the north-star architecture the whole ML org converges on`, `the technical bar the ML org calibrates against`, `the reference architecture the industry cites`, or `SVP / CTO / cross-functional executive review consensus` — you are looking at principal scope. Anything below that altitude is staff or senior.

## Summary

- The verb-and-object table is the vocabulary. Levels differ in objects, not in verbs.
- Principal-scope objects sit at *the ML org's technical direction*, *the north-star architecture*, *the technical bar the ML org calibrates against*, *the reference architecture the industry cites*, and *SVP / CTO influence without authority*. All five appear as verbatim quotes in the 26-posting sample.
- Verbs and adjectives are noise. The load-bearing signal is the object.
- Some objects belong only on the executive branch (P&L, headcount, board reporting) or on the research-principal branch (state-of-the-art publication, pretraining-objective invention). Chapter 4 handles them.
- Chapter 2 applies the table to five real postings from the sample.
