# 🩺 Dr. Semmelweis and the Discovery of Handwashing

A data-driven analysis of Dr. Ignaz Semmelweis's groundbreaking discovery that handwashing dramatically reduces mortality rates in childbirth during the 1840s at Vienna General Hospital.

---

## 🚀 Project Overview

This project reanalyzes the historical data that led Dr. Ignaz Semmelweis to discover the life-saving importance of handwashing in medical practice. Through statistical analysis and data visualization, we explore how mandatory handwashing policies dramatically reduced childbed fever mortality rates at Vienna General Hospital in the 1840s. The analysis demonstrates how proper data presentation could have helped Semmelweis convince the medical community of his revolutionary findings.

---

## 📊 Dataset Information

The analysis utilizes two key datasets covering Vienna General Hospital's obstetric wards from 1841-1849:

### yearly_deaths_by_clinic.csv
Historical mortality data comparing two maternity clinics (1841-1846)
- **Temporal Variables**: year, births, deaths, clinic
- **Key Metrics**: proportion_deaths (calculated mortality rate)
- **Scope**: 12 observations across 2 clinical facilities

### monthly_deaths.csv
Monthly mortality tracking with handwashing intervention point
- **Temporal Variables**: date (monthly intervals), births, deaths
- **Performance Metrics**: proportion_deaths
- **Critical Timeline**: June 1, 1847 handwashing mandate implementation

---

## 🛠️ Technical Implementation

| Technology       | Purpose                                    |
|------------------|--------------------------------------------|
| Python           | Primary programming language               |
| pandas           | Data manipulation and time series analysis |
| matplotlib       | Statistical visualization and plotting     |
| Jupyter Notebook | Interactive development environment        |

---

## 📈 Key Findings

### Clinic Mortality Disparities
- **Clinic 1**: Medical students facility with 6-16% mortality rates
- **Clinic 2**: Midwife-staffed facility with 2-7% mortality rates
- **Root Cause**: Medical students performed autopsies before deliveries without handwashing

### Handwashing Impact Analysis
- **Pre-Handwashing Average**: ~10% mortality rate
- **Post-Handwashing Average**: ~2% mortality rate
- **Absolute Reduction**: 8.4 percentage point decrease
- **Relative Improvement**: 84% reduction in death rates

### Statistical Validation
- **Bootstrap Analysis**: 3,000 resampling iterations
- **95% Confidence Interval**: 6.7-10 percentage point reduction
- **Statistical Significance**: Robust evidence of handwashing effectiveness

---

## 🔬 Methodology

### Data Processing Workflow
1. **Historical Data Integration**: Combined yearly and monthly mortality datasets
2. **Mortality Rate Calculation**: Deaths/births ratio for standardized comparison
3. **Temporal Segmentation**: Pre/post handwashing mandate analysis
4. **Statistical Visualization**: Time series plots highlighting intervention impact