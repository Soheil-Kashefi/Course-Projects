

# ✈️ Analyzing Flight Delays and Cancellations

An analysis of flight operations and weather impacts at major Pacific Northwest airports during the first half of 2022.

---

## 🚀 Project Overview

This project examines flight delay patterns and cancellation trends for departures from Seattle-Tacoma International Airport (SEA) and Portland International Airport (PDX). The analysis focuses on identifying key factors that contribute to operational disruptions, with particular attention to route-specific patterns, airline performance, and weather impacts.

---

## 📊 Dataset Information

The analysis uses two complementary datasets from the ModernDive team covering the first half of 2022

### flights2022.csv
Core flight operations data with 20 variables
- Temporal year, month, day, dep_time, sched_dep_time, hour, minute, time_hour
- Performance dep_delay, arr_time, sched_arr_time, arr_delay
- Flight Details carrier, flight, tailnum, origin, dest, air_time, distance
- Airline Info airline

### flights_weather2022.csv 
Enhanced dataset combining flight data with weather conditions (29 variables)
- All flight variables from flights2022.csv
- Weather Variables temp, dewp, humid, wind_dir, wind_speed, wind_gust, precip, pressure, visib
- Derived Variables route (origin-destination pairing)

---

## 🛠️ Technical Implementation

 Technology  Purpose 
---------------------
 Python  Primary programming language 
 pandas  Data manipulation and aggregation 
 matplotlib  Data visualization and plotting 
 Jupyter Notebook  Interactive development environment 

---


## 📈 Findings

### Route Performance
- Identified routes with highest cancellation rates
- Analyzed mean departure delays across different route combinations
- Generated visualizations showing top 9 most affected routes

### Airline Analysis
- Delay Leaders Airlines with highest mean departure delays
- Operational Reliability Carriers with most cancellations
- Comparative performance across Pacific Northwest operations

### Weather Impact
- Wind Threshold Analysis Compared delays for wind gusts ≥10mph vs 10mph
- Airport-Specific Effects PDX and SEA performance under different wind conditions
- Quantified Impact Measurable increase in delays during high wind conditions

---

## 📁 Project Structure

```
Analyzing-Flight-Delays-and-Cancellations
├── README.md                           # Project documentation
├── flight_analysis.ipynb               # Main analysis notebook
├── flights2022.csv                     # Core flight data
├── flights_weather2022.csv             # Flight + weather data
└── IMG_8801.JPG                        # Header image
```

---

## 📝 Data Sources

Dataset ModernDive team - Pacific Northwest flights 2022 (H1)  
Airports SEA (Seattle-Tacoma International), PDX (Portland International)  
Time Period January - June 2022

