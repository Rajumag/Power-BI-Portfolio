# 📊 Patient Analytics Dashboard Power BI Project
## 📋 Overview
This repository contains a Power BI project analyzing patient data from a healthcare dataset with 1,000 patients. The dashboard provides insights into demographics (gender, age groups, states), medical histories, primary diagnoses, and visit patterns. It includes metrics like average age (51.35), total visits (5,104), and distributions across conditions such as Anxiety, Arthritis, Asthma, Diabetes, Heart Disease, Hypertension, and Migraine. The project helps healthcare providers understand patient profiles, disease prevalence by demographics, and resource allocation needs.
## 📈 Dashboards Included
The project features three main dashboard views, each focusing on different aspects of patient data with interactive filters for Gender, Age Group, State, and Medical History.
1. 🎯 Patient Demographic Overview
This page summarizes overall patient demographics and distributions. It includes:
- Key Metrics
  - Total Patients: 1,000
  - Avg Age: 51.35
  - Total Visits: 5,104
- Interactive Filters
  - Gender (Female, Male, Other), Age Group (All or specific bins like 0-20, 20-40), State (All), Medical History (All or specific conditions).
- Visuals
  - Stacked Bar Chart: # Patients by Age Group and Medical History (e.g., 0-20: 20.35% Anxiety, 19.77% Arthritis; showing percentages across conditions per age bin).
  - Pie Chart: # Patients by Gender (Female: 33.1%, Male: 35.4%, Other: 31.5%), highlighting near-equal distribution.
  - Horizontal Bar Chart: # Patients by State (Manipur and Meghalaya tied at 47, Haryana 43, Himachal Pradesh 42, etc.), identifying regional concentrations.
This dashboard conveys patient composition by key demographics and health conditions, aiding in targeted healthcare planning.
2. 📊 Patient Age Distribution
This page focuses on age-based breakdowns and primary diagnoses. It includes:
- Interactive Filters
  - Same as overview: Gender, Age Group, State, Medical History.
- Visuals
  - Stacked Bar Chart: # Patients by Age Group by Primary Diagnosis (e.g., 0-20: 23.26% Asthma, 21.51% Diabetes; percentages across diagnoses like Asthma, Diabetes, Heart Disease, Arthritis, Hypertension).
  - Pie Chart: # Patients by Age Group (0-20: 17.2%, 20-40: 22.3%, 40-60: 18.8%, 60-80: 20.5%, 80-100: 18.3%, 100+: 2.9%), showing a balanced but slightly skewed distribution toward middle ages.
This dashboard conveys how primary diagnoses vary by age, highlighting age-specific health trends.
3. 🎯 Visits Summary
This page analyzes visit volumes by diagnosis and age. It includes:
- Interactive Filters
  - Same as previous dashboards.
- Visuals
  - Stacked Bar Chart: # Visits by Age Group by Primary Diagnosis (e.g., Asthma: 18.52% in 0-20, 17.04% in 20-40; similar for other diagnoses).
  - Table: Primary Diagnosis by Age Group (counts, e.g., Asthma: 37 in 0-20, 51 in 20-40; totals like Asthma: 212, Hypertension: 27).
      - Sub-rows for combinations (e.g., Asthma, Hypertension: 4 in 0-20, 3 in 20-40).
This dashboard conveys visit frequency patterns, helping identify high-demand diagnoses and age groups for resource optimization.
## ✨ Key Features
- Interactive Filters: Slicers for Gender, Age Group, State, and Medical History allow dynamic data exploration across all pages.
- Dynamic Visuals: Charts and tables update based on filters, enabling cross-analysis (e.g., female patients in 40-60 age group by state).
- Data Source: Based on aggregated patient data (not included in this repo for privacy; assume CSV or Excel import in Power BI).
- Visual Consistency: Light blue-gray theme with colorful accents for conditions and demographics, ensuring intuitive navigation.

## 🧹 Data Cleaning and Integrity Processes
The dataset was cleaned in Power BI's Power Query Editor to ensure reliability and accuracy:
- Header Assignment: The first row was promoted to column headers for fields like Gender, Age Group, State, Medical History, Primary Diagnosis, Visits.
- Duplicate Removal: Duplicates were identified and removed using unique patient IDs to prevent overcounting in totals like patients (1,000) or visits (5,104).
- Null Value Handling: Nulls in categorical fields (e.g., Gender, State) were replaced with "Other" or "Unknown"; null Ages were imputed with median (51); null Visits/Medical History were set to 0 or removed if critical.
- Data Type Conversions: Age to Whole Number, Gender/State to Text, Visits to Integer; binned Age into groups (0-20, 20-40, etc.) via conditional columns.
- Outlier Detection and Correction: Flagged extreme Ages (e.g., >100 or <0) and capped or removed; ensured Visit counts were non-negative.
- Text Normalization: Standardized condition names (e.g., "heart disease" to "Heart Disease"), trimmed whitespace, and converted to proper case for consistency.
- Integrity Validation: Verified totals (e.g., sum of age group patients = 1,000), checked for balanced gender pie (adding to 100%), and cross-referenced distributions; no data loss confirmed via row counts pre/post-cleaning.
These steps ensured a clean, integral dataset free of errors for accurate analytics.
## 💡 Key Insights Derived from the Dashboards
- Demographic Balance: Gender distribution is nearly equal (Female 33.1%, Male 35.4%, Other 31.5%), with average age 51.35, indicating a mature patient base.
- Age and Conditions: 20-40 age group has high Anxiety (19.28%) and Heart Disease (18.39%); older groups (80-100) show higher Hypertension (31.03%) and Arthritis (27.59%), suggesting age-related disease patterns.
- Regional Concentrations: Top states like Manipur and Meghalaya (47 patients each) may indicate regional health hotspots; lower states like Jharkhand and Tamil Nadu (39 each) could reflect data sampling or access issues.
- Diagnosis Prevalence: Asthma is common in younger groups (e.g., 18.52% visits in 0-20), while Hypertension dominates older ones (24.31% in 60-80), with combinations like Asthma+Hypertension rare but present.
- Visit Volumes: Total visits (5,104) exceed patients (1,000), averaging ~5 visits per patient; pie shows balanced age spread, but 20-40 (22.3%) and 0-20 (17.2%) drive younger diagnoses.
- Overall Trends: Primary diagnoses like Asthma (212 total) and Diabetes (not directly totaled but visible in breakdowns) vary by age, emphasizing need for age-targeted interventions.

## 📖 How to Use
- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use slicers to filter (e.g., select "Female" and "Hypertension" to view specific distributions).
- Navigate between pages using tabs for demographics, age, and visits views.

## 📂 Repository Structure
- Patient_Analytics_Dashboard.pbix: The main Power BI file.
- screenshots/: <img width="1258" height="731" alt="Screenshot 2025-08-23 123505" src="https://github.com/user-attachments/assets/72d1c1fb-32ac-4cf0-8d21-c4a50dd69098" />
- Source file : Excel files.
- README.md: This file.

## 🛠️ Requirements

- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.
