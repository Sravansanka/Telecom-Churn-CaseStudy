# 📞 Telecom Churn Prediction Case Study
### Authors - Sravana Kumar Sanka & Srikrishna Jana
## 📝 Problem Statement

In the competitive telecom industry, customers frequently switch service providers, resulting in an average **15-25% annual churn rate**. Given that acquiring a new customer is **5-10 times more expensive** than retaining an existing one, customer retention has become a top priority.

### 🔍 Business Objective
The primary goal of this case study is to build a **machine learning model** that predicts high-risk churn customers based on usage patterns. This enables proactive retention strategies to reduce customer loss.

## 🎯 Key Objectives
1. **Predict High-Value Customer Churn:** Identify customers likely to churn in the near future, enabling targeted offers and discounts.
2. **Identify Important Predictors:** Pinpoint key variables influencing churn, revealing insights into customer behavior.
3. **Recommend Churn Management Strategies:** Develop actionable recommendations based on model insights.

---

## 📊 Customer Lifecycle Phases

Customers typically transition through three phases before churning:

1. **Good Phase:** The customer is satisfied and shows no signs of switching.
2. **Action Phase:** The customer exhibits early dissatisfaction signs — reduced engagement, declining usage, etc. This is the ideal intervention window.
3. **Churn Phase:** The customer finally decides to leave the service provider.

**In this dataset:**
- **Months 6 and 7** represent the **good phase**.
- **Month 8** is the **action phase**.
- **Month 9 (September)** is the **churn phase**.

---

## 🔧 Data Preprocessing Using ColumnTransformer and Pipeline

This project employs a robust and production-ready approach to data preprocessing using `ColumnTransformer` and `Pipeline` from scikit-learn.

### 🚀 Why Pipeline Approach?
✅ Ensures consistent transformations for both training and test data.  
✅ Enhances modularity and makes code easier to maintain.  
✅ Reduces the risk of data leakage by centralizing all transformations.  
✅ Boosts scalability and ensures production readiness.  

### 🔹 Key Preprocessing Steps
- **Custom Feature Engineering:** Creating new features from date columns and handling missing values.  
- **Imputation:** Managing missing values with `SimpleImputer`.  
- **Dropping Unnecessary Columns:** Removing irrelevant data.  
- **Passthrough:** Retaining unchanged columns as-is.  

This streamlined approach ensures data undergoes the same transformations throughout the entire pipeline, improving reliability and reproducibility.

---

## 📈 Models and Evaluation Metrics

### 🔎 For Objectives 2 & 3 (Feature Importance & Recommendations)
**Interpretative Models:** Designed to provide insights into churn factors.  
- **F1 Score** is the chosen metric, balancing precision and recall to ensure insights are actionable and meaningful.

### 🔮 For Objective 1 (Churn Prediction)
**Predictive Models:** Focused on accurately predicting customer churn.  
- **Accuracy** is the primary metric for ensuring reliable predictions across both churners and non-churners.

---

## 📌 Key Insights and Recommendations

### 🔺 Top 10 Positive Contributors (Increase Churn Risk)
1. **Low ARPU in Action Phase**  
2. **Decline in Outgoing On-Net Calls (MOU)**  
3. **Reduced Outgoing ISD Calls (MOU)**  
4. **Lower Incoming Off-Net Calls (MOU)**  
5. **Decrease in Total Outgoing Call Usage (MOU)**  
6. **Drop in Outgoing Local Calls (MOU)**  
7. **Smaller Last Recharge Amount**  
8. **Reduced Incoming On-Net Calls (MOU)**  
9. **Lower Incoming Off-Net Minutes of Use (MOU)**  
10. **Decreased Total Recharge Amount**

### 🟩 Top 10 Negative Contributors (Decrease Churn Risk)
1. **Increasing Trend in Total Recharge Amount**  
2. **Higher Outgoing Local Calls (MOU)**  
3. **Active Local Incoming Calls (MOU)**  
4. **Rising Outgoing ISD Calls (MOU)**  
5. **Higher Data Usage (MB)**  
6. **Increased Outgoing On-Net Calls (MOU)**  
7. **Large Recharge Amounts**  
8. **Frequent Incoming On-Net Calls (MOU)**  

### 📢 Recommendations
1. **Proactive Interventions:** Offer tailored incentives to customers showing early signs of churn.  
2. **Targeted Campaigns:** Prioritize high-value customers with declining usage patterns.  
3. **Customer Monitoring:** Automate alerts for critical behavioral shifts, enabling timely actions.

---

## 🏆 Model Selection
For final submission, the **hyperparameter-tuned XGBoost model** was chosen due to its superior accuracy.  
🔗 [Kaggle Leaderboard Link](https://www.kaggle.com/competitions/telecom-churn-case-study-hackathon-c-69/leaderboard)
