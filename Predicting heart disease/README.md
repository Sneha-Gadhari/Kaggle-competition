Heart Disease Prediction 

Objective
The objective of this project is to predict the probability of heart disease presence using structured tabular clinical data. This is a binary classification problem.

Evaluation metrics:
Log Loss (academic requirement)
ROC-AUC (competition ranking metric)

Dataset Overview
Training samples: 630,000
Test samples: 270,000
Features: 13 numerical features
Target column: Heart Disease
Absence → 0
Presence → 1
All features are numerical (int64 / float64). No categorical encoding was required.

Preprocessing
Converted target labels:
Absence → 0
Presence → 1
Verified:
No missing values
Proper class distribution
Applied:
Stratified 5-Fold Cross Validation
No scaling required (tree-based models)

Cross-Validation Strategy
StratifiedKFold
n_splits = 5
shuffle = True
random_state = 42
Stratification ensures each fold maintains the same class distribution.

Models Implemented and Submitted
1. XGBoost
Gradient boosting framework optimized for performance and efficiency.
2. LightGBM
Highly efficient gradient boosting model suitable for large tabular datasets.
3. CatBoost
Gradient boosting model with strong regularization and stable performance.

Cross-Validation Results
Model	CV Log Loss	CV ROC-AUC
XGBoost	0.2681	0.9553
LightGBM	0.2686	0.9552
CatBoost	(Add your score here)	(Add your score here)

Observation:
All three boosting models perform very closely. XGBoost achieved the best overall CV performance in this experiment.
Evaluation Metrics Explained
Log Loss
Measures how well predicted probabilities match true labels. Lower is better.
ROC-AUC
Measures the model’s ability to distinguish between classes. Higher is better.

ROC Curve Analysis
Separate ROC curves were plotted for:
XGBoost
LightGBM
CatBoost
The curves show strong separation between positive and negative classes across all models.

Submission Files
Submission files were generated separately for:
XGBoost
LightGBM
CatBoost
Each file contains:
id
Heart Disease (predicted probability)

Conclusion
Gradient boosting models perform strongly on structured tabular data.
Proper cross-validation ensures reliable performance estimation.
XGBoost currently provides the best cross-validation performance.
Multiple models were trained and compared before final submission.
