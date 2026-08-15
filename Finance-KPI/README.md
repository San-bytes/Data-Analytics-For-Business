# Finance KPI Dashboard

## Project Overview

The **Finance KPI Dashboard** is an interactive Power BI dashboard developed to analyze financial performance by comparing **budgeted amounts with actual spending**.

The dashboard provides a consolidated view of budget performance, transaction activity, category-wise variance, departmental and regional spending, and payment-method distribution. Interactive filters allow users to explore the data at different levels of detail.

## Problem Statement

Management needs a clear and interactive way to monitor financial performance, identify budget overruns, track transaction activity, and understand how actual spending is distributed across departments, regions, categories, and payment methods.

The objective of this project is to develop a **Finance KPI Dashboard in Power BI** that supports financial monitoring and data-driven decision-making.

## Project Files

```text
Finance-KPI/
│
├── Finance.pbix
├── Exp7-report.pdf
└── README.md
```

* **Finance.pbix** – Power BI dashboard containing the data, DAX measures, visuals, and interactive filters.
* **Exp7-report.pdf** – Experiment report documenting the dashboard development and analysis.
* **README.md** – Project documentation.

## Dashboard Features

### KPI Cards

The dashboard displays four key financial indicators:

* **Total Budget**
* **Total Actual**
* **Total Transactions**
* **Budget Variance**

### Budget Utilization Gauge

The gauge compares actual spending against the available budget and indicates whether expenditure is within or above the planned budget.

### Yearly Budget vs Actual

A combination chart compares **Budget Amount** and **Actual Amount** across the available years (2021–2023).

### Monthly Transaction Trend

An area chart displays the **count of Transaction IDs by month**, helping identify changes in transaction activity throughout the year.

### Budget Variance by Category

A waterfall chart shows how different financial categories contribute to the overall budget variance.

### Department × Region Analysis

A matrix provides a detailed view of actual amounts across departments and regions.

### Payment Method Analysis

A donut chart shows the distribution of actual financial amounts across different payment methods:

* UPI
* Card
* Bank Transfer
* Cash

### Interactive Filters

The dashboard includes interactive controls for:

* **Department**
* **Region**
* **Date**

Selecting a filter dynamically updates the connected dashboard visuals.

## DAX Measures

### Total Budget

```DAX
Total Budget = SUM('Sheet1'[Budget Amount])
```

Calculates the total budgeted amount.

### Total Actual

```DAX
Total Actual = SUM('Sheet1'[Actual Amount])
```

Calculates the total actual amount.

### Budget Variance

```DAX
Budget Variance = SUM(Sheet1[Actual Amount]) - SUM(Sheet1[Budget Amount])
```

Calculates the difference between actual spending and the budget.

* Positive value → Actual spending is higher than budget.
* Negative value → Actual spending is lower than budget.

### Budget Utilization %

```DAX
Budget Utilization % = DIVIDE([Total Actual],[Total Budget],0)
```

Measures actual expenditure relative to the total budget.

## Key Dashboard Results

With no specific department or region filter applied, the dashboard displays approximately:

* **Total Budget:** 796M
* **Total Actual:** 891M
* **Total Transactions:** 10.007K
* **Budget Variance:** 95M
* **Budget Utilization:** approximately 112%

The overall actual expenditure is higher than the allocated budget, indicating an overall budget overrun.

## Interactive Analysis

### Department – HR

When **HR** is selected:

* **Total Budget:** 137M
* **Total Actual:** 156M
* **Budget Variance:** approximately 18M
* **Budget Utilization:** approximately 113%

This indicates that HR actual expenditure is higher than its allocated budget.

### Region – Central

When **Central** is selected:

* **Total Budget:** 26M
* **Total Actual:** 31M
* **Total Transactions:** 343
* **Budget Variance:** approximately 4M
* **Budget Utilization:** approximately 116%

This provides a focused view of financial activity within the Central region.

## Business Insights

* Actual expenditure is higher than the overall allocated budget.
* Budget utilization above 100% indicates that actual spending has exceeded planned spending.
* Category-level variance analysis helps identify areas contributing to the overall financial variance.
* The department-region matrix provides a detailed view of where actual spending is distributed.
* Payment-method analysis helps understand how financial transactions are distributed across different payment channels.
* Monthly transaction trends help identify periods with higher or lower transaction activity.
* Interactive filters allow users to move from an overall financial view to focused departmental or regional analysis.

## Conclusion

The Finance KPI Dashboard provides an interactive view of organizational financial performance. It combines KPIs, budget-versus-actual analysis, variance analysis, transaction trends, departmental and regional analysis, and payment-method distribution in a single dashboard.

The interactive filtering capability makes it possible to investigate specific departments and regions, identify areas of overspending, and support more informed financial monitoring and decision-making.

