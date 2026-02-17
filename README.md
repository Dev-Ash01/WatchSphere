# 🎬 WatchSphere – Movie Recommendation System  

An intelligent movie discovery platform that provides personalized movie suggestions. This repository contains the complete data processing and model training pipeline that generates the files required for the final Streamlit web application.  

Visit here: https://mywatchsphere.streamlit.app/ 

---

## 🚀 About The Project  

**WatchSphere** is a *content-based recommendation system* that predicts user preferences and suggests movies with similar themes, genres, or contributors.  

The recommendation engine is built on cosine similarity applied to a carefully engineered set of metadata, ensuring *contextually relevant and accurate movie matches*.  

---

<img width="2557" height="1260" alt="Image" src="https://github.com/user-attachments/assets/d1edd44e-e099-446f-95cc-9652e5587798" />

---

<img width="2456" height="1203" alt="Image" src="https://github.com/user-attachments/assets/2b4d87d1-0566-4b3a-8502-f3fbd1be2c99" />

---

## 🧠 The Recommendation Pipeline  

The system follows a classic NLP-based pipeline:  

### 1. Feature Engineering  
- Data from the TMDB 5000 dataset is cleaned and merged.  
- Metadata and synopsis are combined into a single **“tag”** for each movie.  

### 2. Text Vectorization  
- Tags are normalized (lowercasing + stemming).  
- Converted to numerical vectors using **CountVectorizer**.  

### 3. Similarity Modeling  
- A **cosine similarity matrix** computes relationships between all movies.  
- The model is saved as `.pkl` files for use in the Streamlit app.  

---

## ✨ Features of the Streamlit App  

- 🧠 **Personalized Recommendations** – Get instant, relevant movie suggestions.  
- 🔥 **Top Picks Section** – Discover trending and popular films.  
- 🔎 **Search Functionality** – Find movies by title.  
- ℹ **Detailed Movie Pages** – Access poster, cast, overview, and more.  
- 📄 **Paginated Results** – Browse large lists of films easily.  
- 🔒 **Secure API Handling** – TMDB API key is stored in `secrets.toml`.  

---

<img width="2454" height="1199" alt="Image" src="https://github.com/user-attachments/assets/58667e45-1f8c-46e6-9726-c0aa47ff1ba1" />

---

<img width="2464" height="1201" alt="Image" src="https://github.com/user-attachments/assets/3dc05fa4-7948-4d7f-a26d-a1ea8854cd52" />

---

## 🛠 Built With  

- 🐍 Python  
- 📓 Jupyter Notebook – Data exploration & model building  
- 🐼 Pandas – Data manipulation  
- 🤖 Scikit-learn – CountVectorizer, cosine_similarity  
- 📚 NLTK – Text preprocessing  
- 🎈 Streamlit – Web application  
- 🌐 Requests – TMDB API calls  

---

## ⚙ Setup and Usage  

This project has **two main parts**: generating the model and running the app.  

### Part 1: Generate Model Files  

1. Place the dataset files (`tmdb_5000_movies.csv`, `tmdb_5000_credits.csv`) in the root folder.  
2. Run the Jupyter Notebook `Movie Recommendation System.ipynb`.  
3. This will generate the `.pkl` files (saved in your project directory).  

---

### Part 2: Run the Streamlit App  

#### 1. API Key Setup  
- Create a folder named `.streamlit` in the project root.  
- Inside it, create a `secrets.toml` file:

```toml
TMDB_API_KEY = "your_actual_api_key_here"
