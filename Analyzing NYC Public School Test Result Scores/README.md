# 📚 NYC Public School SAT Test Results Analysis

A comprehensive SQL-based analysis of SAT performance across New York City's public high schools, examining academic achievement patterns by school and borough.

---

## 🚀 Project Overview

This project analyzes SAT test performance data from NYC public schools to identify top-performing institutions and understand educational achievement patterns across the five boroughs. The analysis focuses on math, reading, and writing scores while examining data quality and school distribution patterns.

---

## 📊 Dataset Information

**Single Table**: `schools`

| Column | Type | Description |
|--------|------|-------------|
| `school_name` | varchar | Name of school |
| `borough` | varchar | Borough location (Manhattan, Brooklyn, Queens, Bronx, Staten Island) |
| `building_code` | varchar | Unique building identifier |
| `average_math` | int | Average SAT math score (0-800) |
| `average_reading` | int | Average SAT reading score (0-800) |
| `average_writing` | int | Average SAT writing score (0-800) |
| `percent_tested` | numeric | Percentage of students who took the SAT |

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| **SQL** | Primary query language |
| **PostgreSQL** | Database management system |
| **Jupyter Notebook** | Interactive development environment |
| **%%sql magic** | SQL execution within notebook cells |

---

## 📈 Key Findings

### **Elite Math Performance**
- Only **10 schools** (2.7%) achieved math scores ≥640 (80% threshold)
- **Stuyvesant High School** leads with 754/800 in math
- Science and technology-focused schools dominate top rankings

### **Performance Extremes**
- **Highest Total SAT**: Stuyvesant High School (2,144/2,400)
- **Lowest Reading Score**: 302/800 (anonymous for privacy)
- **Top Writing School**: Stuyvesant High School (693/800)

### **Borough Rankings by Average SAT**
1. **Staten Island**: 1,439 (10 schools)
2. **Queens**: 1,345 (69 schools)
3. **Manhattan**: 1,340 (89 schools)
4. **Brooklyn**: 1,230 (109 schools)
5. **Bronx**: 1,202 (98 schools)

### **Brooklyn's Top Math Schools**
1. Brooklyn Technical High School (682)
2. Brooklyn Latin School (625)
3. Leon M. Goldstein High School for the Sciences (563)
4. Millennium Brooklyn High School (553)
5. Midwood High School (550)

---

## 📁 Project Structure

```
SQL-Analyzing-NYC-Public-School-Test-Results/
├── README.md                                    # Project documentation
├── nyc_schools_analysis.ipynb                   # SQL analysis notebook
└── schools_modified.csv                         # Dataset
```