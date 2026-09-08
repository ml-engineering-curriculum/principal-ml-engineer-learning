# The Peer Executive-Branch Partnership Contract

> Chapter 3 of mod-504. Prerequisite: chapter 1 (working definition), chapter 2 (audience boundary), and mod-503 chapter 8 (seams with peer platform-side principals and with governance). Downstream: exercise-02 authors the four contracts named here; chapter 4 walks the coalition sequence that operates over them; chapter 6 walks the escalation protocol that runs *through* them.

## Why a partnership contract, not a relationship

Mod-503 chapter 8 named the seam discipline for the peer platform-side principals: *"The seams are contracts, not sentiments. They have named owners, named authorship rights, named citation formats, and named change-management practices."* This chapter extends that discipline to the executive-branch peers.

The four peers — the **Chief AI Officer / Head of AI** (owned by [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning)), the **Head of AI Governance** (owned by [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning)), the **CISO**, and the **CFO** — sit at the table where the ML function's biggest bets get ratified. Each brings something the IC-principal structurally *cannot bring* from the IC seat: headcount and budget authority (CAIO / CFO), policy authorship (governance), regulatory sign-off (CISO / governance), board mandate (CAIO), P&L (CAIO / CFO). Each is a *peer* to the principal at the ratification table, not a superior and not an audience.

Two failure modes make this chapter necessary.

**Failure mode 1 — the "just escalate" model.** The IC-principal treats the executive branch as an *escalation target*: when a cross-org disagreement blocks a bet, the principal escalates it to the CAIO or the CFO to be broken. This works once. It does not scale. The executive-branch peer's willingness to break a decision on the principal's behalf depends on the credibility of the partnership over prior cycles; a principal who only shows up to escalate has no bank of credibility to draw on. Chapter 6 § *escalation is expensive* is the operational reference.

**Failure mode 2 — the "solo genius" model.** The IC-principal produces the ML technical direction alone and hands it to the executive branch to socialise. This treats the peer executives as *distribution channels* for a strategy they did not co-author. The peers, correctly, refuse to carry a direction they had no hand in shaping — the CFO does not underwrite a capacity envelope they were not consulted on, the Head of AI Governance does not co-sign risk framings they did not review, the CAIO does not tell the board about a bet they were not co-invested in. Wiser's *"in partnership with product and business leadership"* framing (chapter 1) is the corrective; the partnership frame is not optional.

The partnership contract is what makes both failure modes go away. It names, per peer, what the principal brings, what the peer brings, on what cadence, and what happens when the two sides disagree. It is a short document — one to two pages per counterpart — ratified annually and refreshed when either principal's or peer's scope shifts.

## The four counterparts

The four are not interchangeable. Each has a distinct object and a distinct partnership shape. Chapter 5 walks the audience craft for each; this chapter walks the *contract*.

### Counterpart 1 — CAIO / Head of AI / VP of ML (the executive-branch tier of the ML function)

