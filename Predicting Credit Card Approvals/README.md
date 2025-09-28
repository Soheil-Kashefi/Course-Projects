# 💳 Predicting Credit Card Approvals
An automated credit card approval predictor using a machine learning pipeline that handles missing values, preprocesses data, and evaluates a logistic regression model.

---

## 🚀 Project Overview
This project builds a machine learning model to automate the credit card application approval process. It uses a confidential dataset from the UCI Machine Learning Repository where features are anonymized. The pipeline covers essential data science steps, including data preprocessing, feature engineering, and model evaluation, to create an efficient and accurate predictor.

---

## 📊 Dataset Information
The analysis uses the Credit Card Approval dataset. The data contains a mix of numerical and non-numerical features, along with missing entries represented by '?'. The features have been anonymized to protect privacy.

### Core Variables
The dataset includes several features related to a person's financial and personal information, such as:
- **`Gender`**
- **`Age`**
- **`Debt`**
- **`YearsEmployed`**
- **`CreditScore`**
- **`Income`**
- **`ApprovalStatus`**: The target variable

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data loading, manipulation, and one-hot encoding |
| NumPy | Numerical computations and handling missing values |
| scikit-learn | Data splitting, feature scaling, model training, and evaluation |
| Jupyter Notebook | Development and analysis environment |

### Machine Learning Pipeline
1.  **Data Preprocessing**: Missing values ('?') are replaced with **NaN**. Numerical missing values are imputed with the mean, while non-numeric values are imputed with the most frequent value.
2.  **Feature Selection**: Unimportant features like `DriversLicense` and `ZipCode` are dropped.
3.  **Encoding and Scaling**: Categorical features are converted to numeric using **one-hot encoding** (`pd.get_dummies()`). All features are then scaled to a uniform range of 0-1 using `MinMaxScaler`.
4.  **Model Training**: A **Logistic Regression** classifier is trained on the preprocessed data.
5.  **Hyperparameter Tuning**: **GridSearchCV** is used to find the optimal hyperparameters for the logistic regression model, improving its performance.

---

## 📈 Key Insights & Results

### Model Performance
- The initial model showed a low accuracy score of 54.8% and failed to correctly predict any of the 'Denied' applications.
- After performing a grid search and finding the best parameters, the model's performance significantly improved.
- The best performing model achieved an accuracy of **69.48%**.

### Practical Applications
This project demonstrates how a robust machine learning pipeline can be used to automate a time-consuming and error-prone process. The final model provides a good foundation for predicting credit card approvals, which can be further optimized with more advanced techniques.