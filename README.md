# E-Commerce Sales Analytics Dashboard

## Project Overview

This project is an interactive E-Commerce Sales Analytics Dashboard built using Microsoft Power BI.

The dashboard analyzes online retail sales data and provides insights into sales performance, orders, customers, quantities, products, and countries.

## Tools Used

- Microsoft Power BI
- Power Query
- DAX
- Excel/CSV Dataset

## Dataset

The dataset contains online retail transaction records with information such as:

- Invoice Number
- Product Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

## Data Cleaning

The following transformations were performed using Power Query:

- Removed duplicate records
- Removed cancelled transactions
- Removed transactions with invalid quantities
- Removed transactions with zero or negative prices
- Created a Sales column using Quantity × Unit Price
- Changed columns to appropriate data types

## DAX Measures

```DAX
Total Sales = SUM(FactTables[Sales])

Total Orders = DISTINCTCOUNT(FactTables[InvoiceNo])

Total Quantity = SUM(FactTables[Quantity])

Total Customers = DISTINCTCOUNT(FactTables[CustomerID])

Average Order Value =
DIVIDE([Total Sales], [Total Orders])
