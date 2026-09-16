# Customer Revenue Intelligence

## From Transactions to Business Decisions

**$2.32M in revenue looks healthy — until you ask where that revenue actually comes from.**

This project investigates customer and sales performance using Power BI, with a focus on identifying revenue concentration, customer value patterns, geographic performance, and opportunities to improve order completion.

Rather than building a dashboard only for visualization, the goal was to answer a more important business question:

> **What is driving revenue performance, and where should management focus its attention?**

---

## Executive Dashboard

![Executive Dashboard](images/01_executive_overview.png)

The executive overview provides visibility into:

- Total Revenue
- Completed Revenue
- Total Orders
- Average Order Value
- Active Customers
- Completion Rate
- Monthly Revenue Trend
- Revenue by City
- Revenue by Customer Segment
- Revenue by Order Status

Interactive filters allow the analysis to be segmented by city and customer segment.

---

## Business Questions

The analysis was designed around five key questions:

1. Where is revenue geographically concentrated?
2. Which customer segments generate the most value?
3. How is revenue changing over time?
4. How much revenue is associated with completed versus pending orders?
5. Where are the strongest opportunities for revenue protection or growth?

---

## Data & Modeling

The analytical model contains five tables:

- Customers
- Orders
- Order Details
- Products
- Calendar

The model separates transactional information from customer, product, and calendar dimensions.

![Data Model](images/02_data_model.png)

Key relationships allow orders to be analyzed by customer attributes and time period.

---

## Data Preparation

Power Query was used to:

- Import structured Excel tables
- Validate column data types
- Standardize categorical fields
- Validate date fields
- Prepare the dataset for modeling
- Create analysis-ready fields

A dedicated calendar structure was used to ensure months were displayed chronologically rather than alphabetically.

---

## DAX Measures

The dashboard uses measures including:

- Total Revenue
- Completed Revenue
- Total Orders
- Average Order Value
- Active Customers
- Completion Rate

These measures respond dynamically to report filters and visual interactions.

---

# Key Business Insights

## 1. Santiago is the main revenue engine — and a concentration point

Santiago generated approximately **$1.20M of $2.32M in total revenue**, accounting for roughly **52% of overall sales**.

This makes Santiago the strongest-performing market while also indicating meaningful geographic revenue concentration.

**Decision opportunity:** Investigate the customer and purchasing patterns driving Santiago's performance and evaluate whether successful patterns can be replicated in Santo Domingo and La Vega.

---

## 2. Premium customers dominate revenue

The Premium segment generated approximately **$1.74M**, representing roughly **75% of total revenue**.

Regular customers generated approximately $0.51M, while Basic customers contributed approximately $0.07M.

**Decision opportunity:** Protect Premium customer retention while identifying high-potential Regular customers who could be developed into higher-value customers.

---

## 3. Pending orders represent a measurable revenue opportunity

Monthly revenue reached its highest level in **August at approximately $0.37M**.

Approximately **79.6% of total order value was associated with completed orders**, leaving roughly **$0.47M associated with pending orders**.

**Decision opportunity:** Investigate why orders remain pending and identify operational or customer-related barriers to completion.

The September decline should not be interpreted as a confirmed deterioration in performance without first validating whether September represents a complete reporting period.

---

# From Insight to Action

| Finding | Business Implication | Potential Action |
|---|---|---|
| ~52% of revenue comes from Santiago | Geographic concentration | Investigate and replicate Santiago's strongest revenue drivers |
| ~75% of revenue comes from Premium customers | High dependence on one customer segment | Prioritize retention and develop Regular-to-Premium opportunities |
| ~20% of order value is not completed | Potential unrealized revenue | Investigate pending-order causes and conversion barriers |
| August recorded peak revenue | Possible seasonal or commercial driver | Identify what changed during August |

---

## What I Would Analyze Next

This analysis identifies **where** revenue is concentrated but does not fully explain **why**.

The next analytical iteration would incorporate:

- Customer purchase frequency
- Customer retention
- Revenue per customer
- Product profitability
- Repeat purchase behavior
- Customer lifetime value
- Pending-order aging
- Month-over-month growth

These analyses would help move the project from descriptive reporting toward deeper diagnostic analysis.

---

## Tools & Skills Demonstrated

**Power BI**
- Interactive dashboard development
- KPI design
- Visual interactions
- Slicers and filtering

**Power Query**
- Data preparation
- Data type validation
- Transformation workflow

**DAX**
- Aggregation measures
- Filtered calculations
- Distinct customer calculations
- Ratio measures

**Analytics**
- Business question definition
- KPI selection
- Data modeling
- Business insight generation
- Decision-oriented recommendations
- Analytical limitation awareness

---

## Dataset

This project uses a **simulated dataset created for portfolio and analytical training purposes**.

No confidential customer, employer, or company data is included.

---

## Author

**Haniel Mendoza**

Junior Data Analyst  
SQL | Excel | Power BI | Data Cleaning | Reporting
