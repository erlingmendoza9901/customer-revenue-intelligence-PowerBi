# Customer Revenue Intelligence

### From Transactions to Business Decisions | Power BI Case Study

> **$2.32M in revenue looks healthy — until you ask where that revenue actually comes from.**

This project was built to answer a management question rather than simply produce another sales dashboard:

> **What is driving revenue performance, where is the business concentrated, and where should management investigate next?**

The analysis uses Power BI, Power Query, DAX, and relational data modeling to move from transaction-level data to an executive view of revenue concentration, customer value, geographic performance, order status, and monthly trends.

**Portfolio note:** The dataset is simulated and contains no confidential customer, employer, or company information.

---

## The Decision Problem

A headline revenue number does not tell management whether performance is diversified, sustainable, or fully realized. This case study therefore focuses on four decision areas:

- **Revenue concentration** — Is performance overly dependent on one geography or customer segment?
- **Customer value** — Which customer groups generate the most value?
- **Revenue realization** — How much order value is completed versus still pending?
- **Trend diagnostics** — When does performance change, and what should be investigated next?

---

## Executive Overview

The report provides an interactive management view of Total Revenue, Completed Revenue, Total Orders, Average Order Value, Active Customers, Completed Revenue %, monthly trends, geographic performance, customer segments, and order status. City and customer-segment slicers allow stakeholders to move from the company view into specific commercial segments.

> **Dashboard asset pending final export:** `images/01_executive_overview.png`

---

## Analytical Model

The solution is structured around five analytical tables: **Customers, Orders, Order Details, Products, and Calendar**. The model separates transactional data from descriptive dimensions so measures can be analyzed consistently across customers, geography, segments, products, and time.

For this case study, **order-level total is the authoritative revenue measure**. Product-line values are not presented as reconciled revenue unless independently validated against order totals.

> **Model asset pending final export:** `images/02_data_model.png`

---

## Data Preparation

Power Query was used for structured Excel imports, data-type validation, categorical-field review, date validation, and analysis-ready transformations.

A meaningful modeling issue occurred when the date fields did not load reliably. The Calendar and Orders date keys were corrected to compatible **Date** types, restoring the model load. Month labels were then sorted using month number so the trend displays January through September chronologically instead of alphabetically.

This project therefore documents not only the finished visuals, but the data-quality and modeling decisions required to make the report trustworthy.

---

## DAX & Metric Semantics

The report uses reusable measures for revenue, completed revenue, order volume, average order value, active customers, and completed revenue share.

A key analytical distinction is explicit:

**Completed Revenue % = Completed Revenue / Total Revenue**

The current value of approximately **79.6%** describes the share of *revenue value* associated with completed orders. It is not an order-count completion rate. A true **Order Completion Rate** would use `Completed Orders / Total Orders`.

Technical references:

- [`DAX Measure Reference`](documentation/dax_measures.md)
- [`Metric Definitions`](documentation/metric_definitions.md)

---

# Key Business Insights

## 1. Santiago is the main revenue engine — and a concentration point

Santiago generated approximately **$1.20M of $2.32M in total revenue**, accounting for roughly **52% of overall sales**. The result identifies Santiago as the strongest-performing market, but it also exposes meaningful geographic concentration.

**Decision opportunity:** Investigate the customer and purchasing patterns behind Santiago's performance and test whether those patterns can be replicated in Santo Domingo and La Vega.

**Next question:** What differentiates Santiago customers from customers in the other markets?

---

## 2. Premium customers dominate revenue

The Premium segment generated approximately **$1.74M**, or roughly **75% of total revenue**. Regular customers generated approximately **$0.51M**, while Basic customers contributed approximately **$0.07M**.

This makes Premium customers the primary revenue engine while also revealing dependence on a single customer segment.

**Decision opportunity:** Protect Premium customer retention and identify Regular customers whose purchasing behavior suggests potential to develop into higher-value customers.

**Next question:** Which Regular customers behave most like the current Premium population?

---

## 3. Pending orders represent a measurable revenue opportunity

Approximately **79.6% of total order value is associated with completed orders**, leaving roughly **$0.47M associated with pending orders**.

Pending value is an opportunity to investigate, not automatically recoverable revenue: the current dataset does not establish why those transactions remain pending.

**Decision opportunity:** Analyze pending-order aging and the operational or customer factors associated with non-completion.

**Next question:** How long do orders remain pending, and what characteristics are associated with those orders?

---

## Time Trend: An Observation, Not a Causal Claim

August recorded the highest monthly revenue in the available period at approximately **$0.37M**. September is lower, but the decline should **not** be interpreted as evidence of deteriorating performance until the reporting period is confirmed to be complete.

That distinction is intentional: the dashboard shows what happened; additional data is required to explain why it happened.

---

## From Insight to Decision

| Evidence | Business implication | Management investigation |
|---|---|---|
| ~52% of revenue comes from Santiago | Geographic concentration | Identify Santiago's strongest customer and purchasing patterns |
| ~75% comes from Premium customers | Customer-value concentration | Protect retention and identify Regular-to-Premium opportunities |
| ~20% of order value is not completed | Potential unrealized value | Diagnose pending-order aging and barriers |
| August records the period's peak | Possible commercial or timing driver | Determine what changed during August before attributing causality |

---

## What I Would Analyze Next

The current solution is intentionally strongest at **descriptive analysis**: it establishes where performance is concentrated. The next iteration moves toward diagnostic customer intelligence with revenue per customer, purchase frequency, repeat behavior, retention, segment migration, pending-order aging, month-over-month growth, and product profitability once line-level revenue and cost data are validated.

This roadmap prevents the project from presenting conclusions that the current dataset cannot support.

---

## Technical Evidence

**Power BI** — executive dashboard design, interactive filtering, KPI reporting, visual interactions  
**Power Query** — import workflow, data preparation, type validation, date handling  
**DAX** — aggregation, filtered measures, distinct-customer measures, ratio measures  
**Data Modeling** — fact/dimension relationships, calendar relationship, metric-grain awareness  
**Business Analysis** — business questions, KPI definitions, insight-to-action reasoning, analytical limitations

Project documentation:

- [`Business Insights Memo`](documentation/business_insights.md)
- [`Metric Definitions`](documentation/metric_definitions.md)
- [`DAX Measure Reference`](documentation/dax_measures.md)
- [`Analytical Journey`](documentation/analytical_journey.md) — what was learned, debugged, and what is being developed next

---

## Target Repository Structure

```text
customer-revenue-intelligence-PowerBi/
├── README.md
├── dashboard/
│   └── Customer_Revenue_Intelligence.pbix
├── data/
│   └── customer_sales_dataset.xlsx
├── images/
│   ├── 01_executive_overview.png
│   └── 02_data_model.png
└── documentation/
    ├── analytical_journey.md
    ├── business_insights.md
    ├── dax_measures.md
    └── metric_definitions.md
```

The report file, source data, screenshots, and analytical documentation are separated so a reviewer can quickly inspect either the finished solution or the reasoning behind it.

---

## Dataset & Limitations

This project uses a **simulated dataset created for portfolio and analytical training purposes**. No confidential customer, employer, or company data is included.

The current analysis should be interpreted as descriptive rather than causal. Additional customer-behavior, profitability, retention, and operational data would be required to establish the causes behind the observed patterns.

---

## About the Analyst

**Haniel Mendoza**  
Junior Data Analyst  
**SQL · Excel · Power BI · Data Cleaning · Reporting**

This project is part of a broader portfolio focused on solving business questions with structured analysis rather than reproducing generic dashboard templates.