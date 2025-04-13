# 🎬 Movie Recommender System (Content-Based)

This is a machine learning project built to showcase practical skills in **data preprocessing**, **feature engineering**, **similarity modeling**, and **deployment**. The goal was to create a **content-based movie recommendation system** using real-world data from TMDB (The Movie Database), and deploy it as an interactive web app using **Streamlit**.

---

## 💼 This Project Demonstrates:

- My ability to handle real-world messy data
- Feature extraction and engineering skills
- ML techniques like vectorization and cosine similarity
- End-to-end deployment of a working ML app

---

## 🛠️ Technologies Used

| Area               | Tools & Libraries                                |
|--------------------|--------------------------------------------------|
| Data Manipulation  | `pandas`, `numpy`                                |
| Feature Engineering| `ast`, `nltk`, `sklearn`                         |
| ML Modeling        | `CountVectorizer`, `cosine_similarity`           |
| Web App Framework  | `Streamlit`, `requests`, `TMDB API`              |
| Deployment         | [Streamlit Community Cloud](https://streamlit.io/cloud) |
| Notebook Workflow  | `Jupyter Notebook` (for preprocessing & modeling) |

---

## 🧠 What I Did

### ✅ Data Preparation
- Combined `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv` using `title` as a key
- Extracted important features:
  - `genres`, `keywords`, `cast`, and `crew` (specifically director)
- Used `ast.literal_eval` to parse stringified JSON fields

### ✅ Feature Engineering
- Limited cast to top 3 actors for relevance
- Normalized and concatenated all selected features into a new column called `tags`
- Applied basic NLP preprocessing: lowercasing, removing spaces, stemming

### ✅ Vectorization & Similarity
- Vectorized `tags` using `CountVectorizer` (max features: 5000, no stopwords)
- Computed cosine similarity between all movies based on tag vectors
- Saved both similarity matrix and movie metadata using `pickle` for use in frontend

### ✅ Web App Frontend (Streamlit)
- Built a Streamlit UI to:
  - Let users pick a movie
  - Show 5 similar movies based on similarity
  - Fetch movie posters dynamically from TMDB API

---



