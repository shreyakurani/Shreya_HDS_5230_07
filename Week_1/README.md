# High Performance Computing – Assignment 1: Simulated Electronic Health Record (EHR) Analysis

## 📋 Overview

This assignment involves analyzing a set of **simulated electronic health record (EHR) datasets** to explore trends in patient health outcomes and healthcare usage patterns. The goal is to apply **high-performance data manipulation techniques using `data.table` in R** to extract meaningful insights.

> ⚠️ *Note: All datasets provided are simulated and not based on real patient data.*

---

## 📂 Dataset Descriptions

The following are the files used for analysis and their major relationships and features:

### 1. `OutpatientVisit.csv`
– Has one row for each outpatient visit.
- **Join keys**:
  - `PatientID` → `Patient.csv`
  - `ClinicID` → `Clinic.csv`
  - `StaffID` → `Staff.csv`
  - `ICD10_1`, `ICD10_2`, `ICD10_3` → `ICDCodes.csv`

### 2. `Patient.csv`
- One row per patient.
- Contains demographic information (e.g., age, gender).
- **Join key**: `PatientID`

### 3. `Clinic.csv`
- Describes each clinic's type: *primary care*, *specialty*, or *emergency*.
- **Join key**: `ClinicID`

### 4. `Staff.csv`
- Contains info about medical staff (e.g., roles, affiliations).
- **Join key**: `StaffID`

### 5. `Mortality.csv`
- Lists `PatientID` and `DateOfDeath` for deceased patients.
- Patients **not listed** are considered alive.

### 6. `ICDCodes.csv`
– Maps an ICD10 code to disease description.

### 7. `DiseaseMap.csv`
- Groups ICD codes into **22 clinically meaningful categories** (e.g., "Diabetes", "Stroke").

---

## ❓ Assignment Questions

### **Q1. Are men more likely to die than women in this group of patients?**
- Use `Patient.csv` and `Mortality.csv` to calculate death rates by gender.
- Assume patients **not listed in `Mortality.csv` are still alive**.
  
  ### **Q2. Are there patterns in the disease groups across gender?**
- For every patient with at least one outpatient visit, determine whether they were diagnosed with any of the 22 disease categories in `DiseaseMap.csv`.
- Examine all the three diagnosis fields. `ICD10_1`, `ICD10_2`, and `ICD10_3`.
- Output a table similar to below:

| Disease   | Men  | Women | All   |
|-----------|------|--------|-------|
| Alcohol   | XX%  | XX%    | XX%   |
| Cancer   | XX% | XX%  | XX%   |
| …. | … | … | … |
Stroke | XX%  | XX%    | XX%   |

### **Q3. Calculate the mortality rate for every year between 2005 and 2018.**
- Use `OutpatientVisit.csv` to determine year of first riskfor each patient.
- Use `Mortality.csv` to record death year, if applicable.
- A patient only contributes to a year if he or she is alive at the beginning of the year.
- Find out whether the annual mortality is rising or falling.

---

 ##**Tips for Implementation**
- Use `fread()` and `data.table` syntax for high-performance manipulation.
- Use merging (`merge()` or `on=.`) and long-format reshaping where applicable.
- Validate joins and missing values (especially for mortality data).
- Use helper functions like `calculate_annual_mortality()` to encapsulate logic.



---

## 👩‍💻 Author
**Shreya Kurani**  
WEEK_1_ASSIGNMENT
Spring 2025

---
