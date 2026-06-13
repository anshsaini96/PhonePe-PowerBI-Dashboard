# 📱 PhonePe Transaction Analytics Dashboard

## 📌 Project Overview

This project presents an interactive Power BI dashboard designed to analyze PhonePe transaction data and provide insights into transaction performance, user activity, payment success rates, and service utilization.

The dashboard enables stakeholders to monitor key business metrics, identify trends, and make data-driven decisions through dynamic visualizations and KPI tracking.

---

## 🎯 Business Objectives

* Analyze transaction value and transaction volume.
* Monitor payment success rates.
* Track month-over-month growth.
* Understand user demographics and engagement.
* Evaluate service-wise transaction performance.
* Identify transaction patterns across weekdays.

---

## 🛠️ Tools & Technologies

* Power BI
* DAX (Data Analysis Expressions)
* Power Query
* Data Modeling
* Excel

---

## 📊 Key Performance Indicators (KPIs)

| KPI                      | Description                               |
| ------------------------ | ----------------------------------------- |
| Total Transaction Value  | Total monetary value of transactions      |
| Total Transactions       | Number of completed transactions          |
| Total Users              | Active users on the platform              |
| Success Rate             | Percentage of successful transactions     |
| Transaction Growth (MoM) | Month-over-Month transaction growth       |
| Value Growth (MoM)       | Month-over-Month transaction value growth |

---

## 📈 Dashboard Features

### Executive Summary

* Transaction Value
* Transaction Count
* Total Users
* Success Rate

### Trend Analysis

* Monthly Transaction Trend
* Growth Analysis

### Service Analysis

* Transaction Value by Service Type
* Service Distribution

### Payment Analysis

* Payment Status Breakdown
* Success vs Failed Transactions

### User Analysis

* Users by Age Group
* User Segmentation Insights

---

## 📸 Dashboard Preview

### Main Dashboard

![Dashboard](Screenshots/Dashboard_Main.png)

### KPI Overview

![KPIs](Screenshots/Dashboard_KPIs.png)

---

## 📋 DAX Measures Used

### Success Rate

```DAX
SuccessRate =
DIVIDE(
    [Successful Transactions],
    [Total Transactions],
    0
)
```

### Transaction Growth %

```DAX
TotalTransMOM% =
VAR PrevMonth =
    CALCULATE(
        [TotalTransaction],
        DATEADD(Date_Table[Date], -1, MONTH)
    )

RETURN
DIVIDE(
    [TotalTransaction] - PrevMonth,
    PrevMonth
)
```

### Transaction Value Growth %

```DAX
TransValueMOM% =
VAR PrevMonth =
    CALCULATE(
        [TotalTransactionValue],
        DATEADD(Date_Table[Date], -1, MONTH)
    )

RETURN
DIVIDE(
    [TotalTransactionValue] - PrevMonth,
    PrevMonth
)
```

---

## 🔍 Key Insights

* Transaction success rate remains consistently above 95%.
* Service categories contribute differently to overall transaction value.
* User activity varies across age segments.
* Transaction performance demonstrates identifiable monthly trends.
* Growth metrics help monitor business performance over time.

---

## 🚀 Future Enhancements

* State-wise transaction analysis
* Geographic visualization using maps
* Customer retention metrics
* Forecasting and predictive analytics
* Advanced KPI drill-through pages

---

## 👨‍💻 Author

Ansh Saini

Power BI | Technology | Business Intelligence

GitHub: https://github.com/anshsaini96
