# E-Commerce Customer Churn Analysis

## Project Overview

This project focuses on analyzing customer churn in an e-commerce environment using MySQL. The project covers data cleaning, data transformation, SQL-based business analysis, and customer return analysis.

The objective is to understand customer churn patterns by analyzing customer tenure, payment preferences, satisfaction, ordering behaviour, complaints, warehouse distance, coupon usage, cashback and other customer-related attributes.

---

## Problem Statement

Customer churn is an important business problem in e-commerce because customer attrition can affect customer satisfaction and long-term business performance.

This project uses SQL to clean and transform an e-commerce customer churn dataset and answer business-oriented questions related to customer behaviour, churn, complaints, payment methods, order categories, satisfaction and returns.

---

## Objectives

- Clean missing values and handle specified outliers.
- Standardize inconsistent categorical values.
- Rename and transform required database columns.
- Create meaningful customer status fields.
- Analyze churned and active customers using SQL.
- Analyze customer behaviour, payment preferences and order patterns.
- Examine complaints and satisfaction scores.
- Analyze cashback and coupon usage.
- Categorize customers based on warehouse-to-home distance.
- Create and analyze customer return information using SQL JOIN operations.

---

## Dataset

The project uses the supplied **E-Commerce Customer Churn dataset**.

The customer data contains attributes related to:

- Customer ID
- Churn status
- Tenure
- Preferred login device
- City tier
- Warehouse-to-home distance
- Preferred payment mode
- Gender
- App usage
- Number of registered devices
- Preferred order category
- Satisfaction score
- Marital status
- Number of addresses
- Complaints
- Order amount hike
- Coupon usage
- Order count
- Days since last order
- Cashback amount

---

## Data Cleaning

The following cleaning operations were performed:

### Missing Value Handling

Mean imputation was applied to:

- `WarehouseToHome`
- `HourSpendOnApp`
- `OrderAmountHikeFromlastYear`
- `DaySinceLastOrder`

Mode imputation was applied to:

- `Tenure`
- `CouponUsed`
- `OrderCount`

### Outlier Handling

Rows where:

```text
WarehouseToHome > 100
