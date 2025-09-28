# 🎮 The Golden Age of Video Games
An SQL-based data analysis project that explores video game sales and reviews from 1977 to 2020 to determine the golden age of gaming.

---

## 🚀 Project Overview
This project investigates whether the quality of video games has improved over time by analyzing a dataset of the top 400 best-selling games. Using SQL, the analysis compares game sales data with critic and user reviews to identify the years that had the highest-rated games, culminating in the discovery of the "golden age" of video games.

---

## 📊 Dataset Information
The analysis is performed on a database containing two tables.

### `game_sales`
| column | type | meaning |
|---|---|---|
| `game` | varchar | Name of the video game |
| `platform` | varchar | Gaming platform |
| `publisher` | varchar | Game publisher |
| `developer` | varchar | Game developer |
| `games_sold` | float | Number of copies sold (millions) |
| `year` | int | Release year |

### `reviews`
| column | type | meaning |
|---|---|---|
| `game` | varchar | Name of the video game |
| `critic_score` | float | Critic score from Metacritic |
| `user_score` | float | User score from Metacritic |

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| SQL | Primary language for data querying and analysis |
| PostgreSQL | Database management system |
| Jupyter Notebook | Development and analysis environment |

### Analysis Pipeline
1.  **Top Sellers**: Identify the ten best-selling video games of all time.
2.  **Data Quality Check**: Count how many games are missing review scores to understand data limitations.
3.  **Critics' Golden Age**: Find the years with the highest average critic scores, and validate these scores by counting the number of games released in those years.
4.  **Users' Golden Age**: Repeat the process to find the years with the highest average user scores.
5.  **Final Determination**: Identify the years that were loved by both critics and users, and then find which of those years also had the highest total sales volume.

---

## 📈 Key Insights & Results

### The Golden Age
The analysis concludes that the golden age of video games, defined as the years with both high average review scores and high sales, occurred in **1998, 2002, and 2008**.

### Top Selling Games
The top-selling games in the dataset span a wide range of years, from 1985 to 2017. `Wii Sports for Wii` from 2006 is the best-selling game in the dataset, with 82.90 million copies sold.

### Review Scores
A total of 31 games in the dataset have no review data. The year 1990 had the highest average critic score (9.80), but this was based on only a single game.