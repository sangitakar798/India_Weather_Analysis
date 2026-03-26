# 🌦️ India Weather Analysis & Heatwave Detection

## 📌 Project Overview
This project analyzes weather data across India to identify heatwave-prone regions, understand temperature trends, and explore relationships between weather parameters.

---

## 🎯 Objectives
- Identify locations with highest heatwaves
- Analyze temperature trends over time
- Study correlation between weather features
- Build interactive dashboard for insights

---

## 🛠️ Tech Stack
- Python (Pandas, NumPy, Matplotlib, Seaborn, Folium)
- MySQL (SQL)
- Power BI
- SQLAlchemy

---

## 📂 Dataset
Weather dataset includes:
- Temperature (min/max)
- Humidity
- Rainfall & Snowfall
- Wind Speed
- Pressure
- Heatwave (0/1)
- Latitude & Longitude

---

## ⚙️ Data Cleaning
- Handled missing values (mean/median/domain logic)
- Removed duplicates
- Fixed invalid negative values
- Treated outliers using IQR capping
- Converted date to datetime
- Extracted features:
  - Year, Month, Day
  - Day name, Weekend flag

---

## 🗄️ SQL Analysis

### 🔹 Heatwave by Location
```sql
SELECT latitude, longitude, SUM(heatwave) AS total_heatwaves
FROM india_weather_data
GROUP BY latitude, longitude
ORDER BY total_heatwaves DESC;

### 📊 Visualizations
- 📍 Heatwave Map (Folium / Power BI)
- 📈 Temperature Trend (Line Chart)
- 📅 Monthly Temperature (Bar Chart)
- 🌧 Rainfall Distribution (Histogram)
- 🔗 Correlation Heatmap
