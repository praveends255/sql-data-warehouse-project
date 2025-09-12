# 📊 Data Architecture

## 📌 Overview  
Data architecture defines how data is collected, stored, processed, and consumed across systems.  
It ensures that data flows smoothly from **sources** into a **data warehouse** where it is transformed into valuable insights and finally **consumed** by business tools.  

---

## 📌 End-to-End Flow  

| Stage | Object Type | Load Method | Transformation | Data Model | Usage |
|-------|-------------|-------------|----------------|------------|-------|
| **Sources (CRM, ERP)** | CSV Files | Files in Folder | ❌ None | N/A | Data Ingestion |
| **Bronze (Raw Data)** | Tables | Batch Processing, Full Load, Truncate & Insert | ❌ None | As-is | Staging Layer |
| **Silver (Cleaned, Standardized Data)** | Tables | Batch Processing, Full Load, Truncate & Insert | ✔ Data Cleansing, Standardization, Enrichment | None (As-is) | Curated Layer |
| **Gold (Business-Ready Data)** | Views | No Load | ✔ Data Integration, Aggregation, Business Logic | Star Schema, Flat Table, Aggregated Table | Analytics Layer |
| **Consume** | N/A | N/A | N/A | N/A | BI & Reporting, Ad-hoc SQL Queries, Machine Learning |

---

## 📌 Key Definitions  

- **CRM (Customer Relationship Management):** A system used to manage interactions with customers, often providing sales and marketing data.  
- **ERP (Enterprise Resource Planning):** A system that manages business processes such as finance, HR, and supply chain.  
- **Bronze Layer:** Stores raw ingested data in its original format without transformation.  
- **Silver Layer:** Contains cleaned and standardized data, making it consistent and enriched for downstream use.  
- **Gold Layer:** Business-ready data optimized for analytics, reporting, and decision-making.  
- **Consume Layer:** The final stage where data is used in BI tools, SQL queries, or machine learning models.  

