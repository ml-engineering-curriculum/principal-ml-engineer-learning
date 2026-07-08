# Three Role Families at Level 48+: IC-Principal, Executive, Research-Principal

> Chapter 4 of mod-501. Prerequisite: chapter 2 (reading a posting) and chapter 3 (title map). This chapter draws the three-way boundary that determines whether a level-48+ posting belongs to this track at all.

## Why this chapter exists

Level 48 is not a single ladder rung on a single ladder. In ML orgs three distinct level-48+ role families coexist, and postings from all three sometimes wear each other's title vocabulary. The IC-principal path (this track), the executive path, and the research-principal path each demand a different multi-year investment. A learner who mistakes one for another spends time preparing for the wrong interview loop, the wrong artifacts, and the wrong career trajectory.

This chapter names the three families, gives you the tells that separate them on sight, and points at the peer tracks in this ecosystem that own the two non-IC-engineering paths.

## The three families

### Family 1 — Principal Machine Learning Engineer (this track)

**Level:** 48. **Ladder:** ML engineering IC. **Direct reports:** none. **Ownership:** the ML org's technical direction across product areas; the north-star applied-ML architecture; the technical bar the ML org calibrates against; cross-org influence up to SVP / CTO without authority; multiplier effect on every ML team; industry voice for the ML function.

Owned in this ecosystem by: `principal-ml-engineer-learning` — this repo.

Load-bearing verb-object signals (from chapter 1 and chapter 2):

- "set the technical North Star for ML across engineering" (SoundCloud)
- "north-star platform architecture with living diagrams and canonical APIs" (Capital One)
- "influence cross-functional stakeholders up to the SVP level" (Capital One)
- "multiply the effectiveness of every ML team" (Upstart)
- "operate as a senior individual contributor … without direct authority" (Bumble)

### Family 2 — Head of AI / VP of ML / Chief AI Officer (executive branch)

**Level:** 48+ (executive tier — the level scaffolding differs from the IC ladder). **Ladder:** people management / executive. **Direct reports:** yes — managers and, at CAIO / VP altitude, managers-of-managers. **Ownership:** the ML org's headcount and budget; hiring plans and comp bands; roadmap commitment to executive peers; board reporting cadence; the org's public AI narrative; regulatory sign-off with the CISO / CPO / General Counsel; P&L (at CAIO altitude).

Owned in this ecosystem by: `chief-ai-officer-learning` and `head-of-ai-governance-learning`.

Load-bearing verb-object signals (from the exec-branch tracks; illustrative, not a full catalogue):

- "own the ML org's P&L for FY27"
- "hire, coach, and manage the VP of ML Platform and the VP of Applied ML"
- "represent the AI function to the board of directors quarterly"
- "own the multi-year AI investment plan approved by the CEO and CFO"
- "sign off on the AI-risk register jointly with the CISO"
- "own the headcount plan across the ML function"

Notice the verbs stay the same as the IC-principal family — `own`, `set`, `influence` — but the objects shift from `technical direction across product areas` to `P&L`, `headcount`, and `board reporting cadence`. Chapter 1's table is the reference.

### Family 3 — Principal Research Scientist / Distinguished Applied Scientist (research branch)

**Level:** 48 (research-track IC; the level scaffolding at AI labs differs from either the exec branch or the engineering IC branch). **Ladder:** research IC. **Direct reports:** typically none at the Principal Research Scientist tier; sometimes small research teams at Distinguished Applied Scientist tier. **Ownership:** the research agenda; state-of-the-art results on benchmarks; first-author publications at top-tier ML venues; pretraining-objective invention; new architectures; theoretical grounding for capabilities.

Owned in this ecosystem: not yet — no track. Flagged as a research-only branch in [`../../JOB_REQUIREMENTS.md`](../../JOB_REQUIREMENTS.md).

Load-bearing verb-object signals (illustrative — no postings from the 2026-Q2 sample belong here; documented from the role definition and public postings at Anthropic, OpenAI, DeepMind, Google Research, Meta AI):

- "publish state-of-the-art on <benchmark>"
- "invent new pretraining objectives"
- "lead the research direction on <capability>"
- "author first-author submissions to ICML / NeurIPS / ICLR"
- "advise the research agenda across the lab"

