# Retail Sales Performance Dashboard

## Excel & Power BI Data Analytics Project

An end-to-end retail sales analysis project developed using Microsoft Excel and Power BI.

The project analyzes 500 simulated retail sales transactions to understand overall business performance, profitability, product performance, regional performance, customer behavior, and monthly sales trends.

The goal was to transform raw transactional data into clear business insights and interactive dashboards that can support business decision-making.

---

## Project Overview

**Role:** Data Analyst

**Tools Used:**
- Microsoft Excel
- Power Query
- Power BI
- DAX

**Dataset:** 500 simulated retail sales transactions

**Project Type:** Sales & Profitability Analysis

---

## Business Questions

The analysis was designed to answer the following questions:

1. What are the total sales and total profit?
2. What is the overall profit margin?
3. Which product category generates the highest sales?
4. Which products generate the most revenue and profit?
5. Which region performs best?
6. Which customers contribute the most revenue?
7. How do sales and profit change month by month?
8. What business recommendations can be derived from the analysis?

---

## Key KPIs

- **Total Sales:** ₹87.92 Lakh
- **Total Profit:** ₹23.62 Lakh
- **Profit Margin:** 26.87%
- **Total Orders:** 500
- **Unique Customers:** 60
- **Top Region:** West
---

---

## Power BI Dashboard

powerbi-dashboard.png

The Power BI dashboard provides an interactive view of sales performance with dynamic KPI cards, Region and Category filters, monthly sales and profit trends, category performance, regional performance, Top 5 products, and Top 5 customers.

---

## Excel Dashboard

excel-dashboard.png

The Excel dashboard was developed using PivotTables, PivotCharts, formulas, calculated fields, and interactive slicers to analyze the same retail business dataset.

---
---

## Key Business Insights

### Overall Performance
- The business generated approximately **₹87.92 lakh in total sales** and **₹23.62 lakh in total profit**.
- The overall **profit margin was 26.87%** across 500 orders.
- The dataset contained **60 unique customers**.

### Category Performance
- **Furniture** was the highest-performing category with approximately **₹52.33 lakh in sales** and **₹13.70 lakh in profit**.
- **Office Supplies** generated considerably lower sales but achieved the highest category profit margin at approximately **52.97%**.

### Regional Performance
- **West** was the highest-performing region overall with approximately **₹25.21 lakh in sales**.
- Regional performance changes dynamically when filters are applied in the Power BI dashboard.

### Product Performance
- **Study Desk** was the highest-selling product with approximately **₹24.20 lakh in sales**.
- Study Desk also generated approximately **₹6.05 lakh in profit**.
- **Monitor** ranked second in sales at approximately **₹23.59 lakh**.

### Customer Performance
- **Omkar Business** was the highest-value customer by sales, generating approximately **₹13.33 lakh** from 51 orders.
- **Nisha Mart** placed 52 orders but generated lower total sales than Omkar Business.
- This shows that a higher number of orders does not necessarily result in higher customer value.

### Monthly Sales Trend
- **September** recorded the highest monthly sales at approximately **₹9.37 lakh**.
- **April** was the weakest month with approximately **₹3.95 lakh in sales**.
- Sales recovered strongly after April, with particularly strong performance in June, August, and September.

---
## Business Recommendations

### 1. Prioritize High-Performing Furniture Products
Maintain sufficient inventory for high-performing Furniture products, particularly **Study Desk**, and evaluate additional promotional opportunities.

### 2. Explore Growth Opportunities in Office Supplies
Office Supplies generated relatively low sales but achieved strong profit margins. The business should evaluate opportunities such as product bundles, cross-selling, promotions, and wider distribution.

### 3. Analyze Regional Success Factors
Study the factors contributing to the strong performance of the **West region** and evaluate whether successful practices can be applied to lower-performing regions.

### 4. Focus on High-Value Customer Retention
Consider retention and relationship-management strategies for high-value customers such as **Omkar Business, Nisha Mart, TechPoint, Nova Traders, and Mehta Traders**.

### 5. Investigate the April Sales Decline
April recorded the lowest monthly sales. Additional business information should be reviewed to determine whether seasonality, inventory availability, promotions, customer demand, or other factors contributed to the decline.

> **Note:** The dataset identifies performance patterns but does not establish the exact cause of the April decline. Further business context would be required before making a causal conclusion.

---
## DAX Measures Used

The Power BI dashboard uses DAX measures to calculate dynamic business KPIs that automatically respond to Region and Category filters.

### Total Sales

```DAX
Total Sales =
SUM(Raw_Sales_Data[Sales_INR])
Total Profit =
SUM(Raw_Sales_Data[Profit_INR])
Profit Margin % =
DIVIDE([Total Profit], [Total Sales], 0)
Total Orders =
DISTINCTCOUNT(Raw_Sales_Data[Order_ID])
Unique Customers =
DISTINCTCOUNT(Raw_Sales_Data[Customer_ID])
Top Region =
VAR RegionTable =
    TOPN(
        1,
        VALUES(Raw_Sales_Data[Region]),
        [Total Sales],
        DESC
    )
RETURN
    CONCATENATEX(
        RegionTable,
        Raw_Sales_Data[Region],
        ""
    )
## Skills Demonstrated

### Data Analysis
- Data cleaning and validation
- Exploratory business analysis
- KPI development
- Sales and profitability analysis
- Product performance analysis
- Customer analysis
- Regional performance analysis
- Monthly trend analysis
- Business insight generation
- Business recommendations

### Microsoft Excel
- Excel Tables
- SUM, COUNTA, and UNIQUE
- PivotTables
- PivotCharts
- Calculated Fields
- Top-N analysis
- Interactive slicers
- KPI cards
- Dashboard development

### Power BI
- Power Query
- Data type validation and transformation
- DAX measures
- DISTINCTCOUNT
- Dynamic KPI cards
- Top-N filtering
- Interactive slicers
- Data visualization
- Interactive dashboard development

### Business Skills
- Translating business questions into analytical requirements
- Identifying meaningful KPIs
- Communicating insights clearly
- Developing data-supported recommendations
- Designing client-friendly dashboards

---

## Project Files

- `powerbi-dashboard.png` - Final Power BI dashboard
- `excel-dashboard.png` - Final Excel dashboard
- `README.md` - Project documentation

> **Note:** This project uses simulated retail sales data and was created for portfolio and skills-demonstration purposes.
