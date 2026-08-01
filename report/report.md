# Delta Lake MERGE Implementation - Report

## Overview
This assignment implements Delta Lake MERGE (upsert) operations on customer sales data using Azure Databricks.

## Steps Performed
1. Loaded customer_master.csv into a Delta table
2. Cleaned and validated the data
3. Created incremental data with updates and new records
4. Applied SCD Type 1 (overwrite) using MERGE
5. Applied SCD Type 2 (history tracking) using MERGE
6. Validated results with record counts and data checks

## Tools Used
- Azure Databricks (Serverless compute)
- Delta Lake
- PySpark
- Python (pandas)
