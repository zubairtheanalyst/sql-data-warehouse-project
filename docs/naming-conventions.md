# 📝 Naming Conventions

This document outlines the **naming conventions** used for schemas, tables, views, columns, and other objects in the data warehouse.

---

## Table of Contents

1. [General Principles](#general-principles)  
2. [Table Naming Conventions](#table-naming-conventions)  
   - [🟫 Bronze Rules](#🟫-bronze-rules)  
   - [⬜ Silver Rules](#⬜-silver-rules)  
   - [🟨 Gold Rules](#🟨-gold-rules)  
3. [Column Naming Conventions](#column-naming-conventions)  
   - [Surrogate Keys](#surrogate-keys)  
   - [Technical Columns](#technical-columns)  
4. [Stored Procedures](#stored-procedures)

---

## General Principles

- **Naming Conventions:** Use `snake_case` with lowercase letters and underscores (`_`) to separate words.  
- **Language:** Use English for all names.  
- **Avoid Reserved Words:** Do not use SQL reserved words as object names.  

---

## Table Naming Conventions

### 🟫 Bronze Rules

- All table names must start with the **source system name** and match the original table name.  
- **Format:** `<sourcesystem>_<entity>`  
  - `<sourcesystem>`: Name of the source system (e.g., `crm`, `erp`)  
  - `<entity>`: Exact table name from the source system  

**Example:**  
`crm_customer_info` → Customer information from the CRM system.

### ⬜ Silver Rules

- Same rules as Bronze: `<sourcesystem>_<entity>`  
- Tables reflect **cleaned and standardized data** from source systems.  

**Example:**  
`crm_customer_info` → Standardized customer information from CRM.

### 🟨 Gold Rules

- Use **meaningful, business-aligned names** starting with a **category prefix**.  
- **Format:** `<category>_<entity>`  
  - `<category>`: Role of the table (e.g., `dim` for dimension, `fact` for fact table)  
  - `<entity>`: Descriptive, business-aligned table name  

**Examples:**  
- `dim_customers` → Dimension table for customer data  
- `fact_sales` → Fact table containing sales transactions  

**Glossary of Category Patterns**

| Pattern   | Meaning         | Example(s)                   |
|-----------|----------------|------------------------------|
| dim_      | Dimension table | dim_customer, dim_product    |
| fact_     | Fact table      | fact_sales                   |
| report_   | Report table    | report_customers, report_sales_monthly |

---

## Column Naming Conventions

### Surrogate Keys

- All primary keys in **dimension tables** must use the suffix `_key`.  
- **Format:** `<table_name>_key`  
- **Example:** `customer_key` → Surrogate key in the `dim_customers` table

### Technical Columns

- All technical columns must start with the prefix `dwh_` followed by a descriptive name.  
- **Format:** `dwh_<column_name>`  
- **Example:** `dwh_load_date` → Stores the date when the record was loaded

---

## Stored Procedures

- All stored procedures used for loading data must follow the naming pattern: `load_<layer>`  
- `<layer>`: Represents the layer being loaded (`bronze`, `silver`, `gold`)  

**Examples:**  
- `load_bronze` → Loads data into Bronze layer  
- `load_silver` → Loads data into Silver layer  
- `load_gold` → Loads data into Gold layer
