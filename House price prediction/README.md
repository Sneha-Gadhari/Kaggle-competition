House Prices - Advanced Regression Techniques

**Overview**
This project applies regression and tree-based machine learning models to predict house prices using the Kaggle House Prices - Advanced Regression Techniques dataset. 

**Objective**
- Implement regression and tree-based models
- Perform data cleaning and feature engineering
- Evaluate models using performance metrics
- Generate a Kaggle submission and analyze results

**Dataset**
Source: Kaggle – House Prices: Advanced Regression Techniques
Link: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques
Files used:
- train.csv
- test.csv
Target variable: SalePrice

**Data Preprocessing**
Checked data structure and missing values
Numerical missing values replaced with median
Categorical missing values replaced with most frequent value
Categorical features encoded using one-hot encoding

**Models Implemented**
- Linear Regression
- Decision Tree Regressor (CART)
- Random Forest Regressor

**Performance Metrics**
Root Mean Squared Error (RMSE)
R² Score

**Model Comparison**
Model	              RMSE	      R² Score
Linear Regression	  51405.09	  0.655
Decision Tree	      45492.37	  0.730
Random Forest	      28352.11	  0.895

**Best Model**
Random Forest Regressor achieved the lowest RMSE and highest R² score and was selected for final prediction and Kaggle submission.


