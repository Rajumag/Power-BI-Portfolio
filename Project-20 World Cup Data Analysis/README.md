# 📊 Cricket World Cup Data Analysis Project

## 📝 Overview
This project involves creating interactive Power BI dashboards to analyze data from various Cricket World Cup tournaments (e.g., WC 2011, 2015, 2019, 2023). The dashboards provide insights into team performances, match statistics, player contributions, and more. The data is visualized through charts, cards, and filters to enable dynamic exploration of cricket metrics like runs, strike rates, sixes, fours, and match outcomes.

The project focuses on transforming raw cricket data into actionable visualizations, highlighting trends across World Cup series and individual matches.

## 🔧 Technologies Used
- **Power BI**: For data modeling, visualization, and dashboard creation.
- **Data Sources**: Atached to be CSV/Excel files containing match data, player stats, and World Cup records (e.g., runs scored, wickets, man of the match details).

## 🚀 Features
Here are the key features and components implemented in the project:

- **World Cup Series Filter**: A dropdown or button filter to select specific World Cup editions (e.g., WC 2011, WC 2015, WC 2019, WC 2023). This dynamically updates all visuals to show data for the chosen tournament.
- **Team Selection Filter**: Allows users to filter data by team (e.g., India, New Zealand, Sri Lanka). Displays team-specific stats like total runs, average strike rate, number of sixes, and number of fours.
- **Match ID Filter**: A dropdown to select individual matches by their unique ID, loading detailed stats for that game.
- **Overall Team Performance Dashboard**:
  - Cards displaying aggregate metrics: Total Runs, Average Strike Rate (formatted as 2.36K for large numbers), Number of Sixes, and Number of Fours.
  - Line chart visualizing "Runs by Match Date" with data points and labels (e.g., 294 on 15 February 2015, 297 on 22 February 2015, 286 on 19 March 2015).
- **Match-Specific Dashboard**:
  - Displays match details like teams involved (e.g., New Zealand vs Sri Lanka), total runs scored by each team, total wickets, winner announcement (e.g., "New Zealand won by 98 runs"), venue (e.g., Hagley Oval), and match date (e.g., 14 February 2015).
  - Bar charts for "Runs Scored" by individual players on both teams, sorted by highest runs (e.g., Corey Anderson as top scorer for New Zealand).
- **Man of the Match Visualization**: Uses Power BI's new card feature to showcase the Man of the Match with the player's name (e.g., Corey Anderson) and an embedded image of the player for a visually engaging presentation.
- **Interactive Elements**: All visuals are interconnected with slicers and filters for seamless navigation. For example, selecting a World Cup series updates team stats and match details automatically.
- **Custom Styling**: Dashboards feature a cricket-themed background (stadium view with lights), color-coded elements (e.g., orange for team names, cyan for bars), and icons (e.g., trophy for winner).

## 📸 Screenshots
Below are screenshots of the dashboards: <img width="1242" height="737" alt="Screenshot 2025-08-25 144935" src="https://github.com/user-attachments/assets/10db2093-4939-453f-ab73-25a0c6a844bf" />

### Match Details Dashboard (New Zealand vs Sri Lanka, Match ID: 656399)
![Match Details Dashboard](path/to/screenshot2.png)  
*Includes match outcome, player runs bar charts, and Man of the Match card with image.*

## 🛠️ What I Did in This Project
- **Data Preparation**: Imported and cleaned cricket World Cup data, including match results, player performances, and stats. Modeled relationships between tables (e.g., matches, teams, players) in Power BI.
- **Dashboard Design**: Created multiple pages for overview and detailed views. Applied custom themes, backgrounds, and layouts to mimic a cricket stadium aesthetic.
- **Visualizations Built**:
  - Cards for key metrics (runs, strike rate, sixes, fours).
  - Line charts for temporal trends (runs by date).
  - Bar charts for player comparisons.
  - New card visuals for enhanced Man of the Match display with images.
- **Filters and Interactivity**: Implemented slicers for series, teams, and matches. Ensured cross-filtering across visuals for dynamic analysis.
- **Testing and Refinement**: Tested dashboards with sample data to ensure accuracy (e.g., verifying run totals and winner logic). Refined visuals for better readability and performance.

## 📥 Installation and Usage
1. **Prerequisites**: Install Power BI Desktop (free from Microsoft).
2. **Open the Project**: Launch the `.pbix` file in Power BI Desktop.
3. **Refresh Data**: Connect to your data source (e.g., CSV files in the repo) and refresh the model.
4. **Interact**: Use the filters to explore different World Cups, teams, and matches.

## 🤝 Contributions
Feel free to fork the repo and submit pull requests for improvements, such as adding more World Cup data or new visuals.

---

This README provides a comprehensive overview of the project. Update paths to screenshots and add actual data sources if available!
