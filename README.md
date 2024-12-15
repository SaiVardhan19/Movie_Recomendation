# Movie Recommendation System Using Clustering and Cosine Similarity

![image](https://github.com/user-attachments/assets/745b1119-b3dd-4f0c-b865-fd71de3fe22c)





## **1. Project Overview**
This project aims to develop a **Movie Recommendation System** that suggests movies to users based on their preferences. The system takes user inputs such as **genre, type (movie or TV show), rating, or a combination of these features** and recommends similar movies from the dataset. To achieve this, we use **clustering techniques and cosine similarity** to group similar movies and identify recommendations.

The key goal is to help users discover movies that match their tastes using a blend of **machine learning, unsupervised clustering, and similarity analysis**.

---

## **2. Problem Statement**
Users often struggle to find movies that match their preferences, especially with the overwhelming number of options available. This project provides a way to recommend movies similar to those the user likes by utilizing the following features from a movie dataset:

- **Title**: Unique identifier for each movie/TV show.
- **Type**: Specifies whether the entry is a movie or a TV show.
- **Genre**: Indicates the category of the movie (Action, Drama, Comedy, etc.).
- **Release Year**: The year in which the movie or show was released.
- **Rating**: Specifies the content rating (G, PG, PG-13, R, etc.).
- **Duration**: The length of the movie in minutes or the number of seasons for TV shows.
- **Country**: The country where the movie or show was produced.

The system allows users to input one or more of these features to receive personalized recommendations.

---

## **3. Objectives**
- **Input Flexibility**: Allow users to provide any combination of filters (Genre, Type, Rating) and receive movie recommendations accordingly.
- **Unsupervised Learning**: Use clustering techniques to group similar movies.
- **Similarity Measure**: Implement **cosine similarity** to identify and rank the most similar movies.
- **Dynamic Recommendations**: Ensure recommendations are updated as user preferences change.

---

## **4. Methodology**
To achieve the objectives, the following approach is used:

1. **Data Preprocessing**:
   - Handle missing values, if any, and encode categorical features using **Label Encoding**.
   - Normalize the data so that the clustering algorithm works effectively.

2. **Clustering**:
   - Use **K-means Clustering** to group similar movies together.
   - Each cluster represents a group of similar movies based on Genre, Type, Rating, and other features.

3. **Feature Representation**:
   - **Label Encoding** is used to convert categorical variables like Genre, Rating, and Type into numerical values.
   - **Feature Vectors** are created for each movie, and cosine similarity is calculated for recommendations.

4. **Recommendation System**:
   - For a given user query (like **Genre = Comedy, Type = Movie, Rating = PG**), filter movies from the same cluster.
   - Use **Cosine Similarity** to rank the movies based on similarity to the user’s input.

5. **User Interaction**:
   - The system accepts user inputs for Genre, Type, and Rating.
   - The system returns the top N most similar movies.

---

## **5. Key Concepts**

### **1. Clustering**
- **Definition**: Clustering is an unsupervised learning technique where similar data points are grouped into clusters.
- **Purpose**: It helps identify groups of similar movies.
- **Algorithm Used**: **K-means Clustering**, which minimizes the distance between points and their assigned cluster centroids.

### **2. Label Encoding**
- **Definition**: Label Encoding converts categorical variables (like Genre, Type, and Rating) into numerical values.
- **Purpose**: Machine learning algorithms work on numerical data, so this step is essential.

### **3. Cosine Similarity**
- **Definition**: Measures the cosine of the angle between two vectors in an n-dimensional space.
- **Formula**:
  
  cos x= (A.B)/(||A||*||B||)
  
  - Where A and B are vectors, and ||A|| and ||B||| are the magnitudes of the vectors.
- **Purpose**: Helps identify how similar two movies are, regardless of the magnitude of the features.

---

## **6. Tools and Libraries**
The following tools and libraries are used in this project:

- **Python**: The programming language used for the project.
- **NumPy**: For numerical operations and vector manipulations.
- **Pandas**: To manage and preprocess the dataset.
- **Scikit-Learn**: For clustering (K-means), Label Encoding, and cosine similarity calculations.
- **Matplotlib/Seaborn**: For visualizing data and clusters.

---

## **7. Results and Evaluation**
- After clustering the movies and calculating cosine similarities, users receive a list of movies similar to their input criteria.
- Recommendations are evaluated by observing how well the system matches user preferences.

---

## **8. Challenges and Limitations**
- **Cold Start Problem**: Users with no prior preferences may receive less accurate recommendations.
- **Choice of Clusters (K)**: Choosing the number of clusters (K) affects system accuracy.
- **Feature Weights**: The importance of features may vary, which can affect recommendations.

---

## **9. Conclusion**
This project demonstrates how **unsupervised clustering** and **cosine similarity** can be used to build an effective movie recommendation system. Using machine learning and mathematical similarity measures, we can recommend movies that match the user's preferences.

The flexible system allows users to filter movies based on one or more features, making it a versatile recommendation tool. Future work can focus on personalized recommendations and the inclusion of more user-specific inputs.

