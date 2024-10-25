# Movie Recommendation System Using Machine Learning
Recommendation systems are becoming increasingly important in today’s extremely busy world. People are always short on time with the myriad tasks they need to accomplish in the limited 24 hours. Therefore, the recommendation systems are important as they help them make the right choices, without having to expend their cognitive resources.

The purpose of a recommendation system basically is to search for content that would be interesting to an individual. Moreover, it involves a number of factors to create personalised lists of useful and interesting content specific to each user/individual. Recommendation systems are Artificial Intelligence based algorithms that skim through all possible options and create a customized list of items that are interesting and relevant to an individual. These results are based on their profile, search/browsing history, what other people with similar traits/demographics are watching, and how likely are you to watch those movies. This is achieved through predictive modeling and heuristics with the data available. 

# Types of Recommendation System :
1.Content-based systems:
which use characteristic information and takes item attriubutes into consideration .
Twitter , Youtube .
User specific actions or similar items reccomendation .
It will create a vector of it .
These systems make recommendations using a user's item and profile features. They hypothesize that if a user was interested in an item in the past, they will once again be interested in it in the future
One issue that arises is making obvious recommendations because of excessive specialization (user A is only interested in categories B, C, and D, and the system is not able to recommend items outside those categories, even though they could be interesting to them).

2.Collaborative Based :
Collaborative filtering systems, which are based on user-item interactions.
Clusters of users with same ratings , similar users .
Book recommendation , so use cluster mechanism .
We take only one parameter , ratings or comments .
In short, collaborative filtering systems are based on the assumption that if a user likes item A and another user likes the same item A as well as another item, item B, the first user could also be interested in the second item .
Issues are :User-Item nXn matrix , so computationally expensive .Only famous items will get recomended .New items might not get reccomended at all .

3.Hybrid Based :
Hybrid systems, which combine both types of information with the aim of avoiding problems that are generated when working with just one kind.
Combination of both and used now a days .
Uses : word2vec , embedding .
# About this project:
 This is a hybrid recommendation model. By combining content-based filtering with classification techniques and hyperparameter tuning, it leverages multiple methods to improve recommendation accuracy and personalization
Data Loading:It begins by loading a CSV file containing movie data  and displays the first few rows to give an initial look at the dataset structure.
Title Preprocessing:

A clean_title function is created to remove special characters from movie titles, keeping only alphanumeric characters. This step standardizes titles, making them suitable for text analysis.
The cleaned titles are stored in a new column called clean_title for use in further processing.
Text Vectorization Using TF-IDF:

The notebook utilizes the TfidfVectorizer from scikit-learn to convert cleaned movie titles into numerical vectors using the TF-IDF (Term Frequency-Inverse Document Frequency) method. This transformation captures the importance of words within each title and is crucial for identifying textual similarity.
Similarity Search Function:

A search function is defined, taking a user-input movie title, transforming it into a TF-IDF vector, and calculating its cosine similarity with other movie titles in the dataset.
Using cosine_similarity, the function ranks movies based on similarity to the input title and outputs the top recommendations.
Interactive Widgets for User Input:

Through ipywidgets, the notebook includes a text box where users can type a movie title.
An on_type function captures each keystroke, triggering real-time recommendations that dynamically update as the user types.



A classification algorithm is introduced to categorize movies based on their features. The dataset is divided into training and testing sets, and model performance is evaluated to assess prediction accuracy.

Hyperparameter tuning is performed to optimize the classification model, enhancing its accuracy and robustness in making predictions.


Finally, this project provides a summary of results, interpreting the model’s predictions to offer insights into its recommendation accuracy.
# Demo:
![1](https://github.com/pyla-prathibha/Movie_Recommendation_System/blob/main/Movie%20Recommendation1.png)

![2](https://github.com/pyla-prathibha/Movie_Recommendation_System/blob/main/Movie%20Recommendation%202.png)



