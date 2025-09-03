Objectives: 
The objective of this project is to perform an end-to-end analysis of YouTube video data (17,590 rows) using Python, ensuring data accuracy, integrity, and consistency through data cleaning, feature engineering, exploratory data analysis (EDA), and visualization.
The analysis focuses on deriving key performance indicators (KPIs) and generating actionable business insights by addressing critical questions, including:

Which video categories receive the highest engagement and views?

How do video duration and resolution influence engagement metrics?

Which categories are consistently high-performing or underperforming?

Do hashtags improve video performance, and which hashtags are most linked to viral videos?

The ultimate goal is to transform raw YouTube metadata into a cleaned, structured, and insight-rich dataset, enabling content creators, marketers, and platform stakeholders to make data-driven decisions.

Dataset:

KPI/Questions:
1. Identify which video categories (e.g., Gaming, Comedy, News) receive the highest engagement in terms of views, likes, and comments.
2. Evaluate whether video duration or resolution influences engagement metrics.
3. Explore whether video popularity can be predicted using metadata features.
4. Assess whether videos with hashtags perform better than those without in terms of views, likes, and engagement rate.
5. Discover which hashtags are most frequently associated with viral videos and how they contribute to content success.

Process:
1. Define Objective
Frame business-driven questions around content performance, engagement predictors, and hashtag effectiveness.

2. Data Collection
Source: YouTube Dataset from Kaggle (17,590 rows, CSV format).
Imported into Python for exploration and analysis.

3. Data Cleaning & Preparation
Removed irrelevant columns (url, description).
Handled missing values (e.g., replaced empty hashtags with "No Hashtags").
Checked and removed duplicates.
Standardized categories and fixed inconsistencies.
Performed sanity checks (no negative/invalid values for views, likes, comments, duration).
Outlier detection and treatment: applied log transformations for skewed metrics.

4. Feature Engineering
Created new fields:
engagement_rate = (likes + comments) / views
duration_category (Short, Medium, Long, Very Long)
resolution (mapped from video height/width)
has_hashtags (binary flag)
is_viral (top 5% videos by views)

5. Exploratory Data Analysis (EDA)
Univariate Analysis: Histograms, boxplots, countplots for numeric & categorical features.
Bivariate Analysis: Scatterplots, heatmaps, grouped averages (views/engagement by category, duration, resolution).
Segmentation: Comparison across hashtags, categories, and viral vs non-viral videos.
Correlation Analysis: Identified relationships among numeric features.

6. Data Visualization & Insights
Barplots, scatterplots, and heatmaps tied directly to business questions:
Category-level performance (views, engagement).
Impact of duration & resolution on engagement.
Hashtag effectiveness.
Viral vs non-viral content patterns.

7. Reporting & Communication
Summarized workflow from objective → data → cleaning → analysis → insights.
Created an Executive Summary with key findings and business recommendations.
Highlighted stakeholders (creators, marketers, YouTube platform, advertisers).

8. Future Work / Next Steps
Add time-based trend analysis (if upload date is available).
Apply text analytics (NLP) on titles/hashtags for deeper insights.
Build an interactive dashboard (Power BI/Tableau).
Extend into predictive modeling for video virality (optional).

Executive Summary
Categories: Gaming & Comedy dominate in views, but Education has stronger engagement efficiency.
Duration: Medium-length videos (4–10 minutes) perform best for engagement.
Resolution: HD videos (720p/1080p) yield slightly higher engagement than low-quality formats.
Predictors: Likes and Comments are the strongest indicators of video success.
Hashtags: Videos with hashtags consistently achieve higher engagement; most viral videos use them.
Viral Content: A small share of videos goes viral, but these drive massive spikes in reach and engagement.
