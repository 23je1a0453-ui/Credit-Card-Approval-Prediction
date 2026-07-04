# Descriptive Analysis

## Overview

Descriptive Analysis is performed to summarize and understand the statistical characteristics of the dataset. In the **Credit Card Approval Prediction** project, this analysis provides insights into numerical features such as applicant income, employment duration, family size, and age. It helps identify the distribution, central tendency, variability, and range of the data before preprocessing and model training.

---

## Generate Descriptive Statistics

Use the `describe()` function to generate summary statistics for all numerical features.

```python
data.describe()
```

**Purpose:**
- Displays the count of non-null values.
- Calculates the mean and standard deviation.
- Shows the minimum and maximum values.
- Displays percentile values (25%, 50%, and 75%).
- Provides a statistical summary of the dataset.

---

## Example Output

| Statistic | Description |
|-----------|-------------|
| Count | Number of non-null values |
| Mean | Average value of the feature |
| Std | Standard deviation (data spread) |
| Min | Minimum value |
| 25% | First quartile |
| 50% | Median value |
| 75% | Third quartile |
| Max | Maximum value |

---

## Benefits of Descriptive Analysis

- Provides a statistical overview of the dataset.
- Helps understand the distribution of numerical features.
- Identifies potential outliers and anomalies.
- Detects inconsistencies in the data.
- Supports feature selection and preprocessing.
- Improves the quality of data before machine learning model training.

---

## Summary

Descriptive Analysis is an essential step in Exploratory Data Analysis (EDA). Using the `describe()` function in Pandas provides a comprehensive statistical summary of numerical features, helping developers understand the dataset, identify irregularities, and prepare high-quality data for building an accurate Credit Card Approval Prediction model.
