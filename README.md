# Databricks and PySpark Notes

My learning notes for **Databricks** and **PySpark**.

***

# Day 1

# What is Databricks?

## Definition

**Databricks** is a **Unified Analytics Platform** that helps organizations:

* Manage data
* Process data
* Analyze data

from a single platform.

It is built on top of **Apache Spark** and provides many enterprise-level features that make big data processing easier, faster, and more efficient.

## Key Points

### Databricks is More Than Just Apache Spark

Many people think Databricks is only a platform to run Spark code.

This is not true.

Databricks uses Apache Spark as its processing engine, but it also provides additional features such as:

* Collaborative Workspace
* Cluster Management
* Delta Lake
* Data Governance
* Machine Learning Support
* Workflow Automation
* Security and Access Control
* Performance Optimization

***

## 1. Collaborative Workspace

Databricks provides a **collaborative workspace** where:

* Data Engineers
* Data Analysts
* Data Scientists

can work together on the same platform.

### Features

* Create personal notebooks.
* View notebooks created by other developers.
* Share notebooks and tables.
* Collaborate in real time.
* Work in a common development environment.

### Simple Explanation

Instead of using separate tools for different teams, Databricks provides a single workspace where everyone can collaborate efficiently.

***

## 2. Support for Data Lake, Data Warehouse, and Machine Learning

Databricks supports **Lakehouse Architecture**, which combines the capabilities of both a Data Lake and a Data Warehouse.

### Data Lake

A Data Lake can store:

* Structured data
* Semi-structured data
* Unstructured data

Examples:

* CSV files
* JSON files
* Images
* Videos
* Log files

### Data Warehouse

A Data Warehouse provides:

* Fast analytics
* High query performance
* Reporting capabilities
* Structured data management

### Lakehouse

A Lakehouse combines:

* Flexibility of a Data Lake
* Performance of a Data Warehouse

### Simple Explanation

With Databricks Lakehouse, organizations do not need separate systems for storage and analytics.

***

## 3. Delta Lake Technology

Databricks uses **Delta Lake** to provide:

* Reliability
* Governance
* Performance Optimization

### Reliability

Ensures data remains:

* Accurate
* Consistent
* Safe

### Governance

Helps with:

* Data control
* Security
* Compliance
* Data management

### Performance

Provides:

* Faster processing
* Faster queries
* Optimized analytics workloads

### Simple Explanation

Delta Lake makes data more reliable and easier to manage while improving performance.

***

# What is Apache Spark?

## Definition

**Apache Spark** is an **open-source distributed computing engine** used to process large amounts of data efficiently.

It is designed for **big data processing** and supports both batch and real-time workloads.

## Key Points

* Open-source framework.
* Distributed data processing engine.
* Processes massive datasets.
* Faster than Hadoop MapReduce.
* Supports multiple workloads.

### Supports

* Batch Processing
* Streaming Processing
* Spark SQL
* Machine Learning
* Graph Processing

***

## Why Apache Spark is Fast?

### In-Memory Processing

Spark processes data primarily in **memory (RAM)** rather than continuously reading from disk.

### Benefits

* Faster execution
* Reduced disk I/O
* Better performance
* Efficient iterative processing

### Simple Explanation

Because data stays in memory during processing, Spark can execute jobs much faster than traditional disk-based frameworks.

***

## Distributed Computing

Spark follows a **distributed computing architecture**.

### Meaning

A large task is divided into multiple smaller tasks.

These tasks are then executed simultaneously across multiple computers.

### Benefits

* Faster processing
* Horizontal scalability
* Better resource utilization

### Simple Explanation

Instead of one machine doing all the work, many machines work together to process data.

***

# What is a Cluster?

## Definition

A **cluster** is a group of computers (nodes) that work together to process large volumes of data.

### Cluster Management Includes

* Cluster setup
* Resource provisioning
* Monitoring
* Scaling
* Security configuration
* Maintenance

### Simple Explanation

A cluster combines multiple machines into one processing environment for handling big data workloads.

***

# Why is Databricks Easier than Spark?

## Apache Spark

When using Spark alone:

* You manage clusters manually.
* You configure infrastructure manually.
* You handle storage integrations.
* You monitor performance.
* You perform scaling operations.

### Challenges

* Requires dedicated manpower.
* Higher maintenance effort.
* Increased operational cost.

***

## Databricks

Databricks simplifies Spark usage by providing:

