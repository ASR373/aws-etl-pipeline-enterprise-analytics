# AWS ETL Pipeline – Enterprise Analytics

### Day 1 Progress
✅ GitHub repo and folders initialized  
✅ Mock datasets created and uploaded to S3  
✅ Ingestion + data validation script built  
✅ Cleaned data written to staging S3 bucket  

### Next Steps (Day 2)
- Implement AWS Glue transformation job (PySpark)
- Create Redshift schema and load transformed data
- Begin Airflow DAG orchestration


Upload → S3(staging)
   ↓ triggers
Lambda → starts Glue ETL
   ↓
Glue → writes Parquet to S3(processed)
   ↓
Glue Crawler → updates Data Catalog
   ↓
Athena → queries analytics data directly from S3
