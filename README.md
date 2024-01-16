# SQL Triggers Lab - Lab4

## Introduction

This script is part of the SQL Triggers Lab (Lab4) and is designed to set up the environment for running the remainder of the script. It includes the creation of the necessary database, tables (customers and sales), data insertion, index creation, and view creation.

## Script Start

The first part of the script sets up the environment in which the remainder of the script will run. This includes setting the date format to `YYYY-MM-DD`, ensuring compatibility with the sales record inserts. The script checks if the `co859` database already exists and deletes it if it does. The database is then created to ensure a clean environment.

## Master Table

The script includes the creation of the `customers` table, which serves as the master table. If your master table is named differently (e.g., `items` or `<description>_services`), update the script accordingly. Additionally, the script creates the `sales` table for tracking sales records.

## Loading the Master and Sales Tables

The master table (`customers`) is loaded with at least 5 records using INSERT statements. Similarly, the sales table is loaded with at least 15 records. You may edit the sample INSERT statements or use an Excel workbook to generate them.

## Creating an Index

An index is created based on the type of master table:

- If the master table is a customers table, an index is created on the customer name.
- If the master table is an items table, an index is created on item description.
- If the master table is a services table, an index is created on service description.

## Creating A View

A view named `high_end_customers` is created to highlight the most expensive elements of the master table. The view includes 15 characters of the name or description field, year-to-date sales, and only selects records where the credit limit is greater than the average.

## Verify Inserts

The script includes verification code to ensure that the inserts were successful. This verification should be the last thing in the script.

## SQL Keywords

Ensure that none of your identifiers (tables, columns, constraints, etc.) are SQL keywords or reserved words. If any identifier changes color from black to any other color in SQL Server Management Studio, it is a reserved word, and you must change it.

## Usage Instructions

1. Open SQL Server Management Studio (SSMS) or another SQL database client.

2. Copy and paste the content of Lab4.txt into a new query window and execute the script.

3. Verify the results by checking the printed messages and querying the necessary tables and views.
