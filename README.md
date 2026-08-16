# SmartCart Clustering System 🛒

An end-to-end unsupervised machine learning solution designed to segment e-commerce customers into actionable behavioral clusters, optimizing targeted marketing campaigns and improving customer retention strategies.

---

## 📌 Problem Statement

SmartCart serves a global customer base but previously relied on generic, one-size-fits-all marketing strategies. This lack of behavioral personalization caused:
* Inefficient allocation of marketing spend.
* Missed opportunities to reward and retain high-value customers.
* Delayed detection of churn-prone users.

This project addresses these challenges by developing an intelligent segmentation model that analyzes 2,240 customer records across 22 attributes to discover hidden behavioral patterns and drive data-backed decision-making.

---

## 📊 Dataset Overview

The dataset consists of **2,240 customer records** spanning four main operational categories:

| Category | Key Attributes | Description |
| :--- | :--- | :--- |
| **Demographics** | `Year_Birth`, `Education`, `Marital_Status`, `Income`, `Kidhome`, `Teenhome`, `Dt_Customer` | Customer background, household composition, and registration date. |
| **Monetary Spending** | `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds` | Spending breakdown across individual product lines over the last 2 years. |
| **Purchasing Channels** | `NumDealsPurchases`, `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`, `NumWebVisitsMonth` | Frequency of transactions across web, catalog, physical stores, and deal usage. |
| **Recency & Feedback** | `Recency`, `Complain` | Days elapsed since last purchase and customer complaint record ($1 = \text{Yes}, 0 = \text{No}$). |

---

## 🛠️ Project Workflow

1. **Data Preprocessing & Cleaning**:
   * Handled missing values in continuous variables (e.g., `Income`).
   * Engineered features: total household spend, age calculation, total children, and customer tenure.
   * Encoded categorical features and standardized data using `StandardScaler`.

2. **Dimensionality Reduction & Modeling**:
   * Applied **Principal Component Analysis (PCA)** for dimensionality reduction while preserving peak variance.
   * Executed **K-Means Clustering** and **Agglomerative Hierarchical Clustering**.
   * Validated cluster count using **Elbow Method** and **Silhouette Score metrics**.

3. **Cluster Insights & Behavioral Segmentation**:
   * **High-Value VIPs**: High income, high spend on premium categories, low deal dependence.
   * **Bargain Hunters**: Moderate income, high interaction with discounted deals (`NumDealsPurchases`), frequent site visits.
   * **At-Risk Accounts**: High recency (long period of inactivity), low overall spend, low engagement.

---

## 💻 Tech Stack

* **Language**: Python 3.x
* **Libraries**: Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn
* **Environment**: Jupyter Notebook / VS Code

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone [https://github.com/Nirbhay404/Smart-Cart-Clustering-System.git](https://github.com/Nirbhay404/Smart-Cart-Clustering-System.git)
