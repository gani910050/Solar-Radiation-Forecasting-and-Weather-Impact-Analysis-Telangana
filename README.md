#  Solar Radiation Forecasting and Weather Impact Analysis – Telangana

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Time%20Series-orange)

---

## Project Overview
This project focuses on analyzing and forecasting solar radiation using **time series models and deep learning techniques**. It also investigates the impact of meteorological variables such as temperature, cloud cover, and wind on solar radiation.

---

## Objectives
- Analyze long-term solar radiation patterns  
- Identify trend and seasonality  
- Forecast future solar radiation values  
- Study the influence of weather variables  

---

## Dataset Description
The dataset includes:

- Surface Solar Radiation (target variable)  
- Temperature (2m)  
- Dew Point Temperature  
- Wind Components (U & V)  
- Total Cloud Cover  
- UTCI  

📅 Time Period: 1979 – 2024  
📈 Frequency: Monthly aggregated data  

---

## Project Workflow

1. Problem Definition  
2. Data Collection  
3. Data Preprocessing  
4. Exploratory Data Analysis (EDA)  
5. Stationarity Testing (ADF Test)  
6. Feature Selection  
7. Model Building (SARIMA, SARIMAX, LSTM)  
8. Model Evaluation  
9. Residual Analysis  
10. Forecasting  
11. Results & Interpretation  

---

## Data Preprocessing
- Converted date column to datetime index  
- Handled missing values using interpolation  
- Aggregated daily data into monthly averages  

---

##  Exploratory Data Analysis
- Strong seasonal patterns observed  
- Key relationships:
  - Solar radiation ↑ with temperature  
  - Solar radiation ↓ with cloud cover  

---

# Stationarity Check (ADF Test)

- ADF Statistic = **-11.21**  
- p-value = **~0**
 The series is **stationary**, suitable for ARIMA models  

---

## Models Used

### SARIMA
- Captures trend and seasonality  
- Univariate model  

---

### SARIMAX (Best Model)
- Includes exogenous variables (weather data)  
- Captures external influence  

**Why best?**
> Solar radiation depends on atmospheric conditions → SARIMAX models this relationship  

---

### LSTM
- Deep learning model  
- Captures nonlinear patterns  
- Uses sequential learning  

---

## Model Evaluation

| Model   | MAE        | RMSE       |
|--------|-----------|-----------|
| SARIMA | 53,849    | 70,097    |
| SARIMAX| 45,260    | 56,368    |
| LSTM   | 52,407    | 66,459    |

---

## Error Interpretation

> High MAE and RMSE values are due to large data scale (10⁵–10⁶), not poor model performance.

---

## Residual Analysis
- Residuals show random behavior  
- No strong autocorrelation  
- Model is statistically valid  

---

## Forecasting
- Generated 12-month future predictions  
- Seasonal patterns preserved  

---

## Key Insights
- SARIMAX performed best  
- Weather variables significantly improve predictions  
- Solar radiation strongly depends on atmospheric conditions  

---

## Tech Stack
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Statsmodels  
- TensorFlow / Keras  

---

---

## Limitations
- Limited external variables  
- LSTM not fully optimized  
- Assumes historical patterns continue  

---

## Future Work
- Add humidity and rainfall  
- Improve LSTM tuning  
- Apply advanced models (Prophet, XGBoost)  

---

## Author
**Ramavath Ganesh**  
M.Sc. Statistics (2024–2026)  
Banaras Hindu University  

---

## GitHub Profile
https://github.com/gani910050  

---

##  Support
If you found this project useful, consider giving it a ⭐
 


