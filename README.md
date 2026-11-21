## Dataset

This project uses the Concrete Compressive Strength
dataset from the UCI Machine Learning Repository.

- Author: I-Cheng Yeh
- Instances: 1,030
- Input features: 8
- Target: Concrete compressive strength (MPa)
- License: CC BY 4.0

### Citation

Yeh, I. (1998). Concrete Compressive Strength
[Dataset]. UCI Machine Learning Repository.
https://doi.org/10.24432/C5PK67

## Data Quality & Preprocessing

The dataset was examined for missing values, duplicate records, invalid measurements, and potential outliers.

### Key Findings

| Quality Check | Result |
|---|---|
| Total observations | 1,030 |
| Missing values | 0 |
| Exact duplicate rows | 25 |
| Negative values | 0 |
| Invalid age values | 0 |
| Invalid strength values | 0 |
| Cement outliers | 0 |
| Water outliers | 9 |
| Age outliers | 59 |
| Strength outliers | 4 |

*Potential outliers were identified using the 1.5 × IQR method for Cement, Water, Age, and Strength.*

### Preprocessing Decisions

- Standardized column names for easier analysis.
- Verified numerical data types and basic measurement validity.
- Retained all 1,030 observations.
- Preserved potential outliers because unusual values are not necessarily errors.
- Retained exact duplicates for further investigation before model training.
- Preserved the original dataset without modification.

### Processed Dataset

The prepared dataset is available at:

`data/processed/concrete_clean.csv`

**Final shape:** 1,030 rows × 9 columns.

### Detailed Analysis

The complete data quality investigation, Python code, and results are available in:

[Task 02 — Data Quality Checking](notebooks/02_data_quality.ipynb)
