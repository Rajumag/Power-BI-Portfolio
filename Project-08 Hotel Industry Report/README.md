# 📊 Project Overview
This Power BI dashboard provides a comprehensive analysis of hotel industry performance across multiple years, regions, market segments, and top hotels. The report helps management track revenue, occupancy, ADR (Average Daily Rate), and RevPAR (Revenue per Available Room) while analyzing performance trends and customer segments.

The dashboard serves as a decision-support tool for hotel executives, analysts, and revenue managers.

## 🧹 Data Preparation & Cleaning
- Extracted first row as headers for proper field naming
- Removed duplicates to ensure reliable KPIs
- Handled null values by replacing with averages/known values
- Converted date fields into time intelligence-friendly format
- Applied numeric formatting for financial & percentage measures
- Categorized hotels by region and market segment for filtering

## 📌 Dashboard Features
## 🔑 KPI Cards
- Revenue (₹411.56M) – Total industry revenue
- Occupancy (54.61%) – Rooms sold vs rooms available
- ADR (2.76M) – Avg. revenue per occupied room
- RevPAR (2.75M) – Revenue per available room

## 📈 Trend Analysis
- Monthly trends for Revenue, Occupancy, ADR, RevPAR
- Identifies seasonality & demand fluctuations

## 📊 ADR Variance
- Staircase chart shows steady month-on-month ADR growth

## 🥧 Revenue Bifurcation
- Segment-wise revenue split:
- Business 20%
- Family 20%
- Budget 20%
- Boutique 20%
- Luxury 20%

## 📌 Regional & Segment Performance
- Matrix chart for Region vs Market Segment comparison

## 🏨 Top 10 Hotels Table
- Includes: Revenue, Occupancy, ADR, RevPAR, Rating, and Satisfaction Score
- Highlights top & low performers

## 🔑 Key Insights
- Revenue & Occupancy
  - Industry revenue is ₹411.56M with ~55% occupancy → growth potential exists.
- ADR & RevPAR
  - ADR (2.76M) and RevPAR (2.75M) are aligned → efficient pricing strategy.
  - ADR shows consistent upward growth → hotels are capturing value.
- Seasonality
  - Peak demand in March & August → seasonal travel spikes.
  - Declines in June–July & Sept–Oct → off-season dips.
- Market Segment Distribution
  - Revenue split evenly across 5 segments → well-diversified customer base.
  - Luxury & boutique → higher ADR; Budget & Family → higher occupancy.
- Top Hotels
  - William S Inc & Smith LLC → highest revenue + satisfaction scores.
  - Walker Group → strong ADR but low occupancy (pricing issue).

## 🎯 Business Recommendations
- Occupancy Growth
  - Launch targeted promotions in low-occupancy months (June–Oct) to boost bookings.
  - Dynamic pricing & seasonal discounts to fill unsold inventory.
- Pricing Strategy
  - Continue ADR growth strategy, but balance with occupancy in regions with weak demand.
  - For hotels like Walker Group, reduce ADR slightly to improve occupancy without hurting RevPAR.
- Market Segment Optimization
  - Leverage Luxury & Boutique for premium revenue growth.
  - Strengthen Budget & Family packages to drive occupancy during off-season.
- Regional Expansion
  - Identify underperforming regions from the Region vs Market Segment matrix.
  - Allocate marketing budget to lagging regions with high growth potential.
- Customer Experience
  - Top hotels with high satisfaction scores (William S Inc, Smith LLC) → best practices can be replicated chain-wide.
  - Focus on guest experience in mid-performing hotels to lift ratings.
## 🛠 Tools & Techniques Used
- Power BI (Data Modeling, DAX Measures, Interactive Slicers)
- Time Intelligence (Year, Month filters)
- Visualization Techniques: KPIs, Line Charts, Donut Charts, Matrix, Tables
- Data Transformation: Cleaning, Handling Nulls, Standardization

## 🚀 Purpose of the Dashboard
- Monitor hotel industry performance in real-time
- Enable data-driven pricing and marketing strategies
- Identify top-performing hotels & underperforming areas
- Support strategic decision-making in occupancy growth & revenue optimization

## 📂 Repository Structure

Hotel_Industry_Report.pbix: The main Power BI file.
screenshots/: <img width="1059" height="736" alt="Screenshot 2025-08-17 110339" src="https://github.com/user-attachments/assets/ac4d1c5c-3d24-409c-a826-cc1a7d928020" />
Dataset Used : 
README.md: This file.
