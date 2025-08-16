# 📊 Anomaly Detection Report Power BI Dashboard
## 📋 Overview
This repository contains a Power BI project analyzing transaction data to detect anomalies across various account types, locations, genders, occupations, and time periods. The dashboard covers data from 2023 and 2024, focusing on transaction amounts, counts, and anomaly metrics for cities like Bangalore, Chennai, Delhi, Hyderabad, Kolkata, Mumbai, and Pune. It helps identify unusual patterns in financial transactions to support fraud detection and risk management.
## 📈 Dashboards Included
1. 🎯 Anomaly Detection Report Dashboard
- This dashboard provides a detailed analysis of transaction anomalies based on multiple dimensions. It includes the following visuals and what they convey:
- Key Metrics
  - Transaction Amount: 1.74M (broken down by account type and gender)
  - Transaction Count: 336 (by gender)
  - Anomaly Transaction Amount: 75K (by gender)
  - Anomaly Transaction Count: 15 (by gender)
  - Anomaly Amount %: 4.33% (by gender)
  - Anomaly Count %: 4.46% (by gender)
- Account Type Breakdown
  - Interactive filters for Business, Joint, and Savings accounts to analyze transaction patterns.
- Anomaly Transaction Amount by Month
  - Line chart showing monthly trends (e.g., peaks in April and July), highlighting periods with higher anomaly amounts.
- Transaction Count by Transaction Type
  - Donut chart showing distribution (e.g., 66.7% Withdrawal, 26.67% Payment, 6.67% Deposit), indicating dominant transaction types.
- Transaction Amount by Income Group (in lakhs)
  - Bar chart comparing anomaly amounts across income brackets (e.g., highest in 15-20 lakhs), suggesting income-related anomaly patterns.
- Transaction Amount by Occupation
  - Bar chart ranking occupations (e.g., IT Professional leads, followed by Engineer, Business, Student, Retired, Doctor), showing occupation-specific anomaly risks.
The dashboard aims to pinpoint where and when anomalies occur, who is most affected, and which transaction types or occupations are prone to irregularities, aiding in targeted monitoring and intervention.
## ✨ Key Features
- Interactive Filters: Slicers for Account Type, Year (2023, 2024), and Month allow users to drill down into specific data subsets.
- Dynamic Visuals: All charts update based on filter selections, providing a flexible analysis tool.
- Data Source: Based on aggregated transaction data (not included in this repo for privacy; assume CSV or Excel import in Power BI).
- Visual Consistency: Green-themed visuals for a clean and professional look.
## 🧹 Data Cleaning Process
- The dataset was cleaned to ensure accuracy and usability in Power BI:
- Header Assignment: The first row was set as the column headers to properly label the data fields.
- Duplicate Removal: All duplicate entries were identified and removed to avoid skewed analysis.
- Null Value Handling: Null values were detected, removed where irrelevant, and replaced with common known values (e.g., median or mode) where applicable to maintain data integrity.
- General Cleanup: Inconsistent formatting was standardized, and irrelevant columns or rows were excluded to focus on key metrics like transaction amount, count, and anomaly indicators.
## 💡 Key Insights Derived from the Dashboard
- High Anomaly Volume: Total anomaly transaction amount is 75K (4.33% of 1.74M), with 15 anomaly transactions (4.46% of 336), indicating a small but notable fraud risk.
- Gender Patterns: Males show slightly higher anomaly amounts (592.63K vs. 605.20K for females) and counts (114 vs. 117 for females), suggesting gender-based behavioral differences.
- Monthly Spikes: Anomalies peak in April and July, possibly linked to seasonal fraud attempts or payment cycles, requiring heightened monitoring during these months.
- Transaction Types: Withdrawals dominate (66.7%), followed by Payments (26.67%) and Deposits (6.67%), with withdrawals being the primary anomaly source.
- Income Correlation: The 15-20 lakh income group has the highest anomaly amount, indicating potential targeting of higher-income accounts.
- Occupation Risks: IT Professionals lead in anomaly amounts, followed by Engineers and Business roles, while Students, Retired individuals, and Doctors show lower but still significant anomalies, suggesting occupation-specific vulnerabilities.
- Regional Variation: Bangalore shows the highest transaction volume (1.74M), but anomaly percentages vary across cities (e.g., Pune at 4.46% Anomaly Count %), pointing to localized fraud trends.
## 📖 How to Use
- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use the slicers (Account Type, Year, Month) to filter and analyze specific segments.
- Explore the visuals to identify anomaly patterns and trends.
## 📂 Project Structure
- Anomaly_Detection_Report.pbix: The main Power BI file.
- screenshots/: <img width="1057" height="733" alt="Screenshot 2025-08-16 180308" src="https://github.com/user-attachments/assets/df37ab57-016d-4db8-b93a-d42bd47d6b11" />
- README.md: This file.
## 🛠️ Requirements
- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.
## 🤝 Contributions
Feel free to fork and suggest improvements, such as adding more DAX calculations or advanced visuals.
