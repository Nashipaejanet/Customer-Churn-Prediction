# Customer Churn Prediction

Predicting customer churn for a telecom company using the Telco Customer Churn dataset (7,043 customers, 21 features).

## Overview

This project walks through a full churn modeling workflow: exploratory data analysis, handling missing values, visualizing churn drivers, preprocessing, and comparing multiple classification models. A Voting Classifier ensemble was selected as the final model, reaching **81.7% accuracy** on the test set.

## Key findings

- Overall churn rate: 26.6% of customers switched providers.
- Contract type is the strongest churn driver: about 75% of month-to-month customers churned, versus 13% on one-year contracts and 3% on two-year contracts.
- Customers paying by electronic check churned at a higher rate than those on automatic bank or credit card payments.
- Fiber optic internet subscribers had a higher churn rate than DSL subscribers.
- Customers without online security or tech support were more likely to churn.
- New customers (low tenure) and those with higher monthly charges were more likely to churn.

## Models compared

KNN, SVC, Random Forest, Logistic Regression, Decision Tree, AdaBoost, Gradient Boosting, and a Voting Classifier ensemble of the top performers.

| Model | Result |
|---|---|
| Voting Classifier (final) | 81.7% accuracy |

## Data

Dataset: [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (IBM sample dataset, via Kaggle).

The CSV is not included in this repo. Download `WA_Fn-UseC_-Telco-Customer-Churn.csv` from the link above and place it in the project root before running the notebook.

## Setup

```bash
git clone <your-repo-url>
cd customer-churn-prediction
pip install -r requirements.txt
jupyter notebook customer_churn_prediction.ipynb
```

## Project structure

```
.
├── customer_churn_prediction.ipynb   # full analysis and modeling
├── requirements.txt
└── README.md
```

## Tech stack

Python, pandas, NumPy, scikit-learn, XGBoost, CatBoost, Matplotlib, Seaborn, Plotly
