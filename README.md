## Label Conversion and Dataset Merging

### Overview

The **STATUS** column in the credit records dataset initially contains multiple payment categories, including **paid on time, overdue payments, bad debt, and no loan records**. Since the objective of this project is to predict whether a credit card application should be **approved** or **not approved**, these multiple categories are converted into **binary class labels**.

This binary classification simplifies the prediction process, reduces model complexity, and improves the overall performance of the machine learning model.

---

## Convert STATUS to Binary Labels

Applicants with a good repayment history are classified as **Approved (1)**, while applicants with overdue payments, bad debt, or poor credit history are classified as **Not Approved (0)**.

Example:

```python
credit["STATUS"] = credit["STATUS"].replace({
    "C": 1,   # Paid on time
    "X": 1,   # No loan record
    "0": 1,   # Current payment
    "1": 0,   # 30 days overdue
    "2": 0,   # 60 days overdue
    "3": 0,   # 90 days overdue
    "4": 0,   # 120 days overdue
    "5": 0    # Bad debt / More than 120 days overdue
})
```

**Purpose:**
- Converts multiple payment categories into binary labels.
- Simplifies the classification problem.
- Improves model training and prediction accuracy.

---

## Merge Applicant and Credit Datasets

After cleaning and transforming both datasets, they are merged using the common **Applicant ID (ID)** column.

```python
final_data = pd.merge(app, credit, on="ID", how="inner")
```

**Purpose:**
- Combines applicant demographic information with credit history.
- Creates a single dataset for machine learning.
- Ensures all required features are available for prediction.

---

## Verify the Merged Dataset

```python
final_data.head()
```

```python
final_data.shape
```

**Purpose:**
- Displays the first few records of the merged dataset.
- Confirms the number of rows and columns after merging.

---

## Benefits

- Converts complex payment categories into a binary classification problem.
- Simplifies machine learning model development.
- Combines applicant and credit history information into one dataset.
- Improves data consistency and prediction accuracy.
- Produces a clean and structured dataset ready for feature selection, model training, and evaluation.

---

## Summary

The **STATUS** column is transformed from multiple payment categories into binary approval labels, making the prediction task more efficient. The cleaned applicant dataset and credit records dataset are then merged using the **ID** column to create a unified dataset that serves as the foundation for training and evaluating the Credit Card Approval Prediction model.
