# exercise-02: Principal / Executive-Branch Partnership Contract Portfolio

**Estimated effort:** 3 hours

## Objective

Author the *four partnership contracts* — with the **CAIO / Head of AI**, the **Head of AI Governance**, the **CISO**, and the **CFO** — that operate over the mod-502 strategy and the mod-503 architecture and that make the coalition-and-escalation practice in chapters 4 and 6 possible. Each contract is a one-to-two page document, ratified annually, that names *what the principal brings*, *what the peer brings*, the *cadence*, the *authorship and ratification rights*, the *decision rights*, the *escalation path*, and the *artifact flow*.

The output is the *portfolio* of contracts. Chapter 3 § *the four contracts as a system* is the acceptance frame: read together, the four should be the engine that converts your mod-502 strategy and your mod-503 architecture into ratified, executed direction across the org.

## Prerequisites

- **Chapter 3 read end-to-end.** All four counterparts' contract elements, the three cross-counterpart disciplines, and the *four contracts as portfolio* framing.
- **Mod-503 chapter 8 read end-to-end.** The seam discipline is the model this exercise extends. Chapter 8 § *contract 1 — policy-to-contract mapping* is the direct antecedent for the Head of AI Governance contract.
- **Exercise-01 complete.** The one-pager and deep-dive are the substrate the four contracts operate over. Section 9 of the deep-dive (*what-we-ask-of-leadership expanded*) is the artifact each contract's *ask* section grounds in.
- **Mod-502 chapter 5 skimmed.** The refresh cadence anchors the *cadence* section of each contract.
- **Optional but recommended:** the peer executive-branch tracks — [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning) and [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning) — read at the README altitude. Each is the *peer's* curriculum; understanding their scope helps you author the contract from their side too.

## Problem statement

Chapter 3 named the four contracts. Each is short. Each is versioned. Each is refreshed annually. Together, they are the mechanism the IC-principal uses in place of line authority.

Two failure modes make this exercise necessary. First, first-cycle principals treat the executive branch as *escalation targets* (chapter 3 § *failure mode 1 — the "just escalate" model*). Second, they treat the executive branch as *distribution channels* for a strategy the executives did not co-author (chapter 3 § *failure mode 2 — the "solo genius" model*). The partnership contract is the corrective for both.

Your job is to author the four contracts as if you were about to walk each into an annual joint-ratification session with the peer. Each is signed at the top; each is walked through, edited live, and ratified. The version you commit to workspace is the *proposed* version; the *ratified* version has both names on it.

## Requirements

Populate a workspace directory `exercise-02-partnership-contracts/`. Suggested layout:

```
exercise-02-partnership-contracts/
├── README.md                              # portfolio overview and cross-references
├── caio-partnership-contract.md
├── governance-partnership-contract.md
├── ciso-partnership-contract.md
├── cfo-partnership-contract.md
├── cross-counterpart-map.md               # how the four contracts interlock
└── refresh-log.md                         # annual refresh history
```

### Per-contract shape

Each of the four contract documents follows the same seven-section shape. Chapter 3 § *contract elements* per counterpart is the reference; every element listed there for that counterpart must appear in your document.

1. **Purpose and identity** — one paragraph. Who each side is (name, title, org affiliation), what job the contract exists to do, and the anchor sentence from mod-501 chapter 4 or chapter 5 in this module that grounds the counterpart's identity.
2. **What each side brings** — two paragraphs.
   - Paragraph 1 — *what the peer brings that the IC-principal does not*: named, per chapter 3.
   - Paragraph 2 — *what the IC-principal brings that the peer does not*: named, per chapter 3.
3. **Cadence** — a compact table of the standing calendar entries with the peer. Each row: cadence (weekly / bi-weekly / monthly / quarterly / semi-annual / annual), duration, purpose. Chapter 3 § *cadence* per counterpart is the required minimum.
4. **Authorship and ratification** — enumerate the artifacts jointly held. For each: who authors, who edits, who ratifies, where the artifact lives, on what cadence it refreshes. Chapter 3 § *authorship and ratification* per counterpart is the required minimum.
5. **Decision rights** — enumerate the decisions that fall on this seam. For each: who decides, who advises, who has veto. Named. Chapter 3 § *decision rights* per counterpart is the required minimum.
6. **Escalation path** — the specific path each class of disagreement takes if not resolvable at this seam. Chapter 3 § *escalation path* per counterpart is the required minimum. Explicitly, for each escalation path: named, and grounded in chapter 6 § *the escalation protocol*.
7. **Artifact flow** — bidirectional. What flows from the principal to the peer, on what cadence, and what flows the other way. Chapter 3 § *artifact flow* per counterpart is the required minimum.

