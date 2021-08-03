# w207_final_project

## Predicting Stock Market Impact Using Sentiment Analysis

The goal of this project was to perform sentiment analysis on Twitter data and use that to predict stock market prices. We started with a concept to predict which bucket of monetary change a stock would fall into based on its sentiment classification. After trying linear regression, and due to our time constraint, we decided to divert to predicting whether or not the market, or a stock, would go up or down, using that day's sentiment as a feature.

Three primary sentiment analyzers were used to assess the data:
1) VADER Sentiment Intensity Analyzer - part of the nltk package in python
2) Flair
3) Text Blob

It was determined that VADER and Text Blob were most similar, with VADER generalizing best to Twitter data.  Flair was ruled unsufficient due to the extreme level of prcessing time required, and also because the data was not trained in a manner that generalizes well to tweets. 

We then derived additional fetures from Twitter, general Stock Market, and S&P 500 datasets, leveraging sentiment classification, to be used in machine learning models.

The primary models selected were Logistic Regression and Decision Trees.  The models are applied to a batch of data for combined companies 'AAPL', 'AMZN', 'TSLA', 'MSFT', 'GOOG', 'GOOGL', as well as to each individual company.
