# 🧭 AWS ETL Pipeline – Enterprise Analytics

### 🚀 End-to-End Serverless Data Engineering Project

This project demonstrates a **fully automated, serverless ETL (Extract–Transform–Load) pipeline** built entirely on **AWS**.  
It ingests raw data into S3, transforms it using **AWS Glue**, orchestrates automation through **Lambda** and **EventBridge**, catalogs processed data with a **Glue Crawler**, and enables analytics directly from **Athena** — all with real-time monitoring and alerts.

---

## 🌐 Architecture Overview

<p align="center">
  <img src="docs/staging_bucket.png" alt="AWS ETL Pipeline Architecture" width="650"/>
</p>

### **Pipeline Flow**

S3 (staging upload)

↓ triggers

Lambda (trigger_glue_etl)

↓

AWS Glue ETL Job (transform_staging_to_processed)

↓

S3 (processed - Parquet output)

↓

EventBridge → Lambda (trigger_glue_crawler)

↓

Glue Crawler → Data Catalog

↓

Athena SQL Queries / BI Dashboards

↓

CloudWatch + SNS → Monitoring & Alerts
