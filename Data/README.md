# Dataset

## Source
This project uses the **Olist Brazilian E-Commerce Public Dataset**.

The raw dataset is not stored in this repository.

## Data Handling
The Power BI model uses prepared analytical tables from the SQL-based analytical workflow and MySQL database rather than directly loading the raw CSV files.

Analytical tables include:
- `dim_customer`
- `dim_date`
- `dim_product`
- `dim_seller`
- `fact_orders`
- `fact_order_items`
- `fact_payments`
- `fact_reviews`

A continuous `dim_calendar` table was created in Power BI for time-intelligence analysis.

## Original Dataset
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

The raw dataset is not redistributed in this repository.
