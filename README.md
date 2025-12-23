# Landman-Toy-Store-Chain-Sales-Analytics
End-to-end Excel BI on the Landman Toy store chain sales dataset

## Table of Contents
- [Project Overview](#Project-overview)
- [Data Sources](#data-sources)
- [Tools Utilized](#Tools-Utilized)
- [Data Cleaning & Transformation](#data-cleaning--transformation)

## Project Overview
This project examines how my client, Nationwide Maven toy chain store, is performing across products, stores, and seasons, enabling the client to make informed, data-driven decisions about what to stock, where to place it, and when to promote it. The analysis transforms raw store data into clear, prioritized actions that drive revenue growth, protect margins, and keep shelves stocked with what customers actually want.

## Business Objectives

- Analyze sales performance across products, stores, and time periods
- Optimize inventory management to reduce stockouts and excess inventory
- Identify top-performing products and underperformers
- Provide actionable insights for business growth and profitability improvement
- Create executive-level dashboards for data-driven decision making

## Data Sources
This project uses 4 tables from the Maven Toys sales data stored in the data folder
- Sales Table - Transaction-level sales data with Sale_ID, Date, Store_ID, Product_ID, and Units sold
- Products Table - Product catalog containing 35 products with pricing and category information
- Inventory Table - Current stock levels for each product at each store location
- Stores Table - Store information, including 50 locations across Mexico, with opening dates and location types
- Calendar Table - Custom calendar table created in Power Query for time intelligence analysis, including Year, Quarter, Month, Week, and Day attributes


## Tools Utilized
- Power Query
- Power Pivot
- DAX
- Excel
- Dynamic Arrays

## Data Cleaning & Transformation
All data cleaning and preparation was performed using Power Query
### Data Quality Assessment/General cleaning steps
- Conducted a comprehensive data quality audit to check for data formatting issues, Text Inconsistency, Missing Values, Orphan Records, and Currency Symbols
-  Check for leading and trailing spaces in text fields
-  Checked the data types in each column
-  Conducted Data Type Verification
-  Check for duplicates and null values, and decide on how to handle all of them according to business needs
## Key Transformations Applied:
#### Calendar table
-  Built a custom date dimension table in Power Query to enable time intelligence analysis
-  Added hierarchical date attributes such as year, quarter, and month.
-  Added business logic, such as 

#### Products Table
- Removed the currency symbol from two columns, preventing numeric calculations
- Changed Product_Cost and Product_Price to Currency type
- Added the profit and profit margin column
- Trimmed whitespace from Product_Name and Product_Category
- 
#### Sales Table


#### Store Table
- 
#### Inventory Table
- Validated no negative stock quantities
- Added a conditional column to show the stock status
- 
#### Products Table
- Conducted data profiling to check the quality of the data
- Filtered rows to remove null values
- Removed duplicates in dimension tables
- Changed Data Types
- Did a data validation to check that there are no negative values in the product cost and price
- Removed the currency symbols before product cost and product price to remove the error that comes when changing data types.
- Removed unnecessary columns
- Added an age column to the date column
- Added custom columns to show profit per unit and profit margin in the product column
- Trimmed whitespace from text fields
- Added an age column in the store table and an age group for store maturity
- Checked for negative stock
- Added a conditional column for stock status anew
  


## Data Modeling
Merged 5 tables into a star schema

Products ➔ Sales (1:Many)
Stores ➔ Sales (1:Many)
Products ➔ Inventory (1:Many)
Stores ➔ Inventory (1:Many)

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

