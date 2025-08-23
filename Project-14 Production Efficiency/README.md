# 📊 Production Efficiency Analysis Power BI Dashboard
## 📋 Overview
This repository contains a Power BI project analyzing production efficiency data for companies across industries like Aerospace, Automotive, Electronics, Energy, Food & Beverage, Pharmaceuticals, and Textiles. The dataset covers metrics from 2020-2022, including revenue (12.24bn total), profit (6.12bn), efficiency rate (74.2%), defect rate (4.99%), resource utilization, supply chain length, technology adoption, and more. Data spans global, local, and regional market expansions, with 10,140 rows of company records. The dashboard helps identify trends in defects, profits, inventory turnover, and efficiency to support operational improvements and decision-making.
## 📈 Dashboards Included
The project features a single main dashboard page with interactive visuals, including a tooltip feature for detailed hover insights.
1. 🎯 Main Production Efficiency Analysis Dashboard
This page provides a comprehensive overview of production metrics, trends, and breakdowns. It includes:
- Key Metrics
  - Revenue: ₹12.24bn (gauge showing progress).
  - Profit: ₹6.12bn (gauge).
  - Efficiency Rate: 74.2% (circular gauge).
  - Defect Rate: 4.99% (line chart vs. goal of 6%).
- Interactive Filters
  - Industry (Aerospace, Automotive, etc.), Market Expansion (Global, Local, Regional), Year (2020, 2021, 2022).
- Visuals
  - Bar Chart: Defect Rate by Industry and Technology Adoption (e.g., Automotive: High 2,939, Low 2,688; colors for High/Low/Medium adoption), highlighting how tech impacts defects.
  - Treemap: Avg Eff Rate by Industry Type (e.g., Textile 0.76, Pharmaceuticals 0.75), showing efficiency hierarchies.
  - Line Chart: Profit by Industry (declining from Aerospace ~940M to Textile ~804M), indicating performance trends.
  - Line Chart: Supply Chain vs Inventory Turnover (monthly from Jan-Dec, starting at 5.43 and declining to 2.73), tracking operational efficiency over time.
  - Scatter Plot: Profit vs Cost Analysis (points for Global, Local, Regional), revealing cost-profit correlations.
  - Table: Company details (e.g., Eco Corporation variations with Per Unit Energy, Defect Rate, Profit, Resource Utilization), listing top performers.
This dashboard conveys industry-specific efficiencies, defect drivers, and financial trends, aiding in pinpointing improvement areas.
2. 📊 Tooltip-Enabled Visuals (Integrated Feature)
- The second screenshot demonstrates a tooltip feature on hover (e.g., on the treemap or bar chart). It provides additional details like exact values (e.g., Tech Industries profit 79.51, Global Systems 71.19), company names, and breakdowns. This enhances interactivity without a separate page, showing contextual data like sustainability index or customer satisfaction on demand.
## ✨ Key Features
- Interactive Filters: Slicers for Industry, Market Expansion, and Year allow dynamic data slicing.
- Tooltip Integration: Hover tooltips on visuals provide deeper insights (e.g., precise profit figures, company names), improving user experience.
- Dynamic Visuals: All charts update with filters, enabling cross-analysis (e.g., defect rates for Automotive in 2022).
- Data Source: Multi-sheet Excel file ("Production efficiency dataset.xlsx") with merged data from Sheet1, M1, and M2.
- Visual Consistency: Light blue-gray theme with color-coded gauges and charts for intuitive navigation.

## 🧹 Data Cleaning and Integrity Processes
The dataset from the Excel file ("Production efficiency dataset.xlsx") with three sheets (Sheet1, M1, M2) was cleaned in Power BI's Power Query Editor:
- Merging Sheets: Combined data from Sheet1 (core metrics), M1 (production details like Volume, Efficiency Rate), and M2 (additional like Resource Utilization, Supply Chain Length) using CompanyID as the key; appended or merged queries to create a unified table.
- Header Assignment: Promoted first rows as headers; renamed columns for clarity (e.g., "ProductionVolume" to "Production Volume").
- Duplicate Removal: Removed duplicates based on CompanyID-Date combinations to eliminate redundant entries, reducing from ~10,140 rows per sheet to a clean merged set.
- Null Value Handling: Identified nulls in numeric fields (e.g., Profit, Defect Rate) and replaced with 0 or median values (e.g., avg Defect Rate ~4.99%); categorical nulls (e.g., IndustryType) filled with "Unknown"; removed rows with all-null critical fields.
- Data Type Conversions: Converted Date to Date type, numeric fields (Revenue, Profit, Efficiency Rate) to Decimal, categorical (IndustryType, MarketExpansion) to Text; parsed truncated fields like "Productio..." to full "Production Cost".
- Outlier Detection and Correction: Flagged extreme values (e.g., negative Defect Rates removed, high Resource Utilization >100% capped at 100%); used conditional columns for bins (e.g., Technology Adoption: High/Medium/Low).
- Text Normalization: Trimmed whitespace, standardized formats (e.g., "India,Maharashtra,Mumbai" split into separate columns if needed), converted currency to consistent ₹ format.
- Integrity Validation: Verified merged row counts, ensured sums match (e.g., total Revenue 12.24bn), checked relationships for no orphans; cross-validated samples (e.g., Eco Corporation entries consistent across sheets).
These steps ensured a robust, error-free dataset for accurate visualizations.
## 💡 Key Insights Derived from the Dashboards
- Financial Performance: Total revenue (12.24bn) and profit (6.12bn) are strong, but profits decline across industries (Aerospace highest ~940M, Textile lowest ~804M), suggesting cost pressures in lower-efficiency sectors.
- Efficiency and Defects: Overall efficiency 74.2%, defect rate 4.99% (below 6% goal); Automotive has high defects (2,939 high-tech), while Textiles lowest (1,395), indicating tech adoption reduces defects but varies by industry.
- Operational Trends: Inventory turnover declines monthly (5.43 Jan to 2.73 Dec), signaling potential supply chain issues; supply chain length correlates with lower turnover.
- Profit-Cost Relation: Scatter shows regional firms with balanced profit-cost, global ones higher profit but variable costs, highlighting scale benefits.
- Company Highlights: Top performers like Tech Industries (79.51 profit) have low defects (0.74) and high resource utilization (80.45), while others like Eco Logistics (17.00 profit) show medium adoption opportunities.
- Yearly Decline: Profits drop from 2020-2022, possibly due to rising costs or defects, emphasizing need for efficiency improvements in Energy and Pharmaceuticals.

## 📖 How to Use
- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use slicers (e.g., select "Aerospace" and "Global") to filter visuals.
- Hover over charts for tooltips with detailed metrics.

## 📂 Repository Structure
- Production_Efficiency_Analysis.pbix: The main Power BI file.
- screenshots/: <img width="1174" height="735" alt="Screenshot 2025-08-23 134546" src="https://github.com/user-attachments/assets/25e89d83-912d-45bf-8c65-d6f6a01cba3a" />
- Source file : Given in the attached files.
- README.md: This file.

## 🛠️ Requirements
- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.
