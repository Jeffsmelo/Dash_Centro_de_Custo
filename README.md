# Dash - Cost Center Purchase Orders

A data visualization platform built in Python (Dash + SQLAlchemy) that consolidates multiple ERP modules into a single interface, replacing fragmented manual reporting with a centralized, real-time view of purchase orders by cost center.

## Features

- Query open purchase orders, filtered by cost center
- Real-time search by PO number, supplier, requester, and other fields
- Export filtered data to CSV
- Detailed view of each order (product, quantities, values, status)
- Login system with per-cost-center access control, plus consolidated admin access (Master and Purchasing profiles)

## Tech stack

- **Python**
- **Dash** (analytics web application framework)
- **SQLAlchemy** (ORM / database connection)
- **Pandas** (data processing and transformation)
- **SQL Server** (data source, via ODBC Driver 18)

## Setup

This project **contains no hardcoded credentials**. All sensitive configuration is loaded from environment variables.

1. Copy `env.example` to `.env` and fill in the real values (database connection, login credentials, per-cost-center passwords).
2. Install dependencies:
   ```
   pip install dash pandas sqlalchemy pyodbc python-dotenv
   ```
3. Run the application:
   ```
   python src.py
   ```

⚠️ The `.env` file should never be committed — it's already listed in `.gitignore`.

## Background

This project was built to solve a real operational problem: consolidating purchase order reports that were scattered across multiple TOTVS ERP modules into a single interface, accessible by cost center, without relying on recurring manual exports.
