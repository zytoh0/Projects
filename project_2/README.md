# README: Predicting House Prices with Linear Regression
#### Author: Zhi Yuan Toh

## Problem Statement
After my first two data science projects solving classification problems, I am looking to expand my skill set by doing a comprehensive regression project. While taking Data Science micro-courses on Kaggle, I came across the House Prices: Advanced Regression Techniques competition. With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges me to predict the final price of each home.

The Ames Housing dataset was compiled by Dean De Cock for use in data science education. The data set describing the sale of individual residential property in Ames, Iowa from 2006 to 2010. The data set contains 2930 observations and a large number of explanatory variables (23 nominal, 23 ordinal, 14 discrete, and 20 continuous) involved in assessing home values.

First, I performed comprehensive exploratory data analysis to understand linear relationships among the most important variables and detect potential issues such as sknewness, outliers and missing values. Then, I handled these issues, cleansed the data and performed feature engineering. Lastly, I built machine learning models to predict house prices. By the time I write this notebook, my best model has Mean Absolute Error of 12293.919, ranking 95/15502, approximately top 0.6% in the Kaggle leaderboard.

**Problem Statement:** We are a team of data analyst working for Livable that is in the home flipping business. Our team’s goal is to use housing data collected between 2006 to 2010 to build a machine learning model that best predicts the potential sale price for properties located in Ames, Iowa.

## Executive Summary
The Ames Housing Dataset was first described in 2011 by Dean De Cock [(4)](http://jse.amstat.org/v19n3/decock.pdf). This dataset provides 80 features (of nominal, discrete, and ordinal types) to describe properties in Ames, Iowa that were sold between the years 2006-2010. During the first step in the workflow (data cleaning), missing values were fixed to the best of my abilities, correct data types were confirmed, and any unsual values were investigated. Once the data was cleaned, Exploratory Data Analysis (EDA) was conducted to explore the relationship between Sale Price and each feature in the model. For numeric features, the linear relationship was examined using a heatmap and correlation coefficients. For categorical data, bar plots were created to visualize the mean Sale Price across categories. During EDA for categorical features, special attention was paid to any patterns or clusters in Sale Prices that emerged. 

Following EDA, features were engineered to reduce dimensionality of the data and to account for the patterns and clusters that emerged during EDA. If a categorical variable was coded during feature engineering, it was removed from the data frame. Any categorical variables of interest were dummified. Data was divided into training sets (80% of data) and testing sets (20% of data) to prepare for modeling. (NOTE: For this project several models were created, including Ridge Regression, Lasso Regression, and Linear Regression. For the regression models with regularization techniques, dummy variables were created for all categorical variables that had not yet been coded. For the final Linear Regression, dummy variables were hand-selected based on EDA and the Lasso Regression. Because different sets of dummy variables were included in the models, there are two sets of data.)

During modeling, five models were built: Null Model, a Linear Regression with 337 features, Ridge Regression with 337 features, Lasso Regression with 20 features, and Linear Regression with 47 features. It is important to note that all of the features included in the final Linear Regression Model were determined to be important based on EDA or the Lasso regression. The models were compared based on R2 score, and the highest scoring model was selected for further evaluation using RMSE and residuals plots. 

Interpretations and recommendations were made based off of the best-performing model. 

## Table of Contents
1. [Project Files](#./datasets)
2. [Data Dictionary](#Data-Dictionary)
2. [Model Selection](#Model-Selection)
3. [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Data Dictionary
A link to the data dictionary can be found [here](https://www.kaggle.com/zhiyuantoh/dataset). 

## Model Selection
As previously mentioned, four models were created for this project. 

Model Name | Training Score | Testing Score
-|-
Baseline/Null Model|0%
Linear Regression |94.6%
Ridge|92.1%
LASSO|92.1%
ElasticNet|92.1%

## Conclusions and Recommendations

In this project, I have conducted a detailed EDA to understand the data and important features. Based on exploratory analysis, I performed data preprocessing and feature engineering. Finally, I train regularized regression models (Ridge, Lasso), and take average predictions from these models to predict final price of each house. By the time I write this notebook, my best model has Mean Absolute Error of 12293.919, ranking 95/15502, approximately top 0.6% in the Kaggle leaderboard.

Among the 4 models, the ElasticNet model performed the best and was able to explain about 92% of variance in sales prices on the train data and produced the lowest RMSE of 0.116 on both the train and test data. Hence, our team recommends ElasticNet model to predict the sale price due to the normality of distribution.

However, since we used the 2006 to 2010 dataset to build the model and the real estate market is constantly changing, our best model might not fit the current market. Going forward, we would recommend frequently recording housing specs and sales prices in the Ames area and maintaining a database with the relevant information to continually improve on the model’s ability to predict sales price, even in the face of an ever-changing market landscape.

I hope to continue making improvements to this model to help automate the property appraisal process.

## References
1. [Population of Ames Iowa](https://datausa.io/profile/geo/ames-ia/)
2. [City of Ames Website](https://www.cityofames.org/about-ames/about-ames)
3. [Machine Learning in Real Estate](https://unionstreetmedia.com/the-rise-of-machine-learning-in-real-estate/#:~:text=Personalized%20Marketing%20Automation%20%E2%80%93%20machine%20learning,neighborhood%20and%20property%20is%20best)
4. [Ames Housing Data - Original Article](http://jse.amstat.org/v19n3/decock.pdf)
