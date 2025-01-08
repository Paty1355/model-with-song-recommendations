# Music Recommendation System

This project performs an exploratory analysis of music data and creates a song recommendation model. The goal is to recommend songs to users based on different recommendation algorithms.

## Libraries and Tools Used:
- **Pandas**: Used for data analysis and manipulation.
- - **NumPy**: Package for numerical computing, used for handling arrays and performing mathematical operations efficiently.
- **Word2Vec**: Applied to encode the 'artist genres' column into vector representations.
- **Frequency Encoder**: A custom encoder used in conjunction with a `Pipeline` for preprocessing.
- **StandardScaler**: Used to scale the data for better performance with machine learning models.
- **KNN (K-Nearest Neighbors)**: A machine learning algorithm used for generating song recommendations.
- **Cosine Similarity**: Used as an alternative approach to finding song similarities.

## Data Preprocessing:
- The **'artist genres'** column is encoded using the **Word2Vec** model to transform the categorical genre data into numeric vector representations.
- The **Frequency Encoder** is used to encode other categorical variables, followed by the scaling of data using **StandardScaler** to improve the performance of machine learning models.
- - **ColumnTransformer**: Used to apply different preprocessing techniques (e.g., encoding text and scaling numerical features) to separate columns in the dataset.

## Hyperparameter Tuning:
- The number of **neighbors** for the KNN algorithm is tuned to optimize the model's performance.

## Functions:

1. **`recommend_songs_KNN(song_index=0)`**:
   - Recommends songs using the KNN algorithm based on a song's index.
   
2. **`recommend_songs_Cosine_Similarity(song_index=0)`**:
   - Recommends songs using cosine similarity between songs based on their feature vectors.
   
3. **`recommend_songs_KNN_and_Cosine_Similarity(song_index=0)`**:
   - Combines the KNN and cosine similarity approaches to generate song recommendations.

4. **`choose_best_recommendation_method(n)`**:
   - Evaluates and compares the performance of different recommendation methods to determine which provides the best results.