* Friendly User Interface
* Auto Cluster Management
* Collaborative Notebooks
* Optimized Connectors
* Governance Tools
* ML Lifecycle Support
* Delta Lake Integration

### Auto Cluster Management

Databricks allows cluster creation with just a few clicks.

Features include:

* Auto-scaling
* Auto-start
* Auto-termination
* Monitoring

### Simple Explanation

Databricks handles infrastructure-related tasks, allowing engineers to focus primarily on development and analytics.

***

# Why Do We Need Databricks if We Already Have Apache Spark?

## Apache Spark

Spark provides:

* Fast distributed processing
* Scalability
* In-memory computation

However, users must manage:

* Clusters
* Storage
* Security
* Integrations
* Monitoring

manually.

***

## Databricks

Databricks adds:

* Unified Workspace
* Auto Cluster Management
* Collaborative Development
* Native Integrations
* Delta Lake
* Governance Tools
* Machine Learning Support
* Performance Optimization

### Simple Explanation

Spark is powerful for processing data, while Databricks makes Spark easier to use at an enterprise level.

***

# Day 2

# Databricks vs Spark Alone

## 1. Setup and Infrastructure

### Spark Alone

You must:

* Install Spark
* Configure Spark
* Create clusters
* Manage infrastructure

Deployment can be:

* On-premise (company-owned servers)
* Cloud-based servers

### Databricks

* Fully managed platform.
* No manual setup required.
* Clusters can be created with a few clicks.

### Remember

**Databricks abstracts infrastructure complexity.**

***

## 2. Cluster Management

### Spark Alone

You must manually:

* Scale clusters up/down
* Monitor clusters
* Shut down clusters
* Manage resources

### Databricks

Provides:

* Auto-scaling
* Auto-termination
* Built-in monitoring
* Resource optimization

### Simple Explanation

Databricks automatically manages cluster resources based on workload requirements.

***

## 3. Data Storage

### Spark Alone

Can read/write from:

* Amazon S3
* HDFS
* Azure Blob Storage

However, Spark does not provide a built-in transactional layer.

### Databricks

Uses **Delta Lake** and provides:

* ACID Transactions
* Schema Enforcement
* Time Travel
* Reliable Storage Layer

***

# ACID Properties

## ACID = Atomicity + Consistency + Isolation + Durability

### Atomicity

Either all operations succeed or none of them succeed.

**Example:** If a transaction has 5 steps and step 4 fails, all previous steps are rolled back.

***

### Consistency

Data always remains in a valid state according to defined rules.

***

### Isolation

Multiple users can perform operations simultaneously without affecting each other's transactions.

***

### Durability

Once data is committed, it remains saved even if the system crashes.

***

## Remember

**ACID properties ensure data reliability and transactional consistency.**

***

# 4. Data Governance and Security

## Spark Alone

* Permissions handled manually.
* Access control managed at file or storage level.

## Databricks

Uses **Unity Catalog** for:

* Centralized Data Governance
* Access Control
* Auditing
* Compliance Management

### Simple Explanation

Unity Catalog provides one place to manage permissions and monitor data access.

***

# 5. Collaboration

## Spark Alone

* No built-in multi-user workspace.
* Scripts must be shared manually.

## Databricks

Provides:

* Shared notebooks
* Team collaboration
* Centralized development environment

### Simple Explanation

Multiple users can work on the same project without using separate tools.

***

# 6. Workflow Automation

## Spark Alone

Requires external schedulers.

### Apache Airflow

Apache Airflow is a workflow orchestration tool used to:

* Schedule workflows
* Manage pipelines
* Monitor tasks

### Cron

Cron is a lightweight scheduler used in Linux/Unix systems to run tasks automatically at specific intervals.

***

## Databricks

Provides a built-in scheduler with:

* Monitoring
* Retry Policies
* Alerts
* Job Scheduling

### Simple Explanation

Databricks eliminates the need for separate scheduling tools for many workloads.

***

# 7. Machine Learning

## Spark Alone

Uses **MLlib**.

Limitations:

* Basic ML functionality
* No experiment tracking
* No model registry
* No deployment management

***

## Databricks

Uses **MLflow** for complete ML Lifecycle Management.

### Features

* Experiment Tracking
* Model Registry
* Model Versioning
* Model Deployment

### Remember

**MLflow = End-to-End ML Lifecycle Management**

***

