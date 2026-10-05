# AI-Assisted E-Commerce Performance & Customer Intelligence — Power BI

## Project Overview
An AI-assisted Power BI business intelligence project using the Olist Brazilian E-Commerce Public Dataset. The project analyzes sales, products, sellers, customer retention, delivery performance, and customer experience through an interactive four-page dashboard.

**Workflow:** Data → Analytical Model → DAX → Business Questions → Findings → Recommendations → Decision Support

## AI-Assisted Analytics
AI was used as an analytical co-pilot for business-question formulation, Power BI data-model design, DAX development and debugging, metric validation, dashboard design, analytical interpretation, and recommendation development. Calculations were implemented in Power BI and validated against SQL results where definitions aligned.

This project does **not** claim to contain a machine-learning model, predictive model, or embedded AI agent.

## Dashboard Pages
### 1. Executive Overview
KPIs: Total Orders, Total Product Sales, Total Customers, Delivery Rate.  
Analysis: monthly sales trend, top categories by sales, non-delivered orders by status, top customer states by sales.

### 2. Sales & Product Performance
KPIs: Total Items Sold, Total Product Sales, Average Item Price, Total Freight.  
Analysis: top sellers, top categories by items sold, average item price by category, seller-state freight.

### 3. Customer Intelligence
KPIs: Total Customers, Repeat Customers, One-Time Customers, Repeat Purchase Rate.  
Analysis: customers by state, repeat vs one-time customers, orders per customer, repeat purchase rate by state.

### 4. Delivery & Customer Experience
KPIs: Average Delivery Days, On-Time Delivery Rate, Late Orders, Average Review Score.  
Analysis: delivery trend, review distribution, review score by state, late-delivery rate by state.

## Key Findings
| Area | Finding |
|---|---|
| Overall | R$13.59M product sales across 99,441 orders and 96,096 unique customers |
| Sales peak | November 2017 had the highest monthly product sales in the observed period |
| Retention | 93,099 one-time customers vs 2,997 repeat customers |
| Repeat rate | 3.12% |
| Delivery | 97.02% of orders were delivered |
| On-time delivery | 91.89% among eligible delivered orders |
| Late delivery | 7,826 orders classified as late using the Power BI definition |
| Satisfaction | Average review score 4.09/5 |
| Positive reviews | 77.07% rated 4 or 5 |
| Low-rated reviews | 14,575 rated 1 or 2 |
| Geographic delivery | BA, RJ and ES showed relatively higher late-delivery rates among states analyzed |
| Geographic satisfaction | Observed state-level average review scores ranged approximately 3.9–4.2/5 |

See [Business Questions & Findings](Documentation/Business-Questions-and-Findings.md) for the complete analysis.

## Tools & Technologies
- Power BI
- DAX
- MySQL
- SQL
- Olist Brazilian E-Commerce Public Dataset
- AI-assisted analytics

## Key Power BI / DAX Concepts
Data modeling, fact/dimension tables, relationships, measures, filter context, `CALCULATE`, `FILTER`, `DISTINCTCOUNT`, `DIVIDE`, `AVERAGEX`, `RANKX`, `KEEPFILTERS`, `SAMEPERIODLASTYEAR`, `DATEADD`, continuous calendar table, KPI development, interactive slicers, cross-page slicer synchronization, and business-focused dashboard design.

## Data Model
Dimensions: `dim_customer`, `dim_product`, `dim_seller`, `dim_calendar`  
Facts: `fact_orders`, `fact_order_items`, `fact_payments`, `fact_reviews`

See [Data Model](Documentation/Data-Model.md).

## Validation
| Metric | Result |
|---|---:|
| Total Orders | 99,441 |
| Total Customers | 96,096 |
| Total Product Sales | R$13.59M |
| Repeat Customers | 2,997 |
| Repeat Purchase Rate | 3.12% |
| Delivered Orders | 96,478 |
| Delivery Rate | 97.02% |
| Average Delivery Days | 12.50 |
| Average Review Score | 4.09/5 |

## Limitations
- Product sales use `fact_order_items[price]`; profit is not calculated.
- On-time delivery rate uses delivered orders with valid delivery-date information.
- Eight delivered orders were outside the on-time/late calculation because required delivery-date information was missing.
- The final observed period is incomplete/sparse.
- Some geographic findings are based on the major/top states displayed.
- The analysis identifies patterns and investigation areas; it does not claim causation.
- Delivery performance versus customer satisfaction was not analyzed as a dedicated comparison.

## Repository Structure
```text
AI-Assisted-E-Commerce-Performance-Customer-Intelligence-PowerBI/
├── README.md
├── PowerBI/
│   └── E-Commerce-Performance-Customer-Intelligence.pbix
├── Screenshots/
│   ├── Customer Intelligence.png
│   ├── Delivery and Customer Experience.png
│   ├── Executive Overview.png
│   └── Sales And Product Performance.png
├── Documentation/
│   ├── Business-Questions-and-Findings.md
│   └── Data-Model.md
└── Data/
    └── README.md
```
