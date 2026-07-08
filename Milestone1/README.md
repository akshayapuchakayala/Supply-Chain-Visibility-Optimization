# Supply Chain Visibility & Optimization - Milestone 1

## Objective

Build a clean and efficient Power BI data model for supply chain analytics by performing data preprocessing, creating a star schema, and preparing the dataset for business analysis.

## Dataset Access Note

The dataset has not been included in this repository because of its large file size. To keep the repository lightweight and comply with GitHub's file size recommendations, the official Kaggle dataset link has been provided. Please download the dataset from the link below and use it with the Power BI project.

Dataset Link:
https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis

## Data Cleaning and Transformation

- Imported dataset into Power BI.
- Removed unnecessary columns (Customer Email, Customer Password, Order Zipcode).
- Corrected data types.
- Removed duplicate records from dimension tables.
- Created dimension tables:
  - Dim_Customer
  - Dim_Product
  - Dim_Category
  - Dim_Department
  - Dim_Shipping
  - Dim_Location
  - Dim_Date
- Added Shipping_id and Location_id using Index Columns.
- Merged Shipping and Location tables with Fact_table using Power Query.
- Created a Calendar table using DAX.
- Additional columns created in Dim_Date:
   - Year
   - Month Number
   - Month
   - Quarter
   - Week
   - Day
   - Day Name
- Established primary and foreign key relationships following a Star Schema.
  
# Relationships

The following relationships were created:

- Dim_Customer → Fact_table (Customer Id)
- Dim_Product → Fact_table (Product Card Id)
- Dim_Category → Fact_table (Category Id)
- Dim_Department → Dim_Product (Department Id)
- Dim_Shipping → Fact_table (Shipping_id)
- Dim_Location → Fact_table (Location_id)
- Dim_Date → Fact_table (Order Date) — Active
- Dim_Date → Fact_table (Shipping Date) — Inactive

## Data Model Overview

The project follows a Star Schema where Fact_table is connected to:

- Dim_Customer
- Dim_Product
- Dim_Category
- Dim_Department
- Dim_Shipping
- Dim_Location
- Dim_Date

This model supports efficient reporting and future analytics.

## Tools Used

- Microsoft Power BI Desktop
- Power Query Editor
- DAX
  
