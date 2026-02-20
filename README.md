🗄 SQL Sales Data Analysis Project – Star Schema Model
📌 Project Overview

This project demonstrates the design and implementation of a Sales Data Warehouse using a Star Schema model in PostgreSQL.

The raw sales dataset was transformed into a structured data model with fact and dimension tables to improve data integrity, reduce redundancy, and enable efficient analytical querying.

🎯 Business Problem

The original sales dataset was stored in a single denormalized table containing repeated customer, product, location, and seasonal information.

This caused:

Data redundancy

Difficulty in analyzing trends

Slow query performance

Poor scalability

The goal was to normalize the dataset into a star schema and perform analytical queries for business insights.

🏗 Data Modeling Approach
🔹 Star Schema Structure

Fact Table

fact _sales

sales _id (Primary Key)

customer _id (Foreign Key)

product _id (Foreign Key)

city _id (Foreign Key)

season _id (Foreign Key)

shipping _id (Foreign Key)

payment _id (Foreign Key)

purchase _amount

review _rating

Dimension Tables

customers

products

city

season_dim

shipping _dim

payment _dim

Each dimension table has a one-to-many relationship with the fact table.

 
 🛠 Technologies Used

PostgreSQL

pgAdmin

SQL (DDL & DML)

Star Schema Data Modeling


🔄 ETL Process

Imported raw CSV dataset into PostgreSQL.

Created dimension tables using SELECT DISTINCT.

Inserted unique values into each dimension.

Created fact_sales table.

Inserted fact data by joining raw table with dimension tables.

Established foreign key relationships.


📊 Analytical Queries Performed

Total Sales Revenue

Sales by Product Category

Seasonal Sales Trends

Average Review Rating by Product

Sales by Location

Customer Loyalty Analysis (previous purchases)

Payment & Shipping Method Analysis

Rolling Average Revenue

CTE & Window Functions


📈 Example Business Insights

Identified top-performing product categories.

Observed seasonal sales fluctuations.

Analyzed customer subscription behavior.

Evaluated shipping and payment preferences.



Data Modeling (Star Schema)

Database Normalization

Foreign Key Relationships

SQL Joins

Aggregations

CTE (Common Table Expressions)

Window Functions

Query Optimization


👩‍💻 About Me

Faesa
Mathematics Graduate
Skilled in SQL, Excel, Power BI, and Tableau
