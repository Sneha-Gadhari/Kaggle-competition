# Binary Classification with a Bank Dataset
This repository contains my solution for the **Binary Classification with a Bank Dataset** competition.  
The objective is to predict a binary target variable using customer-related features and achieve high leaderboard accuracy.

## Problem Overview
- Binary classification problem
- Imbalanced dataset
- Evaluation based on leaderboard accuracy
- Test dataset labels are hidden
- Predictions submitted as CSV files

## Approach
- Handled missing values for numerical and categorical features
- Encoded categorical variables appropriately
- Trained models on the complete training dataset (competition-style approach)
- Generated separate submission files for each model
- Compared models using leaderboard scores

## Models and Leaderboard Accuracy
Logistic Regression : 0.69431  
Random Forest : 0.77041  
Random Forest (Tuned) : 0.80787  
Extra Trees : 0.71763  
XGBoost : 0.81319  
XGBoost (Balanced) : 0.90463  
LightGBM : 0.90671  
CatBoost : 0.81387  
Stacked Ensemble : 0.87873

## Observations
- Traditional models like Logistic Regression perform poorly on imbalanced data
- Tree-based ensemble models significantly improve performance
- Gradient boosting methods outperform bagging-based models
- LightGBM achieved the highest leaderboard accuracy among all tested models
- Simple stacking did not outperform the best single boosting model

## Conclusion
LightGBM proved to be the most effective model for this dataset, demonstrating the importance of advanced gradient boosting techniques for large, imbalanced tabular data. Careful preprocessing and model selection played a crucial role in achieving competitive leaderboard performance.
