# Project 3: Web APIs & NLP

Project 3 done by - **Anand Ramchandani**

## Problem Statement  
Collect posts from 2 subreddits and use NLP to train a classifier to distinguish between posts from the subreddits 'r/beer' and 'r/wine

## Contents
- [Background](#Background)
- [Plan to achieve project goals](#Plan-to-achieve-project-goals)
- [Data Gathering from Subreddits](#Data-Gathering-from-Subreddits)
- [Data Import & Cleaning](#Data-Import-and-Cleaning)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Tokenization and Lemmatization](#Tokenization-and-Lemmatization)
- [Word Cloud](#Word-Cloud)
- [Data Modelling](#Data-Modelling)
- [Model Evaluation](#Model-Evaluation)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Background
- The goal is to select 2 subreddits from American social news aggregation, content rating, and discussion website Reddit. Then train a machine learning model that will classify and distinguish newer posts into its respective subreddit accurately    
- For this project we have selected subreddits r/beer and r/wine. These were chosen as they are similar enough being popular alcoholic beverages with lower alcohol content than hard liquor, hence more widely and recreationally consumed so as to provide a large popular following on Reddit. Plus, these 2 subreddits are differentiated enough to train a machine learning model  

## Plan to achieve project goals
1. Gather data using Reddit's API  
2. Clean Data   
3. Data Exploration  
4. Identify relevant features and conduct feature engineering
5. Vectorize the words using CountVectorizer and TF-IDF
6. Modelling using Linear Regression and Multinomial Naive Bayes
7. Refinements and Hyper Parmeter Tuning
8. Revaluate and select best model
9. Evaluate on new test data

## Data Collection
- Downloaded user posts and comments using  pushshift.io Reddit API
- Identified urls
- Called API
- Converted API output to .json

## Data Cleaning
- Check for duplicates and remove them
- Check for null values
- Merge columns to 1 working column
- Make text lowercase
- Remove HTML special entities
- Remove Hyperlinks
- Remove Punctuation
- Split 's, 't, ‘ve
- Remove whitespace
- Remove characters beyond Basic Multilingual Plane (BMP) of Unicode
- Removal of Stop Words

## Pre-Modelling Processing
- Tokenization and Lemmatization
- Word Cloud

## Modelling 
1. Conduct GridSearch CV (pipe vectorizer with model chosen)
2. Evaluate accuracy score and prediction on test data set
3. Re-evaluate after Hyperparameter Tuning
4. Draw Confusion Matrix
5. Calculate Sensitivity, Specificity, Precision
6. Draw ROC curve
7. Make evaluation of which model is best

## Conclusions
- CountVectorizer with Logistic Regression chosen as most apt model for our classification purposes
- Key words between the 2 subreddits help immensely in message classification
- Differences outweigh similarities
- Can be a useful tool to aid marketing or strategy
- Model works well but will fail if message is too general 

## Recommendations
- Improve removal of noise words
- Try more models to see if any provide greater accuracy
- Collect more training data
- Can do more data cleaning (e.g. increase number of stop words)
- Better Gridsearching methods to optimise model selection
- If a new beer or wine nomenclature comes out accuracy could be affected in the future hence model may not be as accurate in long run
- We could test this model on similar alcohol reddits like whiskey, gin, vodka etc