Objectives: 

The objective of this project is to perform an end-to-end analysis of YouTube video data (17,590 rows) using Python, ensuring data accuracy, integrity, and consistency through data cleaning, feature engineering, exploratory data analysis (EDA), and visualization.
The analysis focuses on deriving key performance indicators (KPIs) and generating actionable business insights by addressing critical questions, including:

Which video categories receive the highest engagement and views?

How do video duration and resolution influence engagement metrics?

Which categories are consistently high-performing or underperforming?

Do hashtags improve video performance, and which hashtags are most linked to viral videos?

The ultimate goal is to transform raw YouTube metadata into a cleaned, structured, and insight-rich dataset, enabling content creators, marketers, and platform stakeholders to make data-driven decisions.

Dataset:

- <a href="https://github.com/NTMASKOSTALIN/You-tube-videos-Data-Analysis/blob/main/youtube_data.csv"> You tube videos dataset
- <a href="https://github.com/NTMASKOSTALIN/You-tube-videos-Data-Analysis/blob/main/cleaned_youtube_dataset.csv"> Cleaned You tube videos dataset
- <a href="https://github.com/NTMASKOSTALIN/You-tube-videos-Data-Analysis/blob/main/You%20tube%20videos%20project%20-%20Jupyter%20Notebook.pdf"> You tube video dataset Project 


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
engagement_rate = (likes + comments) / views,
duration_category (Short, Medium, Long, Very Long),
resolution (mapped from video height/width),
has_hashtags (binary flag),
is_viral (top 5% videos by views).

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

Insights:

Content Categories:
Gaming and Comedy videos dominate in views, while Education videos achieve higher engagement rates.
Some categories (e.g., News, People & Blogs) show underperformance in both reach and engagement.

Video Duration
Medium-length videos (4–10 minutes) strike the best balance of views and engagement.
Very short or very long videos tend to underperform compared to medium-length content.

Resolution
Higher resolutions (720p, 1080p) yield slightly better engagement than lower resolutions (240p, 360p).
Extremely high resolutions (4K) are rare and not significantly different in engagement.

Engagement Predictors
Likes and Comments are strongly correlated with Views → best predictors of video popularity.
Duration shows weak correlation with views or engagement beyond the medium-length optimization.
Bitrate and frame rate have negligible impact on engagement.

Hashtag Effectiveness
Videos with hashtags consistently achieve higher views and engagement rates compared to those without.
Most viral videos include hashtags, and certain trending hashtags are strongly linked to viral content.

Viral vs Non-Viral
Viral videos (~5% of dataset) achieve exponentially higher reach compared to the rest.
They cluster in categories like Gaming and Entertainment, and frequently leverage hashtags.

Conclusion:

This project successfully transformed raw YouTube video data (17,590 rows) into a cleaned, structured, and insight-rich dataset through Python-based exploration, cleaning, feature engineering, and visualization.

The analysis revealed that
Gaming and Comedy dominate in reach, while Education excels in engagement.
Medium-length videos (4–10 minutes) drive the strongest engagement.
Hashtags significantly enhance performance and are common in viral content.
Likes and Comments are the most reliable predictors of video popularity.
These findings provide actionable guidance for content creators, marketers, platform managers, and advertisers to optimize strategies around content categories, duration, resolution, and hashtag usage.
Overall, the project demonstrates how structured data analysis can convert raw metadata into business intelligence that supports data-driven decision-making.
