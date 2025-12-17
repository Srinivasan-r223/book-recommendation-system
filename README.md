📚 Book Recommendation System (Content-Based Filtering)

📌 Overview

This project implements a content-based book recommendation system using machine learning and NLP techniques.
The system recommends books similar to a given book by analyzing textual metadata such as title, author, and publisher, without relying on explicit genre labels.

🎯 Problem Statement

Traditional recommendation systems often depend on genre tags or user interaction data.
This project demonstrates how meaningful recommendations can be generated using only book metadata, making it suitable for datasets with limited features.

🛠️ Technologies Used

Python

Pandas, NumPy

Scikit-learn

TF-IDF Vectorizer

Cosine Similarity

🔍 Approach
1. Data Preprocessing

Selected relevant features: title, authors, publisher

Handled missing values for both text and numerical fields

Combined multiple textual features into a single content field

2. Feature Extraction

Applied TF-IDF (Term Frequency–Inverse Document Frequency) to convert textual data into numerical vectors

Removed common English stop words to reduce noise

3. Similarity Computation

Used cosine similarity to compute similarity scores between books

Identified top similar books based on vector similarity

4. Recommendation Enhancement

Re-ranked similar books using average_rating

Applied popularity filtering using ratings_count to ensure reliable recommendations

5. Evaluation

Evaluated recommendation quality using Precision@K

Defined relevance based on a rating threshold due to lack of user interaction data

📈 Example Output

Given a book title such as “The Hobbit”, the system recommends:

Books with similar content

Higher average ratings

Sufficient number of user ratings

📊 Evaluation Metric

Precision@K was used as the evaluation metric:

Measures the proportion of high-quality books in the top-K recommendations
