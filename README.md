# Movie Recommender System

Welcome to the Movie Recommender System project! This repository contains a movie recommendation engine that utilizes the TMDB 5000 dataset and cosine similarity to suggest movies based on user input.

## Overview

The Movie Recommender System provides personalized movie recommendations based on a user's selected movie. It uses the TMDB 5000 dataset, which contains a comprehensive collection of movie information, and applies cosine similarity to recommend movies that are similar to the chosen one.

## Dataset

### TMDB 5000 Dataset

The TMDB 5000 dataset is a popular dataset for movie recommendations and contains detailed information about movies. This dataset includes:

**Link to dataset**: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

- **Movie ID**: Unique identifier for each movie.
- **Title**: The title of the movie.
- **Overview**: A brief description or synopsis of the movie.
- **Genres**: Categories or genres to which the movie belongs.
- **keywords**: Words which are similar or describes the gist if the movie.
- **cast**: Details of all the artists who worked in that particular film.
- **crew**: Details of all the professionals who worked for that particular film.

The dataset is used to create a movie similarity matrix that allows the recommender system to suggest movies based on content similarity. The larger the distance, the less is the similarity.

## Methods

### Data Preprocessing

1. **Loading Data**: The dataset is loaded and converted into a DataFrame for easier manipulation.
2. **Feature Extraction**: Key features such as movie genres, cast, crew and keywords are extracted and processed.
3. **Vectorization**: Movie descriptions are converted into numerical vectors using TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer.
4. **Stemming**: To remove the excess words with similar meaning, utilization of stemming method is performed.

### Similarity Calculation

1. **Cosine Similarity**: To measure the similarity between movies, cosine similarity is used. This metric calculates the cosine of the angle between two non-zero vectors in an n-dimensional space, which in this case represents the movie features.

### Recommendation Algorithm

1. **Indexing Movies**: Each movie is indexed to quickly locate it during the recommendation process.
2. **Finding Similar Movies**: When a user selects a movie, the system calculates the cosine similarity between the selected movie's vector and all other movie's vectors in the dataset.
3. **Sorting Recommendations**: The movies are sorted based on their similarity scores, and the top 5 recommendations are returned to the user.
