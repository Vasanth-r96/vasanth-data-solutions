# 🔄 SSIS Package: Raw to Cleaned XML Transformation

**Client**: NeoGenomics  
**Tool**: SSIS (SQL Server Integration Services)  
**Domain**: Healthcare, Pharma Data Automation  
**Goal**: Convert raw database records into cleaned XML format for downstream consumption

---

## 🎯 Objective

To design and automate an SSIS pipeline that extracts **raw, multi-source data** (lab reports, patient details, test outcomes), transforms it to a **validated and structured XML format**, and pushes it to downstream systems or APIs.

---

## 🔧 Technical Overview

### ✅ Input:
- SQL Server tables:
  - `Raw_Patient_Data`
  - `Lab_Results_Staging`
  - `Test_Outcome_Master`

### 🔄 Process Flow:

| Step | Task |
|------|------|
| 1 | Extract data from multiple SQL tables using OLE DB Source |
| 2 | Cleanse nulls, trim values, deduplicate using `Derived Column` and `Sort` |
| 3 | Merge datasets using `Merge Join` and `Lookup` |
| 4 | Validate required fields using `Conditional Split` |
| 5 | Generate XML using `Script Task` or `XML Task` |
| 6 | Save XML to shared folder or pass to Mulesoft API |

---

## 🧩 SSIS Components Used

- **Control Flow**:
  - `Execute SQL Task` – For pre-validation and truncation
  - `File System Task` – For output archiving
  - `Script Task` – To build hierarchical XML if advanced logic needed
- **Data Flow**:
  - `Derived Column`, `Data Conversion`, `Lookup`, `Conditional Split`
  - `Sort` + `Union All` for merge cleanup

---

## 🧾 Sample XML Output Format

```xml
<Patient>
  <PatientID>12345</PatientID>
  <Name>John Doe</Name>
  <Test>
    <Type>EGFR</Type>
    <Result>Positive</Result>
    <TestDate>2024-03-15</TestDate>
  </Test>
</Patient>
