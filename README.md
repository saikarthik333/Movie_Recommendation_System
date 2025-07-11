# 🎬 Movie Recommendation System (Collaborative Filtering with k-NN)

This project is a **Collaborative Filtering-based Movie Recommendation System** built using the **k-Nearest Neighbors (k-NN)** algorithm with **cosine similarity**. It suggests movies based on user preferences derived from historical movie ratings.

---

## 📌 Features

- ✅ Predicts similar movies based on user behavior and rating patterns
- ✅ Uses k-NN algorithm with cosine similarity to measure movie similarity
- ✅ Optimized with Compressed Sparse Row (CSR) matrix for large-scale data
- ✅ Filters noisy data by removing low-interaction users and unpopular movies
- ✅ Provides top 10 movie recommendations in under 1 second
- ✅ Data visualization of user/movie engagement

---

## 🧠 Algorithms & Techniques

- **Collaborative Filtering** using **Item-Item Similarity**
- **k-Nearest Neighbors (k-NN)** with `cosine` distance metric
- **Data Sparsity Reduction** (filtering movies with <10 ratings and users with <50 ratings)
- **CSR Matrix** for efficient sparse data representation
- **Exploratory Data Analysis** using scatter plots and rating distributions

---

## 📂 Dataset

This project uses the [MovieLens dataset](https://grouplens.org/datasets/movielens/), consisting of:

- `movies.csv` – Movie metadata like titles and genres  
- `ratings.csv` – User ratings of movies (userId, movieId, rating, timestamp)

---

## 🛠️ Libraries Used

- `pandas`, `numpy` – Data handling and preprocessing  
- `scikit-learn` – k-NN model, cosine similarity, sparse matrix tools  
- `matplotlib`, `seaborn` – Data visualization  
- `scipy.sparse` – Efficient sparse matrix representation  

---

## 🧪 How It Works

1. **Load & Merge Data**  
   Movie and rating data are loaded, with missing values filled and unneeded columns removed.

2. **Create User-Movie Matrix**  
   A pivot table (movies × users) is created with ratings as values and missing ratings filled as 0.

3. **Filter Sparse Data**  
   - Movies rated by fewer than 10 users are removed  
   - Users who rated fewer than 50 movies are filtered out

4. **Optimize Data Structure**  
   The matrix is converted into a **CSR matrix** to reduce memory usage and improve computation time.

5. **Train k-NN Model**  
   Using `NearestNeighbors` with cosine similarity to find similar movies.

6. **Make Recommendations**  
   The function `get_movie_recommendation('Movie Name')` returns the top 10 most similar movies based on cosine distance.

---

## 📊 Example Usage

```python
get_movie_recommendation('Iron Man')
get_movie_recommendation('Iron Man 2')
