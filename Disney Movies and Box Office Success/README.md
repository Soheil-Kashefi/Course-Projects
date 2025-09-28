# 🎬 Disney Movies Box Office Success Analysis
A statistical analysis of Walt Disney Studios' film performance spanning over 80 years, investigating genre trends and predicting box office success factors.

---

## 🚀 Project Overview
This project analyzes the box office performance of 579 Disney movies from 1937 to 2016, examining how different genres have evolved in popularity and financial success over time. Using statistical modeling and bootstrap confidence intervals, the analysis identifies which movie genres are most likely to generate higher box office revenues, providing data-driven insights for Disney's future production strategy.

The study focuses on understanding the relationship between movie genres and inflation-adjusted box office gross, ultimately answering whether Disney should prioritize action and adventure films in their upcoming releases.

---

## 📊 Dataset Information
The analysis uses Disney movie data compiled by Kelly Garrett, containing comprehensive box office and metadata information:

### Core Variables
- **Movie Details**: Title, release date, genre classification, MPAA rating
- **Financial Metrics**: Total gross revenue, inflation-adjusted gross revenue
- **Temporal Span**: 1937-2016 (80 years of Disney film history)
- **Genre Categories**: 12 distinct genres including Action, Adventure, Musical, Comedy, Drama

### Key Statistics
- **Total Movies**: 579 Disney productions
- **Time Range**: 1937 (Snow White) to 2016
- **Top Performer**: Snow White and the Seven Dwarfs ($5.2B inflation-adjusted)
- **Genre Distribution**: Adventure, Musical, and Comedy as primary categories

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data manipulation and temporal analysis |
| NumPy | Statistical computations and bootstrap sampling |
| seaborn | Statistical data visualization |
| scikit-learn | Linear regression modeling |
| Jupyter Notebook | Interactive analysis environment |

### Statistical Methods
1. **Temporal Analysis**: Year-over-year genre performance tracking
2. **One-Hot Encoding**: Categorical variable transformation for regression
3. **Linear Regression**: Genre impact quantification on box office success
4. **Bootstrap Confidence Intervals**: Statistical significance testing (500 replicates)

---

## 📈 Key Findings

### Historical Performance Leaders
- **All-Time Champion**: Snow White and the Seven Dwarfs ($5.2B inflation-adjusted)
- **Top 10 Dominance**: Classic animated films occupy 8 of 10 positions
- **Modern Entries**: Star Wars: The Force Awakens represents contemporary success

### Genre Trend Analysis
- **Rising Stars**: Action and Adventure genres show strongest growth trajectories
- **Consistent Performers**: Musical and Comedy maintain steady popularity
- **Market Evolution**: Clear shift toward action-oriented content in recent decades

### Statistical Modeling Results
- **Action Genre Baseline**: $102.9M average inflation-adjusted gross
- **Adventure Premium**: Additional $87.5M boost over action baseline
- **Statistical Significance**: 95% confidence intervals exclude zero for both genres
- **Model Validation**: Bootstrap analysis confirms robust relationship (500 iterations)

---

## 🔬 Methodology

### Data Preprocessing
- **Temporal Extraction**: Year extraction from release dates for trend analysis
- **Genre Aggregation**: Mean gross calculation by genre and year
- **Categorical Encoding**: One-hot encoding with Action as baseline category

### Visualization Strategy
- **Line Plot Analysis**: Multi-genre performance trends over time using seaborn
- **Statistical Comparison**: Visual identification of fastest-growing genres
- **Trend Validation**: Graphical support for regression modeling approach

### Bootstrap Confidence Intervals
- **Sample Size**: 500 bootstrap replicates for robust estimation
- **Methodology**: Pairs bootstrap maintaining genre-gross relationships
- **Confidence Level**: 95% intervals for intercept and coefficient estimation
- **Validation**: Statistical significance testing for genre effects