# Danish Property Price Prediction Project
This repository contains the code and data used for a machine learning project focused on predicting property prices in Denmark. This project was conducted as part of a machine learning competition, which I won using an XGBoost model. The project demonstrates advanced feature engineering, model selection, and performance optimization techniques.

# Project Overview
In this competition, contestants aimed to improve upon the Danish Property Assessment Authority's property price valuations. The dataset consists 150,000 rows of detailed property characteristics and market data, which was used to develop a highly accurate model for price prediction. My final solution achieved first place among 17 participants, including data scientists, machine learning engineers, and software developers. The competition was hosted by Resights and the prize was a bottle of fine gin.

# Key Components
Feature Engineering: Extensive feature engineering was performed to enhance predictive power. Key engineered features include:

Categorical transformations for MUNICIPALITY_CODE and other categorical features.

Sine-cosine transformations and other manipulations of time-related features.

Geospatial features like latitude, longitude, and distances to nearby landmarks.

Data Preprocessing: Handling of class imbalances, missing values, and mixed data types.

Model Selection and Tuning: XGBoost was selected as the final model based on its performance in cross-validation, outperforming other algorithms tested. These other algorithms include Random Forest, Linear Regression and Deep Learning algorithms using neural networks. Parameters were optimized to maximize accuracy.

# Dataset
The dataset used in this project contains approximately 150,000 records with various attributes related to property features and geographical data. Key features include:

Geographical attributes: LAT, LNG, DISTANCE_LAKE, DISTANCE_HARBOUR, DISTANCE_COAST

Property details: AREA_RESIDENTIAL, AREA_OTHER, CONSTRUCTION_YEAR, REBUILDING_YEAR

Price-related features: MUNICIPALITY_MEAN_SQM_PRICE, STREET_CODE_MEAN_SQM_PRICE

# Model and Approach
My final model used XGBoost with the following key parameters:

max_depth: 10

learning_rate: 0.08

n_estimators: 840

objective: reg

subsample: 0.8

colsample_bytree: 0.8

Log Transformation on Target Variable: A log transformation was applied to the target variable, PRICE, which improved the model's stability and prediction accuracy.

# Files
boligpriser.ipynb: The main Jupyter Notebook containing data processing, feature engineering, and model training code. The version of the notebook here on Github contains all of the code used for the final model as well as code for experimenting with a handful of other models.

README.md: Project documentation.

# Results and Evaluation
The final model was evaluated on a test dataset split chronologically, with training data taken before June 2024 and test data from after June 2024. The model performed significantly well on unseen data, demonstrating robust predictive capabilities for real-world applications.

# What I Learned
This project was a great exercise in combining my skills in optimization, statistics, ML and data engineering to produce a high-performing model.
