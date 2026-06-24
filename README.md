# Movie Recommender System

A machine learning-based movie recommendation system that suggests similar movies based on movie content such as genres, keywords, cast, crew, and overview.

## Project Overview
This project uses **Content-Based Filtering** to recommend movies.  
It compares movie features and suggests the most similar movies to the user.

Example:
Input:
- Avatar

Output:
- Guardians of the Galaxy
- John Carter
- Aliens
- Star Trek

---

## Features
- Movie recommendation based on similarity
- Content-based filtering
- Fast similarity search using cosine similarity
- User-friendly interface (if deployed with Streamlit)

---

## Dataset
This project uses movie datasets containing:
- Movie Title
- Movie ID
- Genres
- Keywords
- Cast
- Crew
- Overview

Datasets can be downloaded from:
- Kaggle
- MovieLens

---

## Machine Learning Workflow

### 1. Data Collection
Collected movie metadata datasets.

### 2. Data Preprocessing
- Removed null values
- Removed duplicate records
- Selected important columns

Columns used:
- movie_id
- title
- overview
- genres
- keywords
- cast
- crew

### 3. Feature Engineering
Combined useful text columns into a single column called **tags**.

Example:
genres + keywords + cast + crew + overview

### 4. Text Processing
Applied:
- Lowercasing
- Tokenization
- Stemming

This helps normalize text data.

### 5. Vectorization
Used **CountVectorizer** to convert text into numerical vectors.

```python
from sklearn.feature_extraction.text import CountVectorizer
```

### 6. Similarity Calculation
Used **Cosine Similarity** to calculate similarity between movies.

```python
from sklearn.metrics.pairwise import cosine_similarity
```

### 7. Recommendation Generation
When a user enters a movie name:
1. Find the movie index
2. Fetch similarity scores
3. Sort movies by similarity
4. Return top recommendations

---

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Streamlit (optional)

## Libraries Required
Install dependencies:

```bash
pip install pandas numpy scikit-learn nltk streamlit
```

---

## Project Structure
```bash
movie-recommender/
│
├── app.py
├── movie_recommender.ipynb
├── movies.pkl
├── similarity.pkl
├── requirements.txt
└── README.md
```

---

## How to Run
1. Clone repository

```bash
git clone <your-repository-link>
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Run project

```bash
streamlit run app.py
```

---

## Future Improvements
- Add poster images using API
- Improve recommendations with collaborative filtering
- Deploy on cloud platform
- Add search suggestions

---

## Conclusion
This project demonstrates how machine learning can be used to build an intelligent recommendation system that helps users discover movies similar to their interests.
