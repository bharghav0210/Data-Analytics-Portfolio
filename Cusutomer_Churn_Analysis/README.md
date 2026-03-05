# Customer Churn Analysis Dashboard

## Project Overview
This project analyzes customer churn behavior using Power BI. The dashboard helps identify factors influencing customer churn such as contract type, tenure group, internet service type, and monthly charges.

The goal is to help businesses proactively identify high-risk customers and reduce churn through targeted retention strategies.

---

# TDSP Methodology

## 1. Business Understanding
Customer churn significantly impacts subscription-based businesses. The objective of this project is to analyze churn patterns and identify factors contributing to customer attrition.

Key questions addressed:
- Which customer segments are most likely to churn?
- How do contract types affect churn rate?
- Do higher monthly charges increase churn probability?
- How does tenure influence customer retention?

---

## 2. Data Understanding

Dataset: **Telco Customer Churn Dataset**

Key attributes include:

| Feature | Description |
|------|------|
CustomerID | Unique customer identifier |
Contract | Contract type |
Tenure | Customer duration |
MonthlyCharges | Monthly subscription charges |
InternetService | Type of internet service |
Churn | Customer churn indicator |

---

## 3. Data Preparation

Steps performed in Power BI:

- Data cleaning
- Handling missing values
- Creating derived features:
  - Tenure Group
  - Churn Rate
- Data transformation using Power Query

---

## 4. Modeling

Calculated measures created using DAX:

Total Customers :
Total Customers = COUNT(Customer[CustomerID])


Churn Customers:
Churn Customers =
CALCULATE(COUNT(Customer[CustomerID]), Customer[Churn] = "Yes")

Churn Rate:
Churn Rate = DIVIDE([Churn Customers], [Total Customers])


---

## 5. Visualization

Dashboard Components:

KPI Section
- Total Customers
- Churned Customers
- Churn Rate
- Average Monthly Charges
- Total Revenue

Customer Segmentation
- Churn by Contract Type
- Churn by Tenure Group
- Churn by Internet Service

Behavioral Insights
- Churn vs Monthly Charges
- Churn Distribution

---

## 6. Key Insights

- Month-to-month customers show the highest churn.
- New customers churn more frequently.
- Higher monthly charges increase churn probability.
- Fiber optic users demonstrate higher churn tendencies.

---

## Tools Used
- Power BI
- Power Query
- DAX
- Data Visualization


