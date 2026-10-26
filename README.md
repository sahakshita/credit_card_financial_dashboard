# 💳 Credit Card Financial & Customer Weekly Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black) ![DAX](https://img.shields.io/badge/DAX-0078D4)

## 📌 Overview

An end-to-end business intelligence solution built with **Power BI and DAX** to track weekly credit card operations, revenue trends, customer profitability, and risk metrics across 10,000+ customer records and 667K+ transactions. It is designed for stakeholder monitoring in the banking and financial domain.

## 🎯 Problem Statement

Stakeholders need a clear weekly view of how the credit card portfolio is performing, where revenue comes from, and which customers carry risk. Static reports hide sudden changes, so the dashboard is built to track week-over-week movement and show spending spikes or drops straight away.

**Business questions:**

- How much revenue does the portfolio generate, and how does it split between transactions, interest, and annual fees?
- Which card tiers drive the most transaction activity?
- Which states bring in most of the transaction value?
- How many new cardholders activate their card within 30 days?
- What is the delinquency (default) rate, and which customer groups carry more risk?
- How did revenue change from one week to the next?

## 🧭 Approach

1. Loaded the transaction and customer datasets, plus the weekly incremental files used for updates
2. Created customer segments with DAX (age groups and income groups)
3. Calculated revenue per record from annual fees, transaction amount, and interest earned
4. Built week-over-week measures to compare the current week with the previous week
5. Designed the Transaction and Customer dashboard reports for stakeholders
6. Summarized the findings in an executive report

## 🛠️ Tools and Skills Used

- 📈 **Power BI:** Power BI Desktop, interactive weekly dashboards
- 🧮 **DAX techniques:**
  - **Dynamic segmentation:** `SWITCH(TRUE(), ...)` for custom age groups (`20-30`, `30-40`, etc.) and income groups (`Low`, `Medium`, `High`)
  - **Calculated revenue column:** `Revenue = Annual_Fees + Total_Trans_Amt + Interest_Earned`
  - **Time intelligence (week-over-week growth):** `Current_Week_Revenue` and `Previous_Week_Revenue` measures using `CALCULATE`, `FILTER`, `ALL`, and `WEEKNUM` to calculate week-over-week percentage change

## 💡 Key Insights

### 📅 Overall (year to date)

- 💰 **Revenue:** the portfolio generated **$56.5M** in total revenue ($45.5M from transactions, $8M from interest, and the rest from annual fees) across **667K+** transactions.
- 🏷️ **Card tiers:** Blue and Silver cards account for **93%** of overall transaction volume and revenue, making them the core profit drivers.
- 🗺️ **Geography:** Texas, New York, and California together account for over **68%** of total transaction activity.
- ✅ **Onboarding:** the 30-day card activation rate is **57.5%**, showing healthy early engagement after card delivery.
- ⚠️ **Credit risk:** the delinquency (default) rate is **6.06%**, with higher risk among self-employed customers.

### 🔍 Latest week (Week 53)

- Revenue jumped **28.8%** week over week, driven by seasonal holiday spending across active cardholders.

## ✅ Recommendations

- Apply stricter credit limits for self-employed customers, where defaults run higher
- Protect and grow the Blue and Silver tiers, since they drive 93% of activity
- Watch concentration risk: three states bring in over 68% of transaction value
- Plan for holiday spikes, as shown by the Week 53 jump

## 📂 Repository Contents

| File | Description |
|------|-------------|
| `credit_card_financial_dashboard.pbix` | Power BI report file (open with Power BI Desktop) |
| `Credit_Card_Portfolio_Report.pdf` | Executive summary report with YTD findings and weekly momentum |
| `credit_card_transaction.pdf` | Exported view of the weekly Transaction Report |
| `credit_card_customer.pdf` | Exported view of the weekly Customer Report |
| `credit_card.csv`, `customer.csv` | Primary transaction and customer datasets |
| `cc_add.csv`, `cust_add.csv` | Incremental weekly data files used for updates |

