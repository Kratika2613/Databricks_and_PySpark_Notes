# Databricks_and_PySpark_Notes
My learning notes for Databricks and PySpark.

# Day - 1 
# What is Databricks -
It is a one kind of unified analytics platform, that will help you - 
-- To manage your data, 
-- To process your data, 
-- To analyze your data into a one single place in a better way.

** imp **
It is built on top of Apache Spark but adds many enterprise features -
-- From the above line few people think like **Databricks** is just kind of the **environment for the Apache Spark**. But Databricks is not just a Apache Spark. It has many other features :-

1. Databricks is providing the one kind of workspace where data engineer, data analyst, data scientist, will work into a one single workspace.
-- They will create there own notebook.
-- They can see other's developer notebook.
-- They can work together and, they can share their tables.

-- It provides a collaborative workspace for data engineer, data analyst, data scientist.

2. Support for data lakes, data warehouse and machine learning.
-- Databricks provide **Data lakehouse** capability :-
-- This means it provide a capability of **data lake** as well as **data warehouse**.
-- DataLake means we can store structure, unstructure every kind of data into a data lake.
-- Because we've a lakehouse capability, so we can also use a data warehouse capability. So, that we can quickly do a analytics in a faster way.

3. Delta lake technology for reliablity, governance, and speed
-- Delta lake is a technology that makes data better and easier to manage.
-- Reliability means data is safe and accurate.
-- Governance means data is controlled and organized.
-- Speed means data is processed quickly.

# What is Apache Spark -
-- Apache Spark is an open-source distributed computing engine used to process large amount of data.
-- Very fast compared to older frameworks like Hadoop MapReduce.
-- Can run batch, streaming, SQL, ML, and graph workloads.
-- Requires you to manage clusters, storage, integrations, and scaling manually.

The Apache Spark will help us to process a large data set into a distributed (work is divided across many computers) manner. And, it process your data in a memory itself. So, it is very fast.

-- What is a cluster -
 A cluster is a group of computers that work together to process large amount of data.

 -- Managing cluster means setting up, monitoring, scaling, and maintaining those computers.

 -- Why is Databricks easier ?
 -- Apache Spark : You **manage the cluster yourself**.
 -- Databricks : Databricks ,**manages the cluster for you**, so you can focus on **writing Spark code**.

-- When we already have Apache Spark that help to process large datasets, then why do we need a Databricks ?
-- Spark - If we're using spark alone no databricks then, it is has fast distributed processing, but you must manage clusters (and, managing cluster is a kind of difficult thing, and the manpower is required, and it is costly also), storage, and integration manually.

-- Databricks - adds a firendly UI, auto-cluster management, collaborative notebook, optimized connectors(it provide connectors to connect to different databases), governance tools, ML lifecycle support, and Delta Lake for reliable data.
-- This means in databricks UI itself, we've one button to create a cluster (auto-cluster will be created). If we're not using cluster automatically it will be shutdown.

***********************************************************************************************************************************
# Day 2

1. Setup & infrastructure

-- Spark Alone -> 
- You have to install,
- configure,
- manage your own clusters (on-premise(means Company's own servers) or cloud(means servers on the internet managed by a cloud provider)).

-- Databricks ->
-- Fully managed service - just click to create clusters, no manual setup.

2. Cluster Management ->

-- Spark Alone -> You must manually scale up/down, monitor, and shut down clusters.
-- Databricks -> Auto-scaling clusters that start/stop based on workload to save cost.

3. Data Storage ->

-- Spark Alone -> Reads/writes from external storage (S3, HDFS, Azure Blob), but no built-in transactionasl layer.
-- Databricks -> Uses Delta Lake for ACID transactions, schema enforcement, and time travel.

-- ACID = ATOMICITY, CONSISTENCY, ISOLATION, DURABILITY
-- ATOMICITY -> Either everything happens or nothing  happens.
-- CONSISTENCY -> Data should always follow rules/valid state.
-- ISOLATION -> Multiple user can work at same time, but they don't disturb each other.
-- DURABILITY -> Once data is saved, it will not be lost even if system crashes.

4. Data Governance & Security ->

-- Spark alone -> You handle permission manually at the file system or storage leavel.
-- Databricks -> Unity Catalog provides centralized data access control, auditing, and compliance.

5. Collaboration ->

-- Spark alone -> No built-in multi user interface - sharing requires exporting scripts and  files.
-- Databricks -> Collaborative notebooks where multiple user can work together.

6. Workflow Automation ->

-- Spark Alone -> Requires external schedulers(**Airflow** - Apache Airflow is a tool used to schedule manage, and monitor complex data workflows (multiple tasks in order), **Cron** - it is a simple scheduler used to run tasks automatically at fixed time intervals in Linux/ Unix systems) for automation.
-- Databricks -> Built-in jobs scheduler with monitoring, retry policies, and alerts.

7. Machine Learning ->

-- Spark Alone -> MLib for basic ML, but no built-in experiment tracking or deployment tools.
-- Databricks -> MLflow integrated for ML lifecycle management (tracking, registry, deployment).

8. Optimization ->

-- Spark Alone -> you manually tune configuration for performance.
-- Databricks -> Auto-optimizations

9. Integrations ->

-- Spark Alone -- You set up JDBC/ODBC drivers manually for BI tools.
-- Databricks -- Native connectors to Power BI, Tableau, Looker, Snowflake, etc.

*************************************************************************************************************************************

# Day 3

- Creating Databricks Free edition Account

**Databricks Overview**
- On the left side panel we have :-

- Workspace : This is the main option in the workspace, where all our development work is done.
     -> Under workspace we have > Users
     -> In users option we try to create all kind of notebook, here only we write our PySpark code, and do all our development activity.
     -> Then, we have create option (on right side) > here we can create folder like..(practical).
     -> Under folder I can create any kind of notebook.
     -> Here we can write different kind of code like R language, Scala, python, SQL.

-- Now, if I want to execute any code I require a computation, a cluster.
-- So, on right hand side there is one option - Connect(Serverless)
-- Here in free edition by default a serverless is available that we can use for processing.

-- When I rename the notebook. If i right click on the notebook with name test or something. There are so many options.
-- Like: **clone** - creating similar kind of notebook.

-- **Unity Catalog** : Here we can see all our data.
                      -> In this we will be able to manage our data also.
                      -> In this I can also do access control.

-- **Jobs & pipelines** : Here we can create a job, and can also schedule them on weekly and monthly basis.

-- **Genie** : It is an AI.

********************************************************************************

# Day 4

-- What is the Databricks Lakehouse ?

-- 


