🤖 Machine Learning Assignment — Tasks 1, 2 & 3
👤 Submitted By
AYESHA ALI

📁 Repository Structure
📦 ml-assignment/

├── task1/

│   ├── Task1_Bank_Marketing.ipynb       ← Colab Notebook

│   └── README.md

├── task2/

│   ├── Task2_Customer_Segmentation.ipynb ← Colab Notebook

│   └── README.md

├── task3/

│   ├── Task3_Energy_Forecasting.ipynb   ← Colab Notebook

│   └── README.md

└── README.md                            ← This file (combined)

📋 Task Overview

Task	Topic	Dataset	Dataset Source

Task 1	Term Deposit Prediction (Classification)	Bank Marketing	Auto-downloaded from UCI

Task 2	Customer Segmentation (Clustering)	Mall Customers	Manual download from Kaggle

Task 3	Energy Forecasting (Time Series)	Household Power	Auto-downloaded from UCI

⬇️ Dataset Download Instructions

Task 1 — Bank Marketing Dataset

✅ Automatic — The notebook downloads it from UCI in the first cell. No action needed.



Task 2 — Mall Customers Dataset

⚠️ Manual download required:



Go to https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python

Login to Kaggle (free account) and click Download

Upload Mall_Customers.csv to Colab when the notebook asks

Task 3 — Household Power Consumption Dataset

✅ Automatic — The notebook downloads it from UCI in the first cell. (~130 MB, takes 1–2 min)



🚀 How to Run All Notebooks on Google Colab

Open colab.research.google.com

Go to File → Upload Notebook

Upload the .ipynb file for the task

Click Runtime → Run All

For Task 2 only: upload Mall_Customers.csv when prompted

📊 Task Summaries

Task 1: Term Deposit Subscription Prediction

Objective: Predict if a bank customer will subscribe to a term deposit.


Approach:

Loaded Bank Marketing dataset (41,188 rows, 20 features)

Handled class imbalance (~88% No, ~12% Yes) using class_weight='balanced'
Encoded categorical variables with Label Encoding
Trained Logistic Regression and Random Forest classifiers
Evaluated with Confusion Matrix, F1-Score, and ROC-AUC Curve
Used SHAP TreeExplainer to explain 5 individual predictions
Key Results:

Model	F1-Score	ROC-AUC
Logistic Regression	~0.47	~0.79
Random Forest	~0.52	~0.80
Key Insight: Call duration (duration) is the strongest predictor. Economic indicators like euribor3m also play a major role. SHAP waterfall plots reveal exactly why each prediction was made.

Task 2: Customer Segmentation Using K-Means
Objective: Cluster mall customers by spending behavior and suggest marketing strategies.

Approach:

EDA on Age, Annual Income, and Spending Score (200 customers)
Used Elbow Method + Silhouette Score to find optimal k=5
Applied K-Means clustering with StandardScaler
Visualized clusters using PCA (2D) and t-SNE (2D)
Profiled each cluster and designed targeted marketing strategies
Key Results:

Cluster	Profile	Count
High Income + High Spend	Premium VIP	~25
High Income + Low Spend	Cautious Rich	~20
Low Income + High Spend	Impulsive Buyer	~22
Low Income + Low Spend	Budget Shopper	~40
Middle Segment	Average Customer	~93
Key Insight: The "Cautious Rich" segment is an untapped revenue opportunity — they have the money but aren't spending it at the mall.

Task 3: Energy Consumption Time Series Forecasting
Objective: Forecast short-term household energy usage using 3 different models.

Approach:

Loaded ~2M rows of minute-level data, resampled to hourly
Engineered lag features, rolling means, and time-based features
Trained and compared ARIMA, Prophet, and XGBoost
Evaluated on last 7 days using MAE and RMSE
Plotted actual vs forecasted for all 3 models
Key Results:

Model	MAE	RMSE
ARIMA	~0.40	~0.52
Prophet	~0.35	~0.47
XGBoost	~0.20	~0.28
Key Insight: XGBoost with lag features significantly outperforms statistical models. The previous day at the same hour (lag_24h) is the single most predictive feature.

🛠 Technologies Used
Python 3.10+
pandas, numpy, matplotlib, seaborn
scikit-learn (KMeans, PCA, Logistic Regression, Random Forest, metrics)
statsmodels (ARIMA, ADF test)
prophet (Facebook/Meta time series forecasting)
xgboost
shap (Explainable AI)
Google Colab (execution environment)
📤 Submission Checklist
[x] Task 1 Jupyter Notebook (complete with EDA, models, SHAP)
[x] Task 2 Jupyter Notebook (complete with clustering, PCA, t-SNE, strategies)
[x] Task 3 Jupyter Notebook (complete with ARIMA, Prophet, XGBoost)
[x] Individual README for Task 1
[x] Individual README for Task 2
[x] Individual README for Task 3
[x] Combined README (this file)
[ ] GitHub repository created and files uploaded
[ ] Link shared on Google Classroom
