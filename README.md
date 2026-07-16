# XGBoost-Breast-Cancer-Prediction-

## 📌 Project Overview

This project implements an **XGBoost (Extreme Gradient Boosting) Machine Learning model** for classification.  
The objective is to build a high-performance predictive model by using advanced boosting techniques and optimize model performance using hyperparameter tuning.

XGBoost is an ensemble learning algorithm based on decision trees that combines multiple weak learners to create a strong predictive model.

---

# 📂 Dataset Information

## Dataset Source

Dataset Used:
```
data.csv
```

The dataset contains multiple independent features and one target variable used for prediction.

### Dataset Features

| Feature Type | Description |
|-------------|-------------|
| Independent Variables | Input features used for prediction |
| Target Variable | Output class to predict |

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- Jupyter Notebook

---

# 📁 Project Structure

```
XGBoost-Project
│
├── data.csv
│
├── XGBoost_Project.ipynb
│
├── README.md
│
├── requirements.txt
│
└── model.pkl
```

---

# 🔍 Project Workflow

## 1. Data Collection

- Loaded dataset using Pandas
- Checked dataset structure
- Verified missing values and duplicate records


## 2. Exploratory Data Analysis (EDA)

Performed:

- Dataset information
- Statistical summary
- Missing value analysis
- Duplicate checking
- Feature distribution analysis
- Correlation analysis


## 3. Data Preprocessing

Steps performed:

- Removed unnecessary columns
- Handled missing values
- Converted categorical variables
- Feature scaling
- Train-test splitting


Example:

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

---

# 🤖 Machine Learning Model

## XGBoost Classifier

XGBoost is an optimized gradient boosting algorithm that improves prediction accuracy using multiple decision trees.

Model:

```python
from xgboost import XGBClassifier

model = XGBClassifier(
    n_estimators=100,
    learning_rate=0.1,
    max_depth=3,
    subsample=0.8,
    colsample_bytree=0.8,
    random_state=42
)

model.fit(X_train,y_train)
```

---

# ⚙️ Model Parameters Explained

| Parameter | Description |
|-----------|-------------|
| n_estimators | Number of boosting trees |
| learning_rate | Step size for weight update |
| max_depth | Maximum depth of each tree |
| subsample | Percentage of samples used per tree |
| colsample_bytree | Percentage of features used per tree |
| random_state | Ensures reproducibility |

---

# 📊 Model Evaluation

The model performance was evaluated using:

## Classification Metrics

### Accuracy

Measures overall correct predictions.

```python
accuracy_score(y_test,y_pred)
```

---

### Precision

Measures how many predicted positive cases are actually positive.

---

### Recall

Measures how many actual positive cases are correctly identified.

---

### F1 Score

Balance between Precision and Recall.

---

### ROC-AUC Score

Measures model ability to separate different classes.

---

# 📈 Feature Importance

Feature importance helps identify which features contribute most to model prediction.

Example:

```
Feature                  Importance

concave points_mean      0.290
concave points_worst     0.129
perimeter_worst          0.120
radius_worst             0.092
area_worst               0.084
```

Visualization:

```python
xgb.plot_importance(model)
```

---

# 🔧 Hyperparameter Tuning

Used:

- GridSearchCV
- RandomizedSearchCV
- Cross Validation


Example:

```python
from sklearn.model_selection import GridSearchCV

params = {
    'n_estimators':[100,200],
    'max_depth':[3,5,7],
    'learning_rate':[0.01,0.1]
}


grid = GridSearchCV(
    model,
    params,
    cv=5,
    scoring='accuracy'
)

grid.fit(X_train,y_train)
```

---

# 📌 Final Model Performance

| Metric | Score |
|--------|-------|
| Accuracy | XX% |
| Precision | XX% |
| Recall | XX% |
| F1 Score | XX% |
| ROC-AUC | XX% |

---

# 🚀 How to Run This Project

### Step 1: Clone Repository

```
git clone <repository-link>
```

### Step 2: Install Dependencies

```
pip install -r requirements.txt
```

### Step 3: Run Notebook

```
jupyter notebook
```

Open:

```
XGBoost_Project.ipynb
```

---

# 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
jupyter
```

---

# 💡 Key Learnings

- Understanding Gradient Boosting Algorithm
- Implementing XGBoost Classifier
- Hyperparameter Optimization
- Feature Importance Analysis
- Model Evaluation Techniques
- Improving ML Model Performance

---

# 👨‍💻 Author

**Gourav Kumar**

Data Science & Machine Learning Enthusiast

GitHub:
```
your-github-link
```

LinkedIn:
```
your-linkedin-profile
```

---

# ⭐ If you found this project useful

Give this repository a ⭐ on GitHub.
