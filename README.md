# anushka_bitsom_ba_2511785_part4_tableau_dashboard
# Executive Sales Performance Dashboard
## Business Problem Summary
The leadership team requires an executive-level dashboard to monitor sales performance, profitability, customer behavior, category performance, shipping effectiveness, discount impact, and return patterns.
The objective is to identify business opportunities, operational risks, and actionable insights through interactive visual analysis.
---
## Dataset Description
Dataset File:
```textdata/dashboard_sales_data.xlsx```
The dataset contains information related to:
- Orders- Sales- Profit- Discounts- Returns- Regions- Categories- Customer Segments- Shipping Information- Order Dates
---
## Tableau Workbook Description
Workbook File:
```texttableau/executive_dashboard.twbx```
The workbook contains:
- Executive Dashboard- Sales Trend View- Regional Performance View- Category Profitability View- Customer Segment View- Shipping Performance View- Discount vs Profit View- Return Analysis View- KPI Sheets
---
## Calculated Fields Created
### 1. Profit Margin
```textProfit / Sales```
Purpose:Measures profitability generated from each sales dollar.
---
### 2. Cost
```textSales - Profit```
Purpose:Estimates operational cost associated with sales.
---
### 3. Average Order Value
```textSUM([Sales]) / COUNTD([Order ID])```
Purpose:Measures average revenue generated per order.
---
### 4. Return Rate
```textSUM([Return Flag]) / COUNTD([Order ID])```
Purpose:Measures percentage of returned orders.
---
### 5. Shipping Delay Bucket
```textIF [Delivery Days] <= 2 THEN "Fast"ELSEIF [Delivery Days] <= 5 THEN "Normal"ELSE "Delayed"END```
Purpose:Classifies delivery performance.
---
### Additional Calculated Fields
#### Sales Category
Classifies sales into performance buckets.
#### Profit Category
Classifies profitability into performance buckets.
---
## Dashboard Components
### KPI Cards
- Total Sales- Total Profit- Return Rate
### Visualizations
- Sales Trend View- Regional Performance View- Category Profitability View- Customer Segment View- Shipping Performance View- Discount vs Profit View- Return Analysis View
---
## Filters and Interactions Used
Dashboard Filters:
- Region- Category- Customer Segment- Ship Mode- Order Date
All filters are applied across the dashboard using the shared data source.
Dashboard interactions allow dynamic exploration of business performance.
---
## Key Business Insights
1. Sales remain relatively stable over time.2. South region generates the highest profitability.3. Copiers, Accessories, and Phones are major profit drivers.4. Several sub-categories generate significantly lower profits.5. Return activity is concentrated within specific categories.6. High discounts reduce profitability.7. Customer segments demonstrate different performance patterns.8. Revenue concentration creates both opportunity and risk.
---
## Dashboard Story Summary
The dashboard highlights strong overall business performance while identifying opportunities to expand profitable categories and reduce operational risks.
Key risks include high return rates and profit erosion from excessive discounting.
The dashboard supports leadership decision-making through interactive analysis and KPI monitoring.
---
## Assumptions and Limitations
### Assumptions
- Data quality is accurate and complete.- Return Flag correctly identifies returned orders.- Delivery Days accurately represent shipping duration.
### Limitations
- Dashboard focuses on historical performance.- External market conditions are not included.- Customer satisfaction metrics are unavailable.
---
## Screenshots Included
```textscreenshots/├── full_dashboard.png├── sales_trend_view.png├── regional_performance_view.png├── category_profitability_view.png└── filter_interaction_view.png```
---
## Repository Structure
```textpart4_tableau_dashboard/├── data/│ └── dashboard_sales_data.xlsx├── tableau/│ └── executive_dashboard.twbx├── outputs/│ ├── dashboard_story.md│ ├── business_insights.md│ └── chart_selection_justification.md├── screenshots/│ ├── full_dashboard.png│ ├── sales_trend_view.png│ ├── regional_performance_view.png│ ├── category_profitability_view.png│ └── filter_interaction_view.png└── README.md```
