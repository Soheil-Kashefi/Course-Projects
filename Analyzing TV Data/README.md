# 📺 Super Bowl TV Viewership and Halftime Show Analysis
A comprehensive analysis of Super Bowl games, television viewership trends, and halftime show performances spanning over 50 years of data (1967-2018).

---

## 🚀 Project Overview
This project explores the relationship between game excitement, television viewership, and halftime show entertainment value across Super Bowl history. The analysis investigates whether close games drive higher viewership, how advertising costs have evolved with audience size, and examines the transformation of halftime shows from marching bands to major musical spectacles.

---

## 📊 Dataset Information
The analysis utilizes three scraped and polished Wikipedia datasets covering all 52 Super Bowls through 2018:

### super_bowls.csv
Game performance and outcome data with 18 variables including:
- **Game Details**: date, venue, city, state, attendance
- **Team Performance**: team_winner, team_loser, winning_pts, losing_pts, combined_pts, difference_pts
- **Personnel**: quarterbacks (qb_winner_1, qb_loser_1) and coaches for both teams

### tv.csv  
Television viewership and advertising metrics with 9 variables:
- **Viewership**: avg_us_viewers, total_us_viewers, rating_household, share_household
- **Demographics**: rating_18_49, share_18_49
- **Commercial**: ad_cost, network broadcasting details

### halftime_musicians.csv
Halftime show performer data with 3 variables:
- **Performance Details**: super_bowl, musician, num_songs

---

## 🛠️ Technical Implementation
| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data manipulation and merging datasets |
| matplotlib | Statistical visualization and plotting |
| seaborn | Advanced statistical graphics and regression analysis |
| Jupyter Notebook | Interactive development and analysis environment |

---

## 📈 Key Findings

### Game Competitiveness Analysis
- **Extreme Scores**: Identified highest-scoring games (74-75 points) featuring dominant QB performances
- **Lowest Scores**: Found defensive battles with scores as low as 21-23 points, often weather-affected
- **Closest Games**: Buffalo Bills vs New York Giants (1991) decided by 1 point with Scott Norwood's missed field goal
- **Biggest Blowouts**: 35+ point margins including Seattle's 43-8 demolition of Denver (2014)

### Viewership vs Game Excitement
- **Blowout Effect**: Regression analysis suggests viewers tend to abandon lopsided games
- **Statistical Relationship**: Downward sloping trend between point differential and household share ratings
- **Sample Limitation**: Weak correlation due to relatively small 52-game sample size

### Television and Advertising Evolution
- **Viewership Growth**: Steady increase in average US viewers over decades
- **Ad Cost Explosion**: 30-second spots reaching $5 million by 2018
- **Network Adaptation**: Ad costs lagged behind viewership growth, suggesting delayed market response

### Halftime Show Transformation
- **Pre-Jackson Era**: Dominated by marching bands, local performers, and variety acts
- **Michael Jackson Turning Point**: Super Bowl XXVII (1993) marked shift to major celebrity performers
- **Modern Spectacle**: Post-2000s featuring A-list artists like Beyoncé, Justin Timberlake, and Bruno Mars
- **Performance Analysis**: Most acts perform 1-3 songs; Justin Timberlake's 11-song 2018 performance was exceptional

### Performer Statistics
- **Most Appearances**: Grambling State University Tiger Marching Band (6 times)
- **Repeat Modern Performers**: Beyoncé, Justin Timberlake, Bruno Mars, and Nelly (2 appearances each)
- **Song Count Leaders**: Justin Timberlake (11), Diana Ross (10), Katy Perry (8)

---

## 🔍 Methodology

### Data Integration
- Merged game and TV datasets using Super Bowl number as key
- Filtered out Super Bowl I due to split network coverage
- Applied data cleaning for missing values in musician performance counts

### Statistical Analysis
- **Regression Modeling**: Used seaborn's regplot for viewership vs point differential analysis
- **Trend Analysis**: Multi-panel time series plots showing viewership, ratings, and ad cost evolution
- **Distribution Analysis**: Histograms for combined points and point differentials

### Data Filtering Techniques
- Excluded marching bands using string pattern matching ("Marching", "Spirit")
- Focused on post-Super Bowl XX data to address missing performance metrics
- Applied musician appearance counting and ranking algorithms