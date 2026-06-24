# 🎬 Movie Recommender System

A machine learning-based movie recommendation system built with Python and Streamlit. This application recommends similar movies based on movie content such as genres, cast, crew, keywords, and overview using **Content-Based Filtering**.

---

## Project Overview

This project suggests movies similar to a selected movie by analyzing textual features and calculating similarity using **Cosine Similarity**.

Instead of storing a precomputed similarity matrix (`similarity.pkl`), similarity is calculated dynamically during runtime inside the Streamlit application.

---

## Features

* Recommend top 5 similar movies
* Content-based filtering
* Interactive Streamlit UI
* Runtime similarity calculation
* Easy deployment and lightweight GitHub repository

---

## Dataset

The dataset contains movie information such as:

* Movie ID
* Title
* Genres
* Keywords
* Cast
* Crew
* Overview

Datasets can be found on:

* Kaggle
* MovieLens

---

## Machine Learning Workflow

### 1. Data Collection

Collected movie metadata datasets.

### 2. Data Cleaning

Performed:

* Null value removal
* Duplicate removal
* Column selection

Important columns:

* movie_id
* title
* genres
* keywords
* cast
* crew
* overview

### 3. Feature Engineering

Combined important columns into a single column called **tags**.

Example:
genres + keywords + cast + crew + overview

### 4. Text Processing

Applied preprocessing techniques:

* Lowercasing
* Tokenization
* Stemming

### 5. Vectorization

Converted text into numerical vectors using CountVectorizer.

```python
from sklearn.feature_extraction.text import CountVectorizer
```

### 6. Similarity Calculation

Calculated movie similarity using Cosine Similarity.

```python
from sklearn.metrics.pairwise import cosine_similarity
```

### 7. Recommendation Process

1. User selects a movie
2. Find movie index
3. Calculate similarity scores
4. Sort scores
5. Return top 5 recommendations

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Streamlit
* Pickle
* NLTK

---

## Project Structure

movie-recommender/
│
├── app.py
├── movie_dict.pkl
├── requirements.txt
└── README.md

---

## Installation

Clone the repository:

```bash
git clone <repository-link>
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Streamlit app:

```bash
streamlit run app.py
```

---

## Future Improvements

* Add movie posters using TMDB API
* Improve recommendation accuracy
* Add search suggestions
* Deploy on cloud platform

---

## Conclusion

This project demonstrates how machine learning can be used to build an intelligent recommendation system that helps users discover movies based on their preferences.
