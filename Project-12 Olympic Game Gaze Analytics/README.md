# 📊 Olympic Game Gaze Analytics Power BI Dashboard
## 📋 Overview
This repository contains a Power BI project analyzing Olympic Games data from 1896 to 2016, covering 35 years, 66 sports, 271.12K medals, 136K participants, and 765 events. The dashboard provides insights into participation, medal distributions, gender trends, geographic event locations, and historical patterns across summer and winter seasons. It helps visualize Olympic achievements by teams, sports, and demographics to support sports analytics and historical research.
## 📈 Dashboards Included
The project features two main dashboard pages, each with interactive visuals, KPIs, and filters for in-depth exploration.
1. 🎯 Main Analytics Dashboard
This page offers key metrics and tabular breakdowns of Olympic data. It includes:
- Key Metrics (DAX Cards)
  - Years: 35 (DISTINCTCOUNT on year column).
  - Sports: 66 (DISTINCTCOUNT on sport column).
  - Medals: 271.12K (SUM or COUNT on medal-related fields).
  - Participants: 136K (DISTINCTCOUNT on participant IDs).
  - Events: 765 (DISTINCTCOUNT on event column).
  - Male Pax: 102K (COUNT filtered by male gender).
  - Female Pax: 34K (COUNT filtered by female gender).
  - Gold Medal: 13.37K (COUNT filtered by gold).
  - Silver Medal: 13.12K (COUNT filtered by silver).
  - Bronze Medal: 13.30K (COUNT filtered by bronze).
- Interactive Filters
  - Year slider (1896-2016), Season (Summer/Winter), Gender (F/M), Team (All or specific), Sport (All or specific), Medal (Bronze/Gold/No Medal/Silver).
- Visuals
  - Table: Top Teams by Medals (e.g., United States: 1,784 total, 747 gold; France: 1,198 total), showing breakdowns by medal type.
  - Table: Sports by First Year and Event Count (e.g., Athletics: 1896, 29,362 events; Gymnastics: 1896, 26,707 events).
This dashboard conveys aggregate statistics and rankings, highlighting dominant teams and sports over time.
2. 📊 Visual Analytics Dashboard
This page emphasizes graphical representations of trends and distributions. It includes:
- Interactive Filters
  - Same as main dashboard: Year slider, Season, Gender, Team, Sport, Medal.
- Visuals
  - Pie Chart: Participants by Gender (Female: 25.07%, Male: 74.93%), illustrating gender participation imbalance.
  - Map: Count of Events by City (bubbles sized by event count, e.g., large in Europe like Paris, London; smaller in Asia/America), showing geographic hosting patterns.
  - Horizontal Bar Chart: Total Medals by Sport (Athletics highest at ~40K, followed by Gymnastics ~30K, Swimming ~25K), ranking sports by medal volume.
  - Line Chart: Total Medals by Year (rising trend from 1890s low to peaks in 1980s-2000s, with fluctuations), depicting historical growth.
This dashboard conveys visual trends in participation, geography, and performance, aiding in spotting evolutions like increasing medals over decades.
## ✨ Key Features
- Interactive Filters: Slicers for Year, Season, Gender, Team, Sport, and Medal enable dynamic slicing across all visuals.
- Dynamic Visuals: Charts and tables update in real-time with filters, allowing cross-analysis (e.g., medals by sport for a specific team).
- Data Source: Based on aggregated Olympic data (not included in this repo for privacy; assume CSV or Excel import in Power BI).
- Visual Consistency: Olympic-themed colors with blue, green, red accents for readability and engagement.

## 🧹 Data Cleaning and Integrity Processes
The dataset was cleaned in Power BI's Power Query Editor to ensure accuracy and usability:
- Header Assignment: Promoted the first row as column headers for fields like Year, Sport, Medal, Participant, Event, Team, City, Gender, Season.
- Duplicate Removal: Identified and removed duplicate rows based on unique keys (e.g., Participant ID + Event + Year) to avoid overcounting medals or participants.
- Null Value Handling: Detected nulls in key columns; replaced null Medals with "No Medal", null Genders with "Unknown", and removed rows with null Years or Teams; for numeric fields like Event Count, nulls were set to 0.
- Data Type Conversions: Converted Year to Whole Number, Medal counts to Integer, Gender/Season to Text; ensured consistent formatting (e.g., standardized country names like "United States" vs. "USA").
- Outlier Detection and Correction: Flagged and investigated anomalies (e.g., negative medal counts removed, extreme participant numbers capped or verified); used conditional columns to categorize seasons (Summer/Winter).
- Text Normalization: Trimmed whitespace, converted to proper case for Teams/Sports/Cities, and split combined fields if needed (e.g., Event descriptions).
- Integrity Validation: Checked row counts pre/post-cleaning, verified sums (e.g., total medals match gold + silver + bronze), and ensured no data loss via queries; cross-referenced with known Olympic facts for accuracy.

- DAX Measures: Defined for KPIs (e.g., Total Medals = COUNTROWS(Fact), Gold Medals = CALCULATE(COUNTROWS(Fact), Fact[Medal] = "Gold")) to handle filters dynamically.
- Performance Optimization: Applied row-level security if needed, summarized data for large sets, and used hierarchies (e.g., Year > Season) for drill-downs.

This model ensures efficient querying, reduces redundancy, and supports complex slicers without performance issues.
## 💡 Key Insights Derived from the Dashboards
- Dominant Teams: United States leads with 1,784 medals (747 gold), followed by France (1,198) and Great Britain (1,140), highlighting Western dominance in Olympics.
- Top Sports: Athletics has the most events (29,362) and medals (~40K), Gymnastics (26,707 events), and Swimming (21,195 events), indicating these as core Olympic disciplines since 1896.
- Gender Imbalance: Males represent 74.93% of participants (102K) vs. females at 25.07% (34K), showing historical male bias, though likely improving in recent years.
- Historical Trends: Medals increase over time, peaking post-1980s, with fluctuations possibly due to world events (e.g., wars); summer events dominate.
- Geographic Hosting: Europe hosts most events (large bubbles in Paris, London, Berlin), followed by North America (Los Angeles, Atlanta), suggesting logistical preferences for developed regions.
- Medal Distribution: Gold (13.37K), Silver (13.12K), and Bronze (13.30K) are nearly equal, but no-medal participants far outnumber winners, emphasizing competition intensity.

## 📖 How to Use
- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use slicers (e.g., select "Summer" and "Gold") to filter visuals.
- Switch between pages using navigation tabs.

## 📂 Repository Structure
- Olympic_Game_Gaze_Analytics.pbix: The main Power BI file.
- screenshots/: <img width="1171" height="727" alt="Screenshot 2025-08-23 105026" src="https://github.com/user-attachments/assets/cb4c9178-f178-42bc-8c6d-db596ba05b10" />
- Source files : 
- README.md: This file.

## 🛠️ Requirements
- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.
