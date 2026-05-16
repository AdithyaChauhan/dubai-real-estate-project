# Azure Databricks Real Estate ETL Pipeline

## Overview

This project implements an end-to-end Azure Data Engineering pipeline using:

- Azure Databricks
- PySpark
- Delta Lake
- Azure Data Lake Storage Gen2
- Databricks Workflows
- SQL Analytics & Visualizations

The pipeline processes Dubai real estate transaction datasets using a Medallion Architecture approach (Bronze → Silver → Gold) and automates transformations using Databricks orchestration workflows.

---

# Architecture

## Medallion Architecture

Bronze Layer → Raw ingestion storage  
Silver Layer → Cleaned & transformed Delta tables  
Gold Layer → Business-ready KPI aggregations

---

# Tech Stack

- Azure Databricks
- PySpark
- Delta Lake
- Azure Data Lake Storage Gen2 (ADLS Gen2)
- Databricks Workflows
- SQL
- Data Visualization

---

# Pipeline Workflow

Automated Databricks workflow executing:

1. Silver Transformations  
2. Gold Aggregations  
3. Power BI Bridge Refresh  
4. Market Dashboard Generation

## Workflow Success

<img width="1614" height="797" alt="Pasted image (14)" src="https://github.com/user-attachments/assets/17c4d134-bdf9-4a0f-b94f-7c423ec84e3e" />

---

# Bronze Layer

Raw datasets are ingested and stored in Azure Data Lake Storage Gen2.

## Bronze Storage Structure

<img width="1248" height="443" alt="Pasted image (2)" src="https://github.com/user-attachments/assets/ec5f400d-669b-4b6e-9689-26faea7c5742" />


## Transactions Landing Zone

<img width="652" height="376" alt="Pasted image (4)" src="https://github.com/user-attachments/assets/f9da216d-601f-4583-a358-3a868d091772" />

## Units Landing Zone

<img width="652" height="376" alt="Pasted image (5)" src="https://github.com/user-attachments/assets/9f9ef087-7694-4e52-bb04-6e2ed7574775" />

## Projects Landing Zone

<img width="652" height="376" alt="Pasted image (3)" src="https://github.com/user-attachments/assets/2a7bcd64-f3df-48d5-8151-c1bf53c5ef38" />

---

# Silver Layer

The Silver layer applies:

- Data cleaning
- Type casting
- Null handling
- Delta formatting
- Business transformations

## Silver Delta Storage

### Transactions Delta Files

<img width="1299" height="679" alt="Pasted image (6)" src="https://github.com/user-attachments/assets/112e9078-7f2e-49ad-a9c1-11836c3ad249" />

### Units Delta Files

<img width="1299" height="679" alt="Pasted image (7)" src="https://github.com/user-attachments/assets/0d875746-089e-41e5-8cbb-36b7f14aa0db" />

---

# Gold Layer

The Gold layer generates analytics-ready KPI tables.

Generated KPIs include:

- Monthly Sales Trends
- Area Performance
- Supply & Inventory Analysis

## Gold Verification

<img width="1384" height="678" alt="Pasted image (10)" src="https://github.com/user-attachments/assets/b2c0d32f-a709-4032-acf9-74b2a66e7566" />

---

# Analytics Dashboard

## Monthly Sales Trend

<img width="1377" height="717" alt="Pasted image (11)" src="https://github.com/user-attachments/assets/ecf72d3b-9179-4394-9e6a-4bb98c38ffe8" />

## Area-wise Sales Volume

<img width="1348" height="750" alt="Pasted image (12)" src="https://github.com/user-attachments/assets/75115632-3d26-408c-be39-ca1cdb24d162" />

## Supply Distribution by Room Type

<img width="1348" height="750" alt="Pasted image (13)" src="https://github.com/user-attachments/assets/f441b14b-0497-4105-8c11-70f7b5cc1fdc" />


---

# Workflow Orchestration

The pipeline is fully automated using Databricks Workflows.

Tasks include:

- 3_transform_silver
- 4_transform_gold
- 5_refresh_bridge
- 6_market_dashboard

## Full Workflow Pipeline

<img width="1627" height="461" alt="Pasted image (15)" src="https://github.com/user-attachments/assets/c659505b-332d-489d-aacc-b1db2e86d494" />

---

# Features

- End-to-end ETL pipeline
- Automated orchestration
- Delta Lake implementation
- Medallion Architecture
- ADLS Gen2 integration
- KPI generation
- Dashboard-ready analytics
- Scheduled execution
- Large-scale distributed processing

---

# Dataset

Dubai Real Estate Transactions Dataset

Data includes:

- Property transactions
- Units inventory
- Projects metadata
- Area-level analytics

---

# Project Structure

```text
project-root/
│
├── notebooks/
│   ├── 1_ingest_bronze_snapshot.py
│   ├── 2_ingest_dimensions_units_projects.py
│   ├── 3_silver_transformation.py
│   ├── 4_gold_transformation.py
│   ├── 5_powerbi_bridge.py
│   └── 6_market_dashboard.py
│
├── images/
│   ├── workflow_dag.png
│   ├── workflow_success.png
│   ├── bronze_storage.png
│   ├── bronze_transactions.png
│   ├── bronze_units.png
│   ├── bronze_projects.png
│   ├── silver_verification.png
│   ├── silver_transactions_delta.png
│   ├── silver_units_delta.png
│   ├── gold_verification.png
│   ├── monthly_sales.png
│   ├── area_stats.png
│   ├── supply_distribution.png
│   └── full_workflow.png
│
└── README.md
```

---

# Security Note

All Azure Storage keys and credentials have been removed from notebooks before publishing this repository.

---

# Future Improvements

- Real-time streaming ingestion
- Azure Key Vault integration
- CI/CD with Azure DevOps
- Power BI cloud dashboards
- Incremental Delta processing
- Unity Catalog integration

---

# Author

Adithya Singh Chauhan
