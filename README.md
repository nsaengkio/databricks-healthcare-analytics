# Healthcare Encounter Analytics on Databricks

This project demonstrates an end-to-end analytics workflow using **Databricks**, **PySpark**, and **Delta Lake** on synthetic healthcare encounter data. It follows the Medallion Architecture (Bronze → Silver → Gold) and produces analytics-ready tables suitable for BI tools such as Power BI.

---

## 🏗️ Architecture Overview

### **Bronze Layer**
Raw CSV files are ingested into Delta Lake tables:
- Patients
- Encounters
- Providers

### **Silver Layer**
Data is cleaned and enriched:
- Standardized date formats  
- No-show flag  
- Length-of-stay categories  
- Basic data quality checks  

### **Gold Layer**
Analytics-ready fact table:
- FactEncounter  
- Supports BI dashboards and reporting  

---

## 🧰 Tech Stack

- **Databricks**
- **PySpark**
- **Delta Lake**
- **SQL**
- **Healthcare domain logic**
- **Power BI (optional)**

---

## 📘 Notebooks

| Notebook | Description |
|---------|-------------|
| `01_ingest_raw_data.py` | Load raw CSVs into Delta bronze tables |
| `02_transform_encounters.py` | Clean & enrich encounter data into silver |
| `03_delta_optimization.py` | Optimize Delta tables with Z-Ordering |
| `04_analytics_tables.sql` | Create gold fact table |
| `05_powerbi_model_notes.md` | Notes for downstream BI modeling |

---

## 🗂️ SQL Layers

- `sql/create_bronze_tables.sql`  
- `sql/create_silver_tables.sql`  
- `sql/create_gold_tables.sql`  

These scripts mirror real Databricks SQL workflows.

---

## 🧩 Dimensional Model

Located in the `models/` folder:

- `fact_encounter.sql`
- `dim_patient.sql`
- `dim_provider.sql`
- `dim_date.sql`

This demonstrates a standard star schema used in BI engineering.

---

## 📊 Data

All data in `data/raw/` is **synthetic** and safe for public use.

---

## 🚀 Future Enhancements

- Add dbt version of the project  
- Add Power BI dashboard  
- Add unit tests for transformations  
- Add CI/CD workflow for Databricks notebooks  

---

## 📄 License

MIT License (optional)
