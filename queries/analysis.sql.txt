/*
===========================================
E-Commerce SQL Case Study
Author : Sakshi Sonone
Database : PostgreSQL
Dataset : Online Retail (UCI)
Records : 541,909
===========================================
*/
/*
===========================================================
Project : E-Commerce SQL Case Study
Author  : Sakshi Sonone
Database: PostgreSQL
Dataset : Online Retail (541,909 Records)
===========================================================
*/

------------------------------------------------------------
-- Query 1 : View First 10 Records
-- Business Question:
-- What does the dataset look like?
-- Concept Used:
-- SELECT, FROM, LIMIT
------------------------------------------------------------

SELECT *
FROM ecommerce
LIMIT 10;


------------------------------------------------------------
-- Query 2 : Total Transactions
-- Business Question:
-- How many transactions are present in the dataset?
-- Concept Used:
-- COUNT(*)
------------------------------------------------------------

SELECT COUNT(*) AS total_transactions
FROM ecommerce;


------------------------------------------------------------
-- Query 3 : Unique Customers
-- Business Question:
-- How many unique customers have placed orders?
-- Concept Used:
-- COUNT(), DISTINCT
------------------------------------------------------------

SELECT COUNT(DISTINCT customer_id) AS total_customers
FROM ecommerce;


------------------------------------------------------------
-- Query 4 : List of Countries
-- Business Question:
-- Which countries have placed orders?
-- Concept Used:
-- DISTINCT, ORDER BY
------------------------------------------------------------

SELECT DISTINCT country
FROM ecommerce
ORDER BY country;


------------------------------------------------------------
-- Query 5 : Total Revenue
-- Business Question:
-- What is the total revenue generated from all sales?
-- Concept Used:
-- SUM(), Arithmetic Expression
------------------------------------------------------------

SELECT
    SUM(quantity * unit_price) AS total_revenue
FROM ecommerce;