# 🎬 Data Pipeline: Movie Metadata & Ratings Integration  

This project builds an end-to-end **ETL (Extract, Transform, Load)** data pipeline to integrate movie metadata stored in a relational database and user ratings stored in a CSV file. The pipeline is implemented using **Apache Spark** for data processing and **PostgreSQL** as the target data warehouse.  

---

## 📌 Problem Statement  
The data required for analysis is scattered across different sources:  
- **Movie Metadata** → stored in a **relational database table** (`movies_metadata`)  
- **User Ratings** → available in a **CSV file** (`ratings.csv`)  

To perform meaningful analysis, these datasets need to be extracted, transformed, and loaded into a single target database with proper logging for traceability.  

---

## 🔑 Components of the Pipeline  

### 1. Extract Data  
- Read `movies_metadata` from the relational database.  
- Read `ratings.csv` from a flat file.  
- Use **Apache Spark** to extract both datasets.  

### 2. Source to Target Mapping  
- Define the **mapping rules** between source fields and target schema.  
- Ensure data types and keys align before transformation.  

### 3. Transform Data  
- Apply business logic and transformations using Spark:  
  - Data cleaning (null handling, type casting, etc.)  
  - Join datasets (ratings with metadata)  
  - Derive additional attributes if required.  

### 4. Load Data  
- Load the transformed data into **PostgreSQL** database for further use.  

### 5. Log Process  
- Store execution logs (`info.log`) for:  
  - Data extraction status  
  - Transformation rules applied  
  - Load success/failure  
- Logs provide **traceability** and help with debugging.  

---

## ⚙️ Tools & Technologies  
- **Apache Spark** → Data extraction & transformation  
- **PostgreSQL** → Target data storage  
- **CSV** → Input flat file format  
- **Python** → Function-based pipeline implementation  
- **Logging** → Process tracking  

---

## 📂 Pipeline Workflow  

1. Extract data from CSV (`ratings.csv`) and database (`movies_metadata`).  
2. Apply source-to-target mapping.  
3. Transform data as per business requirements.  
4. Load transformed data into PostgreSQL.  
5. Log each step in `info.log`.  

---
