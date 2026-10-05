# Data Model

## Dimensions
- `dim_customer` — customer attributes, unique customer identity, state
- `dim_product` — product attributes and English category
- `dim_seller` — seller attributes and location
- `dim_calendar` — continuous calendar used for time intelligence

## Fact Tables
- `fact_orders` — order-level transactions, status, delivery dates
- `fact_order_items` — product-line transactions, price, freight, seller
- `fact_payments` — order payment information
- `fact_reviews` — customer review scores and review information

## Main Relationships
```text
dim_customer[customer_key] 1 ─── 1 fact_orders[customer_key]

fact_orders[order_key] 1 ─── * fact_order_items[order_key]
fact_orders[order_key] 1 ─── * fact_payments[order_key]
fact_orders[order_key] 1 ─── * fact_reviews[order_key]

dim_product[product_key] 1 ─── * fact_order_items[product_key]
dim_seller[seller_key] 1 ─── * fact_order_items[seller_key]

dim_calendar[date_key] 1 ─── * fact_orders[purchase_date_key]
```

## Calendar
A continuous `dim_calendar` table was created for time-intelligence analysis. The primary active date relationship is `dim_calendar[date_key]` to `fact_orders[purchase_date_key]`.

## Core DAX Areas
Sales: Total Product Sales, Average Order Value, Average Item Price, Total Freight, Sales Contribution %, Product Rank, Seller Rank.

Customers: Total Customers, Repeat Customers, One-Time Customers, Repeat Purchase Rate, Orders per Customer.

Delivery: Delivered Orders, Delivery Rate, Average Delivery Days, On-Time Orders, On-Time Delivery Rate, Late Orders, Late Delivery Rate.

Customer Experience: Average Review Score, Positive Review Rate, Low-Rated Reviews, Low-Rated Review Rate.

Time Intelligence: Previous Year Sales, Sales YoY Growth %, Previous Month Sales, Sales MoM Growth %.

## Modeling Approach
The model separates descriptive attributes into dimensions and transactional events into fact tables, supporting reusable DAX measures and interactive filtering.

## Validation
Core Power BI metrics were compared with SQL results where underlying definitions aligned. Where definitions differed, the Power BI definition was documented rather than treating values as automatically interchangeable.
