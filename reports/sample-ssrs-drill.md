# 🧬 Genetic Test Outcomes – SSRS Drill-Through Report

**Client**: NeoGenomics  
**Tool**: SQL Server Reporting Services (SSRS)  
**Use Case**: Drill-through report from summary (disease type) → detail (mutation panel)

---

## 🔍 Main Report (Summary View)

- Grouped by **Cancer Type** (e.g., Breast, Lung, Colon)
- Shows count of patients per week, per lab

![Main Chart](../assets/ssrs-summary-bar-chart.png)

---

## 🔁 Drill-Through Report (Detail View)

- Shows each **Patient ID**, Gene Panel (EGFR, ALK, BRAF, etc.), and result (POS/NEG)
- Triggered by clicking the summary bar

![Drill Chart](../assets/ssrs-drill-table.png)

---

## 🔧 Features

- Linked Reports  
- Parameterized Filters (Hospital, Week, Gene)  
- CSV Export + Email Subscription  
- Built-in Error Handling

---

## ✅ Impact

- Automated genetic reporting for 10+ pharma clients  
- Replaced Excel-based manual summaries  
- Improved data visibility and turnaround time by **80%**
