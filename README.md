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
The first step in the pipeline is setting up azure storage account. This storage account provides secure and scalable environments for storing large amounts of data.
![Storage Account](https://github.com/flynnRider046/Azure-Olympic-Data-Engineering/blob/7720ec3e6b361b591d3f506b7ee9a06d02c70c20/Images/Storage%20Account.png)

## Containers
Storage containers are used for the seperation of different datasets related to 2021 Tokyo Olympics. This is performed to make sure that the data remains organized and easily accessible. Because of this seperation, we can manage ingestion, processing and storage of raw and transformed data. 
The below is the storage accounts used for this project.
![Storage containers](https://github.com/flynnRider046/Azure-Olympic-Data-Engineering/blob/6eb45afbc7b2c222caf81e94a030dbf4aff3d27c/Images/Storage%20Containers.png)

## Linked Services and Resource Groups
These are configured in Azure to manage connections between different services used in the project. Ensure to setup the linked services and resource groups wherever required during the pipeline execution steps.

## Resource Groups
Resource groups are used here to efficiently organize and manage all the azure services associated with olympic data engineering pipeline. By grouping the resources together, we can simplyfy management tasks, streamline deployment processes, enforce access permissions based on project requirement. 
Following image depicts the setup of resource groups used for this project.

## Data Ingestion
Once the storage account is setup, data from Kaggle is ingested to Azure Data Factory. The ingestion process allows for the automated transfer of CSV files to Azure.

## Raw Data Storage (Azure Data Lake Gen2)
After ingestion, the raw data is stored in Azure Data Lake Gen2, which is basically a central repository for both the structred and unstructured data. 

## Data Transformation (Azure Databricks)
The raw data is processed and transformed using Azure Databricks. Here the process like data cleaning, normalization and other transformation tasks are performed. 

## Transformed Data Storage (Azure Data Lake Gen2)
The transformed data is stored back in Azure Data Lake Gen2, making it available for data analytics and further processing.

## Analytics (Azure Synapse Analytics)
The stored data is analyzed using Azure Synapse Analytics, which gives out powerful analytical capabilities for gaining proper insights from data.

## Insights and Analytics
1. <strong>Number of Athletes from each country</strong>:
   * This analysis provides total number of participating athletes representing each country at the 2021 Tokyo Olympics, ranked by their participation.
   * <strong>insight</strong>: With more number of athletes from the country could indicate stronger investment in sports and a good sports infrasturcture. This data reflects the country's size, population and overall sports structure.
2. <strong>Total medals won by each country</strong>:
   * With this analysis, we can aggregate the total number of gold, silver and bronze medals won by each country, allowing for a comparative understanding of thier success in the olympics.
   * <strong>insight</strong>: A higher total medal count suggests a country's strength accross various sports. The data can also highlight specific areas where the country excels and may guide future sports funding and development activities.
3. <strong>Average number of entries by gender for each discipline</strong>:
   * This analysis evaluates the average number of male and female entries for each Olympic discipline, providing insights into gender representation in different sports.
   * <strong>insight</strong>: Understanding gender participation can identify sports with disparities between male and female athletes, informing efforts to promote inclusivity and gender equity in athletics.

## Summary of Insights
* The athlete count provides a snapshot of the sporting strength and investment level of various countries.
* The medal tally serves as a key performance indicator, reflecting each country’s competitive edge in specific sports disciplines.
* The gender entry averages highlight participation trends and can guide initiatives aimed at increasing female or male representation in various sports.






