# Retail Inventory Optimization Workflow

## Project Overview
This project builds an automated inventory analytics workflow using Alteryx to analyze store-level inventory performance, sales trends, and demand forecasting.

---

# TDSP Methodology

## 1. Business Understanding

Retailers must balance inventory levels to avoid stockouts and excess inventory.

Key questions addressed:
- Which stores generate the highest revenue?
- Which product categories require inventory optimization?
- How does demand forecasting influence stock levels?

---

## 2. Data Understanding

Dataset: Retail Store Inventory Dataset

Key attributes include:

- Store ID
- Product ID
- Inventory Level
- Units Sold
- Price
- Discount
- Demand Forecast
- Region

---

## 3. Data Preparation

Performed using Alteryx tools:

- Data Cleanse Tool
- Auto Field Tool
- Data type conversion
- Null value handling

---

## 4. Modeling

Derived metrics created using Formula Tool:

Inventory Value  = [Inventory Level] * [Price]
Estimated Revenue = [Units Sold] * [Price]


---

## 5. Workflow Design

Key workflow steps:

- Data ingestion
- Data cleansing
- Feature engineering
- Aggregation using Summarize Tool
- Output generation

---

## 6. Key Insights

- Certain stores maintain excessive inventory levels.
- Some product categories show higher demand patterns.
- Inventory optimization opportunities exist across multiple stores.

---

## Tools Used

- Alteryx Designer
- Data Preparation
- Workflow Automation
