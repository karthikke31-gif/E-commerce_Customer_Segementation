# 🛒 E-Commerce Customer Segmentation & Power BI Dashboard

### 📘 Overview
This project extends the **E-commerce Customer Segmentation** analysis by integrating a **Power BI Dashboard** for interactive visualization and insights.  
It combines RFM analysis, K-Means clustering, and descriptive analytics to understand customer behavior and revenue drivers.

---

### 🎯 Objectives
- Segment customers based on purchasing behavior and frequency  
- Identify high-, medium-, and low-value customer groups  
- Visualize key KPIs and purchasing trends in Power BI  
- Support targeted marketing and customer retention strategies  

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

![E-commerce Customer Dashboard](https://github.com/karthikke31-gif/E-commerce_Customer_Segementation/blob/cc68cf665057b2d6ab2d1ee3500e6d4b549f9fcd/Image%20of%20Customer.PNG?raw=true)


---

### ⚙️ Installation & Setup

```bash
# Clone the repository
git clone https://github.com/karthikke31-gif/E-commerce_Customer_Segementation.git
cd E-commerce_Customer_Segementation

# (Optional) Install Python dependencies for preprocessing
pip install -r requirements.txt
1.Place df_cleaned.csv in the root directory.
2.Open Online_Retail_Dashboard.pbix in Power BI Desktop.
3.Click Refresh to load and visualize the data.
---
---

### 📝 Usage

Run the Jupyter notebook sequentially to reproduce the full analysis pipeline:

1. **Data Cleaning & Preprocessing**  
   - Remove nulls, duplicates, and invalid transactions  
   - Handle cancellations and compute total sales value (`TotalPrice = Quantity * UnitPrice`)

2. **Exploratory Data Analysis (EDA)**  
   - Analyze customer purchase patterns, frequency, and sales distribution  
   - Visualize revenue by country, time, and customer segments  

3. **Feature Engineering (RFM Metrics)**  
   - Calculate **Recency**, **Frequency**, and **Monetary Value** for each customer  
   - Normalize and prepare features for clustering  

4. **Clustering (K-Means, k=3)**  
   - Apply K-Means clustering to segment customers  
   - Use PCA for dimensionality reduction and visualization  

5. **Visualization of Customer Segments**  
   - Plot clusters to identify High-, Medium-, and Low-Value customers  
   - Generate insights for marketing and retention strategies  

---

### 📈 Insights

| Segment | Characteristics | Behavior |
|----------|-----------------|-----------|
| **High-Value** | Frequent, recent buyers | Generate majority of revenue |
| **Medium-Value** | Moderate purchase volume | Regular but not premium customers |
| **Low-Value** | Infrequent or old purchases | Low activity, need re-engagement |

---

### 💡 Business Recommendations

| Segment | Actionable Strategy | Goal |

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


## 🗺️ Data Source

- Dataset:

- InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country
- Includes derived fields: TotalPrice = Quantity * UnitPrice, QuantityCanceled

## 🚀 Future Enhancements

- Real-time Power BI Service integration
- Churn prediction & CLV forecasting
- Product category segmentation
- Deployment as interactive web dashboard

## 🧩 Contributing

- Fork the repo
- Create a new feature branch
- Commit changes and open a pull request

Feedback and suggestions for dashboard improvement are always welcome!
Built with ❤️ using Python, Pandas, and Power BI.
