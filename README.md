# AdventureWorks Sales Performance Dashboard

## Project Overview
The **AdventureWorks Sales Performance Dashboard** is a Power BI project designed to provide the sales team with dynamic insights into internet sales performance. It visualizes critical metrics and trends, enabling better decision-making by comparing actual sales figures with budgeted targets. The dashboard allows the sales manager to analyze performance by products, customers, and time periods, improving reporting efficiency.

## Business Request
The sales manager requested an interactive, visual dashboard to replace static reports. Key requirements included:
1. Analysis of internet sales over time, broken down by products and customers.
2. Ability to filter by salespeople, products, and customers.
3. Benchmarking of actual sales against budgeted values.
4. A focus on sales data from 2019 to 2021.

## Data Sources
1. **AdventureWorks Database** - Contains tables for product, customer, sales, and date dimensions.
2. **Excel Spreadsheet** - Provides the 2021 budget data to compare with actual sales figures.

## Data Model
The data model comprises two fact tables and three dimension tables:
- **FACT_InternetSales**: Contains sales transaction details (e.g., product, customer, order, and shipment data).
- **FACT_Budget**: Stores budget data for comparing sales performance.
- **DIM_Customer**: Holds customer information, including location and demographics.
- **DIM_Product**: Contains product details such as category, color, and model.
- **DIM_Calendar**: Provides date attributes for time-based analysis.

The data model is optimized to support flexible filtering, allowing users to analyze sales data by various dimensions.

## Data Preparation
Data cleansing and transformation were performed using SQL to ensure accuracy and consistency across the model. Here are the key transformations:
- **DIM_Product**: Combined information from product, subcategory, and category tables to provide detailed product attributes.
- **FACT_InternetSales**: Filtered sales data to include transactions from 2019 onward.
- **DIM_Calendar**: Limited dates to 2019 and later for efficient time-based filtering.
- **DIM_Customer**: Merged customer and geography information for enhanced demographic insights.

## Dashboard Features
The Power BI dashboard includes the following views:
1. **Sales Overview**: A summary of total sales by year, product category, and customer demographics.
2. **Budget Comparison**: Visuals comparing actual sales against budgeted targets for each year.
3. **Product Performance**: Detailed analysis of product sales, including filtering by product category and line.
4. **Customer Insights**: Breakdown of sales by customer location, demographics, and purchasing history.
5. **Time Series Analysis**: Monthly and quarterly sales trends to identify seasonal patterns and growth.

## Key Metrics
- **Total Sales**: Aggregated sales amount by product, customer, and region.
- **Budget Performance**: Difference between actual sales and budgeted targets.
- **Sales by Product Category**: Analysis of sales contribution by product categories and lines.
- **Customer Demographics**: Sales segmentation by customer gender, city, and first purchase date.

## Installation and Setup
To view and interact with this Power BI dashboard:
1. Download the Power BI file (`AdventureWorks_Sales_Performance.pbix`).
2. Open the file in Power BI Desktop.
3. Ensure you have access to the necessary data sources or connect to the AdventureWorks SQL Server database as described in the [AdventureWorks documentation](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms).

## SQL Queries
The SQL scripts used for data cleansing and preparation are located in the `Scripts` folder. These scripts handle data transformation for DIM_Product, FACT_InternetSales, DIM_Date, and DIM_Customer tables, ensuring accurate data integration in Power BI.


