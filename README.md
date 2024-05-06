# Project
To generate BPM Workout Summary and Gym Summary of the registered users for a Wearable Device Manufacturing Company.

## High Level Requirements:
1. Collect and ingest data from the source system to lakehouse platform.
2. Design and Implement a Secure Lakehouse Platform using Medallion Architecture for a dev environment,
3. Prepare following analysis datasets for the data consumers
4. Generate Workout BPM Summary
5. Generate GYM Summary


## Data Schema
### ![Registration](assets/Registration.png)
### ![User Profile](assets/UserProfile.png)
### ![BPM Stream](assets/BPM Stream.png)
### ![Gym_Login_Logout](assets/Login_Logout.png)
### ![Workout_Session](assets/workout_session.png)
### ![BPM_Workout_Gym_Summary](assets/BPM_Workout_Gym_Summary.png)

# Tech Stack:
- Storage: Azure Storage (ADLS Gen2)
- Compute: Azure Databricks
- Language: Pyspark (python 3.10)
- CI/CD: Azure Devops

# Designs:
## Storage Design
![Storage Design](assets/Storage_Design.png)

## Security Design
![Security Design](assets/Implement_Data_Security.png)

## Resource Policies:
![Resource Policies](assets/Implement_resource_policies.png)

## Steps to Implement in Azure Databricks Lakehouse:
![Lakehouse](assets/Implement_Lakehouse_Infrastructure.png)

## Medallion Architecture: Tables Created in Databricks
![Medallion Architecture](assets/Medallion_Architecture.png)

# Work Done
- Created storage containers in ADLS Gen2 to store metadata, managed and unmanaged tables.
  ![storagecontainers](assets/storagecontainers.png)
  
- Created Catalog and External Locations needed for Managed and Unmanaged
  ![catalog](assets/catalog.png)
  
  ![external_locations](assets/external_locations.png)
  
- Supported Batch and Streaming Workflows to ingest data from source system to lakehouse.
- Created Metastore for dev workspace in Azure Databricks
  ![metastore](assets/metastore.png)
  
  ![workspace](assets/workspace.png)
  
- Written pyspark notebooks in databricks to implement Medallion Architecture by creating bronze, silver and gold layer tables.
  ![azure-databricks](assets/azure-databricks.png)
  
- Automated Integration testing to check the process.
- Committed the notebooks to Azure Devops.
  ![devops](assets/devops.png)
  
- Automated deployment pipeline for development environment in Azure Devops.
  
