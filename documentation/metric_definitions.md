# Metric Definitions

Clear metric definitions are part of the analytical solution. This document records how the executive KPIs should be interpreted.

| Metric | Definition | Business meaning |
|---|---|---|
| Total Revenue | Sum of `Orders[total]` across all orders in the current filter context | Total order value represented in the dataset |
| Completed Revenue | Sum of `Orders[total]` for completed orders | Order value already associated with completed transactions |
| Total Orders | Count of orders | Transaction volume |
| Average Order Value | Average `Orders[total]` in the current filter context | Typical order value |
| Active Customers | Distinct customers represented in orders | Customers with order activity |
| Completed Revenue % | Completed Revenue divided by Total Revenue | Share of total order value associated with completed orders |

## Important naming note

The dashboard currently displays **Completion Rate**. Because the 79.6% KPI is based on revenue value rather than the number of completed orders, the more precise business label is **Completed Revenue %**.

A true **Order Completion Rate** would instead be defined as:

`Completed Orders / Total Orders`

Keeping these definitions separate prevents a stakeholder from interpreting a revenue-share metric as an order-count metric.

## Revenue source

For this case study, `Orders[total]` is the authoritative source for revenue KPIs. Product-line totals should not be presented as reconciled revenue unless they are independently validated against the order totals.