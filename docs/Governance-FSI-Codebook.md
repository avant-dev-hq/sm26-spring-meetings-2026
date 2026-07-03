# Governance FSI Codebook — SM26 Policy Papers

## Purpose

This codebook documents the six CSV files in `data/` and provides a clean IMF-oriented reference for variable definitions, units, frequency, and source lineage.

**Repository:** `avant-dev-hq/sm26-spring-meetings-2026`

---

## General Rules

- The CSV files are source-of-truth and should not be reformatted here.
- No new data is introduced in this document.
- Where a direct IMF Financial Soundness Indicator mapping is not possible, the document notes the limitation rather than inventing one.

---

## File 1 — `data/fig1-hyperscaler-capex-vs-lac-growth.csv`

### Metadata
- **Figure:** Hyperscaler Capex vs. LAC GDP Growth
- **Source note in file:** IMF WEO Apr 2026 · Synergy Research · Avant.Dev estimates
- **Frequency:** Annual
- **Seasonal adjustment:** Not applicable
- **Coverage:** 2023–2025

### Variables
| Variable | Description | Unit |
|---|---|---|
| `year` | Calendar year | Year |
| `hyperscaler_capex_usd_trillions` | Hyperscaler capital expenditure | USD trillions |
| `lac_gdp_growth_pct` | Latin America and Caribbean GDP growth | Percent |

### Data lineage
- Hyperscaler capex is presented as a synthesis of market data referenced in the README.
- LAC GDP growth uses the IMF WEO April 2026 framing cited in the repository.

### IMF/FSI relevance
- Indirect macro backdrop only.
- Not an FSI indicator file.

---

## File 2 — `data/fig2-governance-vs-capital-stability.csv`

### Metadata
- **Figure:** Governance vs. Capital Stability
- **Source note in file:** IVA macrofinancial database (2022–2025)
- **Frequency:** Cross-sectional / panel summary
- **Seasonal adjustment:** Not applicable
- **Coverage:** 2022–2025

### Variables
| Variable | Description | Unit |
|---|---|---|
| `rule_of_law_index` | Rule-of-law score | Index (0–1) |
| `capital_flight_premium_bp` | Capital flight premium | Basis points |

### Data lineage
- Rule-of-law input is aligned to governance indicators referenced in the repository.
- Capital flight premium comes from the IVA macrofinancial database cited in the README.

### IMF/FSI relevance
- Cross-cutting governance variable.
- Useful as a macro-financial explanatory input.
- Supports NBFI stability discussion, but should not be presented as a bank-level FSI.

---

## File 3 — `data/fig3-mexico-growth-scenarios.csv`

### Metadata
- **Figure:** Mexico GDP Growth Scenarios
- **Source note in file:** IMF WEO Apr 2026
- **Frequency:** Scenario comparison
- **Seasonal adjustment:** Not applicable
- **Coverage:** 2026–2027 scenario window

### Variables
| Variable | Description | Unit |
|---|---|---|
| `scenario` | Scenario label | Text |
| `year` | Projection year | Year |
| `gdp_growth_pct` | GDP growth rate | Percent |
| `notes` | Scenario annotation | Text |

### Data lineage
- Baseline value is the IMF WEO April 2026 projection cited in the CSV.
- Reform scenario is the repository’s conditional policy case.

### IMF/FSI relevance
- Article IV / surveillance counterfactual use only.
- Not an FSI indicator file.

---

## File 4 — `data/fig4-nbfi-yield-premium.csv`

### Metadata
- **Figure:** NBFI Yield Premium by Institutional Quality
- **Source note in file:** IMF GFSR Ch.2 (Apr 2026) · World Bank Governance Indicators
- **Frequency:** Ordinal comparison
- **Seasonal adjustment:** Not applicable
- **Coverage:** Institutional quality categories from Weak to Very Strong

### Variables
| Variable | Description | Unit |
|---|---|---|
| `institutional_quality` | Qualitative governance category | Text |
| `institutional_quality_score` | Ordinal score for institutional quality | Score (1–5) |
| `nbfi_premium_bp` | NBFI yield premium | Basis points |

### Data lineage
- Uses governance categories mapped to the repository’s institutional-quality framework.
- NBFI premium is cited as an IMF GFSR Ch.2-derived relationship in the repository.

### IMF/FSI relevance
- Primary candidate for NBFI stability discussion.
- Best fit for IMF Statistics Department engagement on nonbank risk transmission.
- Strongest candidate for a future FSI-oriented enhancement note.

---

## File 5 — `data/fig5-sovereign-bank-nexus.csv`

### Metadata
- **Figure:** Sovereign-Bank Nexus Amplification
- **Source note in file:** IMF GFSR Ch.2 (Apr 2026)
- **Frequency:** Contagion illustration / shock decomposition
- **Seasonal adjustment:** Not applicable
- **Coverage:** Single shock example

### Variables
| Variable | Description | Unit |
|---|---|---|
| `component` | Contagion component | Text |
| `basis_points` | Magnitude of component | Basis points |
| `notes` | Annotation | Text |

### Data lineage
- Represents a stylized shock transmission structure drawn from the repository’s IMF GFSR framing.

### IMF/FSI relevance
- Relevant for sovereign risk transmission and contagion discussion.
- Useful in macro-financial surveillance, but not a direct bank balance-sheet indicator.

---

## File 6 — `data/fig6-colombia-reform-impact.csv`

### Metadata
- **Figure:** Colombia Sovereign Spread — Institutional Reform Impact
- **Source note in file:** Banco de la Republica de Colombia · Avant.Dev estimates
- **Frequency:** Quarterly / event-linked time series
- **Seasonal adjustment:** Not applicable
- **Coverage:** Apr 2024 to Apr 2026

### Variables
| Variable | Description | Unit |
|---|---|---|
| `date` | Observation date | Date |
| `colombia_sovereign_spread_bp` | Sovereign spread level | Basis points |
| `notes` | Event annotation | Text |

### Data lineage
- Time series is tied to central bank communications and reform signaling described in the repository.
- The repository uses the series as evidence of spread compression over time.

### IMF/FSI relevance
- Best used as a sovereign risk transmission case study.
- Supports surveillance and reform narrative.
- Should not be labeled as an FSI ratio or balance-sheet measure.

---

## Priority Mapping Order

1. **Priority 1 — NBFI stability indicators**
   - Figures 4 and 5
2. **Priority 2 — Sovereign risk transmission**
   - Figures 5 and 6
3. **Priority 3 — Governance as a macro-financial variable**
   - Figure 2

---

## Summary

This codebook preserves the repository’s source citations and gives IMF readers a disciplined way to understand the dataset without inventing unsupported technical mappings.

*Document prepared for SM26 Geneva / multilateral briefing use.*