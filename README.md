# 🎬 Movie Recommendation System

This project is a **content-based movie recommendation system** built using **Python**, **Pandas**, **NLTK**, and **Scikit-learn**.  
It recommends movies similar to a given movie based on their plot, genres, cast, crew, and keywords.

---

## 📌 Features
- Loads and preprocesses the **TMDB 5000 Movies Dataset**.
- Extracts relevant movie details:  
  - Movie title  
  - Overview (description)  
  - Genres  
  - Keywords  
  - Cast  
  - Crew (Director)  
- Cleans and transforms text data for analysis:
  - Tokenization
  - Stopword removal
  - Stemming using **Porter Stemmer**
- Combines movie metadata into a single **tags** column.
- Converts text to numerical vectors using **CountVectorizer** (max 5000 features).
- Measures similarity between movies using **Cosine Similarity**.
- Returns top 5 most similar movies to a given title.
- Includes basic evaluation with **Precision, Recall, and F1 Score**.

---

## 📂 Dataset
You will need the following datasets:
- **tmdb_5000_movies.csv**
- **tmdb_5000_credits.csv**

Download from:  
[TMDB 5000 Dataset (Kaggle)](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

Place them in the same directory as the script.

---

## 🛠 Installation & Setup
1. **Clone the repository** (or download the script):
   ```bash
   git clone https://github.com/yourusername/movie-recommendation-system.git
   pip install numpy pandas scikit-learn nltk
   cd movie-recommendation-system

## ▶️ Usage
**Run the script:**
    ```bash
    python project__2_movie_recommendation_system_.py
    #Call the recommend() function with a movie title:
    recommend('Avatar')
    Example Output:

    mathematica

    Guardians of the Galaxy
    Star Trek
    Star Wars
    John Carter
    The Last Samurai

## 📊 Evaluation
The script includes a basic evaluation function:

     ```bash
     evaluate_recommendations('Gandhi', ['Avatar', 'The Lego Movie', 'Batman', 'Aliens'])
     Output Example:
     Precision: 0.50
     Recall: 0.50
     F1 Score: 0.50

## 📦 Technologies Used
Python (Data processing & ML)
Pandas & NumPy (Data manipulation)
NLTK (Text processing & stemming)
Scikit-learn (Vectorization & similarity calculation)
Cosine Similarity (Similarity metric)

## 🚀 Future Improvements
Implement TF-IDF Vectorization for better weighting.
Add user-based and hybrid recommendation options.
Build a web interface using Flask or Streamlit.
Enhance evaluation with more comprehensive ground truth data.
Integrate Large Language Models (LLMs) such as GPT, LLaMA, or Mistral to:
Generate context-aware explanations for why a movie is recommended.
Accept natural language queries like "Suggest me sci-fi movies like Inception but with more action".
Use Agentic AI (Autonomous Agents) to:
Continuously fetch and learn from new movie datasets.
Adapt recommendations based on user viewing history and preferences over time.
Combine multiple data sources (reviews, ratings, trailers) for more accurate, multi-modal recommendations.
