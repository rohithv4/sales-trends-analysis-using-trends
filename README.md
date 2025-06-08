# sales-trends-analysis-using-trends

🎯 Objective
Analyze monthly revenue and order volume trends over time.

🛠️ Tools
SQL-based RDBMS (PostgreSQL / MySQL / SQLite)

MySQL:

sql
Copy
Edit
SELECT
    DATE_FORMAT(order_date, '%Y-%m') AS month,
    COUNT(order_id) AS order_volume,
    SUM(total_amount) AS monthly_revenue
FROM orders
GROUP BY month
ORDER BY month;

| Month   | Order Volume | Monthly Revenue |
| ------- | ------------ | --------------- |
| 2023-01 | 120          | 15,000.00       |
| 2023-02 | 95           | 11,200.00       |
| 2023-03 | 130          | 17,800.00       |
| ...     | ...          | ...             |

📘 Dataset
Table: online_sales

Columns: order_date, amount, product_id

Table Schema
The online_sales table includes the following columns:

transaction_id (INT): Unique identifier for each transaction.
date (DATE): Date of the transaction.
product_category (VARCHAR): Category of the product sold.
product_name (VARCHAR): Name of the product.
units_sold (INT): Number of units sold.
unit_price (DECIMAL): Price per unit.
total_revenue (DECIMAL): Total revenue generated from the transaction.
region (VARCHAR): Sales region.
payment_method (VARCHAR): Payment method used.
![task6 1](https://github.com/user-attachments/assets/9c623a47-8e8b-418e-a240-800899ee977c)
![task6 2](https://github.com/user-attachments/assets/8996110a-4673-491a-a679-d4846e93c5a1)

