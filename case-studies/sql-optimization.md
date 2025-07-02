# 🧠 Case Study: Optimizing SQL Stored Procedure for NeoGenomics

**Client**: NeoGenomics (Top 20 Global Pharmaceutical Companies)  
**Tools**: Microsoft SQL Server 2018, SSIS, Tableau  
**Industry**: Healthcare, Cancer Diagnostics  
**Role**: SQL Developer

---

## 🧩 Problem

A critical stored procedure used in weekly data delivery to pharma clients was taking **45–60 minutes to execute**. This delay affected:

- Timely SSRS report generation
- SLA adherence for file delivery
- Internal job scheduling dependencies

---

## 🔍 Root Cause Analysis

- Multiple nested `SELECT` statements and scalar subqueries  
- Improper indexing on high-volume fact tables  
- Unnecessary `DISTINCT` operations  
- Non-parameterized joins across 5+ tables

---

## 🛠️ Solution

- **Refactored logic** using temporary tables and indexed staging views  
- **Implemented CTEs** to avoid redundant subqueries  
- **Introduced filtered non-clustered indexes** on commonly filtered columns  
- Rewrote joins using `INNER JOIN` instead of Cartesian subqueries  
- **Added SET STATISTICS TIME/IO** to benchmark performance

---

## 🚀 Result

| Metric | Before | After |
|--------|--------|-------|
| Execution Time | 47 mins | **7–10 mins** ✅  
| SLA Compliance | 85% | **100% for 6+ months** ✅  
| Report Accuracy | 92% | **99.99% verified via Tableau** ✅

---

## 💡 Client Impact

✔️ Timely delivery of genetic cancer reports to clients like Pfizer & AstraZeneca  
✔️ Helped internal teams reduce overnight job durations by ~45 mins  
✔️ Enhanced data quality, reduced escalation tickets

---
