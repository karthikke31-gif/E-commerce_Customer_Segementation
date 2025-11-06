# Customer Segmentation & Churn Prediction | Machine Learning Project & Power BI Dashboard

### 📘 Overview
This project extends Customer Segmentation analysis with enhanced insights into customer patterns, churn behavior, and retention strategies. 

This project performs **end-to-end customer analytics** using real retail transaction data, including:

✅ Data Cleaning & Feature Engineering  
✅ Unsupervised Learning (Customer Segmentation)  
✅ Supervised Learning (Churn Prediction)  
✅ PCA for Dimensionality Reduction  
✅ Model Evaluation & Business Recommendations  

---


---

## 🎯 Project Objective

To understand customer behavior, classify customers into actionable segments, and **predict churn probability** to support retention & marketing strategies.

---

## 📦 Dataset Overview

- **406,829 transactions**
- **4,339 customers**
- **37 countries**
- 8 key retail variables used:
  `InvoiceNo`, `StockCode`, `Description`, `Quantity`,  
  `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🧹 Data Cleaning

- Removed null `CustomerID` (~24.9%)
- Cleaned text descriptions & corrected spellings
- Handled cancellation invoices (~16%)
- Final dataset after cleaning: **392,857 valid transactions**

---

## 🛠️ Feature Engineering

Customer-level features created:

| Category | Features |
|---|---|
Engagement | # Transactions, Frequency  
Value | Total Spend, Avg Spend, Quantity  
Lifecycle | Recency, Customer Lifespan  

➡️ PCA applied — **95.6% variance explained by first 6 components**

---

## 🤖 Machine Learning Approach

### 📊 Segmentation (Unsupervised Learning)
| Method | Result |
|---|---|
K-Means (k=3) | 3 customer clusters identified  
Metric | Silhouette Score optimization  

### 👥 Customer Segments

| Segment | Profile | Count | Insight |
|---|---|---|---|
High-Value | Loyal, frequent buyers | 2,517 | Sales growth potential |
Medium-Value | Irregular buyers | 1,802 | **High churn risk** |
Low-Value (VIP) | Sparse, big orders | 20 | Personalized attention |

---

## 🔁 Churn Labeling Strategy

- **Churn definition:** No purchase in last **90 days**
- Churn % ≈ **33%**
- Train-test split with **stratified sampling**
- Removed low-value VIP outliers to avoid bias

---
## 🌍 Geographical Churn
-- United Kingdom:
•	3,921 customers (~90% of total base)
•	33.3% churn rate — stable baseline with strong engagement (avg. frequency 0.93 transactions/day)

-- France & Germany:

•	87 and 94 customers respectively
•	Churn rates of 29.9% (France) and 26.6% (Germany) — slightly lower than UK but with reduced engagement (avg. frequency ~0.24/day in churned cohorts)
•	These insights indicate that while churn rates are moderate across key markets, engagement intensity differs significantly by geography.

---

## 🧠 Predictive Models

| Model | Accuracy | AUC-ROC | Notes |
|---|---|---|---|
Logistic Regression | 76% | 0.80 | Strong baseline  
Random Forest | 73% | 0.795 | Great interpretability  
SVM (PCA) | 61% | 0.719 | High recall, low precision  
**Ensemble (Best)** | **75%** | **0.815** | Most stable & best AUC |

### 🧾 Feature Importance (Random Forest)

1. Total Spending  
2. Purchase Frequency  
3. Segment (Medium most risky)  
 

---

## 🧠 Key Insights

### 🔥 Segment-Wise Churn

| Segment | Churn Rate | Action |
|---|---|---|
High | ~13.5% | Upsell & loyalty rewards |
Medium | ~61.4% | **Urgent re-engagement** |
Low / VIP | N/A | High-touch concierge support |

### 📌 Business Recommendations

✅ Target Medium segment with retention offers  
✅ Reward High-value customers (loyal base)  
✅ Use spend + frequency signals to trigger churn alerts  

---

## 🛡️ Technical Stack

| Category | Tools |
|---|---|
Language | Python  
Libraries | Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn, NLTK  
Techniques | PCA, Clustering, Logistic Regression, Ensemble Models  
ML Metrics | Accuracy, Precision, Recall, F1, ROC-AUC  

---

## 📈 Results Summary

| Metric | Score |
|---|---|
Best Model | **Ensemble**  
Accuracy | **75%**  
AUC | **0.815**  

---

## 📌 Future Improvements

- Deploy model as an API / Web App
- Add deep learning-based churn prediction
- Real-time RFM + event based churn triggers
- Power BI / Tableau dashboard integration

---




---

### 📊 Dashboard Features
- **KPI Cards:** Total Revenue, Quantity Sold, Orders, Average Order Value  
- **Time-Series Chart:** Monthly/Yearly Sales Trends (with Country filter)  
- **Top Products Chart:** Top 10 Products by Revenue and Quantity  
- **Customer Table:** Top Customers by Orders & Revenue  
- **Map View:** Revenue Distribution by Country  
- **Cancellation Analysis:** Track return and refund impact over time  
- **Interactive Slicers:** Filter by Country, Date Hierarchy, and Cancellation Status  

### 🖼️ Dashboard Preview

![E-commerce Dashboard](https://github.com/karthikke31-gif/E-commerce_Customer_Segementation/blob/2b903851f956f020d4804e07982c0328b6b6d322/Image%20of%20Customer.PNG)

---

### ⚙️ Installation & Setup


# Clone the repository
git clone https://github.com/karthikke31-gif/E-commerce_Customer_Segementation.git
cd E-commerce_Customer_Segementation

# (Optional) Install Python dependencies for preprocessing
pip install -r requirements.txt
1.Place df_cleaned.csv in the root directory.
2.Open Online_Retail_Dashboard.pbix in Power BI Desktop.
3.Click Refresh to load and visualize the data.

---

### 🧮 DAX Measures Used
- DAX 
- Total Revenue = SUM(df_cleaned[TotalPrice])
- Number of Orders = DISTINCTCOUNT(df_cleaned[InvoiceNo])
- Cancellation Rate = 
- DIVIDE(
   - SUM(df_cleaned[QuantityCanceled]),
   -  SUM(df_cleaned[Quantity]) + SUM(df_cleaned[QuantityCanceled]),
  -  0
-)



## 🚀 Future Enhancements

- Real-time Power BI Service integration
- Product category segmentation
- Deployment as interactive web dashboard

## 🧩 Contributing

- Fork the repo
- Create a new feature branch
- Commit changes and open a pull request

Feedback and suggestions for dashboard improvement are always welcome!
Built with ❤️ using Python, Pandas, and Power BI.
