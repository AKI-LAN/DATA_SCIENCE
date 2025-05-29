# 🛳️ Titanic Survival Prediction

## 📌 Problem Statement
Predict whether a passenger survived the Titanic shipwreck using features such as age, gender, ticket class, and more.

## 📂 Dataset
- **Source**: [Kaggle Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic/data)
- **Files**:
  - `train.csv` – Training data with labels
  - `test.csv` – Test data for submission

## 🧪 Approach
- Exploratory Data Analysis (EDA)
- Data Cleaning & Preprocessing
- Feature Encoding
- Model Building using Logistic Regression
- Evaluation using Accuracy and Classification Report

## 📊 EDA Highlights
- Survival rate by gender showed women were more likely to survive.
- Younger passengers and higher-class passengers had a higher chance of survival.
- 'Cabin' had too many missing values and was dropped.

## 🔧 Data Preprocessing
- Filled missing `Age` with median.
- Filled missing `Embarked` with mode.
- Dropped `Cabin`, `Ticket`, and `Name`.
- Label encoded `Sex` and `Embarked`.

## 🤖 Model
**Logistic Regression** (baseline model):
```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression(max_iter=200)
model.fit(X_train, y_train)