Each contract closes with a *version and refresh cadence* footer: version, effective-from date, effective-through date, next-refresh date. Chapter 3 § *discipline 3 — version and refresh the contract* is the reference.

Length: one to two printed pages per contract.

### The four contracts specifically

**`caio-partnership-contract.md`** — with the peer CAIO / Head of AI / VP of ML. Chapter 3 § *counterpart 1* is the required content minimum. Note that the *co-authorship* of the mod-502 strategy one-pager is the primary artifact — this contract is the one that most directly operates over exercise-01.

**`governance-partnership-contract.md`** — with the Head of AI Governance / Chief Responsible-AI Officer. Chapter 3 § *counterpart 2* is the required content minimum. Note that the *policy-to-contract mapping* (mod-503 chapter 8 § *contract 1*) is the load-bearing co-authored artifact.

**`ciso-partnership-contract.md`** — with the CISO. Chapter 3 § *counterpart 3* is the required content minimum. Note that the *joint threat model* over the mod-502 bet portfolio is the load-bearing co-authored artifact.

**`cfo-partnership-contract.md`** — with the CFO / VP of Finance for Engineering. Chapter 3 § *counterpart 4* is the required content minimum. Note that the *capacity envelope in the strategy one-pager's "what we ask of leadership" section* is the load-bearing co-authored artifact.

### `cross-counterpart-map.md` — how the four interlock

Chapter 3 § *the four contracts as a system* is the reference. This document is a short (one-to-two page) synthesis that:

- Names the four cross-counterpart overlaps chapter 3 § *the four contracts as a system* enumerates (CAIO + governance, CAIO + CFO, governance + CISO, all-four-at-the-strategy-semi-annual).
- For each overlap, names the specific *joint session* on the calendar, the *joint artifact* the session produces, and the *principal's role* in the joint session (mediator, co-author, chair, technical author).
- Includes a *signs the four are working as a portfolio* checklist (chapter 3 § *the four contracts as portfolio, not tasks*).

### `refresh-log.md` — versioning discipline

Per chapter 3 § *discipline 3 — version and refresh the contract*. The log records the current version of each contract, the date of last ratification, the date of next scheduled refresh, and a compact change history. For the first version (this exercise), one entry: *"v1.0 — proposed on <YYYY-MM-DD>; awaiting joint ratification"*.

## Starter guidance

- **Author from the peer's chair, not from your own.** For each contract, imagine you are the peer reading it. Does it match how they would articulate what they bring? If not, the contract is authored from a solo-genius seat (chapter 3 § failure 2) and will fail ratification.
- **Cadences are calendar-persistent, not aspirational.** The weekly with the CAIO is a real recurring meeting on your calendar. If the *cadence* section is a wish list, the contract is not ratifiable. If your current org does not support the cadence, note the specific delta and how you would negotiate it.
- **Decision rights are the sharp edges.** Every decision the seam produces is on one side of a specific line. "Co-decided" is a valid outcome for some decisions; naming *both* sides' veto is required. A contract with no vetoes named is a contract that will not survive its first disagreement.
- **Escalation paths avoid the peer's manager.** Chapter 3 § *counterpart 1 — escalation path* is explicit: *"The principal does not escalate over the CAIO's head to the CAIO's manager; that path is a partnership-breaking move."* Extend the discipline to each of the four contracts. If your escalation path is *"escalate to the CTO"* for every seam, review chapter 6 § *the escalation protocol* and refine.
- **Artifact flow is bidirectional.** Chapter 3 § *artifact flow* per counterpart is a *list*, not a paragraph. What flows in, what flows out. Cadence. Location. If your artifact flow is one-directional, the contract has not internalised the partnership frame.
- **The one-pager and deep-dive from exercise-01 anchor two of the four contracts.** The CAIO co-authors the one-pager; the CFO co-authors the *what we ask of leadership* section. Cite exercise-01 directly.
- **The mod-503 seam contracts anchor two of the four.** The Head of AI Governance contract's policy-to-contract mapping is chapter 8 § *contract 1* verbatim, extended to the Head of AI Governance's ownership. The CISO contract's ML-specific threat model presumes the mod-503 chapter 3 plane decomposition.
- **Sign at the top.** Each contract has a signature block: the IC-principal's name (yours), the peer's name (or *[peer]* placeholder if you are drafting for a hypothetical org), and a *proposed on <date>* line. Ratification happens jointly; the drafting is one-sided.

