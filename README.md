# Customer Churn Prediction Using Machine Learning

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-latest-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## Project Overview

Customer churn is one of the most critical challenges for subscription-based businesses, as retaining existing customers is often more cost-effective than acquiring new ones.

This project aims to analyze customer behavior, identify the key factors associated with churn, and develop machine learning models capable of predicting customer attrition to support proactive customer retention strategies.

---

## Repository Structure

```text
customer-churn-prediction/
│
├── data/
│   └── Telco_Customer_Churn.csv
│
├── images/
│   ├── roc_curve.png
│   ├── feature_importance.png
│
├── Customer_Churn_Analysis.ipynb
├── README.md
└── LICENSE
```

---

## Dataset

The dataset contains customer demographic information, service subscriptions, account details, and churn status.

### Target Variable

**Churn**

* Yes → Customer left the company
* No → Customer remained with the company

---

## Tech Stack

### Data Analysis & Visualization

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn

### Machine Learning

* Scikit-Learn

---

## Data Preprocessing

* Removed CustomerID variable
* Applied One-Hot Encoding for categorical variables
* Train-Test Split (80%-20%)
* Feature Scaling using StandardScaler
* Class imbalance handling using Balanced Logistic Regression

---

## Key Findings & EDA Insights

*  Customers with shorter tenure were significantly more likely to churn.
*  Higher monthly charges were associated with increased churn risk.
*  Fiber optic internet users exhibited higher churn rates.
*  Month-to-month contracts showed substantially higher churn rates than long-term contracts.
*  Technical Support and Online Security services were associated with lower churn rates.
*  Electronic Check users demonstrated the highest churn rate among all payment methods.

---

## Model Performance & Evaluation

Customer churn prediction focuses on identifying customers at risk of leaving. Therefore, **Recall** was prioritized as the primary evaluation metric to minimize False Negatives (missing potential churn customers).

| Model                        | Accuracy | Precision | Recall | F1-Score |
| ---------------------------- | -------- | --------- | ------ | -------- |
| Balanced Logistic Regression | 0.73     | 0.50      | 0.79   | 0.61     |
| Random Forest                | 0.79     | 0.63      | 0.48   | 0.54     |
| Decision Tree                | 0.72     | 0.48      | 0.52   | 0.50     |

### Final Model Selection

Although Random Forest achieved higher accuracy, Balanced Logistic Regression was selected as the final model due to its superior Recall (0.79) and F1-Score (0.61).

This trade-off was preferred because failing to identify a potential churn customer is generally more costly than incorrectly flagging a loyal customer.

---

## ROC-AUC Analysis

**ROC-AUC Score: 0.83**

This result indicates a strong ability to distinguish between customers who churn and those who remain with the company.

### ROC Curve

![ROC Curve](roc_curve.png)

---

## Most Influential Features

The analysis revealed that customer churn was primarily influenced by:

![Feature Importance](feature_importance.png)

---

## Business Recommendations

### Contract Optimization

Encourage customers to switch from month-to-month contracts to longer-term contracts through loyalty programs and targeted promotional campaigns.

### Infrastructure & Service Quality

Investigate the underlying causes of high churn among fiber optic internet customers and improve service quality where necessary.

### Cross-Selling Opportunities

Promote value-added services such as Technical Support and Online Security packages during onboarding and engagement campaigns.

### Proactive Retention Strategy

Monitor customers with high monthly charges and implement personalized retention campaigns using the Balanced Logistic Regression model as an early warning system.

---

## Results

The project successfully identified key drivers of customer churn and developed a predictive model capable of detecting customers at risk of leaving.

### Final Model Performance

* Recall: 0.79
* F1-Score: 0.61
* ROC-AUC: 0.83

These results demonstrate that the model can effectively support customer retention initiatives and proactive churn management.

---

## Author

**Yağmur Ozar**

Statistics Graduate | Data Analytics & Machine Learning
