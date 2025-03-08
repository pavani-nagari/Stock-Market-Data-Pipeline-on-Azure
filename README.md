# Stock-Market-Data-Pipeline-on-Azure
This project demonstrates how to build a real-time data pipeline for stock market data using various Azure services. The pipeline ingests, processes, stores, and visualizes stock data from real-time streams and historical data.

# Real-Time Stock Market Data Pipeline on Azure

This project showcases my implementation of a **real-time stock market data pipeline** using various **Azure services**. The pipeline ingests, processes, stores, and visualizes real-time stock data, enabling accurate predictions and insights for financial decision-making.

---

### **Technologies Used:**

- **Azure Data Factory (ADF)**
- **Azure Databricks (PySpark)**
- **Azure Data Lake Storage Gen2 (ADLS)**
- **Azure Event Hubs**
- **Azure Stream Analytics**
- **Azure SQL Database**
- **Power BI**
- **Python (for data processing and automation)**

---

### **Project Overview:**

I built this end-to-end data pipeline to handle **real-time stock market data** by ingesting data from APIs, processing it, storing it in Azure, and analyzing it. The processed data was visualized using Power BI for better decision-making.

---

### **Project Structure:**

1. **Data Ingestion**
2. **Real-Time Data Processing**
3. **Data Transformation & Aggregation**
4. **Data Visualization**
5. **Automation & Monitoring**

---

## Step-by-Step Guide

### **Step 1: Set Up Azure Blob Storage for Raw Data**

- **Objective**: Store stock market data from APIs and historical data in Azure Blob Storage.
- **Actions**:
  1. Created an **Azure Blob Storage** account.
  2. Created **containers** within Blob Storage to store raw CSV files and API responses.
  3. Configured **Azure Data Factory (ADF)** pipelines to fetch data from APIs (e.g., Alpha Vantage, Yahoo Finance) into Blob Storage.

### **Step 2: Set Up Azure Data Factory (ADF) for Data Ingestion**

- **Objective**: Automate data ingestion.
- **Actions**:
  1. Set up **Azure Data Factory** instance.
  2. Developed **ADF Pipelines** to:
     - Use **REST API connectors** to pull real-time stock data.
     - Schedule data ingestion at regular intervals (e.g., every minute).
  3. Stored the fetched data in **Azure Blob Storage** for further processing.

### **Step 3: Set Up Azure Event Hubs for Real-Time Data Streaming**

- **Objective**: Capture live stock market data and process it in real-time.
- **Actions**:
  1. Set up an **Azure Event Hubs** namespace.
  2. Created a **consumer group** to ingest stock data streams.
  3. Configured data pipeline to send stock data streams from APIs to Event Hubs.

### **Step 4: Set Up Azure Stream Analytics for Real-Time Processing**

- **Objective**: Perform real-time analytics on the data.
- **Actions**:
  1. Set up **Azure Stream Analytics** job.
  2. Defined **input sources** as Event Hubs.
  3. Wrote **SQL-like queries** to:
     - Aggregate data (e.g., calculate stock price averages).
     - Perform **time-series analysis** and **predictive modeling**.
  4. Stored the results in **Azure Data Lake Storage (ADLS) Gen2** for further analysis.

### **Step 5: Process Data in Azure Databricks (PySpark)**

- **Objective**: Clean, transform, and analyze stock market data using Databricks.
- **Actions**:
  1. Set up an **Azure Databricks workspace**.
  2. Used **PySpark** notebooks to:
     - Load data from **Azure Data Lake Storage**.
     - Clean and preprocess data (remove outliers, handle missing values).
     - Implemented **time-series analysis** and **stock forecasting models** (optional: implemented LSTM for stock price prediction).
  3. Saved the processed data into **Azure SQL Database** for querying.

### **Step 6: Set Up Azure SQL Database for Data Storage**

- **Objective**: Store structured data for querying.
- **Actions**:
  1. Created an **Azure SQL Database**.
  2. Designed tables to store processed stock data.
  3. Wrote SQL queries to aggregate, summarize, and report on stock data.

### **Step 7: Create Power BI Dashboards for Data Visualization**

- **Objective**: Build interactive dashboards to visualize stock price data.
- **Actions**:
  1. Connected **Power BI** to **Azure SQL Database**.
  2. Created interactive reports with:
     - **Line charts** for stock prices over time.
     - **Bar charts** for performance metrics.
     - Real-time updates for stock prices.
     - **Predictive insights** based on historical and forecasted data.
  3. Published the dashboard to provide actionable insights.

### **Step 8: Automation and Monitoring**

- **Objective**: Automate the pipeline and monitor its performance.
- **Actions**:
  1. Automated data ingestion and processing using **Azure Data Factory** pipelines.
  2. Set up **Azure Monitor** to track the pipeline, Stream Analytics jobs, and Databricks clusters.
  3. Created alerts for any failures or anomalies.


