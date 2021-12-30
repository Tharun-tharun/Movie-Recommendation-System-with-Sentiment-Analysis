# Movie-Recommendation-System

This application provides all the details of the requested movie such as overview, genre, release date, rating, runtime, top cast, reviews, recommended movies, etc.

The details of the movies(title, genre, runtime, ratings, posters, etc) are fetched using an API by TMDB, https://www.themoviedb.org, and using the IMDB id of the movie in the API, I did web scraping to get the reviews given by the user in the IMDB site using `beautifulsoup4` and performed sentiment analysis on those reviews.

## Link to the application

Check out the live demo: https://lookupforcinema.herokuapp.com

# Medium Article About My Project

https://medium.com/analytics-vidhya/build-a-movie-recommendation-flask-based-deployment-8e2970f1f5f1

## Finding similar movies
### Without taking content into account (Just based on ratings)

Here just based on the ratings of the users for different movies, we use K nearest neighbours algorithm to find the movies which are similar.

### With taking Content into account

Here we just information about the movies, in this case the information of genres to predict the most similar movies.

## Matrix Factorisation(Collabarative Filtering)

Two approaches were tried to do matrix factorisation, the low rank method is very slow, so used scipy's SVD for sparse matrix.

## Architecture

![110212434-597bb700-7ec1-11eb-9ffa-7ac319e33123](https://user-images.githubusercontent.com/41158838/140876791-13716f4e-7e62-4f1e-8f06-155ce8360f16.jpg)

## Deep Learning Methods

One popular recommender systems approach is called Matrix Factorisation. It works on the principle that we can learn a low-dimensional representation (embedding) of user and movie. For example, for each movie, we can have how much action it has, how long it is, and so on. For each user, we can encode how much they like action, or how much they like long movies, etc. Thus, we can combine the user and the movie embeddings to estimate the ratings on unseen movies. This approach can also be viewed as: given a matrix (A [M X N]) containing users and movies, we want to estimate low dimensional matrices (W [M X k] and H [M X k]), such that: A≈W.H<sup>T</sub>
### 1.Matrix Factorisation based on Deep learning
### 2. Matrix Factorisation based on Deep learning with non negative embeddings.
### 3. Advanced neural network with different number of embeddings for both and movies.

## Required Tools

1. Keras
2. Scipy
3. Numpy
4. Pandas
5. python 3

### Sources of the datasets 

1. [IMDB 5000 Movie Dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)
2. [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)
3. [List of movies in 2018](https://en.wikipedia.org/wiki/List_of_American_films_of_2018)
4. [List of movies in 2019](https://en.wikipedia.org/wiki/List_of_American_films_of_2019)
5. [List of movies in 2020](https://en.wikipedia.org/wiki/List_of_American_films_of_2020)

### Please do ⭐ the repository, if it helped you in anyways
