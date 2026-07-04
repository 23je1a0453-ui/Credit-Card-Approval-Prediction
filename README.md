# Decision Tree Model

## Overview

Decision Tree is a supervised machine learning algorithm used for classification and prediction tasks. In the **Credit Card Approval Prediction** project, the Decision Tree model is trained to predict whether a credit card application should be **Approved** or **Not Approved** based on applicant information and credit history.

A function named `d_tree()` is implemented to train, test, and evaluate the model using the training and testing datasets (`X_train`, `X_test`, `y_train`, and `y_test`).

The `DecisionTreeClassifier()` class from the **Scikit-learn** library is used to build the model. The algorithm creates a tree-like structure where each internal node represents a decision based on a feature, each branch represents the outcome of that decision, and each leaf node represents the final prediction.

---

## Import Required Libraries

```python
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import confusion_matrix, classification_report
```

---

## Initialize the Decision Tree Model

```python
model = DecisionTreeClassifier(random_state=42)
```

**Purpose:**
- Creates an instance of the Decision Tree classifier.
- Ensures reproducible results by setting a random state.

---

## Train the Model

```python
model.fit(X_train, y_train)
```

**Purpose:**
- Trains the Decision Tree model using the training dataset.
- Learns decision rules from the input features and target variable.

---

## Generate Predictions

```python
y_pred = model.predict(X_test)
```

**Purpose:**
- Predicts the approval status for unseen test data.
- Produces classification results for evaluation.

---

## Evaluate the Model

### Confusion Matrix

```python
cm = confusion_matrix(y_test, y_pred)
print(cm)
```

### Classification Report

```python
report = classification_report(y_test, y_pred)
print(report)
```

**Evaluation Metrics:**

- **Precision:** Measures the accuracy of positive predictions.
- **Recall:** Measures how many actual positive cases are correctly identified.
- **F1-Score:** Harmonic mean of precision and recall.
- **Support:** Number of actual samples in each class.

---

## Advantages of Decision Tree

- Simple and easy to understand.
- Produces interpretable decision rules.
- Handles both numerical and categorical features.
- Requires minimal data preprocessing.
- Supports non-linear relationships between features.
- Suitable for binary classification problems.

---

## Summary

The **Decision Tree** model is trained using the prepared dataset and evaluated on unseen test data. Predictions are assessed using a **Confusion Matrix** and **Classification Report**, providing key performance metrics such as **Precision**, **Recall**, **F1-Score**, and **Support**. Its interpretability, simplicity, and effectiveness make Decision Tree a valuable algorithm for the Credit Card Approval Prediction project.
