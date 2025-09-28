# 🎶 Name Game: Gender Prediction Using Sound
A data science project that uses phonetic algorithms to predict the gender of authors from their names, with a case study on best-selling children's book authors from the New York Times.

---

## 🚀 Project Overview
This project tackles the challenge of identifying and analyzing names that sound the same but have different spellings. It uses the **New York Soundex (NYSIIS)** phonetic algorithm to convert names into a phonetic representation, allowing for robust name matching. The technique is applied to a dataset of best-selling authors to determine the gender distribution and observe how it has changed over time.

---

## 📊 Dataset Information
The analysis uses two key datasets to perform the gender prediction:

### New York Times Best-Selling Authors (2008-2017)
A CSV file (`nytkids_yearly.csv`) containing records of best-selling children's picture book authors.
- **`Year`**: The year the book was a bestseller
- **`Book Title`**: The title of the book
- **`Author`**: The author's full name

### Baby Names by Sound (NYSIIS)
A CSV file (`babynames_nysiis.csv`) derived from US Social Security Administration data, containing a list of unique names with their phonetic equivalent and gender distribution.
- **`babynysiis`**: The NYSIIS-coded phonetic name
- **`perc_female`**: The percentage of times the name appeared as female
- **`perc_male`**: The percentage of times the name appeared as male

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| fuzzy | NYSIIS phonetic algorithm for name matching |
| pandas | Data loading, manipulation, and merging |
| NumPy | Array manipulation and unique value counting |
| matplotlib | Data visualization (bar charts) |
| Jupyter Notebook | Development and analysis environment |

### Analysis Pipeline
1.  **Name Extraction**: The first name of each author is extracted from the `Author` column.
2.  **Phonetic Encoding**: The `fuzzy.nysiis()` function is used to create a phonetic equivalent for each author's first name.
3.  **Gender Classification**: The phonetic author names are matched against the `babynames_nysiis.csv` dataset. Based on the `perc_female` and `perc_male` columns, a gender (`F`, `M`, or `N` for neutral) is assigned to each author.
4.  **Trend Analysis**: The number of male, female, and "unknown" genders (names without a match in the Social Security dataset) are counted for each year.
5.  **Data Visualization**: A bar chart is created to visualize the yearly trend of authors with "unknown" genders.

---

## 📈 Key Insights & Results

### Gender Distribution
The analysis reveals that between 2008 and 2017, there were significantly more female authors (395) on the New York Times Children's Picture Book best-seller list than male authors (191).

### Unknown Genders
A notable number of authors have an "unknown" gender classification. This is hypothesized to be due to these authors being foreign-born, as the `babynames_nysiis.csv` dataset is based on US Social Security records. The project includes a visualization of the trend of these unknown genders over the years.