# 📊 Movie Recommendation System Power BI Dashboard
## 📋 Overview
This repository contains a Power BI project analyzing movie rating data from 987K users across 3,706 movies, spanning 18 genres and 21 occupations. The dashboard provides insights into user preferences, rating distributions, and demographic trends to support movie recommendations. Data covers genres like Comedy, Drama, and Horror, with average ratings of 3.58. The project includes multiple tabs for detailed exploration, navigation buttons, and a drillthrough page for top-rated movies.
## 📈 Dashboards Included
The project features five main tabs (Overview, Genres, Occupation, Age Group, Top Rated) with interactive visuals, plus a drillthrough page. Each tab conveys specific aspects of user behavior and movie preferences.
1. 🎯 Overview
This tab provides a high-level summary of the dataset and top-level trends. It includes:
- Key Metrics (DAX Cards)
  - Genres: 18 (Calculated using DISTINCTCOUNT on genre column).
  - Occupations: 21 (Calculated using DISTINCTCOUNT on occupation column).
  - Movies Rated: 3,706 (Calculated using DISTINCTCOUNT on movie ID or title).
  - Users Participated: 987K (Calculated using DISTINCTCOUNT on user ID).
- Visuals
  - Bar Chart: Top Rated Genres (e.g., Animation at 4.4, Film-Noir at 4.3, down to Children's at 3.0), showing average ratings per genre.
  - Stacked Bar Chart: Avg Rating by Occupation Name and Genres (multi-colored bars for genres like Action, Adventure, etc., across occupations like retired, scientist, doctor).
This tab conveys overall dataset scale and genre popularity, helping identify universally liked genres.
2. 📊 Genres
This tab focuses on genre-specific participation and ratings. It includes:
- Key Metrics (DAX Cards)
  - Users Participated: 987K (DISTINCTCOUNT on users filtered by genre).
  - Avg Rating: 3.58 (AVERAGE on rating column).
  - Movies Rated: 3,706 (DISTINCTCOUNT on movies filtered by genre).
- Visuals
  - Slicer: Gender (F, M).
  - Bar Chart: Users Participated by Genres and Gender (Comedy highest at ~100K for M, Drama next).
  - Occupation Slicer and Bar Chart: Users by Occupation (academic/educator highest).
  - Stacked Bar Chart: Users Participated by Genres and Age (Comedy popular across ages, e.g., 25-34 at 48K).
  - Table: Genres with Users Participated and Avg Rating (e.g., Comedy: 680,428 users, 3.46 avg).
This tab conveys genre appeal by demographics, highlighting preferences like Comedy's broad reach.
3. 🎯 Occupation
This tab analyzes ratings by occupation. It includes:
- Key Metrics (DAX Cards)
  - Users Participated: 987K.
  - Avg Rating: 3.58.
  - Movies Rated: 3,706.
- Visuals
  - Slicer: Gender (F, M).
  - Bar Chart: Users Participated by Occupation Name (college/grad student highest at ~150K, farmer lowest).
  - Table: Occupation Name with Users Participated and Avg Rating (e.g., writer: 5,297 users, 3.50 avg; retired: 13,540 users, 3.78 avg).
  - Scatter Plot: Avg Rating and Users Participated by Occupation Name (retired highest rating at ~3.80, farmer lowest at ~3.45).
This tab conveys how occupations influence rating patterns, e.g., retired users rate higher overall.
4. 📊 Age Group
This tab explores age-based trends. It includes:
- Key Metrics (DAX Cards)
  - Users Participated: 987K.
  - Avg Rating: 3.58.
  - Movies Rated: 3,706.
- Visuals
  - Slicer: Gender (F, M).
  - Bar Chart: Users Participated by Age (25-34 highest at ~0.39M, Under 18 lowest at ~0.03M).
  - Key Influencers Visual: Factors influencing Avg Rating (e.g., Release Year 1941 increases rating by 0.34, 1952 by 0.03).
  - Bar Chart: Avg Rating by Release Year (higher for older films like 1941 at ~4.2).
This tab conveys age demographics and influences on ratings, showing older users or films impact scores.
5. 🎯 Top Rated (Drillthrough Page)
This drillthrough page activates when drilling from other tabs (e.g., clicking a genre or occupation). It provides detailed info on top-rated movies, including:
- Filters from source (e.g., genre, age group).
-  Visuals: Table or list of top movies by rating, with columns like Movie Title, Avg Rating, User Count, Release Year.

This page conveys granular recommendations, focusing on highest-rated films within selected filters.
## ✨ Key Features
- Navigation Buttons: Custom buttons on each tab link to other tabs (Overview, Genres, Occupation, Age Group, Top Rated) for seamless navigation.
- Drillthrough Functionality: Right-click or drill on visuals (e.g., genre bar) to access the Top Rated page for context-specific top movies.
- Interactive Filters: Slicers for Gender, Occupation, and Age Group across tabs
- DAX Measures as Cards: All KPIs use DAX like DISTINCTCOUNT for counts, AVERAGE for ratings, ensuring dynamic updates.
- Data Source: Imported from DAT files via Python script (detailed below).
- Visual Consistency: Dark theme with red accents for emphasis.

## 🧹 Data Cleaning and Integrity Processes
Data was procured from DAT files (likely MovieLens dataset format with :: separators). A Python script was used to import and preprocess:
- Python Script for Import:
  - Used pandas to load DAT files: e.g., pd.read_csv('movies.dat', sep='::', header=None, names=['MovieID', 'Title', 'Genres'], engine='python') for movies; similar for users (UserID, Gender, Age, Occupation, Zip) and ratings (UserID, MovieID, Rating, Timestamp).
  - Handled encoding issues with encoding='ISO-8859-1'.
  - Split multi-genre fields (e.g., 'Action|Adventure' into separate rows or flags for analysis).
  - Exported cleaned DataFrames to CSV: e.g., movies.to_csv('movies_clean.csv', index=False) for Power BI import.
- Power BI Cleaning:
   - Header Assignment: Promoted first row as headers post-import.
   - Duplicate Removal: Removed duplicates on UserID-MovieID for ratings to avoid double-counting.
   - Null Value Handling: Replaced null ratings with 0 or removed; filled missing demographics with 'Unknown'.
   - Data Type Conversions: Converted Rating to Whole Number, Timestamp to Date, Age to bins (Under 18, 18-24, etc.).
   - Outlier Detection: Filtered ratings outside 1-5 scale; removed invalid genres/occupations.
   - Integrity Validation: Ensured relationships (UserID, MovieID) via star schema; verified totals (e.g., sum of genre ratings matches overall).
   - DAX for Integrity: Measures like CALCULATE(AVERAGE(Ratings[Rating]), FILTER(...)) for filtered averages.
These steps ensured data accuracy, with ~987K users and 3,706 movies post-cleaning.
## 💡 Key Insights Derived from the Dashboards
- Genre Preferences: Animation (4.4) and Film-Noir (4.3) top ratings, while Children's (3.0) and Horror (3.1) are lowest, suggesting users favor artistic or noir films over family/horror.
- Occupation Trends: Retired users rate highest (3.78), possibly due to more time/selectivity; farmers lowest (3.45). Scientists/Doctors prefer Drama/Documentary.
- Age Demographics: 25-34 group dominates participation (~0.39M users), with higher ratings for older films (e.g., 1941 at 4.2), indicating nostalgia bias.
- Gender Differences: Males participate more in most genres (e.g., Comedy ~100K M vs. lower F), but avg ratings similar (3.58 overall).
- Overall Engagement: Comedy has most users (680K) but avg rating 3.46; Documentary fewer users (6K) but higher 3.96, suggesting niche appeal.
- Influencers on Ratings: Release years like 1941 boost ratings by 0.34, highlighting classic films' enduring popularity.

## 📖 How to Use
- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Use navigation buttons to switch tabs.
- Apply filters (e.g., Gender) and drillthrough on visuals for top movies.
- Explore DAX cards for quick stats.

## 📂 Repository Structure
- Movie_Recommendation_System.pbix: The main Power BI file.
- screenshots/: <img width="1306" height="733" alt="Screenshot 2025-08-19 133745" src="https://github.com/user-attachments/assets/c4ef62f3-3064-4434-998e-45ec0a7685a3" />
- README.md: This file.
- import_script.py: Sample Python script for DAT to CSV conversion (optional reference).

## 🛠️ Requirements
- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.

## 🤝 Contributions
Feel free to fork and suggest improvements, such as adding more DAX calculations or advanced visuals.
