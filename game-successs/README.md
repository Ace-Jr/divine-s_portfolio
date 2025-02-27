# What Makes a Game Successful?

## Overview
This project explores the factors that drive a video game's commercial success. By analyzing a comprehensive dataset of video game sales, ratings, genres, and prices, we aim to determine which variables most strongly correlate with high sales. Spoiler alert: Not all blockbusters are created equal—sometimes a quirky indie title can outperform a high-budget AAA game.

## Business Question
What key factors (genre, ratings, price, etc.) contribute to a video game’s success, and how can developers leverage these insights to design games that hit the mark?

## Data Sources
- **Kaggle Video Game Sales Dataset:** Contains data on video game titles, sales, genres, platforms, and release years.
- **Supplementary Data:** Publicly available ratings and pricing data from Metacritic and other game review sites.

## Tools & Techniques
- **Data Acquisition:** Download CSV files from Kaggle and scrape supplementary data using Python.
- **Data Preparation:** Use SQL and Pandas for cleaning, merging, and creating new derived metrics.
- **Data Analytics:** Conduct correlation analysis and regression modeling with Python (Scikit-learn, Pandas).
- **Data Visualization:** Build interactive dashboards in Power BI/Tableau to showcase findings.

## Methodology
1. **Data Collection:** Gather sales, rating, and pricing data from Kaggle and public APIs.
2. **Data Cleaning:** Merge datasets, remove duplicates, and fill missing values. Standardize fields and create new metrics (e.g., rating differences).
3. **Analysis:** 
   - Perform correlation analysis to see which factors most affect sales.
   - Run regression models to quantify the impact of variables like genre and price.
   - Identify outlier games that defy conventional trends.
4. **Visualization:** Create interactive charts and dashboards to enable slicing the data by genre, platform, or release year.
5. **Insights:** Summarize key trends and make recommendations for game developers and publishers.

## Key Insights & Recommendations
- **Genre Impact:** Certain genres (e.g., action-adventure or sports) consistently outperform others.
- **Ratings Matter:** Higher critic and user ratings correlate strongly with better sales.
- **Price Sensitivity:** There is an optimal price range where sales peak—too high or too low can hurt performance.
- **Outliers:** Identify niche games that outperform expectations, suggesting hidden market opportunities
