# 📊 Inventory Management Report Power BI Dashboard
## 📋 Overview
This repository contains a Power BI project analyzing inventory and sales data from January 1, 2021, to July 30, 2023. The dashboard provides insights into revenue, order quantities, SKU performance, vendor contributions, and geographic warehouse overviews. It helps optimize inventory management, identify high-value items via ABC analysis, and track sales patterns to support supply chain decisions.
##📈 Dashboards Included
1. 🎯 Inventory Management Report Dashboard
This dashboard offers a comprehensive view of inventory metrics, sales trends, and vendor performance. It includes the following visuals and what they convey:

- Key Metrics
  - Total Annual Revenue: 36.76M
  - Order Quantity: 1.23M
  - Total Unique SKUs: 303

- Interactive Filters
  - Order Date (range from 01-01-2021 to 30-07-2023) and SKU Name (All or specific) for dynamic data slicing.
- ABC Analysis by Total Revenue and SKUs
  - Stacked bar chart with line overlay showing revenue distribution (A Class: ~25M, B Class: ~8M, C Class: ~4M) and SKU counts (A: 25, B: 41, C: 237), highlighting that A Class items drive the majority of revenue with fewer SKUs.
- Warehouse Overview
  - Map visualizing warehouse or sales locations (e.g., concentrated in North America and Europe), conveying geographic distribution and potential logistics hotspots.
- Sales Pattern
  - Line chart tracking order quantity over time (declining from ~15K in 2021 to ~5K in 2023) alongside total revenue, indicating sales trends and possible market shifts.
- Vendor Overview
  - Table breaking down vendors by ABC Class counts and totals (e.g., SUPERVALU Group: 1 A, 4 B, 10 C, 15 Total; overall totals: 25 A, 41 B, 230 C, 303 SKUs), showing vendor contributions to inventory categories.
- Top 5 Vendors
  - Horizontal bar chart ranking vendors by revenue (Apotex Corp: 7.4M, Cixi Group: 4.9M, Mylan Group: 2.8M, Heritage: 2.8M, Major Corp: 2.5M), emphasizing key suppliers.
The dashboard aims to convey inventory efficiency, revenue concentration, and vendor dependencies, enabling better stock prioritization and supplier management.

## ✨ Key Features
- Interactive Filters: Slicers for Order Date and SKU Name allow users to drill down into specific periods or products.
- Dynamic Visuals: All charts update based on filter selections, providing flexible analysis.
- Data Source: Based on aggregated inventory and sales data (not included in this repo for privacy; assume CSV or Excel import in Power BI).
- Visual Consistency: Green-themed visuals with orange accents for a professional, intuitive interface.

## 🧹 Data Cleaning and Integrity Processes
The dataset underwent thorough cleaning and validation in Power BI's Power Query Editor to ensure accuracy, consistency, and reliability:

- Header Assignment: The first row of the imported data was promoted to column headers to correctly label fields like Order Date, SKU Name, Revenue, Quantity, etc.
- Duplicate Removal: Duplicates were identified and removed based on unique identifiers (e.g., Order ID or SKU combinations) to prevent inflated metrics like revenue or quantity.
- Null Value Handling: Null values were detected across columns; for numeric fields (e.g., Revenue, Quantity), nulls were replaced with 0; for dates, rows with null Order Dates were removed; categorical nulls (e.g., Vendor Name) were filled with "Unknown" or the mode value where appropriate.
- Data Type Conversions: Ensured proper formatting, such as converting Order Date to Date type, Revenue and Quantity to Decimal/Whole Number, and SKU Name to Text. Invalid entries (e.g., non-numeric revenue) were filtered out.
- Outlier Detection and Correction: Checked for negative values in Quantity or Revenue and corrected them (e.g., absolute values or removal if erroneous). Applied trimming for extreme outliers using conditional columns.
- Calculated Fields: Added DAX measures for ABC Classification (based on cumulative revenue thresholds: A=80%, B=15%, C=5%), total revenue, and unique SKU counts to derive insights.
- Data Integrity Validation: Cross-verified totals (e.g., sum of ABC revenues matches total revenue), ensured no data loss during transformations via row count checks, and validated date ranges for consistency. Relationships were established between tables (e.g., SKU to Vendor) to prevent orphaned records.

These steps ensured the data was clean, complete, and ready for accurate analysis, minimizing errors in visualizations.

##💡 Key Insights Derived from the Dashboard

- Revenue Concentration: A Class SKUs (only 25 out of 303) generate ~68% (25M) of total revenue (36.76M), emphasizing the need to prioritize stock for these high-value items to avoid shortages.
- Declining Sales Trend: Order quantity has steadily decreased from ~15K in 2021 to ~5K in 2023, potentially indicating market saturation, economic factors, or supply issues, despite stable revenue—suggesting a shift to higher-value orders.
- Vendor Dependency: Top 5 vendors (Apotex Corp, Cixi Group, etc.) account for a significant portion of revenue (~20M combined), with diverse ABC contributions; diversifying suppliers could mitigate risks.
- SKU Distribution: C Class dominates SKU count (237 or ~78%), but contributes only ~11% revenue (4M), highlighting opportunities for inventory reduction in low-value items to free up warehouse space.
- Geographic Focus: Warehouse activity is concentrated in North America and Europe, suggesting regional demand patterns; expanding to other areas could boost growth.
- Overall Efficiency: With 1.23M orders across 303 SKUs, average revenue per SKU is ~121K, but variance in ABC classes indicates potential for targeted promotions on B/C items to increase their contribution.

## 📖 How to Use

- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source (last refresh: 30-07-2023).
- Use the slicers (Order Date, SKU Name) to filter and analyze specific data.
- Explore visuals for trends, such as hovering over the map for location details or selecting vendors in the table.

## 📂 Repository Structure

- Inventory_Management_Report.pbix: The main Power BI file.
- screenshots/: <img width="1225" height="734" alt="Screenshot 2025-08-19 105847" src="https://github.com/user-attachments/assets/21b88f28-b7f1-4113-a608-3fce1421fd02" />
- README.md: This file.

## 🛠️ Requirements

- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.

## 🤝 Contributions
- Feel free to fork and suggest improvements, such as adding more DAX calculations or advanced visuals.
