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

- **Class 0 (No Churn):** Precision = 0.85, Recall = 0.85, F1 = 0.85  
- **Class 1 (Churn):** Precision = 0.58, Recall = 0.58, F1 = 0.58  

---

## 🔑 Key Insights
- The model performs **very well for non-churners** but moderately for churners.  
- **False Negatives (158 cases)** = missed churners → most costly for the business.  
- Predicted churn probabilities can be used for **customer risk scoring** and prioritized retention efforts.  

---

## 💡 Business Recommendations
- Deploy the model into a **CRM system** as an **early warning tool**.  
- Focus retention campaigns on **high-risk customers** identified by the model.  
- Optimize resource allocation by balancing **retention cost vs. customer lifetime value (CLV)**.  
- Improve recall on churners with:  
  - Hyperparameter tuning (GridSearch, RandomSearch).  
  - Cost-sensitive learning (penalize missed churners).  
  - Advanced ensemble methods (LightGBM, CatBoost).  

---

## 🛠️ Tech Stack
- **Python 3.11**  
- **Libraries:** pandas, numpy, scikit-learn, imbalanced-learn, xgboost, matplotlib, seaborn  
- **Model Export:** pickle (`customer_churn_model.pkl`)  

---

## 🚀 How to Run
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/customer-churn-ml.git
   cd customer-churn-ml
