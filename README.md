# Football Stadium Data Pipeline with Apache Airflow and Azure Data Factory

This project automates the process of collecting, cleaning, and processing data about football stadiums from Wikipedia. The pipeline is built using Apache Airflow to orchestrate tasks, and the data is stored and processed in Azure Data Lake, enabling further analytics and reporting through tools such as Azure Synapse Analytics and Power BI.

## Project Architecture
![digram](https://github.com/aadhil96/Football_Stadium_Data_Pipeline_with_Apache_Airflow_Azure/blob/c375117322b8c44025867dd40c8c09f973540681/Diagram.jpg)

## Key Technologies
- **Python**: For web scraping and data processing.
- **Apache Airflow**: Workflow orchestration and task scheduling.
- **Docker**: Containerization of the Airflow setup.
- **PostgreSQL**: For intermediate data storage and management.
- **Azure Data Lake Storage**: Data storage for raw and processed data.
- **Azure Data Factory**: For orchestrating the movement of data.
- **Azure Databricks**: For further data exploration and processing.
- **Azure Synapse Analytics**: For large-scale data analytics.
- **Power BI**: For data visualization and reporting.

## Project Workflow
### 1. Web Scraping (Data Ingestion)
- The pipeline begins with **Apache Airflow** running a Python-based web scraper to extract data about football stadiums from Wikipedia.
- The scraping task collects relevant information (e.g., stadium name, location, capacity, etc.) and stores the raw data in **PostgreSQL** on an **Azure Linux Virtual Machine**.

### 2. Data Cleaning & Transformation
- The extracted data is cleaned and transformed using **Python** scripts within **Airflow**.
- Airflow manages tasks to transform the data into a structured format suitable for further processing.

### 3. Data Storage (Azure Data Lake)
- The cleaned data is moved to **Azure Data Lake** for persistent storage.
- The data is split into two categories:
  - **Landing Data**: Raw, unprocessed data.
  - **Processed Data**: Cleaned and transformed data ready for analytics.

### 4. Data Orchestration (Azure Data Factory)
- **Azure Data Factory (ADF)** copies the data from the landing zone to the processed data zone within the data lake, enabling the ETL (Extract, Transform, Load) process.

### 5. Data Exploration (Azure Databricks)
- Data engineers and analysts can explore and model the processed data using **Azure Databricks** for further insights.

### 6. Data Analytics (Azure Synapse Analytics)
- The processed data is loaded into **Azure Synapse Analytics (SQL)** for large-scale analysis, enabling complex querying and reporting.

### 7. Data Reporting (Power BI)
- The final insights and reports are visualized using **Power BI**, where the data from **Azure Synapse** is presented in dashboards for decision-makers.

## Prerequisites

Ensure the following are set up before running the pipeline:
- **Python 3.x** installed locally
- **Docker** installed for containerizing Airflow
- **Apache Airflow** installed or running in a Docker container
- An **Azure Account** with access to:
  - Azure Virtual Machines
  - Azure Data Lake Storage
  - Azure Data Factory
  - Azure Databricks
  - Azure Synapse Analytics
  - Power BI for visualization

## Project Screenshots

## Azure Data Lake Storage
![data](https://github.com/aadhil96/Football_Stadium_Data_Pipeline_with_Apache_Airflow_Azure/blob/77524220042b2a5a4e87566aba30fca552ebcc8f/Azure%20Storage.JPG)

## Azure Data Factory
![adf](https://github.com/aadhil96/Football_Stadium_Data_Pipeline_with_Apache_Airflow_Azure/blob/77524220042b2a5a4e87566aba30fca552ebcc8f/ADF.JPG)

## Azure Synapse Analytics
![sys](https://github.com/aadhil96/Football_Stadium_Data_Pipeline_with_Apache_Airflow_Azure/blob/77524220042b2a5a4e87566aba30fca552ebcc8f/Synapse.JPG)
