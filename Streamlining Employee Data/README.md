# 📊 Streamlining Employee Data
A data management project that consolidates scattered human resources data from various file formats into a single, structured pandas DataFrame for a growing business.

---

## 🚀 Project Overview
This project addresses a common business challenge: disparate and disorganized data. It focuses on a use case within human resources, where employee information is spread across multiple files in different formats (CSV, Excel, JSON). The primary objective is to build a data pipeline that loads, merges, cleans, and standardizes this data into one unified DataFrame. The final output is a single, clean CSV file that can serve as a reference for the People Operations team, showcasing a practical approach to data consolidation and preprocessing.

---

## 📊 Dataset Information
The analysis uses data from three distinct sources to build a comprehensive employee profile:

### Core Data Sources
- **`office_addresses.csv`**: Contains the physical addresses of company offices.
- **`employee_information.xlsx`**: An Excel file with two sheets.
  - **Sheet 1**: Employee personal addresses, including country, city, and street information.
  - **Sheet 2 (`emergency_contacts`)**: Emergency contact details for each employee, with column headers that need to be manually defined.
- **`employee_roles.json`**: A JSON file that maps employee IDs to their roles, salaries, and teams.

---

## 🛠️ Technical Implementation

| Technology | Purpose |
|------------|---------|
| Python | Primary programming language |
| pandas | Data loading, merging, cleaning, and manipulation |
| NumPy | Handling numerical computations |
| Jupyter Notebook | Development and analysis environment |

### Data Pipeline Steps
1.  **Data Loading**: Datasets are loaded from their native formats (CSV, Excel, JSON) into separate pandas DataFrames. The JSON file is loaded with the `orient='index'` parameter to ensure employee IDs are used as the index.
2.  **Data Merging**: The three DataFrames (`df_employee_addresses`, `df_emergency_contacts`, `df_employee_roles`) are merged sequentially using `pd.merge()` on their common key, `employee_id`, to create a single, wide table.
3.  **Data Cleaning**: Duplicate columns (`first_name`, `last_name`) are dropped, and several columns are renamed to be more descriptive and consistent with the project's goals.
4.  **Feature Engineering**: A new column, `status`, is added to classify employees as "On-site" or "Remote" based on whether their office address information is available or not.
5.  **Final Formatting**: The columns are reordered for logical flow, the employee ID is set as the DataFrame's index, and the `street_number` column is cast as an integer.

---

## 📈 Key Insights & Results

### Project Outcomes
- The final product is a **clean, unified, and well-structured DataFrame** that gathers all relevant employee data from disparate sources into a single table.
- The project demonstrates how to handle **real-world data issues** such as multiple file formats, missing headers, duplicate columns, and data-type inconsistencies.
- The final dataset, exported to a CSV file, serves as a **single source of truth** for the People Operations team, improving data access and simplifying reporting.