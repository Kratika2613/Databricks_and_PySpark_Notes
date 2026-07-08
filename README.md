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

✅ Data Consistency

✅ Data Integrity

✅ Transactional Reliability

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

