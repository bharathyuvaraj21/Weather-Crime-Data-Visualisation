# Data Visualization Project – Weather and Crime Analysis (2023)

---

## 📘 Overview

This project, **Data Visualization Project**, is part of the coursework for the **Data Visualization (MA304)** module.  
The analysis investigates the **relationship between weather conditions** and **crime frequency** in **January 2023**, exploring whether atmospheric factors like **temperature**, **humidity**, **wind speed**, **precipitation**, and **visibility** have any potential influence on criminal activities.

The aim is to generate meaningful insights that could assist in developing **data-driven strategies** for **crime prevention** and **public safety** planning.

---

## 👨‍💻 Author & Project Info

**Author:** Bharath Yuvaraj  
**Register No:** 2316529  
**Course:** MA304 – Data Visualization  
**Date:** April 24, 2024  
**Language:** R Markdown (`.Rmd`)  
**Output:** HTML document (generated via the *Knit* button in RStudio)

---

## 🧩 Datasets Used

1. **crime23.csv**
   - Contains data on reported criminal incidents.
   - Includes variables such as:
     - Type of crime
     - Location of occurrence
     - Date and time of report
     - Demographic details of offenders and victims

2. **temp2023.csv**
   - Contains aggregated weather data for the year 2023.
   - Features include:
     - Daily temperature (max/min/avg)
     - Humidity
     - Wind speed
     - Precipitation
     - Visibility

### Dataset Dimensions
- **Crime Data:** 6,878 rows × 12 columns  
- **Temperature Data:** 365 rows × 18 columns  

---

## ⚙️ Tools & Libraries Used

The project was developed using **R** and **R Markdown**, leveraging several visualization and data analysis libraries:

| Library | Purpose |
|----------|----------|
| `ggplot2` | Data visualization and charting |
| `dplyr` | Data manipulation and transformation |
| `plotly` | Interactive and dynamic plots |
| `leaflet` | Interactive geographic (map-based) visualization |
| `xts` | Time-series data handling |
| `lubridate` | Date and time manipulation |

---

## 🧠 Project Workflow

### Step 1: Data Import and Initial Exploration
- Imported datasets using:
  ```R
  Crime_Data <- read.csv("crime23.csv")
  Temperature_Data <- read.csv("temp2023.csv")
Verified structure using str() and checked dimensions with dim().

Explored data types, missing values, and descriptive summaries.

Step 2: Data Cleaning and Preprocessing
Renamed inconsistent column headers for clarity.

Converted date columns into standard date formats using lubridate.

Filtered datasets to focus on January 2023.

Checked for and handled missing or invalid values.

Step 3: Data Integration
Merged the two datasets on date, linking each day’s crime frequency with its respective weather attributes.

Created a unified data frame for visualization.

Step 4: Exploratory Data Analysis (EDA)
Analyzed trends in crime counts relative to:

Average daily temperature

Humidity and precipitation

Wind speed and visibility

Calculated summary statistics and correlation metrics.

Step 5: Visualization and Insights
Time Series Plots: Crime frequency over time, layered with temperature or precipitation levels.

Bar Charts: Comparison of crime types under different weather conditions.

Interactive Maps (Leaflet): Geographic distribution of crimes across regions.

Interactive Charts (Plotly): Dynamic visual exploration of trends.

📊 Key Visualizations
Temperature vs. Crime Frequency

Displays the relationship between daily temperature and number of reported crimes.

Humidity & Precipitation Analysis

Shows how moisture or rainfall might coincide with fluctuations in crime rates.

Interactive Crime Density Map

Created using leaflet to visualize high-crime zones geographically.

Crime Type Distribution

Illustrates the proportion of different crime categories under various weather patterns.

Time-Series Correlation

Combines both weather and crime data to examine temporal alignments or anomalies.

📈 Major Findings
Days with warmer temperatures and moderate humidity showed relatively higher crime frequency.

Rainy or extreme weather days tended to have fewer outdoor crime incidents.

Temporal patterns revealed specific days where crime spikes aligned with notable weather variations.

Visual evidence suggests that weather conditions can act as contributing factors influencing the likelihood or type of crime.

