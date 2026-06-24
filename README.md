# Healthcare Data Pipeline using AWS, Apache Spark & Airflow

## Overview

This project implements an end-to-end Healthcare Data Pipeline that extracts healthcare data from a PostgreSQL database, processes and transforms it using Apache Spark (PySpark), stores data in Amazon S3, performs analytical transformations using Hive, and loads reporting datasets into Amazon Redshift. The workflow is orchestrated using Apache Airflow and executed on AWS EMR.

The pipeline automates healthcare data processing and generates analytical datasets for reporting and decision-making.

---

## Architecture

PostgreSQL (AWS RDS)
↓
PySpark ETL
↓
Amazon S3 (Data Lake)
↓
Hive Transformations
↓
Amazon S3 / Amazon Redshift
↓
Analytics & Reporting

Orchestration: Apache Airflow

Processing Engine: Apache Spark on AWS EMR

---

## Features

- Extract healthcare data from PostgreSQL
- Store raw datasets in Amazon S3 as Parquet files
- Process large-scale healthcare records using PySpark
- Create Hive tables for analytical querying
- Generate healthcare business metrics
- Load transformed data into Amazon Redshift
- Automate workflows using Apache Airflow DAGs
- Scalable cloud-based architecture using AWS services

---

## Technology Stack

### Cloud Services
- AWS S3
- AWS EMR
- AWS Redshift
- AWS RDS

### Big Data Technologies
- Apache Spark
- PySpark
- Apache Hive
- Apache Airflow

### Database
- PostgreSQL

### Programming Language
- Python

### File Format
- Parquet

---

## Healthcare Dataset

The pipeline processes the following healthcare entities:

- Patients
- Doctors
- Appointments
- Treatments
- Medications
- Prescriptions
- Billing
- Medical History

---

## Project Structure


Health-Data-Pipeline/
│
├── health_datapipeline_dag.py
├── rdbms_read_and_write_to_s3.py
├── read_from_s3_and_transform_to_hive.py
├── read_from_s3_and_transform_to_redshift.py
├── spark_sql_transformation_and_write_to_s3.py
├── spark_hive_write_to_s3.py
├── s3_pyspark_hive_sample.py
├── sql_health_ddl.sql
├── insert_health_dml.sql
└── README.md


---

## Workflow

### Step 1: Data Extraction

Read healthcare data from PostgreSQL database tables:

- Patients
- Doctors
- Appointments
- Treatments
- Medications
- Prescriptions
- Billing
- MedicalHistory

### Step 2: Data Lake Storage

Store extracted datasets in Amazon S3 using Parquet format.

Benefits:
- Columnar storage
- Faster querying
- Reduced storage cost
- High scalability

### Step 3: Data Transformation

Perform transformations using Spark SQL:

- Full Name generation
- Date formatting
- Appointment analytics
- Billing aggregation
- Condition-based analysis
- Medication analytics
- Treatment statistics

### Step 4: Hive Analytics Layer

Create Hive tables for:

- Appointments with Patient & Doctor Names
- Total Billing Analysis
- Appointment Count Analysis
- Hypertension Patient Analysis
- Billing Statistics
- Treatment Analysis

### Step 5: Data Warehouse Layer

Load transformed datasets into Amazon Redshift for reporting and business intelligence.

---

## Key Analytics Generated

### Patient Analytics
- Total appointments per patient
- Patient billing summary
- Medical history analysis

### Doctor Analytics
- Medication prescription statistics
- Appointment performance metrics

### Billing Analytics
- Total billed amount
- Average billing amount
- Maximum and minimum billing values

### Medical Analytics
- Disease prevalence analysis
- Hypertension patient identification
- Treatment effectiveness reports

---

## Airflow Orchestration

The pipeline is automated using Apache Airflow.

Workflow:

1. Read data from PostgreSQL
2. Write data to Amazon S3
3. Transform data using Hive
4. Store analytical results
5. Load data into Redshift

Airflow DAG:
`health_datapipeline_dag.py`

---

## AWS Components Used

| Service | Purpose |
|----------|----------|
| Amazon RDS | Source Database |
| Amazon S3 | Data Lake |
| Amazon EMR | Spark Processing |
| Amazon Redshift | Data Warehouse |
| Apache Airflow | Workflow Scheduling |
| Apache Hive | Data Analytics |

---

## Business Benefits

- Automated healthcare data processing
- Faster report generation
- Scalable cloud architecture
- Improved healthcare analytics
- Centralized data warehouse
- Reduced manual intervention

---

## Learning Outcomes

Through this project, I gained hands-on experience in:

- Data Engineering
- ETL Pipeline Development
- Apache Spark & PySpark
- AWS Cloud Services
- Data Warehousing
- Apache Airflow
- Apache Hive
- Amazon Redshift
- Big Data Analytics
- Healthcare Data Processing

---

## Future Enhancements

- Real-time streaming using Apache Kafka
- Interactive dashboards using Power BI or Tableau
- Machine Learning-based healthcare prediction
- Automated data quality monitoring
- Data Lakehouse implementation using Delta Lake

---

## Author

**Aditi Mandhare**

B.E. Computer Engineering  
Savitribai Phule Pune University (SPPU)

GitHub: https://github.com/aditimandhare-7
