# 📦 Telecom X — Dataset for Machine Learning

## Challenge Data Science — Stage 2 Input Dataset

---

## Overview

This repository receives the dataset **`df_ML.csv`**, generated during **Stage 1: Data Cleaning and Exploratory Analysis**.

The dataset has been fully processed and prepared for Machine Learning modeling tasks aimed at predicting **customer churn**.

All preprocessing steps such as cleaning, encoding, and normalization were completed previously.

---

## Dataset Description

The dataset contains customer behavioral, service usage, and billing information transformed into a numerical format suitable for supervised learning algorithms.

### Dataset Shape

* **Observations:** 6,808 customers
* **Features:** 19 variables
* **Target Variable:** Binary classification

---

## Target Variable

| Variable | Type      | Description                                         |
| -------- | --------- | --------------------------------------------------- |
| `churn`  | int (0/1) | Indicates whether the customer canceled the service |

Encoding:

* `1` → Customer churned
* `0` → Customer retained

---

## Feature Groups

---

### 👤 Customer Demographics

| Variable                 | Type | Description                               |
| ------------------------ | ---- | ----------------------------------------- |
| `customer_seniorcitizen` | int  | Indicates if customer is a senior citizen |
| `customer_partner`       | int  | Customer has a partner                    |
| `customer_dependents`    | int  | Customer has dependents                   |

Binary encoding:

```
Yes = 1
No = 0
```

---

### ⏳ Customer Relationship

| Variable          | Type           | Description                       |
| ----------------- | -------------- | --------------------------------- |
| `customer_tenure` | float (scaled) | Duration of customer relationship |

Normalized using **StandardScaler**.

---

### 🌐 Internet Services

| Variable                    | Type | Description             |
| --------------------------- | ---- | ----------------------- |
| `internet_onlinesecurity`   | int  | Online security service |
| `internet_onlinebackup`     | int  | Online backup service   |
| `internet_deviceprotection` | int  | Device protection       |
| `internet_techsupport`      | int  | Technical support       |

Binary encoding applied.

---

### 💳 Billing Information

| Variable                   | Type           | Description               |
| -------------------------- | -------------- | ------------------------- |
| `account_paperlessbilling` | int            | Paperless billing enabled |
| `account_charges_monthly`  | float (scaled) | Monthly charges           |
| `account_charges_daily`    | float (scaled) | Estimated daily charges   |

Numerical variables standardized.

---

### 📡 Internet Service Type (One-Hot Encoded)

| Variable                               | Type |
| -------------------------------------- | ---- |
| `internet_internetservice_Fiber optic` | bool |
| `internet_internetservice_No`          | bool |

Reference category removed to avoid multicollinearity.

---

### 📄 Contract Type (One-Hot Encoded)

| Variable                    | Type |
| --------------------------- | ---- |
| `account_contract_One year` | bool |
| `account_contract_Two year` | bool |

Baseline category: **Month-to-month contract**.

---

### 💰 Payment Method (One-Hot Encoded)

| Variable                                        | Type |
| ----------------------------------------------- | ---- |
| `account_paymentmethod_Credit card (automatic)` | bool |
| `account_paymentmethod_Electronic check`        | bool |
| `account_paymentmethod_Mailed check`            | bool |

Baseline payment method removed.

---

## Data Characteristics

✅ No missing values
✅ Fully numerical representation
✅ Encoded categorical variables
✅ Normalized numerical features
✅ Ready for ML pipelines

---

## Intended Use

The dataset is prepared for:

* Classification modeling
* Customer churn prediction
* Feature importance analysis
* Model explainability
* Retention strategy development

---

## Next Stage

Stage 2 focuses on:

* Train/Test split
* Model training
* Model evaluation
* Churn probability prediction
* Business decision support
