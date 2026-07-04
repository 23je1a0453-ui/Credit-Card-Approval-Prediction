# Dataset Download and Understanding

## Overview

The dataset used for the **Credit Card Approval Prediction** project can be collected from open-source repositories such as **Kaggle**, **data.gov**, or the **UCI Machine Learning Repository**. For this project, the dataset is sourced from **Kaggle**.

---

## Dataset Source

**Dataset Name:** Credit Card Fraud Detection

**Dataset Link:** https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

---

## Dataset Description

The dataset contains information related to credit card transactions and is used to develop a machine learning model for predicting fraudulent transactions. It includes both legitimate and fraudulent transaction records, making it suitable for binary classification tasks.

The dataset consists of multiple features representing transaction details, along with a target variable indicating whether a transaction is fraudulent.

---

## Steps

### Step 1: Download the Dataset

Download the dataset from the Kaggle link provided above and extract the files into the project's `dataset/` directory.

### Step 2: Load the Dataset

Load the CSV file into a Pandas DataFrame for further analysis.

```python
import pandas as pd

data = pd.read_csv("dataset/creditcard.csv")
```

### Step 3: Explore the Dataset

Inspect the dataset to understand its structure, features, and target variable.

```python
data.head()
```

```python
data.info()
```

```python
data.describe()
```

---

## Dataset Features

The dataset contains transaction-related features such as:

- Time
- V1 to V28 (PCA-transformed features)
- Amount
- Class (Target Variable)

Where:

- **Class = 0** → Legitimate Transaction
- **Class = 1** → Fraudulent Transaction

---

## Summary

The dataset serves as the foundation for building the Credit Card Approval Prediction model. It is loaded into a Pandas DataFrame, explored to understand its structure, and prepared for preprocessing, feature engineering, model training, and evaluation.
