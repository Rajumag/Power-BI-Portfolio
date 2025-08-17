# 📊 HR Analytics Power BI Dashboard Project

## 📋 Overview

This repository contains a Power BI project analyzing HR data for a company with 1,466 total employees. The project includes multiple dashboard pages focusing on employee overview, performance trends, attrition rates, and ratings. It provides insights into workforce composition, turnover drivers, performance metrics, and employee satisfaction to support HR decision-making and retention strategies.

## 📈 Dashboards Included

The project features four interconnected dashboard pages, each designed to convey specific aspects of HR analytics through KPIs, charts, and interactive filters.

### 1. 🎯 HR Analytics Overview
This page provides a high-level summary of the workforce, including total headcount, activity status, and distributions by department and job role. It includes:
- **Key Metrics**
  - Total Employees: 1,466
  - Active Employees: 1,229
  - Inactive Employees: 146
  - Attrition Rate: 16.2%
  - Average Salary: 113K
- **Interactive Filters**
  - Gender slicer (Female, Male, Non-Binary) to segment data.
- **Visuals**
  - Stacked Bar Chart: Total Employees by Year and Attrition (e.g., 2012: 151 total with 127 No attrition and 24 Yes; showing trends from 2012 to 2022).
  - Pie Chart: Active Employees by Department (Technology: 826 or 67.04%, Sales: 352 or 28.64%, Human Resources: 51 or 4.15%).
  - Horizontal Bar Chart: Active Employees by Job Role (Sales Executive: 268, Software Engineer: 247, Data Scientist: 197, etc.).

This dashboard conveys overall workforce health, historical attrition trends, and current distribution, helping identify growth patterns and departmental imbalances.

### 2. 📊 HR Analytics Performance Analysis
This page focuses on trends in employee performance and satisfaction metrics over time, using line charts to track improvements or declines. It includes:
- **Interactive Filters**
  - Employee Name, Joining Date, Last Review Date, and Latest Manager Review (e.g., Exceeds Expectation).
- **Visuals**
  - Line Chart: Job Satisfaction Score (rising from ~1.5K in 2014 to 3.8K in 2022).
  - Line Chart: Environment Score (rising from ~1.7K in 2014 to 4.2K in 2022).
  - Line Chart: Training Opportunities (rising from 142 in 2014 to 1,019 in 2022).
  - Line Chart: Manager Rating (rising from 151 in 2014 to 1,125 in 2022).
  - Line Chart: Self Rating (rising from ~0.6K in 2014 to 4.5K in 2022).
  - Line Chart: WorkLife Balance (rising from ~0.5K in 2014 to 3.8K in 2022).

This dashboard conveys positive trends in employee engagement and development over the years, highlighting areas of improvement in satisfaction and training to correlate with retention.

### 3. 🎯 HR Analytics Attrition Rate
This page breaks down attrition rates by various factors to identify key drivers of turnover. It includes:
- **Visuals**
  - Pie Chart: By Business Travel (No Travel: 16.87%, Some Travel: 31.25%, Frequent Traveller: 52.0%).
  - Pie Chart: By Department (Technology: 25.86%, Sales: 38.63%, Human Resources: 35.51%).
  - Bar Chart: By Years at Company (highest at 0 years: 31.58%, decreasing to 0.78% at 10+ years).
  - Horizontal Bar Chart: By Job Role (Sales Representative: 39.76%, Recruiter: 37.50%, Data Scientist: 23.94%, etc.).
  - Treemap: By Stock Option Level (Level 0: 24.48%, Level 1: 9.41%, Level 2: 7.64%, Level 3: 17.65%).
  - Bar Chart: By Overtime (Yes: 30.60%, No: 10.47%).

This dashboard conveys factors influencing attrition, such as travel frequency, tenure, and benefits, to pinpoint high-risk groups for targeted interventions.

### 4. 📊 Ratings
This page visualizes employee ratings across satisfaction and performance categories, with a table for detailed employee data. It includes:
- **Interactive Filters**
  - Attrition (No, Yes), Year.
- **Visuals**
  - Bar Chart: Job Satisfaction (levels 1: 130, 2: 1,651, 3: 1,665, 4: 1,569, 5: not shown).
  - Bar Chart: Manager Rating (levels 2: 1.2K, 3: 2.2K, 4: 2.2K, 5: 1.1K).
  - Bar Chart: Work Life Balance (levels 1: 121, 2: 1,702, 3: 1,670, 4: 1,706, 5: 1,510).
  - Bar Chart: Training Opportunities Within Year (levels 1: 2.1K, 2: 2.2K, 3: 2.3K).
  - Table: Employee details (EmpID, Emp Name, Department, Job Role) for top-rated or filtered employees.

This dashboard conveys distribution of ratings and their relation to attrition, emphasizing how satisfaction levels impact employee retention.

## ✨ Key Features
- **Interactive Filters**: Slicers for Gender, Attrition, Year, Employee Name, Dates, and Reviews enable dynamic data exploration.
- **Dynamic Visuals**: Charts update with filters, allowing cross-analysis (e.g., attrition by gender or department).
- **Data Source**: Based on aggregated HR data (not included in this repo for privacy; assume CSV or Excel import in Power BI).
- **Visual Consistency**: Dark-themed interface with orange and blue accents for readability.

## 💡 Key Insights Derived from the Dashboards
- **Workforce Growth and Attrition**: Total employees peaked around 2020-2022, with attrition rates stable at ~16.2%; however, early years (e.g., 2012) show higher proportional attrition (24/151), suggesting onboarding challenges.
- **Departmental Dominance**: Technology department leads with 67% of active employees, but has a 25.86% attrition rate, indicating high demand but potential burnout.
- **Performance Improvements**: All performance metrics (e.g., Job Satisfaction from 1.5K to 3.8K, Training from 142 to 1,019) show upward trends from 2014 to 2022, correlating with reduced attrition over time.
- **Attrition Drivers**: Frequent business travel (52%) and overtime (30.60%) significantly increase attrition; roles like Sales Representative (39.76%) and short-tenure employees (31.58% at 0 years) are most vulnerable.
- **Ratings Correlation**: Higher ratings in Job Satisfaction and Work Life Balance (mostly levels 2-4) align with lower attrition; low ratings (level 1) are rare but highlight dissatisfaction hotspots.
- **Job Role Focus**: Technical roles (e.g., Software Engineer: 247 active) dominate, but sales roles have higher attrition (39.76% for Sales Rep), suggesting need for better support in client-facing positions.

## 📖 How to Use
1. Download the `.pbix` file from this repository.
2. Open in Power BI Desktop (free download from Microsoft).
3. Refresh data if connecting to a live source.
4. Navigate between pages using tabs at the bottom.
5. Use slicers to filter data and explore insights (e.g., select "Yes" for Attrition to view high-risk groups).

## 📂 Repository Structure
- `HR_Analytics_Dashboard.pbix`: The main Power BI file.
- `screenshots/`: <img width="1300" height="733" alt="Screenshot 2025-08-17 162453" src="https://github.com/user-attachments/assets/b23d09ff-f3b8-47c1-af96-6a9b67a2b158" />
- `Dataset` : 
- `README.md`: This file.

## 🛠️ Requirements
- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.

## 🤝 Contributions
Feel free to fork and suggest improvements, such as adding more DAX calculations or advanced visuals.
