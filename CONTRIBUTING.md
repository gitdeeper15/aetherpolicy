# Contributing to AetherPolicy

**Status:** v0.1.0 is an architectural hypothesis. No implementation,
specification, test, or experiment is reported. The architectural
independence of AetherPolicy has not been decided.

The project is paused at Phase 4 (Independence Decision), and the decision
is (E) undetermined. Contributions at this stage are limited to review and
critique.

---

## What is welcome

**For the hypothesis:**
- Review of `ARCHITECTURAL_HYPOTHESIS.md`. The hypothesis is stated so that
  it can fail. Independent review is the most useful next step.
- Review of `research/RESPONSIBILITY_BOUNDARIES.md`. The three open questions
  are: does AetherGovern evaluate, enforce, or resolve conflicts?
- Review of `FALSIFICATION/FALSIFICATION_PLAN.md`. Are the five conditions
  (P-F1 to P-F5) stated so that they can fail?
- Review of `DECISIONS/INDEPENDENCE_DECISION.md`. Is (E) undetermined the
  right interim classification?

**Literature pointers:**
- Policy languages: XACML, Rego/OPA, Cedar.
- Access control: RBAC, ABAC, ReBAC, Zanzibar.
- Policy lifecycle: Sloman, Lupu and Sloman, Rei.
- Decentralized authorization: trust management, Macaroons, Biscuit.
- Enforcement: Schneider (2000), Ligatti et al. (2009).
- Distributed consistency: CALM (Hellerstein and Alvaro, 2020).

**For the independent review (Phase 2):**
- Suggestions for `REVIEW/INDEPENDENT_REVIEW.md`.
- Identification of gaps in the current argument.
- Counter-examples to P-F1, P-F2, P-F3, or P-F4.

## What is not applicable at this stage

- Code contributions (there is no code, and none will be written before
  Phase 5, which is not permitted).
- Test contributions (there are no tests).
- Feature requests (there is no implementation).
- Benchmark results (none have been produced).
- Claims that AetherPolicy is an independent dimension (the evidence is
  insufficient).

## How to contribute

Open an issue and describe:

1. The section of the relevant document affected.
2. What you believe is incorrect or missing.
3. A reference or argument supporting your view.

## What to expect

The hypothesis is not peer reviewed. The author will review issues in good
faith, but no timeline is promised. Independent review is the most useful
next step.

## Code of conduct

Be specific, be charitable, and cite evidence. Disagreement about the
hypothesis is welcome; disagreement about the author is not.
