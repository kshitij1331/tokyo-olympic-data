# 🥇 Tokyo Olympics Data Engineering Project

An **end-to-end Azure Data Engineering Project** to build a **modern data pipeline** for the **Tokyo Olympics dataset** using:

- **Azure Data Factory (ADF)**
- **Azure Data Lake Storage (ADLS)**
- **Azure Databricks (Spark)**
- **Azure SQL Database**
- **Power BI** for reporting
---

## 📌 Project Overview

This project demonstrates **modern Azure data engineering practices** with:

✅ Raw to curated data ingestion using **ADF**  
✅ Layered storage in **ADLS Gen2** following medallion architecture (Raw → Bronze → Silver → Gold)  
✅ Data cleaning and transformation using **PySpark in Databricks**  
✅ Structured storage in **Azure SQL Database**  
✅ Insightful dashboards in **Power BI**

---

## 📂 Folder Structure

```plaintext
tokyo-olympic-data/
├── data/            # Sample Tokyo Olympics datasets (CSV)
├── notebooks/       # Databricks PySpark notebooks
├── adf_pipelines/   # JSON exports of ADF pipelines
└── README.md

```

---

## 🚀 Architecture
<img width="1920" height="1080" alt="DE-Project-FLOW (2)" src="https://github.com/user-attachments/assets/462b35c4-1470-48d8-bbaf-5ddd5e23aea3" />



1️⃣ **Ingestion (ADF)**  
- CSV data loaded from local or blob → ADLS Gen2 (raw zone).

2️⃣ **Processing (Databricks)**  
- Data transformation using PySpark:
  - Clean nulls
  - Standardize column names
  - Join datasets for medal summary

3️⃣ **Loading (ADF)**  
- Transformed data moved to **Azure SQL Database** using ADF.

4️⃣ **Visualization (Power BI)**  
- Power BI dashboards connected to Azure SQL, providing insights on:
  - Medal counts by country
  - Sports-wise analysis
  - Gender-wise medal breakdown

---

## 🛠️ Tech Stack

- **Azure Data Factory:** Orchestration and pipelines.
- **Azure Data Lake Storage Gen2:** Storing raw and processed data.
- **Azure Databricks:** Data transformation with PySpark.
- **Azure SQL Database:** Serving structured, curated data.
- **Power BI:** Dashboarding and reporting.

---

## ⚙️ Steps to Reproduce

### 1️⃣ Provision Azure Resources:
- Create **ADLS Gen2** storage account.
- Set up **Azure SQL Database**.
- Set up **Azure Databricks workspace**.
- Set up **Azure Data Factory**.

### 2️⃣ Upload Data:
- Place Tokyo Olympics CSV data into `raw/` container in ADLS.

### 3️⃣ Configure ADF:
- Create linked services for ADLS, Databricks, and SQL.
- Create pipelines for:
  - Ingesting CSV → ADLS raw.
  - Triggering Databricks notebooks.
  - Copying processed data → Azure SQL Database.

### 4️⃣ Data Transformation:
- Develop Databricks PySpark notebooks for cleaning and transforming data.
- Write outputs to the `gold/` layer in ADLS.

### 5️⃣ Azure SQL Table:
- Create required tables for storing the processed data.
- Use ADF to load cleaned data into Azure SQL Database.

### 6️⃣ Power BI Reporting:
- Connect Power BI to Azure SQL.
- Build dashboards for data insights and presentation.

---

## 📊 Example Visuals

- **Top 10 Countries by Medal Count**
- **Medal Trends Over Time**
- **Athletes Distribution by Sport**
- **Gender-wise Medal Distribution**

---

## 🎯 Learning Outcomes

✅ Practice **Azure Data Engineering workflows**  
✅ Understand **medallion architecture (Raw → Bronze → Silver → Gold)**  
✅ Hands-on with **ADF orchestration**  
✅ PySpark transformations in **Databricks**  
✅ Building dashboards with **Power BI** connected to Azure SQL

---

## 📎 References

- [Tokyo Olympics Dataset (Kaggle)](https://www.kaggle.com/datasets/the-guardian/olympic-games)
- [Azure Data Factory Documentation](https://learn.microsoft.com/en-us/azure/data-factory/)
- [Azure Databricks Documentation](https://learn.microsoft.com/en-us/azure/databricks/)
- [Power BI Documentation](https://learn.microsoft.com/en-us/power-bi/)

---

## 🤝 Contributing

Contributions for enhancements, visuals, or pipeline optimizations are welcome! Please open a pull request or raise an issue for discussion.

---
⭐ **If you found this project helpful, please give this repository a starr**