**Track owner in this ecosystem:** [`chief-ai-officer-learning`](https://github.com/ml-engineering-curriculum/chief-ai-officer-learning).

**What they own that the IC-principal does not.** Headcount plan across the ML function. The ML function's P&L (at CAIO altitude). Board reporting cadence for the AI function. The org's public AI narrative. Hiring pipeline at the VP-and-Director levels. Comp bands. Executive-branch decision authority — the mandate to say *"we are doing this"* and have it stick because the mandate is theirs.

The CAIO / Head of AI is the *closest partner* structurally: they and the principal are jointly responsible for the ML function's success. The CAIO owns the *what commit does the org make*; the principal owns *what commit is defensible technically*. Mod-501 chapter 4 (three role families) is the reference for the identity distinction.

**What the IC-principal brings that they cannot.** The defensible bet framing — *why this bet, why now, what would stop us*. The multi-year architecture direction — *what shape the ML function converges on*. The technical-voice legitimacy — *this framing has been credible over prior cycles* (chapter 1 test 1). The staff-and-below coalition — the ML-function staff-plus engineers whose ratification the CAIO needs to make executive commitments stick. Cross-functional judgement — *does this bet actually land, given the platform substrate and the product context*.

**Contract elements.**

- **Cadence.** Standing weekly 45-min 1:1 (calendar-persistent). Monthly deep-dive on one bet from the mod-502 portfolio, rotating. Quarterly joint session on the strategy refresh cycle. Semi-annual co-authorship on the strategy one-pager (mod-502 chapter 7).
- **Authorship and ratification.** The mod-502 strategy is *co-authored* — the principal drafts, the CAIO edits, both names go on the ratified version. The board-facing narrative for the ML function is *CAIO-authored, principal-reviewed*. The north-star architecture (mod-503) is *principal-authored, CAIO-endorsed*.
- **Decision rights.** Headcount envelope: CAIO decides, principal advises on the technical shape (roles by capability, seniority mix). Public representation to the board or the press: CAIO decides, principal supports; the principal does not become the ML function's public spokesperson (mod-501 chapter 4 hybrid trap B). Technical direction: co-decision — the principal has the technical veto (a bet the principal will not endorse does not go into the strategy), the CAIO has the organisational veto (a bet the CAIO cannot underwrite operationally does not go into the strategy).
- **Escalation path.** Disagreement between the two is resolved between the two; if not resolvable, the CAIO escalates *up* (to the CTO / CEO), the principal escalates *sideways* (to the peer platform-side principal for a technical review, or to the responsible-AI review body). The principal does not escalate over the CAIO's head to the CAIO's manager; that path is a partnership-breaking move.
- **Artifact flow.** The strategy one-pager, the strategy deep-dive, the current-cycle coalition tracker (chapter 4), the escalation log (chapter 6), and the responsible-AI review-body log (mod-503 chapter 7) all flow to the CAIO on a standing cadence. The CAIO's board deck, the headcount plan, and the P&L allocation flow back on the same cadence.

**Signs the contract is not being held.** The strategy one-pager is authored solo. The CAIO is surprised by the current-cycle bet portfolio. Board reporting cadences drift out of sync with the strategy refresh cycle. The principal escalates a decision above the CAIO. The CAIO is asked to make a board commit against a bet framed by someone the principal has not vetted.

### Counterpart 2 — Head of AI Governance / Chief Responsible-AI Officer

**Track owner in this ecosystem:** [`head-of-ai-governance-learning`](https://github.com/ml-engineering-curriculum/head-of-ai-governance-learning).

**What they own that the IC-principal does not.** Policy authorship — the internal policies the ML function is obligated to (risk-tier definition, model-card content requirements, launch-review responsible-AI criteria, red-teaming standard, dataset-provenance discipline). Regulatory interpretation — how the EU AI Act, the NIST AI RMF, ISO/IEC 42001, sector regulations (CFPB, OCC, NYC Local Law 144, OMB M-24-10) land as obligations on the ML function. External audit interface — the auditor conversation is theirs to run. The public responsible-AI narrative for the org. Formal risk-committee membership (at CAIO / General Counsel altitude).

**What the IC-principal brings that they cannot.** Contract-level enforcement — the four canonical APIs (mod-503 chapter 4) that convert policy into invariants a launch has to pass. The technical judgement on whether a policy is enforceable at the substrate level and, if not, what the substrate-level alternative is. The reference architecture (mod-503) whose invariants the policies flow into. The ratified ML-function technical direction that determines *what the risk portfolio even looks like* over the next 3–5 years.

**Contract elements.**

- **Cadence.** Standing bi-weekly 45-min 1:1. Monthly joint session on the policy-to-contract mapping (mod-503 chapter 8 § *contract 1*). Quarterly joint session on the risk-tier taxonomy refresh. Semi-annual joint session on the regulatory-horizon scan.
- **Authorship and ratification.** Policies are *authored* by the governance track; *reviewed* by the principal for enforceability at the contract layer; *cited* in the reference architecture's canonical APIs. Contract invariants are *authored* by the principal; *reviewed* by the governance track for policy sufficiency. The policy-to-contract mapping document (mod-503 chapter 8 § *contract 1*) is *co-authored*; both names on the ratified version.
- **Decision rights.** Policy content: governance decides, principal advises on enforceability. Contract invariants: principal decides, governance reviews for policy fidelity. Documentation requirements (Model Cards, Data Cards, datasheets): governance decides on the required *content*; principal decides on the *contract-side interface* (which fields are required, whether they gate a launch, how they are versioned).
- **Escalation path.** Regulatory disagreement (does an obligation apply?) escalates to General Counsel. Internal-risk-committee disagreement (is a bet within-risk?) escalates to the risk committee itself, with both the principal and the Head of AI Governance present. Enforceability disagreement (governance requires an obligation the principal says is not enforceable at the contract layer) resolves in the joint monthly; if not resolvable, the principal proposes a *deferred launch* or a *tiered rollout* rather than shipping non-enforceable policy.
- **Artifact flow.** The policy-to-contract mapping, the risk-tier taxonomy, the four contract invariant sets, the reference architecture's governance-relevant sections, the responsible-AI review-body log (mod-503 chapter 7) all flow both directions on the standing cadence.

**Signs the contract is not being held.** A regulator activation lands on the ML function's calendar without the principal knowing; a launch ships that violates a policy the governance track authored; a policy ships that the contract layer has no enforcement path for; the two artifacts (policy and contract) drift out of alignment.

### Counterpart 3 — CISO / Chief Information Security Officer

**Track owner in this ecosystem:** No principal-scope security-side track. The peer track for ML security depth is Ai Infra Security (level 35), which is a specialist substrate track that this principal cites but does not manage.

**What they own that the IC-principal does not.** The org's information-security policy and control set. Threat-modelling for enterprise data, customer data, PII, and (in ML orgs) model artifacts, training data, and prompt-and-response corpora. Third-party risk (vendor / API supplier / open-source-model provenance). Incident response leadership for security incidents. Regulatory sign-off for security-facing obligations (GDPR, HIPAA where applicable, SOC 2, ISO/IEC 27001). Board-facing security narrative.

**What the IC-principal brings that they cannot.** The ML-specific threat surface — model theft, data-exfiltration through generation, prompt injection, training-data poisoning, membership-inference attacks, model-inversion attacks — mapped to the reference architecture's planes. The contract-level enforcement of security invariants in the four canonical APIs (feature access controls, registry provenance, gateway policy signature verification, eval-set data-tier classification). The technical direction that determines *what the ML security surface looks like* over the next 3–5 years — a foundation-model programme has a different threat surface than a fine-tuning-only integration bet.

**Contract elements.**

- **Cadence.** Standing monthly 45-min 1:1. Quarterly joint threat-modelling session on the mod-502 bet portfolio, walking each material bet through the ML-specific threat surface. Semi-annual joint session on the regulatory-horizon scan (co-attended with the Head of AI Governance).
- **Authorship and ratification.** Security policies are *CISO-authored*, principal-reviewed for ML enforceability. The ML-specific threat model is *co-authored* — both names on the ratified version. Incident-response runbooks for ML-specific incidents are *co-authored*, with the principal owning the ML-function-side of the runbook and the CISO owning the corporate-response side.
- **Decision rights.** Security controls at the substrate layer: CISO decides, principal advises. Contract-level security invariants: principal decides, CISO reviews for policy sufficiency. Model-artifact and training-data classification: co-decided — the CISO's data-tier taxonomy applies, the principal decides how the tier lands as a contract invariant.
- **Escalation path.** Security incidents follow the CISO's incident-response protocol; the principal is a named respondent for ML-function-side actions. Threat-modelling disagreement resolves in the quarterly joint session; if not resolvable, the bet is *deferred* (chapter 6) rather than shipped under-modelled.
- **Artifact flow.** The ML-specific threat model, the incident-response runbook for ML incidents, the security-relevant sections of the reference architecture, and the current-cycle bet portfolio's threat surfaces all flow both directions.

**Signs the contract is not being held.** A material bet lands in the mod-502 portfolio without a joint threat model. An ML-specific incident is handled by the corporate SOC without the principal in the room. The CISO's data-tier taxonomy is not reflected in the contract layer. The principal proposes a bet the CISO has to red-team from cold, in a decision-room, in real time.

### Counterpart 4 — CFO / VP of Finance for Engineering

**Track owner in this ecosystem:** No principal-scope track; finance is a peer function outside the AI-curriculum ecosystem.

**What they own that the IC-principal does not.** Capital allocation across engineering functions. The multi-year investment envelope for the ML function. Comp-band ownership (with the CAIO). Vendor and cloud-spend approval at scale. External reporting on ML costs (to the board, to investors in public-company orgs). Investment prioritisation across engineering, product, and other functions.

**What the IC-principal brings that they cannot.** The technical direction that determines *what the ML function's cost curve looks like over the next 3–5 years*. The bet-portfolio-level cost defensibility — *why the paved-road substrate bet is a cost move, why the foundation-model pretraining bet is out-of-window this cycle for cost reasons* (mod-502 chapter 4 sunset criteria). The architecture-level cost judgement — *inference cost per query at scale, training cost per bet, storage cost per feature-store growth*. The staff-plus cost-defence artifacts (`staff-ml-engineer-learning` mod-407 owns the portfolio-scope TCO discipline; the principal lifts it to org-scope).

**Contract elements.**

- **Cadence.** Standing monthly 30-min 1:1. Quarterly joint session on the bet-portfolio cost curve. Semi-annual joint session on the multi-year investment envelope. Ad-hoc pre-brief before board-facing cost narratives.
- **Authorship and ratification.** The multi-year capacity envelope in the strategy one-pager (mod-502 chapter 7 § *what we ask of leadership*) is *co-authored* with the CFO — the principal drafts, the CFO validates the envelope range against the org's financial plan, both names on the ratified version. Bet-portfolio cost defence is *principal-authored*, CFO-reviewed. Board-facing cost narrative is *CFO-authored*, principal-reviewed.
- **Decision rights.** Capital allocation between engineering functions: CFO decides. Within-ML-function allocation across bets: co-decided — the principal advises on the bet portfolio's cost shape, the CFO decides on the envelope. Vendor spend at scale: CFO decides, principal advises on technical alternatives.
- **Escalation path.** Cost-envelope disagreement resolves in the quarterly; if not resolvable, escalates jointly to the CAIO. Board-facing cost-narrative disagreement resolves before the board session; the principal does not surprise the CFO in a board sub-committee.
- **Artifact flow.** The strategy one-pager's what-we-ask-of-leadership section, the bet-portfolio cost defence, the multi-year investment envelope, and the current-cycle capacity forecast all flow both directions.

**Signs the contract is not being held.** The capacity envelope in the strategy one-pager is a number the CFO has not seen. Cloud-spend surprises land in a board deck. The CFO defends a bet in front of the board with a talk-track the principal has not vetted. A bet ships with a cost curve the CFO cannot underwrite.

## The three cross-counterpart disciplines

Beyond the per-counterpart contracts, three disciplines cut across all four.

### Discipline 1 — Never surprise your peer

The single sharpest test of a partnership contract in the room is *did the peer know this was coming?* A CAIO who is surprised by a bet in a CTO review, a Head of AI Governance who is surprised by a policy activation in a risk-committee session, a CISO who is surprised by an ML-specific threat surface in an incident post-mortem, a CFO who is surprised by a capacity envelope on a board slide — each is the principal *not holding the contract*.

The corrective is the standing cadence itself. Every counterpart's calendar entry exists so that no substantive item ever reaches a decision-room without having been walked through the 1:1 first. If a bet is going to reach the CTO's review, the CAIO knows by two weeks prior; the Head of AI Governance knows by two weeks prior if the bet touches policy; the CISO knows by two weeks prior if the bet has a novel threat surface; the CFO knows by two weeks prior if the bet moves the capacity envelope. Chapter 4 § *pre-read distribution* walks the mechanics.

### Discipline 2 — The peer's authority is what you borrow, not what you replace

The four peers' formal authority is the mechanism the principal *uses* to make ratifications stick. This is the operational meaning of *influence without authority*: the principal converges the peer executives on a direction, and the peer executives *use their authority* to commit the org against it. The CAIO commits headcount. The CFO underwrites the envelope. The Head of AI Governance signs the policy alignment. The CISO signs the risk model.

A principal who treats the partnership as *"the CAIO will do what I say"* has misunderstood the direction. The peer's authority is theirs to exercise; the principal's job is to make it easy and defensible for them to exercise it in the direction the principal is arguing for. The distinction shows up in artifact language — a partnership-holding principal writes *"the CAIO commits X"*, not *"the CAIO will approve X"*.

### Discipline 3 — Version and refresh the contract, don't wing it

The partnership contract is a document. Version it. Refresh it annually. Refresh it out-of-cycle when either scope shifts — a new CAIO joins, the Head of AI Governance's regulatory obligations expand, the CFO's investment framework changes, the principal's own scope shifts. Mod-503 chapter 8 § *"the seams are versioned like everything else"* extends to the executive-branch seams; the four contracts are not exempt.

The practical form: each contract is a one-to-two-page document, stored in a shared location the peer can find, versioned semi-formally (v1.0, v1.1), with a *last refreshed* date and an *effective through* date. The annual refresh is a joint session — the principal and the peer walk through the current contract, note what has shifted, and ratify the next version. Exercise-02 walks the drafting.

## The four contracts as a system

The four contracts are not independent. Read them together.

- **CAIO + governance overlap.** The strategy one-pager (co-authored with the CAIO) cites the policy-to-contract mapping (co-authored with the Head of AI Governance). When the two peers disagree on a bet's direction — the CAIO wants to accelerate a Gen-AI bet the Head of AI Governance flags as policy-unmapped — the principal is the *technical mediator* who proposes the deferred-launch or tiered-rollout path (chapter 6).
- **CAIO + CFO overlap.** The strategy one-pager's *what we ask of leadership* section (co-authored with the CFO) sits in the same artifact the CAIO co-authors. The two peers ratify the same capacity envelope; the principal is the *authorial* seam.
- **Governance + CISO overlap.** Regulatory obligations (governance) and security controls (CISO) share the same target — model, data, and inference artifacts. The joint quarterly threat-modelling session is co-attended by both peers.
- **All four at the strategy semi-annual.** The strategy refresh cycle (mod-502 chapter 5 § *the refresh cadence*) is a milestone the four counterparts converge at. The principal runs a *four-peer walkthrough* at the semi-annual — the strategy one-pager is walked to each peer in a dedicated session, and their edits are consolidated before the SVP / CTO review that follows.

## The four contracts as portfolio, not tasks

A first-cycle principal treats the four contracts as *four things to schedule* — four sets of 1:1s to hold. This is the mechanics; it is not the practice.

The practice is that the four contracts, together, are the *engine that converts technical direction into org-wide ratified execution*. The principal is the axle; the four peers are the wheels; the coalition of staff engineers, VPs, and product leaders below the four is the road. When the contract is being held, the coalition (chapter 4) does not have to route the principal through every ratification — the peer executive branch is already carrying the direction into the rooms the principal is not in.

Signs the contracts are working as a portfolio:

- The CAIO defends the strategy to the board with the principal's framing but in the CAIO's own words.
- The Head of AI Governance signs a policy the principal has already reflected as a contract invariant, in the same refresh cycle.
- The CISO's threat-modelling calendar includes the mod-502 bet portfolio without the principal having to re-brief every cycle.
- The CFO's board-facing capacity narrative uses the strategy one-pager's *what we ask of leadership* section verbatim.
- The four peers reference *each other's* co-authored artifacts unprompted — the CAIO cites the governance policy mapping; the CFO cites the risk-tier taxonomy; the CISO cites the strategy's non-goals.

When those signs are present, the "influence without authority" mechanism is working. When they are absent, one or more of the contracts has drifted, and the escalation load (chapter 6) is about to spike.

## Summary

- The peer executive branch is four counterparts: CAIO / Head of AI (owned by `chief-ai-officer-learning`), Head of AI Governance (owned by `head-of-ai-governance-learning`), CISO, and CFO. Each is a *peer* at the ratification table, not an audience and not an escalation target.
- The partnership contract with each is a short document that names, per peer: what the principal brings, what the peer brings, the cadence, the authorship and ratification rights, the decision rights, the escalation path, and the artifact flow. Exercise-02 authors the four.
- Three cross-counterpart disciplines: never surprise your peer; borrow their authority rather than replace it; version and refresh the contract like any other artifact.
- The four contracts are a portfolio, not four sets of 1:1s. Read together, they are the engine that converts the mod-502 strategy and the mod-503 architecture into ratified, executed direction across the org.
- Chapter 4 walks the coalition sequence the contracts operate over. Chapter 6 walks the escalation protocol that runs through them. Mod-503 chapter 8 (seam discipline) is the peer chapter on the platform-side.
