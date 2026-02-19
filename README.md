# Movie Recommendation System

A content-based movie recommendation system that suggests similar movies based on genre matching and user ratings.

## Overview

This system recommends movies by analyzing genre similarity and rating patterns. Input a movie you like, and it returns 10 similar recommendations.

**Example:**
- Input: "Toy Story (1995)"
- Output: Other animated family movies with similar genres

## Dataset

**Source:** MovieLens dataset  
**Content:** 
- ~9,700 movies with titles and genres
- ~100,000 user ratings from 610 users
- Rating scale: 0.5 to 5.0 stars

**Files:**
- `movies.csv` - Movie titles and genre information
- `ratings.csv` - User ratings and timestamps

## How It Works

The recommendation system uses **content-based filtering** through genre analysis:

1. Extracts genres from the input movie
2. Searches popular movies (100+ ratings) for genre matches
3. Calculates similarity score based on shared genres
4. Ranks by genre overlap and average rating
5. Returns top 10 recommendations

## Technical Implementation

**Data Processing:**
- Filtered movies with minimum 100 ratings for quality recommendations
- Parsed pipe-separated genre strings
- Merged movie metadata with rating statistics

**Algorithm:**
- Genre-based similarity matching
- Set intersection for finding common genres
- Multi-criteria sorting (genre matches + average rating)
- Efficient implementation without large matrix operations

**Libraries Used:**
- pandas - data manipulation
- numpy - numerical operations
- matplotlib - visualizations
- pickle - model serialization

## Project Structure
```
movie-recommendation-system/
│
├── movie_recommender.ipynb       # Main analysis notebook
├── data/
│   ├── movies.csv                # Movie metadata
│   └── ratings.csv               # User ratings
├── models/
│   ├── popular_movies.pkl        # Processed movie data
│   └── recommend_function.pkl    # Recommendation function
├── images/                        # Saved visualizations
└── README.md
```

## Note on Data Files

The dataset files (`movies.csv`, `ratings.csv`) are not included in this repository due to GitHub's file size limits. 

**To run this project locally:**
1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/parasharmanas/movie-recommendation-system)
2. Place the CSV files in the `data/` folder
3. Run the notebook - it will generate the model files automatically

All code, visualizations, and results are available in the notebook for review.

## Sample Results

**Input:** "Toy Story (1995)"

**Recommendations:**
1. Toy Story 2 (1999)
2. The Incredibles (2004)
3. Monsters, Inc. (2001)
4. Finding Nemo (2003)
5. Shrek (2001)
6. A Bug's Life (1998)
7. The Lion King (1994)
8. Aladdin (1992)
9. Antz (1998)
10. Wallace & Gromit: The Wrong Trousers (1993)

*All recommendations share similar genres: Animation, Adventure, Comedy, Children, Fantasy*

## Features

- Fast execution time
- Genre-based content filtering
- Considers movie popularity (minimum rating threshold)
- Balances genre similarity with quality (average ratings)
- Saved models for reusability

## Key Findings

**From EDA:**
- Most ratings are between 3-4 stars
- Popular movies like "Forrest Gump" and "Shawshank Redemption" have 300+ ratings
- Highest-rated movies tend to be critically acclaimed classics

**Recommendation Performance:**
- Works best with popular movies
- Effectively groups movies by genre
- Provides diverse recommendations within genre constraints

## How to Run

1. **Install dependencies:**
```bash
pip install pandas numpy matplotlib seaborn
```

2. **Run the notebook:**
```bash
jupyter notebook movie_recommender.ipynb
```

3. **Use the recommender:**
```python
recommend_by_genre('Movie Title (Year)', top_n=10)
```

## Example Usage
```python
# Get recommendations
recommendations = recommend_by_genre('Toy Story (1995)', top_n=10)
print(recommendations)
```

## What I Learned

**Technical Skills:**
- Building recommendation systems
- Content-based filtering algorithms
- Genre parsing and text processing
- Working with real-world user rating data
- Model persistence with pickle

**Key Takeaways:**
- Simple approaches can be effective
- Genre-based filtering is intuitive and explainable
- Data preprocessing is crucial for recommendation quality
- Balancing multiple factors (similarity + quality) improves results

## Future Improvements

- Add cast and director similarity
- Implement collaborative filtering
- Hybrid recommendation (content + collaborative)
- User preference learning
- Web interface for easy interaction

## Technologies

- **Language:** Python 3
- **Data:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Persistence:** Pickle

## Dataset Source

MovieLens dataset provided by GroupLens Research

---

**Shubham Jaiswal**

GitHub: [@shubhamjais04](https://github.com/shubhamjais04)  
LinkedIn: [linkedin.com/in/shubhamjaiswal2004](https://linkedin.com/in/shubhamjaiswal2004)  
Email: shubhjais.in@gmail.com

---


*A practical implementation of recommendation systems demonstrating content-based filtering techniques.*

