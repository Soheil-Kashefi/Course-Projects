# 📈 Analyzing Search Trends with Google Trends
A data visualization project that explores and analyzes search interest for the term "diet" using the `pytrends` library, revealing seasonal patterns and underlying trends.

---

## 🚀 Project Overview
This project demonstrates how to use the **Google Trends API** to pull and visualize time-series data for a given search term. The goal is to identify and understand a search term's popularity over time, detect seasonality, and visualize long-term trends. The analysis focuses specifically on the search term "diet," providing a clear example of how public interest fluctuates and peaks annually, often driven by cultural events like New Year's resolutions.

---

## 📊 Dataset Information
The project does not use a pre-existing static dataset. Instead, it dynamically pulls data directly from **Google Trends** using the `pytrends` library.

### Core Data Points
- **Search Term**: "diet"
- **Timeframe**: A specified period from January 2012 to January 2017
- **Interest over time**: A numerical value representing search interest for a given period on a scale of 0 to 100.

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pytrends | Data acquisition from Google Trends |
| pandas | Data manipulation and time-series analysis |
| matplotlib | Static data visualization |
| seaborn | Enhanced data visualization |
| Jupyter Notebook | Development and analysis environment |

### Analysis Pipeline
1. **Data Acquisition**: Connect to the Google Trends API using `pytrends` and retrieve interest data for the search term "diet" over a five-year period.
2. **Time-Series Analysis**: Resample the data to monthly and quarterly frequencies to observe different levels of detail.
3. **Trend Smoothing**: Calculate a **rolling mean** to smooth out weekly fluctuations and reveal the underlying trend.
4. **Data Visualization**: Create various plots, including line charts and heatmaps, to visually represent seasonality and spikes in search interest.

---

## 📈 Key Insights & Results

### Discovery of Seasonality
- **Annual Spikes**: The visualizations clearly show a strong and consistent seasonal pattern, with search interest for "diet" spiking sharply every **January**. This aligns with the New Year's resolution phenomenon.
- **Long-Term Trend**: The project demonstrates how a rolling mean can be used to identify that, despite the annual spikes, the overall search interest for "diet" showed a slight downward trend during the analyzed period.
- **Visual Evidence**: The project's visualizations effectively highlight the recurring weekly and monthly patterns, providing compelling evidence of the data's cyclical nature.