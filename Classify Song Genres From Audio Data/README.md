# 🎵 Music Genre Classification from Audio Features
A machine learning project that classifies songs as Hip-Hop or Rock using audio characteristics and spectral analysis data from The Echo Nest.

---

## 🚀 Project Overview
This project explores the challenge of automated music genre classification by analyzing raw audio features without actually listening to the songs. Using a dataset compiled by The Echo Nest research group, the analysis builds and compares machine learning models to distinguish between Hip-Hop and Rock tracks based on quantitative audio metrics like danceability, energy, and acousticness.

---

## 📊 Dataset Information
The project utilizes two complementary datasets covering 4,802 tracks with genre labels:

### fma-rock-vs-hiphop.csv
Track metadata and genre classifications
- **Genre Labels**: Binary classification (Hip-Hop vs Rock)
- **Track Identifiers**: Unique track_id for data merging

### echonest-metrics.json
Audio feature analysis with 8 spectral characteristics:
- **Rhythm**: danceability, tempo
- **Energy**: energy, acousticness, liveness
- **Vocal Content**: speechiness, instrumentalness
- **Mood**: valence (musical positivity)

All features are normalized on scales from -1 to 1 or 0 to 1 for consistent model input.

---

## 🛠️ Technical Implementation
| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data manipulation and JSON/CSV processing |
| scikit-learn | Machine learning pipeline and algorithms |
| matplotlib | Data visualization and plotting |
| NumPy | Numerical computations and array operations |
| Jupyter Notebook | Interactive development environment |

---

## 🔍 Methodology

### Data Preprocessing
- **Feature Correlation Analysis**: Generated correlation heatmap to identify redundant features
- **Data Integration**: Merged audio metrics with genre labels using track_id
- **Train-Test Split**: 75/25 split with random_state=10 for reproducibility
- **Feature Standardization**: Applied StandardScaler for zero mean and unit variance

### Dimensionality Reduction
- **Principal Component Analysis (PCA)**: Reduced 8 features to 6 components
- **Variance Retention**: 85% of dataset variance preserved with 6 components
- **Scree Plot Analysis**: Visualized explained variance ratios for component selection
- **Cumulative Variance**: Used 85% threshold for optimal dimensionality

### Model Development
- **Decision Tree Classifier**: Rule-based classification with interpretable decision paths
- **Logistic Regression**: Linear classification using logistic function probabilities
- **Cross-Validation**: 10-fold K-fold validation for robust performance assessment

---

## 📈 Key Findings

### Class Imbalance Impact
- **Initial Dataset**: Heavily skewed toward Rock (972 tracks) vs Hip-Hop (229 tracks)
- **Bias Effect**: Models achieved 81-89% accuracy but poor Hip-Hop classification
- **Rock Precision**: 90-91% due to dataset dominance
- **Hip-Hop Precision**: Only 51-78% showing significant bias

### Balanced Dataset Results
- **Sampling Strategy**: Randomly sampled Rock tracks to match Hip-Hop count
- **Improved Fairness**: Balanced precision between genres (75-83%)
- **Model Performance**: Logistic Regression outperformed Decision Tree
- **Cross-Validation Scores**: Decision Tree (72.2%), Logistic Regression (77.3%)

### Feature Importance Insights
- **Audio Characteristics**: 6 principal components captured essential genre-distinguishing features
- **Dimensionality Efficiency**: Reduced computational complexity while maintaining performance
- **Genre Separability**: Clear statistical differences between Hip-Hop and Rock audio profiles

---

## 🧠 Machine Learning Pipeline
The project demonstrates a complete ML workflow:
1. **Data Exploration**: Correlation analysis and feature relationship visualization
2. **Preprocessing**: Standardization and dimensionality reduction via PCA
3. **Model Training**: Implementation of both tree-based and linear classifiers
4. **Bias Detection**: Identification and correction of class imbalance issues
5. **Model Evaluation**: Comprehensive performance assessment using cross-validation
6. **Pipeline Integration**: Automated workflow combining preprocessing and classification