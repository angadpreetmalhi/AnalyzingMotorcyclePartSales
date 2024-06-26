# AnalyzingMotorcyclePartSales

This repository contains SQL queries for analyzing the sales data of a company selling motorcycle parts. The goal is to calculate the net revenue for each product line, grouped by month and warehouse, filtered to include only "Wholesale" orders.

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

```sql
SELECT 
    product_line,
    TO_CHAR(date, 'Month') AS month,
    warehouse,
    (SUM(total) - SUM(payment_fee)) AS net_revenue
FROM 
    sales
WHERE 
    client_type = 'Wholesale'
GROUP BY 
    product_line, month, warehouse
ORDER BY 
    product_line, month, net_revenue DESC;

