
Task 2 — Customer Segmentation Using Unsupervised Learning
🎯 Objective
Cluster mall customers based on their age, annual income, and spending score to identify distinct customer segments and propose targeted marketing strategies.

⬇️ Dataset
Mall Customers Dataset — Kaggle

⚠️ Manual download required from Kaggle

Steps:

Go to: https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python
Click Download (you need a free Kaggle account)
You'll get Mall_Customers.csv
Option A: Upload kaggle.json API token to Colab and run the Kaggle API cell
Option B: Upload Mall_Customers.csv directly to Colab using the manual upload cell
🚀 How to Run on Google Colab
Go to colab.research.google.com
Upload Task2_Customer_Segmentation.ipynb
Download Mall_Customers.csv from Kaggle (link above)
Upload it to Colab when prompted (Option B cell)
Run all remaining cells in order
📋 My Approach
1. EDA
Analyzed distributions of Age, Annual Income, and Spending Score
Checked gender split and its effect on spending behavior
Used pairplot to visually identify natural groupings
2. Finding Optimal Clusters
Applied the Elbow Method (plotting inertia/WCSS for k=1 to 10)
Verified with Silhouette Score (higher = better defined clusters)
Chose k=5 based on both methods agreeing
3. K-Means Clustering
Scaled features with StandardScaler before clustering
Fitted KMeans(n_clusters=5) on Age, Annual Income, Spending Score
Analyzed cluster centroids in original scale for interpretation
4. Dimensionality Reduction
Method	Purpose
PCA	Linear reduction, preserves global variance
t-SNE	Non-linear reduction, preserves local cluster structure
5. Marketing Strategy Development
Named each cluster based on income/spending profile
Designed a targeted marketing approach per segment
📊 Results & Findings
Cluster	Profile	Strategy
High Income + High Spend	Premium spenders	VIP loyalty rewards, exclusive events
High Income + Low Spend	Cautious rich	Value messaging, personalized discounts
Low Income + High Spend	Impulsive buyers	EMI options, flash sales, FOMO tactics
Low Income + Low Spend	Budget shoppers	Coupons, bundles, essential deals
Middle Income + Mid Spend	Average customers	Seasonal promos, cross-sell campaigns
Key Insights:

5 distinct, well-separated customer groups were found
Both PCA and t-SNE confirmed clear cluster boundaries
The "Cautious Rich" segment is an untapped revenue opportunity
Silhouette score confirmed k=5 as the optimal number of clusters
🛠 Skills Demonstrated
K-Means clustering
Elbow Method and Silhouette analysis
PCA and t-SNE dimensionality reduction
Customer profiling and segmentation
Data-driven marketing strategy development
