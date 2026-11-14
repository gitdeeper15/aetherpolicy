# AetherPolicy — Responsibility Boundaries

**Phase:** 1 (Responsibility Mapping)
**Version:** 0.1.0
**Date:** 2026-11-14
**Status:** Analysis. Not a result.

---

## 0. Purpose

This document maps the **actual** responsibilities of the eight existing Aether projects, not their assumed responsibilities. It then asks: which of AetherPolicy's five functions are already covered, and which are not?

The matrix is the input to Phase 2 (Falsification Design). It is not a result.

---

## 1. Method

For each of the eight existing projects, the document records:

- Its **stated** responsibility (from its published description).
- Its **actual** surface (what it specifies, what it does not).
- Its **relation** to the five functions (Definition, Evaluation, Enforcement, Revocation, Conflict Resolution).

The distinction between stated and actual is the point. A project may *state* that it handles authority, but its *actual* surface may stop at issuance.

---

## 2. Responsibility matrix

### 2.1 AetherGit

| Field | Value |
|---|---|
| Stated responsibility | Storage and versioning of agent-generated changes |
| Actual surface | Signed, content-addressed changesets; version history; author keys |
| Relation to Definition | Stores policy records as changesets (not their semantics) |
| Relation to Evaluation | None |
| Relation to Enforcement | None |
| Relation to Revocation | None (storage is append-only) |
| Relation to Conflict Resolution | None |

### 2.2 AetherFlow

| Field | Value |
|---|---|
| Stated responsibility | Integration and post-merge verification |
| Actual surface | Merge verification; conflict resolution of *code*, not of *policy* |
| Relation to Definition | None |
| Relation to Evaluation | Verifies outcomes, not policies |
| Relation to Enforcement | None |
| Relation to Revocation | None |
| Relation to Conflict Resolution | Resolves *code* conflicts, not *policy* conflicts |

### 2.3 AetherProof

| Field | Value |
|---|---|
| Stated responsibility | Specification and evidence |
| Actual surface | Formal verification of claims; evidence artifacts |
| Relation to Definition | Can verify that a policy is well-formed |
| Relation to Evaluation | Can verify that a decision follows from a rule and a fact |
| Relation to Enforcement | None (verification is not enforcement) |
| Relation to Revocation | None |
| Relation to Conflict Resolution | Can verify a precedence order, if one is given |

### 2.4 AetherMesh

| Field | Value |
|---|---|
| Stated responsibility | Distribution and eventual consistency |
| Actual surface | CRDTs; convergent propagation; no global order |
| Relation to Definition | Distributes policy records |
| Relation to Evaluation | None |
| Relation to Enforcement | None |
| Relation to Revocation | Distributes revocation records |
| Relation to Conflict Resolution | None (it does not arbitrate) |

### 2.5 AetherGovern

| Field | Value |
|---|---|
| Stated responsibility | Authority and policy |
| Actual surface | Authority chains; policy issuance; revocation of authority |
| Relation to Definition | Issues policy (authority to define) |
| Relation to Evaluation | **Unclear.** Does it evaluate policy applicability? |
| Relation to Enforcement | **Unclear.** Does it enforce, or only authorize? |
| Relation to Revocation | Revokes authority, not policy |
| Relation to Conflict Resolution | **Unclear.** Does it arbitrate between policies? |

**The three "unclear" rows are the contested region.** They are the reason P-F3 is the most fragile condition.

### 2.6 AetherRuntime

| Field | Value |
|---|---|
| Stated responsibility | Monitoring and runtime assurance |
| Actual surface | Observes agents; issues halt orders; detects anomalies |
| Relation to Definition | None |
| Relation to Evaluation | None (it observes, it does not evaluate policy) |
| Relation to Enforcement | Issues halt orders (a form of enforcement, but not policy-specific) |
| Relation to Revocation | Can halt an agent (not the same as revoking a policy) |
| Relation to Conflict Resolution | None |

### 2.7 AetherOrchestrate

| Field | Value |
|---|---|
| Stated responsibility | Orchestration |
| Actual surface | Assigns tasks; schedules; routes |
| Relation to Definition | None |
| Relation to Evaluation | May consume policy decisions as eligibility input |
| Relation to Enforcement | None |
| Relation to Revocation | None |
| Relation to Conflict Resolution | None |

### 2.8 AetherIdentity

| Field | Value |
|---|---|
| Stated responsibility | Identity and continuity |
| Actual surface | Self-certifying identifiers; continuity chains; reputation; Sybil resistance; delegation |
| Relation to Definition | None (it does not define policy) |
| Relation to Evaluation | May provide the identity against which a policy is evaluated |
| Relation to Enforcement | None |
| Relation to Revocation | Revokes identities, not policies |
| Relation to Conflict Resolution | None |

---

## 3. Coverage analysis

| Function | Covered by | Not covered by |
|---|---|---|
| **Definition** | AetherGovern (authority to issue), AetherGit (storage) | A language for policy that can be evaluated |
| **Evaluation** | AetherProof (verification of a decision) | A model for context-sensitive applicability |
| **Enforcement** | AetherRuntime (halt orders) | Policy-specific enforcement |
| **Revocation** | AetherGovern (revocation of authority), AetherRuntime (halt) | Revocation of a policy (not an identity, not an authority) |
| **Conflict Resolution** | AetherProof (verification of a precedence order) | Arbitration between policies from different issuers |

**The uncovered column is the candidate's proposed scope.** It is not a result; it is a hypothesis about where the gap lies.

---

## 4. The contested region

Three questions remain open:

1. **Does AetherGovern evaluate?** If yes, Evaluation is not a gap.
2. **Does AetherGovern enforce?** If yes, Enforcement is not a gap.
3. **Does AetherGovern resolve conflicts?** If yes, Conflict Resolution is not a gap.

The answers determine whether AetherPolicy is independent, a feature of AetherGovern, or a bounded extension.

---

## 5. What this document does not claim

- That the gap is genuine.
- That the uncovered column is AetherPolicy's responsibility.
- That AetherGovern does not evaluate, enforce, or resolve.
- That the matrix is complete.

It claims only that the matrix is the input to Phase 2.

---

## 6. Next step

**Phase 2 — Falsification Design** (`FALSIFICATION/FALSIFICATION_PLAN.md`). The plan tests the three open questions in §4.
