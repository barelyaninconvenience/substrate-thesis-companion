# Case Study 05 — Apex Analytics Methodology
## Substrate Thesis applied to a single-quarter team-collaborative data-mining project

**Status:** Tight seed 2026-04-24.

---

## Why this case demonstrates the framework outside personal-OS work

Cases 01-04 demonstrate the framework within Clay's personal-OS infrastructure. Case 05 demonstrates it in a **bounded external project** with team collaboration, client deliverables, and academic rubrics.

This tests whether Substrate Thesis patterns apply when Clay isn't the sole architect — when the project has external constraints, teammate methodology choices, and rubric requirements.

---

## The empirical project frame

| Element | Description |
|---|---|
| Course | IS7036 Data Mining for Business Intelligence (Spring 2026) |
| Team | Apex Analytics — Navedita / Archana / Harshita / Clay |
| Client | Lindner Career Services (LCS) |
| Dataset | 10,142 placement records × 3,122 unique employers (5 years) |
| Cycle | March 31 → April 24 (~25 days, end-to-end) |
| Output | Master notebook + 15-slide deck + Tableau dashboard + segmentation memo + Week 4 Lab |

---

## FKS instance — CRISP-DM as Module Sequencing

```
Module 1: Project Charter (business understanding)
   ↓
Module 2: Cleaned Master Dataset (data understanding + prep)
   ↓
Module 3: Predictive Modeling — Wage Predictor regression (Week 4 Lab)
   ↓
Module 4: Unsupervised Learning — K-Means segmentation
   ↓
Module 5: Final Capstone (synthesis + recommendations)
```

Each module's deliverable consumes the immediate-prior module's outputs. The Capstone reads Modules 1-4's deliverables, not the underlying raw data.

**Test of FKS payoff:** when the cleaning methodology updated (audit corrections in Module 2 → wage cap, location parsing), Modules 3-4 needed re-validation. Modules 1 + Capstone were unaffected because the cleaned-data interface remained stable. This is the bounded-blast-radius FKS guarantee in action.

---

## SCC instances — methodology decisions + tier output

| SCC | Versioning | Purpose |
|---|---|---|
| **10 methodology decisions** | Frozen at `apex-analytics-submission/docs/METHODOLOGY_JUSTIFICATION.md` | Citable rationale for K=4 / 4-feature / 3,122-employer / random_state=42 / wage-cap-$80/hr / etc. |
| **Tier output** (T1-T4 named) | v1 (Apr 20 team memo) → v2 corrected (Apr 21 audit) → final (Apr 23 deck v3) | Stable reference for AM allocation recommendation |
| **Cleaned dataset** | Single canonical file `data/processed/cleaned_master_dataset.csv` | All downstream notebooks consume this; no re-derivation from raw |

Each SCC enables version-aware citation. "Per the v1 team memo headline (371 employers, 11.9%, 51.5% placements)" vs "per the corrected v2 (424, 13.6%, 61%)" — both are correct citations depending on the question being asked.

---

## SRD instance — Reinvigoration template applied within the project

Within the 25-day project span, the reinvigoration template (case 01) applied multiple times:

| Artifact | v1 → v2 | Catalyst |
|---|---|---|
| Caddell_Descriptive_Insights_Memo | Apr 16 → Apr 24 | Audit (case 01) |
| Caddell_Individual_Segmentation_Memo | Apr 14 → Apr 24 | Audit + team-K=4 reconciliation |
| Apex Analytics Thursday deck | v1 → v2 → v3 (Apr 21) | Peer feedback integration |
| Apex Analytics tier counts | v1 (371/11.9%) → corrected (424/13.6%) | Wage-cap audit |

Same five-element template each time; different artifacts. SRD demonstrated within a single project frame.

---

## Researcher positionality + Substrate Thesis

The Apex Analytics team are co-op students analyzing the co-op system — simultaneously subjects, data producers, and analysts. This is exactly the kind of motivated-reasoning risk where Substrate Thesis discipline matters most:

- **FKS layering** prevented the cleaned-data Module 2 from being silently re-derived by Module 4 to support a preferred conclusion
- **SCC versioning** of methodology decisions made the rationale citable + auditable rather than retrofittable
- **SRD reinvigoration template** ensured the audit-corrected v2 numbers superseded the inflated v1 numbers — the framework forced the correction rather than allowing the inflated $87/hr Tier 3 to persist

The framework provides empirical guard-rails against the positionality risk, not just architectural elegance.

---

## What this case adds beyond cases 01-04

1. **External constraints:** the framework holds under team collaboration (4 teammates), academic rubric (200 pts), and client expectations (LCS Director audience)
2. **Bounded time scale:** 25 days end-to-end; framework operates at project-cycle scale, not just personal-OS lifetime scale
3. **Empirical validation through correction:** the audit catalyst forced the SCC update + the FKS layering bounded the blast radius + the reinvigoration template propagated the correction across artifacts
4. **Researcher-positionality test:** the framework provided empirical guard-rails when motivated reasoning could have allowed v1 inflated numbers to persist

---

## TODO for elaboration

- Document teammate-collaboration dynamics in framework terms (whose SCC is the team-final memo? whose FKS is the segmentation methodology?)
- Compare with peer projects (do teams without explicit Substrate Thesis discipline produce different correction-handling outcomes?)
- Quantify the audit catalyst's value — how much would the team have lost without the wage-cap correction?
- Cross-reference with the Apex Analytics submission package's `docs/NUMERIC_AUDIT.md` + `docs/CORRECTED_ANALYSIS.md` as primary sources

---

*Case Study 05 tight seed 2026-04-24. Anchored to `apex-analytics-submission/` (full repo) + `apex-analytics-submission/docs/METHODOLOGY_JUSTIFICATION.md` + `apex-analytics-submission/docs/NUMERIC_AUDIT.md` + `apex-analytics-submission/docs/CORRECTED_ANALYSIS.md`.*
