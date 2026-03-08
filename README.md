# Zepto-Project
# Zepto Inventory Data Analysis (SQL Project)

## Project Overview

This project analyzes an e-commerce inventory dataset from Zepto using
SQL and PostgreSQL. The goal is to perform data cleaning, exploratory
data analysis (EDA), and generate business insights related to product
pricing, discounts, and stock availability.

## Dataset

The dataset contains product inventory information scraped from Zepto's
online store and sourced from Kaggle.

Each row represents a unique product SKU.

Columns included: - sku_id - product name - category - mrp (Maximum
Retail Price) - discountPercent - discountedSellingPrice -
availableQuantity - weightInGms - outOfStock - quantity

## Tools Used

-   SQL
-   PostgreSQL
-   pgAdmin
-   CSV Dataset

## Database Schema

``` sql
CREATE TABLE zepto (
  sku_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);
```

## Key Analysis

The following analysis was performed using SQL queries:

-   Top 10 products with the highest discount
-   Category-wise product distribution
-   Products that are currently out of stock
-   Average price per product category
-   High-value products with minimal discounts
-   Inventory availability across categories

## Example SQL Query

``` sql
SELECT name, category, discountPercent
FROM zepto
ORDER BY discountPercent DESC
LIMIT 10;
```

## Project Structure

    zepto-sql-data-analysis
    │
    ├── zepto_v2.csv
    ├── create_table.sql
    ├── analysis_queries.sql
    └── README.md

## Conclusion

This project demonstrates practical SQL skills including data cleaning,
data exploration, and business-driven analysis on a real-world
e-commerce dataset.
