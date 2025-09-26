
---

# 🎓 Student Exam Score Prediction – TASK 01

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data--Analysis-green.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-red.svg)](https://seaborn.pydata.org/)
[![Dataset](https://img.shields.io/badge/Dataset-Kaggle-brightgreen.svg)](https://www.kaggle.com/)

---

## 📌 Project Overview

This project applies **Machine Learning** techniques to predict **student exam scores** based on academic, socio-economic, and behavioral factors.

The workflow includes:

✔️ Data Preprocessing (handling missing values, encoding, scaling)

✔️ Exploratory Data Analysis (EDA)

✔️ Model Training (Linear Regression, Polynomial Regression)

✔️ Model Evaluation & Comparison

---

## ⚙️ Installation

Make sure you have Python 3.x installed. Then, install the required dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 📂 Dataset

* **Source**: [Kaggle – Student Performance Factors](https://www.kaggle.com/)
* **Total Records**: 6,607
* **Features**: 20

  * Numerical: `StudyHours`, `SleepHours`, `Attendance`, `FamilyIncome`
  * Categorical: `Parental_Involvement`, `School_Type`, `Extracurricular_Activities`, `Preparation`
* **Target Variable**:

  * `Exam_Score` (continuous numeric: 0–100)

---

## 🔧 Data Preprocessing

1. **Missing Values**

   * Filled using **mean** for numerical features, **mode** for categorical.

2. **Encoding**

   * Binary categorical features → **Label Encoding**
   * Multi-class categorical features → **One-Hot Encoding**

3. **Scaling**

   * StandardScaler applied to numerical features.

---

## 📊 Exploratory Data Analysis (EDA)

* **Histograms**: distribution of numerical features
* **Scatterplot**: Study Hours vs Exam Score
* **Boxplot**: Parental Involvement vs Exam Score
* **Correlation Heatmap**: feature relationships with Exam Score

📌 **Key Insights**:

* Strong positive correlation: Study Hours, Parental Involvement
* Negative correlation: Absenteeism, Low Resource Access

---

## 🤖 Model Training

### Data Splitting

* Train-test split: **80% training, 20% testing**

### Models Used

1. **Linear Regression** – baseline model
2. **Polynomial Regression (Degree 2)** – captures non-linear relationships

---

## 📈 Model Evaluation

### Metrics Used

* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

### Results

| Model                 | RMSE | R² Score |
| --------------------- | ---- | -------- |
| Linear Regression     | 2.05 | 0.74     |
| Polynomial Regression | 1.89 | 0.75     |

---

## ✅ Conclusion

* **Polynomial Regression** slightly outperformed Linear Regression.
* Key predictors: **Study Hours, Parental Involvement, Preparation, Family Income**.
* Future improvements:

  * Try advanced models (Random Forest, XGBoost)
  * Perform hyperparameter tuning
  * Add feature selection

👉 **Final Choice: Polynomial Regression (Degree 2)** for predicting exam scores.

---

## 📚 References

* [Kaggle – Student Performance Dataset](https://www.kaggle.com/)
* [Scikit-learn Documentation](https://scikit-learn.org/)

---

