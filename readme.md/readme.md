# Credit Card Fraud Detection using Machine Learning

## Overview

This project focuses on detecting fraudulent credit card transactions using Machine Learning techniques. Since fraudulent transactions are extremely rare compared to legitimate ones, the dataset is highly imbalanced. To address this challenge, the project applies **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset before training multiple classification models.

The project includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, performance comparison, and feature importance analysis to identify the most effective fraud detection model.

---

# Problem Statement

Credit card fraud causes significant financial losses to banks and customers every year. Traditional rule-based systems struggle to identify sophisticated fraudulent transactions.

The objective of this project is to build a machine learning model capable of accurately distinguishing fraudulent transactions from legitimate ones while minimizing false positives and false negatives.

---

# Dataset

**Dataset:** Credit Card Fraud Detection Dataset

The dataset contains:

- 284,807 transactions
- 30 input features
- 1 target variable

### Features

- **Time** – Time elapsed between transactions.
- **V1 – V28** – PCA-transformed anonymous features.
- **Amount** – Transaction amount.

### Target

- **Class = 0** → Legitimate Transaction
- **Class = 1** → Fraudulent Transaction

---

# Project Workflow

## 1. Data Understanding

Performed an initial analysis to understand:

- Dataset structure
- Feature descriptions
- Data types
- Statistical summary
- Missing values
- Class distribution

---

## 2. Data Cleaning

Data preprocessing included:

- Checking for missing values
- Handling null values
- Preparing the dataset for machine learning

---

## 3. Exploratory Data Analysis (EDA)

Several visualizations were created to understand transaction behavior.

### Analysis Included

- Distribution of fraudulent vs legitimate transactions
- Time vs Fraud relationship
- Transaction amount analysis
- Correlation heatmap
- PCA feature relationships
- Feature distributions

Key observations:

- Fraudulent transactions occur in specific time intervals.
- Certain PCA features (e.g., V4 and V14) show strong correlations with fraud.
- Higher transaction amounts are associated with increased fraud probability in specific ranges.

---

## 4. Handling Class Imbalance

The original dataset is highly imbalanced.

### Before SMOTE

```
Majority Class  >>>>>>>>>>>>>>> Minority Class
```

### After SMOTE

```
Majority Class  ========= Minority Class
```

The project uses:

- **SMOTE (Synthetic Minority Over-sampling Technique)**

to generate synthetic fraud samples and balance the training dataset.

---

## 5. Machine Learning Models

Multiple classification algorithms were trained and evaluated.

### Models Implemented

- Logistic Regression
- Support Vector Classifier (SVC)
- Decision Tree Classifier
- Random Forest Classifier
- Gaussian Naive Bayes
- K-Nearest Neighbors (KNN)

Each model was evaluated using:

- Accuracy
- Confusion Matrix
- Precision
- Recall
- F1-Score

---

## 6. Feature Importance

Random Forest was used to analyze feature importance.

This helps identify which transaction features contribute the most to fraud detection.

---

# Project Architecture

```text
                    Credit Card Dataset
                             │
                             ▼
                  Data Understanding & EDA
                             │
                             ▼
                    Data Cleaning
                             │
                             ▼
                 Missing Value Handling
                             │
                             ▼
                Train-Test Split
                             │
                             ▼
          Class Imbalance Handling (SMOTE)
                             │
                             ▼
              Machine Learning Models
      ┌──────────────────────────────────────┐
      │ Logistic Regression                  │
      │ Support Vector Classifier            │
      │ Decision Tree                        │
      │ Random Forest                        │
      │ Gaussian Naive Bayes                 │
      │ K-Nearest Neighbors                  │
      └──────────────────────────────────────┘
                             │
                             ▼
                  Model Evaluation
                             │
                             ▼
               Best Model Selection
                             │
                             ▼
              Feature Importance Analysis
```

---

# Machine Learning Pipeline

```text
Raw Dataset
      │
      ▼
Data Cleaning
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Feature Selection
      │
      ▼
Train-Test Split
      │
      ▼
SMOTE Oversampling
      │
      ▼
Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Best Model Selection
```

---

# Technology Stack

### Programming

- Python

### Data Processing

- Pandas
- NumPy

### Visualization

- Matplotlib
- Seaborn
- Plotly

### Machine Learning

- Scikit-learn
- SMOTE (Imbalanced-learn)

### Algorithms

- Logistic Regression
- Support Vector Machine
- Decision Tree
- Random Forest
- Gaussian Naive Bayes
- K-Nearest Neighbors

---

# Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

# Key Features

- Comprehensive Exploratory Data Analysis
- Data Cleaning and Preprocessing
- Handling Imbalanced Data using SMOTE
- Comparison of Multiple Machine Learning Models
- Feature Importance Analysis
- Fraud Detection Pipeline
- Visual Analytics

---

# Future Improvements

- Hyperparameter tuning using GridSearchCV
- Ensemble learning techniques (XGBoost, LightGBM, CatBoost)
- Deep Learning models for fraud detection
- Real-time fraud detection API using Flask or FastAPI
- Model Explainability using SHAP or LIME
- Deployment with Streamlit or Docker

---

# Project Structure

```text
Credit-Card-Fraud-Detection
│
├── Understanding_of_Data.ipynb
├── creditcard.csv
├── requirements.txt
├── README.md
└── images/
```

---

# Author

**SRISHHA**
