# ❄️ Case Study: Hybrid ETL Flow Using Snowflake for Precision Oncology

**Client**: NeoGenomics  
**Tools**: Snowflake, SSIS, SQL Server, Tableau  
**Industry**: Precision Medicine, Pharma  
**Role**: Snowflake Developer

---

## 🧩 Problem

Pharmaceutical clients needed **weekly genomics datasets** from multiple systems (SQL Server + external APIs) consolidated into Snowflake for:

- Cancer mutation tracking  
- Drug-response modeling  
- Clinical research dashboards

---

## 🌐 Challenges

- **Inconsistent schema** across hospitals & labs  
- 500,000+ rows per week (biomarker-level data)  
- Manual data transformation created bottlenecks  
- Multiple endpoints per client

---

## 🛠️ Solution Design

- Used **SSIS** to extract and cleanse raw data from SQL Server  
- Built **XML payloads** in SQL and ingested them to **Snowflake** staging area  
- Developed **Snowflake tasks** and `MERGE` logic to insert/update clinical data  
- Created **modular views** with secure filters for each client  
- Automated file delivery using SSRS subscriptions + Snowflake scheduler

---

## 📊 Data Flow Diagram

```mermaid
graph TD
  A[SQL Server] --> B[SSIS XML Builder]
  B --> C[Snowflake Staging Table]
  C --> D[Snowflake MERGE Logic]
  D --> E[Client-Specific Views]
  E --> F[SSRS Reports + Tableau Dashboards]
