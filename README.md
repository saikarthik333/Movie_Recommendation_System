##Model performs the following:

1. **Data Loading and Preprocessing:** Loads movie and rating data, pivots the ratings data into a user-item matrix, and fills missing values with zeros.  It then filters the data to include only movies with at least 10 ratings and users with at least 50 ratings. This is visualized with scatter plots.

2. **Data Sparsity Calculation:**  Calculates and prints the sparsity of a sample matrix and converts the main ratings matrix to a Compressed Sparse Row (CSR) matrix.  CSR matrices are more efficient for storing and processing sparse data.

3. **Model Training (k-NN):** Trains a k-Nearest Neighbors model using cosine similarity on the CSR matrix. The model finds the nearest neighbors in the movie-rating space, which will later be used for recommendations.

4. **Recommendation Function:** Defines a function `get_movie_recommendation` that, given a movie title, finds similar movies based on the trained k-NN model. It returns a DataFrame of recommended movies, ranked by similarity.

5. **Example Recommendations:**  Calls the `get_movie_recommendation` function for "Iron Man" and "Iron Man 2" to demonstrate the system's functionality.


**In summary:** The code builds a movie recommendation system using collaborative filtering. It preprocesses the data to improve the quality of recommendations, uses a k-NN model to find similar movies, and provides a function to get recommendations for a given movie title.  The final output of the code are the two example recommendations for "Iron Man" and "Iron Man 2".  Note that the code does not evaluate the accuracy of the recommendations; it only demonstrates how to generate recommendations.
