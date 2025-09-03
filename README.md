# You-tube-videos-Data-Analysis
**Objectives:** 

The objective of this project is to perform an end-to-end analysis of YouTube video data (17,590 rows) using Python, ensuring data accuracy, integrity, and consistency through data cleaning, feature engineering, exploratory data analysis (EDA), and visualization.
The analysis focuses on deriving key performance indicators (KPIs) and generating actionable business insights by addressing critical questions, including:

Which video categories receive the highest engagement and views?

How do video duration and resolution influence engagement metrics?

Which categories are consistently high-performing or underperforming?

Do hashtags improve video performance, and which hashtags are most linked to viral videos?

The ultimate goal is to transform raw YouTube metadata into a cleaned, structured, and insight-rich dataset, enabling content creators, marketers, and platform stakeholders to make data-driven decisions.

**Dataset:**

- <a href="https://github.com/NTMASKOSTALIN/You-tube-videos-Data-Analysis/blob/main/youtube_data.csv"> You tube videos dataset
- <a href="https://github.com/NTMASKOSTALIN/You-tube-videos-Data-Analysis/blob/main/cleaned_youtube_dataset.csv"> Cleaned You tube videos dataset
- <a href="https://github.com/NTMASKOSTALIN/You-tube-videos-Data-Analysis/blob/main/You%20tube%20videos%20project%20-%20Jupyter%20Notebook.pdf"> You tube video dataset Project 


**KPI/Questions:**
1. Identify which video categories (e.g., Gaming, Comedy, News) receive the highest engagement in terms of views, likes, and comments.
2. Evaluate whether video duration or resolution influences engagement metrics.
3. Explore whether video popularity can be predicted using metadata features.
4. Assess whether videos with hashtags perform better than those without in terms of views, likes, and engagement rate.
5. Discover which hashtags are most frequently associated with viral videos and how they contribute to content success.

**Process:**

**1. Define Objective**
   
Frame business-driven questions around content performance, engagement predictors, and hashtag effectiveness.

**2. Data Collection**
   
Source: YouTube Dataset from Kaggle (17,590 rows, CSV format).
Imported into Python for exploration and analysis.

**3. Data Cleaning & Preparation**

Removed irrelevant columns (url, description).
Handled missing values (e.g., replaced empty hashtags with "No Hashtags").
Checked and removed duplicates.
Standardized categories and fixed inconsistencies.
Performed sanity checks (no negative/invalid values for views, likes, comments, duration).
Outlier detection and treatment: applied log transformations for skewed metrics.

**4. Feature Engineering**

Created new fields:
engagement_rate = (likes + comments) / views,
duration_category (Short, Medium, Long, Very Long),
resolution (mapped from video height/width),
has_hashtags (binary flag),
is_viral (top 5% videos by views).

**5. Exploratory Data Analysis (EDA)**

Univariate Analysis: Histograms, boxplots, countplots for numeric & categorical features.
Bivariate Analysis: Scatterplots, heatmaps, grouped averages (views/engagement by category, duration, resolution).
Segmentation: Comparison across hashtags, categories, and viral vs non-viral videos.
Correlation Analysis: Identified relationships among numeric features.

**6. Data Visualization & Insights**
   
Barplots, scatterplots, and heatmaps tied directly to business questions:
Category-level performance (views, engagement).
Impact of duration & resolution on engagement.
Hashtag effectiveness.
Viral vs non-viral content patterns.

**7. Reporting & Communication**
   
Summarized workflow from objective → data → cleaning → analysis → insights.
Created an Executive Summary with key findings and business recommendations.
Highlighted stakeholders (creators, marketers, YouTube platform, advertisers).

**8. Future Work / Next Steps**
   
Future extensions could include time-based analysis, interactive dashboards, and text analytics on hashtags/titles.

**Dashboard:**

<img width="600" height="593" alt="image" src="https://github.com/user-attachments/assets/ee15e062-47cb-470c-8f7e-b1f973642d77" />
<img width="588" height="593" alt="image" src="https://github.com/user-attachments/assets/795296e8-aecb-498c-9cde-74a516793f0c" />
<img width="579" height="593" alt="image" src="https://github.com/user-attachments/assets/02039cef-0cf0-4ba7-b0d0-473139cfe315" />
<img width="586" height="458" alt="image" src="https://github.com/user-attachments/assets/029d2642-b0d4-45ba-8c30-1a521127f3d9" />
<img width="603" height="458" alt="image" src="https://github.com/user-attachments/assets/52666fc0-162a-4bf4-ac78-1facef3fa995" />
<img width="588" height="529" alt="image" src="https://github.com/user-attachments/assets/17e98dd3-90db-4b4b-b701-3ef0f6475003" />
<img width="566" height="457" alt="image" src="https://github.com/user-attachments/assets/21c4efa4-a49d-4e68-968c-b8fa772e91d6" />
<img width="567" height="457" alt="image" src="https://github.com/user-attachments/assets/58f6939c-19e8-4bc0-9a2d-787d1dd69088" />
<img width="567" height="457" alt="image" src="https://github.com/user-attachments/assets/9288c663-462e-498a-b3ea-104a0246d4d9" />
<img width="737" height="635" alt="image" src="https://github.com/user-attachments/assets/156a5260-e1e7-4659-b775-070a586b4afd" />
<img width="583" height="593" alt="image" src="https://github.com/user-attachments/assets/689fcedd-f682-4213-8069-25e132e4f8ea" />
<img width="583" height="529" alt="image" src="https://github.com/user-attachments/assets/515e0a00-0c84-4f14-b465-2a18a73b5062" />
<img width="592" height="458" alt="image" src="https://github.com/user-attachments/assets/a929bb5c-ebb1-4c6d-9485-d071b91e28cd" />
<img width="600" height="458" alt="image" src="https://github.com/user-attachments/assets/70240a18-5c33-410c-96cf-fd0429046ae1" />
<img width="588" height="458" alt="image" src="https://github.com/user-attachments/assets/abd6a752-d9b1-470a-89c8-4becb645418d" />
<img width="592" height="457" alt="image" src="https://github.com/user-attachments/assets/fc574d4e-6ad8-4f24-a710-dc51ec75ec41" />
<img width="595" height="437" alt="image" src="https://github.com/user-attachments/assets/4b71f774-1f18-4512-9130-97e969bab872" />

**Insights:**

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

**Conclusion:**

This project successfully transformed raw YouTube video data (17,590 rows) into a cleaned, structured, and insight-rich dataset through Python-based exploration, cleaning, feature engineering, and visualization.

The analysis revealed that
Gaming and Comedy dominate in reach, while Education excels in engagement.
Medium-length videos (4–10 minutes) drive the strongest engagement.
Hashtags significantly enhance performance and are common in viral content.
Likes and Comments are the most reliable predictors of video popularity.
These findings provide actionable guidance for content creators, marketers, platform managers, and advertisers to optimize strategies around content categories, duration, resolution, and hashtag usage.
Overall, the project demonstrates how structured data analysis can convert raw metadata into business intelligence that supports data-driven decision-making.
