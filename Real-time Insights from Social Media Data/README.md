# 📊 Real-time Insights from Social Media Data
A data science project that leverages Twitter's API to analyze and visualize local and global trends in near real-time, providing insights into thought patterns and public sentiment.

---

## 🚀 Project Overview
This project demonstrates how to collect and analyze social media data to uncover real-time trends. Using a snapshot of Twitter's `GET trends/place` API, the project explores what topics were trending worldwide and in the United States. It showcases how to handle JSON data from an API and perform a basic analysis to understand the most talked-about topics and their corresponding tweet volumes.

---

## 📊 Dataset Information
This project utilizes data pulled directly from the Twitter API, providing a real-time snapshot of trends. The data is in JSON format.

### Core Variables
- **`name`**: The name of the trending topic (e.g., a hashtag or a phrase)
- **`url`**: The URL to a Twitter search for the topic
- **`tweet_volume`**: The number of tweets for the topic in the last 24 hours

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| json | Loading and inspecting JSON data |
| pandas | Data manipulation and conversion |
| Jupyter Notebook | Development and analysis environment |

### Analysis Pipeline
1.  **Data Loading**: The project loads JSON files containing trends data for both worldwide and the United States.
2.  **Data Structuring**: The raw JSON data is converted into pandas DataFrames to facilitate easier manipulation and analysis.
3.  **Insights Generation**: The analysis focuses on identifying the top trending hashtags and topics, as well as those with significant tweet volumes.

---

## 📈 Key Insights & Results

### Top Trends Analysis
The project successfully identifies the top trending topics based on their tweet volume. For example, topics like `#WeLoveTheEarth` and `#GoodFriday` were trending heavily worldwide, showcasing the platform's ability to reflect both global movements and cultural events.

### Location-Based Insights
By comparing worldwide trends with those in a specific location like the US, the analysis can reveal which topics are gaining traction on a local level versus those that are globally significant.