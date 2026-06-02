# 🏦 Bank Churn Analysis — Power BI Report

## Overview

> This Power BI report provides a comprehensive analysis of **bank customer churn** — identifying why customers leave, who is most at risk, and what financial impact churn has on the business. It is designed for bank management, data analysts, and retention strategy teams.

The report is built on the `Bank_Churn` dataset and structured across **5 interactive pages**, each focusing on a distinct analytical lens.

## 📊 Report Pages

### 1. Summary Page

<img width="1324" height="786" alt="Bank Churn Summary" src="https://github.com/user-attachments/assets/b05d1cb7-dbf3-41b6-8250-c7110b4c6f06" />


### A high-level executive overview of overall churn performance.

**Key Visuals:**
- **KPI Cards** — Total Customers, Churned Customers, Retained Customers, Churn Rate %, Avg Balance, Avg Credit Score
- **Donut Chart** — Churned vs. Retained Customer split
- **Bar Chart** — Churn by Age Group & Credit Score Group
- **Map** — Geographic distribution of churn
- **Line Chart** — Active vs. Churned customers over time (by month)
- **Combo Chart** — Churn Customers & Churn Rate % by Credit Score Group

**Slicers:** Active Member · Geography · Credit Card Holder · Gender

---

### 2. Customer Analysis 

<img width="1317" height="791" alt="Customer Analysis" src="https://github.com/user-attachments/assets/470423e2-2c07-49da-ac0e-77ccf1159899" />


### Demographic breakdown of churned vs. retained customers.

**Key Visuals:**
- **Clustered Column Chart** — Churn and Retained Customers by Gender
- **Column Chart** — Churn Customers by Tenure
- **Pivot Table** — Churn Rate % by Geography & Age Group
- **Gauge** — Show Churn Rate %

**Slicers:** Gender · Geography · Active Member · Credit Card Holder

---

### 3. Financial Analysis

<img width="1316" height="787" alt="Financial analysis" src="https://github.com/user-attachments/assets/bf5206bf-a6e5-44ae-92c1-a4240caeede9" />


### Financial profile of churned customers and revenue implications.

**Key Visuals:**
- **KPI Cards** — Revenue Impact · Avg Salary of Churned Customers
- **Bar Chart** — Avg Balance Distribution by Churn Status
- **Scatter Chart** — Credit Score vs. Balance Analysis (segmented by churn)
- **Column Charts** — Product Usage Analysis · Salary Group vs. Churn

**Key Fields Used:** `EstimatedSalary`, `Balance`, `CreditScore`, `NumOfProducts`, `Revenue Impact`

**Slicers:** Gender · Geography · Credit Card Holder · Active Member

---

### 4. Behavior Analysis

<img width="1315" height="788" alt="Behavior Analysis" src="https://github.com/user-attachments/assets/72187165-40d1-4e2e-98ac-fd3c991b0a28" />


### Customer behavioral patterns linked to churn risk.

**Key Visuals:**
- **Donut Chart** — Active vs. Inactive Members
- **Column Chart** — Credit Card Holder Analysis by Churn
- **Bar Chart** — Churn Rate by Activity Status
- **Combo Chart** — Active vs. Churned Customers by Tenure

**KPI Cards:** Customer Retention % · Avg Tenure · Credit Card Churn %

**Slicers:** Gender · Geography · Credit Card Holder · Active Member

---

### 5. Customer Details


<img width="1320" height="787" alt="Customer Details (drill through)" src="https://github.com/user-attachments/assets/7054f4bd-ce1a-4ce4-b7c5-34d6e099bed4" />


### Granular, row-level customer data for drill-through and investigation.

**Key Visuals:**
- **Table** — Customer ID, Gender, Geography, Balance, Credit Score, Exit Status, Estimated Salary

**Slicers:** Gender · Geography · Credit Card Holder · Active Member · Churn Status · Age

---

## 🗃️ Data Model

### Using Star Schema

<img width="1589" height="787" alt="Model View" src="https://github.com/user-attachments/assets/9aafc507-3de8-45af-9a07-3bac07135a41" />


### Tables

| Table | Description |
|---|---|
| `Bank_Churn` | Core fact table with customer attributes and churn flag |
| `Geography` | Geographic dimension (country/region per customer) |
| `Gender` | Gender dimension table |
| `ActiveCustomer` | Dimension for active/inactive membership status |
| `CreditCard` | Credit card holder categorization |
| `ExitCustomer` | Exit/churn status dimension |
| `01Measures` | Dedicated measures table |


----

## 📐 Key DAX Measures (`01Measures`)

| Measure | Description |
|---|---|
| `Total_Customer` | Total number of customers |
| `Churn Customers` | Count of customers who exited |
| `Retained Customers` | Count of customers who stayed |
| `Churn Rate %` | Churn Customers / Total Customers |
| `Active_customers` | Count of active members |
| `Avg Balance` | Average account balance |
| `Avg Credit Score` | Average credit score |
| `Revenue Impact` | Estimated financial loss from churn |
| `Avg Salary Churned` | Average salary of churned customers |
| `Customer Retention %` | Inverse of churn rate |
| `Avg Tenure` | Average years customers stay |
| `Credit Card Churn %` | Churn rate among credit card holders |

---

## 🎛️ Interactive Filters (Global Slicers)

All report pages (except Customer Details) share the following slicers for cross-filtering:

- **Gender** — Male / Female
- **Geography** — Country/region of the customer
- **Active Member** — Active / Inactive
- **Credit Card Holder** — Yes / No

The **Customer Details** page additionally includes:
- **Churn Status** — Churned / Retained
- **Age** — Age range slider

---

## 🚀 How to Use

1. Open `Bank_Churn.pbix` in **Microsoft Power BI Desktop** (or publish to Power BI Service).
2. Use the **navigation buttons** to switch between pages.
3. Apply **slicers** to filter the entire page dynamically.
4. Click on any visual element (bar, donut segment, map region) to **cross-highlight** related visuals.
5. Use the **Customer Details** page for row-level drill-through on specific customer segments.

---

## 🛠️ Requirements

- Microsoft Power BI Desktop (latest recommended)
- No external data source connection required — data is embedded in the model

---

## 📌 Use Cases

- Identify high-risk customer segments for proactive retention campaigns
- Understand the financial cost of churn by geography or salary group
- Benchmark current churn rate against targets using the gauge visual
- Explore behavioral factors (tenure, activity, credit card usage) driving attrition
- Export the Customer Details table for CRM or outreach workflows

---

## 👩‍💻 About the Author

**Shalini Saha**  
*Data Analyst | Power BI | Excel | SQL*

💬 Passionate about transforming raw HR data into meaningful workforce insights  
🔗 [LinkedIn](https://www.linkedin.com/in/shalini-saha-b127b428b/) | [GitHub](https://github.com/ShaliniSaha97/)


---

## ⭐ If you found this helpful

Give this repo a ⭐ star — it helps others find it and motivates me to keep building!

---
