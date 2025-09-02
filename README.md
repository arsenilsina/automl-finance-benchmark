# AutoML Benchmark on Financial Time Series

This project benchmarks AutoML frameworks (Optuna + Random Forest / Gradient Boosting) on **financial time series**, focusing on **daily stock returns**.

## Goals
- Evaluate AutoML on noisy, real-world stock data.
- Compare regression (predicting next-day returns) vs classification (up/down direction).
- Highlight the importance of **feature engineering, baselines, and realistic evaluation (TimeSeriesSplit)**.

## Datasets
- Yahoo Finance (AAPL)
- Daily data (2015–2024)
- Feature engineering: returns, moving averages, volatility, momentum, volume changes.

## Methods
- **Regression task:** predict next-day return (continuous).
- **Classification task:** predict up/down direction.
- **Models:** RandomForest, HistGradientBoosting, tuned with **Optuna**.
- **Evaluation:** 
  - Regression: MAE, RMSE, R2
  - Classification: Accuracy, Balanced Accuracy, F1
  - Baselines: majority class, persistence

## Results
- **Regression:**  
  - With engineered features, achieved MAE close to 0.01.  

- **Classification:**  
  - TimeSeriesSplit accuracy fluctuated between 46–57%, averaging ~50%.  
  - Baselines (majority, persistence) achieved similar results.  
  - Difficult problem of short-term direction prediction.  

## Key Insights
- AutoML can fit **price levels and returns with engineered features**, but struggles with direction classification.  
- **Baselines and realistic evaluation** are important to avoid misleading results.   

## Repo Structure
