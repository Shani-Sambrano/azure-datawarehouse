# Azure Data Warehouse – Elevate AI Solutions

Azure Synapse & Data Lake project for **Elevate AI Solutions** – Data Engineering and AI Analytics.

This repository contains the **Azure Synapse & Data Lake implementation** for Elevate AI Solutions.  
It serves as a learning and production-ready environment for data engineering, analytics, and AI orchestration projects.

---

## 🧱 Architecture Overview
- **Azure Data Lake (ADLS Gen2)** – raw, silver, and gold zones  
- **Azure Synapse Analytics (Serverless SQL Pool)** – query and transformation layer  
- **Azure Data Factory / Synapse Pipelines** – ETL orchestration  
- **Power BI / QuickSight** – visualization and reporting  
- **GitHub Integration** – version control for SQL, notebooks, and pipelines

---

## 📁 Data Lake Zones

data/
├─ raw/ # landing zone for unprocessed source data
├─ silver/ # cleaned & standardized datasets
└─ gold/ # business-ready, aggregated models

| Zone | Purpose | Typical Files | Example Actions |
|------|----------|----------------|----------------|
| **raw** | Exact copies from source systems | CSV, JSON, Parquet | Ingest data, maintain history, add partitions |
| **silver** | Cleaned and standardized datasets | Parquet | Apply schema, deduplicate, enrich |
| **gold** | Curated analytical data | Parquet, views | Aggregate facts, create ML features, build reports |

**Quick links:**  
[`data/raw`](./data/raw) • [`data/silver`](./data/silver) • [`data/gold`](./data/gold)

---

## 🧩 Synapse Mapping
- External source → **ADLS Gen2** (this repo mirrors its structure)  
- Ingest to `raw/` via Copy activity or Spark  
- Transform to `silver/` using SQL or Data Flow  
- Publish `gold/` layer as Parquet and expose via external tables or views  

---

## 📁 Full Folder Structure

azure-datawarehouse/
├─ data/
│ ├─ raw/
│ ├─ silver/
│ └─ gold/
│
├─ notebooks/ # Synapse or Spark notebooks for transformations
├─ sql/ # SQL scripts for transformations & queries
├─ pipelines/ # JSON pipeline definitions
├─ linkedServices/ # Connection configs (Key Vault, Storage, SQL)
├─ datasets/ # Pipeline datasets (source/target mappings)
├─ triggers/ # Optional time/event triggers
├─ externalTables/ # CREATE EXTERNAL TABLE scripts
└─ views/ # Analytical or business SQL views


---

## 🧠 Learning Goals
- Practice **DP-203 Azure Data Engineering** lab patterns  
- Build reusable **data warehouse templates**  
- Showcase **data + AI pipeline orchestration** with version control  
- Experiment with **Synapse Serverless SQL** and **Spark Notebooks**

---

## ⚙️ Next Steps
1. Create an **ADLS Gen2 container** with folders `data/raw`, `data/silver`, `data/gold`.  
2. Connect **Synapse Studio → Manage → Git configuration → this repository.**  
3. Import or build pipelines for:  
   - `raw → silver` cleansing  
   - `silver → gold` aggregations  
4. Link **Power BI / QuickSight** for final visualization.  

---

## 🔗 Connect with Me
**Shani Sambrano**  
Chief Information Technology Officer – *Marinia Group, Inc.*  
🌐 [Elevate AI Solutions](https://elevate-aisolutions.com)  
📧 S.Sambrano@MariniaGroup.com  

---

*“Don’t just build data pipelines. Orchestrate intelligence.”* 🚀
