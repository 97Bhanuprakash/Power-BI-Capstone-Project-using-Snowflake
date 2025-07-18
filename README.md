# Power-BI-Capstone-Project-using-Snowflake

# 🚗 Dream Craft: Sales Data Management & Business Intelligence Solution

## 📘 Project Overview

**Dream Craft** is a global company specializing in producing and selling miniaturized classic car models and collectibles. With offices across multiple countries and a wide customer base of gift and toy retailers, Dream Craft needed a centralized system to consolidate sales data and gain actionable business insights.

This project delivers a comprehensive **data warehouse in Snowflake** and an interactive **Power BI dashboard** to enhance sales performance, customer management, and reporting capabilities.

---

## 🧩 Scenario

Dream Craft operates worldwide, with each office employing sales representatives to manage relationships with retail customers. Customers place orders for different products from Dream Craft’s catalog, often paying for multiple orders at once. The existing system struggled with:
- Fragmented sales data across locations
- Lack of centralized visibility
- Manual and inaccurate reporting

The goal was to solve these issues using:
- Centralized database in **Snowflake**
- Interactive BI dashboards using **Power BI**

---

## ❗ Problem Statement

Dream Craft faced difficulty in accurately auditing and consolidating sales data due to geographical dispersion. This project implements:
- A normalized database schema in **Snowflake**
- Data cleaning and transformation
- BI dashboard in **Power BI** for visualization and decision-making

---

## 🛠️ Tasks Completed

### ✅ Database Setup (Snowflake)
- Created Snowflake account and database named `DreamCraft`
- Built an ER model with tables: `Offices`, `Employees`, `Customers`, `ProductLines`, `Products`, `Orders`, `OrderDetails`, `Payments`
- Enforced primary and foreign key constraints
- Populated tables with sample records
- Cleaned null values (`NA`, `0`) in relevant fields
- Added calculated fields:
  - `Markup_Percentage` in `Products`
  - `Total_Cost` in `OrderDetails`
- Created SQL views:
  - `Sale_Details`
  - `High_Value_Customers`
- Stored Procedures:
  - `GET_MARKUP_HIGHER`
  - `GET_HIGHCREDIT_CUSTOMER`
- Used `OFFSET` and `UNDROP` to retrieve historical data
- Exported and loaded data into Snowflake

### ✅ Data Visualization (Power BI)
- Connected Power BI to Snowflake
- Removed high-null columns (`AddressLine2`, `HtmlDescription`)
- Built relationships per ERD
- Created two Power BI reports:

#### 📊 Report 1: Sales Performance Overview
- Gauge chart for `Markup_Percentage`
- Tree map for `Customer Count by Country`
- Card chart for `Total Revenue`
- Stacked bar for `Top 10 Customers`
- Stacked column chart for `Revenue by Month & Year`
- Slicer for `Year`

#### 📊 Report 2: Sales & Customer Insights
- Card chart for `Order Count` & `Customer Count`
- Stacked bar for `Top Selling Product Line`
- Stacked column chart for `Quantity Sold by Product`
- Pie chart for `Yearly Customer Order Count`
- Donut chart for `Shipment Status`
- Slicer for `Year`

### ✅ Power BI Service Publishing
- Published both reports
- Edited y-axis and x-axis labels
- Enabled data labels for key charts
- Enabled Q&A feature
- Pinned reports and visuals to dashboards
- Viewed Lineage and Usage Metrics

---

