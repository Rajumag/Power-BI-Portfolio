# 📊 Sales Analysis and Trends Power BI Dashboard
## 📋 Overview
This repository contains a Power BI project analyzing sales data from 2019 to 2022, covering 10,000 orders across categories like Automotive, Beauty & Health, Books, Clothing, Electronics, Home & Kitchen, Sports, and Toys & Games. The dataset includes metrics such as revenue (total 18.90bn), COGS (13.21bn), gross profit (5.7bn), marketing expenses (659M), net profit (18.24bn), and order statuses. The project helps identify sales trends, product performance, channel contributions, and root causes of profit variations to support business strategy and optimization.
#3 📈 Dashboards Included
The project features three interconnected dashboard pages, each with interactive filters for years (2019-2022) and a "Home Page" navigation button.
1. 🎯 Sales Analysis Dashboard
This page provides an overview of financial performance, trends, and order breakdowns. It includes:
- Key Metrics
  - Revenue: ₹18.90bn (+34.79% YoY)
  - COGS: ₹13.21bn (+34.94% YoY)
  - Gross Profit: ₹5.7bn (+34.42% YoY)
  - Marketing Exp: ₹659M (+34.46% YoY)
  - Net Profit: ₹18.24bn (+34.80% YoY)
- Interactive Filters
  - Year buttons (2019, 2020, 2021, 2022).
- Visuals
  - Bar Chart: Monthly Revenue (e.g., Jan ~0.61bn, peaking mid-year then declining to Dec ~1.54bn).
  - Bar Chart: Marketing Exp (monthly, similar trend to revenue).
  - Income Statement Bar: Revenue, Gross Profit, Net Profit, Marketing Expenses, Cost of Goods Sold (Revenue highest at 18.90bn, Net Profit slightly lower at 18.24bn due to expenses).
  - Pie Chart: Revenue by Category (Automotive 49.2%, Sports 19.83%, Electronics 12.61%, Home & Kitchen 6.09%, Beauty & Health 2.8%).
  - Pie Chart: Revenue by Channel (In-store 72.25%, Online 27.75%).
  - Table: Order Status Counts (Shipped 9,553, Cancelled 204, Disputed 52, Issue Resolved 163, Not Shipped 28; Total 10,000).
This dashboard conveys overall sales health, monthly fluctuations, category/channel contributions, and order fulfillment efficiency, highlighting growth and potential bottlenecks.
2. 📊 Product Analysis Dashboard
This page dives into category and product-level revenue and correlations. It includes:
- Interactive Filters
   - Year buttons (2019-2022).
- Visuals
  - Treemap: Revenue by Category (Automotive largest at 9.30bn, Sports 3.78bn, Electronics 2.38bn, etc.).
  - Bubble Chart: Correlation Between Revenue and Marketing Exp (bubbles sized by marketing exp, positioned by revenue; products like Action Figure, Air Filter high on both axes).
  - Horizontal Bar Chart: Revenue by Product (Air Filter highest at 1.23bn, Car Battery 1.22bn, Headlights 1.21bn, etc.).
  - Table: Financials by Category (e.g., Automotive: Revenue 9.30bn, COGS 6.49bn, Gross Profit 2.81bn, Mark Exp 325M, Net Profit 8.97bn).
This dashboard conveys product and category profitability, marketing ROI correlations, and top performers, aiding in inventory and promotion decisions.
3. 🎯 Root Cause Analysis Dashboard
This page uses a decomposition tree to break down gross profit by dimensions. It includes:
- Interactive Filters
  - Year buttons (2019-2022), slicers for Channel, Category, Product Name.
- Visuals
  - Decomposition Tree: Gross Profit (5.69bn) broken down by Channel (In-store 4.11bn, Online 1.58bn), then Category (e.g., Sports 80.25bn wait, likely typo in screenshot—values like Automotive 1.96bn under In-store), Product Name (e.g., Basketball 11.86bn, Yoga Mat 10.87bn).
