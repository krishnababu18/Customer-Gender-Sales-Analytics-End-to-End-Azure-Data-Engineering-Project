# Azure Gender Sales Analytics (End-to-End Data Engineering Project)

## 📌 Project Overview
This project demonstrates an **end-to-end Azure Data Engineering pipeline** designed to analyze **customer demographics and sales behavior**, focusing on **gender distribution and product categories**.  

The main goal is to build a **KPI dashboard** that shows:
- **Total Products Sold**
- **Total Sales Revenue**
- **Customer Gender Split**
- **Sales by Gender × Product Category**  
with filters for **Category, Gender, and Date Range**.

---

## 🛠️ Tech Stack
- **Source:** On-Prem SQL Server  
- **Orchestration:** Azure Data Factory (ADF)  
- **Storage:** Azure Data Lake Storage Gen2 (Bronze → Silver → Gold layers)  
- **Transformations:** Azure Databricks (PySpark, Delta)  
- **Warehouse:** Azure Synapse Analytics  
- **Visualization:** Power BI  
- **Security & Governance:** Entra ID (IAM/RBAC), Key Vault (secrets), Purview (optional for lineage)  

---

## ⚙️ Architecture

On-Prem SQL Server
       │
       ▼
Azure Data Factory (Ingestion via Self-Hosted IR)
       │
       ▼
Azure Data Lake Storage Gen2
   ├─ Bronze (raw data)
   ├─ Silver (cleaned & standardized)
   └─ Gold (curated analytics / star schema)
       │
       ▼
Azure Databricks (Transformations with PySpark & Delta Lake)
       │
       ▼
Azure Synapse Analytics (Warehouse & Views)
       │
       ▼
Power BI Dashboard (KPIs, Gender Split, Filters)


## 📊 Business Value
- Identify **who is buying what** (male vs. female purchase trends).  
- Enable **data-driven marketing** and product decisions.  
- Provide **real-time insights** through Power BI.  
- Standardize storage using **Medallion Architecture** (Bronze/Silver/Gold).  

---

## 🚀 Current Status
✅ Project initialized  
🔄 Working on pipelines and transformations (updates coming soon)  
📊 Power BI dashboard design in progress  

---

## 🔮 Next Steps
- [ ] Ingest data from On-Prem SQL → ADLS Bronze using ADF  
- [ ] Transform Bronze → Silver/Gold with Databricks (Delta)  
- [ ] Load Gold data into Synapse Analytics  
- [ ] Build Power BI dashboard (KPIs, filters, slicers)  
- [ ] Implement RBAC + Key Vault integration  
- [ ] (Optional) Add lineage with Purview  

---

