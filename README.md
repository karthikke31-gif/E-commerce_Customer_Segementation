git add screenshots/
git commit -m "Image of Customer"
git push



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

### 🖼️ Dashboard Previews
Image of Customer.png
![Dashboard Overview](Image of Customer.png)

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

💡 Key Insights

High-Value Customers: Frequent and recent buyers — ideal for loyalty programs.

Medium-Value Customers: Good purchase volume — target with upsell offers.

Low-Value Customers: Low frequency — engage via discount campaigns.

Peak Sales: Observed around holiday months (e.g., December).

Cancellation Rate: ~2–3% — requires policy monitoring.

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
