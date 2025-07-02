# 📈 Tableau KPI Dashboard – Cancer Diagnostics & Drug Trials

**Client**: Pfizer, AstraZeneca, Novartis (via NeoGenomics)  
**Tool**: Tableau + Snowflake backend  
**Purpose**: Track test volumes, TAT, positive rates, and drug-match efficiency

---

## 🧩 Dashboard Snapshots

### 📍 Tests by Location (Map)

![Map](../assets/tableau-map-tests.png)

---

### 📊 Weekly Volume Trend

![Line Chart](../assets/tableau-weekly-volume.png)

---

### ⏱️ Turnaround Time (TAT) by Lab

![Bar Chart](../assets/tableau-tat-bar.png)

---

## 🔄 Data Flow

- Raw test data pulled via **SSIS** from SQL Server  
- Snowflake staging for data modeling  
- Tableau connects to Snowflake live extract  
- Auto-refresh every Monday via task scheduler

---

## ✅ Business Value

- Enabled Pharma clients to **track real-time lab performance**  
- Improved compliance & response to FDA audits  
- Prioritized drug pipeline based on **mutation-positive rates**

---
