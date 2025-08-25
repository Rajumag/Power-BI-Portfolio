# 📊 Procurement Spend Report Power BI Dashboard

## 📋 Overview

This repository contains a Power BI project analyzing procurement spend data, covering total invoices (115K), spend (517.34M), vendors (2K), savings (8.48M), and average discount (3.86%). The data includes breakdowns by year, month, category (Direct, Indirect, Other), subcategory, vendor, tier, country/region, city, commodity, and payment terms. The project helps identify spending patterns, savings opportunities, discount trends, and geographic distributions to optimize procurement strategies and cost management.

## 📈 Dashboards Included

### 1. 🎯 Spend Overview Dashboard
This page provides a high-level summary of procurement metrics and trends. It includes:
- **Key Metrics**
  - Total Invoices: 115K
  - Total Spend: 517.34M
  - Total Vendors: 2K
  - Total Savings: 8.48M
  - Avg Disc %: 3.86%
- **Interactive Filters**
  - Year (All), Category (All, Direct, Indirect), Vendor Name (All), Tier (All).
- **Visuals**
  - Bar Chart: Total Spend by Month (e.g., January ~80M, declining to December ~34M).
  - Line Chart: Total Invoices by Month (starting at 12.4K in January, declining to 9.1K in December).
  - Pie Chart: Total Spend by Category (Direct 41.88% or 216.68M, Indirect 30.32% or 156.85M, Other 23.17% or 119.86M).
  - Map: Total Spend by City (bubbles sized by spend, e.g., large in Chicago, IL; St. Louis, MO; Atlanta, GA; smaller in Mexico and Miami, FL).

This dashboard conveys overall spend volume, monthly trends, category distributions, and geographic concentrations, highlighting potential cost-saving areas.

### 2. 📊 Discount Analysis Dashboard
This page focuses on savings and discount percentages over time and by vendors/tiers. It includes:
- **Key Metrics**
  - Total Savings: 8.48M
  - Avg Disc %: 3.86%
- **Interactive Filters**
  - Year (All), Category (All), Vendor Name (All).
- **Visuals**
  - Line and Clustered Column Chart: Total Savings and Avg Disc % by Month (e.g., savings ~1.0M in January declining to ~0.2M in December, disc % fluctuating from 8.21% to 1.64%).
  - Bar Chart: Avg Disc % by Vendor Name (e.g., Bigelectron... 35.00%, Bigron Inc. 32.63%, Kantatax C... 30.00%).
  - Treemap: Avg Disc % by Tier (Tier 10: 8.21%, Tier 1: 4.38%, Tier 6: 2.74%, showing tier-based discount variations).

This dashboard conveys discount-driven savings trends, with a parameter created for Year, Month, and Subcategory, used in the Total Savings and Avg Disc % line and clustered column chart, enabling dynamic switching for detailed analysis.

### 3. 🎯 Overall Summary Dashboard
This page offers a hierarchical and detailed view of spend with a table summary. It includes:
- **Interactive Filters**
  - Year (All), Category (All), Vendor Name (All), Country/Region, City, Sub Category, Commodity, Commodity Detail.
- **Visuals**
  - Decomposition Tree: Total Spend (517.35M) broken down by Country/Region (USA 45.84bn, Mexico 5.90M), City (Chicago, IL 25.90M), Category (Direct 13.43M), Sub Category (Hardware 6.59M), Commodity (Fabrication 2.73M), Commodity Detail (Fabrication - Steel St... 1.73M).
  - Table: Vendor details by Tier, Category, Commodity Detail, Sub Category, City, Line Item Quantity, Invoice Amount, Savings, Payment Terms Days (e.g., Acefind LLC: Tier 10, Direct, Outsourced Vents, Outsourced, Chicago, IL, 200.00 qty, 84.00 invoice, 0.00 savings, 75 days).

This dashboard conveys granular spend hierarchies and vendor performance, supporting in-depth audits and negotiations.

