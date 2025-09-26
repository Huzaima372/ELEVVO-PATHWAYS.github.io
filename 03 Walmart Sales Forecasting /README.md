
---

# 🛒 Walmart Sales Forecasting – TASK 07

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data--Analysis-green.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-red.svg)](https://seaborn.pydata.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-Gradient--Boosting-blueviolet.svg)](https://xgboost.readthedocs.io/)
[![Dataset](https://img.shields.io/badge/Dataset-Kaggle-brightgreen.svg)](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast)

---

## 📌 Project Overview

This project applies **Machine Learning and Time Series Analysis** to predict **weekly Walmart sales**.

The workflow includes:
✔️ Data Cleaning & Preprocessing (handling missing values, encoding, feature engineering)
✔️ Exploratory Data Analysis (EDA)
✔️ Baseline Model (Linear Regression)
✔️ Advanced Model (XGBoost Regressor)
✔️ Model Evaluation & Comparison

---

## ⚙️ Installation

Make sure you have Python 3.x installed. Then, install the required dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost kagglehub
```

---

## 📂 Dataset

* **Source**: [Kaggle – Walmart Sales Forecasting](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast)
* **Files Used**:

  * `features.csv` → additional features (holidays, fuel price, etc.)
  * `train.csv` → weekly sales data
  * `stores.csv` → store metadata
* **Target Variable**:

  * `Weekly_Sales` (numeric, continuous)

---

## 🔧 Data Preprocessing

1. **Data Merging**

   * Combined `features.csv`, `train.csv`, and `stores.csv`.

2. **Cleaning**

   * Dropped Markdown columns (`MarkDown1`–`MarkDown5`).
   * Removed records with zero or negative sales.

3. **Feature Engineering**

   * Extracted `year`, `month`, and `day` from `Date`.
   * Encoded categorical features (`IsHoliday`, `Type`) using **Label Encoding**.

---

## 📊 Exploratory Data Analysis (EDA)

* Visualized sales distribution over time.
* Correlation heatmap between features.
* Actual vs Predicted Sales plots for model performance comparison.

📌 **Key Insight**: Sales patterns are **seasonal** (holidays, promotions) and strongly depend on **store type** and **location features**.

---

## 🤖 Model Training

### Baseline Model – Linear Regression

* Train-Test Split: **80% training, 20% testing**.
* Performance was weak due to inability to capture non-linear/seasonal patterns.

### Advanced Model – XGBoost Regressor

* Train-Test Split: **time-aware split** (pre-2012 → train, 2012+ → test).
* Tuned hyperparameters: `n_estimators=500`, `max_depth=8`, `learning_rate=0.05`.

---

## 📈 Model Evaluation

### Metrics Used

* Mean Squared Error (MSE)
* Mean Absolute Error (MAE)
* R² Score

### Results

| Model             | MSE         | MAE    | R² Score             |
| ----------------- | ----------- | ------ | -------------------- |
| Linear Regression | 464,612,749 | 14,523 | 0.09 (poor fit)      |
| XGBoost Regressor | 22,122,995  | 2,703  | 0.95 (excellent fit) |

---

## ✅ Conclusion

* **Linear Regression** failed to capture the complex, seasonal trends in Walmart sales.
* **XGBoost Regressor** achieved **R² ≈ 0.95**, demonstrating excellent predictive power.
* Further improvements could include:

  * Lag features and rolling averages
  * Time-series decomposition
  * Hyperparameter tuning and cross-validation

👉 **Final Choice: XGBoost Regressor** for Walmart Sales Forecasting.

---

## 📚 References

* [Kaggle – Walmart Sales Forecasting Dataset](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast)
* [Scikit-learn Documentation](https://scikit-learn.org/)
* [XGBoost Documentation](https://xgboost.readthedocs.io/)

---
