# Removing Duplicate Records

## Overview

Removing duplicate records is an essential data preprocessing step in the **Credit Card Approval Prediction** project. Duplicate entries may occur due to repeated data collection, data merging, or system errors. These duplicate records can negatively impact the accuracy and reliability of the machine learning model.

Each applicant should have a unique **Applicant ID**. Therefore, duplicate records are identified and removed to ensure data consistency and improve model performance.

---

## Check for Duplicate Records

Before removing duplicates, check how many duplicate rows exist in the dataset.

```python
data.duplicated().sum()
```

**Purpose:**
- Counts the total number of duplicate records.
- Helps determine whether data cleaning is required.

---

## Remove Duplicate Records

Remove all duplicate rows from the dataset.

```python
data = data.drop_duplicates()
```

**Purpose:**
- Removes duplicate records.
- Keeps only unique rows in the dataset.
- Improves data quality.

---

## Remove Duplicates Based on Applicant ID

If the dataset contains an **Applicant_ID** column, remove duplicates while keeping the first occurrence.

```python
data = data.drop_duplicates(subset="Applicant_ID", keep="first")
```

**Purpose:**
- Removes duplicate applicant records.
- Retains only the first occurrence of each Applicant ID.
- Ensures every applicant appears only once in the dataset.

---

## Verify the Updated Dataset

Check the dataset shape after removing duplicates.

```python
data.shape
```

**Purpose:**
- Displays the number of rows and columns after cleaning.
- Confirms that duplicate records have been removed successfully.

---

## Benefits of Removing Duplicate Records

- Improves data quality and consistency.
- Prevents bias during model training.
- Ensures each applicant has a unique record.
- Reduces redundant data.
- Enhances machine learning model accuracy.
- Produces more reliable prediction results.

---

## Summary

Removing duplicate records is a crucial preprocessing step in the Credit Card Approval Prediction project. Using the `drop_duplicates()` function ensures that each applicant is represented only once in the dataset, resulting in cleaner, more reliable data for preprocessing, feature engineering, model training, and evaluation.
