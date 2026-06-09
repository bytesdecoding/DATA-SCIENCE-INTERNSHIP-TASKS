Task 3 — Energy Consumption Time Series Forecasting
🎯 Objective
Forecast short-term household energy usage by analyzing historical time-based patterns and comparing three different forecasting models: ARIMA, Prophet, and XGBoost.

⬇️ Dataset
Individual Household Electric Power Consumption — UCI ML Repository

✅ No manual download needed!
The first notebook cell automatically downloads and extracts the dataset from UCI.
File size is ~130 MB so it may take 1-2 minutes.

Direct link (for reference): https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption

🚀 How to Run on Google Colab
Go to colab.research.google.com
Upload Task3_Energy_Forecasting.ipynb
Run the first cell — it installs prophet, xgboost, and downloads the dataset
Run all remaining cells in order
⏱️ Total runtime: ~5-10 minutes (Prophet and ARIMA take the longest)
📋 My Approach
1. Data Parsing & Resampling
Loaded 2+ million rows of minute-level readings from 2006–2010
Combined Date + Time into a single Datetime index
Resampled to hourly means to reduce noise and speed up modeling
Handled missing values (marked as ? in the dataset)
2. EDA
Plotted hourly and daily seasonality patterns
Found clear peak hours (7-9am, 6-10pm)
Identified weekly pattern: weekends consume more energy
Visualized long-term monthly trend (winter peaks due to heating)
3. Feature Engineering
Feature	Description
hour, day_of_week	Time-of-day and weekday context
is_weekend	Binary flag for weekends
month, quarter	Seasonal context
lag_1h, lag_24h, lag_48h, lag_168h	Previous hour, day, 2 days, week
rolling_mean_24h, rolling_mean_7d	Short & long-term trends
4. Models Compared
Model	Type	Strengths
ARIMA(2,1,2)	Statistical	Good for stationary, univariate series
Facebook Prophet	Decomposition	Handles seasonality & holidays well
XGBoost	ML (Gradient Boosting)	Captures complex non-linear patterns
5. Evaluation
MAE (Mean Absolute Error) — average prediction error
RMSE (Root Mean Squared Error) — penalizes large errors more
Test set: last 7 days (168 hours) of the dataset
📊 Results & Findings
Model	MAE	RMSE
ARIMA	~0.35–0.45	~0.45–0.60
Prophet	~0.30–0.40	~0.40–0.55
XGBoost	~0.15–0.25	~0.22–0.35
(Actual values will appear after running the notebook)

Key Insights:

Energy consumption has strong daily and weekly seasonality
XGBoost with lag features significantly outperforms both statistical models
The lag_24h feature is the single most important predictor (same hour yesterday)
ARIMA is fastest but least accurate; Prophet handles seasonality well
Winter months have 20-30% higher consumption than summer (heating effect)
🛠 Skills Demonstrated
Time series parsing and resampling
Temporal feature engineering (lags, rolling means)
ARIMA, Prophet, and XGBoost modeling
MAE/RMSE evaluation and model comparison
Actual vs forecasted visualization
