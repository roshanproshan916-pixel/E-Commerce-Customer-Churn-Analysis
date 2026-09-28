# 🛒 E-Commerce Customer Churn Analysis

> **MySQL | SQL Data Cleaning | Data Transformation | Business Analysis**

An end-to-end SQL project focused on analyzing customer churn in an e-commerce environment.  
The project demonstrates how raw customer data can be cleaned, transformed, analyzed, and combined with return information using relational SQL operations.

---

## 📌 Project Overview

Customer churn is an important business problem in e-commerce, as customer attrition can affect customer satisfaction and long-term business performance.

This project uses **MySQL** to analyze an E-Commerce Customer Churn dataset and explore patterns related to:

- Customer churn
- Customer tenure
- Complaints
- Payment preferences
- Order behaviour
- Customer satisfaction
- Coupon usage
- Cashback
- Warehouse-to-home distance
- Customer returns

The project follows a structured data-analysis workflow from **data cleaning to business-oriented SQL analysis**.

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Clean and prepare the customer churn dataset.
- Handle missing values using mean and mode imputation.
- Remove specified outlier records.
- Standardize inconsistent categorical values.
- Transform and rename database columns.
- Create meaningful customer status fields.
- Perform SQL-based business analysis.
- Analyze customer behaviour and churn-related patterns.
- Create a customer returns table.
- Perform relational joins between customer and return data.
- Verify the final database and analysis workflow.

---

## 🗂️ Dataset

The project uses the supplied **E-Commerce Customer Churn dataset**.

### Major Attributes

| Category | Attributes |
|---|---|
| Customer | CustomerID, Gender, MaritalStatus |
| Churn | ChurnStatus, ComplaintReceived |
| Customer Behaviour | Tenure, OrderCount, CouponUsed |
| Device | PreferredLoginDevice, NumberOfDeviceRegistered |
| Location | CityTier, WarehouseToHome |
| Payment | PreferredPaymentMode |
| Orders | PreferredOrderCat, OrderAmountHikeFromlastYear |
| Engagement | HoursSpentOnApp, DaySinceLastOrder |
| Satisfaction | SatisfactionScore |
| Value | CashbackAmount |

---

# 🧹 Data Cleaning

The following data-cleaning operations were implemented using SQL.

### Missing Value Treatment

Mean imputation was applied to:

- `WarehouseToHome`
- `HourSpendOnApp`
- `OrderAmountHikeFromlastYear`
- `DaySinceLastOrder`

Mode imputation was applied to:

- `Tenure`
- `CouponUsed`
- `OrderCount`

The rounded mean value of `DaySinceLastOrder` was verified as **4**.

### Outlier Removal

Customer records with:

```sql
WarehouseToHome > 100
