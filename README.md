# Customer Segmentation & Sales Analytics Dashboard

## Project Overview

This project focuses on analyzing online retail sales and customer behavior using **MySQL and Power BI**.

The goal is to understand sales performance, identify valuable customer groups, and analyze customer purchasing behavior using **RFM (Recency, Frequency, Monetary) analysis**.

---

## Objective

- Analyze sales and revenue trends
- Identify top-performing products and countries
- Analyze customer purchasing behavior
- Calculate Recency, Frequency, and Monetary (RFM) metrics
- Segment customers based on their RFM scores
- Provide data-driven insights for customer retention and business decisions

---

## Tools & Technologies

- **MySQL**
- **SQL**
- **Power BI Desktop**
- **DAX**
- **RFM Analysis**

---

## Dataset

**UCI Online Retail Dataset**

- 541,909 transaction records
- 8 variables
- Online retail transaction data

Dataset source:

https://archive.ics.uci.edu/dataset/352/online-retail

---

## Data Preparation

The raw transaction data was cleaned using MySQL.

The cleaning process included:

- Removing records with missing CustomerID
- Removing cancelled orders
- Removing invalid quantities
- Removing invalid unit prices
- Creating a Revenue column using Quantity × UnitPrice

### Dataset Summary

| Metric | Value |
|---|---:|
| Raw Transactions | 541,909 |
| Clean Transactions | 397,884 |
| Customers Analyzed | 4,338 |
| Total Orders | 18,532 |
| Total Revenue | 8.91M |
| Units Sold | 5.17M |

---

## RFM Analysis

RFM analysis was used to understand customer purchasing behavior.

### Recency
Measures how recently a customer made a purchase.

### Frequency
Measures how frequently a customer placed orders.

### Monetary
Measures the total amount spent by a customer.

Customers were scored using **NTILE(4)** and classified into different customer segments based on their combined RFM scores.

---

## Customer Segmentation

Customers were classified into four segments:

| Segment | Customers |
|---|---:|
| High-Value | 1,306 |
| Loyal | 1,299 |
| At-Risk | 1,289 |
| Lost | 444 |
| **Total** | **4,338** |

---

## Power BI Dashboard

The dashboard contains two pages.

### Page 1 — Sales Overview

The Sales Overview dashboard provides analysis of:

- Total Revenue
- Total Customers
- Total Orders
- High-Value Customers
- Average Order Value
- Units Sold
- Average Units per Order
- Monthly Revenue Trend
- Top 10 Products by Revenue
- Top 10 Countries by Revenue
- Top 10 Products by Units Sold
- Average Order Value Trend

### Page 2 — Customer Segmentation & RFM Analysis

The second dashboard provides:

- Customer Segment Distribution
- Customers by Segment
- Average Monetary Value by Segment
- Average Purchase Frequency by Segment
- Customer Recency vs Monetary Value
- RFM Customer Details
- Customer Segment filtering
- Country filtering

---

## Key Insights

- Total revenue analyzed is approximately **8.91M**.
- The analysis includes **4,338 identified customers**.
- **High-Value customers** form the largest customer segment with 1,306 customers.
- **Loyal** and **At-Risk** customers contain 1,299 and 1,289 customers respectively.
- **444 customers** fall into the Lost segment.
- The **United Kingdom** contributes the majority of revenue among the countries shown in the top-10 ranking.
- RFM analysis helps identify customers with high monetary value and strong purchasing behavior.
- The dashboard combines sales performance and customer value analysis to support business decision-making.

---

## Business Recommendations

### 1. Focus on High-Value Customers

Develop personalized offers and loyalty strategies to retain high-value customers.

### 2. Re-engage At-Risk Customers

Use targeted promotions and follow-up campaigns to encourage customers who are becoming inactive.

### 3. Retain Loyal Customers

Provide loyalty rewards and exclusive offers to maintain repeat purchasing behavior.

### 4. Improve Lost Customer Re-engagement

Identify lost customers with previous high spending and target them with suitable win-back campaigns.

### 5. Optimize Product Performance

Use product-level sales and quantity analysis to identify products that contribute strongly to revenue and sales volume.

---

## Project Outcome

Created an interactive **Sales and Customer Segmentation Dashboard** using MySQL and Power BI, combining SQL-based data cleaning, RFM analysis, customer segmentation, and business visualization to support sales performance and customer retention analysis.

---

## Project Files

```text
rfm_project/
│
├── rfm_dashboard.pbix
├── rfm_analysis.sql
├── Customer_Segmentation_Sales_Analytics_Report.docx
├── Page1_Sales_Overview.png
├── Page2_Customer_Segmentation.png
└── README.md
