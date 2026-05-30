# Car Sales Analytics | Azure Data Engineering Project
## Introduction
This project focuses on building an end-to-end Azure data engineering pipeline for car sales data using Azure Data Factory for ingestion, Databricks for transformation, and Unity Catalog for governance. The data is modeled using a star schema with fact and dimension tables, implementing Slowly Changing Dimensions (SCD) to track historical changes. This solution enables scalable, well-governed, and analytics-ready data for reporting and insights.

## Architecture
![Project Architecture](Architecture.png)

The project follows the Medallion Architecture (Bronze → Silver → Gold) for structured data processing:
- Bronze Layer → Raw data ingestion
- Silver Layer → Cleaned and transformed data
- Gold Layer → Business-ready, aggregated data

## Summary

- Designed and implemented an end-to-end data engineering pipeline on Azure, processing raw data into analytics-ready datasets.
- Built scalable ETL pipelines using Azure Data Factory with batch and incremental data ingestion strategies.
- Developed data transformation workflows using Azure Databricks and PySpark, including joins, aggregations, and data cleansing.
- Implemented Medallion Architecture (Bronze–Silver–Gold) to structure data processing layers and improve data reliability.
- Modeled data using Star Schema design, enabling optimized querying and reporting.
- Applied Slowly Changing Dimensions (SCD) techniques for handling historical data changes.
- Managed data governance and access control using Unity Catalog in Databricks.
- Stored and processed large datasets using Delta Lake for improved performance and reliability.

## Technology Used
1. Programming Language : Python
2. Scripting Language : SQL
3. Azure
    - Data Factory
    - Azure Data Lake Gen2
    - Azure Databricks, PySpark
    - Azure SQL Database
    - Github
      
## Dataset used

- Initial Load Data [SalesData.csv](SalesData.csv)
- Incremental Load Data [IncrementalSales.csv](IncrementalSales.csv)

## Data Model

![Data Model Image](DataModel.png)

Data Modeling (Gold Layer)
Techniques used:
- Star Schema (Fact + Dimension tables)
- Aggregations & business logic
- Slowly Changing Dimensions (SCD Type 1)

## Project Scripts

1. [Create Catalog and schema](db_notebook.ipynb)
2. [Silver layer](Silver_notebook.ipynb)
3. [Fact Table Notebook](gold_fact_sales.ipynb)
4. [Branch Dimention Notebook](gold_dim_branch.ipynb)
5. [Date Dimention Notebook](gold_dim_date.ipynb)
6. [Dealer Dimention Notebook](gold_dim_dealer.ipynb)
7. [Model Dimention Notebook](gold_dim_model.ipynb)

## Key Learnings
- Designing scalable data pipelines in Azure
- Implementing lakehouse architecture
- Using PySpark for distributed data processing
- Managing data governance and access
- Building analytics-ready datasets

## Conclusion
This project simulates a real-world enterprise data engineering workflow, demonstrating how raw data can be transformed into reliable, governed, and analytics-ready datasets using Azure ecosystem tools.
