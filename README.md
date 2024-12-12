# Time-Series Forecasting Using IoT Sensor Data

## Overview
This project demonstrates the application of time-series forecasting techniques to IoT sensor data. By leveraging statistical and machine learning approaches, this analysis identifies patterns, trends, and seasonality in temperature data, aiding in better decision-making for IoT-based systems.

---

## Features
1. **Data Preprocessing**
   - Dropped non-relevant features for temperature forecasting.
   - Visualized time series data to understand trends and seasonality.

2. **Stationarity Testing**
   - Applied the Augmented Dickey-Fuller (ADF) test to assess stationarity of variables such as Temperature, Humidity, and Light.
   - Differencing methods were used to transform non-stationary data.

3. **Autocorrelation and Partial Autocorrelation**
   - Generated ACF and PACF plots to identify significant lags for model selection.

4. **SARIMA Modeling**
   - Built and evaluated a Seasonal AutoRegressive Integrated Moving Average (SARIMA) model for temperature forecasting.

---

## Dataset
The dataset consists of IoT sensor readings, including:
- **Date:** Timestamp of the readings.
- **Temperature:** Temperature values.
- **Humidity, Light, CO2, and Humidity Ratio:** Additional environmental variables.
- **Occupancy:** Whether the room is occupied (binary).

---

## Methodology
1. **Exploratory Data Analysis**
   - Visualized the time-series data to identify trends and periodicity.

2. **Stationarity Testing**
   - Conducted the ADF test for stationarity.
   - Differenced the data to handle non-stationarity.

3. **Modeling**
   - Used SARIMA with parameters optimized based on ACF and PACF plots.
   - Evaluated the model's performance using diagnostics like AIC, BIC, and residual analysis.

---

## Results
- **Stationarity Analysis:**
  - Temperature and Light were found to be stationary after first differencing.
  - Humidity and CO2 were non-stationary, excluded from forecasting.
  
- **SARIMA Model Performance:**
  - Successfully modeled temperature data with seasonal patterns.
  - Key parameters:
    - **Order:** (0, 1, 1)
    - **Seasonal Order:** (2, 1, 1, 12)
  - Diagnostics indicated well-fit residuals and statistically significant coefficients.

---

## Technologies Used
- **Python**
- **Libraries:**
  - `NumPy` and `Pandas`: Data manipulation and preprocessing.
  - `Matplotlib`: Data visualization.
  - `Statsmodels`: Time-series modeling (ADF test, SARIMA).
  - `Seaborn`: Visualization enhancements.
