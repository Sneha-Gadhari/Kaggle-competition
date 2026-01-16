Project Overview
This project is based on the famous Titanic - Machine Learning from Disaster Kaggle competition.
The objective is to predict whether a passenger survived the Titanic disaster using passenger data such as class, gender, age, and family information.
The project demonstrates a complete machine learning workflow, including data exploration, preprocessing, feature engineering, model training, and result submission.


Dataset
  The dataset is provided by Kaggle and includes:
  - train.csv – training data with survival labels
  - test.csv – test data without labels
  - Dataset source: Kaggle Titanic Competition


Exploratory Data Analysis (EDA)
  Key observations from the data:
  - Women had a much higher survival rate than men
  - First-class passengers survived more than second and third class
  - Passengers traveling with family had higher survival chances than those traveling alone
  - These insights helped in selecting meaningful features for the model.


Feature Engineering
  The following features were used:
  Pclass – Passenger class
  Sex – Gender (encoded)
  Age – Missing values filled using median
  Fare
  FamilySize – SibSp + Parch + 1
  IsAlone – Binary feature indicating whether a passenger traveled alone
  Categorical features were converted using one-hot encoding.


Model Used
  Random Forest was chosen for its robustness and ability to handle both numerical and categorical features effectively.


Results
  Best Kaggle public leaderboard accuracy achieved: 0.78708
  Increasing the number of trees improved model stability and prediction consistency


Output
  The final predictions are saved in a CSV file in the required Kaggle submission format: PassengerId, Survived


Libraries Used
  Python, NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn


Conclusion
  This project highlights how basic preprocessing, feature engineering, and a well-tuned Random Forest model can achieve strong performance on a classic machine learning problem. It also demonstrates the importance of exploratory data analysis in understanding real-world datasets.
