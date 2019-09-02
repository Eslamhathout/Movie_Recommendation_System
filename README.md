# Movie_Recommendation_System
Domain Background
“Student briefly details background information of the domain from which the project is proposed. Historical information relevant to the project should be included. It should be clear how or why a problem in the domain can or should be solved. Related academic research should be appropriately cited. A discussion of the student's personal motivation for investigating a particular problem in the domain is encouraged but not required.”

I would like to build a full commercial solution in my capstone project. I decided to build a full django website for movie recommendations. I will add the logging, rating, as well as the recommendation system which will cluster the users based on their tests and use such clusters to recommend new movies to the user which are the top rated in his/her cluster. 

Movie recommendation systems could lead to a good commercial project  for companies such as Netflix, etc or even websites such as Rotten Tomatoes, etc
 
 
Problem Statement

“Student clearly describes the problem that is to be solved. The problem is well defined and has at least one relevant potential solution. Additionally, the problem is quantifiable, measurable, and replicable.”

The problem which I need to implement a solution for in my project is to best classify new users based on their ratings for a list of movies. The list of movies should be from different categories “action, comedy, etc” and the aim of this ratings is to assign the user to a predefined clusters, then recommend the movies which is best rated from the users in the same cluster. This will guarantee that the user will like the movie which is liked by the users who have the same taste. The recommended sys

In this project, I will focus on just building the clustering system that will use a dataset of pre-rating movies and create suitable clusters to be used in the project for assigning the users to.






Datasets and Inputs
“The dataset(s) and/or input(s) to be used in the project are thoroughly described. Information such as how the dataset or input is (was) obtained, and the characteristics of the dataset or input, should be included. It should be clear how the dataset(s) or input(s) will be used in the project and whether their use is appropriate given the context of the problem.
The dataset which I will be using throughout the project is the movielens dataset which is presented here: https://grouplens.org/datasets/movielens/. I will use the Full Movielens dataset which is a dataset of 27,000,000 ratings and 1,100,000 tag applications applied to 58,000 movies by 280,000 users. Includes tag genome data with 14 million relevance scores across 1,100 tags. Last updated 9/2018.
Solution Statement

“Student clearly describes a solution to the problem. The solution is applicable to the project domain and appropriate for the dataset(s) or input(s) given. Additionally, the solution is quantifiable, measurable, and replicable.”
The solution which I will be using in the capstone project will use the existing Movielens dataset and it’s ratings to create clusters of users based on their ratings to different types of movies. 
The input: Should be new user ratings for different types of movies.
The processing: The model should then add the user to a predefined cluster. 
The output: Should be suggestion to watch new movies. 
 
Benchmark Model
“A benchmark model is provided that relates to the domain, problem statement, and intended solution. Ideally, the student's benchmark model provides context for existing methods or known information in the domain and problem given, which can then be objectively compared to the student's solution. The benchmark model is clearly defined and measurable.”
The benchmark model which I will be looking for in the project is the K-means clustering project which was already implemented in nano degree on a smaller dataset. The K-means clustering shows great results in successfully classifying users into different clusters so I am looking forward to achieve similar results on the Full dataset. 
 
Evaluation Metrics
“Student proposes at least one evaluation metric that can be used to quantify the performance of both the benchmark model and the solution model presented. The evaluation metric(s) proposed are appropriate given the context of the data, the problem statement, and the intended solution.”

I will be using K-means clustering algorithm. There are several ways of choosing the number of clusters, k. We'll look at a simple one called "the elbow method". The elbow method works by plotting the ascending values of k versus the total error calculated using that k. Then. I will choose the K value that achieved the best results in the Full dataset to be implemented in the final solution which will build the output clusters.

For comparing my capstone’s model with the benchmark models, I will use F-beta score for comparing the results in both models. 

 
Project Design
“Student summarizes a theoretical workflow for approaching a solution given the problem. Discussion is made as to what strategies may be employed, what analysis of the data might be required, or which algorithms will be considered. The workflow and discussion provided align with the qualities of the project. Small visualizations, pseudocode, or diagrams are encouraged but not required.”
I will start by parsing the Full Movielense dataset. Then build a model using the K-means algorithm after deciding the best K value that achieve best results in terms of the Loss function “Using the elbow method.”. 
The current Full dataset is not very ready for such a project, so I will do extra steps in preparing the data and adjust the ratings/user to be ready for the clustering process. Then, I will start building the clusters using the adjusted K-means model. 
Finally, I will use the clusters to classify the new users against the different generated clusters and after clustering, I will use the knowledge in the same cluster to make recommendations. 
 