# 8. Performance Optimization

## Spark Alone

Performance tuning must be done manually.

Examples:

* Memory tuning
* Resource tuning
* Spark configurations

## Databricks

Provides:

* Auto Optimization
* Performance Enhancements
* Query Optimization

### Simple Explanation

Databricks automatically applies several optimizations to improve workload performance.

***

# 9. Integrations

## Spark Alone

Requires manual setup of:

* JDBC Drivers
* ODBC Drivers

for BI tools and databases.

***

## Databricks

Provides native connectors for:

* Power BI
* Tableau
* Looker
* Snowflake
* Other Enterprise Systems

### Remember

**Databricks offers better integration capabilities with analytics and reporting tools.**

***

# Day 3

# Databricks Overview

## Workspace

The **Workspace** is the main development area in Databricks.

Most development activities are performed here.

### Workspace → Users

Under Users, developers can:

* Create notebooks
* Organize folders
* Develop solutions
* Manage project files

***

## Notebooks

Databricks notebooks support multiple languages:

* Python
* SQL
* Scala
* R

### Uses

* Data Processing
* Analytics
* ETL Development
* Machine Learning

***

## Compute Requirement

To execute code, a compute resource is required.

### Serverless Compute

Databricks provides **Serverless Compute**.

Benefits:

* No infrastructure management
* Faster startup
* Easy execution

### Free Edition

A default Serverless option is available for processing workloads.

***

## Notebook Options

### Clone

Creates a copy of an existing notebook.

Useful when:

* Reusing code
* Creating templates
* Testing changes separately

***

# Unity Catalog

## Definition

**Unity Catalog** is Databricks' centralized governance solution.

### Features

* View Data Assets
* Manage Data Assets
* Access Control
* Permission Management
* Governance

### Simple Explanation

Unity Catalog provides centralized management and governance of organizational data.

***

# Jobs & Pipelines

## Features

* Create jobs
* Schedule jobs
* Weekly scheduling
* Monthly scheduling
* Workflow automation

### Simple Explanation

Jobs and Pipelines help automate repetitive data engineering tasks.

***

# Genie

## Definition

**Genie** is an AI-powered capability available in Databricks.

***

# Day 4

# Databricks Lakehouse

## Definition

**Databricks Lakehouse** is a modern data architecture that combines the best features of both a **Data Lake** and a **Data Warehouse** in a single system.

### Formula

**Lakehouse = Cheap Storage + Fast Analytics + Reliable Data**

***

# Data Lake

## Characteristics

Stores:

* Structured Data
* Semi-Structured Data
* Unstructured Data

### Advantages

* Low Cost
* High Scalability
* Flexible Storage

***

# Data Warehouse

## Characteristics

Provides:

* Fast SQL Queries
* Strong Governance
* Reliable Data
* Business Analytics

***

# What Makes Lakehouse Possible?

## Delta Lake

Databricks Lakehouse is built on top of **Delta Lake**.

Delta Lake adds enterprise-grade reliability to a Data Lake.

***

# Delta Lake Features

## ACID Transactions

Provides safe and reliable data updates.

- Data Consistency

- Data Integrity

- Transactional Reliability

***

## Schema Enforcement

Prevents incorrect or unexpected data from being written.

### Benefit

Improves data quality.

***

## Time Travel

Allows users to:

* Access previous table versions
* Restore historical data
* Audit data changes

### Benefit

Supports debugging and data recovery.

***

## Faster Performance

Provides optimized storage and query execution for analytics workloads.

### Remember

**Delta Lake = Data Lake + Reliability**

***

# Problems Solved by Lakehouse

## 1. Data Silos

### Before Lakehouse

* Data stored in a Data Lake.
* Analytics performed in a separate Data Warehouse.
* Data copied between systems.

### Challenges

* Duplicate data
* Extra storage costs
* Complex ETL pipelines

### Lakehouse Solution

* Single platform
* No duplicate storage
* Fewer ETL pipelines
* Simplified architecture

### Simple Explanation

Lakehouse reduces data duplication and keeps analytics closer to the data.

***

## 2. Reliability Problems in Traditional Data Lakes

Traditional Data Lakes do not provide:

* ACID Transactions
* Schema Enforcement
* Version Control
* Time Travel

### Lakehouse Solution

Using Delta Lake provides:

* Reliable transactions
* Data validation
* Historical version access
* Better data quality

### Simple Explanation

