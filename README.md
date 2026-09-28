# 🗄️ Enterprise Data Warehouse Analytics Platform (SQL)

## 📌 Project Overview
This project demonstrates the design, deployment, and querying of an enterprise-grade **Data Warehouse (`DataWarehouseAnalytics`)** built on **SQL Server**. The repository contains modular SQL scripts covering the end-to-end data engineering and analytics pipeline—from schema creation (`gold` schema star model) and bulk ETL loading to advanced T-SQL analytical reporting.

---

## 🏗️ Architecture & Schema
- **Schema Model:** Star Schema (`gold` schema)
- **Dimension Tables:** `gold.dim_customers`, `gold.dim_products`
- **Fact Table:** `gold.fact_sales`
- **RDBMS Engine:** Microsoft SQL Server (T-SQL)

---

## 📂 Repository Structure & SQL Pipeline
- `00_init_database.sql`: Database initialization, schema creation (`gold`), and bulk data ingestion (`BULK INSERT`).
- `01_database_exploration.sql`: Metadata analysis using `INFORMATION_SCHEMA` for column and constraint verification.
- `02_dimensions_exploration.sql`: Entity integrity checks on customer origins and product catalog hierarchies.
- `03_date_range_exploration.sql`: Temporal boundary analysis using `MIN()`, `MAX()`, and `DATEDIFF()`.
- `04_measures_exploration.sql`: KPI aggregation reports built with `UNION ALL` for key business metrics.
- `05_magnitude_analysis.sql`: Grouped aggregate distributions across countries, categories, and channels.
- `06_ranking_analysis.sql`: Performance ranking using window functions (`RANK() OVER()`, `ROW_NUMBER()`).
- `07_change_over_time_analysis.sql`: Time-series trend analysis using `DATETRUNC()` and `FORMAT()`.
- `08_cumulative_analysis.sql`: Running sales totals and moving average calculations (`SUM() OVER(ORDER BY)`).
- `09_performance_analysis.sql`: Year-over-Year (YoY) comparative analysis utilizing CTEs, `LAG()`, and conditional growth logic (`CASE`).

---

## 💡 Advanced T-SQL Techniques Featured
- **Data Warehousing & ETL:** Star Schema design, metadata management, transaction controls, and automated bulk loads.
- **Analytic Window Functions:** `RANK()`, `DENSE_RANK()`, `SUM() OVER()`, `AVG() OVER()`, `LAG() OVER()`.
- **Advanced Aggregations:** CTEs, subqueries, conditional formatting (`CASE`), temporal calculations (`DATETRUNC`, `DATEDIFF`), and multi-table joins.
