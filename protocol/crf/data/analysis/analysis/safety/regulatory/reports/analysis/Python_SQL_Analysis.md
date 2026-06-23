# Python and SQL Analysis for HPV Screening Dataset

## Objective

Demonstrate the use of Python and SQL for clinical data management and healthcare analytics.

---

# Python Analysis Workflow

## Import Dataset

```python
import pandas as pd

df = pd.read_csv("hpv_clinical_dataset.csv")
print(df.head())
```

## HPV Positivity Rate

```python
positive_rate = (df["HPV_Result"] == "Positive").mean() * 100
print(f"HPV Positivity Rate: {positive_rate:.1f}%")
```

## Average Participant Age

```python
average_age = df["Age"].mean()
print(f"Average Age: {average_age:.1f}")
```

## Adverse Event Summary

```python
df["Adverse_Event"].value_counts()
```

---

# SQL Queries

## Total Participants

```sql
SELECT COUNT(*) AS Total_Participants
FROM hpv_dataset;
```

## HPV Positive Participants

```sql
SELECT COUNT(*) AS Positive_Cases
FROM hpv_dataset
WHERE HPV_Result = 'Positive';
```

## Average Age

```sql
SELECT AVG(Age) AS Average_Age
FROM hpv_dataset;
```

## Adverse Event Review

```sql
SELECT Participant_ID, Adverse_Event
FROM hpv_dataset
WHERE Adverse_Event <> 'No';
```

---

# Skills Demonstrated

* Python for Healthcare Analytics
* SQL for Clinical Data Review
* Clinical Data Management
* Statistical Analysis
* Data Validation
* Healthcare Reporting
* Clinical Research Analytics
