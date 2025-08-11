# End-to-End ML Pipeline for Customer Churn Prediction

## 📌 Objective
The objective of this project is to build a **reusable and production-ready machine learning pipeline** to predict whether a customer will churn (leave the service) based on their demographic and service usage data.

This is part of the **DevelopersHub AI/ML Engineering Internship – Advanced Task 2**.

---

## 📊 Dataset
**Name:** [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/blastchar/telco-customer-churn)  
**Description:**  
The dataset contains information about 7,043 customers, including:
- Demographics (gender, senior citizen, partner, dependents)
- Account information (tenure, contract type, payment method)
- Service usage details (internet, phone, TV, security services)
- Churn status (Yes/No)

---

## 🛠 Approach
1. **Data Loading & Exploration**
   - Loaded dataset into Pandas DataFrame
   - Checked for missing values, class distribution, and feature types

2. **Feature Engineering**
   - Separated features into numerical and categorical groups
   - Encoded categorical variables with `OneHotEncoder`
   - Scaled numerical variables with `StandardScaler`

3. **Pipeline Construction**
   - Used `ColumnTransformer` for preprocessing
   - Integrated preprocessing with model training in a single `Pipeline`

4. **Model Training**
   - Trained a `RandomForestClassifier`
   - Tuned hyperparameters with `GridSearchCV`

5. **Evaluation**
   - Evaluated with Accuracy, Precision, Recall, F1-score
   - Plotted a Confusion Matrix for visual performance analysis

---

## 📈 Results
- **Best Model:** RandomForestClassifier with tuned hyperparameters
- **Evaluation Metrics (Test Set):**
  - Accuracy: ~0.80
  - F1-score: ~0.65 (macro)
- **Insights:**
  - Short-term customers (low tenure) are more likely to churn
  - Month-to-month contracts have the highest churn rate
  - Fiber optic customers tend to churn more in this dataset
Note
The trained model file model/churn_pipeline.joblib is NOT included due to GitHub's file size limit.
To test with a trained model, run the notebook to retrain it or request the file separately.


---

## 🚀 How to Run the Project
### **1. Clone the repository**
```bash
git clone https://github.com/your-username/customer-churn-prediction-pipeline.git
cd customer-churn-prediction-pipeline
