# Azure-Olympic-Data-Engineering-Project

## Introduction
This project performs the Data engineering pipeline implementation for Olympic data using Microsoft Azure services. This projects helps to understand the implementation of data injestion, storage, transformation, analysis and visualization of olympic-data

## Project Overview
This project uses the 2021 Tokyo Olympics data from Kaggle. This dataset provides information about Tokyo Olympics, including details on athletes, coaches, events, and medal outcomes.

## Architecture
![Architecture Diagram](https://github.com/flynnRider046/Azure-Olympic-Data-Engineering/blob/edb5d63ba24c032ddc57b155c58503190880de76/Images/Architecture%20diagram.png)
The project leverages the following Azure services:
* Data Azure Factory
* Azure Data Lake Storage Gen2
* Azure Databricks
* Azure Synapse Analytcis

The data flows through following stages:
1. <strong>Data Source</strong>: The source of the data is 2021 Olympic dataset that is present in Kaggle.
2. <strong>Storage Account</strong>: Storage accounts are configured to provide a secure and scalable environment for storing large amounts of data.
3. <strong>Resource groups and Linked Services</strong>: Resource groups and linked services are configured in Azure to manage the connections between different services used in the project.
4. <strong>Data Ingestion</strong>: Data from kaggle is ingested to Azure Data Factory, here the data is prepared for processing.
5. <strong>Raw Data Storage</strong>: The ingested data is stored in Azure Data Lake Gen2 for easy access and management.
6. <strong>Data Transformation</strong>: With the help of Azure Databricks, data is transformed. Various operations are performed to clean the data.
7. <strong>Transformed Data Storage</strong>: For further analysis, the transformed data is stored in Azure Data Lake Gen2.
8. <strong>Analytics</strong>: The data is analyzed through Azure Synapse Analytics to generate insights.

## Technologies Used
* Microsoft Azure
* Python
* SQL
* Azure Data Factory
* Azure Databricks
* Azure Synapse Analytics

## DataSource
The project data is used from Kaggle
* <strong>DataSet</strong>: [2021 Tokyo Olympic Data](https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo)
The dataset involves multiple files with information about
* Athletes
* Coaches
* Gender-wise entries
* Medal stats
* Team compositions

## Data Ingestion Pipeline (Kaggle to Data Factory)
The data ingestion pipline in Azure Data Factory includes multiple datasets whicha re Athletes, Coaches, Gender-wise entries, Medal stats and Team compositions.

## Storage Accounts
Setting up the Azure Storage accounts 
* 




