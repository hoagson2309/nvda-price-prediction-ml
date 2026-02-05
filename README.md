# NVDA Price Prediction with Random Forest

This project utilizes a **Random Forest Regressor** to predict the next-day returns of NVIDIA (NVDA) stock. By engineering features from technical indicators, the model identifies patterns in market volatility and momentum.

## Features
- **Data Source:** Real-time and historical data via Alpaca Markets API.
- **Indicators:** SMA (5, 10, 20), RSI, and Bollinger Band Volatility.
- **Machine Learning:** Random Forest model with time-series cross-validation (no data leakage).
- **Visualizations:** Reconstructed price charts comparing actual market price vs. model predictions.

## Key Results
- **Mean Absolute Error (MAE):** ~$2.78 (Daily price variance).
- **Top Predictor:** 5-day Simple Moving Average (SMA_5).
- **Logic:** The model successfully avoids "data leakage" by shifting targets, ensuring it predicts the *future* based on *present* data.

## Setup
1. Clone the repo: `git clone https://github.com/hoagson2309/NVDA-Stock-Prediction-ML.git`
2. Install requirements: `pip install alpaca-py pandas scikit-learn ta matplotlib`
3. Add your Alpaca Keys to the notebook.