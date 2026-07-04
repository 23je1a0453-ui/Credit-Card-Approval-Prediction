# Data Cleaning and Feature Transformation

## Overview

Data Cleaning and Feature Transformation are essential preprocessing steps in the **Credit Card Approval Prediction** project. These processes ensure that the dataset is clean, consistent, and suitable for machine learning algorithms. Raw datasets often contain unnecessary columns, missing values, inconsistent information, negative values, and categorical features that must be transformed into numerical representations.

The `data_cleaning()` function is used to perform these preprocessing tasks and prepare the dataset for model training.

---

## Data Cleaning

The following operations are performed during data cleaning:

- Remove unnecessary columns that do not contribute to prediction.
- Eliminate duplicate records.
- Handle missing values.
- Convert negative values into positive values where appropriate.
- Standardize the dataset for further analysis.

---

## Feature Engineering

### Create Family Size Feature

A new feature is created by combining the number of family members and children to better represent the applicant's family dependency.

```python
data["Family_Size"] = data["CNT_FAM_MEMBERS"] + data["CNT_CHILDREN"]
```

**Purpose:**
- Represents the applicant's overall family responsibility.
- Improves feature representation for model training.

---

### Convert Negative Values

The `DAYS_BIRTH` and `DAYS_EMPLOYED` columns contain negative values. These values are converted into positive numbers using the `abs()` function.

```python
data["DAYS_BIRTH"] = data["DAYS_BIRTH"].abs()
data["DAYS_EMPLOYED"] = data["DAYS_EMPLOYED"].abs()
```

**Purpose:**
- Improves readability.
- Makes numerical analysis easier.
- Maintains consistent feature values.

---

### Remove Unnecessary Columns

Columns that are not useful for prediction are removed.

```python
data.drop(columns=["OCCUPATION_TYPE"], inplace=True)
```

**Purpose:**
- Reduces dataset complexity.
- Improves model efficiency.
- Removes irrelevant information.

---

## Feature Transformation

Categorical variables are converted into numerical values using mapping or encoding techniques.

Example:

```python
data["CODE_GENDER"] = data["CODE_GENDER"].map({
    "M": 1,
    "F": 0
})
```

Other categorical features transformed include:

- Housing Type
- Income Type
- Education Type
- Family Status
- Occupation Type (if retained)

---

## Credit Record Processing

The credit record dataset is grouped by the applicant's **ID** to combine multiple monthly records into a single record.

Example:

```python
credit.groupby("ID")
```

Additional features are created from the `MONTHS_BALANCE` column, including:

- **Open Month**
- **End Month**
- **Credit History Window**

The `STATUS` column is analyzed to determine:

- Timely payments
- Overdue payments
- No loan records

These features improve the prediction capability of the machine learning model.

---

## Benefits

- Cleans inconsistent data.
- Removes unnecessary information.
- Creates meaningful features.
- Converts categorical values into numerical format.
- Improves machine learning model performance.
- Enhances prediction accuracy.

---

## Summary

Data Cleaning and Feature Transformation prepare the dataset for machine learning by removing redundant information, handling inconsistencies, engineering new features, and converting categorical variables into numerical values. These preprocessing steps improve data quality and help build a more accurate and reliable Credit Card Approval Prediction model.
