# 📊 Customer Churn Prediction (Supervised ML)

## 👋 Hi there!
This project focuses on predicting customer churn for a Telco company using **Supervised Machine Learning**.  
The main goal is to identify customers who are likely to churn, so the company can take proactive actions to retain them.

## 🎯 Assignment Objectives
- Perform data preparation and cleaning
- Conduct Exploratory Data Analysis (EDA)
- Build at least **two supervised learning models** for classification
- Evaluate models using metrics like Accuracy, Precision, Recall, F1-score, and AUC-ROC
- Interpret the results to support business decisions

## 📂 Dataset Overview

- **customerID**: Unique ID for each customer  
- **gender**: Customer gender (Male / Female)  
- **SeniorCitizen**: Whether customer is a senior citizen (1 = Yes, 0 = No)  
- **Partner**: Whether customer has a partner (Yes / No)  
- **Dependents**: Whether customer has dependents (Yes / No)  
- **tenure**: Number of months the customer has been with the company  
- **PhoneService**: Whether customer has phone service (Yes / No)  
- **MultipleLines**: Whether customer has multiple phone lines (Yes / No / No phone service)  
- **InternetService**: Customer internet service type (DSL / Fiber optic / No)  
- **OnlineSecurity**: Whether customer has online security addon (Yes / No / No internet service)  
- **OnlineBackup**: Whether customer has online backup addon (Yes / No / No internet service)  
- **DeviceProtection**: Whether customer has device protection addon (Yes / No / No internet service)  
- **TechSupport**: Whether customer has tech support addon (Yes / No / No internet service)  
- **StreamingTV**: Whether customer subscribes to streaming TV (Yes / No / No internet service)  
- **StreamingMovies**: Whether customer subscribes to streaming movies (Yes / No / No internet service)  
- **Contract**: Contract type (Month-to-month / One year / Two year)  
- **PaperlessBilling**: Whether customer uses paperless billing (Yes / No)  
- **PaymentMethod**: Customer payment method (Electronic check / Mailed check / Bank transfer / Credit card)  
- **MonthlyCharges**: Customer’s monthly charges (numeric)  
- **TotalCharges**: Customer’s total charges (numeric)  
- **Churn**: Whether customer churned (Yes / No)  

## 🛠 Tools & Libraries
- Python  
- Pandas & NumPy  
- Matplotlib & Seaborn  
- Scikit-learn  
- Imbalanced-learn (for oversampling if needed)  
- Google Colab (for coding & sharing notebook)  

## 📝 Project Workflow

### 1️⃣ Data Preparation
- Imported necessary libraries  
- Loaded dataset from CSV  
- Handled missing values  
- Encoded categorical variables  
- Split dataset into features (`X`) and target (`y`)  

### 2️⃣ Exploratory Data Analysis (EDA)
- Checked distribution of numerical features → **skewed right** (tenure, MonthlyCharges, TotalCharges)  
- Checked categorical features → mostly binary (Yes/No) with imbalances in non-binary categories like Contract, PaymentMethod  
- Visualized correlations and distribution patterns  

### 3️⃣ Data Preprocessing & Feature Engineering
- Handled skewed variables and scaling if needed  
- Split dataset into training and test sets  

### 4️⃣ Modeling
- Tested multiple supervised learning models:  
  - Logistic Regression  
  - Decision Tree  
  - Random Forest  
  - XGBoost  
- Trained models on training set and validated performance  

### 5️⃣ Model Evaluation
- Metrics used: **Accuracy, Precision, Recall, F1-score, ROC-AUC**  
- Compared models based on these metrics  

## 📊 Analysis & Insights

### 1️⃣ General Data Analysis
- Numerical features are skewed to the right → most customers have lower tenure/charges, few with very high values  
- Binary categorical features dominated by “No”, except PhoneService and PaperlessBilling → mostly “Yes”  
- Non-binary categorical features show imbalanced categories → one dominant category, others smaller but roughly balanced  

### 2️⃣ Training Set Results
- **ROC-AUC:** highest for XGBoost, Logistic Regression, Random Forest → models can distinguish classes well  
- **Recall:** highest for Logistic Regression and Decision Tree → detect positive cases effectively  
- **F1-score:** highest for Logistic Regression and XGBoost → good balance between Recall and Precision  
- **Conclusion:** Logistic Regression is the best performing model overall  

### 3️⃣ Test Set Results
- **ROC-AUC:** highest for Logistic Regression and Random Forest  
- **Recall:** highest for Logistic Regression; Random Forest recall is very low  
- **F1-score:** highest for Logistic Regression and Decision Tree  
- **Conclusion:** Logistic Regression remains the best choice for deployment  
