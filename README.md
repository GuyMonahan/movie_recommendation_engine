# movie_recommendation_engine
A project where we aim to predict the top 5 movies for an individual based on their previous ratings.


Outline:
- Business Proposal
- Our Approach
- Model
- Conclusions

Business Proposal:
In a world where the need to best target your customer is arms race for their patronage, needing to stand out from your competitors is key. Being able to utilize recommendation systems to help customers better find products or services that they are likely to want keeps all parties happy. In this instance we are using recommendation systems to create a program that will return the top five most likely films a user will enjoy depending on how they have rated other films. This has broad applications for other topics and situations, but here it is especially important for corporations like Amazon, Netflix, Hulu, and Disney, and the many dozens of streaming services that seem to pop up every year or two. By having a good algorithm, and an environment to improve upon it, a streaming service will be able to potentially retain more viewers by recommending items they didn’t realize they wanted to see.



Our Approach:
Using the MovieLens small dataset we had over 100,000 movies to work with. The data included ratings, genres, movie titles, and more. We were specifically interested in the ratings as building a system around that made a lot of sense in that reviewers that had similar reviews for a movie might explain how others might act (user-user model). Once we had sectioned our pertinent data and created visualizations to better understand our data we set up our pandas dataframe in a surprise framework for the recommendation engine. After fitting the model and creating train and test sets we applied many different models to find the one with the best fit (lowest MSRE). After we had that figured we created a function that would utilize the model and functions to return the top five recommendations.

<p align="center">
 <img width="275" height="400" src=images/collab_filter.png>
 </p>

Model:
We used many different models, starting with KNN (K-Nearest Neighbors) using cosine & Pearson, but found that cosine was better for our needs, as the users weights were not a factor, and similar did KNN Baseline, and KNN Means. After that we wanted to use SVD (Singular Value Decomposition) to possibly find a better result, and used GridSearch to reveal the best parameters. SVD ended up having the best results, and therefore it was used.

<p align="center">
 <img width="1000" height="336" src=images/User_rec_system.png>
 </p>

Conclusions:
We created a solid model of a recommendation system using the MovieLens dataset for finding movies a user might also enjoy. The execution of the process of cleaning and modeling the data is applicable for many situations but in our case the movie ratings are much easier to grasp. Using our data cleaning techniques and processes to trial different models we were able to find a powerful way to help a user find their five movies that they would likely enjoy.  
