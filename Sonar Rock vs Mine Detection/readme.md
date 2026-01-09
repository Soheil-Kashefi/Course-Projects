# ⚓ Sonar Rock vs. Mine Prediction

A machine learning project that detects underwater threats by classifying sonar return signals as either Naval Mines or Rocks.

[View Dataset on Kaggle](https://www.kaggle.com/datasets/rupakroy/sonarcsv/data)

---

## 🚀 Project Overview
This project addresses a critical safety challenge in maritime navigation and defense: automated object recognition using sonar data. By analyzing the energy returned from sonar chirps across various frequency bands, the model distinguishes between metal cylinders (mines) and cylindrical rocks. The goal is to build a robust classification system that minimizes false negatives—ensuring that dangerous mines are not mistaken for harmless rocks.

---

## 📊 Dataset Information
The dataset, originally collected by Gorman and Sejnowski, consists of 208 sonar return patterns:

### Features (60 Columns)
Each entry contains 60 numerical attributes. Each attribute represents the energy within a specific frequency band, integrated over a certain period of time.
- **Values**: Floating point numbers between 0.0 and 1.0.
- **Meaning**: Represents signal strength at increasing angles/frequencies.

### Target Labels
- **M**: Mine (Metal Cylinder)
- **R**: Rock (Rough Cylindrical Rock)

---

## 🛠️ Technical Implementation
| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data loading and manipulation |
| scikit-learn | Model training, scaling, and hyperparameter tuning |
| seaborn | Heatmaps and confusion matrix visualization |
| matplotlib | Plotting data distributions |
| NumPy | Numerical array processing |
| Jupyter Notebook | Interactive development environment |

---

## 🔍 Methodology

### Data Preprocessing
- **Exploratory Data Analysis (EDA)**: Visualized class balance and feature correlations using heatmaps to understand signal relationships.
- **Stratified Split**: Used `stratify=Y` during train-test splitting to maintain the ratio of Mines vs. Rocks in both datasets.
- **Feature Standardization**: Applied `StandardScaler` to normalize the 60 continuous features (Mean=0, Variance=1), which is critical for the performance of the SVM model.

### Model Optimization
- **Algorithm Selection**: Moved from basic Logistic Regression to **Support Vector Machines (SVM)** to better handle high-dimensional boundaries.
- **Hyperparameter Tuning**: Implemented `GridSearchCV` to automatically find the optimal values for:
    - **C**: Regularization parameter.
    - **Kernel**: Radial Basis Function (RBF) vs Polynomial.
    - **Gamma**: Kernel coefficient.

---

## 📈 Key Findings

### Model Performance
- **Accuracy Improvement**: The optimized SVM model significantly outperformed the baseline Logistic Regression model.
- **Generalization**: The model achieved high accuracy (~85-90%) on unseen test data, indicating distinct spectral signatures between metal and rock.

---

## 🧠 Machine Learning Pipeline
The project follows a professional end-to-end workflow:
1.  **Data Ingestion**: Loading raw sonar signal data.
2.  **Visualization**: Analyzing correlation matrices and class distribution.
3.  **Preprocessing**: Standardizing signal strengths to a common scale.
4.  **Training**: Fitting an SVM Classifier with Cross-Validation Grid Search.
5.  **Evaluation**: Generating Classification Reports and Confusion Matrices.
6.  **Deployment**: A reusable function for generating predictions on new sonar data files.