This project demonstrates how to build a scalable data pipeline using AWS EMR, PySpark, and Amazon S3.
The pipeline extracts raw data from Redfin.com
, processes millions of rows using PySpark on EMR, and stores both raw and transformed data in S3 buckets.





Project Workflow

Cluster Setup

Created an AWS EMR cluster to leverage distributed computing.

Configured a PySpark workspace on the cluster.

Data Extraction

Collected property listing data from Redfin.com.

The dataset contained ~5.9M rows (5,978,674 records).

Loaded raw data into an Amazon S3 bucket (s3://emr-transform-data-dak).

Data Transformation

Used PySpark to clean, filter, and extract relevant columns for organizational use.

Optimized schema for downstream analytics.

Data Loading

Saved the processed dataset into a separate S3 bucket (s3://emr-transform-data-dak).

Ensured scalability and easy integration with BI tools.

Architecture Diagram

Redfin.com → Raw Data (S3) → EMR Cluster (PySpark Transformations) → Processed Data (S3)




Tech Stack

AWS EMR – Distributed data processing cluster

Amazon S3 – Data lake storage (raw + processed)

PySpark – Data transformation & ETL

Python – Core scripting
