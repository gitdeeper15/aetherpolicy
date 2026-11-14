# 🛡️ AetherPolicy — Research Repository

### Decentralized Policy Lifecycle and Enforcement for Autonomous Agent Systems

*A Falsification-First Investigation of Policy Definition, Evaluation, Enforcement, Revocation, and Conflict Resolution in Multi-Agent Software Ecosystems*

---

[![DOI Zenodo](https://zenodo.org/badge/DOI/10.5281/zenodo.24160047.svg)](https://doi.org/10.5281/zenodo.24160047)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--8903--0029-a6ce39)](https://orcid.org/0009-0003-8903-0029)
[![Status](https://img.shields.io/badge/Status-Architectural%20Investigation-blue)]()
[![Version](https://img.shields.io/badge/Version-0.1.0-green)]()
[![Phase](https://img.shields.io/badge/Phase-4%20(Undetermined)-amber)]()
[![DOI Figshare](https://img.shields.io/badge/DOI%20Figshare-10.6084%2Fm9.figshare.35009833-blue)](https://doi.org/10.6084/m9.figshare.35009833)

---

> **Status: Architectural Investigation.**
> This is a **research repository**, not a software repository.
> No implementation is planned unless the architectural investigation supports it.
> **Decision: (E) undetermined (interim).**
> See [`DECISIONS/INDEPENDENCE_DECISION.md`](DECISIONS/INDEPENDENCE_DECISION.md).

> *"AetherPolicy is a candidate, not a result."*

---

## Table of Contents

- [Overview](#overview)
- [Central Question](#central-question)
- [Five Functions](#five-functions-initial-scope)
- [Failure Conditions](#failure-conditions-p-f1-to-p-f5)
- [Propositions](#propositions-p1-p2)
- [Decision (Phase 4)](#decision-phase-4)
- [Repository Structure](#repository-structure)
- [Phase Status](#phase-status)
- [What This Repository Does Not Claim](#what-this-repository-does-not-claim)
- [Related Aether Projects](#related-aether-projects)
- [Figures](#figures)
- [Research Status](#research-status)
- [Author](#author)
- [License](#license)

---

## Overview

**AetherPolicy** is the **ninth project (candidate)** of the Aether family. It investigates whether a decentralized policy lifecycle gap genuinely exists between governance authority (AetherGovern) and runtime monitoring (AetherRuntime).

**AetherPolicy is not a replacement for AetherIdentity** (the eighth project). AetherIdentity remains the eighth project, with its architectural independence still unresolved.

This repository is a **research repository**. It contains no `src/`, no `tests/`, no `experiments/`. It will not contain them unless the investigation concludes that AetherPolicy is independent.

**The paper (v0.1.0) is published on Zenodo:** [10.5281/zenodo.24160047](https://doi.org/10.5281/zenodo.24160047).
**Mirror on Figshare:** [10.6084/m9.figshare.35009833](https://doi.org/10.6084/m9.figshare.35009833).

---

## Central Question

> How can policies be transformed from declarative rules into evaluable, enforceable, and revocable operational constraints across decentralized autonomous agent systems?

The central question has four clauses, mapping to the failure conditions:

| Clause | Condition |
|---|---|
| (i) Not already specified | P-F1 |
| (ii) Does not decompose into AetherGovern and AetherRuntime | P-F2, P-F3 |
| (iii) No central policy decision point | P-F4 |
| (iv) Observable benefit | P-F5 |

A positive answer needs all four. A negative answer on any one is sufficient to reject the candidate.

---

## Five Functions (Initial Scope)

The paper labels the functions **Fn1–Fn5** (not P1–P5), to avoid a clash with the propositions P1–P2 and the failure conditions P-F1 to P-F5.

| # | Function | Question |
|---|---|---|
| **Fn1** | Policy Definition | How is a policy expressed as a rule that can be evaluated? |
| **Fn2** | Policy Evaluation | How is a policy determined to apply to an action and its context? |
| **Fn3** | Policy Enforcement | How is a disallowed action prevented or restricted? |
| **Fn4** | Policy Revocation | How is an authorization withdrawn during operation? |
| **Fn5** | Policy Conflict Resolution | How are conflicting policies resolved? |

These five are **not** assumed to be complete, independent, or necessary.

---

## Failure Conditions (P-F1 to P-F5)

| ID | Claim under test | Status |
|:-:|---|:-:|
| **P-F1** | Non-redundancy | 🟡 Not falsified (author's reading of own records) |
| **P-F2** | Orthogonality to verification and governance | 🟡 Not falsified (remainder may be small) |
| **P-F3** | Boundary with governance | 🟡 Not falsified (**most fragile**) |
| **P-F4** | Decentralizability | 🟡 Not falsified (with residuals: revocation window, honest enforcer) |
| **P-F5** | Observable benefit | 🔴 **Untested** |

> **"Not falsified" is a weaker status than "confirmed". "Untested" is not a pass.**
> The paper's decision rule: the candidate is accepted as an independent dimension only if all five conditions have been tested and none falsified, with P-F5 supported by measured results. With four conditions not falsified by argument alone, one untested, and one fragile, the third case applies: **(E) undetermined**.

---

## Propositions P1–P2

| # | Proposition | Status |
|:-:|---|---|
| **P1** | Determinism of local policy evaluation | Proof sketch (near-trivial; content in the purity conditions) |
| **P2** | Irreducible conflict-resolution anchor | Proof sketch (symmetry argument; small model) |

**P1** is close to trivial: it says that a pure function of its inputs is a function of its inputs. Its content is in the conditions (Pur1–Pur4), which real policy engines can violate.

**P2** states that any deterministic, binary conflict-resolution function rests on an asymmetric rule that the conflicting policies cannot supply: an irreducible anchor. The anchor is a decision about standing, which the paper notes is plausibly a governance matter. This cuts **against** independence.

Neither is machine-checked.

---

## Decision (Phase 4)

**AetherPolicy is classified as (E) undetermined (interim).**

The evidence is insufficient to accept AetherPolicy as an independent dimension, and insufficient to reject it. A test is needed to decide. See [`DECISIONS/INDEPENDENCE_DECISION.md`](DECISIONS/INDEPENDENCE_DECISION.md).

**Why insufficient to accept:**
- P-F5 is untested: no benefit has been observed.
- P-F3 is fragile: two of five functions straddle the boundary with governance.
- The attempts at P-F1 and P-F2 are arguments by the author about the author's own records.
- The propositions are small (P1 near-trivial; P2 cuts against independence).
- AetherIdentity, which supplies one of the three inputs, is itself unresolved.

**Why insufficient to reject:**
- No failure condition has been falsified.
- The comparison found a remainder after composition with the neighbours (P-F2).
- The decentralization argument did not reach a requirement for a central decision point (P-F4).
- The rejection would rest on the same author's reading that is here judged insufficient to accept.

**"Undetermined" is not a failure.** It states that the evidence is insufficient to decide, and names what is missing.

---

## Repository Structure

```text
AetherPolicy/
│
├── README.md
├── ARCHITECTURAL_HYPOTHESIS.md
├── ROADMAP.md
├── CHANGELOG.md
├── PROJECT_SUMMARY.txt
├── CITATION.cff
├── AUTHORS.md
├── CONTRIBUTING.md
├── VERSION
├── manifest.json
├── scientific_state.json
├── LICENSE
│
├── research/
│   └── RESPONSIBILITY_BOUNDARIES.md
│
├── FALSIFICATION/
│   └── FALSIFICATION_PLAN.md
│
├── DECISIONS/
│   └── INDEPENDENCE_DECISION.md
│
├── REVIEW/
│   └── INTERNAL_REVIEW.md  (internal, not independent)
│
├── REFERENCES/
│   └── (to be populated with the 29 references from the paper)
│
├── docs/
│   └── figures/
│       ├── Fig1_Nine_Dimensions.png
│       ├── Fig2_Policy_Lifecycle.png
│       ├── Fig3_Five_Functions.png
│       ├── Fig4_Boundaries.png
│       ├── Fig5_Falsification_Procedure.png
│       ├── Fig6_Phase_Status.png
│       ├── Fig7_Decision_Outcomes.png
│       ├── Fig8_Overlap_Matrix.png
│       └── Fig9_Evaluation_Design.png
│
└── REPORTS/
    └── architectural_investigation/
        └── investigation_report.md
```

No src/, no tests/, no experiments/.

---

Phase Status

Phase Status
0 — Architectural Hypothesis ✅ Complete (ARCHITECTURAL_HYPOTHESIS.md)
1 — Responsibility Mapping ✅ Complete (research/RESPONSIBILITY_BOUNDARIES.md)
2 — Falsification Design ✅ Complete (FALSIFICATION/FALSIFICATION_PLAN.md)
3 — Independent Review ⏳ Not started (REVIEW/INDEPENDENT_REVIEW.md; internal review in REVIEW/INTERNAL_REVIEW.md)
4 — Independence Decision ⚠️ Interim: (E) undetermined (DECISIONS/INDEPENDENCE_DECISION.md)
5 — Architectural Specification ❌ Not permitted
6 — Reference Implementation ❌ Not permitted

Note: The paper's Figure 6 shows Phase 2 (Hypothesis Review) as not started although Phase 3 (Falsification Conditions) is complete. The paper keeps the order and notes the consequence: no independent review has taken place, and the failure conditions were stated and attempted by the author alone. This is threat T1.

---

What This Repository Does Not Claim

· That AetherPolicy is an independent architectural dimension.
· That the five functions are complete, independent, or necessary.
· That the boundaries with AetherGovern, AetherIdentity, and AetherRuntime are sufficient.
· That the gap is genuine.
· That implementation should begin.
· Any observed benefit (P-F5 is untested).
· Any causal effect.

---

Related Aether Projects

# Project Status DOI
1 AetherGit Foundational 10.5281/zenodo.23976986
2 AetherFlow Foundational 10.5281/zenodo.23979129
3 AetherProof Foundational 10.5281/zenodo.24013124
4 AetherMesh Foundational 10.5281/zenodo.24038038
5 AetherGovern Foundational 10.5281/zenodo.24054524
6 AetherRuntime Foundational 10.5281/zenodo.24078477
7 AetherOrchestrate Foundational 10.5281/zenodo.24095399
8 AetherIdentity Candidate (paper + v2.0.0) 10.5281/zenodo.24102739
9 AetherPolicy Candidate (paused at phase 4) 10.5281/zenodo.24160047

---

Figures

# Figure Description
1 docs/figures/Fig1_Nine_Dimensions.png The nine functional dimensions of the Aether family
2 docs/figures/Fig2_Policy_Lifecycle.png The policy lifecycle in AetherPolicy
3 docs/figures/Fig3_Five_Functions.png The five functions of AetherPolicy (Fn1–Fn5)
4 docs/figures/Fig4_Boundaries.png AetherPolicy and its boundaries
5 docs/figures/Fig5_Falsification_Procedure.png The falsification procedure (P-F1 to P-F5)
6 docs/figures/Fig6_Phase_Status.png Phase status (paused at Phase 4)
7 docs/figures/Fig7_Decision_Outcomes.png The five Phase 4 outcomes and the evidence each needs
8 docs/figures/Fig8_Overlap_Matrix.png Overlap of the five functions with existing records
9 docs/figures/Fig9_Evaluation_Design.png Scenarios mapped to metrics and failure conditions

Figures 1–6 are redrawn from the draft. Figures 7–9 are supplementary additions.

---

Research Status

Item Status
Project AetherPolicy — candidate ninth project of the Aether family; does not replace AetherIdentity
Phase Paused at Phase 4 (Independence Decision)
Decision (E) Undetermined: the argument is insufficient to accept and insufficient to reject
Propositions P1 (near-trivial) and P2 stated as proof sketches; not machine-checked
Failure conditions P-F1, P-F2, P-F3, P-F4 not falsified by argument; P-F3 most fragile; P-F5 untested
Implementation None
Experiments None executed; Section 9 of the paper is a proposal
Independent review Not started (Phase 2)
Claims not made Independence of the dimension; completeness of the five functions; sufficiency of the boundaries; any observed benefit; any causal effect

---

Author

Samir Baladi
Interdisciplinary AI Researcher, Ronin Institute / Rite of Renaissance

 
Email gitdeeper@gmail.com
ORCID 0009-0003-8903-0029
GitHub gitdeeper15/aetherpolicy
GitLab gitlab.com/gitdeeper15/aetherpolicy
Codeberg codeberg.org/gitdeeper15/aetherpolicy
Bitbucket bitbucket.org/gitdeeper15/aetherpolicy
Website aetherpolic-y.netlify.app
Zenodo 10.5281/zenodo.24160047

---

License

CC-BY-4.0 (this document).

---

AetherPolicy v0.1.0 — Architectural Investigation.
© 2026 Samir Baladi — Ronin Institute / Rite of Renaissance.
DOI: 10.5281/zenodo.24160047
