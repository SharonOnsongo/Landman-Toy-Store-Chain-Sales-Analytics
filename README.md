# Landman-Toy-Store-Chain-Sales-Analytics
End-to-end Excel BI on the Landman Toy store chain sales dataset

## Table of Contents
- [Project Overview](#Project-overview)
- [Data Sources](#data-sources)





## Project Overview
This project examines how my client, Nationwide Maven toy chain store, is performing across products, stores, and seasons, enabling the client to make informed, data-driven decisions about what to stock, where to place it, and when to promote it. The analysis transforms raw store data into clear, prioritized actions that drive revenue growth, protect margins, and keep shelves stocked with what customers actually want.

## Data Sources
This project uses 4 tables from the Maven Toys sales data stored in the data folder
- Sales Table - Transaction-level sales data with Sale_ID, Date, Store_ID, Product_ID, and Units sold
- Products Table - Product catalog containing 35 products with pricing and category information
- Inventory Table - Current stock levels for each product at each store location
- Stores Table - Store information, including 50 locations across Mexico, with opening dates and location types


## Tools Utilized
- Power Query
- Power Pivot
- DAX
- Excel
- Dynamic Arrays

## Data Cleaning & Transformation

#### Products Table
- Conducted data profiling to check the quality of the data
- Filtered rows to remove null values
- Removed duplicates in dimension tables
- Changed Data Types
- Did a data validation to check that there are no negative values in the product cost and price
- Removed the currency symbols before product cost and product price to remove the error that comes when changing data types.
- Removed unnecessary columns
- Added an age column to the date column
- Added custom columns to show profit per unit and profit marginunit margin in the product column
- Trimmed whitespace from text fields
- Added a age column in the store table and age group for store maturity
- Checked for negative stock
- Added anew conditional column for stock status
  


## Data Modeling
Merged 5 tables into star schema
### Fact Tables
- Sales 
- Inventory
### Dimension Tables
- Added a date table to the data model
- Changed Data Types in the date table
- Added columns to the date table, such as day of week and month
- 
  
## DAX
## Data Analysis
-Pivot Tables
## Dashboard

