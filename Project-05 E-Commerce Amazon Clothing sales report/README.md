# 📊 Amazon Clothing Sales and Cancelled Orders Power BI Dashboard
## 📋 Overview
- This report contains a Power BI project analyzing Amazon clothing sales data from April 1, 2022, to June 12, 2022. The project includes two main dashboards:
  - Cancelled Orders Dashboard: Focuses on insights into cancelled orders, including trends over time, breakdowns by state, category, and other metrics.
- Clothing Sales Report Dashboard: Provides an overview of overall clothing sales, including fulfillment methods, courier status, order status, and shipping details.
- The data visualizes key performance indicators (KPIs) such as total sales amount, quantity, number of orders, and cancellation rates. These dashboards help identify patterns in sales performance, cancellation reasons, and regional preferences to support business decisions in e-commerce.
## 📈 Dashboards Included
###  1. 🎯 Cancelled Orders Dashboard
- This dashboard highlights cancelled orders during the period, emphasizing the impact on revenue and inventory. It includes the following visuals and what they convey:
  - KPIs: Cancelled Sales Amount (1.54M), Cancelled Quantity (1,117), Cancelled Orders (3,624), and % Cancelled Orders (2.98%). These provide a quick snapshot of the scale of cancellations relative to total activity.
  - By Day Bar Chart: Shows daily trends in the selected metric (e.g., #Orders by Day, Quantity by Day, or Sales by Day), revealing fluctuations and potential peak cancellation days.
  - By Ship-State Bar Chart: Breaks down the selected metric by Indian states (e.g., Maharashtra leads with high values across metrics, followed by Karnataka, Telangana, etc.). This identifies regions with higher cancellation rates, possibly due to logistics issues or customer behavior.
  - By Category Bar Chart: Displays the selected metric by clothing categories (e.g., Set and Kurta have the highest cancellations, while Blouse and Bottom are minimal). This points to product-specific issues like sizing or quality.
  - Category Table: Lists styles (e.g., Western Dress JNE3797, Kurta JNE3801) with total quantity, sales, and #orders for cancelled items, allowing detailed product-level analysis.
The dashboard aims to explain why cancellations occur, where they are concentrated, and which products are most affected, helping to pinpoint areas for improvement like supply chain or product descriptions.
### 2. 📊 Clothing Sales Report Dashboard
- This dashboard provides a comprehensive view of successful clothing sales, focusing on fulfillment, shipping, and status metrics. It includes:
  - By Day Bar Chart: Tracks daily sales trends in the selected metric (e.g., #Orders by Day peaks around 1,500-1,900, Quantity by Day around 1,400-1,800, Sales by Day around 0.95M-1.0M), showing growth or dips over time.
  - By Fulfillment Pie Chart: Compares Amazon-fulfilled (68.19% for #Orders, 70.38% for Quantity, 67.68% for Sales) vs. Merchant-fulfilled orders, highlighting reliance on Amazon's logistics.
  - By Courier Status Bar Chart: Visualizes changes in courier performance (e.g., increases in Shipped, decreases in Unshipped/Cancelled), indicating efficiency in delivery processes.
  - By Category Bar Chart: Ranks categories (e.g., Set leads with 9.9K #Orders, 9.4K Quantity, 8.3M Sales; Kurta follows closely), revealing top-selling items.
  - By Status Bar Chart: Shows order statuses as percentages (e.g., 100% Shipped - Delivered to Buyer for most, with minor pending or other statuses), demonstrating high completion rates.
  - By Ship-Service-Level Pie Chart: Compares Expedited (67.46% for #Orders, 69.66% for Quantity, 67.67% for Sales) vs. Standard shipping, showing customer preferences for faster delivery.
This dashboard illustrates overall sales health, operational efficiency, and customer preferences, aiding in inventory planning, marketing strategies, and logistics optimization.
## ✨ Key Features
- Dynamic Parameter for Metrics: A parameter has been created to switch between "Sales", "Quantity", and "Number of Orders". This parameter is applied as a filter to every visual in both dashboards, allowing users to toggle views dynamically without recreating reports. For example, selecting "#Orders" updates all charts to display order counts, while "Sales" shows monetary values in millions.
- Interactive Filters: Dashboards include slicers for State, Date Range, and Category to drill down into specific data subsets.
- Data Source: Based on aggregated Amazon sales data (not included in this repo for privacy; assume CSV or Excel import in Power BI).
- Visual Consistency: Orange-themed bars and pies for branding alignment with Amazon's style.

## 💡 Key Insights Derived from the Dashboards

- Cancellation Trends: Cancellations represent only 2.98% of total orders, but amount to 1.54M in lost sales. Maharashtra and Karnataka account for the majority (~40-50% across metrics), suggesting regional factors like delivery delays or competition. Categories like Set and Kurta see the highest cancellations (e.g., 1,463 #Orders for Set), possibly due to fit issues in ethnic wear.
- Sales Performance: Total sales reach ~17.8M (inferred from aggregates), with consistent daily peaks early in the period. Amazon fulfillment handles ~68-70% of volume, reducing merchant dependency. Expedited shipping is preferred (67-70%), correlating with higher completion rates (100% delivered in most statuses).
- Category Dominance: Set and Kurta dominate sales (over 80% combined), while Western Dress and Top follow. Low performers like Blouse, Bottom, and Saree (<1%) may need promotional boosts or discontinuation.
- Regional Hotspots: Maharashtra leads in both sales and cancellations, followed by southern states (Karnataka, Telangana, Tamil Nadu), indicating strong demand in urban areas but potential logistics challenges.
- Operational Efficiency: Minimal unshipped or cancelled items in the sales dashboard (near 0% in some views) show robust processes, but courier status decreases in unshipped suggest areas for improvement to maintain 100% delivery.

## 📖 How to Use

- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use the parameter slicer to switch between Sales, Quantity, and #Orders views.
- Interact with state/date slicers for filtered analysis.

## 📂 Project Structure

- Amazon_Clothing_Dashboards.pbix: The main Power BI file.
- screenshots/:<img width="1376" height="735" alt="Screenshot 2025-08-16 124307" src="https://github.com/user-attachments/assets/0447442d-5446-4b6a-83ee-e73f850ea769" />

- README.md: This file.

## 🛠️ Requirements

- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.
## 🤝 Contributions
- Feel free to fork and suggest improvements, such as adding more DAX calculations or advanced visuals.
