
# README

## Dataset Description
- **Dataset**: Cleveland Heart Disease Dataset.
- **Columns**: 
  - Features: `"age"`, `"sex"`, `"cp"`, `"trestbps"`, `"chol"`, `"fbs"`, `"restecg"`, `"thalach"`, `"exang"`, `"oldpeak"`, `"slope"`, `"ca"`, `"thal"`.
  - **Target Variable**: `"num"` (binary classification):
    - `0`: No heart disease.
    - `1`: Some level of heart disease.

---

## Data Preprocessing
1. **Data Type Conversion**: Converted string columns to numeric.
2. **Handling Missing Values**:
   - Replaced any `?` values with `NaN`.
   - Removed rows with `NaN` values.
   
---

## Dataset Preparation
- Performed a **3-way holdout split**:
  - **Training Set**
  - **Validation Set**
  - **Test Set**
- **Test Set Size**: 20% of the dataset.

---

## Feature Selection
- A **correlation matrix** was used to analyze feature relationships and justify feature selection.

---

## Validation Set Results: Algorithm Comparison
| Algorithm                  | Hyperparameter Tuning           | Validation Accuracy |
|----------------------------|----------------------------------|---------------------|
| **XGBoost**                | `RandomizedSearchCV`            | **81%**            |
| **Logistic Regression**    | `RandomizedSearchCV`            | **81%**            |
| **Random Forest**          | `RandomizedSearchCV`            | **83%**            |
| **Artificial Neural Network (ANN)** | Custom tuning       | **83%**            |

---

## Test Set Performance
- **Best Algorithm**: **XGBoost** with the highest accuracy.
- **Test Accuracy**: **88.3%**

---

## Metrics for XGBoost
- **Confusion Matrix**:
  - **True Predictions**: 53
  - **False Predictions**: 7
  - **F1 Score**: 0.8834
  - **Precision Score**: 0.8879


---

## Model Explainability with LIME
- **LIME (Local Interpretable Model-Agnostic Explanations)** was used to explain the decision-making process of the XGBoost model.
- Example: Explanation of the model's decision for the first data point in the test set.

---

## Summary
- The XGBoost model outperformed other algorithms with a test accuracy of **88.3%**.
- Using LIME, we gained insights into the model's predictions, enhancing interpretability and trust in its decisions.

---
