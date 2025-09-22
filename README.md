Airline Data Analysis – Full Report



## 🌟 Introduction  

Air travel is one of the busiest transportation systems in the world. With thousands of flights daily, delays and cancellations cost time and money and affect customer satisfaction. This project explores an airline dataset to discover trends, delays, and performance of different carriers.

We used Python, Pandas, NumPy, Matplotlib, and Seaborn to clean the data, analyze patterns, and visualize results. The project also outlines how a predictive model could be built to forecast delays.

## 📑 Table of Contents
- [Introduction](#-introduction)
- [Dataset Overview](#-dataset-overview)
- [Objectives](#-objectives)
- [Data Cleaning](#-data-cleaning)
- [Exploratory Analysis](#-exploratory-analysis)
- [Visualizations](#-visualizations)
- [Predictive Modeling](#-predictive-modeling)
- [Findings & Recommendations](#-findings--recommendations)
- [How to Reproduce](#-how-to-reproduce)
- [Conclusion](#-conclusion)

---

---

## 🗂 Dataset Overview  

- **File**: `airlines_flights_data.csv`  
- **Size**: ~100,000 flights (example)  
- **Key Columns**:  

| Column | Description |  
|---------|-------------|  
| FlightDate | Date of the flight |  
| Airline | Carrier name/code |  
| Origin/Destination | Airport codes |  
| DepDelay / ArrDelay | Delay in minutes at departure/arrival |  
| Cancelled | Whether the flight was canceled |  
| CarrierDelay, WeatherDelay, NASDelay, SecurityDelay, LateAircraftDelay | Delay reasons in minutes |  

---

## 🎯 Objectives  

1. Clean and prepare the dataset for analysis.  
2. Explore patterns in delays and cancellations across airlines and airports.  
3. Visualize the data to understand seasonal or hourly trends.  
4. (Optional) Build a predictive model to forecast delays.  

---

## 🧹 Data Cleaning  

- **Missing values**: Checked for `NaN` and imputed or dropped.  
- **Date columns**: Converted `FlightDate` to datetime. Extracted Month, Day of Week, and Hour for trend analysis.  
- **Categorical columns**: Normalized carrier names and airport codes.  
- **Feature engineering**: Created flags like `IsWeekend`, `IsPeakHour`.  

---

## 📊 Exploratory Analysis  

### ✈️ Flights by Airline  
- Horizontal bar graph of flights per airline.  
- Airline A had the highest number of flights; Airline C the lowest but best on-time performance.  

### ⏱ Delay Distributions  
- Most flights depart on time, but some face very large delays.  
- Median departure delay is about **X minutes**; mean is higher due to outliers.  

### ❌ Cancellation Rates  
- Overall cancellation rate: **~3%** (example).  
- Weather-related cancellations spike during winter months.  

### ⚠️ Delay Causes  
- Carrier delays: ~40%  
- Weather delays: ~20%  
- NAS delays: ~30%  
- Security delays: <5%  

### 🕒 Time Trends  
- Delays peak during evening hours (5–9 PM).  
- Mondays and Fridays see the highest average delays.  

---

## 📈 Visualizations  

- **Horizontal Bar Chart**: Flights per airline.  
- **Bar Chart**: Average delay by airline.  
- **Histogram/KDE**: Delay distributions.  
- **Line Plot**: Delay trends by hour/day.  
- **Stacked Bar Chart**: Delay reasons by airline.  
- **Heatmap**: Delays by Day-of-Week vs Hour-of-Day.  

> 💡 *Export plots as PNG and include them with `![alt text](path/to/image.png)`*  

---

## 🤖 Predictive Modeling  

- **Features**: Airline, Origin, Destination, Day of Week, Hour, Weather conditions.  
- **Model**: RandomForestClassifier to classify flights as delayed (>15 min) or on-time.  
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1, ROC AUC.  

Example metrics:  

Accuracy: 0.87
Precision: 0.82
Recall: 0.79
F1-score: 0.80
ROC AUC: 0.91

yaml
Copy code

---

## 💡 Findings & Recommendations  

- Concentrate on airlines/routes with highest delay and cancellation rates.  
- Allocate more resources during peak delay hours (evenings, Mondays/Fridays).  
- Plan proactively for winter months to handle weather delays.  
- Provide early alerts to passengers for high-risk flights.  

---

## 🛠 How to Reproduce  

1. Clone the repository.  
2. Place the dataset CSV file at the specified path.  
3. Install dependencies:  

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

yaml
Copy code

4. Run the notebook `airline_data_analysis.ipynb`.  

---

## ✅ Conclusion  

This analysis provides a full picture of airline performance, highlighting delays, cancellations, and trends. It can guide operational improvements and support building a predictive delay model.  

---

<p align="center">✨ Built with Python & ❤️ for Data Analysis ✨</p>
