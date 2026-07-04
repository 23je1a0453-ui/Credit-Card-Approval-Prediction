# Reading the Dataset

## Overview

Reading the dataset is one of the first steps in the **Credit Card Approval Prediction** project. It helps understand the structure, features, and records available for machine learning. The dataset is loaded using the **Pandas** library with the `read_csv()` function, which reads CSV files and stores the data in a **DataFrame** for further analysis and preprocessing.

After loading the dataset, functions such as `head()`, `shape`, and `info()` are used to inspect the data, verify its structure, identify missing values, and understand the data types of each feature.

---

## Import Pandas

```python
import pandas as pd
```

---

## Read the Dataset

Use the `read_csv()` function to load the CSV file.

```python
data = pd.read_csv("dataset/creditcard.csv")
```

**Purpose:**
- Reads the dataset from the specified file path.
- Loads the data into a Pandas DataFrame.
- Prepares the dataset for analysis and preprocessing.

---

## Display the First Five Rows

Use the `head()` method to view a sample of the dataset.

```python
data.head()
```

**Purpose:**
- Displays the first **five rows** of the dataset by default.
- Provides a quick overview of the available features and sample records.

---

## Check Dataset Dimensions

```python
data.shape
```

**Purpose:**
- Returns the number of rows and columns in the dataset.
- Helps understand the dataset size.

---

## Display Dataset Information

```python
data.info()
```

**Purpose:**
- Displays column names.
- Shows data types of each feature.
- Identifies missing (null) values.
- Provides memory usage information.

---

## Generate Statistical Summary

```python
data.describe()
```

**Purpose:**
- Generates descriptive statistics for numerical features.
- Displays count, mean, standard deviation, minimum, maximum, and percentile values.

---

## Summary

Reading the dataset is a crucial step in the machine learning workflow. Using `pd.read_csv()`, the dataset is loaded into a Pandas DataFrame for analysis. Functions such as `head()`, `shape`, `info()`, and `describe()` provide valuable insights into the dataset, helping prepare it for preprocessing, visualization, model training, and evaluation.
