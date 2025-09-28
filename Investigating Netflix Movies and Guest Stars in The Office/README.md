# 📺 Investigating Netflix Movies and The Office
A two-part data analysis project exploring trends in Netflix movie durations and the correlation between guest star appearances and IMDb ratings for episodes of *The Office*.

---

## 🚀 Project Overview
This repository contains a dual analysis aimed at answering two distinct questions:
1.  **Netflix Movie Trends**: What are the typical runtimes for movies on Netflix, and are there notable outliers?
2.  **The Office Ratings**: Do guest star appearances in episodes of *The Office* have a visible impact on their IMDb ratings?

The project uses foundational data manipulation and visualization techniques to uncover insights from two different datasets, showcasing how data science can be applied to popular culture.

---

## 📊 Dataset Information
This analysis uses two separate datasets:

### Netflix Titles
A CSV file containing metadata for movies and TV shows available on Netflix.
- **`type`**: The category of the title (e.g., 'Movie', 'TV Show')
- **`title`**: The name of the movie or show
- **`duration`**: The runtime of the movie in minutes

### The Office Guest Stars
A CSV file listing episodes of *The Office* with boolean flags for guest star appearances and their corresponding IMDb ratings.
- **`episode_number`**: The episode's sequential number
- **`imdb_rating`**: The episode's rating on IMDb
- **`guest_star_appearance`**: A boolean (True/False) indicating a guest star's presence

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data loading, filtering, and merging |
| matplotlib | Data plotting |
| seaborn | Advanced statistical data visualization |
| Jupyter Notebook | Development and analysis environment |

### Analysis Pipeline
1.  **Data Filtering**: Filter the Netflix dataset to include only movies and clean the duration column.
2.  **Data Merging**: Join the guest star data with the episode ratings to create a single, unified dataset for analysis.
3.  **Visualization**: Use scatter plots to visualize the data, color-coding points to highlight the presence of guest stars.

---

## 📈 Key Insights & Results

### Netflix Movie Durations
The analysis revealed that the majority of Netflix movies have a runtime between 75 and 100 minutes. The scatter plot visualization highlights this concentration, with a few outliers representing short-form films and documentaries.

### The Office Guest Stars
The scatter plot of episode ratings vs. episode number, with guest-star episodes color-coded, suggests a **positive correlation**. Episodes featuring guest stars tend to cluster at the top of the plot, indicating a visual link between their appearances and higher IMDb ratings.