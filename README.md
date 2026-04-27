# Customer Segmentation Analysis (RFM)

## Overview
This project analyzes e-commerce transaction data to identify high-value customers and support data-driven marketing strategies using the **RFM (Recency, Frequency, Monetary) model**.

The goal is to transform raw transaction data into **actionable customer insights** that can improve retention, targeting, and revenue growth.

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
- `InvoiceNo` → Transaction ID  
- `StockCode` → Product code  
- `Description` → Product name  
- `Quantity` → Number of items  
- `InvoiceDate` → Transaction timestamp  
- `UnitPrice` → Price per unit  
- `CustomerID` → Unique customer ID  
- `Country` → Customer location

### Dataset Description
- ~500,000+ transaction records
- E-commerce transaction data
- Suitable for customer segmentation and behavioral analysis

## Methodology
1. Data Cleaning
   - Removed missing `CustomerID`
   - Filtered invalid values (`Quantity <= 0`, `UnitPrice <= 0`)
   - Converted `InvoiceDate` to datetime format  
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
   - 🟢 **Best Customers** → High value, frequent, recent buyers
   - 🔵 **Loyal Customers** → Frequent buyers
   - 🟡 **Big Spenders** → High spending customers
   - ⚫ **Regular Customers** → Low engagement  

## Key Results
- Revenue distribution is **highly skewed** → small group contributes majority of revenue  
- High-frequency customers generate significantly higher revenue  
- Majority of customers are low-frequency buyers → growth opportunity 

## Visualizations
### 1. Customer Segmentation Distribution
<img width="866" height="533" alt="Customer Segmentation Distribution" src="https://github.com/user-attachments/assets/38a5f1ce-9dc6-4386-99c9-c3a8d1f226a7" />

**Insight:** Most customers fall into the *Regular* segment, while a smaller group drives most revenue.

---

### 2. Frequency vs Revenue
<img width="857" height="557" alt="Frequency vs Revenue" src="https://github.com/user-attachments/assets/1d8410c1-b551-401d-8ade-2e5008700715" />

**Insight:** Higher purchase frequency generally leads to higher revenue.

---

### 3. Revenue by Segment
<img width="857" height="557" alt="Revenue by Segment" src="https://github.com/user-attachments/assets/313e4f73-d1c4-4206-ada5-7f1221bf89e2" />

**Insight:** Best Customers dominate revenue contribution across all segments.

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

## Author
**Talita Sri Indrayuni**  
Aspiring Data Analyst | Data Enthusiast 