## ✨ Key Features
- **Dynamic Parameter**: A parameter was created for the Discount Analysis dashboard for Year, Month, and Subcategory, used in the Total Savings and Avg Disc % line and clustered column chart, allowing users to toggle views dynamically for focused insights.
- **Interactive Filters**: Slicers for Year, Category, Vendor Name, Tier, Country/Region, City, Sub Category, Commodity, and Commodity Detail enable comprehensive data slicing across dashboards.
- **Data Source**: Assumed Excel or CSV import with procurement transaction data (not included; inferred from visuals).
- **Visual Consistency**: Gray-blue theme with colorful accents for metrics (orange for invoices, blue for spend, red for vendors, purple for savings, teal for disc %).

## 🧹 Data Cleaning and Integrity Processes
The dataset was cleaned in Power BI's Power Query Editor to ensure accuracy and usability:
- **Header Assignment**: Promoted first row as headers for fields like Date, Category, Sub Category, Vendor Name, Tier, Spend, Discount %, Savings, Invoice Amount, City, Country/Region, Commodity, Commodity Detail, Payment Terms Days.
- **Duplicate Removal**: Removed duplicates based on unique invoice or transaction IDs to avoid overcounting, preserving ~115K invoices.
- **Null Value Handling**: Filled null Discount % with 0 (no discount), null Savings with 0; removed rows with null Spend or Category; imputed null Tier with "Unknown".
- **Data Type Conversions**: Converted Date to Date type, Spend/Savings/Invoice Amount to Decimal with currency format, Discount % to Percentage, Tier to Whole Number, categorical fields (Category, Vendor Name) to Text.
- **Outlier Detection and Correction**: Flagged negative Spend/Savings (set to 0 or removed), extreme Discount % (>100% capped at 100%); ensured Payment Terms Days positive.
- **Text Normalization**: Trimmed whitespace, standardized names (e.g., "Chicago, IL" consistent), split Commodity into Detail if combined.
- **Integrity Validation**: Verified aggregates (e.g., total Spend 517.34M, savings 8.48M), checked row counts pre/post-cleaning, ensured category pies sum to 100%; cross-validated monthly trends.

These processes resulted in a reliable dataset for precise reporting.

## 💡 Key Insights Derived from the Dashboards
- **Spend Patterns**: Total spend 517.34M across 115K invoices, peaking in January (~80M) and declining to December (~34M), suggesting seasonal procurement cycles.
- **Category Distribution**: Direct category dominates (41.88% or 216.68M), Indirect 30.32% (156.85M), Other 23.17% (119.86M), indicating focus on direct costs for savings.
- **Geographic Concentration**: USA leads spend (45.84bn), with Chicago, IL highest (~25.90M); Mexico smaller (5.90M), highlighting North American bias.
- **Savings Trends**: Total savings 8.48M from 3.86% avg discount, fluctuating monthly (high 8.21% in January, low 1.64% in December); vendors like Bigelectron... offer highest disc (35%).
- **Tier Performance**: Tier 10 has 8.21% disc, Tier 1 4.38%, showing higher tiers yield better discounts; subcategories like Hardware in Direct category drive volume.
- **Vendor Summary**: Table reveals vendors like Acefind LLC (Tier 10, 200 qty, 84 invoice amount, 75 payment days), useful for negotiation; overall, USA/Chicago vendors dominate.

## 📖 How to Use
1. Download the `.pbix` file from this repository.
2. Open in Power BI Desktop (free download from Microsoft).
3. Refresh data if connecting to a live source.
4. Use slicers (e.g., select "Direct" category and "2024" year) to filter visuals.
5. Toggle the parameter in Discount Analysis for Year/Month/Subcategory in charts.
6. Drill into decomposition tree for hierarchical insights.

## 📂 Repository Structure
- `Procurement_Spend_Report.pbix`: The main Power BI file.
- `screenshots/`:<img width="1173" height="734" alt="Screenshot 2025-08-25 143714" src="https://github.com/user-attachments/assets/b305cf9a-7f20-48d0-80cd-ae9087f642a3" />
- `Data Source` : Given Attached Excel file.
- `README.md`: This file.

## 🛠️ Requirements
- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.

## 🤝 Contributions
Feel free to fork and suggest improvements, such as adding more DAX calculations or advanced visuals.

