# 🌦️ Weather Dashboard – Power BI Project

A visually rich, real-time weather monitoring dashboard built in **Power BI** using live data from [WeatherAPI.com](https://www.weatherapi.com/). This project demonstrates API integration, advanced DAX measures, optimized data modeling, and user-centric UI/UX design for dynamic, actionable insights.

---

## 📌 Project Highlights

* **Live Weather Data**: API-driven real-time updates
* **Multi-City Dashboard**: Compare conditions in Alexandria, Cairo, and Hurghada
* **Air Quality Index (AQI)**: Visual gauges with pollutant-level breakdown
* **Forecast Panel**: Interactive 7-day and hourly forecasts
* **UX-First Design**: Responsive layout, weather-themed colors, smooth transitions

---

## 🔗 Data Architecture & Sources

### 🌐 API Integration

* **Source**: [WeatherAPI.com](https://www.weatherapi.com/)
* **Data Points**: Current conditions, forecasts, air quality, sunrise/sunset, UV index
* **Refresh Strategy**: Live data refresh with `Last_Updated_Timestamp` displayed

### 🧩 Data Model Structure

| Table                 | Description                                                           |
| --------------------- | --------------------------------------------------------------------- |
| `Weather_Report(1-5)` | Raw API responses                                                     |
| `MasterTable`         | Consolidated view                                                     |
| `Current`             | Real-time metrics                                                     |
| `Forecast_Day`        | Daily forecasts, with derived columns like `Day_Name`, `Sunrise_Date` |
| `Forecast_Hour`       | Hour-by-hour weather conditions                                       |

* **Schema**: Star schema with DAX-created `Locations` dimension
* **Relationships**: Bi-directional filtering for interactivity

---

## 📐 DAX & Calculated Measures

Stored in a dedicated `_Measures` table, including:

* `AQI Color` & `Status Text`
* Conditional formatting for pollutants: `CO`, `NO2`, `O3`, `PM2.5`, `SO2`
* Temperature conversions: `Current_Temp_C`, `For_Temp_C`
* `Humidity`, `Wind_Speed`, `Visibility`, `UV_Index`
* `Left_Value_PM10`, `Max_Value` for air quality thresholds
* `Last_Updated_Date_Current`: Refresh monitoring

---

## 🖥️ Dashboard Features

### 🔴 Current Conditions Panel

* **Live City Switching**: Buttons for Alexandria, Cairo, Hurghada
* **Real-Time Icons**: Weather-adaptive visuals
* **Primary Display**: Current temperature & condition status

### 📈 Forecasts

* **7-Day Forecast**: Interactive trend line + high/low temperatures
* **Hourly Forecast**: Scrollable panel for temperature, condition, precipitation

### 🌫️ Environmental Metrics

* Humidity, Wind Speed, Visibility, Pressure, UV Index, Rain Probability

### 🧪 Air Quality Dashboard

* AQI Gauge (e.g., 45 – *Good*)
* Pollutant breakdown (PM10, PM2.5, CO, O3, NO2, SO2)
* Health status indicators & color-coded warnings

### 🌄 Sunrise & Sunset

* Icon-based daily solar schedule for planning and awareness

---

## ⚙️ Technical Highlights

| Area            | Techniques Used                              |
| --------------- | -------------------------------------------- |
| **API**         | REST endpoint integration in Power BI        |
| **Modeling**    | Star schema, optimized relationships         |
| **DAX**         | Advanced conditional logic, dynamic visuals  |
| **UX**          | Responsive layout, visual hierarchy, theming |
| **Performance** | Efficient calculations, memory management    |

---

## 🧠 Business Value

### ✅ Use Cases

* Personal weather planning
* Health monitoring (AQI)
* Travel & tourism recommendations
* Agricultural forecasting
* Event planning

### 💼 Skills Demonstrated

* API integration in Power BI
* DAX proficiency
* Real-time analytics
* Data modeling & optimization
* Dashboard design for usability

---

## 📸 Screenshots

```
/assets/
  weather-dashboard-main.png
  forecast-panel.png
  air-quality-dashboard.png
  sunrise-sunset.png
```

---
## 🚀 Getting Started

1. Download the `.pbix` file
2. Open in **Power BI Desktop**
3. Ensure your internet connection for API to refresh live data
4. Use city buttons and slicers to explore insights
