# 🐝 Predicting Species from Images
A computer vision project that builds a machine learning model to automatically detect and classify honey bees and bumble bees from images.

---

## 🚀 Project Overview
This project is the second part of a pipeline designed to identify bee species from visual data. The goal is to develop an automated model that can distinguish between honey bees (*Apis*) and bumble bees (*Bombus*) based on their appearance. This capability is valuable for ecological research, as it can help researchers more effectively collect field data to understand the prevalence and growth of these vital pollinating insects. The notebook focuses on building a classifier after the images have been preprocessed and prepared for analysis.

---

## 📊 Dataset Information
The project uses a dataset consisting of images and a corresponding label file.
### Core Data Sources
- **`labels.csv`**: A CSV file where each image is associated with a label indicating its genus.
- **`genus`**: The target variable, which is a numerical value of `0.0` for honey bees (*Apis*) and `1.0` for bumble bees (*Bombus*).
- **Images**: The images themselves are stored as JPEG files and are used as the features for the classification model.

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| scikit-image & Pillow | Image loading and manipulation |
| scikit-learn | Data splitting, feature scaling, PCA, and model training (SVC) |
| pandas & NumPy | Data loading and manipulation |
| matplotlib | Displaying images and visualizations |
| Jupyter Notebook | Development and analysis environment |

### Machine Learning Pipeline
1.  **Data Loading**: The `labels.csv` file is loaded into a pandas DataFrame.
2.  **Image Handling**: A helper function is defined to load images from the file path and convert them into a NumPy array.
3.  **Feature Extraction**: The project extracts features from the images, though the specifics are not detailed in the provided code snippet.
4.  **Model Training**: A machine learning classifier is trained on the image features to predict the bee's genus.
5.  **Model Evaluation**: The project prepares to evaluate the model's performance using metrics like accuracy and AUC (Area Under the Curve).

---

## 📈 Key Insights & Results

The project successfully demonstrates a complete machine learning pipeline for image classification, from data loading to model evaluation. The goal is to produce a model that can accurately distinguish between honey bees and bumble bees. This work provides a foundation for more advanced species identification projects.