The applied-ML engineering-track industry-influence artifacts (KDD industry track, O'Reilly AI, engineering blogs) are *not* the same as first-author top-tier ML conference submissions. Mod-506 in this track explicitly bounds itself to the engineering-track publication venues, not the research-track ones, because that's where the 2026-Q2 evidence sits.

## How to classify a posting

Given a posting titled `Principal ML Engineer`, `Distinguished AI Engineer`, `Head of AI`, `VP of ML`, or something similar, run the following classification:

**Step 1 — count the direct reports and budget signals.**

Scan for: "direct reports", "manage a team of", "hire, coach, and manage", "own the P&L", "own the budget", "headcount plan", "board reporting", "report to the CEO", "manage the (VP|Director) of".

- Zero of these signals across the whole posting → not Family 2. Continue.
- One or two, embedded in a mostly-technical posting → the hiring manager is confused. Ask in the recruiter screen which ladder this posting is really on. If they name a people-management track, it is Family 2.
- Three or more, dominating the responsibilities section → Family 2 (executive branch). Route to `chief-ai-officer-learning` or `head-of-ai-governance-learning`, not this track.

**Step 2 — count the state-of-the-art / publication signals.**

Scan for: "publish state-of-the-art", "first-author submissions", "invent new pretraining objectives", "novel architectures", "PhD required", "research agenda", "advise the research direction", "PhD dissertation on <topic>".

- Zero across the whole posting → not Family 3. Continue.
- Mixed: some publication expectations, applied-engineering framing dominant → likely a Distinguished Applied Scientist / Principal Applied Scientist hybrid at an AI lab or research-heavy product company. This is a peer track this ecosystem does not yet own; the closest engineering-track adjacent is this one, but the interview loop will emphasize first-author research artifacts. Track fit is uncertain.
- Three or more publication / research-agenda signals dominating the posting → Family 3 (research-principal). Not this track.

**Step 3 — confirm Family 1.**

If Family 2 and Family 3 are both ruled out, run the chapter 2 scan for the four principal-scope themes and confirm the load-bearing verb-object altitude sits at the IC-principal tier (`the ML org's technical direction across product areas`, `the north-star applied-ML architecture`, `the technical bar the ML org calibrates against`, SVP / CTO influence without authority). If yes, this posting is Family 1. This track's material is the right investment.

## The hybrid trap

Two common hybrid patterns to watch for:

**Hybrid A — IC-principal that grew a small team.** Some employers give a titled Principal ML Engineer 2–4 direct reports (usually a very small research or "special projects" team). This is a hybrid but stays predominantly Family 1 if the direct reports are a small fraction of the total scope and the load-bearing sentences remain technical (North Star, architecture, bar, cross-org influence). The posting will typically call it out explicitly ("may occasionally have direct reports"). Track fit is Family 1 with the caveat that if the team grows, the trajectory bends toward Family 2.

**Hybrid B — VP that likes to code.** Some executive-branch postings put technical bullets in the top half ("set the North Star", "unified architecture") because the hiring manager wants a technical VP. The bottom half then has all the executive-branch bullets (P&L, headcount, board reporting). The technical bullets are aspirational — the actual scope is Family 2. Route accordingly.

The reliable test is the direct-reports and budget signals from step 1. When they exist and dominate, the role is Family 2 no matter how technical the top half of the JD sounds.

## Trajectories from Family 1

The IC-principal ladder does not extend indefinitely as a canonical ladder in the 2026-Q2 sample. A learner at Family 1 has, in practice, four progressions after multi-year time-in-role — cited in [`../../CURRICULUM.md`](../../CURRICULUM.md) already but worth repeating here as part of the boundary drawing:

- **Stay Family 1, deepen** — the modal outcome. Larson's *Staff Engineer* interviews and the StaffEng.com Distinguished / Fellow archetype describe the same thing. The north-star architecture evolves through multiple bets; the technical bar the ML org calibrates against gets tightened over years; industry-influence artifacts accumulate.
- **Slide to Family 2** — take on direct reports, headcount, and board reporting. Path defined by `chief-ai-officer-learning` and `head-of-ai-governance-learning`.
- **Slide to peer platform-side principal** — [`ai-infra-principal-engineer-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-engineer-learning) and [`ai-infra-principal-architect-learning`](https://github.com/ai-infra-curriculum/ai-infra-principal-architect-learning) own the platform-side principal path (level 50). Complementary scope: platform vs. modelling.
- **Slide to Family 3** — take a Principal Research Scientist / Distinguished Applied Scientist path at an AI lab. Requires a research-focused track record this ecosystem does not yet coach; not authored here.

If your target trajectory is Family 2, most of this track still applies (chapters mod-502 through mod-505 describe the technical-strategy skills a technical executive still needs), but the exec-branch tracks are the closer fit for the mod-506-scale investment.

## The IC-only guardrail

This track presumes IC-only. When you complete the four principal-scope themes and the three capstone projects, the artifact portfolio you carry is designed for an IC-principal interview loop, not a VP interview loop. The staff-plus hiring-loop calibration you practice in mod-505 is IC-principal-scope (calibrating peer staff engineers and staff-plus interview loops), not exec-scope (calibrating a manager cohort). The exec-audience narrative you practice in mod-504 targets *convincing* SVPs and CTOs, not *becoming* one.

If you are aiming at Family 2, layer `chief-ai-officer-learning` on top of this track once you finish mod-504.

## Summary

- Three level-48+ role families coexist in ML orgs: IC-principal (this track), executive branch (CAIO / VP / Head of AI, owned by peer tracks), and research-principal (Principal Research Scientist / Distinguished Applied Scientist, no owner in this ecosystem).
- The classification test runs in three steps: direct-reports / budget signals (Family 2 tell), publication / research-agenda signals (Family 3 tell), then verify chapter 2's principal-scope theme pattern (Family 1 confirm).
- Hybrids exist. When they do, the direct-reports and budget signals decide.
- Trajectories from Family 1: stay Family 1 (modal), slide Family 2, slide platform-side principal, slide Family 3.
- The mod-506 external-voice module bounds itself to engineering-track publication venues; research-track venues belong to Family 3.
