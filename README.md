# TMDB Open Source API to apply NLP Content-Based Recommendation System for Streaming App Data | Part 2
# Why Part 2?

If we noticed from the data we have from the previous post (Recommendation System Using (Rank, User-User, Matrix Factorization) on Streaming App). We have limited advantages from the dataset. Some of the examples we lack of is:

* movie/tv year released to understand years' trends
full-content details such as overviews of the content would help us in applying content-based recommendations
more tags of genre because we know each content can have more genre
metrics of each content such as ratings, votes, and reviews. These can help identify which content has more value. Since STC did not add their ratings, we cannot conclude local popularity by using ratings because these ratings were collected globally from TMDB. Therefore, we can add ratings globally. For example, "Most Voted Movies Globally"
Business Understanding
In the previous article, I had planned to add a content-based recommendation system but unfortunately, that was not possible due to a lack of data points from STC that can help us to apply the content-based recommendation. In this article, our main goal is to make that happen by feeding our data with another source of data using TMDB OpenSource API. This will help us fetch required data points such as release date, overview, and genre.

Objective
Our goal here is simple, we will try to get as much information as possible to feed our dataset. We have a list of Movies/TVs from STC JAWWY, and we want to use TMDB API to get more information about STC movies. Steps:

Identfy Movies and TV Shows Names from STC datasets
Search these the Movies and TV Shows in TMDB API
Merge new variables into our main df
build content-based recommendation system based on cosine similarity