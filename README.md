# 📊 Customer Churn Prediction with Machine Learning

## 📌 Project Overview
This project focuses on predicting **customer churn** for a telecommunications company using **supervised Machine Learning** models.  
Customer churn—defined as the percentage of customers who stop using a service—is a critical metric for telecom businesses.  
By anticipating churn, companies can implement **proactive retention strategies**, optimize costs, and improve customer lifetime value.  

---

## 🎯 Objectives
- Build predictive models to classify customers as **Churn** or **No Churn**.  
- Handle **imbalanced data** using oversampling techniques.  
- Compare the performance of multiple classification algorithms.  
- Provide **actionable business recommendations** based on model insights.  

---

## 📂 Dataset
The dataset used in this project is the **Telco Customer Churn Dataset**, which is publicly available on **Kaggle**:  
👉 [Telco Customer Churn on Kaggle](https://www.kaggle.com/blastchar/telco-customer-churn)  

- **Size:** 7,043 records  
- **Features:** Demographics, service subscriptions, contract details, payment methods, monthly charges, tenure, etc.  
- **Target Variable:** `Churn` (Yes/No)  

### Data Challenges
- **Imbalanced target variable**: ~73% stayed vs. 27% churned.  
- **Solution:** Applied **SMOTE (Synthetic Minority Oversampling Technique)** to rebalance the dataset (4,138 per class).  

---

## ⚙️ Data Preparation
- **Missing values** handled.  
- **Categorical variables** encoded with `LabelEncoder`.  
- **Train/Test split:** 80% / 20%.  
- **Scaling:** Not required (tree-based models handle raw scales).  

---

## 🤖 Models Implemented
Three classification algorithms were trained and evaluated:  

1. **Decision Tree** 🌳 – interpretable but prone to overfitting.  
2. **Random Forest** 🌲 – ensemble method with robust performance.  
3. **XGBoost** ⚡ – gradient boosting with strong accuracy.  

---

## 📈 Model Evaluation
Evaluation metrics included **Accuracy, Precision, Recall, F1-score**, and a **Confusion Matrix**.  
A **5-fold cross-validation** strategy was applied for robustness.  

### Cross-Validation Accuracy
- Decision Tree: **0.78**  
- Random Forest: **0.84** ✅  
- XGBoost: **0.83**  

👉 **Random Forest was selected as the best-performing model**.  

---

## 🧪 Test Results (Random Forest)
- **Accuracy:** 0.78  

**Confusion Matrix:**  
