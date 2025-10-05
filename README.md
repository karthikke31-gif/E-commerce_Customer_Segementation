# E-commerce Customer Segmentation 🚀

[![Python](https://img.shields.io/badge/python-3.12+-blue.svg)](https://www.python.org/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)  
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](Customer_Segmentation.ipynb)

---

## 🔍 Overview
Segment e-commerce customers based on purchasing behavior using **RFM analysis**, **K-Means clustering**, and **PCA**.  
Helps identify **high-value**, **medium-value**, and **low-value** customers for targeted marketing, retention, and revenue optimization.

---

## 🎯 Objectives
- Identify customer segments by behavior & transaction history  
- Recognize high-value customers driving revenue  
- Understand purchase patterns, frequency, and geography  
- Enable personalized marketing campaigns & offers  

---

## 📊 Dataset
**Source:** Retail transactions (`data.csv`)  
**Rows:** 541,909 (raw), 406,829 (cleaned)  

**Key Columns:**  
- `InvoiceNo` – Transaction ID  
- `StockCode` – Product code  
- `Description` – Product name  
- `Quantity` – Units purchased  
- `InvoiceDate` – Timestamp  
- `UnitPrice` – Price per unit  
- `CustomerID` – Customer identifier  
- `Country` – Customer location  

**Notes:** Includes cancellations and special codes (e.g., postage fees).  

## 📝 Usage

Run the notebook sequentially:

1. **Data Cleaning & Preprocessing**  
2. **Exploratory Data Analysis (EDA)**  
3. **Feature Engineering (RFM metrics)**  
4. **Clustering (K-Means, k=3)**  
5. **Visualization of Customer Segments**  

---

## 📈 Insights

- **High-Value:** Frequent, recent buyers  
- **Medium-Value:** High-volume, high-value  
- **Low-Value:** Infrequent, older purchases  

---

## 💡 Business Recommendations

- **High-Value:** VIP programs, personalized offers  
- **Medium-Value:** Upsell bundles, frequency incentives  
- **Low-Value:** Re-engagement campaigns, discounts for repeat purchases  

---

## ⚠️ Limitations

- Static dataset (no real-time updates)  
- No demographic or external features included  
- Assumes spherical clusters (other clustering methods may improve accuracy)  

---

## 🚀 Future Work

- Churn prediction using machine learning  
- Customer lifetime value forecasting  
- Deploy as an interactive web app for segmentation

---

## ⚙️ Installation
```bash
# Clone repository
git clone [https://github.com/your-username/ecommerce-customer-segmentation.git](https://github.com/karthikke31-gif/E-commerce_Customer_Segementation/tree/main)
cd ecommerce-customer-segmentation

# Install dependencies
pip install -r requirements.txt
