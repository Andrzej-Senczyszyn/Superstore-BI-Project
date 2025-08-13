# 🛍️ Superstore BI Project — End-to-End Data Analysis & Tableau Dashboards

## 📄 Project Overview
This project delivers a complete Business Intelligence (BI) workflow — from raw data to interactive dashboards in Tableau.  
The goal was to explore *Superstore sales data* to uncover insights on profitability, customer behavior, delivery performance, and product trends.

---

## 🛠 Workflow Included:
- 🧹 **Data cleaning and transformation in Python**
- 🗂 **Building a Star Schema data model**
- 📊 **Designing KPIs and dashboards in Tableau**

---

## 🏗 Project Architecture
The solution is structured into four layers:

### 1. 📥 Data Source Layer  
**Dataset:** [Superstore Sales Dataset (Kaggle)](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)  
**Format:** CSV  
**Granularity:** Transaction-level (1 row per order line)  
**Key Fields:** Sales, Profit, Quantity, Product Details, Shipping, Customer, Region, Dates  

---

### 2. 🔄 ETL Layer (Extract, Transform, Load) — *Performed in Python (pandas)*
- Removed unnecessary columns (`Row ID`)
- Replaced missing postal codes with `0`
- Dropped rows with missing critical fields (`Order Date`, `Ship Date`, `Customer ID`)
- Added calculated column: **Delivery Delay = Ship Date − Order Date**

---

### 3. 🗃 Modeling Layer — *Star Schema Design*
**Fact Table:**  
`fact_sales` — sales, profit, discount, dates, shipping

**Dimension Tables:**
- `dim_customer` — customer details, segment, tier, repeat orders
- `dim_product` — product details, category, sub-category
- `dim_date` — order date, month, quarter, year
- `dim_shipping` — ship mode
- `dim_region` — country, region, state, city, postal code

---

## 📊 Visualization Layer (Tableau Dashboards)
The final Tableau dashboard contains **7 main pages**:

1. **Overview** — KPIs, sales map, yearly trends  
2. **Sales Analysis** — by region, category, segment  
3. **Profit Insights** — by category, product, and time  
4. **Customer Insights** — tiers, repeat orders, top customers  
5. **Product Performance** — best/worst sub-categories  
6. **Delivery Insights** — delays by region and ship mode  
7. **Time Series Analysis** — monthly & quarterly sales/profit trends  

---

## ✅ Conclusion
This project demonstrates the **full BI lifecycle**:
- Cleaned & transformed data in Python
- Modeled with a **Star Schema**
- Built **dynamic KPIs** in Tableau
- Delivered **interactive dashboards** for business decision-making
