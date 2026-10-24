# Credit Card Financial & Customer Weekly Analytics Dashboard
**Author:** Akshita Sah

## Executive Summary
Built an end-to-end business intelligence and data analytics solution using Power BI and DAX to track and analyze weekly credit card operations, revenue trends, customer profitability, and risk metrics across 10,000+ customer records and 667K+ transactions. Designed specifically for stakeholder monitoring in the financial and banking domain.

---

## Dashboard Preview
*Preview of the weekly Power BI dashboard reports:*

### Weekly Transaction Report
![Transaction Dashboard Preview](transaction_report.png)

### Weekly Customer Report
![Customer Dashboard Preview](customer_report.png)

---

## Tech Stack & Key Features
* **BI and Visualization:** Power BI Desktop, DAX.
* **Key DAX Techniques Used:**
  * **Dynamic Segmentation:** `SWITCH(TRUE(), ...)` for custom Age Groups (`20-30`, `30-40`, etc.) and Income Groups (`Low`, `Medium`, `High`).
  * **Calculated Revenue Columns:** `Revenue = Annual_Fees + Total_Trans_Amt + Interest_Earned`.
  * **Time Intelligence (WoW Growth):** Built dynamic `Current_Week_Revenue` and `Previous_Week_Revenue` measures using `CALCULATE`, `FILTER`, `ALL`, and `WEEKNUM` to calculate week-over-week percentage variance.

---

## Key Business Insights & Findings (YTD Overview)
* **Total Financial Scale:** Generated **$56.5M** in total YTD revenue ($45.5M in transactions, $8M in interest, and the rest from annual fees) across **667K+** transactions.
* **Card Tier Concentration:** **Blue and Silver credit cards** drive **93%** of overall transaction volume and revenue.
* **Geographic Top Performers:** Top 3 states (**Texas, New York, California**) account for over **68%** of total transaction activity.
* **Risk and Operations:** Maintained a healthy **57.5% 30-day card activation rate**, while tracking a **6.06% delinquency (default) rate** with higher risk concentrated among self-employed user segments.

---

## Repository Contents
* **`Credit_Card_Portfolio_Report.pdf`** — Executive summary report detailing YTD findings and weekly momentum.
* **`credit_card_transaction.pdf`** — High-resolution dashboard view of the weekly Transaction Report.
* **`credit_card_customer.pdf`** — High-resolution dashboard view of the weekly Customer Report.
* **`credit_card.csv` & `customer.csv`** — Primary transaction and customer raw datasets.
* **`cc_add.csv` & `cust_add.csv`** — Incremental weekly data files used for updates.