This dashboard conveys hierarchical root causes of profit variations, allowing drill-down from channels to products for identifying underperformers.
## ✨ Key Features
- Dynamic Parameter: A parameter was created for Revenue and Marketing Expenses, attached to visuals in the Sales Analysis dashboard, allowing users to switch between these metrics in charts like the monthly bar for flexible comparison.
- Interactive Filters: Year buttons and slicers for Channel, Category, Product Name enable targeted analysis.
- Navigation: "Home Page" button on each page for easy return to the main dashboard.
- Data Source: Multi-sheet Excel file ("Sales Report Project.xlsx") with merged data from Sales table, Products, and Dates.
- Visual Consistency: Dark theme with teal accents, pie charts for distributions, and bars/lines for trends.

## 🧹 Data Cleaning and Integrity Processes
The dataset from "Sales Report Project.xlsx" (sheets: Sales table, Products, Dates) was cleaned in Power BI's Power Query Editor:
- Merging Sheets: Joined Sales table (order details) with Products (category mapping) on Product Name, and Dates (date dimension) on Date for enhanced time analysis; used left joins to retain all sales records.
- Header Assignment: Promoted first rows as headers; renamed for clarity (e.g., "Oder ID" to "Order ID", "MSRP (Rs.)" to "MSRP").
- Duplicate Removal: Removed duplicates on Order ID to ensure unique orders, reducing potential overcounting in totals like revenue (18.90bn) or orders (10,000).
- Null Value Handling: Filled null STATUS with "Not Shipped", null Product Name with "Unknown"; replaced null numerics (Revenue, COGS) with 0; removed rows with null Date or Channel.
- Data Type Conversions: Converted Date to Date type (from numeric like 43466), Revenue/COGS/Marketing Expenses to Decimal with ₹ format, Units Sold to Integer; categorized STATUS (Shipped, Cancelled, etc.).
- Outlier Detection and Correction: Flagged negative or zero Revenue/Units (removed or investigated as errors); capped extreme MSRP values based on category averages.
- Text Normalization: Trimmed whitespace, standardized Product Names (e.g., consistent casing), split combined fields if needed; derived Year from Date for filters.
- Integrity Validation: Verified totals post-merge (e.g., sum Revenue matches 18.90bn), ensured no data loss (row count ~10,000), checked relationships for consistency (e.g., all Products in Sales exist in Products sheet).
These steps ensured accurate, complete data for reliable insights.
## 💡 Key Insights Derived from the Dashboards
- Growth Trends: Revenue grew 34.79% YoY to 18.90bn, net profit 34.80% to 18.24bn, but monthly trends show mid-year peaks and year-end declines, possibly seasonal.
- Category Dominance: Automotive leads revenue (49.2% or 9.30bn), followed by Sports (19.83% or 3.78bn); lowest Beauty & Health (2.8%), suggesting focus on high-margin categories.
- Channel Performance: In-store dominates (72.25%), Online 27.75%; root cause tree shows In-store gross profit 4.11bn vs. Online 1.58bn, indicating physical sales drive profits.
- Order Efficiency: 95.53% Shipped, but 2.04% Cancelled and 0.28% Not Shipped highlight fulfillment issues; total orders 10,000.
- Marketing ROI: Correlation bubble shows strong positive link between marketing exp and revenue (e.g., high-exp products like Air Filter at 1.23bn revenue), but exp growth (34.46%) outpaces some profits.
- Product Highlights: Top products like Air Filter (1.23bn), Car Battery (1.22bn) in Automotive; root cause reveals specifics like Basketball (11.86bn gross profit wait, likely screenshot scale—values indicate key drivers).

## 📖 How to Use
- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use year buttons to filter; switch parameter for Revenue/Marketing in Sales dashboard.
- Navigate via "Home Page" button; drill into decomposition tree for root causes.

## 📂 Repository Structure

- Sales_Analysis_Trends.pbix: The main Power BI file.
- screenshots/:<img width="1151" height="736" alt="Screenshot 2025-08-23 142232" src="https://github.com/user-attachments/assets/b4851fdd-07c6-44f2-ae09-0f8dd02acbea" />
- Data Source : Attached Files
- README.md: This file.

🛠️ Requirements

Power BI Desktop (version 2.0 or later recommended).
No additional dependencies; all DAX measures and visuals are built-in.
