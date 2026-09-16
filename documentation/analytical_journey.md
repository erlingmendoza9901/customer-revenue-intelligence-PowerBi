# Analytical Journey

## Why this section exists

This case study is also evidence of an analyst-development process. The objective was not to start from a polished template; it was to work through the same kinds of decisions a junior analyst must make when turning raw business data into a report that stakeholders can trust.

## Skills demonstrated during the build

### 1. Business logic before visuals
The project was framed around revenue concentration, customer value, order completion, and trend analysis before dashboard design decisions were finalized. This keeps the report tied to management questions rather than chart selection.

### 2. Data-quality discipline
Raw data was treated as source evidence rather than something to overwrite casually. Data types, categorical fields, date keys, and model relationships were reviewed before relying on the visuals.

### 3. Debugging the model
A meaningful issue appeared when date fields did not load reliably. The Calendar and Orders date keys were corrected to compatible Date types, which restored the model load. Month names were then sorted by month number to preserve chronological order.

### 4. Metric-definition discipline
The build exposed an important KPI-definition lesson: a ratio of Completed Revenue / Total Revenue is not the same as Completed Orders / Total Orders. The project therefore documents the revenue-based metric as **Completed Revenue %** and keeps a separate definition for a true order completion rate.

### 5. Analytical interpretation
The report moved beyond statements such as “Santiago is highest” by connecting evidence to business implications, decision opportunities, and next questions. It also avoids treating the September decline as a confirmed negative trend without first checking whether the reporting period is complete.

## Current technical scope

This project demonstrates foundational-to-intermediate Power BI work appropriate for a developing Junior Data Analyst:

- Power Query preparation and type validation
- Relational modeling
- Basic reusable DAX measures
- Filter context through slicers and visual interactions
- KPI design
- Executive dashboard construction
- Business insight communication

It intentionally does **not** claim advanced DAX, advanced time intelligence, complex calculation groups, enterprise semantic-model administration, or causal analysis.

## Skills being developed next

The next iteration should deepen the analysis rather than duplicate the same dashboard with different colors or data. Priority areas are:

1. Customer-level analysis: revenue per customer, order frequency, repeat behavior
2. Time intelligence: month-over-month and period comparisons
3. More advanced DAX and filter-context reasoning
4. Diagnostic analysis of pending orders
5. Continued SQL analysis, including CTEs and later window functions
6. Continued Excel work with multi-criteria formulas, lookups, PivotTables, and Power Query

## Analyst principle

> A dashboard is not the analysis. The analysis is the chain from business question → validated data → defined metric → evidence → interpretation → decision opportunity → next question.

That principle is the standard used to evaluate future portfolio projects as well.