# Landman-Toy-Store-Chain-Sales-Analytics
End-to-end Excel BI on the Landman Toy store chain sales dataset

## Table of Contents
- [Project Overview](#Project-overview)
- [Data Sources](#data-sources)
- [Tools Utilized](#Tools-Utilized)
- [Data Cleaning & Transformation](#data-cleaning--transformation)

## Project Overview
This project analyzes the performance of Maven Toys, a nationwide toy chain store across Mexico, examining sales patterns across products, stores, and seasons. The objective is to transform raw transactional and operational data into actionable business insights that support strategic decisions around revenue growth, inventory optimization, store performance, product performance, seasonal trends, and support data-driven decision-making.

## Business Objectives

- Analyze sales performance across products, stores, and time periods
- Optimize inventory management to reduce stockouts and excess inventory
- Identify top-performing and underperforming products
- Compare performance across store lifecycle stages
- Provide actionable insights for business growth and profitability improvement
- Create executive-level dashboards to support data-driven decision making

## Data Sources
This project uses 4 tables from the Maven Toys sales data stored in the data folder
- Sales Table - Transaction-level sales data with Sale_ID, Date, Store_ID, Product_ID, and Units sold
- Products Table - Product catalog containing 35 products with pricing and category information
- Inventory Table - Current stock levels for each product at each store location
- Stores Table - Store information, including 50 locations across Mexico, with opening dates and location types
- Calendar Table - Custom calendar table created in Power Query for time intelligence analysis, including Year, Quarter, Month, Week, and Day attributes


## Tools Utilized
 Excel
- Power Query
- Power Pivot
- DAX
- Pivot Tables & Charts
- Dynamic Arrays

## Data Cleaning & Transformation
All data preparation was performed in Power Query following best-practice ETL principles.

### Data Quality Assessment
- Conducted a comprehensive data quality audit checking for:
  1. Data type inconsistencies
  2. Text formatting issues (leading/trailing spaces)
  3. Missing values and null records
  4. Duplicates in dimension tables
  5. Orphan records (referential integrity)
- Performed data profiling to validate dataset integrity.

### Key Transformations Applied:
#### Calendar table
-  Built a custom date dimension table in Power Query for time intelligence analysis
-  Added hierarchical date attributes such as year, quarter, and month.
-  Added business logic, such as 

#### Products Table
- Removed the currency symbol from two columns, preventing numeric calculations
- Converted cost and price columns to Currency data type
- Added calculated columns
  1. profit per unit
  2. profit margin
- Trimmed whitespace from Product Name and Product Category
- Validated no negative values in pricing columns
  
#### Sales Table
- Ensured Units sold contain only positive values
- Verified all Sale IDs are unique
- Confirmed all Store IDs and Product IDs have matching records in dimension tables

#### Store Table
- Created calculated column.Calculated store age in completed years, accounting for leap years (365.25 days) and rounding down to whole numbers for 
  business and financial analysis purposes
- Added a conditional column. Implemented store lifecycle segmentation using conditional logic . This segmentation enables comparative analysis across store maturity levels.
- 
#### Inventory Table
- Validated no negative stock quantities
- Added conditional column: Stock Status
- Confirmed all Store_IDs and Product_IDs reference valid dimension records
  
#### Products Table
- Did a data validation to check that there are no negative values in the product cost and price
-Product_Cost and Product_Price columns contained currency symbols ("$") stored as text, preventing conversion to numeric data types and blocking mathematical operations
- Added custom columns to show profit per unit and profit margin in the product column

### Data Loading
- Loaded all tables using Connection Only mode
- Added all tables to the Data Model for relationship management in Power Pivot


## Data Modeling
The data model follows a star schema design with proper fact and dimension tables
  #### Fact Tables
- Sales 
- Inventory
  #### Dimension Tables
- Products
- Stores
- Calender
  
Created 5 dimension-to-fact relationships with appropriate cardinality
   - Products ➔ Sales (1:Many)
   - Stores ➔ Sales (1:Many)
   - Products ➔ Inventory (1:Many)
   - Stores ➔ Inventory (1:Many)
![](https://github.com/SharonOnsongo/Maven-Toy-Store-Chain-Sales-Analytics/blob/main/Data%20model%20.png)

  

  
## DAX
## Data Analysis
-Pivot Tables
## Dashboard

