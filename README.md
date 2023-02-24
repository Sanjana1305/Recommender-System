# Recommender-System
Movie-Recommender-System

Types of recommender system

1)Content based -: recommender system which recommends on the basis of similarities of content.
                   like if we are watching romantic movie then recommender system recommends us romantic movies

2)Collaborative filtering-: recommends on th basis of similarities of users.
ex- 2 user A and B are there and their similarity score is 9(out of 10)

if A likes a movie M then recommender system can recommend movie M to user B.


3)Hybrid -: combination of the above two approaches.

 
In our project Movie  Recommender system we will be using content based recommender system.

 PROJECT FLOW-

1.DATA 
2.Preprocess the  data according to our need.
3.Model building.
4.Website development
5.Deployement



** dataset used is TMDB 5000 movie dataset from kaggle.
in the project we have merged both the dataset movies and credits and rensame it as movies.
 

since we have to apply content based recommender system  ,we have to create tags for the  movies ,so we have to delete some unnecessary columns from the movies dataset.

keeping those  columns which required and remove unnecessary
# 1.genres
# 2.id
# 3.keywords
# 4.title
# 5.overview
# 6.cast
# 7.crew


so far we done with the processing of the data and at last we have created a feature called tags of the movie.


## problem statement-:

 we have to create a website in which user entered a movie name or search for a movie and the recommender system has to recommend similar movies based on the users choice.

similarities b/w the movies is calculated on the basis of tags.(find the similar words among tags of the movies)
but this brute force approach is not efficient.

so we go for vectorization approach.

we have movie_id ,name and tags of the movies.we have to convert  the tags of the movie into vector
in 2d space vector can be represented (having x and y coordinate).
suppose user picked a vector (movie) so the closest vector represent the similar movies to the movies what user searched for or picked .
 this technique is called text vectorization.
there are various technique to convert text into vector. and we use " bag of words technique".


suppose a tag contains 100 words ,so for 5000 movies 

in this we concatenate all the tags of the all the movies.then most we extract top 5000  most frequent words . 
 
then we  compare the individual tags of each movie with those 5000 words.this craete a table and each row represent a vector
 while doing vectorization we won't consider the stopwors like  "are","the" etc which have no contribution in the meaning of the sentence





