# Video Game Recommender System

In this project I implemented various recommendation strategies to suggest video games to users based on their preferences and historical data. It involves exploratory data analysis, user-based and item-based collaborative filtering, content-based filtering, and TensorFlow-based neural network models.

---

## Dataset

Two CSV files were used:

- `steam.csv`: Metadata for thousands of games on Steam, including genres, tags, playtime, ratings, etc.
- `user_ratings.csv`: User-generated ratings for different games.

---

## Exploratory Data Analysis

- Checked for missing values and duplicates
- Filtered ratings to ensure values are between 1 and 5
- Plotted:
  - Top 10 rated games within a specific `appid` range
  - Distribution of games by genre (pie chart & bar chart)
  - Boxplot for user rating distribution
  - Correlation heatmap

---

## Recommendation Techniques

### 1. **User-Based Collaborative Filtering**

- Built a user-item matrix
- Used k-nearest neighbors with cosine similarity
- Recommended games based on similar users’ preferences

---

### 2. Item-Based Collaborative Filtering

- Built an item-user matrix  
- Used k-nearest neighbors with cosine similarity
- Recommended games similar to those the user rated highly  

---

### 3. Content-Based Filtering

- Combined game name and genres into a single text feature  
- Used TF-IDF Vectorizer to transform text data  
- Computed cosine similarity between games  
- Recommended games similar to the one specified  

---

### 4. Cold-Start Recommendations

- Designed for users with minimal or no prior ratings  
- Stored user preferences in a dictionary format  
- Used content-based filtering to recommend games based on manually entered ratings  

---

### 5. Neural Network-Based Model - TensorFlow

- Built a simple neural network recommender using TensorFlow  
- Trained on user and item embeddings  
- Predicted user ratings for unseen games  
- Used for personalized recommendations based on learned interactions  

---

## Libraries Used

- **pandas**
- **numpy**  
- **matplotlib** & **seaborn** for data visualization  
- **sklearn** for modeling (KNN, TF-IDF, cosine similarity)  
- **TensorFlow**
