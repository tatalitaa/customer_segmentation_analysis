# Customer Segmentation Analysis (RFM)

## Overview
This project analyzes e-commerce transaction data to identify high-value customers and support data-driven marketing strategies using RFM (Recency, Frequency, Monetary) segmentation.

## Business Problem
Many companies struggle to:
- Identify their most valuable customers
- Understand customer purchasing behavior
- Design effective retention and marketing strategies
Without proper segmentation, businesses risk treating all customers the same, leading to inefficient marketing and missed revenue opportunities.

## Objectives
- Identify high-value and loyal customers
- Analyze customer purchasing patterns
- Segment customers based on behavior
- Provide actionable business recommendations

## Dataset
This project uses the Online Retail Dataset available on Kaggle:
🔗 https://www.kaggle.com/datasets/ulrikthygepedersen/online-retail-dataset

### Dataset Description
This dataset contains transactional data from a UK-based online retail store, covering transactions between December 2010 and December 2011.

It includes information such as:
- InvoiceNo → Unique transaction ID
- StockCode → Product code
- Description → Product name
- Quantity → Number of items purchased
- InvoiceDate → Transaction date and time
- UnitPrice → Price per unit
- CustomerID → Unique customer identifier
- Country → Customer location

### Dataset Description
- ~500,000+ transaction records
- E-commerce transaction data
- Suitable for customer segmentation and behavioral analysis

## Methodology
1. Data Cleaning
   - Removed missing CustomerID
   - Filtered invalid values (Quantity ≤ 0, UnitPrice ≤ 0)
   - Converted InvoiceDate to datetime format
2. Feature Engineering
   - Revenue = Quantity × UnitPrice
3. RFM Calculation
   - Recency → Days since last purchase
   - Frequency → Number of transactions
   - Monetary → Total spending
4. RFM Scoring
   - Customers segmented into quartiles (1–4)
   - Combined into RFM Score (e.g., 444 = best customers)
6. Customer Segmentation
- 🔵 Big Spender 
- 🟠 Best Customer 
- 🟢 Regular Customer
- 🔴 Loyal Customer 

## Key Results
- Customer spending is highly skewed → a small group contributes most of the revenue
- High-frequency customers generate significantly higher revenue
- Majority of customers are low-frequency buyers → strong growth opportunity


## Visualizations

### Revenue Distribution
![Revenue](images/revenue_dist.png)

**Insight:**
Revenue distribution is highly right-skewed, indicating that a small number of customers contribute most of the revenue.

### Frequency vs Revenue
![Frequency](images/freq_vs_revenue.png)

**Insight:**
There is a positive relationship between purchase frequency and revenue. Customers with higher frequency tend to generate higher total revenue.

### Customer Segmentation
![Segment](images/segment_dist.png)

**Insight:**
Most customers fall into the Regular segment, while a smaller group of high-value customers (Best Customers and Big Spenders) contributes significantly to overall revenue.

## Key Insights
- A small percentage of customers drives the majority of revenue (Pareto principle)
- Purchase frequency strongly influences customer value
- Customer behavior varies significantly across segments
  
## Business Recommendations
- Prioritize retention of high-value customers (VIP programs, exclusive offers)
- Increase purchase frequency through loyalty programs
- Target low-frequency customers with personalized campaigns
- Re-engage inactive customers using promotions and incentives

## Tools & Technologies
- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab
  
## Conclusion
RFM segmentation provides a simple yet powerful approach to understanding customer behavior. By leveraging transactional data, businesses can implement targeted strategies to improve customer engagement and drive revenue growth.

