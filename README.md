🛒 Retail Superstore Data Pipeline (AWS)

This project demonstrates an end-to-end data pipeline built using AWS services to process and analyze retail superstore sales data.

📊 Objective

To automate the ETL process of a retail sales dataset, enable querying through SQL, and create insightful dashboards using AWS tools.

---

🧰 Tech Stack

- Amazon S3– Raw data storage  
- AWS Glue– Data cleaning, transformation (ETL), and Data Cataloging  
- AWS Athena – SQL querying directly over S3  
- Amazon QuickSight – Interactive dashboards and visual analytics  
- IAM Roles & Policies – Secure access and permissions

---

🧱 Architecture Overview

1. Data Upload  
   Retail Superstore dataset (`.csv`) is uploaded to an S3 bucket in a `raw/` folder.

2. Crawling & Cataloging  
   AWS Glue crawler scans the data and catalogs it into a Glue database.

3. ETL Job (Glue)  
   Glue jobs (PySpark) clean and transform the data, storing output into a `cleaned/` folder in S3.

4. Athena Querying  
   Athena reads the cleaned data via the Glue Catalog using SQL for exploration.

5. QuickSight Visualization  
   QuickSight is connected to Athena to build dashboards on sales trends, category performance, and geographic insights.

---

🧼 Data Cleaning (ETL Highlights)

- Removed nulls and duplicates  
- Standardized date formats and category values  
- Renamed columns for clarity  
- Saved cleaned data in `Parquet` format for efficient querying

---

📈 Sample Dashboards (QuickSight)

- Total Sales & Profit by Region  
- Category and Sub-Category Performance  
- Monthly Trends and KPIs

---

🚀 How to Run

1. Upload your CSV to an S3 bucket under `raw/`
2. Set up IAM roles for Glue, Athena, and QuickSight  
3. Run the Glue crawler to catalog the raw data  
4. Launch ETL job to clean & transform the data  
5. Query transformed data via Athena  
6. Connect QuickSight to Athena for visualization
