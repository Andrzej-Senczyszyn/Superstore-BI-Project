📊 Superstore BI Project — End-to-End Data Analysis & Tableau Dashboards
📝 Project Overview
This project delivers a complete Business Intelligence (BI) workflow — from raw data to interactive dashboards in Tableau.
The objective was to explore Superstore sales data to uncover insights on profitability, customer behavior, delivery performance, and product trends.

The workflow included:

Data cleaning and transformation in Python

Building a Star Schema data model

Designing KPIs and dashboards in Tableau

🏗 Project Architecture
The solution is structured into four layers:

1. 📥 Data Source Layer
Dataset: Superstore Sales Dataset (Kaggle)

Format: CSV

Granularity: Transaction-level (1 row per order line)

Key Fields: Sales, Profit, Quantity, Product Details, Shipping, Customer, Region, Dates

2. 🔄 ETL Layer (Extract, Transform, Load)
Performed in Python (pandas):

Removed unnecessary columns (Row ID)

Replaced missing postal codes with 0

Dropped rows with missing critical fields (Order Date, Ship Date, Customer ID)

Added calculated column: Delivery Delay = Ship Date - Order Date

3. 🗃 Modeling Layer
Designed a Star Schema for reporting:

Fact Table: fact_sales — sales, profit, discount, dates, shipping

Dimension Tables:

dim_customer — customer details, segment, tier, repeat orders

dim_product — product name, category, sub-category

dim_date — day, month, quarter, year

dim_region — country, region, city, postal code

dim_ship_mode — shipping method

4. 📊 Visualization Layer
Interactive dashboards built in Tableau to answer core business questions.

📍 Dashboard Pages
Overview

KPIs: Total Sales, Profit, Profit Margin, Order Count

Annual sales trend (line chart)

Sales map by region

Sales Analysis

Sales by category, segment, region

Top sub-categories

Profit Analysis

Profit by category

Profit per order

Profit margin trend over time

Customer Insights

Top customers by sales

Repeat customers list

Delivery Insights

Average delivery delay

Delay by region

Delay by shipping mode

🎯 Key Results
Clean, scalable data model ready for BI solutions

Reusable KPI calculations for strategic decision-making

Clear, visually appealing Tableau dashboards

Identification of top products, high-value customers, and efficient shipping methods

📂 Repository Structure
bash
Копіювати
Редагувати
/data          → raw dataset files
/notebooks     → Python ETL scripts
/dashboards    → Tableau dashboard exports & screenshots
README.md      → project documentation
📎 Next Steps
Automate data refresh for real-time dashboards

Add predictive analytics (e.g., sales forecasting)

Extend comparative analysis to multi-year trends

