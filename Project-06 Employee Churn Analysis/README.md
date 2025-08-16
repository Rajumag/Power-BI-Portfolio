# 📊 Employee Attrition Analysis Power BI Dashboard
## 📋 Overview
- This repository contains a Power BI project analyzing employee attrition data for a company with a total of 1,470 employees. The dashboard provides insights into attrition trends based on various factors such as department, job role, age group, income, overtime, gender, and job satisfaction. It helps HR teams identify key drivers of employee turnover and develop strategies to improve retention.
## 📈 Dashboards Included
### 1. 🎯 Employee Attrition Analysis Dashboard
This dashboard offers a comprehensive view of employee attrition metrics and their distribution across different categories. It includes the following visuals and what they convey:

- Key Metrics
  - Total Employees: 1,470
  - Attrition Count: 237
  - Attrition Rate: 16.1%
  - Average Age: 36.92 years
  - Average Monthly Income: 6.50K
  - Overtime %: 28.3%
- Gender Breakdown
  - Displays the proportion of male and female employees, with interactive filters to analyze attrition by gender.
- Attrition by Department
  - Pie chart showing attrition distribution (e.g., 13.84% in Human Resources, 25.86% in Research & Development), highlighting departments with higher turnover.
- Attrition by Job Role
  - Bar chart ranking job roles by attrition rate (e.g., Sales Representative at 20.63%, Laboratory Technician at a lower rate), identifying roles with significant turnover.
- Attrition by Age Bin
  - Bar chart showing attrition rates by age groups (e.g., 30% for 50 Above, 10% for 20-29), indicating age-related turnover patterns.
- Attrition by Income
  - Bar chart comparing attrition across income levels (e.g., highest in Low income bracket), suggesting income as a potential factor.
- Attrition by Overtime
  - Pie chart showing 10.64% attrition for employees with no overtime vs. 30.53% with overtime, highlighting the impact of overtime on retention.
- Attrition Rate by Job Satisfaction
  - Bar chart linking attrition rates to job satisfaction levels (e.g., 22.84% for satisfaction level 1, 11.33% for level 4), showing a clear correlation.
The dashboard aims to provide actionable insights into which employee segments are most at risk of leaving and the factors contributing to attrition, aiding in targeted retention strategies.
## ✨ Key Features
- Interactive Filters: Slicers for Gender, Overtime, Age Group, and Department allow users to drill down into specific data subsets.
- Dynamic Visuals: All charts update based on filter selections, providing a flexible analysis tool.
- Data Source: Based on aggregated employee data (not included in this repo for privacy; assume CSV or Excel import in Power BI).
- Visual Consistency: Green-themed visuals for a clean and professional look.
## 💡 Key Insights Derived from the Dashboard
- High Attrition Rate: The overall attrition rate of 16.1% (237 out of 1,470 employees) indicates a significant turnover challenge, particularly in certain departments and roles.
- Departmental Impact: Research & Development (25.86%) and Sales (20.63%) show the highest attrition, suggesting potential issues like workload or job satisfaction in these areas.
- Age Influence: Employees aged 50 and above have the highest attrition rate (30%), while the 20-29 age group is lowest (10%), possibly due to retirement or dissatisfaction among older workers.
- Overtime Correlation: Employees working overtime have a 30.53% attrition rate compared to 10.64% for those who don’t, indicating overtime as a major contributor to turnover.
- Income Levels: Attrition is highest in the low-income bracket, suggesting that salary dissatisfaction may drive exits.
- Job Satisfaction Link: Attrition decreases with higher job satisfaction, with a 22.84% rate at the lowest satisfaction level (1) dropping to 11.33% at the highest (4), underscoring the need for better employee engagement.
- Gender Balance: The gender breakdown shows a balanced workforce, but further analysis by gender filter could reveal specific trends.

## 📖 How to Use
- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use the slicers (Gender, Overtime, Age Group, Department) to filter and analyze specific segments.
- Explore the visuals to identify trends and correlations.

## 📂 Repository Structure

- Employee_Attrition_Dashboard.pbix: The main Power BI file.
- screenshots/: <img width="1269" height="731" alt="Employee" src="https://github.com/user-attachments/assets/53654a95-b999-4ea5-9463-105dd61362d5" />
- README.md: This file.

## 🛠️ Requirements

- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.

## 🤝 Contributions
- Feel free to fork and suggest improvements, such as adding more DAX calculations or advanced visuals.
