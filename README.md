# Retail Sales Analysis using SQL

A beginner-friendly SQL project that cleans, explores, and analyzes retail sales data to answer common business questions.

## Project Overview

- **Database:** `sql_project_p2`
- **Table:** `retail_sales`
- **SQL Dialect:** PostgreSQL
- **Skills Used:** Table creation, data cleaning, `GROUP BY`, aggregate functions, `CASE`, CTEs, subqueries, window functions

## Files

| File | Description |
|------|-------------|
| `sql_query_p1.sql` | All SQL queries (setup, cleaning, exploration, analysis) |
| `SQL_-_Retail_Sales_Analysis_utf_.csv` | Dataset used in the project |

## Dataset Columns

| Column | Type | Description |
|--------|------|-------------|
| `transaction_id` | INT | Unique ID of each transaction (primary key) |
| `sale_date` | DATE | Date of the sale |
| `sale_time` | TIME | Time of the sale |
| `customer_id` | INT | Unique ID of the customer |
| `gender` | VARCHAR | Gender of the customer |
| `age` | INT | Age of the customer |
| `category` | VARCHAR | Product category |
| `quantity` | INT | Number of units sold |
| `price_per_unit` | FLOAT | Price of one unit |
| `cogs` | FLOAT | Cost of goods sold |
| `total_sale` | FLOAT | Total sale amount |

## Project Steps

1. **Setup:** Create the database and the `retail_sales` table, then import the CSV.
2. **Data Cleaning:** Check for `NULL` values and delete incomplete records.
3. **Data Exploration:** Count total sales, unique customers, and product categories.
4. **Data Analysis:** Solve 10 business questions using SQL.

## Business Questions Solved

1. Retrieve all sales made on `2022-11-05`.
2. Retrieve all `Clothing` transactions with quantity of 4 or more in Nov 2022.
3. Calculate total sales for each category.
4. Find the average age of customers who bought from the `Beauty` category.
5. Find all transactions where `total_sale` is greater than 1000.
6. Count transactions made by each gender in each category.
7. Calculate the average sale for each month and find the best selling month in each year.
8. Find the top 5 customers based on total sales.
9. Find the number of unique customers in each category.
10. Count orders by shift (Morning < 12, Afternoon 12–17, Evening > 17).

## Sample Query

```sql
-- Top 5 customers by total sales
SELECT 
    customer_id,
    SUM(total_sale) AS total_sales
FROM retail_sales
GROUP BY 1
ORDER BY 2 DESC
LIMIT 5;
```

## How to Run

1. Install PostgreSQL and open pgAdmin (or any SQL client).
2. Create the database `sql_project_p2`.
3. Run the table creation script from `sql_query_p1.sql`.
4. Import `SQL_-_Retail_Sales_Analysis_utf_.csv` into the `retail_sales` table.
5. Run the cleaning, exploration, and analysis queries one by one.

## What I Learned

- Cleaning data by finding and removing `NULL` records
- Summarizing data with aggregate functions and `GROUP BY`
- Ranking results with window functions (`RANK() OVER`)
- Grouping data into time-based shifts using `CASE` and CTEs

## Author

**Arghyadeep**
B.Tech ECE, NIT Durgapur
