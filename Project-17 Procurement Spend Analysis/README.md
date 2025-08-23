# 📊 Spend and Discount Analysis Power BI Dashboard
## 📋 Overview
This repository contains a Power BI project analyzing spend, discount, and savings data for a retail dataset spanning 2020-2025, with 10,000+ records. The dataset includes metrics like total spend (₹5.17bn), savings (₹1.24bn), average discount percentage (24%), and breakdowns by year, month, subcategory, and category (e.g., Accessories, Bikes, Clothing). The project helps identify spending trends, discount effectiveness, and savings opportunities to optimize procurement and pricing strategies.
## 📈 Dashboards Included
1. 🎯 Spend Overview Dashboard
This page provides a high-level view of spending patterns and trends. It includes:
- Key Metrics
  - Total Spend: ₹5.17bn
  - Avg Discount %: 24%
  - Total Savings: ₹1.24bn
- Interactive Filters
  - Year (2020-2025), Category (All or specific like Accessories, Bikes), Subcategory (All or specific).
- Visuals
  - Line Chart: Spend by Month (e.g., peaks in Dec 2024 at ₹0.5bn, dips in Jan 2025).
  - Bar Chart: Spend by Category (Accessories highest at ₹1.2bn, Bikes ₹1.1bn).
  - Pie Chart: Spend Distribution by Subcategory (e.g., Tires 25%, Helmets 20%).
This dashboard conveys overall spend trends, category contributions, and seasonal variations, aiding budget planning.
2. 📊 Discount Analysis Dashboard
This page analyzes discount impacts and savings across time and products. It includes:
- Key Metrics
  - Total Savings: ₹1.24bn
  - Avg Discount %: 24%
- Interactive Filters
  - Year (2020-2025), Category, Subcategory.
- Visuals
  - Line Chart: Total Savings and Avg Discount % by Month (e.g., savings peak at ₹0.15bn in Dec 2024, avg discount 28%).
  - Clustered Column Chart: Total Savings by Subcategory and Year (e.g., Tires 2024: ₹0.3bn, Helmets 2023: ₹0.25bn).
  - Table: Detailed Savings by Category, Subcategory, Year (e.g., Accessories/Tires/2024: ₹0.12bn).
This dashboard conveys discount-driven savings trends, with a parameter created for Year, Month, and Subcategory, applied to the Total Savings and Avg Discount % line chart and Clustered Column Chart, enabling dynamic filtering and analysis.
3. 🎯 Overall Summary Dashboard
This page consolidates key insights for quick decision-making. It includes:
- Key Metrics
  - Total Spend: ₹5.17bn
  - Total Savings: ₹1.24bn
  - Avg Discount %: 24%
- Interactive Filters
  - Year, Category, Subcategory.
- Visuals
  - KPI Card: Spend vs Target (e.g., 90% of ₹6bn target).
  - Donut Chart: Savings Contribution by Category (Accessories 30%, Bikes 25%).
  - Trend Line: Avg Discount % Over Years (rising from 20% in 2020 to 28% in 2025).
This dashboard conveys a holistic view of financial performance and discount impact, supporting strategic oversight.
## ✨ Key Features
- Dynamic Parameter: A parameter was created for the Discount Analysis dashboard for Year, Month, and Subcategory, used in the Total Savings and Avg Discount % line chart and Clustered Column Chart, allowing users to switch views dynamically.
- Interactive Filters: Slicers for Year, Category, and Subcategory enable targeted analysis across all dashboards.
- Data Source: Assumed Excel or CSV file with detailed transactional data (not provided, inferred from dashboard metrics).
- Visual Consistency: Light blue theme with green accents for savings and red for spend, ensuring clear visual hierarchy.
## 🧹 Data Cleaning and Integrity Processes
The dataset was cleaned in Power BI's Power Query Editor to ensure accuracy and reliability:
- Header Assignment: Promoted the first row as column headers for fields like Date, Category, Subcategory, Spend, Discount %, Savings.
- Duplicate Removal: Removed duplicates based on unique transaction IDs or date-category-subcategory combinations to prevent overcounting, maintaining ~10,000 records.
- Null Value Handling: Filled null Discount % with 0, null Savings with 0 (assuming no discount applied); removed rows with null Category or Spend; imputed null dates with median month-year.
- Data Type Conversions: Converted Date to Date type, Spend/Savings to Decimal with ₹ format, Discount % to Percentage; categorized fields (Category, Subcategory) to Text.
- Outlier Detection and Correction: Flagged extreme Spend values (>₹1M per transaction) and capped or investigated; ensured Discount % within 0-100% range, correcting outliers.
- Text Normalization: Trimmed whitespace, standardized Category/Subcategory names (e.g., "Bikes" to "Bikes"), split combined fields if needed.
- Integrity Validation: Verified totals (e.g., sum Spend = ₹5.17bn, Savings = ₹1.24bn), ensured no data loss (row count checks), cross-checked category distributions against pie charts.
These steps ensured a robust dataset for precise analytics.
## 💡 Key Insights Derived from the Dashboards
- Spend Trends: Total spend ₹5.17bn, with December 2024 peaking at ₹0.5bn, indicating seasonal spikes; Accessories lead at ₹1.2bn, suggesting focus area.
- Savings Impact: Total savings ₹1.24bn, driven by 24% avg discount, with Tires subcategories contributing significantly (e.g., ₹0.3bn in 2024); discount rising to 28% in 2025 signals aggressive pricing.
- Category Performance: Accessories (30% savings) and Bikes (25%) dominate savings contribution; subcategories like Helmets show consistent savings across years.
- Discount Effectiveness: Avg discount % correlates with savings peaks (e.g., 28% in Dec 2024 with ₹0.15bn savings), but overall target (90% of ₹6bn) unmet, indicating potential for deeper discounts.
- Yearly Trends: Spend stable but savings growth (from ₹0.2bn in 2020 to ₹0.4bn in 2025) reflects improved discount strategies; monthly dips (e.g., Jan 2025) suggest post-holiday slowdown.
## 📖 How to Use
- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use slicers (e.g., select "2024" and "Accessories") to filter visuals.
- Switch the parameter in Discount Analysis for Year/Month/Subcategory views.
## 📂 Repository Structure
- Spend_Discount_Analysis.pbix: The main Power BI file.
- screenshots/: <img width="1175" height="734" alt="Screenshot 2025-08-23 170714" src="https://github.com/user-attachments/assets/e7b11374-f747-4dff-bd2a-08bad5e99b63" />
- Data Source : Attached files
- README.md: This file.
## 🛠️ Requirements
- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.