Lakehouse makes Data Lakes suitable for enterprise-grade analytics.

***

## 3. Scalability and Cost Challenges

### Data Warehouse

* Fast analytics
* Expensive storage
* Mainly optimized for structured data

### Data Lake

* Low-cost storage
* Supports all data types
* May lack reliability features

### Lakehouse

Combines:

- Low-Cost Cloud Storage

- Fast SQL Analytics

- Enterprise Reliability

- High Scalability

- Delta Lake Capabilities

### Simple Explanation

A Lakehouse provides the cost benefits of a Data Lake and the performance benefits of a Data Warehouse in a single architecture.

# How Databricks Lakehouse Works Internally

Databricks Lakehouse is built using multiple layers that work together to provide **scalability, reliability, governance, and high-performance analytics**.

***

## 1. Data Storage Layer

### Definition

The **Data Storage Layer** is where the actual data is stored.

### Storage Locations

Databricks stores data in cloud object storage such as:

* **Amazon S3 (Simple Storage Service)**
* **Azure Data Lake Storage (ADLS)**
* **Google Cloud Storage (GCS)**

### Supported File Formats

Data can be stored in open formats such as:

* **Parquet**
* **JSON**
* **Avro**
* **ORC**

### Why Open Formats?

Benefits:

* Easy to access data.
* Better interoperability.
* No vendor lock-in.
* Compatible with multiple tools.

### Simple Explanation

The storage layer acts as the foundation of the Lakehouse where all data files are physically stored.

***

## 2. Delta Lake Layer (The Magic Layer)

### Definition

**Delta Lake** sits on top of the storage layer and adds reliability, governance, and transactional capabilities to the data.

### Transaction Log

Delta Lake maintains a transaction log called:

```text
_delta_log
```

This folder keeps track of all changes made to the data.

### What Delta Lake Provides

#### ACID Transactions

Ensures reliable and safe data operations.

Benefits:

* No partial writes.
* No corrupted updates.
* Consistent data.

***

#### Change Tracking

Delta Lake tracks every:

* Insert
* Update
* Delete

operation performed on the data.

***

#### Schema Enforcement

Prevents invalid or unexpected data from being written to tables.

### Example

If a column is defined as:

```text
salary = Integer
```

Delta Lake prevents writing:

```text
salary = ABC
```

This helps maintain data quality.

***

#### Schema Evolution

Allows schema changes when required.

Examples:

* Adding new columns
* Modifying schema in a controlled way

***

#### Time Travel

Allows users to access previous versions of data.

Benefits:

* Data recovery
* Auditing
* Historical analysis
* Easy debugging

### Simple Explanation

Delta Lake converts a normal Data Lake into a reliable and enterprise-ready storage system by adding transaction management, version control, and data quality checks.

***

## 3. Query & Compute Layer

### Definition

The Query & Compute Layer is responsible for processing and analyzing data.

### Supported Languages

Databricks allows processing data using:

* SQL
* Python
* PySpark
* Scala
* R
* Java

### Processing Engine

Databricks uses **Apache Spark** as the core distributed processing engine.

### Photon Engine

Databricks includes the **Photon Engine**, which provides:

* Faster SQL query execution
* Improved performance
* Optimized analytics workloads

### Workloads Supported

#### Batch Processing

Process historical data.

Examples:

* Daily sales reports
* Monthly transactions

***

#### Stream Processing

Process real-time incoming data.

Examples:

* IoT data
* Sensor data
* User activity logs

***

#### Machine Learning

Build and deploy ML models using Databricks and MLflow.

***

#### Business Intelligence (BI)

Connect BI tools for reporting and dashboard creation.

Examples:

* Power BI
* Tableau
* Looker

### Simple Explanation

The compute layer is where data is processed, transformed, analyzed, and queried using Spark and other supported technologies.

***

## 4. Governance & Security Layer

### Definition

Governance and Security ensure that data remains secure, controlled, and compliant.

### Unity Catalog

Databricks uses **Unity Catalog** as a centralized governance solution.

### Unity Catalog Features

#### Data Access Control

Manages who can:

* View data
* Modify data
* Delete data

***

#### Metadata Management

Stores information about:

* Tables
* Columns
* Schemas
* Data Assets

***

#### Data Lineage

Tracks:

* Where data comes from
* How data moves
* Which transformations were applied

### Why Data Lineage is Important?

