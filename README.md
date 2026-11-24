# ❤️ Heart Disease Prediction using Machine Learning

## 📌 Project Overview

This project develops a machine learning system to predict the presence of heart disease using patient clinical features.

Three machine learning algorithms were trained and compared:

- Logistic Regression
- Random Forest
- XGBoost

The models were evaluated using Accuracy, Precision, Recall, F1-Score, and ROC-AUC.

SHAP (SHapley Additive exPlanations) was also used to understand how different features influence model predictions.

---

## 🎯 Problem Statement

Heart disease is one of the major health concerns worldwide. Early identification of patients at higher risk can support timely medical attention.

The objective of this project is to build a binary classification model that predicts whether a patient is likely to have heart disease based on clinical measurements.

> **Note:** This project is for educational purposes and is not intended for medical diagnosis.

---

## 📊 Dataset

The project uses the UCI Heart Disease dataset.

The dataset contains clinical information such as:

- Age
- Sex
- Chest pain type
- Resting blood pressure
- Cholesterol
- Maximum heart rate
- Exercise-induced angina
- ST depression
- Number of major vessels
- Thalassemia
- Other clinical attributes

The target variable represents the presence or absence of heart disease.

---

## 🔧 Data Preprocessing

The following preprocessing steps were performed:

- Data loading and inspection
- Handling missing values
- Duplicate checking
- Feature and target separation
- Categorical feature encoding
- Numerical feature preprocessing
- Train-test splitting

A preprocessing pipeline was used to ensure consistent transformations during training and prediction.

---

## 🤖 Machine Learning Models

The following models were trained:

### 1. Logistic Regression

Used as an interpretable baseline classification model.

### 2. Random Forest

An ensemble learning algorithm based on multiple decision trees.

### 3. XGBoost

A gradient boosting algorithm used for high-performance classification.

---

## ⚙️ Hyperparameter Tuning

Random Forest and XGBoost were tuned using GridSearchCV with cross-validation to find better-performing hyperparameter combinations.

---

## 📈 Model Comparison

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 88.52% | 83.87% | 92.86% | 88.14% | **0.966** |
| Random Forest | 85.25% | 82.76% | 85.71% | 84.21% | 0.947 |
| XGBoost | 86.89% | 81.25% | 92.86% | 86.67% | 0.930 |

---

## 🏆 Final Model

Logistic Regression was selected as the final model because it achieved the best overall performance.

### Final Test Performance

- **Accuracy:** 88.52%
- **Precision:** 83.87%
- **Recall:** 92.86%
- **F1-Score:** 88.14%
- **ROC-AUC:** 0.966

Recall was given particular importance because false-negative predictions can be especially important in a medical screening context.

---

## 🔍 Model Explainability

SHAP was used to analyze the contribution of individual features to model predictions.

The SHAP analysis helps understand which features have greater influence on the model's output.

### SHAP Summary Plot

![SHAP Summary](images/shap_summary.png)

---

## 📊 Model Evaluation

### ROC Curve

![ROC Curve](images/roc_curve.png)

### Confusion Matrix

![Confusion Matrix](images/confusion_matrix.png)

The final confusion matrix contained:

- True Negatives: 28
- False Positives: 5
- False Negatives: 2
- True Positives: 26

---

## 📁 Project Structure

```text
heart-disease-ml/
│
├── data/
│   └── heart_disease_cleaned.csv
│
├── images/
│   ├── shap_summary.png
│   ├── roc_curve.png
│   └── confusion_matrix.png
│
├── model/
│   └── heart_disease_model.pkl
│
├── notebooks/
│   └── heart_disease_analysis.ipynb
│
├── .gitignore
├── requirements.txt
└── README.md