 Company-Sales-Analysis-three-years-
📊 Interactive Power BI report analyzing $9.6M in export sales across countries, product lines, and years using JSON data, DAX, and advanced modeling.
 🌍 Export Sales Performance Dashboard | Power BI + DAX + JSON

This is a full-scale,  BI project that transforms raw JSON data into an interactive sales intelligence report — covering product lines, regions, customer trends, and profit metrics. With **$9.6M in total sales**, this project brings together robust data modeling, advanced DAX measures, and dynamic Power BI visuals to tell a story that matters.

---

 📁 Dataset Overview

The dataset was provided in **JSON format**, mimicking raw ERP-style data with multiple embedded layers — including:

- 📦 Product Details (productName, productLine, profit, sales)
- 📅 Order Records (orderDate, year, quantity)
- 🌍 Country & Region Info (customer, location)
- 📊 Employee & Office Data

> Total Sales: **$9.6M**  
> Total Profit: **$3.83M**  
> Time Frame: **2003–2005**  
> Product Lines: **Classic Cars**, **Vintage Cars**, **Motorcycles**, etc.

---

 🧹 Data Preparation & Modeling

 ✅ Step-by-Step Process

1. **Converted JSON to Table** via Power Query Editor  
2. **Flattened nested fields** (product info, customer details)
3. Fixed data inconsistencies:
   - Removed duplicate order records
   - Standardized date fields and converted to `datetime`
   - Formatted currency fields
4. Created a **star schema** with:
   - Fact Table: `Orders`
   - Dim Tables: `Products`, `Customers`, `Dates`, `Offices`

5. Added custom columns:
   - `order_month`, `order_year`, `product_category`
   - Split customer names and country for mapping

---

 🧠 Key DAX Measures

DAX
Total Sales = SUM('Sales'[sale])

Total Profit = SUM('Sales'[profit])

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Sales Growth % = 
DIVIDE(([Sales_This_Year] - [Sales_Last_Year]), [Sales_Last_Year], 0)

Most Ordered Product =
CALCULATE(
    FIRSTNONBLANK(Sales[productName], 1),
    TOPN(1, SUMMARIZE(Sales, Sales[productName], "Qty", SUM(Sales[quantityOrdered])), [Qty], DESC)
)



⚙️ Also used conditional formatting, ranking functions, and time intelligence across multi-year data

📊 Report Features & Visual Design
Every visual is intentional — built to answer real business questions.

🎯 Executive KPIs
Total Sales (multi-year)

Total Profit & Profit Margin

YoY Sales Growth

Most Ordered Product

📦 Product Performance
Top/Bottom 5 Selling Products

Quantity Ordered by Product Line

Profit by Category

Product-wise Revenue Share

🧭 Region & Customer Trends
Sales by Country (Map View)

Top Customers by Revenue

Office-wise Sales & Employee Count

📅 Time Series Breakdown
Monthly Sales by Year (2003, 2004, 2005)

Order Trends & Sales Targets

Year-over-Year Comparisons

🔍 Advanced Features
Dynamic Slicers: Year, Product Line, Customer

Custom Theme for CV/Resume-friendly presentation

Tooltip Cards & Drill-through navigation

📸 Dashboard Preview:

🔥 Key Insights
🚗 Classic Cars dominated with over $3.85M in total sales

📈 Highest growth recorded in 2005 with $4.5M+ sales

🏆 Most sold product: 1992 Ferrari 360 Spider

💼 High-value customers included Euro+ Shopping Channel and Mini Gifts Distributors Ltd.

🌍 Sales distributed across 7 product lines, 122 employees, and 202 customers

⚙️ Tools Used
Purpose	Tool
Data Source	Nested JSON
BI Platform	Power BI Desktop
Calculations	DAX
Data Modeling	Star Schema
Visuals	Cards, Maps, Bar, Line, Table
UX	Slicers, Conditional Formatting, Tooltips


🧠 What I Learned
Structuring and transforming complex JSON into a clean BI model

Writing DAX for advanced logic like YoY growth, profit margins, and dynamic product ranking

Designing story-first visuals that deliver both clarity and insight

Building CV-grade dashboards optimized for professional portfolios

💼 Why This Project Matters
This project represents real-world BI problem solving:

Converting raw, nested data into usable metrics

Making sense of sales performance across time, geography, and customer segments

Delivering a user-friendly report that can help sales managers, analysts, and decision-makers

It's more than just a dashboard — it's a complete end-to-end data story from raw data to ready insights.

👋 Connect With Me
📧 harsh201130@gmail.com
🔗 LinkedIn – Harsh Sharma
