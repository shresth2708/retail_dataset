Project Overview

Retail cafés generate large volumes of daily transaction data through food and beverage sales. However, this data is often underutilized for business decision-making.

This project analyzes transaction-level café sales data and develops an interactive dashboard to identify key revenue drivers, understand customer purchasing behavior, and improve operational efficiency.

The dashboard transforms raw data into actionable insights that help café owners and operations managers make data-driven decisions related to product offerings, promotions, and sales strategies.

🎯 Problem Statement

How can a retail café improve sales performance and operational efficiency by analyzing raw transaction-level sales data and identifying key revenue drivers?

🎯 Objectives

Develop an interactive sales dashboard using Google Sheets.

Identify high-performing products and categories.

Analyze customer purchasing behavior and payment preferences.

Understand monthly sales trends and operational patterns.

Support data-driven decision-making for promotions and product strategies.

📂 Dataset Description

Dataset Source: Kaggle – Cafe Sales Dataset

Dataset Structure

The dataset contains transaction-level sales records including:

Transaction ID

Items

Quantity

Price Per Unit

Total Spent

Payment Method

Transaction Location

Transaction Date

Data Size

10,000 transactions

8 primary columns

Data recorded across multiple months

Derived Columns

Item Category (Bakery, Drinks, Food)

Transaction Month

Data Limitations

No profit or cost data available

No customer demographic information

External factors such as promotions or seasonal events not included

🧹 Data Cleaning & Preparation

All data cleaning and transformation steps were performed in Google Sheets.

Cleaning Steps

Missing or inconsistent values in items, payment method, and location were replaced with “Other”.

Missing numerical values were calculated using available columns.

Date formats were standardized for time-based analysis.

Feature Engineering

Created item categories: Bakery, Drinks, and Food.

Extracted transaction month for trend analysis.

Assumptions

Total Spent = Quantity × Price Per Unit

Unknown values grouped under “Other”.

📈 KPI & Metrics Framework

The following KPIs were used to evaluate performance:

1️⃣ Total Transactions

Formula: COUNT(Transaction ID)
Measures total customer purchases.

2️⃣ Total Spent (Revenue)

Formula: SUM(Total Spent)
Represents overall sales performance.

3️⃣ Total Quantity Sold

Formula: SUM(Quantity)
Indicates product demand.

4️⃣ Average Order Value (AOV)

Formula:

Total Revenue / Total Transactions


Measures average customer spending per visit.

Why These KPIs?

These KPIs help identify revenue drivers, measure demand patterns, and support operational decisions aligned with project objectives.

🔍 Exploratory Data Analysis (EDA)
Key Findings

A limited number of products contribute significantly to total revenue.

Quantity sold is relatively balanced, but pricing influences revenue differences.

Drinks category contributes the largest share of total sales.

Monthly sales trends show fluctuations indicating demand variability.

Digital payments are preferred over cash.

Takeaway and in-store orders dominate transaction types.

🧠 Advanced Analysis

A root cause and segmentation analysis was performed to understand factors influencing sales performance.

Analysis Performed

Product-level revenue vs quantity analysis

Category-based segmentation

Monthly sales trend analysis

Payment method and order type analysis

New Understanding

Sales growth is driven by high-performing products.

Product pricing and mix significantly affect revenue.

Sales fluctuations highlight opportunities for targeted promotions.

Customer preference for digital payments and takeaway orders impacts operational efficiency.

📊 Dashboard Design

The dashboard was built in Google Sheets using pivot tables, formulas, and interactive filters.

Dashboard Objective

Provide a centralized and interactive view of sales performance and operational metrics.

Dashboard Views
Executive View

Total Transactions

Total Spent

Total Quantity Sold

Average Order Value

Operational View

Total Sales by Product

Units Sold per Product

Sales Distribution by Category

Sales Trend by Month

Order Type Distribution

Transactions by Payment Method

Filters

Item filter

Payment method filter

Month filter

💡 Insights Summary

Few products drive most of the revenue.

Drinks category dominates sales contribution.

Revenue differences depend on pricing and product mix.

Monthly fluctuations indicate demand variability.

Digital payment usage exceeds cash usage.

Takeaway orders form a large share of transactions.

Product demand remains relatively consistent.

Increasing AOV presents a major revenue opportunity.

✅ Recommendations

Promote high-performing products through combo offers.

Improve or replace low-performing items.

Increase average order value through upselling strategies.

Run promotions during low-sales periods.

Improve efficiency in digital payment and takeaway operations.

📈 Impact & Value
Revenue Impact

Upselling and product optimization can increase average order value and overall revenue.

Operational Efficiency

Demand-based product focus improves service flow and reduces inefficiencies.

Time Efficiency

Automated dashboards reduce manual reporting effort.

Improved Decision Making

Centralized analytics support faster and more accurate decisions.

⚠️ Limitations

Dataset limited to transaction-level data.

Profitability analysis not possible without cost data.

External factors affecting sales not captured.

No predictive forecasting included.

🚀 Future Scope

Integration of profit and cost data.

Customer segmentation analysis.

Sales forecasting models.

Promotional effectiveness analysis.

Real-time dashboard automation.

✅ Conclusion

This project demonstrates how transaction-level sales data can be transformed into meaningful business insights through data cleaning, analysis, and visualization. The dashboard enables café management to identify revenue drivers, understand customer behavior, and make informed decisions to improve sales performance and operational efficiency.

📎 Appendix
Data Dictionary

Transaction ID – Unique sale identifier

Item – Product name

Quantity – Units sold

Price Per Unit – Item price

Total Spent – Revenue per transaction

Payment Method – Mode of payment

Transaction Location – Order type

Transaction Date – Date of sale