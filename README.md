# Delta Lake MERGE Implementation

## Assignment - Celebal Technologies Data Engineering Internship

## Objective
Perform incremental data processing using Delta Lake MERGE operation on customer sales data.

## Dataset
- **Source:** Superstore Sales Dataset (Kaggle)
- **File:** customer_master.csv
- **Size:** 19,988 rows, 21 columns

## Steps Completed

### 1. Data Loading
- Loaded customer_master.csv into Databricks
- Verified: 19,988 rows, 21 columns

### 2. Data Cleaning
- Checked null values (none found)
- Removed duplicates
- Fixed column names (spaces → underscores for Delta compatibility)
- After cleaning: 15,227 rows

### 3. Delta Table Creation
- Saved cleaned data as Delta table: `customer_master_delta`

### 4. Incremental Data
- Created 102 incremental records (100 updates + 2 new customers)

### 5. MERGE Operation
- Applied Delta Lake MERGE (upsert)
- Matched on: `Order_ID`
- whenMatchedUpdateAll + whenNotMatchedInsertAll

### 6. Validation
- Final rows after MERGE: 15,229
- New records inserted: 2

### 7. Summary
- MERGE Operation: ✅ SUCCESS
- Delta Lake Implementation: ✅ COMPLETE

## Repository Structure

delta-lake-assignment/
├── notebooks/ → Databricks notebook (.ipynb)
├── data/ → Dataset (customer_master.csv)
├── screenshots/ → Output screenshots
└── README.md

## Tools Used
- Azure Databricks
- Apache Spark (PySpark)
- Delta Lake
- Python
