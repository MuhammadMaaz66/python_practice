# 🛳️ Titanic - Machine Learning from Disaster

This repository contains my solution to the **Titanic: Machine Learning from Disaster** competition on Kaggle. The goal is to build a predictive model that determines whether a passenger survived the Titanic shipwreck based on features such as age, sex, class, and fare.

---

## 📌 Competition Link
🔗 [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic)

---

## 🎯 Objective

Predict survival on the Titanic using passenger data (`train.csv`) and submit predictions (`test.csv`) in the required format.

- **Target Variable**: `Survived` (0 = No, 1 = Yes)  
- **Metric**: Accuracy (percentage of correct predictions)

---

## 🗂️ Dataset Description

| File                    | Description                                                       |
|-------------------------|-------------------------------------------------------------------|
| `train.csv`             | 891 samples with features and survival label                      |
| `test.csv`              | 418 samples with features; survival label to predict              |
| `gender_submission.csv` | Baseline submission assuming all female passengers survived       |

### Key Features

| Feature    | Description                                                  |
|------------|--------------------------------------------------------------|
| `Pclass`   | Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)                   |
| `Sex`      | Gender (male/female)                                         |
| `Age`      | Age in years                                                 |
| `SibSp`    | Number of siblings/spouses aboard the Titanic                |
| `Parch`    | Number of parents/children aboard the Titanic                |
| `Fare`     | Ticket fare                                                  |
| `Embarked` | Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

---

## 🧪 Approach

### 🔧 Data Preprocessing
- Imputed missing values:
  - `Age`: median
  - `Fare`: median (in test set)
  - `Embarked`: most frequent
- Applied label encoding for:
  - `Sex`
  - `Embarked`

### 📊 Feature Selection
Selected features:
- `Pclass`
- `Sex`
- `Age`
- `SibSp`
- `Parch`
- `Fare`
- `Embarked`

### 🤖 Model
- **Random Forest Classifier** from `scikit-learn`
- Used default hyperparameters
- Trained on the training set and predicted on the test set

### 📤 Submission Format
CSV file containing:
PassengerId,Survived
892,0
893,1
894,0
...


---

## 📈 Result

- ✅ **Public Score on Kaggle**: `0.75119` (75.12%)
- Solid baseline performance without advanced feature engineering or tuning
📘 [View Full Kaggle Notebook](https://www.kaggle.com/code/muhammadmaaz66/baseline-prediction-model-titanic)


---

## 🧰 Tech Stack

- Python  
- pandas  
- scikit-learn  
- Jupyter Notebook / Kaggle Notebooks  

---

## 🚀 Next Steps

- [ ] Feature engineering (e.g., extract `Title` from `Name`, create `FamilySize`)
- [ ] Try other models (e.g., Logistic Regression, XGBoost)
- [ ] Perform hyperparameter tuning (GridSearchCV or RandomizedSearchCV)
- [ ] Use ensemble models (VotingClassifier, stacking)

---

## 📁 Files

| File                         | Description                                                  |
|------------------------------|--------------------------------------------------------------|
| `titanic_baseline_model.ipynb` | Jupyter Notebook with preprocessing, training, and submission |
| `submission.csv`             | Prediction CSV for Kaggle submission                         |
| `README.md`                  | This documentation file                                      |

---

## 🤝 Acknowledgements

Thanks to Kaggle and the Titanic competition team for this classic beginner-friendly machine learning challenge.
