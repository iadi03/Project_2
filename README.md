1.🌾 Prediction of Agriculture Crop Production in India

📌 Project Overview
This project focuses on analyzing and predicting agricultural crop production trends in India using historical data (2001–2014) sourced from [data.gov.in](https://data.gov.in/). The goal is to gain actionable insights through data cleaning, exploratory data analysis (EDA), and machine learning modeling to support decision-making in agricultural planning.

✅ Data cleaning: standardizing column names, handling missing values  
✅ Filtered crop production records from broader dataset  
✅ Reshaped wide-format data (year columns) into long-format for time-series analysis  
✅ Visualizations:
  - Top 10 crops by total production
  - Year-wise production trends

2. Quality Prediction in a Mining Process.

📌 Project Overview
This project implements a machine learning–based predictive analytics system for a real-world mining flotation plant. The primary objective is to forecast the % Silica Concentrate in iron ore to enable proactive decision-making, reduce impurities, and optimize plant operations. Using industrial process data sampled at both minute and hourly intervals, the system provides accurate short-term and multi-hour-ahead forecasts.

🎯 Objectives
  Predict % Silica Concentrate every minute.
  Forecast silica concentration hours ahead to support preventive actions.
  Evaluate model performance with and without the highly correlated % Iron Concentrate feature.

📂 Dataset
Source: Real process data from a mining flotation plant.
Timeframe: March 2017 – September 2017.

Content:

  Initial pulp quality measurements.
  Process parameters (air flow, pulp levels, feed rates).
  Final quality measurements from the lab.
  Target Variable: % Silica Concentrate in the final ore.

⚙️ Methodology
Data Preprocessing

  Convert timestamps and handle invalid dates.
  Replace commas with decimal points for numerical consistency.
  Remove or impute missing values.
  Feature Engineering
  Lag features (1h, 2h, 3h) to capture time dependencies.
  Rolling mean features for smoothing fluctuations.

Model Development

  Baseline: Random Forest Regressor.
  Advanced: XGBoost Regressor.
  Time-series aware evaluation with TimeSeriesSplit.

Evaluation Metrics

  R² Score for variance explanation.
  RMSE (Root Mean Squared Error) for prediction error.

Horizon Testing

  Predictions at multiple forecast horizons: 1h, 2h, 4h, 6h, 12h, 24h.
  Performance drop visualized over increasing horizons.

📊 Results
  High accuracy for short-term predictions with % Iron Concentrate feature included.
  Significant performance drop when excluding % Iron Concentrate, confirming its strong correlation with % Silica         Concentrate.
  Lag and rolling features improved predictions in absence of % Iron Concentrate.
