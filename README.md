# Real-Time-Data-Pipeline-Architecture-with-AWS-Apache-NiFi-and-Snowflake

<img width="1536" height="1024" alt="ChatGPT Image May 15, 2026, 10_08_18 PM" src="https://github.com/user-attachments/assets/57d5679e-18fe-4591-ada6-31dac0012953" />

A scalable and cloud-based real-time data engineering pipeline built using AWS services, Apache NiFi, Docker, and Snowflake. This project demonstrates how to ingest, process, transform, and analyze streaming or batch data in a modern data warehouse architecture.

###  Project Overview

This project implements a complete end-to-end real-time data pipeline capable of:

Collecting data from multiple sources
Ingesting data using Apache NiFi
Storing raw data in Amazon S3
Processing and transforming data using AWS Glue
Loading curated data into Snowflake
Enabling analytics and reporting through dashboards

The architecture is designed to be scalable, secure, reliable, and production-ready for modern data engineering workflows.

### Architecture Workflow

The pipeline follows the following workflow:
Data Sources
     ↓
EC2 Instance
     ↓
Docker Container
     ↓
Apache NiFi
     ↓
Amazon S3 (Raw Zone)
     ↓
AWS Glue (ETL Processing)
     ↓
Amazon S3 (Curated Zone)
     ↓
Snowflake Data Warehouse
     ↓
Dashboards / Analytics

### Technologies Used

Cloud Services
AWS EC2
Amazon S3
AWS Glue
AWS IAM
AWS CloudWatch
AWS CloudTrail
AWS Step Functions

Data Engineering Tools
Apache NiFi
Docker
Snowflake
Python
SQL

### Key Features
Real-time data ingestion using Apache NiFi
Containerized environment using Docker
Scalable cloud architecture on AWS
Raw and curated data lake design
Automated ETL processing with AWS Glue
Secure storage and access management using IAM
Monitoring and logging with CloudWatch & CloudTrail
High-performance analytics using Snowflake
Modular and production-style architecture

### Pipeline Components Explanation
Data Sources

The pipeline can collect data from various sources such as:

APIs
IoT devices
Application logs
CSV/JSON files
Streaming events

These sources continuously generate data that needs to be processed in real time.

### EC2 Instance

An AWS EC2 instance acts as the main compute server where the ingestion tools and services are deployed.

Responsibilities:

Hosting Docker containers
Running Apache NiFi
Managing ingestion workflows

### Docker

Docker is used to containerize Apache NiFi and related services.

Benefits:

Easy deployment
Environment consistency
Portability
Simplified dependency management
### Apache NiFi

Apache NiFi is responsible for:

Real-time data ingestion
Flow management
Routing and scheduling
Data movement automation

NiFi collects incoming data and transfers it to Amazon S3.

### Amazon S3 (Raw Zone)

The raw zone stores unprocessed data exactly as received from the source.

Features:

Durable cloud storage
Cost-effective
Supports structured and semi-structured data
Stores JSON, CSV, and Parquet files

### AWS Glue (ETL Layer)

AWS Glue performs ETL (Extract, Transform, Load) operations.

Tasks performed:

Data cleaning
Schema transformation
Data enrichment
Format conversion
Preparing analytics-ready datasets

### Amazon S3 (Curated Zone)

After ETL processing, transformed data is stored in the curated zone.

This layer contains:

Clean datasets
Analytics-ready data
Optimized storage formats
### Snowflake Data Warehouse

Curated data is loaded into Snowflake for analytics and reporting.

Benefits:

High-performance querying
Scalable compute
Data warehousing capabilities
Business intelligence integration
