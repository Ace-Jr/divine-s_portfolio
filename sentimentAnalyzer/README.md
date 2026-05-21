# Review Sentiment Analyzer
NLP pipeline that classifies 23,000+ women's clothing reviews as Positive, Negative, or Neutral. It surfaces which product categories and keywords drive each sentiment. 

***

##Pipeline
+ Cleans and normalizes review text (lowercase, punctuation removal)
+ Scores each review with VADER compound sentiment → labels it Positive / Negative / Neutral
+ Aggregates scores by product department and class to rank best and worst performers
+ Generates keyword word clouds and frequency charts for each sentiment bucket

Dataset: [Women's Clothing E-Commerce Reviews](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews/data) via Kaggle


## Requirements
+ Python
+ Jupyter
+ TextBlob / VADER
+ pandas
+ matplotlib

## Key Findings

> $\color{Bittersweet}{Trend\ department\ has\ 15.5%\ negative\ rate.}$ vs. 8–10% elsewhere, sizing inconsistencies appear as the main driver.

> 81% of reviews are positive. Top keywords: "love", "perfect fit", "flattering", "great".

> Dresses flagged for "small" / "fabric" are strong discontinuation candidates based on recurring negative terms.

> $\color{Red}{Trend\ department\ has\ 15.5\% negative\ rate.} $ vs. 8–10% elsewhere, sizing inconsistencies appear as the main driver.
