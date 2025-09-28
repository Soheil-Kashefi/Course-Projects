# 🩸 Predicting Blood Donations
A data science project to forecast future blood supply by predicting donor behavior using the RFMTC marketing model and machine learning classification.

---

## 🚀 Project Overview
This project focuses on building a predictive model to identify which donors are most likely to give blood in the future. The analysis uses a dataset from a mobile blood donation vehicle in Taiwan, where donor behavior is captured by the **RFMTC** (Recency, Frequency, Monetary, Time, and a binary classification target) marketing model. The goal is to develop a robust binary classifier that can assist the Blood Transfusion Service Center in managing and forecasting their blood supply.

---

## 📊 Dataset Information
The analysis uses the `transfusion.data` file, a dataset containing 748 records of blood donations in Taiwan. The data is structured around the RFMTC model, with five key variables:

### Core Variables
- **Recency**: Months since the last donation
- **Frequency**: Total number of donations
- **Monetary**: Total blood donated (in c.c.)
- **Time**: Months since the first donation
- **Target**: A binary variable indicating whether the donor gave blood in March 2007 (1 = yes, 0 = no)

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data loading and manipulation |
| NumPy | Numerical computations, log normalization |
| scikit-learn | Data splitting, logistic regression, AUC score evaluation |
| TPOT | Automated machine learning (AutoML) for model selection |
| Jupyter Notebook | Development and analysis environment |

### Machine Learning Pipeline
1. **Data Preprocessing**: Renaming the target column and analyzing class imbalance.
2. **Data Splitting**: Stratified `train_test_split` to maintain target incidence.
3. **Automated Model Selection**: TPOT finds the optimal pipeline, identifying `LogisticRegression` as the best model.
4. **Feature Normalization**: Log transformation to correct for high variance in the 'Monetary' feature.
5. **Model Training & Evaluation**: Training a final logistic regression model on normalized data and evaluating its performance with the AUC score.

---

## 📈 Key Insights & Results

### Model Performance Improvement
- **Baseline Model (TPOT)**: The automated search with TPOT yielded a `LogisticRegression` model with a baseline **AUC score of 0.7850**.
- **Variance Correction**: The `Monetary` feature had a variance of over 2 million, orders of magnitude higher than other features. Log normalization was applied to correct this imbalance.
- **Final Model**: Training a logistic regression model on the normalized data resulted in an improved **AUC score of 0.7891**, a 0.5% increase in performance.

### Practical Implications
- **Actionable Insights**: An accurate predictive model allows the Blood Transfusion Service Center to better target donors, ensuring a stable blood supply and potentially saving more lives.
- **Model Interpretability**: The use of a simple `LogisticRegression` model makes it easy to interpret how each feature (Recency, Frequency, etc.) contributes to the prediction.