# IPL 2026 Data Immersion & Wrangling Project

## Project Overview

This project was completed as part of a Data Analytics Internship focused on Data Immersion and Data Wrangling. The objective was to understand, assess, clean, and transform an IPL 2026 ball-by-ball deliveries dataset into an analysis-ready format.

---

## Objectives

* Understand the structure and contents of the dataset.
* Perform data quality assessment.
* Identify missing values and duplicate records.
* Clean and transform the dataset.
* Create meaningful features for future analysis.
* Generate a final cleaned dataset.

---

## Dataset Information

* Dataset Name: IPL 2026 Deliveries Dataset
* Total Records: 17,477
* Original Features: 21
* Final Features: 25

The dataset contains ball-by-ball information including match details, batting and bowling teams, players, runs scored, extras, and wicket events.

---

## Data Dictionary

A separate Data_Dictionary.xlsx file has been created containing:

* Column names
* Data types
* Descriptions
* Business relevance

---

## Data Quality Assessment

### Missing Values

| Column           | Missing Values |
| ---------------- | -------------: |
| wicket_type      |         16,598 |
| player_dismissed |         16,602 |
| fielder          |         16,791 |

**Observation:**

These missing values are expected because most deliveries do not result in wickets. Therefore, they represent valid cricket match scenarios rather than data quality issues.

### Duplicate Records

* Duplicate Rows Found: 0

No duplicate records were identified in the dataset.

---

## Data Cleaning Performed

The following cleaning operations were performed:

1. Loaded and explored the dataset.
2. Verified column data types.
3. Assessed missing values.
4. Checked for duplicate records.
5. Converted the date column to datetime format.
6. Standardized text-based fields by removing unnecessary spaces.
7. Validated dataset consistency.

---

## Feature Engineering

The following new features were created:

| Feature    | Description                           |
| ---------- | ------------------------------------- |
| year       | Year extracted from match date        |
| month      | Month extracted from match date       |
| day        | Day of week extracted from match date |
| total_runs | Sum of runs_of_bat and extras         |

Example:

```python
df['total_runs'] = df['runs_of_bat'] + df['extras']
```

---

## Final Dataset

The final cleaned dataset contains:

* Rows: 17,477
* Columns: 25
* Duplicate Records: 0

The dataset is ready for:

* Team performance analysis
* Batting analysis
* Bowling analysis
* Venue analysis
* Scoring trend analysis
* Match outcome studies

---

## Technologies Used

* Python
* Pandas
* NumPy
* Jupyter Notebook

---

## Project Files

```text
IPL-2026-Data-Wrangling/
│
├── IPL_Data_Wrangling.ipynb
├── IPL_2026_Cleaned.csv
├── Data_Dictionary.xlsx
└── README.md
```

---

## Author

Data Analytics Internship Project – IPL 2026 Data Wrangling
