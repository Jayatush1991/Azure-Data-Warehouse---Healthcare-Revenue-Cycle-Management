
# Azure Data Warehouse - Healthcare Revenue Cycle Management

The **Azure Data Warehouse Healthcare Revenue Cycle Management (RCM)** project is designed around a metadata-driven architecture. Revenue Cycle Management refers to the end-to-end process that healthcare providers, such as hospitals, use to manage the financial aspects of patient care. This includes everything from the time a patient schedules an appointment to the moment the healthcare provider receives payment for services rendered.

The primary objective of this project is to monitor and analyze healthcare providers' accounts receivable (AR) metrics, while also building a profitability calculator. To achieve this, I have developed an automated data pipeline using the **Azure technology stack**, including **Azure Databricks** and **Azure Data Factory**. The pipeline operates based on metadata, leveraging a metadata-driven architecture for efficient and scalable data processing.

### Datasets Used in the Project:
- **EMR (Electronic Medical Records)**: Data from two different hospitals (Hospital A and Hospital B).
- **Claims Data**: Flat files containing claims information.
- **NPI Codes**: Unique identification numbers for healthcare providers and doctors. The NPI code is essential for tracking medical professionals within the system.
- **ICD and CPT Codes**: Standard codes used to identify medical diagnoses and procedures.

### Data Processing using Databricks Medallion Architecture

The project leverages the **Databricks Medallion Architecture** to refine, process, and optimize the data. This architecture ensures a structured approach for handling large volumes of healthcare data, making it easier to maintain data quality and consistency throughout the processing stages.

### System Architecture

The system architecture for this project is divided into two main parts:

- **Part 1**: Extract and move EMR data from an Azure SQL Database to the **Bronze Layer** (parquet files).
  
- **Part 2**: Implement a **Common Data Model (CDM)** with surrogate keys, perform data quality checks, and use **SCD Type 2 (Slowly Changing Dimension)** to filter out invalid or inconsistent data. This process standardizes naming conventions, ensures a consistent column structure, and maintains historical data for dimension tables as the data progresses through the layers.

For further details on the system architecture, please refer to the accompanying architecture diagram.



