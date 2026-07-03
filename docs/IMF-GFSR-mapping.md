# IMF GFSR Mapping — SM26 Policy Papers

## Overview

This document maps each SM26 figure to its IMF source context and explains how the SM26 evidence base aligns with IMF surveillance frameworks.

**Repository:** `avant-dev-hq/sm26-spring-meetings-2026`  
**Source files:** `data/fig1-hyperscaler-capex-vs-lac-growth.csv` through `data/fig6-colombia-reform-impact.csv`

---

## Figure-to-Source Mapping

| Figure | Data file | IMF document | Chapter / section | Methodology note |
|---|---|---|---|---|
| Figure 1 — Hyperscaler Capex vs. LAC GDP Growth | `data/fig1-hyperscaler-capex-vs-lac-growth.csv` | IMF World Economic Outlook (Apr 2026) | Regional outlook — Latin America and the Caribbean | Uses WEO regional growth estimates as the macro backdrop for comparing hyperscaler capex concentration against LAC growth performance. |
| Figure 2 — Governance vs. Capital Stability | `data/fig2-governance-vs-capital-stability.csv` | IMF Global Financial Stability Report (Apr 2026) | Chapter 2 — Institutional quality and financial stability | Treats governance quality as a macro-financial explanatory variable and links rule-of-law variation to capital flight premiums (r = 0.67). |
| Figure 3 — Mexico GDP Growth Scenarios | `data/fig3-mexico-growth-scenarios.csv` | IMF World Economic Outlook (Apr 2026) | Mexico country outlook / conditional scenario | Presents a baseline (1.6%) and a governance-reform scenario (2.2%) consistent with IMF-style conditional macroeconomic analysis. |
| Figure 4 — NBFI Yield Premium by Institutional Quality | `data/fig4-nbfi-yield-premium.csv` | IMF Global Financial Stability Report (Apr 2026) | Chapter 2 — Nonbank financial institutions / yield spread analysis | Maps institutional quality to NBFI yield premiums. Primary candidate for FSI-oriented engagement. |
| Figure 5 — Sovereign-Bank Nexus Amplification | `data/fig5-sovereign-bank-nexus.csv` | IMF Global Financial Stability Report (Apr 2026) | Chapter 2 — Cross-sector contagion / sovereign-bank nexus | Quantifies how a 100bp sovereign spread shock transmits through the NBFI channel into 160bp total amplification. |
| Figure 6 — Colombia Sovereign Spread Impact | `data/fig6-colombia-reform-impact.csv` | Central Bank of Colombia / IMF Article IV surveillance context | Sovereign spread and institutional reform signaling (Apr 2024 – Apr 2026) | Time-series case showing −110bp spread compression associated with governance reform signals. |

---

## FSI Framework Alignment

SM26 evidence aligns most directly with the following IMF Financial Soundness Indicator priorities:

### Priority 1 — NBFI Stability Indicators (FSI Group 7, Other Financial Institutions)
- **Primary evidence:** Figures 4 and 5
- **Why it matters:** These figures quantify the nonbank channel and the associated yield premium under different institutional quality environments. The $4T nonbank portfolio inflows to emerging markets (IMF GFSR Ch.2 Apr 2026) is the macro anchor.

### Priority 2 — Sovereign Risk Transmission
- **Primary evidence:** Figures 5 and 6
- **Why it matters:** The repo shows how sovereign stress amplifies through related financial channels (100bp → 160bp) and how reform signals compress that spread over time (Colombia −110bp, 2024–2026).

### Priority 3 — Governance as a Macro-Financial Variable (cross-cutting)
- **Primary evidence:** Figure 2
- **Why it matters:** Institutional quality is used as an explanatory input, not background context. The r = 0.67 correlation between rule-of-law and NBFI stability is the methodological contribution. 1pp improvement in rule-of-law yields −60bp in capital flight premium.

**Not mapped:** Capital adequacy ratios, asset quality, bank-level liquidity indicators. The dataset does not support those mappings and no spurious mapping is introduced here.

---

## Article IV / Surveillance Use Cases

| Figure | Surveillance use case |
|---|---|
| Figure 2 | Governance-to-stability hypothesis for cross-country comparative surveillance |
| Figure 3 | Conditional growth scenario for Mexico institutional reform policy discussion |
| Figure 6 | Sovereign spread case study — Colombia governance reform pathway (2024–2026) |

---

## Predictive Alignment Note

SM26 was published April 2026. Between May and June 2026, the US export control episode affecting frontier AI access demonstrated the exact hyperscaler-dependency vulnerability quantified in Paper I. The NBFI fragility mechanism described in Paper II — whereby institutional quality determines the speed and scale of capital flight — reflects dynamics visible in real-time emerging market stress events in the same window.

This alignment is noted here for context, not as a claim of causation. The research predated these events.

---

## Repository Context

This repository is a policy research artifact. Its value comes from:
- Reproducible tabular evidence in `data/`
- Citation support in `CITATION.md`
- Long-form policy framing in `README.md`
- This mapping document as the institutional traceability layer

---

*Avant.Dev Policy Intelligence · erick@avant.dev · [avant.dev](https://avant.dev)*  
*UN ITU P2C #7528 · IMF ROC Phase II · GDAIG Geneva Jul 2026*
