# AetherPolicy — Investigation Report

**Version:** 0.1.0
**Date:** 2026-11-14
**Author:** Samir Baladi
**ORCID:** [0009-0003-8903-0029](https://orcid.org/0009-0003-8903-0029)
**Status:** Investigation report. Not a result.

---

## 0. Purpose

This report documents the investigation of AetherPolicy, the candidate ninth project of the Aether family, from Phase 0 to Phase 4.

It records:
- What was done.
- What was found.
- What was not found.
- What the decision is.

It does not replace the paper (`AetherPolicy_Research_Paper.pdf`). It is a companion document.

---

## 1. Summary

| Item | Result |
|---|---|
| Project | AetherPolicy — candidate ninth project of the Aether family |
| Phase | Paused at Phase 4 (Independence Decision) |
| Decision | **(E) undetermined (interim)** |
| Implementation | None |
| Experiments | None |
| Independent review | Not started |
| Paper | Published on Zenodo (10.5281/zenodo.24160047) and Figshare (10.6084/m9.figshare.35009833) |

---

## 2. Phases completed

### Phase 0 — Architectural Hypothesis

**Output:** `ARCHITECTURAL_HYPOTHESIS.md`.

**What was done:** The hypothesis was stated. Five functions (Fn1–Fn5) were proposed as initial scope. Four boundaries (AetherGovern, AetherIdentity, AetherRuntime, AetherPolicy) were named. The hypothesis was made falsifiable.

**What was found:** The hypothesis is falsifiable in principle. The functions were chosen after the observations, which is a selection bias (threat T3).

### Phase 1 — Responsibility Mapping

**Output:** `research/RESPONSIBILITY_BOUNDARIES.md`.

**What was done:** The actual surface of the eight existing records was mapped against the five functions. Three "Unclear" cells were identified (AetherGovern vs Evaluation, Enforcement, Conflict Resolution).

**What was found:** The matrix makes the gap explicit. But the "Unclear" cells are the author's uncertainty, not a measured result. The matrix is coarse.

### Phase 2 — Hypothesis Review

**Output:** `REVIEW/INTERNAL_REVIEW.md` (internal, not independent).

**What was done:** The hypothesis, the matrix, the plan, and the decision were reviewed by the author.

**What was found:** The review is internal, not independent. It records what the author can see, and where the author's judgement may be unreliable. It does not replace independent review.

### Phase 3 — Falsification Design

**Output:** `FALSIFICATION/FALSIFICATION_PLAN.md`.

**What was done:** Five conditions (P-F1 to P-F5) were stated. Each condition was stated so that it can fail. P-F5 was marked as untested.

**What was found:** The plan is well-designed but unexecuted. It specifies what would count as failure, not what the result is.

### Phase 4 — Independence Decision

**Output:** `DECISIONS/INDEPENDENCE_DECISION.md`.

**What was done:** The evidence was reviewed. The decision was recorded.

**What was found:** **(E) undetermined (interim).** The evidence is insufficient to accept AetherPolicy as an independent dimension, and insufficient to reject it.

---

## 3. What the investigation found

### 3.1 What supports the candidate

- **The matrix shows a gap.** The "Unclear" cells in AetherGovern are not a measured result, but they are a candidate gap.
- **The plan is falsifiable.** P-F1 to P-F5 are stated so that they can fail.
- **The decision is honest.** (E) undetermined is not a failure; it is a statement that the evidence is insufficient.

### 3.2 What does not support the candidate

- **The evidence is the author's reading.** The matrix, the plan, and the decision are by the same author.
- **P-F3 is fragile.** Two of five functions straddle the boundary with governance.
- **P-F1 is partly falsified** for Definition and Revocation.
- **P-F5 is untested.** No benefit has been observed.
- **No independent review has been done.**

### 3.3 What the investigation did not find

- **No counter-example** to P-F1, P-F2, P-F3, or P-F4.
- **No demonstration** that AetherGovern already evaluates, enforces, or resolves.
- **No demonstration** that the five functions can be reduced to fewer than five.
- **No experiment** (Phase 5 and 6, not permitted).

---

## 4. The decision

**(E) undetermined (interim).**

The evidence is insufficient to accept AetherPolicy as an independent dimension, and insufficient to reject it. A test is needed to decide.

The most fragile condition is **P-F3** (boundary with governance). The condition most likely to fail is **P-F5** (observable benefit), because it has not been tested.

---

## 5. What would change the decision

| Target classification | What would be needed |
|---|---|
| **(A) Independent** | Independent review that finds the functions not covered; or an experiment (Phase 5–6, not permitted). |
| **(B) Feature of AetherGovern** | Evidence that AetherGovern evaluates, enforces, and resolves. |
| **(C) Feature of AetherRuntime** | Evidence that AetherRuntime enforces and revokes. |
| **(D) Bounded extension** | A construction showing that a bounded addition covers all five functions. |
| **(E) Undetermined** | Current state. |

---

## 6. What remains open

- Independent review (Phase 2).
- Specification (Phase 5, not permitted).
- Implementation (Phase 6, not permitted).
- Evaluation (Phase 7, not permitted).

---

## 7. Recommendations

1. **Obtain independent review.** This is the most useful next step. The author cannot provide it.
2. **If independent review is not obtained within a reasonable period, pause the project indefinitely.** "Undetermined" should not become a permanent state.
3. **Do not proceed to Phase 5** (specification) on the current evidence.
4. **Do not claim** that AetherPolicy is an independent dimension. The evidence does not support it.

---

## 8. Relationship to AetherIdentity

AetherIdentity reached Phase 4 with **F1–F4 not falsified, F5 untested**, and proceeded to Phase 5 (implementation) because its argument was stronger and its F1–F4 assessment was reviewed.

AetherPolicy's argument is weaker:
- P-F3 is more fragile than AetherIdentity's F3.
- P-F1 is partly falsified for two of the five functions.
- P-F4 has a policy-specific residual that AetherIdentity does not have.

The asymmetry is not a criticism of AetherPolicy. It is a statement about the evidence.

---

## 9. Summary

| Question | Answer |
|---|---|
| What was investigated? | Whether AetherPolicy is an independent architectural dimension. |
| What was found? | A candidate gap, but the evidence is the author's reading. |
| What is the decision? | (E) undetermined (interim). |
| What is the next step? | Independent review. |
| What should not happen? | Proceeding to specification or implementation on the current evidence. |

**AetherPolicy is a candidate, not a result.**
