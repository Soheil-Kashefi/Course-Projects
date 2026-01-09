# 😴 Sleep Health Analysis: Understanding Factors Influencing Sleep Quality

A data analytics project for SleepInc that explores how lifestyle, demographic, and physiological variables correlate with sleep duration, sleep quality, and potential sleep disorders.

---

## 🚀 Project Overview

SleepInc provided an anonymized dataset capturing multiple attributes for individuals over a six-month period. The goal of this project is to identify behavioral and biological patterns associated with healthy and unhealthy sleep habits. This includes quantifying relationships among stress levels, physical activity, occupation, sleep duration, sleep disorders, and overall sleep quality.

The analysis was completed using Python, with an emphasis on exploratory data analysis (EDA), feature correlation inspection, and data-driven insights.

---

## 📊 Dataset Information

### **sleep_health_data.csv**

A structured dataset with 13 columns capturing demographic, lifestyle, physiological, and sleep-related attributes.

| Column                            | Description                            |
| --------------------------------- | -------------------------------------- |
| Person ID                         | Unique identifier for each participant |
| Gender                            | Male or Female                         |
| Age                               | Age in years                           |
| Occupation                        | Participant’s profession               |
| Sleep Duration (hours)            | Average daily sleep duration           |
| Quality of Sleep (1–10)           | Self-reported sleep quality            |
| Physical Activity Level (min/day) | Daily exercise duration                |
| Stress Level (1–10)               | Self-reported stress score             |
| BMI Category                      | Underweight / Normal / Overweight      |
| Blood Pressure                    | Systolic/diastolic resting measurement |
| Heart Rate (bpm)                  | Resting heart rate                     |
| Daily Steps                       | Average step count                     |
| Sleep Disorder                    | None / Insomnia / Sleep Apnea          |

---

## 🛠️ Technical Implementation

| Technology       | Purpose                                                |
| ---------------- | ------------------------------------------------------ |
| Python           | Core analytics environment                             |
| pandas           | Data ingestion, cleaning, and aggregation              |
| matplotlib       | Visualization tools for trend and correlation analysis |
| Jupyter Notebook | Interactive EDA workflow                               |

---

## 🔍 Methodology

### **1. Data Loading & Structure Inspection**

* Loaded `sleep_health_data.csv` and previewed the first rows.
* Examined schema using `.info()` and statistical distributions using `.describe()`.

### **2. Data Quality Checks**

* Assessed missing values across all fields (`isna().any()`), confirming that the dataset was complete and required no imputation.

### **3. Exploratory Data Analysis (EDA)**

Key exploratory steps included:

#### **Sleep Duration by Occupation**

* Grouped data by occupation to compute mean sleep duration.
* Identified roles associated with the lowest average sleep duration.
* Used this to inform hypotheses regarding work-related lifestyle pressures.

#### **Stress vs. Sleep Quality Trend Analysis**

* Computed average sleep quality across stress levels.
* Visualized the relationship using a line plot to assess negative correlation patterns.
* Confirmed that increased stress is associated with reduced perceived sleep quality.

#### **Descriptive Trends**

* Compared sleep metrics across BMI categories, gender, and age groupings (via summary statistics).
* Evaluated whether individuals with diagnosed sleep disorders exhibit lower sleep durations or quality.

---

## 📈 Key Findings

### **1. Occupational Impact on Sleep Duration**

* professions such as **Sales Representative** exhibited the **lowest average sleep duration**, suggesting that job demands or lifestyle factors in these fields may contribute to insufficient sleep.

### **2. Strong Negative Relationship Between Stress and Sleep Quality**

* Higher stress levels consistently correlated with lower sleep quality ratings.
* Visualization revealed a monotonic decreasing trend.

### **3. Lifestyle Factors Influence Sleep Health**

* Increased physical activity generally aligned with higher sleep quality and marginally higher sleep duration.
* Those recording fewer daily steps or higher resting heart rates tended to show lower sleep scores.

### **4. Sleep Disorders**

* Individuals diagnosed with **Insomnia** or **Sleep Apnea** had:

  * Lower average sleep duration
  * Lower sleep quality
  * Higher stress levels

---

## 🧠 Data Analysis Workflow

This project implements a structured analytics pipeline:

1. **Data Review**: Schema validation and statistical exploration
2. **Quality Checks**: Ensuring absence of missing or corrupted entries
3. **Feature Exploration**: Group-based and trend analyses
4. **Visualization**: Matplotlib-based plots to evaluate correlations
5. **Insight Generation**: Actionable conclusions for SleepInc regarding sleep health drivers
