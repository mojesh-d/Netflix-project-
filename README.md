# Netflix Movie Recommendation System

##📌 Project Description

This project builds a personalized movie recommendation system using the Netflix dataset. The main goal is to predict user ratings for unseen movies and recommend the most suitable ones to each user. It applies collaborative filtering techniques to learn user preferences from historical rating data.

##📂 Data Loading and Description

The dataset is loaded from CSV/Netflix files. It contains user IDs, movie IDs, and their corresponding ratings. Each row represents a rating that a user has given to a movie. The data is explored to understand its size, structure, and basic statistics before applying any modeling.

##📊 Exploratory Data Analysis (EDA)

EDA helps in understanding the distribution of ratings, user behavior, and movie popularity. Key steps include:

-Checking the number of ratings per user.

-Checking the number of ratings per movie.

-Identifying the most popular and least popular movies.

-Visualizing the rating distribution to see overall trends. This analysis helps decide how to clean and filter the dataset for better model performance.

##⚙️ Pre-Filtering Techniques

To improve recommendation quality and reduce noise, we apply two main filtering strategies:

*Remove movies with very few ratings – Movies rated by only a handful of users may not provide enough information for reliable predictions, so they are removed.

*Remove users who rated very few movies – Users with too few ratings may not have enough data to learn their preferences accurately, so they are also removed. These steps ensure that the remaining dataset is dense enough for the model to learn meaningful patterns.

##🤖 Model Implementation

We use the SVD (Singular Value Decomposition) algorithm from the Surprise library to build the recommendation model. Steps include:

*Converting the data into the Surprise format.

*Training the SVD model on the training set.

*Evaluating the model using cross-validation with RMSE to measure prediction accuracy. SVD learns latent factors for users and movies to estimate how a user would rate an unseen movie.

##🎯 Recommendation Part

After training, the model predicts ratings for all unseen movies for a target user. Then it sorts the predictions and recommends the top-rated movies for that user. This helps each user discover new movies they are likely to enjoy based on their previous ratings.

##✅ Conclusion

The system successfully recommends personalized movies using collaborative filtering and SVD. Pre-filtering users and movies significantly improved the model’s accuracy and recommendations. This approach can be further extended by adding more data or hybrid models combining content and collaborative filtering.
