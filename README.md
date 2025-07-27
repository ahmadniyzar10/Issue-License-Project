# 🏙️ NYC Business Licenses ELT Pipeline

This project demonstrates an end-to-end ELT (Extract, Load, Transform) data pipeline using NYC's open dataset on issued business licenses. The goal is to build a production-grade data engineering pipeline using cloud-native tools, perform transformations using dbt, and prepare data for analytics and reporting.

---

## 📂 Project Structure

```
nyc_licenses_pipeline/
├── data/                        # Raw and processed data
│   ├── raw/
│   │   └── issued_licenses.csv
│   └── schema/
│       └── raw_schema.sql       # DDL or table structure
├── docs/                        # Project documentation
│   └── dataset_overview.md
├── dbt/                         # dbt project for transformations
├── dags/                        # (Optional) Airflow DAGs
├── notebooks/                  # Jupyter notebooks for exploration
├── requirements.txt            # Python dependencies
├── README.md                   # This file
└── .env                        # Environment config for local dev
```



---

## 🧪 Dataset Overview

Source: [NYC Open Data - Issued Licenses](https://data.cityofnewyork.us/Business/Issued-Licenses/w7w3-xahh)

The dataset contains structured records of all business licenses issued by NYC’s Department of Consumer and Worker Protection (DCWP). It includes metadata on:

- 🏷️ Business and license identifiers  
- 📍 Location (borough, ZIP, latitude/longitude)  
- 📅 Issuance and expiration dates  
- 📞 Contact and address information  
- 🗃️ License category, type, and status  

### Example Schema Summary

| Column Name         | Description                                       | Data Type   |
|---------------------|---------------------------------------------------|-------------|
| license_number      | Unique license number                             | String      |
| business_name       | Legal registered business name                    | String      |
| dba_trade_name      | Trade name (Doing Business As)                    | String      |
| license_status      | Status of license (Active, Expired, etc.)         | Categorical |
| license_creation_date | Date license was originally issued             | Date        |
| license_expired_date  | License expiration date                           | Date        |
| address_city        | City where business is located                    | String      |
| address_borough     | NYC borough                                       | String      |
| latitude, longitude | Geo-coordinates                                   | Float       |

---

## 🧰 Tools & Technologies

| Layer        | Tool                     | Purpose                                |
|--------------|--------------------------|----------------------------------------|
| **Storage**  | AWS S3                   | Stores raw CSV data                    |
| **Warehouse**| Snowflake                | Central data warehouse                 |
| **Transform**| dbt                      | SQL-based transformations              |
| **Orchestration** | (Optional) Airflow | DAG management (future step)          |
| **Exploration** | Jupyter, Snowflake UI | Data analysis and validation           |

---

## Data Model

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.
