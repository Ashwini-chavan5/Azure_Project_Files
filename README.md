# Azure Data Engineering Projects

This repository showcases two end-to-end data engineering projects built on Azure, demonstrating metadata-driven ETL design, medallion architecture, and orchestration across Azure Data Factory and Azure Databricks.

Full project write-ups (with pipeline screenshots) are available in the [`Project_Documentation`](./Project_Documentation) folder.

---

## Project 1: Azure Data Factory — Metadata Driven ETL Project

**Overview:** This project demonstrates an end-to-end ETL solution built using Azure Data Factory, using a metadata-driven design to make pipelines dynamic, reusable, and scalable across multiple source files and tables.

**Architecture:**
```
GitHub → ADF → ADLS Silver → ADLS Gold
GitHub → ADF → SQL Bronze → SQL Silver → ADLS Gold
```

**Features:**
1. Dynamic file ingestion
2. Metadata-driven processing
3. Incremental loading
4. Bronze/Silver/Gold architecture
5. Largest file detection
6. Latest table detection
7. Parameterized datasets
8. Reusable pipelines

**Technologies:**
1. Azure Data Factory
2. Azure SQL Database
3. Azure Data Lake Storage Gen2
4. GitHub
5. T-SQL

**Business Scenarios Covered:**
1. Data ingestion
2. Incremental loading
3. Dynamic routing
4. Data lake processing
5. SQL-based transformations

---

## Project 2: Azure Databricks — End-to-End Data Engineering Pipeline

**Overview:** This project extends the ETL workflow into a full Databricks-based pipeline, using PySpark transformations and Unity Catalog–governed Delta tables to implement a medallion architecture.

**Architecture:**
```
ADLS Gen2 (Raw) → Databricks (Bronze) → Databricks (Silver) → ADLS Gen2  (Gold) → Unity Catalog Delta Table (Gold)
Orchestrated end-to-end via Azure Data Factory–triggered Databricks notebooks
```

**Features:**
1. Medallion architecture (Bronze / Silver / Gold layers)
2. PySpark-based transformations
3. Data profiling, cleansing, validation, and reconciliation
4. Unity Catalog–governed Delta Tables
5. ADLS Gen2 Gold layer
6. ADF-orchestrated Databricks notebook execution

**Technologies:**
1. Azure Databricks
2. PySpark
3. Delta Lake / Delta Tables
4. Unity Catalog
5. Azure Data Lake Storage Gen2 (ADLS Gen2)
6. Azure Data Factory (orchestration)

**Business Scenarios Covered:**
1. Large-scale data ingestion and transformation
2. Data quality validation and reconciliation
3. Layered (medallion) data processing
4. Governed data access via Unity Catalog
5. Cross-service orchestration (ADF + Databricks)

---

## Repository Structure
```
├── source/                      # Pipeline source files
├── Project_Documentation/       # Detailed write-ups with screenshots for both projects
└── README.md                    # This file
```
