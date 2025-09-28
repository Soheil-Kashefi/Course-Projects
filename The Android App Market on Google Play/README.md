# 🤖 Android App Market Analysis
A data science project that performs a comprehensive analysis of the Google Play Store, comparing over ten thousand apps across different categories to find key insights for growth and retention strategies.

---

## 🚀 Project Overview
This project provides an in-depth look at the Android app market, focusing on over 10,000 apps from the Google Play Store. By analyzing two separate datasets—one with app details and another with user reviews—the project aims to uncover patterns and trends that can inform business strategies for app development and marketing. The analysis includes a focus on app categories, pricing, ratings, and a preliminary look at user sentiment.

---

## 📊 Dataset Information
The analysis uses two datasets to provide a complete picture of the app market.

### Core Data Sources
- **`apps.csv`**: Contains details for all applications on Google Play, with 13 features describing each app.
- **`user_reviews.csv`**: Contains 100 of the most helpful reviews for each app. The text has been pre-processed to include sentiment, sentiment polarity, and sentiment subjectivity.

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data loading, cleaning, and manipulation |
| plotly | Interactive data visualization |
| Jupyter Notebook | Development and analysis environment |

### Analysis Pipeline
1.  **Data Cleaning**: The raw data is cleaned by dropping duplicate app entries. Special characters like `+`, `,`, and `$` are removed from the `Installs` and `Price` columns to enable conversion to a numerical data type.
2.  **Type Conversion**: The `Installs` and `Price` columns are converted from `object` to `float` data types to allow for mathematical calculations and analysis.
3.  **Exploratory Data Analysis (EDA)**: The project explores the distribution of app categories in the market.
4.  **Data Visualization**: A bar chart is created to visualize the number of apps in each category.

---

## 📈 Key Insights & Results

### App Categories
The analysis reveals that there are **33 unique app categories** in the dataset. The `Family` and `Game` categories have the highest number of apps, indicating their dominance in the market. Other top categories include `Tools`, `Business`, and `Medical`.