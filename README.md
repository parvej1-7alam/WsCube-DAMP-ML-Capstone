#  WsCube DAMP Capstone: Predictive Modeling

This repository contains the end-to-end implementation of the Machine Learning Capstone Project for the **WsCube DAMP program**. The project addresses core business challenges in e-commerce through two distinct, yet complementary, predictive modeling applications: Return Risk Prediction and Monthly Demand Forecasting.

---

##  Part 1: Return Prediction Model

###  Project Overview

This component focuses on developing a robust machine learning model to predict whether a given sales transaction is **high-risk for product return**. The model provides actionable intelligence to operations and supply-chain teams.

###  Objective

To construct a predictive model capable of **accurately identifying high-risk return transactions** for timely, corrective actions.

###  Key Tasks & Methodology

* **Data Preprocessing & Cleaning:** Handling missing values, outliers, and balancing the imbalanced target variable (`Is_Return`) using **SMOTE** (Synthetic Minority Over-sampling Technique).
* **Exploratory Data Analysis (EDA):** Deep dive into **Customer, Product, and Store return rates** and generating key insights.
* **Machine Learning Modeling:** Implemented **Logistic Regression** (Baseline) and **Random Forest Classifier** (Robustness).
    * **Advanced Techniques:** **Pipeline creation** with `imblearn` (integrating SMOTE to prevent data leakage) and **Threshold Optimization** using **Youden’s J Statistic** (maximizing $TPR - FPR$).

###  Feature Engineering: The 21 Input Variables

21 highly predictive engineered features were derived, categorized as: **Transaction-Level**, **Customer Behavioral**, **Product-Level**, **Store-Level**, and **Time-Based Cyclical Features**.

###  Model Evaluation: Key Performance Metrics

Evaluated using **Precision**, **Recall (Sensitivity)**, **F1-Score**, **ROC-AUC Score**, and **Custom Threshold Tuning** for business alignment.

---

##  Part 2: Monthly Demand Forecasting

###  Project Overview

This component focuses on developing robust **Time Series Models** to accurately forecast the **monthly units sold** by specific product category and region, crucial for optimizing the supply chain and minimizing inventory costs.

###  Objective

To construct accurate time series models capable of predicting monthly demand at a granular level to support **proactive inventory planning**.

###  Key Tasks & Methodology

* **Data Preparation & Aggregation:** Aggregated raw data into **monthly time series** segmented by `Product Category` and `Region`.
* **Model Selection & Training:** 
    * **Machine Learning (Gradient Boosting):** Using **lagged features** and **time-based features**.

###  Model Evaluation: Key Forecasting Metrics

Forecast accuracy was assessed using business-relevant error metrics:

1.  **MAPE (Mean Absolute Percentage Error):** Provides the average percentage of error, ideal for business interpretation.
2.  **RMSE (Root Mean Square Error):** Measures the standard deviation of the forecast errors.

---

##  Technologies & Libraries Used (Combined)

* **Python** (Core Language)
* **Data Handling & Analysis:** `Pandas`, `NumPy`
* **Machine Learning (Scikit-learn):** `Logistic Regression`, `Random Forest`, `ColumnTransformer`, `StandardScaler`, `GradientBoostingRegressor`
* **Imbalanced Data:** `Imbalanced-learn` (`imblearn`), **SMOTE**
* **Workflow:** `Pipeline`
* **Visualization:** `Matplotlib`, `Seaborn`
* **Development Environment:** `Jupyter Notebook`