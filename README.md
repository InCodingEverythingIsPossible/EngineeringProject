# 📊 Financial Data Pipeline with Databricks & Polygon.io

## Overview

This project implements a complete data engineering pipeline that imports financial data from the [Polygon.io](https://polygon.io) API and processes it using the **Bronze-Silver-Gold** architecture within **Databricks**.

---

## 🔧 Pipeline Stages

### 1. **Data Ingestion (Bronze)**
- Raw financial data is ingested from REST endpoints (e.g., stock prices, dividends, financial data).
- Data is stored in JSON format in the Bronze layer of the data lake.

### 2. **Data Cleaning & Transformation (Silver)**
- Datasets are validated, cleaned, and enriched.
- Joins and calculations are performed to prepare the data for analytics.
- Data is stored in Delta format in the Silver layer of the data lake.

### 3. **Aggregations & Business Logic (Gold)**
- Final tables are created for analysis and visualization.
- Data is aggregated and filtered for high-quality investment candidates.
- Data is stored in Delta format in the Gold layer of the data lake.

---

## 🧠 Company Evaluation Logic

The project applies a value investing approach inspired by:
- **Warren Buffett**
- **Benjamin Graham**

Companies are scored based on their fundamentals, price history, and dividend performance. Only those passing the evaluation are selected for reporting.

---

## 📈 Outputs & Reporting

For companies that meet the investment criteria, the following are generated:
- 📉 **Price Chart**
- 🕯️ **Candlestick Chart**
- 💰 **Dividends Chart**
- 📊 **Evaluation Summary Tables**

These are automatically compiled and **emailed** to the end user as part of the scheduled workflow.

---

## 🚀 Technologies Used

- **Databricks (PySpark, Delta Lake)**
- **Polygon.io API**
- **Azure Key Vault** – for storing the Polygon API key and service principal credentials
- **Service Principal** – used to authenticate and mount ADLS2 to Databricks
- **Managed Identity** – used for all other services and secure access
- **Databricks Workflows (Jobs)**
- **Email Automation (Logic App)**
- **Lakehouse Architecture (Bronze / Silver / Gold)**

---

## 📬 Contact

For questions or collaboration, feel free to reach out!
