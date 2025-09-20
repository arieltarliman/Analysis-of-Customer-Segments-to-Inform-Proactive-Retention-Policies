# Analysis of Customer Segments to Inform Proactive Retention Policies

## Overview
This project focuses on **customer segmentation for a telecommunications company** using dataset **2B**. The objective is to cluster customers based on their behaviors and attributes, then identify actionable strategies to improve **customer retention**.

The project applies **Exploratory Data Analysis (EDA)**, **K-Means clustering**, and **cluster profiling** to deliver insights that can guide proactive retention policies.

---

## A. Exploratory Data Analysis (EDA)
- Performed data inspection to check distributions, correlations, and missing values.  
- Identified anomalies such as:
  - Outliers in call duration and data usage.
  - Inconsistent categorical entries in subscription types.  
- Handled anomalies by filtering, imputing missing values, and normalizing features for clustering.  

**Key Findings:**
- High churn tendency observed in customers with lower data usage but high monthly costs.  
- Customers with longer tenures showed lower churn likelihood.  

---

## B. K-Means Clustering
- Applied **K-Means clustering** for customer segmentation.  
- Fine-tuned number of clusters (`k`) using **two metrics**:
  - **Elbow Method (Inertia)**
  - **Silhouette Score**
- Optimal cluster count was chosen based on both metrics.  
- Visualized results using:
  - **2D PCA projection of clusters**
  - **Distribution plots of features by cluster**

---

## C. Cluster Analysis
Each cluster was profiled to identify key customer characteristics:

1. **Cluster 1 – Price-Sensitive Customers**
   - Low data usage, moderate call usage.
   - Higher churn risk due to high perceived cost.
   - **Action:** Offer tailored discount plans or flexible billing.

2. **Cluster 2 – Loyal Long-Term Customers**
   - Long tenure, stable usage patterns.
   - Low churn risk.
   - **Action:** Reward with loyalty perks to maintain satisfaction.

3. **Cluster 3 – Heavy Data Users**
   - High internet usage, strong dependency on telecom services.
   - Medium churn risk if competitors offer better deals.
   - **Action:** Provide premium packages with added benefits.

4. **Cluster 4 – New Customers**
   - Short tenure, exploratory service usage.
   - Higher churn risk in first months.
   - **Action:** Enhance onboarding, provide welcome offers.

---

## Technologies Used
- **Python 3.10**
- **Jupyter Notebook**
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/arieltarliman/Analysis-of-Customer-Segments-to-Inform-Proactive-Retention-Policies.git
   cd Analysis-of-Customer-Segments-to-Inform-Proactive-Retention-Policies
