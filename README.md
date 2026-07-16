# XGBoost-Breast-Cancer-Prediction-
Project Overview

This project uses the XGBoost (Extreme Gradient Boosting) machine learning algorithm to classify breast cancer tumors as:

M (Malignant) → Cancerous
B (Benign) → Non-Cancerous

The dataset contains measurements computed from digitized images of breast mass cell nuclei.

Problem Statement

Build a machine learning model that predicts whether a tumor is malignant or benign based on medical measurements.

Dataset Information

Dataset Name

Breast Cancer Wisconsin Diagnostic Dataset

Rows

569

Columns

33

Target Variable

diagnosis

M → Malignant
B → Benign
Removed Columns
id
Unnamed: 32
Technologies Used
Python
Pandas
NumPy
Matplotlib
Scikit-Learn
XGBoost
Machine Learning Workflow
Load Dataset
      ↓
Data Cleaning
      ↓
Feature Selection
      ↓
Train-Test Split
      ↓
XGBoost Model
      ↓
Model Training
      ↓
Prediction
      ↓
Evaluation
      ↓
Feature Importance
Libraries Used
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder
from sklearn.metrics import accuracy_score
from sklearn.metrics import confusion_matrix
from sklearn.metrics import classification_report

from xgboost import XGBClassifier
Data Preprocessing
Removed unnecessary columns
Converted diagnosis into numerical values
Split features and target
Performed Train-Test Split
Model Parameters
XGBClassifier(

n_estimators=300,
learning_rate=0.05,
max_depth=5,
min_child_weight=3,
gamma=0.2,
subsample=0.8,
colsample_bytree=0.8,
reg_alpha=0.5,
reg_lambda=1,
objective='binary:logistic',
booster='gbtree',
tree_method='hist',
eval_metric='logloss',
random_state=42
)
Evaluation Metrics
Accuracy
Confusion Matrix
Precision
Recall
F1 Score
Feature Importance
Project Structure
Breast-Cancer-XGBoost/

│
├── data.csv
├── xgboost_model.py
├── README.md
├── requirements.txt
└── images/
requirements.txt
numpy
pandas
matplotlib
scikit-learn
xgboost
Advantages of XGBoost
Very High Accuracy
Fast Training
Handles Missing Values
Built-in Regularization
Prevents Overfitting
Parallel Processing
Supports Feature Importance
Limitations
Training can be slower than simple models.
Many hyperparameters require tuning.
Less interpretable than Decision Trees.
Future Improvements
Hyperparameter Tuning
Cross Validation
ROC-AUC Analysis
SHAP Explainability
Model Deployment using Flask/FastAPI
