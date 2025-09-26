
---

# 🎬 Movie Recommendation System – TASK 05

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data--Analysis-green.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-red.svg)](https://seaborn.pydata.org/)
[![Dataset](https://img.shields.io/badge/Dataset-MovieLens%20\(Kaggle\)-brightgreen.svg)](https://www.kaggle.com/datasets/mukeshmanral/movielens-rating-dataset)

---

## 📌 Project Overview

This project builds a **Movie Recommendation System** using the **MovieLens dataset**. It applies **Collaborative Filtering** approaches to suggest movies to users:

✔️ **User-Based Collaborative Filtering** – recommends movies based on ratings from similar users.
✔️ **Item-Based Collaborative Filtering** – recommends movies based on similarity between movies a user has already rated.
✔️ **Evaluation** – recommendations are validated using **Precision@K**.
✔️ **Visualization** – distribution of ratings & most popular movies.

---

## ⚙️ Installation

Make sure you have Python 3.x installed. Then, install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn kagglehub
```

---

## 📂 Dataset

* **Source**: [MovieLens Ratings Dataset (Kaggle)](https://www.kaggle.com/datasets/mukeshmanral/movielens-rating-dataset)
* **Files Used**:

  * `movie_info.csv` → Movie titles, genres, and IDs
  * `ratings.csv` → User ratings for movies
  * `user_demographics.csv` → Age, gender, and user attributes

---

## 🔧 Data Preprocessing

1. **Merging**

   * Combined `ratings.csv` with `movie_info.csv` on `movie_id`.

2. **Train-Test Split**

   * Performed **user-level split**: 80% training, 20% testing.
   * Users with <5 ratings kept only in training set.

3. **Matrix Creation**

   * Built **User-Item Matrix** (users × movies).
   * Built **Item-User Matrix** for item similarity.

---

## 📊 Exploratory Data Analysis (EDA)

* **Distribution of Ratings** – showed user rating tendencies.
* **Top 10 Most Rated Movies** – identified the most popular movies.

---

## 🤖 Recommendation Approaches

### 1. User-Based Collaborative Filtering

* **Similarity Metric**: Cosine Similarity between users.
* **Recommendation Process**:

  * Find nearest neighbors.
  * Aggregate neighbor ratings (weighted by similarity).
  * Exclude already watched movies.
* **Evaluation**: Precision@K (e.g., Precision@10).

### 2. Item-Based Collaborative Filtering

* **Similarity Metric**: Cosine Similarity between items.
* **Recommendation Process**:

  * Identify movies the user rated.
  * Recommend similar movies.
  * Weight predictions by user’s ratings.
* **Evaluation**: Precision@K.

---

## 📈 Model Evaluation

### Metric Used

* **Precision@K** – measures relevance of top-K recommended movies.

### Example Results

| Method                             | Precision@10 |
| ---------------------------------- | ------------ |
| User-Based Collaborative Filtering | ~0.32        |
| Item-Based Collaborative Filtering | ~0.35        |

*(values may vary depending on random splits)*

---

## ✅ Conclusion

* Both **User-Based** and **Item-Based** collaborative filtering provide meaningful recommendations.
* **Item-Based** filtering performed slightly better in Precision@10.
* The system can be extended with:

  * Matrix Factorization (SVD, NMF)
  * Deep Learning (Neural Collaborative Filtering)
  * Hybrid Models combining CF + Content-based features

👉 **Final Choice: Item-Based Collaborative Filtering** for better recommendation quality.

---

## 📚 References

* [MovieLens Ratings Dataset – Kaggle](https://www.kaggle.com/datasets/mukeshmanral/movielens-rating-dataset)
* [Scikit-learn Documentation](https://scikit-learn.org/)

---