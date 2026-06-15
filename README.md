# Retail-Analytics-Databricks-PowerBI
# Retail Analytics Platform using Databricks and Power BI

## Project Overview

Developed an end-to-end Retail Analytics Platform using the Olist Brazilian E-commerce dataset. The solution follows the Medallion Architecture pattern (Bronze, Silver, Gold) using Databricks Delta Lake and Power BI for business reporting.

The objective of the project is to transform raw e-commerce data into business-ready analytical datasets and provide insights into sales, customers, products, sellers, and reviews.


## Architecture

Olist Dataset
↓
Bronze Layer
↓
Silver Layer
↓
Gold Layer
↓
Power BI Dashboard

### Technologies Used

* Databricks
* PySpark
* Spark SQL
* Delta Lake
* Power BI
* Star Schema
* Medallion Architecture


## Dataset

Dataset: Olist Brazilian E-Commerce Dataset

Files Used:

* customers
* orders
* order_items
* products
* payments
* reviews
* sellers


## Bronze Layer

Purpose:
Store raw source data without modifications.

Activities:

* Loaded CSV files into Databricks
* Created Delta tables
* Preserved original source data

Tables:

* bronze.customers
* bronze.orders
* bronze.order_items
* bronze.products
* bronze.payments
* bronze.reviews
* bronze.sellers


## Silver Layer

Purpose:
Clean and standardize data.

Transformations:

* Removed duplicates
* Converted date columns to timestamp
* Handled missing values
* Applied business validation rules
* Segregated invalid records

Data Quality Rules:

* Payment value > 0
* Review score between 1 and 5

Tables:

* silver.customers
* silver.orders
* silver.order_items
* silver.products
* silver.payments
* silver.reviews
* silver.sellers


## Gold Layer

Purpose:
Create business-ready analytical models.

### Dimension Tables

* dim_customers
* dim_products
* dim_sellers
* dim_date

### Fact Table

* fact_orders

### Aggregated Tables

* sales_summary
* customer_summary
* product_summary


## Star Schema Design

Fact Table:

* fact_orders

Dimensions:

* dim_customers
* dim_products
* dim_sellers
* dim_date

This model enables efficient analytical reporting and Power BI visualization.


## Delta Lake Features Implemented

### MERGE

Implemented incremental loading using Delta Lake MERGE operations to update existing records and insert new records.

### Time Travel

Used Delta Lake Time Travel to access historical versions of tables for auditing and recovery.

### OPTIMIZE

Optimized Delta tables to reduce small-file problems and improve query performance.

### VACUUM

Removed obsolete files and reduced storage consumption.


## Workflow Automation

Created Databricks Workflow Jobs to automate:

Bronze Load
↓
Silver Transformation
↓
Gold Transformation

Scheduling can be configured for daily or hourly execution.


## Power BI Dashboard

### Executive Dashboard

KPIs:

* Total Revenue
* Total Orders
* Total Customers
* Average Order Value
* Average Review Score

### Customer Analytics

* Customer Distribution
* Top Customers
* State-wise Analysis

### Product Analytics

* Revenue by Category
* Best Selling Products

### Seller Analytics

* Seller Performance
* Revenue by Seller

### Review Analytics

* Rating Distribution
* Average Review Score


## Business Outcomes

* Improved visibility into sales performance.
* Enabled customer and product analytics.
* Demonstrated enterprise-grade Medallion Architecture.
* Implemented Delta Lake best practices.
* Delivered interactive business dashboards.


## Resume Highlights

* Built an end-to-end Retail Analytics Platform using Databricks and Power BI.
* Implemented Bronze, Silver, and Gold layers using Delta Lake.
* Designed a Star Schema data warehouse with Fact and Dimension tables.
* Developed incremental data loading using Delta MERGE.
* Utilized Time Travel, OPTIMIZE, and VACUUM for data management.
* Created interactive dashboards for sales, customer, product, and seller analytics.
