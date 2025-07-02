# 📈 Tableau KPI Dashboard – Cancer Clinical Trials

**Client**: NeoGenomics + Partner Pharma Clients  
**Tool**: Tableau (connected to Snowflake and SQL Server)  
**Domain**: Oncology, Diagnostics  
**Purpose**: Performance & Outcome Monitoring

---

## 📊 Dashboard Overview

The dashboard was created to monitor and optimize performance KPIs for cancer testing labs and trial sites. Data is refreshed weekly from ETL pipelines processed via Snowflake and SSIS.

---

## 🧩 KPI Components

### 1. Test Volume by Location (Map View)
- Displays testing centers across the US.
- Bubble size = Volume of tests conducted in that location.
- Drillable by test type or disease.

### 2. Weekly Volume Trend (Line Graph)
- X-axis: Test Weeks
- Y-axis: Number of Samples Processed
- Shows spike or drop in test processing over time.

### 3. Turnaround Time by Lab (Bar Chart)
- TAT measured in hours.
- Compares labs: Lab A, Lab B, Lab C.
- Highlighted bars for outliers or underperforming labs.

---

## 🔄 Data Pipeline

- Source: Raw test data from SQL Server
- ETL: Processed via SSIS into Snowflake staging
- Transformation: Snowflake Views & Materialized Tables
- Visualization: Tableau Public dashboards with embedded filters

---

## ✅ Client Benefits

- Enabled real-time monitoring of lab efficiency
- Facilitated faster decision-making in clinical trials
- Reduced turnaround time variance by 32%
- Improved trial drug targeting by mutation positivity analysis

---

## 📌 Notes

- Refreshed every Monday 6 AM EST via Tableau scheduler
- Used in FDA submission documentation and R&D reviews
- View-level row-level security implemented for client segmentation
