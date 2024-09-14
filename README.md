# Data Engineering on AWS

## Summary

This project demonstrates a data engineering pipeline implemented on AWS, utilizing Amazon Databricks for data processing and transformation, and Amazon Redshift for data analysis.

1. **Data Extraction and Storage**:
   - Employed **AWS Glue** to extract Olympic data from a GitHub repository.
   - Loaded the extracted data into **Amazon S3**, organizing the data into:
     - A **raw data bucket** for initial unprocessed data.
     - A **transformed data bucket** for processed and cleaned data, optimized for analysis.

2. **Data Transformation**:
   - Leveraged **AWS Databricks** to perform comprehensive data transformations:
     - Cleaned and structured the Olympic dataset.
     - Stored the transformed data back into the **S3 transformed data bucket** for efficient querying.

3. **Data Analysis**:
   - Configured **Amazon Redshift** to load the transformed data from S3.
   - Enabled data integration and executed queries on the structured Olympic dataset to derive insights.

---

## Architecture

1. **AWS Glue**:
   - Extracts raw data from GitHub.
   - Loads the data into the raw S3 bucket for initial storage.
   
2. **AWS Databricks**:
   - Processes and transforms the data using Apache Spark.
   - Performs data cleaning and transformation operations.
   - Outputs clean, structured data into the S3 transformed data bucket.

3. **Amazon Redshift**:
   - Loads transformed data from S3 for analysis.
   - Provides a scalable data warehouse to run queries and generate insights.

---

## Prerequisites

- AWS account with access to Glue, S3, Databricks, and Redshift.
- S3 buckets for raw and transformed data storage.
- Data source from GitHub or an external repository for extraction.

---

## How to Run

1. **Setup AWS Glue**:
   - Create a Glue job to extract data from GitHub and store it in the raw S3 bucket.

2. **Data Transformation with AWS Databricks**:
   - Spin up a **Databricks cluster** on AWS.
   - Process and clean the data using **Databricks Notebooks** and **Apache Spark**.
   - Save the transformed data into the S3 transformed bucket.

3. **Query and Analyze in Redshift**:
   - Configure **Amazon Redshift** to load the transformed data from the S3 bucket.
   - Use SQL to perform queries and analyze the dataset within Redshift.

---

## Results

- The data pipeline extracts, processes, and transforms the Olympic dataset using **AWS Glue** and **AWS Databricks**.
- The transformed data is stored in Amazon S3, and **Amazon Redshift** enables fast querying and analysis for insights.

