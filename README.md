# CDP 2019 Corporate Climate Change Disclosure — ESG Carbon Analysis

A full ESG carbon emissions analysis of 965 companies using 2019 CDP (Carbon Disclosure Project) corporate climate disclosure data — covering Scope 1/2/3 benchmarking, carbon intensity modeling, disclosure gap analysis, and data quality flagging.

---

## Research Questions

1. Which companies and sectors are the largest Scope 1 emitters?
2. How large is the Scope 3 disclosure gap across industries?
3. Which companies deviate most from their sector average emissions?
4. What is the carbon intensity (tCO₂e per $M revenue) of US-listed companies?
5. Which companies report anomalous zero emissions — and why does it matter?

---

## Repository Structure

```
cdp-esg-carbon-analysis/
├── cdp_esg_analysis.ipynb        # Main analysis notebook
├── figures/                       # Output visualizations
│   ├── fig1_disclosure_gap.png
│   ├── fig2_sector_benchmark.png
│   ├── fig3_industry_deviation.png
│   └── fig4_carbon_intensity.png
├── results/                       # Output tables (CSV)
│   ├── disclosure_gap.csv
│   ├── emissions_model.csv
│   ├── sector_benchmark.csv
│   ├── intra_sector_ranking_electrical.csv
│   ├── industry_deviation.csv
│   ├── carbon_intensity.csv
│   └── zero_reporters.csv
└── data/
    └── data_source.md             # Data source documentation
```
---

## Key Findings

| Finding | Detail |
|---------|---------|
| **Scope 3 disclosure gap** | 415 companies missing vs 200 (Scope 1) and 280 (Scope 2) |
| **Highest Scope 1 sectors** | Air transport and thermal power generation |
| **Tesla non-disclosure** | Absent from entire 2019 CDP dataset — itself an ESG signal |
| **Highest carbon intensity** | Major US electric utilities (AES, OGE, AEP) |
| **Data quality flags** | 15 companies report Scope 1+2 = 0, including Atmos Energy (gas company) |

---

## Methods

- **Scope extraction:** CDP long-format questionnaire filtered by question codes C6.1, C6.3, C6.5
- **Emissions models:**
  - Industry standard: Scope 1 + Scope 2 (GHG Protocol)
  - Weighted model: Scope1×0.5 + Scope2×0.3 + Scope3×0.2 (exploratory)
  - Carbon intensity: (Scope1+2) / Revenue × 1,000,000 (tCO₂e per $M revenue)
- **Industry deviation:** Company Scope 1+2 minus sector mean
- **Revenue data:** Yahoo Finance via `yfinance` (US-listed companies only, ~372 of 965)

---

## Data Source

[CDP 2019 Full Climate Change Dataset — Kaggle](https://www.kaggle.com/datasets/cdp-unlocking-climate-solutions)

Data files not included due to size. See `data/data_source.md` for details.

---

## Dependencies

```bash
pip install pandas matplotlib yfinance
```

---

## Author

**Mingzhen Gao**
May 2026
