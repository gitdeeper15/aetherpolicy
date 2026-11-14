# AetherPolicy — Falsification Conditions

**Phase:** 3 (Falsification Conditions)
**Version:** 0.1.0
**Date:** 2026-11-11
**Input:** ARCHITECTURAL_HYPOTHESIS.md (Phase 1)
**Status:** Conditions, not results.

---

## 0. Purpose

This document defines the conditions under which AetherPolicy does **not** deserve to be a separate architectural dimension. Each condition is stated so that it can fail. None is assumed to fail or pass.

The conditions are **specific to AetherPolicy**. They are not copied from AetherIdentity's F1–F5. They are designed around the five functions (Definition, Evaluation, Enforcement, Revocation, Conflict Resolution) and the four boundaries (AetherGovern, AetherIdentity, AetherRuntime, AetherPolicy).

A condition is **not falsified** if an attempt to falsify it, by the stated means, did not succeed. "Not falsified" is weaker than "confirmed". No condition is confirmed by argument alone.

---

## 1. Decision rule

| Outcome | Meaning | Consequence |
|---|---|---|
| **Falsified** | The condition is met: AetherPolicy is redundant, reducible, centralizing, or has no observable benefit. | Fold into an existing dimension, narrow the scope, or drop. |
| **Not falsified (with reservation)** | The attempt did not succeed; the reservation says what could change this. | Candidate retained for further investigation. |
| **Untested** | The condition requires an experiment that has not been run. | Report as untested; do not promote to "not falsified". |

The status "confirmed" is **not used** for any condition in this document.

---

## 2. The five conditions (P-F1 to P-F5)

### P-F1 — Non-redundancy

**Falsified if:** every one of the five functions (Definition, Evaluation, Enforcement, Revocation, Conflict Resolution) is already provided by AetherGovern, AetherRuntime, or a bounded extension of exactly one of them.

**Attempt.** Map each function to the existing dimensions:

| Function | AetherGovern | AetherRuntime | Bounded extension of one? |
|---|---|---|---|
| Definition | Authority to issue | — | — |
| Evaluation | ? | ? | ? |
| Enforcement | ? | Monitoring, halt orders | ? |
| Revocation | Revocation of authority | Halt orders | ? |
| Conflict resolution | Policy precedence? | — | ? |

**Reservation.** If AetherGovern's authority chains already evaluate policy applicability and enforce it, then P-F1 is falsified. If AetherRuntime's monitoring already enforces and revokes, then P-F1 is falsified. The attempt here is an argument that they do not; it is not a construction of the absorbing extension.

**Status.** Not falsified (with reservation).

---

### P-F2 — Orthogonality to verification and governance

**Falsified if:** every policy decision (definition, evaluation, enforcement, revocation, conflict resolution) can be encoded as a verified claim in AetherProof or as a governance decision in AetherGovern.

**Attempt.** Some policy facts are checkable: a rule is well-formed; a decision follows from a rule and a fact. These are properties of artifacts and belong with AetherProof. Others are not: whether a policy applies to an action in context is not decidable from cryptographic evidence alone; conflict resolution between policies from different issuers is not a property of a single artifact; and revocation during operation is a lifecycle event that AetherProof does not model.

**Reservation.** If conflict resolution is always reducible to a precedence order issued by AetherGovern, then P-F2 is falsified for that function. If enforcement is always reducible to a halt order issued by AetherRuntime, then P-F2 is falsified for that function.

**Status.** Not falsified (with reservation).

---

### P-F3 — Boundary with governance

**Falsified if:** AetherPolicy reduces to AetherGovern plus conventional verification.

**Attempt.** AetherGovern issues policy; AetherPolicy evaluates and enforces it. The boundary is porous: if AetherGovern's authority chains already evaluate and enforce, AetherPolicy is a feature of AetherGovern. If AetherGovern's revocation already covers policy revocation, AetherPolicy adds nothing on revocation. The contested region is **conflict resolution**: whether two policies from different issuers conflict, and how the conflict is resolved, is not obviously a governance decision (governance issues policy; it does not necessarily arbitrate between policies).

**Reservation.** This is the most fragile condition. If AetherGovern's principals are simply keys and its chains already attenuate and resolve conflicts, then AetherPolicy reduces to AetherGovern. What would remain distinctive is the **operational lifecycle** (evaluation, enforcement, revocation as events), not the authority to issue.

**Status.** Not falsified (with reservation). **Most fragile.**

---

### P-F4 — Decentralizability

**Falsified if:** any design that preserves the five functions needs a central authority or strong consistency.

**Attempt.** Most policy functions are deterministic functions of the admitted set:
- Definition: a signed record.
- Evaluation: a deterministic function of the record, the action, and its context.
- Enforcement: a deterministic function of evaluation.
- Revocation: a signed record; effect is antitone.
- Conflict resolution: a deterministic function of a precedence order, if one is issued.

The residuals are: (i) who resolves conflicts when no precedence order exists; (ii) how enforcement reaches a node that has not yet received the policy; (iii) how revocation reaches a node that has not yet received it. These are the same residuals as AetherIdentity's F4 (anchor, fork resolution, recovery, single-instance), plus a **policy-specific** residual: **conflict resolution without a precedence order**.

**Reservation.** The trust anchor, the revocation window, and conflict resolution without precedence cannot be removed by architectural design alone. If conflict resolution always requires a central arbiter, P-F4 is falsified for that function.

**Status.** Not falsified (with reservation). **Hardest condition.**

---

### P-F5 — Observable benefit

**Falsified if:** no scenario class can be constructed in which the best existing baseline fails and AetherPolicy succeeds.

**Attempt.** None; the condition needs an experiment, and no experiment has been run.

**Reservation.** Scenario classes chosen by the proposer risk circularity. Baselines must include AetherGovern plus AetherRuntime, and a composition of existing policy mechanisms.

**Status.** Untested.

---

## 3. Provisional assessment

| Condition | Status | Reservation (summary) |
|---|---|---|
| P-F1 Non-redundancy | Not falsified | Definition, revocation, conflict resolution may be absorbed |
| P-F2 Orthogonality | Not falsified | Conflict resolution may reduce to precedence order |
| P-F3 Boundary with governance | Not falsified | **Most fragile:** AetherGovern may already cover evaluation and enforcement |
| P-F4 Decentralizability | Not falsified | Anchor, revocation window, conflict resolution without precedence |
| P-F5 Observable benefit | **Untested** | Requires an experiment |

**Overall:** not falsified on P-F1 to P-F4 by argument, each with a reservation, P-F3 weakest; P-F5 untested.

This does **not** justify a standalone project. It justifies **Phase 4** (independence decision), where the argument is tested, not merely stated.

---

## 4. What would change the assessment

- **If AetherGovern's authority chains already evaluate and enforce**, P-F3 is falsified; AetherPolicy is a feature of AetherGovern.
- **If AetherRuntime's halt orders already cover revocation**, P-F1 is falsified for revocation; AetherPolicy is a feature of AetherRuntime for that function.
- **If conflict resolution always requires a central arbiter**, P-F4 is falsified for conflict resolution.
- **If no scenario distinguishes AetherPolicy from AetherGovern + AetherRuntime**, P-F5 is falsified.

These are the four outcomes that would stop the project.

---

## 5. What this document does not claim

- That AetherPolicy is independent.
- That the five functions are complete.
- That the boundaries are sufficient.
- That the gap is genuine.
- That implementation should begin.

This document claims only that the conditions are stated so that they can fail.

---

## 6. Next step

**Phase 4 — Independence Decision** (`DECISION.md`). The decision tests the argument in §3. It does not re-state it.
