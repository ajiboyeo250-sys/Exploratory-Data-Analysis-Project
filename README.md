# Exploratory Data Analysis (EDA): E-Commerce Sales & Fulfillment Performance

## Executive Summary
This project delivers a comprehensive Exploratory Data Analysis (EDA) on an e-commerce dataset comprising **1,200 transaction records** spanning from **January 2023 through June 2025**. Utilizing Microsoft Excel, the analysis evaluates overall revenue performance, customer ordering patterns, distribution channel effectiveness, and critical fulfillment bottlenecks.

The primary objective is to transform raw transactional records into actionable business intelligence, identifying key revenue drivers and highlighting operational risks—most notably a **41.4% unfulfilled order rate** representing over $524,000 in lost gross sales.

---

## Core Business Questions
1. **Sales Performance:** Which product lines and acquisition channels generate the highest gross revenue and order volume?
2. **Data Distribution & Outliers:** What is the underlying distribution of order values, and are extreme values driven by data entry errors or legitimate bulk purchases?
3. **Fulfillment Efficiency:** What proportion of placed orders successfully reach the customer versus ending in cancellations or returns?

---

## Dataset Architecture
The raw dataset consists of **1,200 rows and 14 variables**:
* **Order Identifiers:** `OrderID`, `TrackingNumber`, `CustomerID`
* **Timeline & Location:** `Date` (Jan 2023 – Jun 2025), `ShippingAddress`
* **Product Details:** `Product`, `Quantity`, `UnitPrice`, `TotalPrice`
* **Customer Behavior:** `PaymentMethod`, `OrderStatus`, `ItemsInCart`, `CouponCode`, `ReferralSource`

---

## Analytical Methodology
The project was executed in Microsoft Excel through a structured four-stage workflow:

1. **Data Cleaning & Quality Audit:**
   * Audited all 1,200 records for duplicate `OrderID` values.
   * Verified mathematical integrity across all rows (`TotalPrice = Quantity × UnitPrice`).
   * Addressed missing values in non-critical columns (`CouponCode` left blank where no discount applied).

2. **Descriptive Statistical Modeling:**
   * Applied Excel formulas (`COUNT`, `AVERAGE`, `MEDIAN`, `MIN`, `MAX`, `SUM`) to establish foundational metrics across numerical columns.

3. **Outlier Detection via IQR Method:**
   * Calculated First Quartile ($Q_1$), Third Quartile ($Q_3$), and Interquartile Range ($IQR = Q_3 - Q_1$).
   * Set upper bound threshold ($Q_3 + 1.5 \times IQR$) to isolate extreme order values without removing valid business transactions.

4. **PivotTable & Visual Dashboard Construction:**
   * Modeled revenue breakdown by product line and acquisition channel (`ReferralSource`).
   * Categorized order fulfillment statuses into percentage distributions to assess operational leakage.

---

## Descriptive Statistics Summary

| Metric | Total Price ($) | Unit Price ($) | Order Quantity | Items in Cart |
| :--- | :---: | :---: | :---: | :---: |
| **Count** | 1,200 | 1,200 | 1,200 | 1,200 |
| **Mean** | $1,053.97 | $356.41 | 2.95 | 5.49 |
| **Median** | $823.62 | $364.21 | 3.00 | 5.00 |
| **Minimum** | $11.39 | $11.39 | 1 | 1 |
| **Maximum** | $3,456.40 | $699.93 | 5 | 10 |
| **Total Sum** | $1,264,761.96 | $427,695.30 | 3,535 | 6,582 |

---

## Key Business Insights

### 1. Skewed Order Value Distribution
* The average order value (**Mean: $1,053.97**) is significantly higher than the typical midpoint order (**Median: $823.62**).
* This right-skewed distribution indicates that high-value sales pull up the overall average, making the median $823.62 a more accurate representation of a standard customer transaction.

### 2. Validated Bulk Purchase Outliers
* Using the Interquartile Range (IQR) threshold, **8 orders were flagged as high-value outliers**, reaching up to **$3,456.40**.
* Cross-referencing confirmed these are legitimate large orders where customers purchased maximum quantity (5 units) of premium products, rather than system logging errors.

### 3. Fulfillment Leakage & Operational Risk
* **Cancelled Orders:** 20.8% (250 orders)
* **Returned Orders:** 20.6% (247 orders)
* **Combined Failure Rate:** **41.4% of total orders** were never fulfilled successfully, tying up **over $524,000** in unrealized revenue and increasing administrative costs.

### 4. Top Performing Products & Acquisition Channels
* **Chairs** generated the highest cumulative revenue (**$205,885.34** across 547 units).
* **Printers** logged the highest overall transaction frequency (**181 orders**).
* **Instagram and Facebook** stood out as top revenue-generating marketing channels, leading referral sources in total gross sales.

---

## Strategic Recommendations
1. **Fulfillment Audit:** Conduct an immediate operational review into logistics, delivery estimates, and product descriptions to reduce the 41.4% cancellation and return rate.
2. **VIP Customer Segment:** Establish a dedicated bulk-order experience and priority support channel for high-value orders ($2,500+).
3. **Channel Optimization:** Maintain marketing spend on high-performing social channels (Instagram and Facebook) while testing promotional adjustments on lower-converting acquisition sources.

---

## Repository Deliverables
* **`Cleaned data set.xlsx`**: The primary Excel workbook containing raw transaction records, calculated descriptive statistics, outlier formulas, and interactive PivotTables/PivotCharts.
* **`README.md`**: Detailed documentation covering project objectives, methodologies, statistical outputs, and strategic takeaways.
