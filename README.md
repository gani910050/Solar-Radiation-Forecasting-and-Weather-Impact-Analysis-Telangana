# Solar Radiation Forecasting and Weather Impact Analysis – Telangana

# Overview
This project focuses on analyzing and forecasting solar radiation using time series models and LSTM. It also studies the impact of weather variables such as temperature, cloud cover, and wind on solar radiation.

---

# Objectives
- Analyze long-term solar radiation patterns  
- Identify trend and seasonality  
- Forecast future solar radiation values  
- Study the influence of weather variables  

---

# Dataset
The dataset contains long-term meteorological observations:

- Surface Solar Radiation (min, mean, max)  
- Temperature (2m)  
- Dew Point Temperature  
- Wind Components (U & V)  
- Total Cloud Cover  
- UTCI  
 Time Period: 1979 – 2024  
Frequency: Monthly aggregated data  

---

# Data Preprocessing
- Converted date column to datetime index  
- Handled missing values using interpolation  
- Aggregated daily data into monthly values  

---

# Exploratory Data Analysis
- Identified strong seasonal patterns  
- Observed relationships:
  - Solar radiation ↑ with temperature  
  - Solar radiation ↓ with cloud cover  

---

# Models Used

# 1. SARIMA
- Captures trend and seasonality  
- Univariate model  

# 2. SARIMAX  (Best Model)
- Includes exogenous variables  
- Captures weather impact  

# 3. LSTM
- Deep learning model  
- Captures nonlinear patterns  

---

# Model Performance

| Model   | MAE        | RMSE       |
|--------|-----------|-----------|
| SARIMA | 53,849    | 70,097    |
| SARIMAX| 45,260    | 56,368    |
| LSTM   | 52,407    | 66,459    |

---

# Key Insights
- SARIMAX performed best due to inclusion of weather variables  
- Solar radiation is strongly influenced by atmospheric conditions  
- Seasonal patterns are consistent over time  

---

Note on Errors
Although MAE and RMSE values appear large, they are proportional to the scale of solar radiation values (10⁵–10⁶), making the model performance acceptable.

Forecasting
- Generated 12-month future predictions  
- Seasonal patterns maintained in forecasts  

---

# Future Work
- Include more variables (humidity, rainfall)  
- Improve LSTM performance  
- Apply advanced models like Prophet  

---

# Tech Stack
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Statsmodels  
- TensorFlow / Keras  
