# 📊 Telecom Customer Churn Analysis

An end-to-end data analytics and machine learning project that explores telecom customer behavior, identifies key factors associated with customer churn, predicts churn risk using machine learning models, and presents actionable business insights through an interactive Tableau dashboard.

This project demonstrates a complete data analytics workflow using **Python, Pandas, SQL, statistical analysis, machine learning, and Tableau**.

---

## 📌 Project Overview

Customer churn is a major challenge for telecommunications companies because losing existing customers can directly affect revenue and long-term business growth.

The main objective of this project is to analyze historical telecom customer data to:

- Understand overall customer churn behavior.
- Identify the major factors associated with customer churn.
- Explore customer patterns using exploratory data analysis.
- Perform SQL-based business analysis.
- Statistically validate relationships between customer characteristics and churn.
- Build and compare machine learning models for churn prediction.
- Identify potential high-risk customers.
- Create an interactive Tableau dashboard for business-focused decision support.

---

## 🎯 Project Objectives

The key objectives of this project are:

1. Clean and prepare the telecom customer dataset for analysis.
2. Explore customer behavior and churn patterns.
3. Use SQL to answer important business questions.
4. Apply statistical tests to identify significant relationships with churn.
5. Build machine learning models to predict customer churn.
6. Compare Logistic Regression and Random Forest models.
7. Identify customers who may be at higher risk of leaving.
8. Build an interactive Tableau dashboard to communicate insights clearly.

---

## 📂 Dataset

This project uses a **publicly available telecom customer churn dataset** containing customer demographics, account information, subscribed services, contract details, billing information, and churn status.

### Dataset Summary

| Attribute | Value |
|---|---:|
| Total Customer Records | 7,032 |
| Total Features | 21 |
| Duplicate Rows After Cleaning | 0 |
| Missing Values After Cleaning | 0 |
| Overall Churn Rate | 26.58% |

### Key Features

The dataset includes features such as:

- Customer ID
- Gender
- Senior Citizen status
- Partner
- Dependents
- Tenure
- Phone Service
- Multiple Lines
- Internet Service
- Online Security
- Online Backup
- Device Protection
- Tech Support
- Streaming TV
- Streaming Movies
- Contract Type
- Paperless Billing
- Payment Method
- Monthly Charges
- Total Charges
- Churn Status

---

## 🧹 Data Cleaning and Preparation

The dataset was cleaned and prepared in Google Colab using Python and Pandas.

The main preprocessing steps included:

- Loading and inspecting the dataset.
- Checking dataset dimensions and data types.
- Identifying missing values.
- Checking duplicate records.
- Converting `TotalCharges` into a suitable numeric format.
- Removing or handling invalid records where required.
- Verifying the cleaned dataset before analysis.

### Final Cleaning Results

- **7,032 valid customer records**
- **21 features**
- **0 duplicate rows**
- **0 missing values**

---

## 🔎 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand customer behavior and discover patterns associated with churn.

The analysis included:

- Overall customer churn distribution.
- Churn rate by contract type.
- Churn rate by internet service.
- Churn rate by payment method.
- Churn rate by technical support availability.
- Churn rate by online security.
- Customer tenure distribution.
- Monthly charges distribution.
- Comparison of monthly charges between retained and churned customers.

The exploratory analysis helped identify several important patterns that were later investigated through SQL analysis, statistical testing, and machine learning.

---

## 💾 SQL-Based Churn Analysis

SQL queries were executed within **Google Colab** to analyze important business questions related to customer churn.

The SQL analysis focused on:

- Churn rate by contract type.
- Churn rate by internet service.
- Churn rate by payment method.
- Churn rate by technical support availability.

### Major SQL Findings

| Business Factor | Highest-Risk Category | Churn Rate |
|---|---|---:|
| Contract Type | Month-to-month | 42.71% |
| Internet Service | Fiber optic | 41.89% |
| Payment Method | Electronic check | 45.29% |
| Technical Support | No technical support | 41.65% |

These results indicate that customers with flexible contracts, certain service configurations, and limited technical support may require greater attention from retention teams.

---

## 📈 Statistical Analysis

Statistical testing was performed to determine whether observed relationships between customer characteristics and churn were statistically significant.

### Chi-Square Tests

Chi-Square tests were applied to categorical variables, including:

- Contract Type
- Internet Service
- Payment Method
- Tech Support
- Online Security

The analysis found statistically significant relationships between these customer characteristics and churn.

### Mann-Whitney U Tests

Mann-Whitney U tests were used for numerical variables such as:

