# Univariate Analysis

## Overview

Univariate Analysis is performed to study a single feature or variable independently. In the Credit Card Approval Prediction project, it helps understand the distribution, frequency, and patterns of applicant-related attributes such as occupation type, income category, education level, and family status.

## Frequency Distribution

```python
app['OCCUPATION_TYPE'].value_counts()
```

## Count Plot

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(12,6))
sns.countplot(x='OCCUPATION_TYPE', data=app)
plt.xticks(rotation=90)
plt.title("Distribution of Occupation Type")
plt.show()
```

## Histogram

```python
sns.histplot(app['AMT_INCOME_TOTAL'], bins=30, kde=True)
plt.show()
```
