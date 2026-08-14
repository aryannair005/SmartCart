# SmartCart: E-commerce Customer Segmentation System

## Overview

SmartCart is a customer segmentation system built using unsupervised machine learning. The objective of this project is to identify groups of customers with similar purchasing behaviour so that an e-commerce company can better understand its customer base and design personalized marketing strategies.

Instead of treating every customer the same, the system discovers hidden patterns in customer demographics, purchasing habits, and engagement data to create meaningful customer segments.

---

## Problem Statement

The dataset contains information for 2,240 customers collected from an e-commerce platform. Although the company has access to demographic and purchasing data, it currently follows a generic marketing strategy for all customers.

The goal of this project is to segment customers into distinct groups based on their behaviour, allowing the business to:

- Identify high-value customers
- Improve customer retention
- Design targeted marketing campaigns
- Support data-driven business decisions

---

## Dataset

The dataset contains 2,240 customer records with 22 features describing customer demographics, purchase history, website activity, and campaign responses.

The major categories of features include:

- Customer demographics
- Income
- Purchase amounts across different product categories
- Purchase frequency
- Website visits
- Customer complaints
- Campaign responses

---

## Project Workflow

### 1. Data Preprocessing

The preprocessing stage focused on improving data quality before applying clustering algorithms.

The following tasks were performed:

- Missing values in the Income column were handled using median imputation.
- New features such as Age, Customer Tenure, Total Spending, and Total Children were created.
- Education and Marital Status were simplified into fewer business-relevant categories.
- Original columns that became redundant after feature engineering were removed.
- Extreme outliers in Age and Income were filtered to reduce their impact on clustering.

---

### 2. Exploratory Data Analysis

To better understand the dataset before clustering:

- Pair plots were used for visual inspection of outliers.
- A correlation heatmap was generated to study relationships between numerical features.

This step provided insights into customer behaviour and feature relationships.

---

### 3. Feature Encoding

Categorical variables were converted into numerical form using One-Hot Encoding.

Encoded features included:

- Education
- Living_With

---

### 4. Feature Scaling

Since clustering algorithms are distance-based, all numerical features were standardized using StandardScaler.

---

### 5. Dimensionality Reduction

Principal Component Analysis (PCA) was applied to reduce the dataset into three principal components.

The reduced representation was used only for visualization and cluster analysis.

---

### 6. Determining the Optimal Number of Clusters

Two evaluation techniques were used to determine the appropriate number of clusters:

- Elbow Method
- Silhouette Score

Both methods suggested that four clusters provide a suitable segmentation of the customer base.

---

### 7. Customer Segmentation

Two clustering algorithms were implemented and compared:

#### K-Means Clustering

Used to partition customers into four clusters based on feature similarity.

#### Agglomerative Clustering

Hierarchical clustering using Ward linkage was applied to compare its segmentation with K-Means.

---

### 8. Cluster Analysis

After clustering, each customer was assigned to a cluster.

The clusters were analyzed using:

- Income
- Total Spending
- Purchase Frequency
- Website Activity
- Customer Tenure
- Family Size

Cluster summaries and visualizations were generated to understand the characteristics of each customer group.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

Machine Learning techniques:

- One-Hot Encoding
- StandardScaler
- Principal Component Analysis (PCA)
- K-Means Clustering
- Agglomerative Clustering

---

## Results

The project successfully segmented customers into four distinct groups based on purchasing behaviour and customer attributes.

The generated segments can support:

- Personalized marketing
- Customer retention strategies
- Targeted promotional campaigns
- Customer behaviour analysis

---

## Repository Structure

```
SmartCart/
│
├── SmartCart.ipynb
├── smartcart_customers.csv
├── README.md
```

---

## Future Improvements

Potential extensions to this project include:

- Deploying the model using Streamlit
- Comparing additional clustering algorithms such as DBSCAN
- Automating cluster labeling based on business rules
- Integrating the system with a recommendation engine

---

## Author

Aryan Nair