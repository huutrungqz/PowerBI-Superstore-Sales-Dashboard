# Power BI Superstore Sales Dashboard

## Project Overview

This project analyzes Superstore sales performance using Power BI to identify trends in revenue, profitability, customer behavior, and regional performance.

The dashboard enables stakeholders to monitor business KPIs, evaluate sales efficiency, and support data-driven decision-making through interactive visual analytics.

---

## Business Objectives

- Monitor overall sales and profitability performance
- Identify top-performing regions and product categories
- Analyze customer purchasing behavior
- Evaluate return rates and profit margins
- Track year-over-year business growth trends

---

## Tools & Technologies

- Power BI
- Power Query
- DAX
- Excel

---

## Data Preparation

The dataset was cleaned and transformed using Power Query before building the data model and visualizations.

Data preparation tasks included:

- Handling missing values
- Formatting date fields
- Creating calculated columns
- Building relationships between tables
- Optimizing the data model

---

## Key KPIs

- **Total Revenue**
- **Total Profit**
- **Profit Margin**
- **Return Rate**
- **Total Customers**
- **Average Revenue per Customer**
- **Revenue Growth YoY**
- **Profit Margin Growth YoY**

---

## Dashboard Features

- Interactive slicers and filters
- Regional sales performance analysis
- Product category comparison
- Customer segmentation metrics
- Time-series trend analysis
- Profitability and return analysis
- Dynamic KPI cards and charts

---

## Sample DAX Measures

### Total Revenue

```DAX
Total Revenue =
SUM(Orders[Sales])
```

### Total Profit Margin

```DAX
Total Profit Margin =
SUM(Orders[Profit]) / SUM(Orders[Sales])
```

### Revenue %YoY

```DAX
Revenue %YoY =
VAR CurrentRevenue = [Total Revenue]
VAR PreviousRevenue =
    CALCULATE(
        [Total Revenue],
        SAMEPERIODLASTYEAR(Date[Date])
    )
RETURN
DIVIDE(CurrentRevenue - PreviousRevenue, PreviousRevenue)
```

### Return Rate

```DAX
Return Rate =
DIVIDE(
    COUNTROWS(Returns),
    COUNTROWS(Orders)
)
```

### Avg Revenue per Customer

```DAX
Avg Revenue per Customer =
DIVIDE([Total Revenue], [Total Customer])
```

---

## Dashboard Preview

![Dashboard Preview](assets/images/dashboard.png)

---

## Key Insights

- **Technology products** generated the highest revenue contribution
- Certain categories showed ***high sales but low profitability***
- **West region** achieved the strongest overall sales performance
- Return rates negatively impacted profitability in several product segments
- Revenue growth increased significantly during peak seasonal periods

---

## Skills Demonstrated

- Data Cleaning & Transformation
- Data Modeling
- DAX Calculations
- Time Intelligence
- KPI Analysis
- Business Intelligence Reporting
- Data Visualization
- Customer Analytics

---

## Repository Structure

```text
.
├── reports/
│   └── PowerBI-Superstore-Sales-Dashboard.pbix
├── assets/
│   └── images/
│       └── dashboard.png
├── docs/
├── README.md
```

---

## Author

Trung Nguyen
