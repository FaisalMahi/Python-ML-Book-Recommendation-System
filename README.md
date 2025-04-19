# 📚 Python-ML-BookRecommendationSystem

> A smart book recommendation system built with Python, Pandas, Scikit-learn, and Flask — using collaborative filtering and popularity-based recommendation techniques.

---

## 🚀 Project Overview

This project is a **Book Recommendation System** that suggests books based on user preferences using:

- 🔥 **Popularity-based filtering**
- 🔄 **Collaborative filtering** (using cosine similarity)
- 📊 Real-world dataset from Kaggle containing **books, ratings, and user demographics**

The app is powered by **Flask** as a lightweight backend and served with a responsive **Bootstrap** frontend.

---

## 🧠 ML Concepts Used

While simple, this project uses **unsupervised machine learning** through:

- 📌 **User-Item Matrix** using `pandas.pivot_table`
- 🔗 **Cosine Similarity** via `sklearn.metrics.pairwise.cosine_similarity`
- 📈 Matrix manipulation for finding the **top-N similar books**
- 📦 Models are saved using `pickle` and reused in a lightweight Flask app

---

## 🗂️ Dataset

📍 [Book Recommendation Dataset on Kaggle](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset)

Files used:
- `Books.csv` – Metadata about books (title, author, image, etc.)
- `Ratings.csv` – User ratings for books
- `Users.csv` – User demographic data

---

## 📸 Features & UI

✨ Features:
- View **Top 50 Most Popular Books**
- Input a book name and get **5 similar recommendations**
- Simple and clean UI using **Bootstrap**
- Display covers, authors, average rating, and vote count

---

## 🛠️ Tech Stack

| Area         | Technologies                   |
|--------------|--------------------------------|
| Backend      | Python, Flask                  |
| ML/Preprocessing | Pandas, NumPy, Scikit-learn  |
| Frontend     | HTML, CSS, Bootstrap           |
| Model Saving | Pickle                         |

---

## 💡 How It Works

1. **Preprocessing**: Books with >250 ratings are selected for popularity-based filtering.
2. **Collaborative Filtering**:
   - Active users (rated >200 books) are selected.
   - Books with >50 ratings are filtered.
   - A user-item matrix is built.
   - Cosine similarity is used to find similar books.
3. **Flask App**: Loads `pickle` models and renders predictions.

---

## 💻 Run It Locally

```bash
# Clone the repo
git clone https://github.com/yourusername/Python-ML-BookRecommendationSystem

# Go to the project folder
cd Python-ML-BookRecommendationSystem

# Install dependencies
pip install -r requirements.txt

# Run the Flask app
python app.py
