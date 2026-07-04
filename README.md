# Random Forest Model

## Overview

Random Forest is a supervised machine learning algorithm widely used for classification and prediction tasks. In the **Credit Card Approval Prediction** project, the Random Forest model is trained to predict whether a credit card application should be **Approved** or **Not Approved** based on applicant information and credit history.

A function named `random_forest()` is implemented to train, test, and evaluate the model using the training and testing datasets (`X_train`, `X_test`, `y_train`, and `y_test`).

The `RandomForestClassifier()` class from the **Scikit-learn** library is used to build the model. Random Forest creates multiple decision trees during training and combines their predictions through majority voting, resulting in improved accuracy and reduced overfitting.

---

## Import Required Libraries

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import confusion_matrix, classification_report
```

---

## Initialize the Random Forest Model

```python
model = RandomForestClassifier(random_state=42)
```

**Purpose:**
- Creates an instance of the Random Forest classifier.
- Initializes the model with a fixed random state for reproducible results.

---

## Train the Model

```python
model.fit(X_train, y_train)
```

**Purpose:**
- Trains the model using the training dataset.
- Learns patterns and relationships between input features and the target variable.

---

## Generate Predictions

```python
y_pred = model.predict(X_test)
```

**Purpose:**
- Predicts the approval status of unseen test data.
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
- **Recall:** Measures the percentage of actual positive cases correctly identified.
- **F1-Score:** Harmonic mean of precision and recall.
- **Support:** Number of actual samples in each class.

---

## Advantages of Random Forest

- High prediction accuracy.
- Reduces overfitting by combining multiple decision trees.
- Handles large datasets efficiently.
- Works well with both numerical and categorical features.
- Robust against noise and missing values.
- Suitable for binary classification problems.

---

## Summary

The **Random Forest** model is trained using the prepared dataset and evaluated on unseen test data. Predictions are assessed using a **Confusion Matrix** and **Classification Report**, providing key performance metrics such as **Precision**, **Recall**, **F1-Score**, and **Support**. Due to its high accuracy, robustness, and ability to reduce overfitting, Random Forest is one of the most effective algorithms for the Credit Card Approval Prediction project.
