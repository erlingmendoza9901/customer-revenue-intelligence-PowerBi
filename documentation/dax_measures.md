# DAX Measure Reference

This file documents the core measures used or recommended for the executive layer of the report. Table and column names follow the model used in the project.

```DAX
Total Revenue =
SUM(OrdersTable[total])
```

```DAX
Completed Revenue =
CALCULATE(
    [Total Revenue],
    OrdersTable[estado] = "Completada"
)
```

```DAX
Total Orders =
COUNT(OrdersTable[order_id])
```

```DAX
Average Order Value =
AVERAGE(OrdersTable[total])
```

```DAX
Active Customers =
DISTINCTCOUNT(OrdersTable[customer_id])
```

```DAX
Completed Revenue % =
DIVIDE(
    [Completed Revenue],
    [Total Revenue],
    0
)
```

## Optional order-count KPI

If management wants to measure transaction completion rather than revenue realization, keep it as a separate KPI:

```DAX
Completed Orders =
CALCULATE(
    [Total Orders],
    OrdersTable[estado] = "Completada"
)
```

```DAX
Order Completion Rate =
DIVIDE(
    [Completed Orders],
    [Total Orders],
    0
)
```

## Why the distinction matters

`Completed Revenue %` answers **“What share of order value is associated with completed transactions?”**

`Order Completion Rate` answers **“What share of orders are completed?”**

They can produce different percentages and should never share the same business label.