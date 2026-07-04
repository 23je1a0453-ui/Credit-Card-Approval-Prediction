# Multivariate Analysis

## Overview

Multivariate Analysis is performed to study the relationship between multiple features in the dataset simultaneously. In the **Credit Card Approval Prediction** project, it helps identify how applicant attributes such as income, employment duration, family size, age, and other financial factors are related to each other and how they influence the credit card approval decision.

This analysis is useful for identifying feature dependencies, detecting multicollinearity, and selecting the most relevant features for model training.

---

## Calculate Correlation Matrix

Use the `corr()` function to calculate the correlation between numerical features.

```python
correlation_matrix = app.corr(numeric_only=True)

print(correlation_matrix)
```

**Purpose:**
- Calculates the correlation coefficient between numerical variables.
- Identifies positive and negative relationships.
- Helps select important features for model development.

---

## Correlation Heatmap

Visualize the correlation matrix using a heatmap.

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(12, 8))

sns.heatmap(
    correlation_matrix,
    annot=True,
    cmap="coolwarm",
    fmt=".2f"
)

plt.title("Correlation Heatmap")
plt.show()
```

**Purpose:**
- Displays the correlation between features.
- Positive correlations appear in warmer colors.
- Negative correlations appear in cooler colors.
- Helps identify highly correlated variables.

---

## Benefits of Multivariate Analysis

- Identifies relationships between multiple features.
- Detects feature dependencies and multicollinearity.
- Supports feature selection.
- Improves preprocessing and model optimization.
- Enhances machine learning model performance.

---

## Summary

Multivariate analysis is an important Exploratory Data Analysis (EDA) technique used to understand relationships among multiple variables. By using correlation analysis and heatmaps, it becomes easier to identify significant features, reduce redundancy, and improve the accuracy and efficiency of the Credit Card Approval Prediction model.
