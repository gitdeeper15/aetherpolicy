# AetherPolicy — Complete Inventory

**Version:** 0.1.0 (Architectural Investigation)
**Release Date:** 2026-11-11
**Author:** Samir Baladi
**Email:** gitdeeper@gmail.com
**ORCID:** [0009-0003-8903-0029](https://orcid.org/0009-0003-8903-0029)
**License:** CC-BY-4.0 (docs, manuscript, figures) · MIT (code, future — none in this release)
**Status:** Architectural Investigation · Candidate (Phase 4: undetermined)
**Record ID:** AETHERPOLICY-01
**DOI (Zenodo):** 10.5281/zenodo.24160047
**DOI (Figshare):** 10.6084/m9.figshare.35009833
**Website:** [aetherpolic-y.netlify.app](https://aetherpolic-y.netlify.app)

---

## Research Status

| Item | Status |
|---|---|
| Document type | Research article (architectural hypothesis + decision) |
| Paper (v0.1.0) | ✅ Published (Zenodo + Figshare) |
| Implementation | ❌ Not built (not permitted at Phase 4) |
| Tests | ❌ None |
| Experiments | ❌ None executed (Section 9 of the paper is a proposal) |
| PyPI package | ❌ Not published |
| Real-world deployment | None; no deployed system has been benchmarked |
| Propositions P1–P2 | Stated with proof sketches; not machine-checked |
| Failure conditions | P-F1–P-F4 not falsified by argument; P-F5 untested; P-F3 most fragile |
| Independent review | ❌ Not started (Phase 2 not started) |
| Review status | Not peer reviewed |
| Decision | **(E) Undetermined (interim)** |

---

## Repository Links

| Platform | URL | Role | Status |
|----------|-----|------|--------|
| GitHub | https://github.com/gitdeeper15/aetherpolicy | Primary | ✅ Active |
| GitLab | https://gitlab.com/gitdeeper15/aetherpolicy | Mirror | ✅ Active |
| Codeberg | https://codeberg.org/gitdeeper15/aetherpolicy | Mirror | ✅ Active |
| Bitbucket | https://bitbucket.org/gitdeeper15/aetherpolicy | Mirror | ✅ Active |
| Website | https://aetherpolic-y.netlify.app | Live documentation | ✅ Active |
| Zenodo | https://doi.org/10.5281/zenodo.24160047 | Citable DOI | ✅ Published |
| Figshare | https://doi.org/10.6084/m9.figshare.35009833 | Preprint archive | ✅ Published |
| ORCID | https://orcid.org/0009-0003-8903-0029 | Identity | ✅ Active |

---

## Root Files

| File | Purpose | Status |
|------|---------|:-:|
| `.gitignore` | Git ignore rules | ✅ |
| `AUTHORS.md` | Contributors | ✅ |
| `CHANGELOG.md` | Version history | ✅ |
| `CITATION.cff` | Citation metadata | ✅ |
| `CONTRIBUTING.md` | Contribution guidelines | ✅ |
| `INVENTORY.md` | This file | ✅ |
| `LICENSE` | CC-BY-4.0 (docs) + MIT (code, future) | ✅ |
| `PROJECT_SUMMARY.txt` | One-page summary | ✅ |
| `README.md` | Main documentation | ✅ |
| `ARCHITECTURAL_HYPOTHESIS.md` | The hypothesis under investigation | ✅ |
| `ROADMAP.md` | Phase status (0 → 6) | ✅ |
| `VERSION` | `0.1.0` | ✅ |
| `manifest.json` | Project manifest | ✅ |
| `scientific_state.json` | Scientific state record | ✅ |
| `netlify.toml` | Netlify configuration | ✅ |

---

## Directories

| Directory | Contents | Status |
|-----------|----------|:-:|
| `docs/figures/` | 9 figures (Fig1–Fig9) | ✅ Complete |
| `research/` | `RESPONSIBILITY_BOUNDARIES.md` | ✅ Complete |
| `FALSIFICATION/` | `FALSIFICATION_PLAN.md` | ✅ Complete |
| `DECISIONS/` | `INDEPENDENCE_DECISION.md` | ✅ Complete (interim) |
| `REVIEW/` | `INTERNAL_REVIEW.md` (internal, not independent) | ✅ Complete (internal) |
| `REVIEW/` | `INDEPENDENT_REVIEW.md` | ⏳ Not started |
| `REFERENCES/` | To be populated with the 29 references from the paper | 🔄 In progress |
| `REPORTS/architectural_investigation/` | `investigation_report.md` | ✅ Complete |
| `paper/` | `AetherPolicy_Research_Paper.pdf` | ✅ Published |
| `PUBLICATION/Netlify/public/` | Website (4 HTML pages + robots/sitemap) | ✅ Live |

No `src/`, no `tests/`, no `experiments/` — and none is planned unless Phase 4 becomes positive.

---

## Formal Artifacts

| Category | Count |
|---|---|
| Functions (Fn1–Fn5) | 5 |
| Failure Conditions (P-F1 to P-F5) | 5 |
| Propositions (P1–P2, proof sketches) | 2 |
| Boundaries (AetherGovern, AetherIdentity, AetherRuntime, AetherPolicy) | 4 |
| Open Questions (Q1–Q10) | 10 |
| Figures | 9 |
| References | 29 |
| Related Aether projects | 9 (including AetherPolicy) |
| Phases | 7 (0–6) |
| Tests run | 0 |
| Experiments executed | 0 |

---

## Failure Conditions (P-F1 to P-F5)

| ID | Claim under test | Status |
|:-:|---|:-:|
| P-F1 | Non-redundancy | 🟡 Not falsified (author's reading of own records) |
| P-F2 | Orthogonality to verification and governance | 🟡 Not falsified (remainder may be small) |
| P-F3 | Boundary with governance | 🟡 Not falsified (**most fragile**) |
| P-F4 | Decentralizability | 🟡 Not falsified (residuals: revocation window, honest enforcer) |
| P-F5 | Observable benefit | 🔴 **Untested** |

> "Not falsified" is weaker than "confirmed". "Untested" is not a pass. The decision rule requires **all five** to be tested with none falsified.

---

## Phase Status

| Phase | Description | Status |
|---|---|---|
| 0 | Architectural Hypothesis | ✅ Complete |
| 1 | Responsibility Mapping | ✅ Complete |
| 2 | Hypothesis Review (Independent) | ⏳ Not started |
| 3 | Falsification Design | ✅ Complete |
| 4 | Independence Decision | ⚠️ Interim: (E) undetermined |
| 5 | Architectural Specification | ❌ Not permitted |
| 6 | Reference Implementation | ❌ Not permitted |

---

## Companion Works

AetherPolicy is the **ninth project (candidate)** of the Aether family. It does **not** replace AetherIdentity (the eighth project).

| # | System | Dimension | Status | DOI |
|:-:|---|---|---|---|
| 1 | AetherGit | Storage / Foundation | Foundational | [10.5281/zenodo.23976986](https://doi.org/10.5281/zenodo.23976986) |
| 2 | AetherFlow | Integration | Foundational | [10.5281/zenodo.23979129](https://doi.org/10.5281/zenodo.23979129) |
| 3 | AetherProof | Verification | Foundational | [10.5281/zenodo.24013124](https://doi.org/10.5281/zenodo.24013124) |
| 4 | AetherMesh | Decentralization | Foundational | [10.5281/zenodo.24038038](https://doi.org/10.5281/zenodo.24038038) |
| 5 | AetherGovern | Governance | Foundational | [10.5281/zenodo.24054524](https://doi.org/10.5281/zenodo.24054524) |
| 6 | AetherRuntime | Runtime Assurance | Foundational | [10.5281/zenodo.24078477](https://doi.org/10.5281/zenodo.24078477) |
| 7 | AetherOrchestrate | Orchestration | Foundational | [10.5281/zenodo.24095399](https://doi.org/10.5281/zenodo.24095399) |
| 8 | AetherIdentity | Identity | Candidate (paper + v2.0.0) | [10.5281/zenodo.24102739](https://doi.org/10.5281/zenodo.24102739) |
| 9 | **AetherPolicy** | **Policy Lifecycle (candidate)** | **Candidate (paused at Phase 4)** | [10.5281/zenodo.24160047](https://doi.org/10.5281/zenodo.24160047) |

**Preprint:** Figshare DOI `10.6084/m9.figshare.35009833`

---

## What This Repository Does Not Claim

- That AetherPolicy is an independent architectural dimension.
- That the five functions are complete, independent, or necessary.
- That the boundaries with AetherGovern, AetherIdentity, and AetherRuntime are sufficient.
- That the gap is genuine.
- That implementation should begin.
- Any observed benefit (P-F5 is untested).
- Any causal effect.

---

## Citation

### Paper (v0.1.0)

```bibtex
@techreport{baladi2026aetherpolicy,
  author       = {Baladi, Samir},
  title        = {AetherPolicy: Decentralized Policy Lifecycle and Enforcement
                  for Autonomous Agent Systems},
  institution  = {Ronin Institute / Rite of Renaissance},
  type         = {Research Paper},
  year         = {2026},
  month        = {November},
  version      = {0.1.0},
  doi          = {10.5281/zenodo.24160047},
  url          = {https://doi.org/10.5281/zenodo.24160047},
  note         = {Architectural investigation; Phase 4 (undetermined)}
}
```

---

Contact

· Email: gitdeeper@gmail.com
· ORCID: 0009-0003-8903-0029
· Website: aetherpolic-y.netlify.app
· GitHub: gitdeeper15/aetherpolicy

---

Last Updated: 2026-11-14
Current Version: 0.1.0
Decision: (E) Undetermined (interim)
