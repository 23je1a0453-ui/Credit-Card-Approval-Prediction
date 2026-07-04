# Importing Required Libraries

## Overview

Importing the required Python libraries is the first step in developing the **Credit Card Approval Prediction** project. These libraries provide built-in functions for data loading, preprocessing, visualization, machine learning model development, and performance evaluation. Using these libraries ensures an efficient and organized workflow throughout the project.

---

## Import Required Libraries

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder, StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
```

---

## Library Description

### NumPy
Provides support for numerical computing, multidimensional arrays, and mathematical operations.

### Pandas
Used to load, clean, preprocess, and analyze datasets using DataFrames.

### Matplotlib
Creates charts, graphs, and visualizations for data analysis.

### Seaborn
Provides high-level statistical visualizations such as heatmaps, count plots, and pair plots.

### Scikit-learn
Offers machine learning algorithms and tools for:

- Data preprocessing
- Feature scaling
- Label encoding
- Train-test splitting
- Model training
- Model evaluation

---

## Purpose

The imported libraries are used to:

- Load and analyze the dataset.
- Clean and preprocess the data.
- Visualize feature distributions and relationships.
- Train multiple machine learning models.
- Evaluate model performance using classification metrics.
- Compare models and select the best-performing one for deployment.

---

## Summary

Importing the required libraries establishes the foundation for the Credit Card Approval Prediction project. These libraries support every stage of the machine learning pipeline, from data preprocessing and visualization to model training, evaluation, and deployment.
