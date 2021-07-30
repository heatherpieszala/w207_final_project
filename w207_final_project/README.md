w207_final_project
==============================

## Predicting Stock Market Impact Using Sentiment Analysis

The goal of this project was to perform sentiment analysis on Twitter data and use that to predict stock market prices. We started with a concept to predict which bucket of monetary change a stock would fall into based on its sentiment classification. After trying linear regression, and due to our time constraint, we decided to divert to predicting whether or not the market, or a stock, would go up or down, using that day's sentiment as a feature.

Three primary sentiment analyzers were used to assess the data:
1) VADAR Sentiment Intensity Analyzer - part of the nltk package in python
2) Flair
3) Text Blob

It was determined that VADAR and Text Blob were most similar, with VADAR generalizing best to Twitter data.  Flair was ruled unsufficient due to the extreme level of prcessing time required, and also because the data was not trained in a manner that generalizes well to tweets. 

We then derived additional fetures from Twitter, general Stock Market, and S&P 500 datasets, leveraging sentiment classification, to be used in machine learning models.

The primary models selected were Logistic Regression and Decision Trees.  The models are applied to a batch of data for combined companies 'AAPL', 'AMZN', 'TSLA', 'MSFT', 'GOOG', 'GOOGL', as well as to each individual company.

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
