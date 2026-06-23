# 🎬 Movie Recommendation System

A **content-based** movie recommender built on the TMDB 5000 dataset.  
Enter any movie title and get 5 similar movies instantly.

## 🚀 How It Works

1. Merges movie metadata (genres, keywords, cast, director, overview)
2. Builds a unified `tags` string per movie
3. Vectorizes with `CountVectorizer` (top 5000 features)
4. Ranks similarity using **cosine similarity**

## 📁 Project Structure

```
movie-recommendation-system/
├── notebooks/
│   └── Movie_Recommendation_System.ipynb   # Full pipeline
├── src/
│   ├── preprocess.py                        # Data cleaning & tag building
│   └── recommend.py                         # Recommendation logic
├── data/
│   └── README.md                            # Dataset download instructions
├── models/
│   └── README.md                            # Where .pkl files go
├── requirements.txt
├── .gitignore
└── README.md
```

## ⚙️ Setup

```bash
# 1. Clone the repo
git clone https://github.com/Mrudula7-P/movie-recommendation-system-tmbd-dataset.git
cd movie-recommendation-system-tmbd-dataset

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download the dataset → see data/README.md

# 4. Run the notebook to generate pickle files
jupyter notebook notebooks/Movie_Recommendation_System.ipynb
```

## 🎯 Example

```python
from src.recommend import load_artifacts, recommend

movies, similarity = load_artifacts()
recommend(
