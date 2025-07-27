# Review Sentiment Analyzer

This project is a full data analysis and Natural Language Processing (NLP) solution designed to help an e-commerce clothing business understand the voice of its customers. By programmatically analyzing thousands of text reviews, we can move beyond simple star ratings to uncover specific drivers of customer satisfaction and dissatisfaction. The goal is to provide actionable insights that can be used to improve product quality, reduce returns, and enhance marketing efforts.

## Businnes Questions Addresed:
- What is the overall sentiment distribution (Positive, Negative, Neutral) across all products?
- Which product departments or classes receive the most negative feedback?
- What specific keywords (e.g., "sizing," "fabric," "color") are most frequently associated with positive vs. negative reviews?
- Can we identify specific products that are strong candidates for promotion or discontinuation based on sentiment?
## Goal
To explore customer sentiment and derive product-level quality scores from text reviews.

## Dataset
Women's Clothing E-Commerce Reviews
Source: [Kaggle](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews)

## Tools
- Python (Pandas, TextBlob, Matplotlib)
- Jupyter Notebooks
- GitHub

## Project Structure
- Data Cleaning & Preprocessing: Loaded the CSV dataset using Pandas; handled missing values and prepared review text for analysis (e.g., lowercasing, removing punctuation).
- Sentiment Analysis: Applied the VADER (or TextBlob) sentiment analyzer to each review to generate a compound sentiment score. Classified reviews into 'Positive', 'Negative', and 'Neutral' categories based on this score.
- Exploratory Data Analysis (EDA): Combined sentiment scores by product category and department are used to identify high- and low-performing sectors.
- Insight Generation: Created word clouds and frequency distributions for positive and negative review keywords to diagnose specific issues like sizing, fabric quality, or style.

## Insights & Recommendations

