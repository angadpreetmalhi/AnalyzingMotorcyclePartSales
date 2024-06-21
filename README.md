# AnalyzingMotorcyclePartSales
# Unicorns Analysis

This repository contains SQL queries and Python visualizations for analyzing the sales data of a company selling motorcycle parts. The goal is to calculate the net revenue for each product line, grouped by month and warehouse, filtered to include only "Wholesale" orders.

## SQL Queries

The SQL queries used in this analysis can be found in the `sql/` directory.

## Visualizations

The visualizations generated from the analysis can be found in the `visualizations/` directory.

## Analysis

The analysis was performed using the data from the `sales` table, which contains the following columns:
- `order_number`: Unique order number.
- `date`: Date of the order (June to August 2021).
- `warehouse`: The warehouse where the order was made (North, Central, West).
- `client_type`: Type of order (Retail or Wholesale).
- `product_line`: Type of product ordered.
- `quantity`: Number of products ordered.
- `unit_price`: Price per product (dollars).
- `total`: Total price of the order (dollars).
- `payment`: Payment method (Credit card, Transfer, Cash).
- `payment_fee`: Percentage of total charged as a result of the payment method.

## Running the Analysis

To run the analysis and generate the visualizations, open the `unicorns_analysis.ipynb` Jupyter notebook and execute the cells.

