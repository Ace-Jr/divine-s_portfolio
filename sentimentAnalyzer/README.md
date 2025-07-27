# Review Sentiment Analyzer

This project is a comprehensive data analysis and Natural Language Processing (NLP) solution designed to help an e-commerce clothing business understand its customers' voice. By programmatically analyzing thousands of text reviews, we can move beyond simple star ratings to uncover specific drivers of customer satisfaction and dissatisfaction. The goal is to provide actionable insights that can be used to improve product quality, reduce returns, and enhance marketing efforts.

## Business Questions Addressed:
- What is the overall sentiment distribution (Positive, Negative, Neutral) across all products?
- Which product departments or classes receive the most negative feedback?
- What specific keywords (e.g., "sizing," "fabric," "color") are most frequently associated with positive vs. negative reviews?
- Can we identify specific products that are strong candidates for promotion or discontinuation based on sentiment?

## Dataset
Women's Clothing E-Commerce Reviews.

Source: [Kaggle](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews)

## Tools
- Python (Pandas, TextBlob, Matplotlib)
- Jupyter Notebooks
- GitHub

## Project Pipeline:
- Data Cleaning & Preprocessing: Loaded the CSV dataset using Pandas; handled missing values and prepared review text for analysis (e.g., lowercasing, removing punctuation).
- Sentiment Analysis: Applied the VADER (or TextBlob) sentiment analyzer to each review to generate a compound sentiment score. Classified reviews into 'Positive', 'Negative', and 'Neutral' categories based on this score.
- Exploratory Data Analysis (EDA): Combined sentiment scores by product category and department are used to identify high- and low-performing sectors.
- Insight Generation: Created word clouds and frequency distributions for positive and negative review keywords to diagnose specific issues.

## Insights & Recommendations:
- Investigate the "Top" Department: The "Trend" department shows a significantly higher proportion of negative reviews (15.5%) compared to other departments like "Dresses" (8.5%) and "Tops" (9.7%). The business should prioritize investigating the root causes of this dissatisfaction. This could involve analyzing product quality, sizing inconsistencies, or misleading product descriptions specific to this department.
- Leverage Positive Feedback for Marketing: With over 81% of reviews classified as positive, the marketing team has a rich source of user-generated content. Make use of words like "love", "perfect fit", "flattering" and "great" in their social media posts, email campaings and provide descroptions to attract and reassure customers.
- Conduct a Deep Dive into "Dresses":
Examine sales and return statistics for particular dress styles. Identify which dresses are consistently praised for their fit and style and promote them. Meanwhile, discontinue or investigate dresses that are frequently reviewed as "small", "short" or made of poor "fabric".
