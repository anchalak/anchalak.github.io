## Recommender System
A recommender system is a filtering system that is used to predict "rating" or "preference" a user would give to an item. 
Recommender systems are utilized in a variety of areas and are most commonly recognized as playlist generators for video and music services like Netflix, YouTube and Spotify.
Amazon uses recommender systems as well to make accurate product recommendations to their users. There are multiple filtering methods that can be used to build a recommmender system; two of the most common ones are collaborative filterting and content-based filtering.
## Content-Based Filtering
Content-based filtering methods are based on a description of the item and a profile of the user's preferences. 
Many algorithms can be used to extract key features of a the product that a user likes and then find another product with same or similar key features.
This method involves creating a user profile to indicate the type of item this user likes. In order to create a user profile, one can either create a model of the user's preference or a history of the user's interaction with the recommender system.
For the purposes of this project, we decided not to use content-based filtering as we wanted to give a variety of suggestions with variety of key features.
## Collaborative Based Filtering
Another approach to the design of recommender systems that has wide use is collaborative filtering. 
This approach is based on the assumption that people who agrees in the past will agree in the future, and that they will like similar kinds of items as they will like similar kinds of items as they liked in the past.
With our project we decided to take this approach. The dataset we are working with is made of users and their ratings for different movies. There are about 1000 users and about 2700 movies. 
##### Principle Component Analysis (PCA)
PCA is a dimensionality reduction technique with minimum loss of information. 
Given a collection of points in two, three, or higher dimensional space (in our case, 2700), a "best fitting" line can be defined as one that minimizes the average squared distance from a point to the line. The next best-fitting line can be similarly chosen from directions perpendicular to the first. 
Repeating this process yields an orthogonal basis in which different individual dimensions of the data are uncorrelated.
These basis vectors are called principal components, and several related procedures principal component analysis (PCA). 
In terms of our project, these principal components are key features of the movies, resulting in each row being a linear combination of all the movies. This linear combination of all the movies can be thought of as a hypothetical movie with only key features of the movies that the user has highly rated.
##### K-Nearest Neighbors (KNN)
The KNN algorithm is a type of supervised machine learning algorithms. It simply calculates the distance of a new data point to all other training data points. 
The distance can be of any type e.g Euclidean or Manhattan etc. In terms of our project, we used KNN algorithm on the PCA table where we compared one user's perference to the hypothetical movies to find which five users are closest in their preference.
