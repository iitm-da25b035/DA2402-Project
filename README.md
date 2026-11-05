# DA2402-Project

Airline recovery after COVID and other performance factors for Indian domestic airlines.

**Live dashboard:** https://iitm-da25b035.github.io/DA2402-Project-Deploy/

## Run order
1. `notebooks/dgca_download_pipeline.ipynb`: collects the raw files and builds `data/interim/`. By default it rebuilds from `data/raw/` with no network; set `REFRESH = True` to collect again.
2. `notebooks/dgca_cleaning_analysis.ipynb`: builds `data/clean/`, including the cleaning log and data dictionary.
3. `notebooks/dgca_dashboard_v5.ipynb`: writes `outputs/dashboard/dgca_dashboard_v5_<date>.html`.

Install the packages with `pip install -r requirements.txt`. The collection step also needs Google Chrome.

## Sources
- DGCA monthly domestic air transport statistics: https://www.dgca.gov.in/digigov-portal/?baseLocale=en_US?page=259/4184/servicename, collected 2026-11-01.
- Vonter/india-aviation-traffic (ODbL), commit `e197170`: https://github.com/Vonter/india-aviation-traffic, collected 2026-11-01; `city.csv` fetched 2026-11-04 from the same commit.

## Folders
- `data/raw/`: files as collected, never edited.
- `data/interim/`: parsed table, city-pair table, profiles and cross-checks.
- `data/clean/`: clean tables, `cleaning_log`, `data_dictionary` and check results.
- `outputs/dashboard/`: the final dashboard.
