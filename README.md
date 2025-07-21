# Superstore Data Analysis — End-to-End AWS Data Engineering Pipeline

Project: Superstore Data Analysis — End-to-End AWS Data Engineering Pipeline

Overview:
This project demonstrates a complete data engineering workflow using AWS services — 
IAM, S3, Glue, Athena, and QuickSight — with the Superstore dataset from Kaggle as the source.

Step-by-step process:

1) IAM User Creation:
An IAM user (with admin permissions) is created specifically for data engineering tasks, keeping the AWS root account secure.

2) S3 Bucket Setup and Data Upload:
A new S3 bucket is created (e.g., “namaste-sql”), and the Superstore dataset from Kaggle is uploaded, 
logically organized in folders and possibly partitioned 
(by snapshot date or similar).

3) Glue Crawler and Data Catalog:
A Glue database is set up, and a Glue Crawler is configured to scan the S3 bucket. 
The crawler automatically detects the schema (columns, types, partitions) and 
creates a corresponding table in the Glue Data Catalog.
Any time the raw data changes, re-running the crawler will update the catalog schema automatically.

4) Athena Querying:
The table registered with Glue appears in Athena, allowing you to write and run SQL
 queries directly against the data stored in S3 (no need for a separate database server).
Common queries include aggregations, trends, and other analytical operations.

5) Visualization with QuickSight:
Signed up for QuickSight and connected it to Athena/Glue data.
Built interactive dashboards and data visualizations using the analyzed data.

6) Skills/Concepts Demonstrated:

Setting up and managing AWS IAM users for security
Building and organizing data lakes using S3
Automatic data cataloging and schema discovery with Glue Crawlers
Running serverless SQL queries via Athena
Creating interactive business dashboards in QuickSight

Outcome:
The project showcases how to design and implement a cloud-based data pipeline—
from raw data ingestion in S3 to automated data cataloging, serverless querying, and business insights 
visualization—entirely using AWS services.
