# ⚡ US Energy Consumption Forecasting
### Time Series Analysis | Forecasting | SAS | Energy Analytics

This project analyzes **historical U.S. energy consumption data** from the Energy Information Administration (EIA) to identify trends, seasonality, and the most effective forecasting methods for the **commercial and industrial sectors**.

The goal is to support **energy providers and policymakers** with accurate, data-driven forecasting insights.

---

## 🎯 Objective

- Identify key drivers of U.S. energy consumption
- Detect trend and seasonal patterns
- Compare multiple forecasting techniques
- Determine the most reliable models for future prediction

---

## 📊 Data Source

- Source: U.S. Energy Information Administration (EIA)
- Frequency: Monthly
- Time range: **January 1973 – July 2024**
- Sectors analyzed:
  - Commercial
  - Industrial

Dataset includes:
- Total energy consumption
- Primary energy
- End-use energy
- Electricity sales
- Electricity losses

---

## 🔧 Data Preparation

- Date standardized to SAS-compatible `MONYY7.` format
- Time series partitioned:
  - 80% training
  - 20% validation
- Target variable:
  - Total energy consumption (sector-wise)

---

## 📈 Exploratory Time Series Analysis

### Commercial Sector
- Clear upward trend
- Strong seasonal pattern
- ACF shows significant autocorrelation at lags 1, 12, 24, 36

### Industrial Sector
- Non-linear trend
- Pronounced seasonality
- Strong correlations with primary consumption and end-use energy

---

## 🧠 Forecasting Models Evaluated

### ✔ Holt-Winters Exponential Smoothing
- Additive
- Multiplicative

### ✔ Regression Models
- Multiple Linear Regression (with dummy variables)
- Non-linear Regression
- Deseasonalized & Reseasonalized Regression

### ✔ ARIMA
- Multiple seasonal ARIMA configurations tested
- Residual diagnostics revealed non–white noise behavior

---

## 📊 Model Evaluation Metrics

- MAE
- MSE
- MAPE
- AIC / BIC
- Durbin–Watson test (independence)

---

## 🏆 Best Performing Models

### Commercial Sector
- **Holt-Winters (Multiplicative)** performed best on training data
- **Regression with deseasonalization** performed best on validation data

### Industrial Sector
- **Holt-Winters with seasonal dummy variables** fit training data well
- **Deseasonalized regression** provided the most reliable forecasts on validation data

---

## 🔍 Key Findings

- Energy consumption exhibits **strong seasonal patterns**
- Regression models with deseasonalization outperform ARIMA
- Key drivers include:
  - Primary energy consumption
  - End-use energy
  - Electricity sales
- ARIMA models failed to produce reliable forecasts due to residual autocorrelation

---

## ⚠️ Limitations

- Serial correlation violates independence assumptions
- Potential multicollinearity in regression models
- ARIMA models struggled with complex seasonality

---

## 🔮 Future Enhancements

- Incorporate weather variables (temperature)
- Include economic indicators (GDP, population growth)
- Explore hybrid ML + time series models
- Validate models using rolling-window forecasting

---

## 🛠 Tools & Technologies

- **SAS**
  - PROC ESM
  - PROC REG
  - PROC ARIMA
  - PROC TIMESERIES
- Time series analysis
- Forecast accuracy evaluation

---

## 👩‍💻 Author

**Vishaka Sharma**  
Business Analytics | Time Series Forecasting | Energy Analytics
