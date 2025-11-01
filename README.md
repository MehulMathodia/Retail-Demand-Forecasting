Retail Sales Demand Forecasting

A project on time series forecasting for retail sales using ARIMA and Prophet.

Project Overview

This project focuses on forecasting daily sales for an individual Rossmann store using time series analysis. The primary goal is to build and evaluate different forecasting models to predict future demand accurately, which is crucial for optimizing inventory and promotions.

Methodology & Features

Data Cleaning: The raw training and store data was merged, cleaned, and preprocessed. The analysis focuses on a single store (Store 1) for a univariate time series forecast, filtering for days the store was open.

Exploratory Data Analysis (EDA): Visualized the sales data over time to identify trends, seasonality, and potential outliers.

Model Implementation: Three different models were built and compared:

ARIMA: A classic statistical model for time series forecasting. Autocorrelation (ACF) and Partial Autocorrelation (PACF) plots were used to guide the choice of model order (p,d,q).

Prophet (Baseline): Facebook's Prophet model was used, incorporating yearly seasonality and holiday effects.

Prophet with Regressor: An enhanced Prophet model that includes external information about store promotions (Promo feature) to improve accuracy.

Evaluation: Models were evaluated on a hold-out test set of 90 days using Root Mean Squared Error (RMSE) and Mean Absolute Percentage Error (MAPE) as the primary metrics.

Key Results

The enhanced Prophet model, which included promotional data as an external regressor, was the top-performing model.

MAPE Improvement: Adding the 'Promo' feature reduced the MAPE from 15.33% to 9.66%, a significant improvement in forecast accuracy.

Final Comparison:

ARIMA(5,1,0): MAPE: 10.20%

Prophet (Original): MAPE: 15.33%

Prophet (+Promo): MAPE: 9.66%

Technologies Used
Python

Pandas

Matplotlib & Seaborn

Statsmodels (for ARIMA)

Prophet (by Facebook)

Jupyter Notebook

How to Run This Project

Prerequisites: Ensure you have Python and the following libraries installed:

pip install pandas matplotlib seaborn statsmodels prophet jupyter


Download the Repository: Clone or download this GitHub repository to your local machine. You should have two main files:

Demand_Forecasting_for_Retail.ipynb

rossmann-store-sales.zip

Unzip the Data: Unzip the rossmann-store-sales.zip file. This will extract the necessary train.csv and store.csv files into the same directory as your notebook.

Launch and Run: Open the Demand_Forecasting_for_Retail.ipynb notebook in Jupyter and run the cells in order. The notebook is configured to read the data files from the local directory.

Data Source
The data used is the "Rossmann Store Sales" dataset from Kaggle, included in this repository as rossmann-store-sales.zip.m0d
