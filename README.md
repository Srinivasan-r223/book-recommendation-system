
# 📚 Book Recommendation System (Content-Based Filtering)

## 📌 Project Overview
This project implements a **content-based book recommendation system** using **Natural Language Processing (NLP)** techniques. The system recommends books similar to a given book based on textual features such as **title, author, and language**, rather than relying on user ratings or collaborative data.

The core idea is to represent books as text vectors using **TF-IDF** and compute similarity using **Cosine Similarity**.

---

## 🎯 Problem Statement
Online book platforms often need to suggest books that are similar in content to a book a user likes. In the absence of explicit genre labels or user interaction data, this project demonstrates how **content-based filtering** can be used to generate meaningful recommendations purely from book metadata.

---

## 🧠 Approach & Methodology

### 1. Data Preprocessing
- Selected relevant features:
  - `title`
  - `authors`
  - `language_code`
  - `average_rating`
  - `ratings_count`
- Removed missing values to ensure clean text processing
- Combined textual features into a single column for vectorization

### 2. Feature Extraction (TF-IDF)
- Used **TF-IDF Vectorizer** to convert text into numerical feature vectors
- This emphasizes important words while reducing the impact of common terms

### 3. Similarity Computation
- Applied **Cosine Similarity** on TF-IDF vectors
- Generated a similarity matrix to measure how close books are to each other

### 4. Recommendation Logic
- Identified the most similar books based on cosine similarity scores
- Removed self-recommendations
- Re-ranked results using **average rating** to improve recommendation quality

### 5. Evaluation
- Used **Precision@K** as a basic evaluation metric
- Measures how many of the top-K recommended books have high ratings (≥ 4.0)

---

## 🛠️ Technologies Used
- Python
- Pandas & NumPy
- Scikit-learn
  - TF-IDF Vectorizer
  - Cosine Similarity
- Jupyter Notebook

---

---

## ▶️ How to Run the Project

1. Clone the repository
```bash
git clone https://github.com/Srinivasan-r223/book-recommendation-system.git
```

2. Install dependencies
```bash
pip install pandas numpy scikit-learn
```

3. Open the notebook
```bash
jupyter notebook "book rec sys.ipynb"
```

4. Run all cells and test recommendations:
```python
recommend_books("The Hobbit")
```

---

## 📊 Sample Output
```
Title                         Author              Average Rating
---------------------------------------------------------------
The Fellowship of the Ring    J.R.R. Tolkien      4.36
The Two Towers                J.R.R. Tolkien      4.45
The Return of the King        J.R.R. Tolkien      4.56
```

---

## ✅ Key Learnings
- Implemented a complete **content-based recommendation pipeline**
- Learned how TF-IDF converts text into meaningful numerical representations
- Understood similarity-based ranking using cosine similarity
- Applied basic evaluation metrics for recommender systems

---
