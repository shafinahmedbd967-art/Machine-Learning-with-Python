# Machine Learning With Python 🤖🐍

Welcome to my Machine Learning learning repository!
This repository contains my class notebooks, datasets, practice files, and hands-on machine learning work using Python.

---

# 📌 Repository Information

* **Repository Name:** `Machine-Learning-with-Python`
* **GitHub Username:** `shafinahmedbd967-art`

---

# 🚀 Topics Covered

This repository includes:

* Introduction to Machine Learning
* Python for Machine Learning
* Data Analysis Basics
* Working with CSV datasets
* Data Cleaning & Preprocessing
* Data Visualization
* Study Hours Dataset Analysis
* Titanic Dataset Practice
* Mobile Dataset Analysis
* Machine Learning Fundamentals
* Jupyter Notebook Practice
* Hands-on ML Exercises

---

# 📂 Repository Structure

```text id="3j4w2m"
Machine-Learning-with-Python/
│
├── Class 01/
│   ├── ML_Class01.ipynb
│   └── titanic.csv
│
├── Class 02/
│   ├── ML_Class02.ipynb
│   └── titanic.csv
│
├── Class 03/
│   ├── ML_Class03.ipynb
│   ├── Study_Hours.csv
│   ├── titanic.csv
│   └── Working_With_Study_Hours_Dataset.ipynb
│
├── Class 04/
│   ├── ML_With_Python_Class04.ipynb
│   └── mobile_dataset.csv
│
├── Class 05/
│   ├── data.csv
│   └── ML_With_Python_Class05_ipynb.ipynb
│
├── Class 06/
│   └── ML_With_Python_Class06_ipynb.ipynb
│
├── Class 07/
│   └── 5048.csv
│   └── ML_With_Python_Class07_ipynb.ipynb
│   
└── README.md
```

---
# 📚 Class-wise Learning Journey

## 🎓 Class 01 — Foundations of Data Ingestion & Dataset Inspection

### Topics Covered

* Introduction to Machine Learning workflow
* Python environment setup for ML
* Data loading using Pandas
* Reading CSV files using `pd.read_csv()`
* Dataset structure inspection
* Understanding rows and columns
* Initial missing value identification
* Exploratory dataset analysis

### Key Concepts

```python
import pandas as pd
import matplotlib.pyplot as plt

dataset = pd.read_csv("titanic.csv")
dataset.head()
dataset.info()
dataset.isnull().sum()
```

---

## 🎓 Class 02 — Missing Data Handling & Statistical Imputation

### Topics Covered

* Missing value diagnosis
* Null value counting
* Data visualization using Matplotlib
* Mean Imputation
* Median Imputation
* Mode Imputation
* Missing value verification

### Key Concepts

```python
dataset.isnull().sum()

dataset["Agemean"] = dataset["Age"].fillna(dataset["Age"].mean())

dataset["Agemode"] = dataset["Age"].fillna(
    dataset["Age"].mode()[0]
)

dataset["Agemedian"] = dataset["Age"].fillna(
    dataset["Age"].median()
)
```

---

## 🎓 Class 03 — Random Sample Imputation & Correlation Analysis

### Topics Covered

* Random Sample Imputation
* DataFrame slicing and filtering
* Feature and target variable understanding
* Correlation analysis
* Heatmap visualization
* Study Hours vs Exam Score analysis
* Introduction to regression concepts

### Key Concepts

```python
random_sample = dataset["Age"].dropna().sample(
    dataset["Age"].isnull().sum(),
    random_state=0
)

dataset.corr()

import seaborn as sns
sns.heatmap(dataset.corr(), annot=True)
```

---

## 🎓 Class 04 — Feature Engineering & Feature Selection

### Topics Covered

* Mobile dataset analysis
* Feature variance inspection
* Feature importance analysis
* Chi-Square Feature Selection
* SelectKBest
* ExtraTreesClassifier
* Correlation-based feature filtering

### Key Concepts

```python
from sklearn.feature_selection import SelectKBest, chi2

bestfeatures = SelectKBest(
    score_func=chi2,
    k=10
)

from sklearn.ensemble import ExtraTreesClassifier

model = ExtraTreesClassifier()
model.fit(X, y)
```

---

## 🎓 Class 05 — Data Transformation & Train-Test Split

### Topics Covered

* Handling categorical data
* Label Encoding
* Feature matrix creation
* Target variable extraction
* Train-Test Split
* Dataset preparation for ML models

### Key Concepts

```python
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

dataset["column"] = le.fit_transform(
    dataset["column"]
)

X = dataset.iloc[:, :-1]
y = dataset.iloc[:, -1]

from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.20,
    random_state=42
)
```

---

## 🎓 Class 06 — Machine Learning Models & Performance Evaluation

### Topics Covered

### Tree-Based Models

* Decision Tree
* Random Forest
* Extra Trees Classifier

### Boosting Algorithms

* AdaBoost
* Gradient Boosting

### Distance-Based Algorithms

* K-Nearest Neighbors (KNN)

### Margin-Based Algorithms

* Support Vector Classifier (SVC)

### Linear Models

* Ridge Classifier
* SGD Classifier

### Probabilistic Models

* Gaussian Naive Bayes

### Performance Evaluation

* Accuracy Score
* Model Comparison
* Benchmark Ranking

### Key Concepts

```python
from sklearn.metrics import accuracy_score

ypred = model.predict(X_test)

accuracy_score(y_test, ypred)
```

---

## 🎓 Class 07 — End-to-End Machine Learning Pipeline

### Topics Covered

* Complete Machine Learning workflow
* New dataset implementation
* Feature preprocessing
* Correlation analysis
* Data cleaning pipeline
* Feature transformation
* Multi-model evaluation
* End-to-end predictive system development

### Learning Outcome

By the end of this class, I was able to:

✅ Load datasets

✅ Clean and preprocess data

✅ Handle missing values

✅ Encode categorical features

✅ Select important features

✅ Train multiple ML algorithms

✅ Evaluate model performance

✅ Build a complete Machine Learning pipeline

---

# 💻 Technologies Used

* Python 3
* Jupyter Notebook
* Google Colab
* VS Code

---

# 📚 Libraries Used

Some commonly used Python libraries in this repository:

* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

# 🎯 Purpose of This Repository

The main goals of this repository are:

* Learn Machine Learning step by step
* Practice real datasets
* Improve data analysis skills
* Build ML fundamentals
* Store class notebooks and exercises

---

# 📈 Datasets Used

This repository contains practice datasets such as:

* Titanic Dataset
* Study Hours Dataset
* Mobile Dataset
* Custom CSV datasets

---

# ▶️ How to Run

1. Clone the repository

```bash id="v1i1pb"
git clone https://github.com/shafinahmedbd967-art/Machine-Learning-with-Python.git
```

2. Open the project folder

```bash id="d41m5l"
cd Machine-Learning-with-Python
```

3. Run Jupyter Notebook

```bash id="ec1z5m"
jupyter notebook
```

---

# 🌱 Learning Progress

I will continuously update this repository with new machine learning notebooks, datasets, and projects as I continue learning.

---

# ⭐ Support

If you find this repository helpful:

* Give this repository a ⭐
* Follow my GitHub profile
* Share your suggestions and feedback

---

# 👨‍💻 Author

## Shafin Ahmed

GitHub:
https://github.com/shafinahmedbd967-art

---

# 📌 Note

This repository is created for educational and learning purposes only.
