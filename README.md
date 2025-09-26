# ZEPTO-Inventory-Analysis-with-PostgreSQL
This project provides a detailed analysis of a ZEPTO inventory dataset using PostgreSQL. The goal was to extract meaningful insights from the data, such as product performance, inventory valuation, and stock management. The analysis was conducted by writing and executing a series of SQL queries.

# Project Files
ZEPTO (DATASET).csv: The raw dataset containing detailed information on products, including category, price, weight, and stock status.

ZEPTO(QUERIES).sql: A complete set of SQL queries used for data exploration and analysis. This file includes the table creation statement and all the queries that were executed to derive the insights.

ZEPTO (INSIGHTS Q&A).pdf: A summary of the key findings, including the approach and insights for each question posed.

# Tools and Technologies Used
PostgreSQL: A powerful, open-source relational database system used for storing and querying the data.

Kaggle: The platform from which the dataset was sourced.

SQL (Structured Query Language): The language used to interact with the database and perform all data analysis.

# Key Insights and Methodology
The project followed a methodical approach to answer specific business questions about the inventory. Here's a brief overview of the key findings and the SQL techniques used to get them.

1. Top 10 Best-Value Products
Objective: To identify products with the highest discount percentage, providing insights into promotional strategies.

Methodology:

Products were filtered to find unique entries.

They were then sorted in descending order of discountPercent.

The results were limited to the top 10 to highlight the best deals.

Insight: The highest discounts were often applied to a wide variety of products, from snacks like wafers to food essentials, suggesting a strategy to attract customers across different categories.

2. Products with High MRP but Out of Stock
Objective: To find high-value products that are currently unavailable, which could indicate a potential revenue loss.

Methodology:

The query filtered for products where outOfStock was TRUE.

A condition was added to select only those with a mrp greater than a specific threshold.

The results were sorted by mrp to highlight the most expensive out-of-stock items.

Insight: This analysis revealed critical stock management issues, identifying high-demand items that are not in stock and are likely being missed by customers.

3. Estimated Revenue for Each Category
Objective: To calculate the potential revenue contribution of each product category.

Methodology:

The SUM() aggregate function was used to calculate the total revenue by multiplying discountedSellingPrice with availableQuantity.

Results were grouped by category and ordered to see which categories contribute the most or least to the total revenue.

Insight: This provided a clear picture of which product categories drive the most revenue for the business, highlighting the importance of categories like Munchies and Cooking Essentials.

4. Inventory Weight and Logistics
Objective: To calculate the total physical weight of the inventory by category, which is crucial for logistics and storage planning.

Methodology:

The weightInGms was multiplied by availableQuantity for each product.

The results were then summed up and grouped by category.

The output was ordered to show the lightest to the heaviest categories.

Insight: This analysis showed that perishable goods like "Meats, Fish & Eggs" had the lowest inventory weight, likely due to their quick turnover and limited shelf life. In contrast, "Munchies" had the highest inventory weight, suggesting a large, stable stock.

# How to Replicate This Analysis
To run this analysis yourself, follow these steps:

Set up PostgreSQL: Make sure you have PostgreSQL installed and running on your system.

Create the Table: Run the CREATE TABLE statement from the ZEPTO(QUERIES).sql file to create the zepto table in your database.

Import the Data: Import the ZEPTO (DATASET).csv file into the zepto table.

Execute Queries: Run the SQL queries from ZEPTO(QUERIES).sql to perform the analysis.

# Conclusion
This project demonstrates the power of SQL and relational databases for in-depth business intelligence. By using a series of targeted queries, we were able to transform raw data into actionable insights for inventory management, pricing, and logistics.
