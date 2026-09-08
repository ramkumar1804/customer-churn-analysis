# 📊 Customer Churn Analysis

An end-to-end customer churn analysis project using **Python, SQL, Pandas, NumPy, Matplotlib, and Seaborn** to identify churn patterns, customer risk, revenue impact, and retention opportunities.

---

## 📌 Project Overview

Customer churn is a major challenge for subscription-based businesses. This project analyzes **customer, subscription, and support data** to understand who is churning, which customer segments have higher churn, and which factors are associated with customer attrition.

The project covers:

- Customer churn and retention
- Churn by subscription plan
- Churn by contract type
- Churn by geography
- Subscription-type analysis
- Customer tenure
- Revenue at risk
- Customer Lifetime Value (CLTV)
- Support escalations and complaints
- Churn-risk segmentation
- Business recommendations

---

## 🎯 Business Objectives

- Measure overall churn and retention
- Identify high-churn customer segments
- Compare churn across plans and contracts
- Analyze geographic and subscription-type churn patterns
- Measure revenue and CLTV impact of churn
- Examine the relationship between support escalations and churn
- Segment customers based on churn risk
- Generate actionable retention recommendations

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Data analysis and processing |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations and feature engineering |
| SQL / SQLite | Database access and data extraction |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Analysis environment |
| Excel | Raw data source |

---

## 🗂️ Dataset

The project uses three related tables stored in SQLite.

### `db_customer`

Contains customer information such as:

- Customer ID
- Name
- Country
- State
- Gender
- Date of Birth

### `db_subscription`

Contains subscription and churn-related information such as:

- Customer ID
- Subscription Start Date
- Renewal Date
- Subscription Type
- Plan Type
- Contract Type
- Cancellation Date
- Cancellation Reason
- Monthly Charges
- CLTV
- Churn Score

### `db_support`

Contains customer support information such as:

- Customer ID
- Complaint Date
- Escalations
- CSAT Score
- Comments

The tables are joined using `customerid`.

---

## 🔄 Project Workflow

```text
Raw Data
   ↓
SQLite Database
   ↓
SQL Data Extraction
   ↓
Data Cleaning
   ↓
Feature Engineering
   ↓
Exploratory Data Analysis
   ↓
KPI Calculation
   ↓
Data Visualization
   ↓
Risk Segmentation
   ↓
Business Insights
   ↓
Recommendations
```

---

## 🔍 Analysis Performed

### Data Cleaning

- Renamed columns
- Removed unnecessary columns
- Converted date fields to datetime
- Standardized gender values
- Handled missing country values
- Removed duplicate support records before merging

### Feature Engineering

- Created `churn_flag` from cancellation status
- Calculated customer tenure in days
- Created complaint counts
- Created churn-risk categories using churn scores
- Merged customer, subscription, and support data

### Exploratory Data Analysis

- Overall churn and retention
- Churn by subscription plan
- Churn by contract type
- Churn by state
- Churn by subscription type
- Cancellation reasons
- Customer tenure
- Revenue impact
- Support escalations
- Churn-risk segmentation
- Correlation analysis

---

## 📈 Key KPIs

| KPI | Result |
|---|---:|
| Churn Rate | **28.57%** |
| Retention Rate | **71.43%** |
| ARPU | **Rs 18.85** |
| Average Customer Tenure | **1,534 days** |
| Revenue at Risk | **Rs 73.94** |
| Escalation Rate | **19.05%** |
| Average Complaints per Customer | **0.43** |
| Escalation–Churn Correlation | **0.77** |

---

## 📊 Key Findings

### 1. Overall Churn

The analysis identified an overall **churn rate of 28.57%** and a **retention rate of 71.43%**.

### 2. Churn by Plan

| Plan | Churn Rate |
|---|---:|
| Basic | **60.00%** |
| Standard | **22.22%** |
| Premium | **14.29%** |

The **Basic plan has the highest churn rate**, making it an important segment for further investigation.

### 3. Churn by Contract Type

| Contract Type | Churn Rate |
|---|---:|
| Monthly | **55.56%** |
| Annual | **8.33%** |

Monthly-contract customers show a substantially higher churn rate than annual-contract customers.

### 4. Geographic Churn

Karnataka and Meghalaya recorded the highest number of churned customers in the analyzed dataset, with **2 churned customers each**.

### 5. Subscription Type

The **Referral** segment recorded the highest number of churned customers among the analyzed subscription types, with **5 churned customers**.

### 6. Revenue Impact

The analysis identified **Rs 73.94 in monthly revenue associated with churned customers**.

The total CLTV associated with churned customers was **Rs 2,047**.

### 7. Support and Churn

The analysis found an **escalation–churn correlation of 0.77**, indicating a strong positive association between support escalations and churn within this dataset.

> Correlation indicates association and does not by itself establish causation.

---

## 🚨 Churn Risk Segmentation

Customers were categorized using the available `churn_score`.

| Churn Score | Risk Level |
|---|---|
| `< 50` | Low |
| `50–69` | Medium |
| `≥ 70` | High |

The analysis identified:

- **13 Low-risk customers**
- **2 Medium-risk customers**
- **6 High-risk customers**

Risk segmentation can help prioritize customers for proactive retention efforts.

---

## 💡 Business Recommendations

### 1. Investigate the Basic Plan

The Basic plan has the highest churn rate. Investigate pricing, service experience, product value, and customer expectations for this segment.

### 2. Encourage Longer-Term Contracts

Monthly-contract customers show much higher churn than annual-contract customers. Suitable customers could be targeted with annual-plan incentives and contract-migration campaigns.

### 3. Prioritize High-Risk Customers

Use churn risk together with customer value, complaints, and support history to create a retention priority list.

### 4. Investigate Support Escalations

Customers with escalated support interactions should be monitored closely and proactively supported where appropriate.

### 5. Investigate High-Churn Locations

Review high-churn states for possible pricing, technical, service, or customer-experience issues.

### 6. Monitor Revenue at Risk

Retention efforts should consider both churn probability and customer value so that higher-impact customers can be prioritized.

---

## 📁 Project Structure

```text
customer-churn-analysis/
│
├── README.md
├── .gitignore
│
├── data/
│   ├── customer_churn.db
│   ├── customer_churn_data_raw.xlsx
│   ├── exported_churn_data.csv
│   └── test_database.sqlite
│
├── notebook/
│   └── churn_analysis.ipynb
│
└── report/
    └── churn_analysis_report.pdf
```

---

## ▶️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/customer-churn-analysis.git
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

### 3. Open the Notebook

```text
notebook/churn_analysis.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

---

## 📄 Project Report

A detailed PDF report containing the project's analysis, KPIs, findings, and recommendations is available at:

```text
report/churn_analysis_report.pdf
```

---

## 🎓 Skills Demonstrated

- SQL / SQLite
- Python
- Pandas
- NumPy
- Data Cleaning
- Feature Engineering
- Exploratory Data Analysis
- Data Visualization
- KPI Analysis
- Customer Segmentation
- Business Analytics
- Insight Generation
- Business Recommendations

---

## 👨‍💻 Author

**Ramkumar Sharma**

B.Tech Information Technology

**Data Analytics | Python | SQL | Excel | Power BI**

---
