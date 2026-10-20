# Data Warehouse Project

This project demonstrates a data warehousing solution built with SQL Server, from raw source files to a business-ready analytical model.

> **Credit:** This project was designed by [Data With Baraa](https://github.com/DataWithBaraa/sql-data-warehouse-project). I implemented it by following his tutorial, using his dataset. The documentation in `docs/` (diagrams, data catalog, naming conventions) is adapted from the original project.

---

## 🏗️ Data Architecture

The architecture follows the Medallion Architecture with **Bronze**, **Silver**, and **Gold** layers:

![Data Architecture](docs/data_architecture.png)

1. **Bronze Layer**: Stores raw data as-is from the source systems. Data is ingested from CSV files into a SQL Server database.
2. **Silver Layer**: Includes data cleansing, standardization, and normalization processes to prepare data for analysis.
3. **Gold Layer**: Houses business-ready data modeled into a star schema required for reporting and analytics.

---

## 📖 Project Overview

This project involves:

1. **Data Architecture**: Designing a modern data warehouse using Medallion Architecture (Bronze, Silver, Gold).
2. **ETL Pipelines**: Extracting, transforming, and loading data from the source systems into the warehouse.
3. **Data Modeling**: Developing fact and dimension tables optimized for analytical queries.
4. **Data Quality Checks**: SQL test scripts that validate the Silver and Gold layers.

---

## 🛠️ Tools

- **[SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-downloads):** Lightweight server for hosting the database.
- **[SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms):** GUI for managing and querying the database.
- **[Git / GitHub](https://github.com/):** Version control.
- **[draw.io](https://www.drawio.com/):** Architecture, data flow, and data model diagrams.

---

## 🚀 Project Requirements

### Objective

Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

### Specifications

- **Data Sources**: Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality**: Cleanse and resolve data quality issues prior to analysis.
- **Integration**: Combine both sources into a single, user-friendly data model designed for analytical queries.
- **Scope**: Focus on the latest dataset only; historization of data is not required.
- **Documentation**: Provide clear documentation of the data model to support both business stakeholders and analytics teams.

---

## 📂 Repository Structure

```
sql-data-warehouse-project/
│
├── datasets/                # Raw source files (ERP and CRM data)
│
├── docs/                    # Project documentation and architecture details
│   ├── data_architecture    # Project architecture diagram
│   ├── data_flow            # Data flow diagram
│   ├── data_model           # Data model (star schema)
│   ├── data_catalog.md      # Catalog of Gold layer tables, with field descriptions
│   ├── naming_conventions.md# Naming guidelines for tables, columns, and files
│
├── scripts/                 # SQL scripts for ETL and transformations
│   ├── init_database.sql    # Creates the database and the bronze/silver/gold schemas
│   ├── bronze/              # Scripts for loading raw data
│   ├── silver/              # Scripts for cleaning and transforming data
│   ├── gold/                # Scripts for creating the analytical model
│
├── tests/                   # Data quality check scripts
│
├── README.md
└── LICENSE
```

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE). The original project by Data With Baraa is also MIT-licensed.
