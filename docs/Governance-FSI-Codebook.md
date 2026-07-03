# Governance FSI Codebook — SM26 Policy Papers

## Purpose

This codebook documents the six CSV files in `data/` and provides an IMF-oriented reference for variable definitions, units, frequency, and source lineage. It supports reproducibility review, FSI framework engagement, and formal research submission.

**Repository:** `avant-dev-hq/sm26-spring-meetings-2026`

---

## General Rules

- The CSV files in `data/` are source-of-truth. This codebook does not restate or normalize the raw data.
- No new data is introduced in this document.
- Where a direct IMF Financial Soundness Indicator mapping is not possible, the document notes the limitation rather than inventing one.
- Every variable described here traces to a source cited in the README.

---

## File 1 — `data/fig1-hyperscaler-capex-vs-lac-growth.csv`

**Figure:** Hyperscaler Capex vs. LAC GDP Growth (2023–2025)

| Field | Value |
|---|---|
| Source | IMF WEO Apr 2026 · Synergy Research · Avant.Dev estimates |
| Frequency | Annual |
| Seasonal adjustment | Not applicable |
| Coverage | 2023–2025 |

### Variables

| Variable | Description | Unit |
|---|---|---|
| `year` | Calendar year | Year |
| `hyperscaler_capex_usd_trillions` | Aggregate hyperscaler capital expenditure (top providers) | USD trillions |
| `lac_gdp_growth_pct` | Latin America and Caribbean GDP growth | Percent |

### Data lineage
- Hyperscaler capex is a synthesis of market data referenced in the README (Synergy Research).
- LAC GDP growth uses the IMF WEO April 2026 regional estimate.

### FSI/IMF relevance
- Macro backdrop only. Not an FSI indicator file.
- Contextualizes the structural dependency argument in Paper I.

---

## File 2 — `data/fig2-governance-vs-capital-stability.csv`

**Figure:** Governance vs. Capital Stability — r = 0.67 correlation (rule-of-law ↔ NBFI stability)

| Field | Value |
|---|---|
| Source | IVA macrofinancial database (2022–2025) |
| Frequency | Cross-sectional panel summary |
| Seasonal adjustment | Not applicable |
| Coverage | 2022–2025 |

### Variables

| Variable | Description | Unit |
|---|---|---|
| `rule_of_law_index` | Rule-of-law governance score | Index (0–1 scale) |
| `capital_flight_premium_bp` | Capital flight premium associated with governance level | Basis points |

### Data lineage
- Rule-of-law input aligned to World Bank Governance Indicators as cited in the repository.
- Capital flight premium from the IVA macrofinancial database (2022–2025).
- Correlation r = 0.67 computed across the index-premium series in this file.

### FSI/IMF relevance
- **Priority 3:** Governance as a macro-financial variable.
- Useful as an explanatory input for NBFI stability and capital flow analysis.
- Should not be presented as a bank-level FSI balance-sheet ratio.
- 1pp improvement in rule-of-law index yields −60bp in capital flight premium.

---

## File 3 — `data/fig3-mexico-growth-scenarios.csv`

**Figure:** Mexico GDP Growth Scenarios — Baseline vs. Governance Reform

| Field | Value |
|---|---|
| Source | IMF WEO Apr 2026 · Avant.Dev conditional scenario |
| Frequency | Scenario comparison (annual) |
| Seasonal adjustment | Not applicable |
| Coverage | 2026–2027 scenario window |

### Variables

| Variable | Description | Unit |
|---|---|---|
| `scenario` | Scenario label | Text |
| `gdp_growth_pct` | GDP growth rate | Percent |

### Data lineage
- Baseline (1.6%) is the IMF WEO April 2026 projection for Mexico.
- Reform scenario (2.2%) is the repository's governance-conditional policy case, consistent with IMF Article IV conditional analysis methodology.

### FSI/IMF relevance
- Article IV / surveillance counterfactual use.
- Not an FSI indicator file.
- Supports the Mexico governance reform recommendation in Paper II.

---

## File 4 — `data/fig4-nbfi-yield-premium.csv`