It helps answer questions like:

> "Where did this report data come from?"

and

> "Which tables were used to create this dataset?"

***

#### Fine-Grained Security

Security can be applied at:

* Table Level
* Column Level
* File Level

### Simple Explanation

Unity Catalog provides centralized governance, security, visibility, and auditing across the entire Databricks platform.

***

# Advantages of Databricks Lakehouse

## 1. Unified Platform

### Definition

Databricks Lakehouse combines the capabilities of both a **Data Lake** and a **Data Warehouse** into a single platform.

### Benefits

* No need to maintain separate systems.
* Data storage and analytics happen in one place.
* Reduces architectural complexity.
* Simplifies data management.

### Simple Explanation

Traditionally, organizations stored data in a Data Lake and performed analytics in a separate Data Warehouse. Lakehouse brings both together into one platform.

***

## 2. Open Data Format

### Definition

Databricks stores data using open formats such as:

* **Parquet**
* **Delta Lake**

### Benefits

* Data remains accessible.
* Easy integration with other tools.
* No vendor lock-in.
* Better interoperability across platforms.

### Simple Explanation

Your data is not tied to a single vendor and can be accessed by multiple technologies.

***

## 3. ACID Transactions

### Definition

Delta Lake provides **ACID Transactions**, making data operations reliable and consistent.

### Benefits

* Safe updates
* No partial writes
* Data consistency
* Transaction reliability

### Simple Explanation

Data behaves like a traditional database, ensuring that updates are completed correctly.

### Remember

**ACID = Atomicity + Consistency + Isolation + Durability**

***

## 4. Time Travel

### Definition

**Time Travel** allows users to access historical versions of data.

### Benefits

* Query older data versions
* Restore previous versions
* Audit data changes
* Simplify debugging

### Simple Explanation

If data is accidentally modified or deleted, you can go back and access an earlier version.

### Remember

**Time Travel = View or Restore Historical Data**

***

## 5. High Performance

### Definition

Databricks Lakehouse is optimized for fast analytics and query execution.

### Performance Features

* Advanced Indexing
* Data Caching
* Photon Engine

### Benefits

* Faster SQL queries
* Improved analytics performance
* Reduced query execution time

### Simple Explanation

Databricks uses several optimization techniques to process large datasets quickly.

### Interview Keyword

**Photon Engine = High-Performance Query Engine for Databricks**

***

## 6. Cost Efficient

### Definition

Lakehouse combines inexpensive cloud storage with high-performance analytics.

### Benefits

* Lower storage cost
* Better resource utilization
* Reduced infrastructure expenses

### Simple Explanation

Organizations can store large volumes of data at low cost while still getting fast analytical performance.

### Remember

**Data Lake Cost + Data Warehouse Performance**

***

## 7. Supports All Workloads

### Definition

Databricks Lakehouse supports multiple types of workloads on a single platform.

### Supported Workloads

#### Business Intelligence (BI)

Examples:

* Power BI
* Tableau
* Looker

#### Machine Learning

Examples:

* Model Training
* Model Tracking
* Model Deployment

#### Streaming

Examples:

* Real-time Events
* IoT Data
* Clickstream Data

#### Batch ETL

Examples:

* Daily Data Loads
* Historical Processing
* Data Transformation Pipelines

### Simple Explanation

Instead of separate tools for analytics, ML, and streaming, everything can run on the same platform.

### Interview Keyword

**Multi-Workload Platform**

***

## 8. Scalable and Elastic

### Definition

Databricks leverages cloud infrastructure to automatically scale resources based on workload demand.

### Features

* Auto Scaling
* Elastic Compute
* Dynamic Resource Allocation

### Benefits

* Handles large workloads efficiently
* Optimizes cloud costs
* Improves performance during peak demand

### Simple Explanation

When workload increases, more resources are added automatically. When workload decreases, resources are reduced to save costs.

### How Databricks Lakehouse Works Internally

```text
                    Users
                       │
                       ▼
         Query & Compute Layer
      (Spark, SQL, Python, Photon)
                       │
                       ▼
             Delta Lake Layer
   (_delta_log, ACID, Schema Enforcement,
      Schema Evolution, Time Travel)
                       │
                       ▼
             Cloud Storage Layer
      (S3, ADLS, GCS, Parquet, JSON)
                       │
                       ▼
          Governance & Security
      (Unity Catalog, Lineage, Access Control)
```




