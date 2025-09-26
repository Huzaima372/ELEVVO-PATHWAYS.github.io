# 🎓 Student Exam Score Prediction  

<p align="center">
  <img src="https://img.freepik.com/free-vector/online-exams-concept-illustration_114360-5572.jpg" width="500" alt="exam illustration"/>
</p>

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)  
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellowgreen)  
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)  
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-blueviolet)  
![Colab](https://img.shields.io/badge/Colab-Notebook-gold)  
![Status](https://img.shields.io/badge/Status-Completed-success.svg)  

---

## 📑 Table of Contents
1. [Overview](#-overview)  
2. [Dataset](#-dataset)  
3. [Methodology](#-methodology)  
4. [Models](#-models)  
5. [Results](#-results)  
6. [How to Run](#-how-to-run)  
7. [Future Work](#-future-work)  
8. [License](#-license)  

---

## 📖 Overview  

This project explores **factors influencing student performance** and predicts exam scores using **machine learning regression techniques**.  

✨ **Key Highlights**  
- Data Cleaning & Preprocessing 🧹  
- Exploratory Data Analysis (EDA) 📊  
- Regression Models (Linear & Polynomial) 🤖  
- Model Evaluation (RMSE, R²) 📏  
- Feature Importance / Ablation Study 🔬  

---

## 📂 Dataset  

- **Source:** [Kaggle – Student Performance Factors](https://www.kaggle.com/)  
- **Records:** 6,607 students  
- **Features:** Study Hours, Attendance, Parental Involvement, Resources, Peer Influence, Family Income, Motivation, etc.  
- **Target Variable:** `Exam_Score`  

<p align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/3135/3135755.png" width="200" alt="dataset icon"/>
</p>

---

## ⚙️ Methodology  

### 🔹 Data Preprocessing  
✔️ Missing values imputed (mean/mode)  
✔️ Categorical features → Label/One-Hot Encoding  
✔️ Numerical features → Standard Scaling  

### 🔹 Exploratory Data Analysis  
- Histograms of numeric features  
- Scatter plots *(Study Hours vs Exam Score)*  
- Boxplots *(Parental Involvement vs Exam Score)*  
- Heatmaps *(feature correlation)*  

<p align="center">
  <img src="https://seaborn.pydata.org/_images/seaborn-heatmap-1.png" width="500" alt="heatmap"/>
</p>

---

## 🤖 Models  

1. **Linear Regression** – Baseline, interpretable  
2. **Polynomial Regression (degree=2)** – Tested non-linear patterns  

### 📏 Evaluation Metrics  
- MSE (Mean Squared Error)  
- RMSE (Root Mean Squared Error)  
- R² Score  

---

## 📊 Results  

| Model                 | RMSE  | R² Score | Notes |
|------------------------|-------|----------|-------|
| Linear Regression      | ~1.80 | 0.77     | ✅ Best performer |
| Polynomial Regression  | ~1.89 | 0.74     | ❌ Slightly worse |

📌 **Key Findings**  
- Participation in extracurriculars strongly influences scores.  
- Sleep hours contributed little to predictive power.  
- Linear regression explained **~77% of variance** in scores.  

<p align="center">
  <img src="https://raw.githubusercontent.com/mwaskom/seaborn-data/master/docs/_static/scatterplot.png" width="450" alt="scatter plot"/>
</p>

---

## 🚀 How to Run  

### 1️⃣ Install Dependencies  
```bash
pip install numpy pandas matplotlib seaborn scikit-learn

````

### 2️⃣ Run Notebook

* Open in **Colab / Jupyter Notebook**
* Load `StudentPerformanceFactors.csv` into the correct path
* Run all cells ✅

<p align="center">
  <img src="https://colab.research.google.com/img/colab_favicon_256px.png" width="80" alt="colab"/>
</p>

---

## 🔮 Future Work

🔹 Try advanced ML models:

* Random Forests 🌳
* Gradient Boosting ⚡
* Neural Networks 🧠

🔹 Hyperparameter tuning for better accuracy
🔹 Subgroup analysis (socio-economic, school types)

---

## 📜 License

For **educational and research purposes** only.
Dataset available on [Kaggle](https://www.kaggle.com/).

---

<p align="center">  
  Made with ❤️, ☕, and 📊 by a Data Science Enthusiast  
</p>
```

---
