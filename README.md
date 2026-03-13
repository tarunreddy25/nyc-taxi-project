# 🚕 NYC Taxi Data Analysis

![Python](https://img.shields.io/badge/Python-3.10+-blue) ![DuckDB](https://img.shields.io/badge/DuckDB-SQL-yellow) ![Pandas](https://img.shields.io/badge/Pandas-Data%20Cleaning-green) ![GitHub](https://img.shields.io/badge/Status-Complete-brightgreen)

A real-world data engineering project analyzing **2.96 million NYC Yellow Taxi trips** from January 2024. Covers data ingestion, cleaning, SQL analysis, and exporting results — the core workflow of a professional data engineer.

---

## 📊 Project Overview

| Item | Detail |
|---|---|
| Dataset | NYC Yellow Taxi Trip Records — January 2024 |
| Source | NYC Taxi & Limousine Commission (Open Data) |
| Total rows | 2,964,624 |
| Cleaned rows | 2,723,805 |
| Bad rows removed | 240,819 |
| Tools used | Python, Pandas, DuckDB, SQL |

---

## 🔍 Key Findings

1. **Peak hours are 3pm–7pm** — evening rush hour dominates taxi demand
2. **Wednesday is the highest revenue day** — $13.3M vs $9M on Sundays
3. **60% of trips are under 2 miles** — averaging $9.91 per trip
4. **Average tip is exactly 20%** — riders tap the default suggested tip
5. **Groups of 4 pay the most** — averaging $22.86 per trip

---

## 🛠️ What This Project Does

### 1. Data Ingestion
Downloads the NYC Taxi Parquet file (2.96M rows) programmatically using Python's `requests` library.

### 2. Data Cleaning
Uses Pandas to identify and remove bad records:
- Trips with zero or negative distance
- Trips with zero or negative fare
- Missing passenger counts
- Impossible values (e.g. a trip distance of 312,722 miles!)

### 3. SQL Analysis with DuckDB
Runs 5 business questions directly on the Parquet file using DuckDB — no database server needed:
- Average fare by passenger count
- Busiest pickup hours
- Top revenue days of the week
- Average tip percentage
- Trip distribution by distance category

### 4. Results Export
Saves all query results as CSV files for use by analysts or downstream pipelines.

---

## 📁 Project Structure

```
nyc-taxi-project/
│
├── analyze.py              # Main analysis script
├── summary.md              # Written findings
├── .gitignore              # Excludes large parquet file
│
└── results/
    ├── hourly_trips.csv        # Trips and avg fare by hour
    ├── daily_revenue.csv       # Revenue and trips by day
    └── trip_categories.csv     # Short / medium / long trip breakdown
```

---

## 🚀 How to Run

**1. Clone the repository:**
```bash
git clone https://github.com/tarunreddy25/nyc-taxi-project.git
cd nyc-taxi-project
```

**2. Install dependencies:**
```bash
pip install pandas duckdb requests pyarrow
```

**3. Download the dataset and run analysis:**
```bash
python analyze.py
```

Results will be saved to the `results/` folder.

---

## 💡 Skills Demonstrated

- **Data ingestion** — fetching real data from a public source
- **Data cleaning** — identifying and removing invalid records with Pandas
- **SQL querying** — GROUP BY, aggregations, CASE statements, date functions
- **Data quality** — spotting anomalies in real-world messy data
- **Git & GitHub** — version control and portfolio publishing

---

## 📈 Next Steps

This project is **Phase 1** of my AI Data Engineering learning path. Coming next:
- Phase 2 — ETL pipeline with Apache Airflow + PostgreSQL
- Phase 3 — Cloud data lake on AWS S3 + Delta Lake
- Phase 4 — RAG pipeline with vector databases

---

## 👤 Author

**Tarun Reddy Gaddam**  
Aspiring AI Data Engineer  
GitHub: [@tarunreddy25](https://github.com/tarunreddy25)
