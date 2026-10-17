# superstore-sales-sql-python-analytics
End-to-end data pipeline with data cleaning, SQL CTEs, window functions, and Seaborn visualizations.
# 📊 Retail Sales Performance & Supply Chain Logistics Pipeline

An end-to-end data analytics pipeline integrating **relational SQL databases** and **Python (Pandas, Seaborn, Matplotlib)** to evaluate retail sales drivers, regional revenue contribution, and supply chain turnaround metrics across 9,800+ transactions.

---

## 📌 Project Overview
Retail operations require continuous monitoring of revenue streams, product category performance, and logistics fulfillment turnaround. This project establishes an automated analytics pipeline that ingests raw transactional data into an SQLite relational database, performs structured SQL querying (including CTEs and Window Functions), and generates publication-grade visualizations.

---

## 🛠️ Tech Stack & Skills Demonstrated
- **Programming & Analysis:** Python (Pandas, NumPy, Datetime conversion)
- **Database Architecture:** SQLite3 / Relational Schema Ingestion
- **SQL Competencies:** Aggregations (`SUM`, `AVG`, `COUNT DISTINCT`), Subqueries, Common Table Expressions (CTEs), Window Functions (`RANK() OVER PARTITION BY`)
- **Data Visualization:** Matplotlib, Seaborn
- **Environment:** Google Colab, Jupyter Notebook, GitHub

---

## 📊 Executive Business KPIs Summary

| Enterprise Metric | Value |
| :--- | :--- |
| **Total Orders Analyzed** | 4,922 |
| **Unique Customer Base** | 793 |
| **Total Line Items Sold** | 9,800 |
| **Gross Sales Revenue** | $2,261,536.78 |
| **Average Order Value (AOV)** | $230.77 |
| **Average Shipping Turnaround** | 4.0 Days |

---

## 🔍 Key Analytical Findings & Business Insights

### 1. Regional Sales Dominance
- The **West** ($710,219.68 | 31.40%) and **East** ($669,518.73 | 29.60%) regions generate over **61%** of total gross revenue.
- The **South** region accounts for the lowest revenue share ($389,151.46 | 17.21%), indicating opportunities for targeted marketing expansion.

### 2. High-Grossing Product Sub-Categories
- **Phones** ($327,782.45) and **Chairs** ($322,822.73) represent the highest revenue-generating sub-categories.
- Office Supplies items (like Binders and Paper) contribute high order volumes with lower average order values ($134.07 AOV for Binders).

### 3. Supply Chain Turnaround Efficiency
- Transit durations strictly conform to logistics service levels:
  - **Same Day:** 0.0 Days average delivery
  - **First Class:** 2.2 Days average delivery
  - **Second Class:** 3.2 Days average delivery
  - **Standard Class:** 5.0 Days average delivery

### 4. Multi-Year Sales Velocity
- Annual gross revenue exhibited steady upward growth:
  - **2015:** $479,856.21
  - **2016:** $459,436.01
  - **2017:** $600,192.55
  - **2018:** $722,052.02 (Peak sales velocity with 1,661 orders)

---

## 🗂️ Project Pipeline Architecture

```text
train.csv (Raw Transactions)
    │
    ├──> Python Pipeline (Data Cleaning & Datetime Parsing)
    │
    ├──> Ingest to SQLite DB (`orders` table)
    │
    ├──> Analytical SQL Queries (CTEs, Window Functions, Group Aggregations)
    │
    └──> Seaborn & Matplotlib Visual Reporting (Trends, Distributions, Turnaround)
