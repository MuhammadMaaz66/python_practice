🛳️ Titanic - Machine Learning from Disaster
This repository contains my solution to the Titanic: Machine Learning from Disaster competition on Kaggle. The goal is to build a predictive model that determines whether a passenger survived the Titanic shipwreck based on features such as age, sex, class, and fare.

📌 Competition Link
Kaggle Titanic Competition

🎯 Objective
Predict survival on the Titanic using passenger data (train.csv) and submit predictions (test.csv) in the required format.

Target Variable: Survived (0 = No, 1 = Yes)

Metric: Accuracy (percentage of correct predictions)

🗂️ Dataset Description
train.csv: 891 samples with features and survival label.

test.csv: 418 samples with features, label to predict.

gender_submission.csv: Baseline submission (assumes all females survived).

Key Features:

Feature	Description
Pclass	Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)
Sex	Gender (male/female)
Age	Age in years
SibSp	Number of siblings/spouses aboard
Parch	Number of parents/children aboard
Fare	Ticket fare
Embarked	Port of Embarkation (C, Q, S)

🧪 Approach
Data Preprocessing

Missing value imputation:

Age: median

Fare: median (test set)

Embarked: most frequent

Label Encoding for Sex and Embarked.

Feature Selection

Selected features: Pclass, Sex, Age, SibSp, Parch, Fare, Embarked.

Model

Random Forest Classifier with default hyperparameters.

Trained on the training set and predicted on the test set.

Submission

Predictions exported to a CSV with format:

python-repl
Copy
Edit
PassengerId,Survived
892,0
893,1
...
📈 Result
Public Score on Kaggle: 0.75119 (75.12%)

This baseline model performs better than the gender-based baseline (~0.76588) with no advanced tuning or feature engineering.

🧰 Tech Stack
Python

pandas

scikit-learn

Jupyter Notebook / Kaggle Notebooks

🚀 Next Steps
Feature engineering (e.g., Title from Name, Family Size)

Hyperparameter tuning

Try other models like XGBoost or Logistic Regression

Ensemble methods

📁 Files
File	Description
titanic_baseline_model.ipynb	Full notebook with preprocessing, training, and submission steps
submission.csv	Generated predictions file
README.md	This documentation file

🤝 Acknowledgements
Thanks to Kaggle and the Titanic competition team for providing this classic beginner-friendly machine learning challenge.