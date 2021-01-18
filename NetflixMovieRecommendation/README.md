# Project Overview
Netflix is one of the fastest growing OTT platforms in the world today. It has acquired a big viewer base of movie and TV show lovers across the globe especially in the last decade. This project contains my analysis of Netflix data as well as building a movie recommender system. The project has three parts...

## Exploratory Data Analysis
I perform EDA of the netflix data and gain insights on content type, genres, content contributing countries, high rated and low rated movies. To get the ratings for movies listed in Netflix, I merged external IMDB dataset with Netflix dataset. Here is a preview of movies with high IMDB rating on Netflix

![Analysis](https://user-images.githubusercontent.com/58431708/99895823-8e685300-2cb0-11eb-82fb-9d5d0eb47cb8.png)

## Data cleaning and preparation for building a basic recommender system
Building a recommender system involves numerical computations. As the data is initially in the text format, I make use of sklearn NLP tools to convert text data to numerical data. I also clean the data by filling null values with empty strings and converting all text to lowercase.

## Model building and Testing
The model is based on cosine similarity matrix on movie title, cast, director, plot, genre. Based on a selected movie, 10 similar movies are recommended to a user. Here is a preview of results.

![Result](https://user-images.githubusercontent.com/58431708/99895924-a42a4800-2cb1-11eb-9a1d-09a2b87b2e5a.png)

## To view the full project on nbviewer, click the following link: 
https://nbviewer.jupyter.org/github/praveenmaripeti/Data-Science-Projects/blob/main/NetflixMovieRecommendation/netflix-eda-movie-recommendation.ipynb