## Acceptance criteria

Your portfolio is done when it can pass all of the following:

- [ ] Four contracts exist: `caio-partnership-contract.md`, `governance-partnership-contract.md`, `ciso-partnership-contract.md`, `cfo-partnership-contract.md`.
- [ ] Each contract has all seven sections: purpose and identity, what each side brings, cadence, authorship and ratification, decision rights, escalation path, artifact flow. Each is one to two printed pages.
- [ ] The *what each side brings* section for each contract has two named paragraphs — one for the peer, one for the IC-principal — grounded in chapter 3's per-counterpart enumeration.
- [ ] The *cadence* section for each contract is a calendar-persistent table (weekly / bi-weekly / monthly / quarterly / semi-annual / annual). Each cadence entry has a duration and a purpose. Chapter 3's minimums (per counterpart) are met.
- [ ] The *authorship and ratification* section for each contract names at least two joint artifacts, per counterpart, with the specific author / editor / ratifier roles.
- [ ] The *decision rights* section for each contract enumerates at least three named decisions the seam produces, with the specific decides / advises / veto pattern per decision.
- [ ] The *escalation path* section for each contract names the escalator (specific title, not "the exec branch") and specifies the case-by-case routing (chapter 3 per counterpart). No contract's escalation path is *"escalate to the CTO for everything"*.
- [ ] The *artifact flow* section for each contract is bidirectional and enumerates named artifacts.
- [ ] `cross-counterpart-map.md` names all four overlaps from chapter 3 § *the four contracts as a system* and, for each overlap, names the joint session, the joint artifact, and the principal's role.
- [ ] `cross-counterpart-map.md` includes a *signs the four are working as a portfolio* checklist derived from chapter 3 § *the four contracts as portfolio, not tasks*.
- [ ] Each contract has a *version and refresh cadence* footer with version, effective-from, effective-through, next-refresh date.
- [ ] `refresh-log.md` exists with the v1.0 proposed-on entry.
- [ ] Each contract has a signature block. IC-principal is named; peer is named or placeholder.
- [ ] The three cross-counterpart disciplines (chapter 3 § *§the three cross-counterpart disciplines*) are visibly enforced in every contract: no cadence is a "we'll figure it out"; every contract borrows the peer's authority explicitly; every contract is versioned.

## Stretch goals

- **Draft each contract from the peer's side too.** For one of the four counterparts (the CAIO is the recommended starting point), author a *parallel* one-page contract *from the peer's chair* — what they would author about you if they were writing this exercise. Compare with your own. Divergences are the seam frictions the first joint-ratification session will surface.
- **Draft the first joint-ratification session's agenda.** Chapter 3 § *the annual refresh is a joint session*. Draft the agenda: how the session opens, how each section is walked, how ratification is captured, how the follow-up is confirmed. Modal duration: 60 minutes. This connects to chapter 4 § *stage C* — the joint-ratification session is a decision-room in miniature.
- **Draft one contract for a peer role you are missing.** Some orgs have a **Chief Data Officer** whose scope overlaps the CFO's on data-cost, the CAIO's on data strategy, and the Head of AI Governance's on data-tier policy. Some orgs have a **General Counsel** whose scope overlaps the CISO's and the Head of AI Governance's on regulatory sign-off. Pick one and draft a fifth partnership contract. Note the overlap explicitly with the four core contracts.
- **Draft a *contract-breaking-cases* appendix.** For each of the four contracts, one paragraph on: what the contract *does not cover*, what would break it, and what the recovery looks like. Chapter 3 § *signs the contract is not being held* per counterpart is the antecedent.
- **Author the *what-changed* delta for the current annual refresh.** If you have run one cycle already (you probably have not, this being the first-cycle exercise), draft the one-paragraph delta between v0.9 and v1.0 for each contract. Otherwise, sketch what the FY26-to-FY27 refresh would need to note. This forces you to think about what actually changes cycle-over-cycle.
- **Cross-reference the contracts into the mod-503 chapter 8 seam contracts.** The peer platform-side principals are a fifth-and-sixth partnership pattern. Draft the *rendering* of your CAIO contract into the format mod-503 chapter 8 § *communication rhythm with the platform-side principals* uses. This is the discipline of "different peers, same contract discipline".

## Deliverable location

Local workspace / personal git repo, extending the workspace from exercise-01. Do not commit into this curriculum repo. The four contracts are the artifact system that carries every subsequent exercise: exercise-03's coalition tracker is walked with the four peers on their standing cadences; exercise-04's escalation log routes through the four contracts' escalation paths.
