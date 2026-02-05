# NVDA Price Prediction using Random Forest

This project builds a machine learning model to predict short-term NVIDIA (NVDA) stock price movements using historical market data and technical indicators.

The goal is not to perfectly predict future prices, but to evaluate whether machine learning can extract meaningful signals from past price behavior.

---

##  Project Overview

- **Model**: Random Forest Regressor  
- **Target**: Next trading day's return / price movement  
- **Data Source**: Alpaca Markets API  
- **Time Period**: 2022-01-01 → 2026-02-04  
- **Evaluation Metric**: Mean Absolute Error (MAE)

---

##  Features Used

The model uses common technical indicators, including:

- Simple Moving Averages (SMA 10, SMA 20)
- Relative Strength Index (RSI 14)
- Rolling Volatility
- Lagged daily returns

Feature importance analysis confirms the model prioritizes momentum and trend-based indicators, consistent with financial intuition.

---

##  Model Evaluation & Visualization

Several visualizations are used to interpret model behavior:

- **Actual vs Predicted Returns**  
  Shows directional alignment and smoothing behavior typical of Random Forest models.

- **Cumulative Returns Comparison**  
  Highlights conservative bias and reduced volatility in predictions.

- **Feature Importance Plot**  
  Confirms reliance on technically meaningful signals.

The model performs well during stable market regimes and shows increased error during high-volatility periods, indicating regime sensitivity rather than overfitting.

---

##  Limitations

- Predictions are based solely on historical price data.
- Random Forest models smooth extreme price movements and cannot extrapolate well during sudden regime changes.
- This model is not intended as a live trading strategy.

---

##  Future Improvements

- Compare with linear regression and gradient boosting models
- Reframe prediction as classification (up/down movement)
- Add macro or volume-based features
- Walk-forward validation

---

##  Tech Stack

- Python
- pandas
- numpy
- matplotlib
- scikit-learn
- Alpaca Markets API

---

##  Disclaimer

This project is for educational and research purposes only.  
It does not constitute financial advice.
