# 🌍 Earthquake Lakehouse – Medallion Architecture with Airflow

## 🚀 Project Overview

End-to-end Data Engineering project implementing a Lakehouse architecture using:

- Apache Airflow (Orchestration)
- Dockerized Environment
- Python
- Parquet Storage
- Medallion Architecture (Raw, Bronze, Silver, Gold)
- Dimensional Modeling (Star Schema)
- Power BI Dashboard

---

## 🏗 Architecture

Medallion pattern:

Raw → Bronze → Silver → Gold

### 🔹 Raw
- Ingestion of earthquake data from USGS API (JSON)

### 🔹 Bronze
- Structured parquet conversion
- Basic normalization

### 🔹 Silver
- Data cleaning
- Deduplication
- Type standardization
- Quality filters

### 🔹 Gold
- Star Schema design
- Fact table: `fact_earthquakes`
- Dimensions:
  - dim_date
  - dim_location
  - dim_event_type
  - dim_status

---

## 📊 Analytics & Visualization

Power BI dashboard built on dimensional model:

- Temporal trend analysis
- Magnitude distribution
- Depth vs Magnitude correlation
- Geospatial mapping
- Tsunami impact analysis

---

## 🧠 Data Engineering Concepts Applied

- ETL orchestration with Airflow
- TaskGroups
- Docker containerization
- Parquet-based lakehouse
- Dimensional modeling
- Clean separation of layers
- Git version control

---

## 🛠 How to Run

```bash
docker compose up -d
