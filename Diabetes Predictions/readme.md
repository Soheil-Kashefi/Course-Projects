Dataset Source -> [https://www.kaggle.com/datasets/saurabh00007/diabetescsv/data](https://www.kaggle.com/datasets/saurabh00007/diabetescsv/data)

# 🩺 Diabetes Detection using Logistic Regression

A machine learning project that predicts the likelihood of diabetes in patients based on diagnostic measurements using the Pima Indians Diabetes Database.

---

## 🚀 Project Overview

This project addresses the critical healthcare challenge of early diabetes detection. By analyzing medical diagnostic features such as glucose levels, BMI, and age, the system builds a predictive model to classify patients as diabetic or non-diabetic. The workflow utilizes the Pima Indians Diabetes dataset and implements a robust Logistic Regression pipeline including data standardization and stratified splitting to ensure reliable diagnostic predictions.

---

## 📊 Dataset Information

The analysis uses the Pima Indians Diabetes Database containing 768 records with the following diagnostic attributes:

### Medical Predictors

* **History**: Pregnancies (Number of times pregnant)
* **Metabolic**: Glucose (Plasma glucose concentration), Insulin (2-Hour serum insulin)
* **Vitals**: BloodPressure (Diastolic), SkinThickness (Triceps skin fold)
* **Physical**: BMI (Body mass index), Age (Years)
* **Genetics**: DiabetesPedigreeFunction (Diabetes pedigree function)

### Target Variable

* **Outcome**: Binary classification
* `0`: Non-diabetic (500 instances)
* `1`: Diabetic (268 instances)



---

## 🛠️ Technical Implementation

| Technology | Purpose |
| --- | --- |
| Python | Primary programming language |
| pandas | Data manipulation and CSV processing |
| scikit-learn | Model building, scaling, and splitting |
| matplotlib | Visualization and plotting |
| seaborn | Statistical graphics (Heatmaps, Countplots) |
| NumPy | Numerical computations |
| Jupyter Notebook | Interactive development environment |

---

## 🔍 Methodology

### Data Preprocessing

* **Exploratory Data Analysis (EDA)**: Analyzed class distribution (Countplot) and feature relationships (Correlation Heatmap).
* **Feature Selection**: Separated diagnostic features () from the target Outcome ().
* **Stratified Split**: Applied an 80/20 train-test split using `stratify=y` to maintain the ratio of diabetic/non-diabetic patients in both sets.
* **Feature Standardization**: Implemented `StandardScaler` to normalize feature variance, essential for Logistic Regression convergence.

### Model Development

* **Logistic Regression**: Selected for its efficiency in binary classification problems and probabilistic output.
* **Hyperparameter Tuning**: Increased `max_iter` to 1000 to ensure solver convergence on the standardized data.

### Inference System

* **New Patient Pipeline**: Created a workflow to load external CSV data (`new_patients_examples.csv`).
* **Probability Scoring**: configured the model to output both binary classifications and specific probability percentages for diabetes risk.

---

## 📈 Key Findings

### Model Performance

* **Test Accuracy**: Achieved an accuracy of **78.57%** on the unseen test set.
* **Convergence**: Successful model convergence achieved through proper feature scaling.

### Data Insights

* **Class Distribution**: The dataset is imbalanced (approx. 65% non-diabetic vs 35% diabetic), necessitating the use of stratified sampling during training.
* **Feature Correlation**: The correlation heatmap indicates relationships between variables, helping to understand which physiological factors (like Glucose and BMI) contribute most strongly to the diagnosis.

---

## 🧠 Machine Learning Pipeline

The project demonstrates a complete medical diagnostic ML workflow:

1. **Data Ingestion**: Loading and inspecting clinical data structure.
2. **EDA**: Visualizing correlations and outcome balance.
3. **Preprocessing**: Standardization (Z-score normalization) and Stratified Train-Test splitting.
4. **Model Training**: Fitting a Logistic Regression classifier.
5. **Evaluation**: Assessing performance via accuracy metrics.
6. **Prediction System**: Applying the trained scaler and model to new patient data for real-time diagnosis.