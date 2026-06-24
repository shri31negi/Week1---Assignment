# Customer Churn Prediction – EDA & Feature Engineering

## Project Overview

The objective of this project is to analyze customer behavior and identify factors that contribute to customer churn. The dataset contains customer demographics, service usage, account information, and churn status.

The project focuses on:

* Exploratory Data Analysis (EDA)
* Data Cleaning
* Feature Engineering
* Data Preprocessing
* Feature Selection
* Building a machine learning-ready dataset

---

# Phase 1: Data Audit & Initial Exploration

## Objective

Understand the structure, quality, and characteristics of the dataset.

## Analysis Performed

* Dataset shape and dimensions
* Data type inspection
* Missing value analysis
* Duplicate record detection
* Summary statistics
* Unique value counts
* Outlier detection

## Findings

* Missing values were identified and handled appropriately.
* Several categorical features required encoding.
* Numerical variables showed varying scales and distributions.
* Some columns contained highly imbalanced classes.

---

# Phase 2: Distribution & Skewness Analysis

## Objective

Investigate whether numerical variables are normally distributed.

## Analysis Performed

* Histograms
* Boxplots
* Mean vs Median comparison
* Skewness calculations

## Findings

* Monthly charges and total charges showed positive skewness.
* Outliers existed in customer spending variables.
* Log transformation can be considered for heavily skewed features.

## Impact

Reducing skewness improves model stability and predictive performance.

---

# Phase 3: Categorical Feature Assessment

## Objective

Identify categorical variables requiring preprocessing.

### Nominal Features

Examples:

* Gender
* Internet Service
* Payment Method

Recommended:

* One-Hot Encoding

### Ordinal Features

Examples:

* Customer Loyalty Level
* Subscription Tier

Recommended:

* Ordinal Encoding

### High Cardinality Features

Examples:

* City
* Customer ID

Recommended:

* Frequency Encoding or removal if non-informative.

---

# Phase 4: Customer Churn Analysis

## Objective

Identify factors influencing customer churn.

## Key Findings

### Contract Type

Customers on month-to-month contracts showed significantly higher churn rates than customers on long-term contracts.

### Tenure

Customers with shorter tenure were more likely to churn.

### Monthly Charges

Higher monthly charges were associated with increased churn probability.

### Payment Method

Certain payment methods showed higher churn rates.

### Customer Support Services

Customers lacking value-added services such as online security or technical support exhibited higher churn rates.

## Business Recommendations

* Improve retention efforts for new customers.
* Offer incentives for long-term contracts.
* Monitor customers with high monthly charges.
* Promote additional service subscriptions.

---

# Phase 5: Feature Engineering & Preprocessing Pipeline

## Numerical Features

Processing:

* Median Imputation
* StandardScaler
* RobustScaler for outlier-sensitive features

## Categorical Features

Processing:

* Missing value handling
* One-Hot Encoding
* Ordinal Encoding

## Pipeline Benefits

* Consistent preprocessing
* Prevention of data leakage
* Improved reproducibility

---

# Phase 6: Correlation & Feature Importance

## Objective

Identify the strongest predictors of customer churn.

## Correlation Analysis

A correlation matrix was used to detect multicollinearity.

### Findings

* Monthly Charges and Total Charges showed moderate correlation.
* Highly correlated variables were reviewed to avoid redundancy.

## Feature Importance Analysis

Top Predictive Features:

1. Tenure
2. Monthly Charges
3. Contract Type
4. Total Charges
5. Internet Service
6. Payment Method

Least Predictive Features:

* Customer ID
* Non-informative administrative variables

## Business Impact

Understanding the key drivers of churn enables targeted retention strategies and reduces customer attrition.

---

# Conclusion

The analysis revealed that customer tenure, contract type, monthly charges, and service subscriptions are the primary drivers of churn. Appropriate preprocessing, feature engineering, and feature selection techniques were applied to prepare the data for predictive modeling. These insights can help the business improve customer retention and reduce churn rates.
