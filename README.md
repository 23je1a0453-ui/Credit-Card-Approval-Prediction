# Label Encoding

## Overview

Machine learning algorithms require numerical input data for training and prediction. Since the dataset contains categorical features such as gender, education level, income type, housing type, and family status, these values must be converted into numerical form.

In this project, the **LabelEncoder** class from the **Scikit-learn** preprocessing module is used to transform categorical variables into integer labels. The `fit_transform()` method identifies each unique category and assigns it a unique numerical value, making the dataset suitable for machine learning models.

---

## Import LabelEncoder

```python
from sklearn.preprocessing import LabelEncoder
```

---

## Create a LabelEncoder Object

```python
label_encoder = LabelEncoder()
```

**Purpose:**
- Creates an instance of the `LabelEncoder` class.
- Prepares the encoder to transform categorical features.

---

## Apply Label Encoding

Convert categorical columns into numerical values.

```python
data["CODE_GENDER"] = label_encoder.fit_transform(data["CODE_GENDER"])
data["NAME_INCOME_TYPE"] = label_encoder.fit_transform(data["NAME_INCOME_TYPE"])
data["NAME_EDUCATION_TYPE"] = label_encoder.fit_transform(data["NAME_EDUCATION_TYPE"])
data["NAME_FAMILY_STATUS"] = label_encoder.fit_transform(data["NAME_FAMILY_STATUS"])
data["NAME_HOUSING_TYPE"] = label_encoder.fit_transform(data["NAME_HOUSING_TYPE"])
```

**Purpose:**
- Converts text categories into numerical labels.
- Prepares the dataset for machine learning algorithms.
- Maintains consistency across categorical features.

---

## How Label Encoding Works

Example:

| Original Value | Encoded Value |
|---------------|--------------:|
| Male | 1 |
| Female | 0 |

| Income Type | Encoded Value |
|-------------|--------------:|
| Working | 3 |
| Commercial Associate | 0 |
| Pensioner | 2 |
| State Servant | 1 |

> **Note:** The assigned numbers are only identifiers. They do **not** indicate ranking or importance.

---

## Benefits of Label Encoding

- Converts categorical data into numerical format.
- Makes the dataset compatible with machine learning algorithms.
- Simplifies preprocessing.
- Preserves unique category information.
- Works effectively with tree-based models such as Decision Tree, Random Forest, and XGBoost.

---

## Summary

Label Encoding is an important preprocessing technique used to convert categorical features into numerical values. Using Scikit-learn's `LabelEncoder` and the `fit_transform()` method ensures that the dataset is properly formatted for machine learning, enabling efficient training and accurate prediction in the Credit Card Approval Prediction project.