- Tenure
- Monthly Charges

The results indicated statistically significant differences between churned and retained customer groups for these variables.

This statistical validation strengthened the findings discovered during exploratory and SQL-based analysis.

---

## 🤖 Machine Learning

Two supervised machine learning classification models were developed and compared:

1. **Logistic Regression**
2. **Random Forest**

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

### Model Performance

The Logistic Regression model achieved approximately:

| Metric | Score |
|---|---:|
| Accuracy | 80.53% |
| Precision | 65.15% |
| Recall | 57.49% |
| F1-Score | 61.08% |
| ROC-AUC | 83.61% |

Based on the overall evaluation results in this project, **Logistic Regression performed better overall for this dataset**.

The project also includes:

- Logistic Regression vs Random Forest performance comparison.
- ROC curve comparison.
- Confusion matrix analysis.
- Random Forest feature importance analysis.
- Predicted churn probability distribution.

---

## 🎯 High-Risk Customer Identification

In addition to overall churn analysis, a potential high-risk customer segment was identified based on selected business conditions.

The high-risk segment included customers with characteristics such as:

- Month-to-month contracts.
- Relatively short customer tenure.
- Higher monthly charges.

### High-Risk Segment Results

| Metric | Result |
|---|---:|
| Potential High-Risk Customers | 935 |
| Churn Rate Within High-Risk Segment | 68.02% |

This segmentation can help businesses prioritize customers for targeted retention strategies, personalized offers, improved support, and proactive engagement.

> **Note:** The business-rule-based high-risk segment is different from the machine learning model's predicted churn probability. The high-risk segment was created using selected business conditions, while the machine learning model estimates churn probability from learned historical patterns.

---

## 📊 Tableau Dashboard

An interactive Tableau dashboard was created to present the main analytical findings in a clear and business-focused format.

### Dashboard KPIs

- Total Customers: **7,032**
- Churned Customers: **1,869**
- Overall Churn Rate: **26.58%**
- Average Monthly Charges: **64.80**
- Potential High-Risk Customers: **935**
- High-Risk Segment Churn Rate: **68.02%**

### Dashboard Visualizations

The dashboard includes:

- Customer Churn Distribution
- Churn Rate by Contract Type
- Churn Rate by Internet Service
- Churn Rate by Payment Method
- Churn Rate by Tech Support
- Potential High-Risk Customer Details Table
- Interactive filtering

---

## 💡 Key Business Insights

The analysis produced several important findings:

- The overall customer churn rate was **26.58%**.
- Customers with **month-to-month contracts** recorded the highest contract-related churn rate at **42.71%**.
- **Fiber optic customers** recorded a churn rate of **41.89%**.
- Customers using **electronic check** had the highest payment-method-related churn rate at **45.29%**.
- Customers without technical support recorded a churn rate of **41.65%**.
- A segment of **935 potential high-risk customers** was identified.
- The churn rate within this high-risk segment was **68.02%**.
- Logistic Regression achieved approximately **80.53% accuracy** and **83.61% ROC-AUC**.

---

## 🏢 Business Recommendations

Based on the findings, telecom companies could consider:

- Providing incentives for month-to-month customers to move to longer-term contracts.
- Investigating the customer experience of fiber optic users.
- Encouraging customers to use alternative or automatic payment methods where appropriate.
- Improving access to technical support and online security services.
- Proactively engaging customers with short tenure and high monthly charges.
- Using churn probability estimates to support targeted retention campaigns.
- Prioritizing high-risk customer segments for personalized retention offers.

---

## 🛠️ Tools and Technologies

| Category | Technologies |
|---|---|
| Programming | Python |
| Data Manipulation | Pandas, NumPy |
| Data Visualization | Matplotlib |
| SQL Analysis | SQL executed within Google Colab |
| Statistical Analysis | SciPy |
| Machine Learning | Scikit-learn |
| Models | Logistic Regression, Random Forest |
| Development Environment | Google Colab |
| Business Intelligence | Tableau |
| Version Control & Portfolio | GitHub |

---

## 📁 Repository Structure

```text
telecom-customer-churn-analysis/
│
├── README.md
│
├── notebooks/
│   └── telecom_customer_churn_analysis.ipynb
│
├── data/
│   └── cleaned_telecom_customer_churn.csv
│
├── dashboard/
│   └── telecom_customer_churn_dashboard.twbx
│
└── images/
    ├── tableau_dashboard.png
    ├── exploratory_data_analysis.png
    ├── sql_based_churn_analysis.png
    └── machine_learning_model_analysis.png
