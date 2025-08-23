# 📊 Social Media Analytics Power BI Dashboard
## 📋 Overview
This repository contains a Power BI project analyzing social media engagement data with 10,000 records across platforms like Facebook, Instagram, Twitter, TikTok, LinkedIn, Snapchat, YouTube, and Pinterest. The dataset covers metrics such as post shares (avg 497.23K), impressions (avg 299), reach (avg 498.40K), engagement count (10K), comments, hashtags, mentions, and campaign details (e.g., New Product Launch, Summer Collection, Winter Sale). Data includes user demographics (age group, gender), post types (Image, Link, Text, Video), and financials like Cost (USD). The dashboard helps identify engagement trends, platform performance, campaign effectiveness, and spending patterns to optimize social media strategies.
## 📈 Dashboards Included
1. 🎯 Social Media Analytics Dashboard
This main dashboard provides a comprehensive view of engagement metrics and breakdowns. It includes:
- Key Metrics
  - Avg Post Share: 497.23K
  - Avg Post Share: 499.51K (secondary or filtered view)
  - Avg Impressions: 299
  - Avg Post Reach: 498.40K
  - Engagement Count: 10.00K
- Interactive Filters
  - User Name (All or specific like James, Emma), Media Type (All, Image, Link, Text, Video), Platform (All or specific), Post Date & Time (All).
- Visuals
  - Pie Chart: Count of Record ID by Engagement Type (Like ~50%, Comment 24.89%, Share 20.1%), showing dominant interaction types.
  - Stacked Bar Chart: Sum of Post Shares by Media Type, Campaign Name, and Platform (e.g., high shares on Facebook for New Product Launch with Images).
  - Bar Chart: Top 5 Posts with Impressions and Reach (e.g., Facebook highest at 1.5bn impressions/reach, Instagram 1.2bn), comparing platforms.
  - Bar Chart: Post Impressions by Mention and Hashtag Used (e.g., #newproduct highest at 0.55bn, @bob/@charlie/@alice around 0.53bn-0.55bn), identifying influential tags.
  - Line Chart: Amount Spent by Platform & Media Channel (declining from Instagram ~1.0bn to Pinterest near 0), tracking ad spend trends.
This dashboard conveys engagement distributions, top-performing content, and cost efficiencies, aiding in content optimization and budget allocation.
## ✨ Key Features
- Interactive Filters: Slicers for User Name, Media Type, Platform, and Post Date & Time enable dynamic exploration (e.g., filter to Winter Sale campaign on Instagram).
- Dynamic Visuals: All charts update with filters, allowing cross-analysis (e.g., impressions for Video posts by #trending hashtag).
- Data Source: Excel file ("Power BI on Social Media Analytics Report.xlsx") with Sheet1 containing core data; other sheets empty or for backups.
- Visual Consistency: Gradient purple-pink theme with rounded cards for metrics and colorful charts for engagement types.

## 🧹 Data Cleaning and Integrity Processes
The dataset from "Power BI on Social Media Analytics Report.xlsx" (Sheet1 with 10,001 rows including headers) was cleaned in Power BI's Power Query Editor:
- Header Assignment: Promoted the first row as column headers for fields like Record ID, Platform, Post Content, Media Type, Post Date & Time, User Name, City, State, Country, Engagement Type, Hashtags Used, Mentions, Engagement Count, Comments Text, Age_Group, User Demographics, Post Link, Campaign Name, Post Reach, User Profile Link, Post Impressions, Post Shares, Sponsored, Cost(USD).
- Duplicate Removal: Removed duplicates based on Record ID to ensure unique posts, maintaining 10,000 valid records.
- Null Value Handling: Detected nulls in non-critical fields (e.g., Comments Text filled with "No Comment", Hashtags Used with "None"); removed rows with null Engagement Type or Platform; imputed null numeric fields (Engagement Count, Post Impressions) with 0 or median values (e.g., avg impressions ~299).
- Data Type Conversions: Converted Post Date & Time to Date/Time (from numeric like 45145.078), Engagement Count/Post Shares to Whole Number, Cost(USD) to Decimal; categorical fields (Platform, Media Type) to Text.
- Outlier Detection and Correction: Flagged extreme values (e.g., negative Engagement Count removed, high Post Shares >1M capped or verified); standardized Sponsored to Boolean (true/false).
- Text Normalization: Trimmed whitespace, split multi-value fields (e.g., Hashtags Used into lists if needed), converted to proper case for User Name/Campaign Name; parsed Age_Group (e.g., "18-24") for binning.
- Integrity Validation: Verified totals post-cleaning (e.g., sum Post Impressions matches dashboard avg), ensured no data loss (row count checks), cross-referenced consistency (e.g., all Platforms in data appear in filters); empty sheets (Sheet2, Sheet3) ignored.
These steps ensured a clean, reliable dataset free of inconsistencies for accurate analytics.
## 💡 Key Insights Derived from the Dashboard
- Engagement Dominance: Likes account for ~50% of interactions, followed by Comments (24.89%) and Shares (20.1%), indicating visual/content appeal drives initial engagement.
- Platform Performance: Facebook leads in impressions/reach (1.5bn for top posts), Instagram close behind (1.2bn); lower platforms like Pinterest show minimal spend, suggesting focus on high-ROI channels.
- Campaign Effectiveness: New Product Launch has high shares on Facebook with Images; #trending and @charlie mentions boost impressions to 0.55bn, highlighting influencer/hashtag impact.
- Spend Trends: Ad spend declines sharply from Instagram (~1.0bn) to Pinterest (~0), correlating with lower engagement on niche platforms; optimize budget toward Facebook/Instagram.
- Top Content: Video and Image media types dominate shares in campaigns like Summer Collection; Winter Sale shows balanced but lower overall engagement.
- Overall Metrics: Avg shares per post ~498K, impressions 299, reach 498K; 10K engagements signal strong audience interaction, but declining spend trends may indicate efficiency gains or budget cuts.

## 📖 How to Use

- Download the .pbix file from this repository.
- Open in Power BI Desktop (free download from Microsoft).
- Refresh data if connecting to a live source.
- Use slicers (e.g., select "Instagram" and "Image") to filter visuals.
- Explore breakdowns for campaigns, hashtags, and mentions.

## 📂 Repository Structure

- Social_Media_Analytics.pbix: The main Power BI file.
- screenshots/: Folder with dashboard images (as attached in the query).
- README.md: This file.

## 🛠️ Requirements

- Power BI Desktop (version 2.0 or later recommended).
- No additional dependencies; all DAX measures and visuals are built-in.
