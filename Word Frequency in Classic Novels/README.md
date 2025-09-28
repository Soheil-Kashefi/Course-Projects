# 📖 Word Frequency in Classic Novels
A natural language processing project that scrapes the text of Herman Melville's *Moby Dick* from a website, cleans it, and analyzes the most frequent words using Python's text-processing libraries.

---

## 🚀 Project Overview
This project develops a data science pipeline to analyze the word frequency distribution of a classic novel. By scraping the HTML content of *Moby Dick* from Project Gutenberg, the project demonstrates how to handle unstructured text data. The pipeline tokenizes the text, removes common English words (stop words), and then counts the occurrences of each word to determine the most frequent terms. This methodology can be applied to any book available on Project Gutenberg to reveal key thematic elements through a data-driven approach.

---

## 📊 Dataset Information
The analysis uses the full text of Herman Melville's novel, *Moby Dick*, which is scraped directly from the Project Gutenberg website.

### Core Data Source
- The novel's full text is retrieved as HTML from: `https://www.gutenberg.org/files/2701/2701-h/2701-h.htm`.

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| requests | Web scraping (to fetch HTML content) |
| BeautifulSoup | HTML parsing (to extract text from HTML) |
| nltk | Natural Language Toolkit (for tokenization and stop word removal) |
| collections.Counter | Counting word frequencies |
| Jupyter Notebook | Development and analysis environment |

### Analysis Pipeline
1.  **Web Scraping**: The HTML content of *Moby Dick* is fetched from Project Gutenberg using the `requests` library.
2.  **Text Extraction**: The `BeautifulSoup` object is used to parse the HTML and extract the raw, plain text of the novel.
3.  **Text Processing**: The raw text is cleaned by:
    * **Tokenization**: Splitting the text into individual words using a regular expression tokenizer to remove punctuation.
    * **Normalization**: Converting all words to lowercase to ensure consistency.
    * **Stop Word Removal**: Removing common, uninteresting English words like "the" and "a" using `nltk`'s built-in list.
4.  **Frequency Analysis**: The `collections.Counter` class is used to efficiently count the occurrences of each word in the cleaned list.

---

## 📈 Key Insights & Results

### The Most Frequent Words
The analysis successfully answers the project's central question by identifying the top 10 most frequent words in *Moby Dick*. The results highlight the novel's key themes:
-   **Top Word**: The most common word, not surprisingly, is **"whale"**, which appears 1,246 times.
-   **Other Top Words**: Other frequent words include "one", "like", "upon", "man", "ship", "ahab", "ye", "sea", and "old". These terms reflect the novel's focus on the sea, the crew, and Captain Ahab's obsessive quest.