# ADF Sales View Data Pipeline Project

## Project Overview

This project implements an end-to-end data engineering pipeline using Azure Data Factory, Azure Data Lake Storage Gen2, and Azure Databricks.

The pipeline ingests raw customer, product, store, and sales files from ADLS using Azure Data Factory and stores them in the Bronze layer. Databricks is then used to transform raw data into cleaned Silver Delta tables and finally create an analytics-ready Gold table.

## Architecture

Source Files → Azure Data Factory → Bronze Layer → Databricks → Silver Layer → Databricks → Gold Layer

This project follows the Medallion Architecture:

- Bronze Layer: Raw data
- Silver Layer: Cleaned and transformed Delta tables
- Gold Layer: Business-ready analytical table

## Technologies Used

- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks
- PySpark
- Delta Lake
- Azure DevOps / Git

## ADLS Folder Structure

```text
bronze/sales_view/
  ├── customer/
  ├── product/
  ├── store/
  └── sales/

silver/sales_view/
  ├── customer/
  ├── product/
  ├── store/
  └── customer_sales/

gold/sales_view/
  └── StoreProductSalesAnalysis/
