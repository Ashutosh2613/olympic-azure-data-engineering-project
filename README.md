# Olympic Azure Data Engineering Project

## Introduction
This project demonstrates a complete data engineering pipeline for analyzing Olympic data. The pipeline starts with data ingestion from CSV files, data transformation using Azure Databricks, and final storage in Azure Synapse Analytics. The architecture uses Azure Data Factory, Azure Data Lake Gen 2, Azure Synapse Analytics, and Databricks for data processing and management.

## Architecture Diagram
![azure (1)](https://github.com/user-attachments/assets/aaa9a6ae-2e56-4af3-94b9-c85e8872c201)

## Project Workflow
* Data Souurce :
   - The dataset consists of CSV files containing historical Olympic data.
   - Files were uploaded to GitHub so that we can ingest it from Azure using Data factory.
* Data Ingestion :
   - Used Azure Data Factory to ingest the data from GitHub (CSV format) via HTTP.
   - The ingested raw data was stored in Azure Data Lake Gen 2.
* Data Transformation :
   - Azure Databricks (Spark code) was used to process and transform the raw data. The transformations included:
      - Data cleaning and preparation.
      - Aggregation and computation of key metrics.
      - Formatting the data for further analysis.
   - Transformed data was stored back in Azure Data Lake Gen 2.
* Data Storage and Analytics :
   - After transformation, the data was moved to Azure Synapse Analytics.
   - A database was created in Synapse, where the data was stored in structured tables for further querying and analysis.

## Tools and Technologies Used
- Azure Data Factory: For orchestrating the data ingestion pipeline.
- Azure Data Lake Gen 2: For storing both raw and transformed data.
- Azure Databricks: For transforming the data using Apache Spark.
- Azure Synapse Analytics: For final storage and querying of the transformed data.
- GitHub: For storing the dataset CSV files.
