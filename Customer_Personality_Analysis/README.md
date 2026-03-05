# Customer Marketing Campaign Performance Dashboard

## Project Overview
This project analyzes customer demographics, spending behavior, and marketing campaign performance using Power BI. The goal is to identify key customer segments, evaluate campaign effectiveness, and uncover insights that support data-driven marketing strategies.

---

# TDSP Methodology

## 1. Business Understanding
The marketing team wants to understand:
- Which customer segments generate the highest revenue
- Which marketing campaigns perform best
- How demographic attributes influence purchasing behavior

Key questions addressed:
- What age groups dominate the customer base?
- How does income influence spending behavior?
- Which campaigns produce the highest responses?
- Which product categories drive the most revenue?

---

## 2. Data Understanding
Dataset: **Marketing Campaign Dataset**

Key attributes include:
- Customer demographics (Age, Education, Marital Status)
- Income levels
- Product spending across categories
- Marketing campaign responses

Main variables used:

| Feature | Description |
|------|------|
| Income | Customer annual income |
| Education | Education level |
| Total_Spending | Total amount spent across product categories |
| Customer_Age | Derived from birth year |
| AcceptedCmp1–5 | Campaign response indicators |

---

## 3. Data Preparation
Data preparation was performed in Power BI using Power Query.

Steps included:

- Data cleaning and type correction
- Creation of derived features:
  - **Customer_Age**
  - **Total_Spending**
  - **Income_Group**
- Handling missing values
- Creating calculated measures:
  - Total Customers
  - Average Customer Income
  - Total Customer Spending
  - Campaign Responses

---

## 4. Modeling
Additional calculated columns and measures were created using DAX.

Example:
Income_Group =
SWITCH(
TRUE(),
'marketing_campaign'[Income] < 30000, "Low Income",
'marketing_campaign'[Income] < 60000, "Middle Income",
'marketing_campaign'[Income] < 90000, "High Income",
"Very High Income"
)

Measures used for KPIs:
Total Customers = COUNTROWS(marketing_campaign)
Average Income = AVERAGE(marketing_campaign[Income])
Total Revenue = SUM(marketing_campaign[Total_Spending])
Campaign Responses =
SUM(marketing_campaign[AcceptedCmp1]) +
SUM(marketing_campaign[AcceptedCmp2]) +
SUM(marketing_campaign[AcceptedCmp3]) +
SUM(marketing_campaign[AcceptedCmp4]) +
SUM(marketing_campaign[AcceptedCmp5])


---

## 5. Visualization
An interactive Power BI dashboard was built to analyze customer behavior and marketing performance.

### Dashboard Components

**KPI Section**
- Total Customers
- Average Customer Income
- Total Customer Spending
- Campaign Responses

**Customer Demographics**
- Customer Age Distribution

**Marketing Campaign Analysis**
- Campaign Response Performance

**Customer Spending Insights**
- Product Category Spending
- Spending by Education Level
- Average Spending by Income Group

**Filters**
- Age Range
- Education Level
- Marital Status

---

## 6. Key Insights
- Majority of customers fall within the **40–60 age group**.
- **Higher income customers spend significantly more**.
- **Graduation and PhD customers generate the highest spending**.
- **Campaigns 3 and 4 achieved the strongest responses**.
- **Meat and Sweet categories drive the largest share of product spending**.
- **Mid-income customers show strong growth potential**.

---

## Tools & Technologies
- Power BI
- Power Query
- DAX
- Data Visualization

---

## Project Outcome
The dashboard enables marketing teams to identify high-value customer segments, evaluate campaign effectiveness, and make informed decisions for targeted marketing strategies.