**Figure:** NBFI Yield Premium by Institutional Quality

| Field | Value |
|---|---|
| Source | IMF GFSR Ch.2 (Apr 2026) · World Bank Governance Indicators |
| Frequency | Ordinal institutional quality comparison |
| Seasonal adjustment | Not applicable |
| Coverage | Institutional quality categories: Weak → Very Strong |

### Variables

| Variable | Description | Unit |
|---|---|---|
| `institutional_quality` | Qualitative governance category | Text |
| `nbfi_premium_bp` | NBFI yield premium associated with quality level | Basis points |

### Data lineage
- Governance categories mapped to the World Bank Governance Indicators framework referenced in the repository.
- NBFI premium relationship cited from IMF GFSR Chapter 2, April 2026.

### FSI/IMF relevance
- **Priority 1:** Primary NBFI stability indicator candidate.
- Best fit for IMF Statistics Department engagement on nonbank risk transmission.
- Directly relevant to the $4T nonbank portfolio inflows to emerging markets context (IMF GFSR Ch.2).
- Strongest candidate for FSI framework enhancement discussion.

---

## File 5 — `data/fig5-sovereign-bank-nexus.csv`

**Figure:** Sovereign-Bank Nexus Amplification — 100bp → 160bp

| Field | Value |
|---|---|
| Source | IMF GFSR Ch.2 (Apr 2026) |
| Frequency | Stylized shock decomposition |
| Seasonal adjustment | Not applicable |
| Coverage | Single illustrative shock example |

### Variables

| Variable | Description | Unit |
|---|---|---|
| `component` | Contagion component label | Text |
| `basis_points` | Magnitude of component | Basis points |

### Data lineage
- Shock transmission structure derived from the sovereign-bank nexus discussion in IMF GFSR Chapter 2, April 2026.
- Illustrative decomposition: 100bp sovereign spread → 60bp NBFI premium → 160bp total amplification.

### FSI/IMF relevance
- **Priority 1 + Priority 2:** NBFI channel + sovereign risk transmission.
- Relevant for cross-sector contagion modeling in macro-financial surveillance.
- Not a bank balance-sheet FSI; functions as a transmission mechanism illustration.

---

## File 6 — `data/fig6-colombia-reform-impact.csv`

**Figure:** Colombia Sovereign Spread — Institutional Reform Impact (Apr 2024 – Apr 2026)

| Field | Value |
|---|---|
| Source | Banco de la República de Colombia · Avant.Dev estimates |
| Frequency | Quarterly / event-linked time series |
| Seasonal adjustment | Not applicable |
| Coverage | Apr 2024 – Apr 2026 |

### Variables

| Variable | Description | Unit |
|---|---|---|
| `date` | Observation date | Date (YYYY-MM) |
| `colombia_sovereign_spread_bp` | Colombia sovereign spread level | Basis points |

### Data lineage
- Time series constructed from Central Bank of Colombia communications and market data.
- Net change: −110bp from Apr 2024 (320bp) to Apr 2026 (210bp).
- Movement associated with institutional reform signals as described in Paper II.

### FSI/IMF relevance
- **Priority 2:** Sovereign risk transmission case study.
- Best used as a reform-credibility and spread-compression narrative.
- Supports Article IV surveillance discussion for Colombia.
- Should not be labeled as an FSI ratio or bank balance-sheet measure.

---

## Priority Summary

| Priority | Coverage | Files |
|---|---|---|
| 1 — NBFI stability indicators | Nonbank yield premium + contagion channel | Figures 4, 5 |
| 2 — Sovereign risk transmission | Spread amplification + Colombia case | Figures 5, 6 |
| 3 — Governance as macro-financial variable | Rule-of-law to NBFI stability | Figure 2 |
| Background — Macro context | Capex vs. growth · Mexico scenarios | Figures 1, 3 |

---

*Avant.Dev Policy Intelligence · erick@avant.dev · [avant.dev](https://avant.dev)*  
*UN ITU P2C #7528 · IMF ROC Phase II · GDAIG Geneva Jul 2026*
