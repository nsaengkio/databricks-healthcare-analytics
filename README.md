# Healthcare Encounter Analytics on Databricks

This project demonstrates an end-to-end analytics workflow using Databricks, PySpark, and Delta Lake on synthetic healthcare data.

## Architecture

- **Bronze**: Raw Delta tables from CSV (patients, encounters, providers)
- **Silver**: Cleaned and enriched encounters (IsNoShow, LOS_Category)
- **Gold**: Analytics-ready fact table for BI tools

## Tech Stack

- Databricks
- PySpark
- Delta Lake
- SQL
- (Optional) Power BI

## Notebooks

1. `01_ingest_raw_data.py` – Load CSVs into Delta bronze tables  
2. `02_transform_encounters.py` – Clean and enrich encounters into silver  
3. `03_delta_optimization.py` – Optimize Delta tables  
4. `04_analytics_tables.sql` – Create gold fact table  
5. `05_powerbi_model_notes.md` – Notes for downstream BI modeling

## Data

All data in `data/raw/` is synthetic and for demonstration only.
