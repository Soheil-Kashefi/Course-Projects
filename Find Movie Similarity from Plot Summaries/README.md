# 🎬 Finding Movie Similarity from Plot Summaries
A content-based recommendation system that finds similar movies by analyzing the semantic content of their plot summaries using TF-IDF vectorization and cosine similarity.

---

## 🚀 Project Overview
This project develops a recommendation engine that suggests movies based on their plot summaries. Unlike systems that rely on user ratings or genre tags, this approach analyzes the textual content of movie plots to identify hidden relationships and provide recommendations for films with similar narratives. The analysis uses text processing and a powerful similarity metric to create a simple yet effective recommendation system.

---

## 📊 Dataset Information
The analysis uses a comprehensive dataset of movie plot summaries sourced from IMDb and Wikipedia.

### Core Variables
- **Title**: The title of the movie
- **Genre**: The genre(s) associated with the movie
- **Plot Summary**: A detailed summary of the movie's plot

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data loading and manipulation |
| nltk | Natural language processing (removing stop words) |
| scikit-learn | TF-IDF vectorization and cosine similarity calculation |
| Jupyter Notebook | Development and analysis environment |

### Machine Learning Pipeline
1. **Data Preprocessing**: Load the movie dataset, filter out missing plot summaries, and select movies of a specific genre for analysis.
2. **Text Processing**: Clean the plot summaries by removing common English stop words.
3. **Feature Extraction**: Use **TF-IDF (Term Frequency-Inverse Document Frequency)** to convert the plot summaries into a numerical matrix, where each movie is represented by a vector of keyword importance scores.
4. **Similarity Measurement**: Compute the **cosine similarity** between all movie vectors to quantify the narrative similarity between any two films.
5. **Recommendation Engine**: Develop a function that takes a movie title and returns the 10 most similar movies based on the calculated cosine similarity scores.

---

## 📈 Key Insights & Results

### Narrative-Based Recommendations
- **Semantic Similarity**: By analyzing plot summaries, the system can recommend movies that share similar narrative structures or themes, even if they belong to different sub-genres or have different ratings.
- **Example Case Study**: The system successfully identifies movies with similar plots, such as recommending superhero-themed films for "The Dark Knight Rises" and animated adventure stories for "The Lion King."
- **Content-Based Clustering**: The project demonstrates how text data can be used to group and recommend items based on their intrinsic content, providing a valuable alternative to traditional collaborative filtering methods.