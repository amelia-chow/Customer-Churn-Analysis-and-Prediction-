# Telco Customer Churn Analysis

## Project Overview
An analytical deep dive into customer attrition dynamics within the telecommunications sector. This project investigates the underlying patterns behind customer churn, identifying how demographic factors, contract terms, billing preferences, and value-added services influence customer retention. 

---

## Project Objectives
* **Identify and explain key trends in the data:** Analyze the distribution of churn across customer segments, tenure cohorts, and contract structures.
* **Evaluate churn drivers:** Determine which service configurations (e.g., tech support, online security) and account terms correlate most strongly with customer retention versus cancellation.
* **Illustrate with visual elements:** Utilize annotated bar charts, demographic grids, and distribution plots to clearly highlight high-risk customer profiles.

---

## Dataset
* **Source:** Telco Customer Churn dataset (7,043 customer records across 21 features).
* **Target Feature:** `Churn` (Customers who left within the last month: *Yes* / *No*).

Link to the dataset is available [here](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

---

## 🛠️ Tools and Libraries Used
* **Python** (Data processing & exploratory analysis)
* **Pandas & NumPy** (Data cleaning, type casting, and feature wrangling)
* **Matplotlib & Seaborn** (Data visualization & multi-panel chart grids)
* **Jupyter Notebook** (Interactive analysis environment)

---

## 📁 Project Workflow

### 1. 🧹 Data Cleaning and Preparation
* **Data Hygiene & Type Casting:** Identified whitespace blanks (`" "`) within the `TotalCharges` column, resolved missing values, and cast the feature from `object` to `float64`.
* **Categorical Optimization:** Converted discrete columns (`gender`, `Partner`, `Dependents`, `Contract`, `PaymentMethod`, `Churn`) into memory-efficient `category` dtypes.
* **Category Standardization:** Merged redundant sub-categories (e.g., converting `"No internet service"` and `"No phone service"` into `"No"`) across service add-on columns to streamline feature cardinality.

### 2. 📈 Exploratory Data Analysis (EDA)
* **Global Attrition Rate:** Evaluated overall customer churn split to benchmark baseline attrition.
* **Tenure Dynamics:** Analyzed tenure distributions across churned vs. retained cohorts to pinpoint critical drop-off windows in the customer lifecycle.
* **Churn Segment Deep Dive:** Isolated churned customers (`Churn == 'Yes'`) across demographic and account variables to identify vulnerable sub-segments.

### 3. 📊 Data Visualization & Storytelling
* **Annotated Count Plots:** Displayed churn totals alongside exact percentage annotations.
* **Tenure Distribution Boxplots:** Compared median customer tenure across retained and churned groups.
* **Automated Feature Grid:** Generated a multi-panel subplot grid analyzing categorical distributions across all customer features simultaneously.

---

## 🔑 Key Insights & Results
* **Contract Commitment:** Customers on **Month-to-Month contracts** show the highest propensity to churn, while long-term commitments (1-year and 2-year) exhibit significantly higher retention.
* **Payment & Invoicing Friction:** Customers subscribed to **Paperless Billing** and those paying via **Electronic Check** represent the largest proportion of churned users.
* **Early Lifecycle Vulnerability:** Churn is heavily concentrated among low-tenure customers within their initial months of onboarding.
* **Impact of Add-On Services:** The absence of core support services—particularly **Online Security** and **Tech Support**—correlates strongly with higher attrition rates.

Full code can be found (here)[
---

##❓What's Next:
* **Predictive Modeling:** Train baseline classification algorithms (e.g., Logistic Regression, Random Forest, XGBoost) to predict customer churn probability.
* **Model Evaluation & Interpretation:** Assess model performance using **Recall**, **ROC-AUC**, and **F1-Score**.
* **Actionable Business Strategy:** Formulate targeted retention programs (e.g., promotional incentives for migrating month-to-month users to annual plans and dedicated onboarding support during the first 6 months).
