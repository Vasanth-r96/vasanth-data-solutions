# 🧬 SSRS Drill-Through Report – Genetic Test Outcomes

**Client**: NeoGenomics  
**Tool**: SQL Server Reporting Services (SSRS)  
**Domain**: Healthcare, Pharma  
**Report Type**: Summary + Drill-through

---

## 🔍 Overview

This report suite was designed to allow cancer research labs and pharma companies to drill from **summary patient counts by disease type** to **detailed mutation-level test outcomes**.

---

## 📊 Summary Report

- Displays total number of patients tested per week.
- Grouped by: Disease Type (Breast, Lung, Colon), Lab, and Test Week.
- Designed using bar charts with color-coded disease markers.
- Filters: Date Range, Lab, Disease Type.

---

## 🔁 Drill-Through Report

- Activated by clicking on a disease/lab/week from the main report.
- Shows:
  - Patient ID
  - Gene tested (e.g., EGFR, ALK, BRAF)
  - Mutation Result (POS / NEG)
- Fully parameterized for export in CSV or PDF.
- Drill-through implemented using linked SSRS reports.

---

## ✅ Business Impact

- Replaced manual Excel-based reporting workflows.
- Reduced average reporting time from 2 days to under 2 hours.
- Increased accuracy of reported mutations by 98.7%.
- Used by over 10 pharma clients, including Pfizer and GSK.

---

## 📌 Notes

- Reports scheduled for weekly delivery via SSRS subscriptions.
- Security: Filtered views ensure client-specific access to data.
