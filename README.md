# 🎬 Movie Recommendation System

A content-based movie recommendation system that suggests similar movies based on genre matching and user ratings — built on 100,000+ real ratings across 9,700+ movies from the MovieLens dataset.

---

## 📌 Project Overview

Ever wondered how Netflix or Spotify knows what you want next? This project builds a recommendation engine from scratch using content-based filtering — analyzing genre patterns, user rating behavior, and multi-criteria scoring to deliver personalized movie suggestions.

---

## 💡 How It Works

1. **Genre Extraction** — Genres parsed and vectorized from the input movie
2. **Similarity Search** — Searches 100+ rating movies for genre matches
3. **Similarity Scoring** — Cosine Similarity ranks movies by genre overlap
4. **Multi-criteria Sorting** — Results ranked by similarity + average rating
5. **Top 10 Output** — Returns the 10 most relevant recommendations

---

## ✨ Features

- 🎯 Content-based filtering through genre analysis
- ⭐ Minimum rating threshold filtering (100+ ratings for quality)
- 📊 Multi-criteria ranking — similarity score + average rating
- 🔀 Genre overlap and average rating combined scoring
- 💾 Model persistence for reusability without retraining

---

## 📊 Dataset

- **Source:** MovieLens (GroupLens Research)
- **Movies:** ~9,700 titles with genres
- **Ratings:** 100,000+ ratings from 610 users
- **Rating Scale:** 0.5 to 5.0 stars
- **Files:** `movies.csv` (titles + genres), `ratings.csv` (user ratings)

---

## 🏆 Sample Results

**Input:** "Toy Story (1995)"

| Recommendation | Year |
|----------------|------|
| Toy Story 2 | 1999 |
| The Incredibles | 2004 |
| Monsters, Inc. | 2001 |
| Finding Nemo | 2003 |
| Shrek | 2001 |

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

---

## 📁 Project Structure

```
Movie-Recommendation-System/
├── movie_recommender.ipynb        # Main recommendation notebook
├── data/
│   ├── movies.csv                 # Movie titles and genres
│   └── ratings.csv                # User ratings data
├── models/                        # Saved model files
├── .gitignore                     # Excludes large CSV files
└── README.md                      # Project documentation
```

> ⚠️ Note: `movies.csv` and `ratings.csv` are not included due to GitHub file size limits. Download from [MovieLens](https://grouplens.org/datasets/movielens/) and place in the `data/` folder.

---

## 🚀 How to Run

**1. Clone the repository**
```bash
git clone https://github.com/shubhamjais04/Movie-Recommendation-System.git
cd Movie-Recommendation-System
```

**2. Install dependencies**
```bash
pip install pandas numpy scikit-learn matplotlib jupyter
```

**3. Download the dataset**

Download from [MovieLens](https://grouplens.org/datasets/movielens/) and place `movies.csv` and `ratings.csv` inside the `data/` folder.

**4. Open and run the notebook**
```bash
jupyter notebook movie_recommender.ipynb
```

**5. Use the recommender**
```python
recommendations = recommend_by_genre("Toy Story (1995)", top_n=10)
```

---

## 👨‍💻 Author
 
**Shubham Jaiswal**  
*ML engineer | Building systems that understand taste — one recommendation at a time*

---

## 📬 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/shubhjais04)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/shubhamjais04)












