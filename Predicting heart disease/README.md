# Heart Disease Prediction
Binary classification project for predicting heart disease using structured tabular data.

## Overview
This project was developed for the Kaggle Playground Series Season 6 Episode 2 competition.
The goal is to predict the probability of heart disease using 13 numerical clinical features.
- Train samples: 630,000
- Test samples: 270,000
- Features: 13 
- Target: Heart Disease (0 = Absence, 1 = Presence)

## Exploratory Data Analysis
- Checked data types and dataset shape
- Verified no missing values
- Analyzed target distribution
- Visualized class balance
The dataset is moderately balanced.

## Validation Strategy
Stratified 5-Fold Cross Validation was used to maintain class distribution across folds.
- n_splits = 5
- shuffle = True
- random_state = 42
Out-of-fold (OOF) predictions were generated to compute unbiased Log Loss and ROC-AUC.

## Models Implemented
Logistic Regression (Baseline)
Used as a linear baseline model.
XGBoost
- 800 estimators
- learning_rate = 0.05
- max_depth = 5
- subsample = 0.8
- colsample_bytree = 0.8
LightGBM
- 800 estimators
- learning_rate = 0.05
- num_leaves = 31
- subsample = 0.8
- colsample_bytree = 0.8
CatBoost
- 800 iterations
- learning_rate = 0.05
- depth = 6
- loss_function = Logloss
All boosting models used 5-fold averaging for final test predictions.

## Cross-Validation Results
Model	              CV Log Loss	     CV ROC-AUC
Logistic Regression	0.2818	         0.9505
XGBoost	            0.2681	         0.9553
LightGBM	          0.2686	         0.9552
CatBoost	          0.2677	         0.9554

## Kaggle Leaderboard (ROC-AUC)
Model	     Public Score
XGBoost	   0.95349
LightGBM	 0.95339
CatBoost	 0.95353
CatBoost achieved the best public leaderboard score.

## Visualizations
- Combined ROC Curve comparison
- Individual ROC curves for each model

## Submission Files
- submission_xgb.csv
- submission_lgb.csv
- submission_cat.csv
Each submission contains:
- id
- Predicted probability of heart disease

## Key Takeaways
- Gradient boosting models outperform linear models on structured tabular data.
- Proper cross-validation is essential for reliable performance estimation.
- All three boosting models perform very closely.
- CatBoost provided the best leaderboard result in this experiment.
