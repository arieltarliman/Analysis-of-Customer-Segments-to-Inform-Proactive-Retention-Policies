# Analysis of Customer Segments to Inform Proactive Retention Policies

## 🚀 Introduction

This project presents a data-driven approach to understanding customer behavior within a telecommunications company. By leveraging unsupervised machine learning, specifically **K-Means clustering**, this analysis segments customers into distinct groups based on their demographic information, service usage, and satisfaction levels. The ultimate goal is to uncover actionable insights that can inform the development of proactive retention policies, thereby reducing customer churn and improving overall business health.

The analysis is documented in the accompanying Jupyter Notebook, which details each step from data cleaning and exploration to model training and cluster interpretation.

***

## 🎯 Problem Statement

The primary objective of this project is to **segment the customer base of a telecommunications company into meaningful clusters**. By analyzing the distinct characteristics of each cluster, the project aims to identify and recommend specific, targeted actions that the company can undertake to improve customer retention and satisfaction.

***

## 📊 Dataset

The analysis utilizes the "Dataset 2B (telecommunications customers)," which contains a rich set of attributes for each customer. The key features include:

* **Customer Demographics**: Gender, Age (derived from Birth Date), Marital Status, and Dependents.
* **Service Usage**: Tenure in months, average monthly long-distance charges, internet service and type, and average monthly GB download.
* **Subscription Details**: Information on subscriptions to services like premium tech support and streaming movies/music.
* **Contract and Billing**: Contract type, paperless billing status, and payment method.
* **Engagement and Satisfaction**: Number of referrals made and customer satisfaction score.

***

## 🛠️ Methodology

The project follows a structured data science workflow to ensure robust and reliable results.

### 1. Exploratory Data Analysis (EDA)

A thorough EDA was performed to understand the dataset's structure, identify key patterns, and handle anomalies. The main steps included:

* **Data Cleaning**: Checked for and handled missing values, specifically in the `Internet Type` column, where `None` was imputed for customers without internet service. Duplicated values were also checked, and none were found.
* **Feature Engineering**:
    * The `Birth Date` column was converted into an `Age` column for more effective modeling.
    * A binary `Refunds_Status` feature was created from the `Total Refunds` column due to high data imbalance.
* **Handling Redundancy and High Cardinality**:
    * Uninformative columns like `Customer ID` and `Country` (containing only one unique value) were dropped.
    * The `Number of Dependents` column was found to be redundant with the `Dependents` column and was subsequently removed.
    * The `City` column, with its high cardinality (1106 unique values), was dropped as it was unlikely to provide meaningful clustering insights for the project's objective.
* **Data Visualization**: Histograms, box plots, and count plots were used to visualize the distributions of numerical and categorical features, providing initial insights into customer characteristics.

### 2. K-Means Clustering

A K-Means clustering model was trained to segment the customers. The process was fine-tuned using the following metrics to determine the optimal number of clusters:

* **Elbow Method**: This technique was used to identify the point where the within-cluster sum of squares (WCSS) starts to diminish, suggesting an appropriate number of clusters.
* **Silhouette Score**: The silhouette score was analyzed for different numbers of clusters to measure how similar an object is to its own cluster compared to other clusters.

Based on these metrics, **two distinct customer clusters** were identified as the optimal segmentation for this dataset.

### 3. Cluster Analysis and Visualization

After clustering, the data was visualized using Principal Component Analysis (PCA) to reduce dimensionality and plot the clusters in a 2D space. The characteristics of each cluster were then thoroughly analyzed by examining the distribution of various features within each segment.

***

## 📈 Key Findings & Analysis of Customer Segments

The analysis revealed two primary customer segments with distinct profiles:

### Cluster 0: The Engaged and High-Value Customers

* **Demographics**: This cluster has a balanced gender distribution and tends to include customers who are married and have dependents.
* **Service Engagement**: These customers are highly engaged with the company's services, showing a strong preference for **Fiber Optic internet**. They are also more likely to subscribe to premium services like tech support and streaming options.
* **Contract and Billing**: A significant portion of this cluster is on **one-year or two-year contracts**, indicating a higher level of commitment. They predominantly use bank withdrawals and credit cards for payments.
* **Satisfaction**: While satisfaction scores vary, this cluster shows higher peaks in satisfaction, suggesting that when their needs are met, they are very happy with the service.

### Cluster 1: The Casual and Low-Engagement Customers

* **Demographics**: This group also has a balanced gender mix but is more likely to be unmarried and without dependents.
* **Service Engagement**: These customers show lower engagement with internet services, with a large number having **no internet service at all**. For those who do, DSL is a common choice. They rarely opt for premium support or streaming services.
* **Contract and Billing**: The majority of this cluster is on **month-to-month contracts**, making them a higher churn risk. They show a higher preference for mailed checks compared to Cluster 0.
* **Satisfaction**: Satisfaction levels in this cluster are more consistent but generally lower than the peaks seen in Cluster 0, indicating a baseline level of satisfaction without high levels of delight.

***

## 💡 Actionable Insights & Recommendations

Based on the cluster analysis, the following strategic recommendations are proposed to enhance customer retention:

### Customer Behavior and Satisfaction Analysis:

The referral program shows room for improvement across both clusters, though there's potential for growth. The satisfaction scores tell an intriguing story: Cluster 0 shows higher satisfaction peaks but more variability, while Cluster 1 maintains more consistent, though lower, satisfaction levels. This suggests different expectations and needs between the segments.

### Action Plan for Customer Experience:

1.  **Referral Program Revamp**
    * Implement referral challenges with special prizes.
    * Develop social media sharing incentives.

2.  **Satisfaction Enhancement Program**
    * Establish regular customer feedback sessions.
    * Create a VIP support line for high-value customers.
    * Launch a customer appreciation program.

3.  **Personalized Engagement Strategy**
    * Create customized service recommendations.
    * Launch a customer loyalty recognition program.

***

## ⚙️ How to Reproduce

To reproduce this analysis, you can follow these steps:

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/arieltarliman/Analysis-of-Customer-Segments-to-Inform-Proactive-Retention-Policies.git](https://github.com/arieltarliman/Analysis-of-Customer-Segments-to-Inform-Proactive-Retention-Policies.git)
    ```
2.  **Install dependencies**: Ensure you have Python and the necessary libraries (e.g., pandas, scikit-learn, seaborn) installed.
3.  **Run the Jupyter Notebook**: Open and run the `UAS NO 2.ipynb` notebook to see the full analysis.
