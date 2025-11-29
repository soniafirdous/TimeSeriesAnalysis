
# 📈 Time Series Analysis & Forecasting

A complete workflow for exploring, modeling, and forecasting time-dependent data.

## 🔍 Overview

This project performs end-to-end time series analysis, including preprocessing, interpolation of missing values, exploratory data analysis (EDA), trend & seasonality detection, and forecasting using both classical statistical models and deep learning approaches.

The goal is to compare different forecasting techniques and evaluate which model gives the most accurate future predictions.

## 📊 Dataset

The project uses a monthly passenger dataset containing historical observations of the number of passengers per month.
It includes:

Monthly timestamp column (Date)

Numeric target variable (Passengers)


Clear trend & seasonality

## 🧹 Data Preprocessing

✔ Convert date column to datetime

✔ Set datetime as index

✔ Sort chronologically

✔ Detect & handle missing values using interpolation:

Linear interpolation

Logistic (growth-based) interpolation

✔ Decompose the series into:

Trend

Seasonal component

Residuals

✔ Train–test split (last 12 months as test set)

## 🧭 Exploratory Data Analysis

Line plots of the full series

Seasonal decomposition

Autocorrelation (ACF) & Partial autocorrelation (PACF)


## Stationarity test (ADF)

## 🤖 Models Implemented
1️⃣ Holt-Winters Exponential Smoothing

Captures trend + seasonality with smoothing parameters α, β, γ.

2️⃣ SARIMA (Seasonal ARIMA)

Used for seasonally patterned series with AR, I, MA orders + seasonal components.

3️⃣ Prophet (Facebook/Meta)

Handles trend, seasonality, holiday effects.
Automatically manages missing values during fitting.

4️⃣ LSTM Neural Network

Deep learning model trained on:

Windowed sequences (“timesteps”)

Reshaped input: (samples, timesteps, features)
Forecast generated for last 12 months.

## 📈 Forecast Visualization

Plots included:

Actual vs Training vs Testing


🧪 Model Evaluation

Evaluation metrics for each model:

MAE – Mean Absolute Error

RMSE – Root Mean Squared Error

MAPE – Mean Absolute Percentage Error

Example output:

Model	MAE	RMSE	MAPE
SARIMA	12.57	17.09	2.78
Holt-Winters	10.30	15.81	2.20
Prophet	33.43	43.06	6.61
LSTM	47.67	54.70	—

## 🧾 Key Findings

Holt-Winters performs best for smooth seasonal data.

SARIMA is competitive but requires tuning.

Prophet struggles on datasets with strict monthly seasonality.

LSTM requires more data to outperform classical models.


## 🙋‍♀️Author:
Sonia Firdous
soniafirfous1985@gmail.com
