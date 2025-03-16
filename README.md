# Azure-End-to-End-Data-Engineering-Project

## Overview
This project demonstrates an end-to-end Data Engineering workflow using Azure technologies. The pipeline is built using **Azure Data Factory, Databricks, PySpark, Delta Lake, and Unity Catalog**, leveraging the **Medallion Architecture** to efficiently process and store data.

## Technologies Used
- **Azure Data Factory**: For data ingestion from various sources
- **Azure Databricks**: For data transformation using PySpark
- **Azure Data Lake Gen2**: For efficient data storage
- **Delta Lake & Delta Tables**: For ACID transactions and data versioning
- **Unity Catalog**: For data governance and access control
- **Power BI**: For visualization and reporting

## Architecture
The project follows the **Medallion Architecture**, which consists of three layers:
1. **Bronze (Raw Data Store)**: Stores raw data in **Parquet** format.
2. **Silver (Transformed Data)**: Data is cleaned and transformed using **Databricks**.
3. **Gold (Serving Layer)**: Data is stored in **Delta Lake** using **Star Schema** for analytical reporting.

## Data Pipeline Flow
1. **Ingestion**:
   - Data is extracted from an **SQL source** using **Azure Data Factory**.
   - Data is stored in **Azure Data Lake Gen2** as raw **Parquet** files.
2. **Transformation**:
   - Data is processed using **Databricks (PySpark)**.
   - Unity Catalog is used for data governance.
   - Data undergoes transformations such as **Dimensional Data Modeling** and handling **Slowly Changing Dimensions (SCDs)**.
3. **Serving**:
   - The transformed data is loaded into the **Gold layer (Delta Lake)**.
   - Data is structured using a **Star Schema** for reporting.
4. **Visualization**:
   - Processed data is visualized using **Power BI** for insights and business reporting.

## Key Features
- **Incremental Data Processing** for efficient handling of updates.
- **One Big Table (OBT) Approach** to optimize queries.
- **Security & Access Control** using Azure services.
- **CI/CD Integration** using GitHub for version control.


## Setup Instructions
1. Clone the repository:
   ```sh
   git clone https://github.com/HareenaChowdary/Azure-End-to-End-Data-Engineering-Project.git
   ```
2. Configure Azure services (Data Factory, Databricks, Data Lake).
3. Run the Data Factory pipeline for ingestion.
4. Execute the Databricks notebooks for transformation.
5. Use Power BI for visualization.


---

