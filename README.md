# Fraud Detection with Temporal Modeling

This repository explores various fraud detection techniques across different datasets and model configurations. The focus is on binary classification (Fraud = 1, Non-Fraud = 0), where experiments were conducted to understand how different sampling strategies, feature engineering, and temporal evaluation methods impact model performance.


## Project Structure

The project is divided across multiple Jupyter notebooks, each targeting different datasets and setups:

- **2013 Dataset**
- **2022 Dataset**
- **2023 Dataset**

These datasets vary in class imbalance, volume, and complexity. Some notebooks focus on **significantly imbalanced datasets**, while others explore **balanced subsets** for comparison.

---

## Techniques Used

### Models Explored
- **XGBoost (XGBClassifier)**
- **LightGBM (LGBMClassifier)**
- **Logistic Regression**

Each model was evaluated under multiple experimental configurations to compare performance and robustness.

---

### Oversampling Techniques

To address class imbalance, we experimented with several oversampling methods:

- **SMOTE**
- **ADASYN** (SELECTED)
- **SVMSMOTE**

---

### Train/Test Splitting Strategies

Care was taken to avoid data leakage and to reflect real-world prediction scenarios.

- **Temporal Split** – Based on transaction time (e.g., oldest 80% for training, newest 20% for testing).
- **Temporal K-Fold** – A custom method that preserves chronological integrity while cross-validating over multiple folds.

---

### Lag Features

Lag features were engineered using:

- **Autocorrelation Function (ACF)**
- **Partial Autocorrelation Function (PACF)**

These features help models "remember" past transaction patterns, injecting temporal dependencies directly into the input features.

---

## Evaluation

Final model performance was measured using:

- **Precision**
- **Recall**
- **F1-score**
- **Accuracy**

The effect of oversampling, feature engineering, and temporal validation was evaluated across models and datasets.

---

##  Notes

- Each notebook contains a standalone experiment, including preprocessing, model training, and evaluation.
- The project emphasizes **temporal integrity**, avoiding unrealistic model performance from data leakage.
- Results may vary depending on the specific dataset and technique used.

---
