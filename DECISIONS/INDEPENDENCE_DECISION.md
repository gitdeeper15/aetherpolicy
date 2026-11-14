# AetherPolicy — Independence Decision

**Phase:** 4 (Independence Decision)
**Version:** 0.1.0
**Date:** 2026-11-11
**Input:** ARCHITECTURAL_HYPOTHESIS.md (Phase 1), FALSIFICATION.md (Phase 3)
**Status:** Decision. Not a result of experiment.

---

## 0. What this document decides

This document decides whether AetherPolicy is:

- **(A)** an independent architectural dimension;
- **(B)** a feature of AetherGovern;
- **(C)** a feature of AetherRuntime;
- **(D)** a bounded extension of AetherGovern, AetherRuntime, or both;
- **(E)** undetermined.

The decision is made **by argument**, not by experiment. It is provisional. It is subject to revision if Phase 6 (experiment) is ever reached.

---

## 1. Evidence reviewed

| Source | What it says |
|---|---|
| `ARCHITECTURAL_HYPOTHESIS.md` | States the gap, the five functions, the four boundaries. |
| `FALSIFICATION.md` | States P-F1 to P-F5. P-F1 to P-F4 are not falsified by argument, each with a reservation. P-F5 is untested. |
| `README.md` | States that AetherPolicy is a candidate, not a result. |

**No experiment has been run.** The decision is an argument, not a measurement.

---

## 2. Decision

**AetherPolicy is classified as (E) undetermined.**

The argument does not justify (A). It does not justify (B), (C), or (D) either. The state of the evidence is:

- **P-F3 is the most fragile condition.** If AetherGovern already evaluates and enforces policy, AetherPolicy is a feature of AetherGovern. The argument does not settle whether AetherGovern already does this.
- **P-F1 is partly falsified for Definition and Revocation.** AetherGovern already issues policy and revokes authority. The distinctive functions are Evaluation, Enforcement, and Conflict Resolution.
- **P-F4 has residuals that are shared with AetherIdentity**: the trust anchor, the revocation window, and a policy-specific residual (conflict resolution without a precedence order).
- **P-F5 is untested.** No observable benefit has been demonstrated.

A decision of (A) would require evidence that the five functions are not absorbed. That evidence does not exist. A decision of (B) would require evidence that AetherGovern absorbs the five functions. That evidence also does not exist.

**The honest classification is (E): undetermined.**

---

## 3. What "undetermined" means

Undetermined is **not** a failure. It is a statement that:

- The hypothesis is still open.
- The argument is not sufficient to accept it.
- The argument is not sufficient to reject it.
- A test is needed to decide.

Undetermined is **weaker** than "independent". It is **stronger** than "falsified".

---

## 4. What would change the decision

The decision would change to **(A) independent** if:

- An experiment (Phase 6) shows that AetherPolicy's five functions are not covered by AetherGovern + AetherRuntime + a bounded extension.
- Conflict resolution cannot be reduced to a precedence order.
- Enforcement and revocation cannot be reduced to halt orders.

The decision would change to **(B) feature of AetherGovern** if:

- AetherGovern's authority chains already evaluate and enforce policy.
- Conflict resolution is always a governance decision.

The decision would change to **(C) feature of AetherRuntime** if:

- AetherRuntime's monitoring already enforces and revokes policy.
- The five functions reduce to monitoring plus halt orders.

The decision would change to **(D) bounded extension** if:

- AetherGovern or AetherRuntime, with a bounded addition, covers all five functions.
- The addition is small enough to be a feature, not a dimension.

---

## 5. Consequences of "undetermined"

| Consequence | Status |
|---|---|
| Specification (`SPECIFICATION.md`) | Not written. |
| Implementation (`src/aetherpolicy/`) | Not built. |
| Test design (`TESTS.md`) | Not written. |
| Invariants (`INVARIANTS.md`) | Not written. |
| Experiment | Not run. |
| Publication | Not submitted. |

The project remains at **phase 4**. It does not proceed to phase 5.

---

## 6. What would justify proceeding

Proceeding to phase 5 (Specification) requires one of:

- An argument that (A) holds, stronger than the one in `FALSIFICATION.md`.
- An experiment that shows (A) holds.

The argument in `FALSIFICATION.md` is not strong enough. An experiment has not been run. Therefore the project does not proceed.

---

## 7. What this decision is not

- It is **not** a claim that AetherPolicy is useless.
- It is **not** a claim that AetherPolicy is redundant.
- It is **not** a final rejection.
- It is **not** a final acceptance.

It is a statement that the evidence is insufficient to decide, and that the project is paused at phase 4.

---

## 8. Next steps (optional)

If the project is to proceed, the next step is **Phase 2: Hypothesis Review** (`REVIEW.md`), followed by a re-examination of the argument in `FALSIFICATION.md`. If that re-examination is positive, the project may proceed to Phase 5 (Specification). If not, the project remains at phase 4.

**Stopping at phase 4 is a legitimate outcome.** The project does not need to be completed to be useful.

---

## 9. Relationship to AetherIdentity

AetherIdentity reached phase 4 (independence decision) with the status **not falsified on F1–F4, F5 untested**. It proceeded to phase 5 (implementation) because its argument was stronger, and because its F1–F4 assessment was reviewed.

AetherPolicy's argument is weaker:
- P-F3 is more fragile than AetherIdentity's F3.
- P-F1 is partly falsified for two of the five functions.
- P-F4 has a policy-specific residual that AetherIdentity does not have.

The asymmetry is not a criticism of AetherPolicy. It is a statement about the evidence.

---

## 10. Summary

| Question | Answer |
|---|---|
| Is AetherPolicy independent? | **Undetermined.** |
| Is it a feature of AetherGovern? | Not established. |
| Is it a feature of AetherRuntime? | Not established. |
| Is it a bounded extension? | Not established. |
| Should it proceed to specification? | **No**, not on the current argument. |
| Should it be abandoned? | **No.** Paused at phase 4. |

**Decision: (E) undetermined.**
