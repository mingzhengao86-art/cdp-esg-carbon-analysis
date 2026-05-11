# Data Source

**CDP 2019 Full Climate Change Dataset**

- **Provider:** Carbon Disclosure Project (CDP)
- **Source:** [Kaggle — CDP Unlocking Climate Solutions](https://www.kaggle.com/competitions/cdp-unlocking-climate-solutions/data)
- **Format:** Apache Feather (.feather)
- **Coverage:** 965 companies, 2019 disclosure year

## Files Used
- `2019_Full_Climate_Change_Dataset.feather` — Full questionnaire responses (~1.1M rows)
- `2019_Corporates_Disclosing_to_CDP_Climate_Change.feather` — Corporate metadata

## Note
- The large file (`2019_Full_Climate_Change_Dataset.feather`, 551MB) is stored via **Git LFS**.
- Revenue data sourced from Yahoo Finance via `yfinance` (US-listed companies only).
