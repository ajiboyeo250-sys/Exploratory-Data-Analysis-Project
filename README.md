# Project 2: Exploratory Data Analysis (EDA) - E-Commerce Dataset

## 📌 Project Overview
This project performs an Exploratory Data Analysis (EDA) on an e-commerce dataset of **1,200 transactions** (January 2023 – June 2025) to uncover revenue trends, customer acquisition channel performance, and operational fulfillment risks.

---

## 📊 Summary Statistics

| Metric | Total Price ($) | Unit Price ($) | Order Quantity | Items in Cart |
| :--- | :--- | :--- | :--- | :--- |
| **Count** | 1,200 | 1,200 | 1,200 | 1,200 |
| **Mean** | $1,053.97 | $356.41 | 2.95 | 5.48 |
| **Median** | $823.62 | $364.21 | 3.00 | 5.00 |
| **Min** | $11.39 | $11.39 | 1.00 | 1.00 |
| **Max** | $3,456.40 | $699.93 | 5.00 | 10.00 |
| **Total Sum** | **$1,264,761.96** | **$427,695.30** | **3,535 units** | **6,582 items** |

---

## 🔍 Key Insights & Observations

1. **Top Revenue & Sales Drivers:**
   - **Chairs** brought in the highest overall revenue (**$205,885.34**) with 547 units sold.
   - **Printers** logged the highest total order volume (**181 orders**).
   - **Monitors** produced the lowest revenue ($158,868.87).

2. **High Cancellation & Return Risk (Critical Operational Bottleneck):**
   - **Cancelled Orders:** 20.83% (250 orders)
   - **Returned Orders:** 20.58% (247 orders)
   - **Combined Risk:** **41.41% of all orders** were unfulfilled or returned, representing over **$524,000 in lost/returned gross sales**.

3. **Outlier Detection:**
   - Identified **8 high-value outlier transactions** using the Interquartile Range (IQR) threshold of **$3,330.41**.
   - Highest outlier: Order `ORD200789` at **$3,456.40** (5 Laptops at $691.28 each).

---

## 📁 Repository Files
- `Cleaned data set.xlsx` — Excel sheet containing raw data, descriptive statistics, Pivot Tables, and visual charts.
- `README.md` — Project summary report and analytical findings.
