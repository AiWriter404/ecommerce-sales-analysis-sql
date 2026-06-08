# ecommerce-sales-analysis-sql
I have started analysis with SQL and today is my first analysis report create by SQL this results are matching with Python Outputs.
## Key Findings

- Total Records: 5,000
- Total Revenue: $5.1M+
- Electronics generated the highest revenue.
- Clothing ranked second in revenue generation.
- West region generated the highest sales revenue.
- Revenue distribution across regions was relatively balanced.
SQL Day 1 Report
Project Overview
This project analyzes an e-commerce sales dataset containing 5,000 transactions using SQL in MySQL Workbench. The objective was to validate business insights previously generated using Python and Pandas.

Dataset Summary

| Metric             |         Value |
| ------------------ | ------------: |
| Total Records      |         5,000 |
| Total Revenue      | $5,109,775.74 |
| Product Categories |             4 |
| Regions            |             4 |


Query 1: Total Records


SELECT COUNT(*)
FROM ecommerce_sales;

Result
5000

Insight
The dataset contains 5,000 sales transactions and was successfully imported into MySQL.

Query 2: Total Revenue
SELECT SUM(revenue)
FROM ecommerce_sales;

Result
5109775.74

Query 3: Revenue by Product Category
Results
| Category    |       Revenue |
| ----------- | ------------: |
| Electronics | $1,829,899.22 |
| Clothing    | $1,531,931.72 |
| Home        |   $982,083.92 |
| Beauty      |   $765,860.88 |


Insight
Electronics is the highest-performing category.
Clothing is the second strongest category.
Electronics and Clothing together generate most of the revenue.

Query 4: Revenue by Region
SELECT region,
       SUM(revenue)
FROM ecommerce_sales
GROUP BY region;

Results

| Region |       Revenue |
| ------ | ------------: |
| West   | $1,345,582.16 |
| North  | $1,281,508.45 |
| South  | $1,246,640.90 |
| East   | $1,236,044.23 |

Insight

West region generated the highest revenue.
Revenue distribution is balanced across all regions.
The business is not dependent on a single geographic market.

Conclusion
The SQL analysis successfully validated all key findings from the Python-based analysis. Aggregate functions and GROUP BY queries were used to identify revenue trends, top-performing product categories, and regional performance.


