# 💄 Comparing Cosmetics by Ingredients
A data science approach to cosmetic product recommendation using ingredient similarity analysis and machine learning visualization techniques.

---

## 🚀 Project Overview
This project develops a content-based recommendation system for cosmetic products by analyzing their chemical ingredient compositions. Using advanced dimensionality reduction and interactive visualization techniques, the system helps users discover similar products based on ingredient profiles rather than relying on marketing descriptions or brand preferences.

The analysis focuses specifically on moisturizers suitable for dry skin, creating an ingredient-based similarity map that reveals hidden relationships between products from different brands and price points.

---

## 📊 Dataset Information
The analysis uses Sephora cosmetics data containing 1,472 products with comprehensive ingredient and metadata information:

### Core Variables
- **Product Details**: Label, Brand, Name, Price, Rank (customer rating)
- **Ingredient Lists**: Complete chemical composition for each product
- **Skin Type Compatibility**: Binary indicators for Combination, Dry, Normal, Oily, Sensitive skin

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data manipulation and filtering |
| NumPy | Numerical computations and matrix operations |
| scikit-learn | t-SNE dimensionality reduction |
| Bokeh | Interactive data visualization |
| Jupyter Notebook | Development and analysis environment |

### Machine Learning Pipeline
1. **Text Processing**: Ingredient tokenization and normalization
2. **Feature Engineering**: One-hot encoding of ingredient presence/absence
3. **Dimensionality Reduction**: t-SNE transformation from 2,233D to 2D space
4. **Interactive Visualization**: Bokeh-powered scatter plot with hover tooltips

---

## 🧪 Methodology

### Data Preprocessing
- **Ingredient Tokenization**: Split comma-separated ingredient lists into individual components
- **Dictionary Creation**: Built comprehensive ingredient index (2,233 unique ingredients)
- **Binary Encoding**: Created sparse matrix representation of product-ingredient relationships

### Document-Term Matrix Construction
- **Matrix Size**: 190 products × 2,233 ingredients
- **Encoding Strategy**: Binary presence/absence (1 = ingredient present, 0 = absent)
- **Similarity Metric**: Cosine similarity based on shared ingredient profiles

### Dimensionality Reduction
- **Algorithm**: t-SNE (t-Distributed Stochastic Neighbor Embedding)
- **Parameters**: 2 components, learning rate 200, random state 42
- **Objective**: Preserve local neighborhood structure while enabling 2D visualization

---

## 📈 Key Insights

### Product Similarity Discovery
- **Spatial Clustering**: Products with similar ingredient profiles cluster together in 2D space
- **Cross-Brand Relationships**: Identified similar products across different brands and price points
- **Ingredient-Based Grouping**: Chemical composition creates more meaningful clusters than brand categorization

### Practical Applications
- **Cost-Effective Alternatives**: Found cheaper products with nearly identical ingredient profiles
- **Example Case Study**: 
  - AMOREPACIFIC Color Control Cushion ($60, rating 4.0)
  - LANEIGE BB Cushion Hydra Radiance ($38, rating 4.3)
  - **Result**: 37% cost savings with higher customer satisfaction

### Recommendation Engine Performance
- **Distance-Based Similarity**: Closer points indicate more similar ingredient compositions
- **Interactive Exploration**: Hover functionality reveals product details for easy comparison
- **Visual Pattern Recognition**: Users can identify ingredient-based clusters without chemistry knowledge