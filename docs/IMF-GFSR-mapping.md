# IMF GFSR Mapping — SM26 Policy Papers

## Overview

This document maps each SM26 figure to its IMF source context and explains how the SM26 evidence base can be read alongside IMF surveillance frameworks.

**Repository:** `avant-dev-hq/sm26-spring-meetings-2026`  
**Source files:** `data/fig1-hyperscaler-capex-vs-lac-growth.csv` through `data/fig6-colombia-reform-impact.csv`

---

## Figure-to-Source Mapping

| Figure | Data file | IMF document | Chapter / section | Methodology note |
|---|---|---|---|---|
| Figure 1 — Hyperscaler Capex vs. LAC GDP Growth | `data/fig1-hyperscaler-capex-vs-lac-growth.csv` | IMF World Economic Outlook (Apr 2026) | Regional outlook for Latin America and the Caribbean | Uses WEO regional growth estimates as the macro backdrop for comparing hyperscaler capex concentration against LAC growth performance. |
| Figure 2 — Governance vs. Capital Stability | `data/fig2-governance-vs-capital-stability.csv` | IMF Global Financial Stability Report (Apr 2026) | Institutional quality and financial stability discussion | Treats governance quality as a macro-financial explanatory variable and links rule-of-law variation to capital flight premiums. |
| Figure 3 — Mexico GDP Growth Scenarios | `data/fig3-mexico-growth-scenarios.csv` | IMF World Economic Outlook (Apr 2026) | Mexico country outlook / scenario discussion | Presents a baseline and a governance-reform scenario consistent with IMF-style conditional macroeconomic analysis. |
| Figure 4 — NBFI Yield Premium by Institutional Quality | `data/fig4-nbfi-yield-premium.csv` | IMF Global Financial Stability Report (Apr 2026) | Nonbank financial institutions / yield spread analysis | Maps institutional quality to NBFI yield premiums and is the strongest candidate for FSI-oriented discussion. |
| Figure 5 — Sovereign-Bank Nexus Amplification | `data/fig5-sovereign-bank-nexus.csv` | IMF Global Financial Stability Report (Apr 2026) | Cross-sector contagion / sovereign-bank nexus | Shows how a sovereign spread shock transmits through the NBFI channel into larger systemic amplification. |
| Figure 6 — Colombia Sovereign Spread Impact | `data/fig6-colombia-reform-impact.csv` | Central bank / IMF Article IV-style surveillance context | Sovereign spread and institutional reform signaling | Serves as a time-series policy case showing spread compression associated with governance reform signals. |

---

## FSI Framework Alignment

The SM26 repo should be read primarily through the following IMF Financial Soundness Indicator lens:

1. **NBFI stability indicators**
   - Primary evidence: Figure 4 and Figure 5
   - Why it matters: these figures quantify the nonbank channel and the associated yield premium under different institutional environments

2. **Sovereign risk transmission**
   - Primary evidence: Figure 5 and Figure 6
   - Why it matters: the repo shows how sovereign stress can amplify through related financial channels

3. **Governance as a macro-financial variable**
   - Primary evidence: Figure 2
   - Why it matters: institutional quality is used as an explanatory input rather than as background context only

---

## Article IV / Surveillance Use Cases

The figures can be used as policy counterfactuals or supporting evidence in IMF-style surveillance work:

- **Figure 2**: supports a governance-to-stability hypothesis for cross-country surveillance
- **Figure 3**: supports conditional growth scenarios for Mexico-style policy discussion
- **Figure 6**: supports a sovereign spread case study for Colombia-like reform signaling

---

## Notes on Evidence Handling

- The CSV files in `data/` are the source of truth.
- This mapping document does not restate or normalize the raw data.
- The purpose is traceability: figure → source → IMF-relevant framing.

---

## Repository Context

This repository is a policy research artifact rather than a code project. Its value comes from:
- reproducible tabular evidence in `data/`
- citation support in `CITATION.md`
- the long-form policy framing in `README.md`

---

*Document prepared for SM26 Geneva / multilateral briefing use.*