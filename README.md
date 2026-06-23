# 🎬 Movie Recommendation System

A **content-based** movie recommender built on the TMDB 5000 dataset.

## How It Works
Merges movie metadata → extracts genres, keywords, top 3 cast, director  
→ builds a unified `tags` string → CountVectorizer → cosine similarity

## Project Structure
