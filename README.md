# Customer Churn Prediction – Model Comparison

## 📌 Overview
This project compares multiple machine learning models to predict customer churn using the Telco Customer Churn dataset.
The goal is to evaluate model performance, understand tradeoffs, and recommend a model suitable for business decision-making.

## 📊 Dataset
- Source: Kaggle – Telco Customer Churn
- Size: 7,043 customers
- Target variable: `Churn` (Yes / No)
- Features: Demographics, services, contract details, billing information

## 🧠 Models Implemented
- Logistic Regression (Baseline)
- Random Forest
- Gradient Boosting Classifier

All models use a unified preprocessing pipeline including:
- One-hot encoding for categorical variables
- Feature scaling for numeric variables
- Train/Test split with stratification
- Cross-validation for hyperparameter tuning

## ⚙️ Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score

Recall was prioritized due to the business importance of identifying potential churners.

## 📈 Results Summary

| Model | Accuracy | Recall (Churn) | Notes |
|------|--------|----------------|------|
| Logistic Regression | ~73% | Moderate | Interpretable baseline |
| Random Forest | ~78% | Better | Handles non-linearities |
| Gradient Boosting | ~80% | Best | Strong bias-variance tradeoff |

## 🏆 Final Recommendation
Gradient Boosting provided the best balance between recall and overall performance, making it the most suitable model for proactive churn prevention strategies.

## 💼 Business Impact
The model can help businesses:
- Identify high-risk customers
- Trigger targeted retention campaigns
- Optimize discounts and follow-ups

## 🚀 How to Run
```bash
pip install -r requirements.txt
jupyter notebook
