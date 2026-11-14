# AetherPolicy — Roadmap

**Version:** 0.1.0
**Status:** Paused at Phase 4 (Independence Decision).
**Decision:** (E) undetermined.
**No implementation.**

---

## Phase Status

| Phase | Status |
|---|---|
| 0 — Architectural Hypothesis | ✅ Complete (`ARCHITECTURAL_HYPOTHESIS.md`) |
| 1 — Responsibility Mapping | ✅ Complete (`research/RESPONSIBILITY_BOUNDARIES.md`) |
| 2 — Hypothesis Review | ⏳ Not started (`REVIEW/INDEPENDENT_REVIEW.md`) |
| 3 — Falsification Design | ✅ Complete (`FALSIFICATION/FALSIFICATION_PLAN.md`) |
| 4 — Independence Decision | ⚠️ Interim: (E) undetermined (`DECISIONS/INDEPENDENCE_DECISION.md`) |
| 5 — Architectural Specification | ❌ Not permitted |
| 6 — Reference Implementation | ❌ Not permitted |

---

## Phase 0 — Architectural Hypothesis ✅ Complete

**Output:** `ARCHITECTURAL_HYPOTHESIS.md`.

The hypothesis is stated. It is falsifiable. It is not a result.

---

## Phase 1 — Responsibility Mapping ✅ Complete

**Output:** `research/RESPONSIBILITY_BOUNDARIES.md`.

The matrix maps the actual surface of the eight existing projects against the five functions. Three questions remain open.

---

## Phase 2 — Hypothesis Review ⚠️ Internal only

**Output:** `REVIEW/INTERNAL_REVIEW.md` (internal, not independent).

**Status:** Internal review complete. Independent review not started. Required before Phase 4 is final.

**Note:** The paper's Figure 6 shows Phase 2 as not started although Phase 3 is complete. The consequence is threat T1: no independent review has taken place, and the failure conditions were stated and attempted by the author alone.

---

## Phase 3 — Falsification Design ✅ Complete

**Output:** `FALSIFICATION/FALSIFICATION_PLAN.md`.

The plan specifies how to test the three open questions. It does not run the tests.

---

## Phase 4 — Independence Decision ⚠️ Interim (E) undetermined

**Output:** `DECISIONS/INDEPENDENCE_DECISION.md`.

**Status:** Interim. The decision is (E) undetermined. It is not final, because Phase 2 (Independent Review) has not been completed.

**Companion report:** `REPORTS/architectural_investigation/investigation_report.md`.

---

## Phase 5 — Architectural Specification ❌ Not permitted

**Output:** `SPECIFICATION.md`.

**Status:** Not permitted. Requires a positive Phase 4 decision.

---

## Phase 6 — Reference Implementation ❌ Not permitted

**Output:** `src/aetherpolicy/`, `tests/`, `experiments/`.

**Status:** Not permitted. Requires Phase 5.

---

## What would change the status

To move from Phase 4 (interim) to Phase 4 (final), one of the following is needed:

1. **Phase 2 completion** — an independent review of the hypothesis and the plan.
2. **A stronger argument** addressing P-F3 (the most fragile condition).
3. **An experiment** (requires Phase 5 and 6, which are not permitted).

Without one of these, the project remains at Phase 4 (interim).

---

## What is not on this roadmap

- Any implementation before Phase 4 is positive.
- Any claim that AetherPolicy is an independent dimension.
- Any renumbering of AetherIdentity.
