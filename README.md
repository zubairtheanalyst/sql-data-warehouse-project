SQL Data Warehouse and Analytics Project 🚀

This repository contains my implementation of a complete SQL-based Data Warehouse and Analytics solution, following modern best practices in Data Engineering and Analytics.

The project takes raw ERP & CRM business data, builds a data warehouse using Medallion Architecture (Bronze, Silver, Gold layers), and delivers actionable insights through SQL-based reporting and analysis.

💡 Why I Did This Project

I built this project as part of my portfolio to demonstrate end-to-end skills in Data Engineering, Data Modeling, and Analytics.

Working through the full data lifecycle – from raw CSV ingestion to business-ready analytics – helped me strengthen my understanding of:

Structuring a modern Data Warehouse

Designing ETL pipelines for data transformation

Creating star schema models for analytics

Writing SQL-based insights that answer key business questions

This project was both a practical challenge and an opportunity to showcase the way I approach real-world data problems.

🏗️ Data Architecture

The solution is structured using the Medallion Architecture pattern:

Bronze Layer: Stores raw data (CSV source files) ingested into SQL Server.

Silver Layer: Cleansed, standardized, and normalized data ready for integration.

Gold Layer: Business-ready data modeled into a Star Schema for analytics and reporting.

📖 Project Overview

Data Architecture: Designing a modern Data Warehouse using Bronze, Silver, and Gold layers.

ETL Pipelines: Extracting, transforming, and loading data into SQL Server.

Data Modeling: Building fact and dimension tables optimized for analytical queries.

Analytics & Reporting: Writing SQL queries and reports to generate actionable insights.

🎯 Skills Demonstrated

SQL Development

ETL Pipelines & Data Engineering

Data Modeling (Star Schema)

Analytics & Reporting

Data Architecture Design

🛠️ Tools & Technologies

SQL Server Express – Database engine

SQL Server Management Studio (SSMS) – Development environment

DrawIO – Architecture, data flow, and schema diagrams

Notion – Project planning and documentation

Git/GitHub – Version control

🚀 Project Requirements
Data Warehouse (Data Engineering)

Import raw ERP & CRM datasets (CSV files)

Cleanse and standardize data

Integrate into a single model

Build fact/dimension tables in star schema

Document design for future analytics teams

Analytics (Data Analysis)

Customer Behavior analysis

Product Performance insights

Sales Trend reporting

📂 Repository Structure
data-warehouse-project/
│
├── datasets/                # Raw datasets (ERP and CRM)
│
├── docs/                    # Documentation & diagrams
│   ├── etl.drawio
│   ├── data_architecture.drawio
│   ├── data_catalog.md
│   ├── data_flow.drawio
│   ├── data_models.drawio
│   ├── naming-conventions.md
│
├── scripts/                 # SQL ETL scripts
│   ├── bronze/              # Raw data ingestion
│   ├── silver/              # Data cleaning & transformations
│   ├── gold/                # Star schema & analytical models
│
├── tests/                   # Test scripts & validation
│
├── README.md                # Project overview (this file)
├── LICENSE                  # License info
├── .gitignore               # Git ignore rules
└── requirements.txt         # Dependencies

📊 Example Insights

Some of the business questions answered through this warehouse include:

Which customers contribute the most revenue?

What are the top-performing products?

How are sales trending over time?

🙌 Credits

This project was fully implemented by me (Muhammad Zubair) as part of my portfolio work.

Special credit goes to Baraa Khatib Salkini, also known as Data With Baraa, who designed the original project concept and made it freely available. His work is an inspiring example of high-quality content that helps learners build real-world skills.
