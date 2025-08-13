# Daily-Revenue-Dashboard
Daily Revenue Dashboard simulates a hypermarket’s real-time sales using a star schema in PostgreSQL and Python-generated dummy data. Build operational Tableau dashboards to track daily revenue, sales trends, top products, and payment methods. Ideal for practicing BI, data modeling, and dashboard automation.

---

# Git Setup
git clone git@github.com:Ponmani-Manoharan/Daily-Revenue-Dashboard.git
cd Daily-Revenue-Dashboard
git add .
git commit -m "Initial commit"
git push origin main


---


# Daily Revenue Dashboard - Operational Star Schema Project

This repository contains a complete setup for an **operational dashboard** simulating a hypermarket’s daily revenue transactions. The project includes a **star schema in PostgreSQL**, Python scripts to generate dummy transactional data, and Tableau dashboard integration.

---

## 🏆 Project Objective

- Provide **real-time insights** into daily revenue, sales by hour, top-selling products, and payment methods.
- Simulate a **hypermarket environment** with perishable and non-perishable products across multiple branches in the US.
- Enable **hourly refresh** of transaction data to mimic real operational behavior.

---

## 📂 Repository Structure

daily_revenue_dashboard/
│
├── README.md                # Project overview, instructions, objectives
├── requirements.txt         # Python dependencies (psycopg2, pandas, SQLAlchemy, etc.)
├── sql/
│   ├── create_tables.sql    # PostgreSQL table creation scripts (star schema)
│   └── 
├── python/
│   ├── generate_dim_data.py # Script to create and populate dimension tables
│   ├── generate_fact_data.py # Script to generate and insert fact transactions
│   └── scheduler.py         # Optional: code to schedule hourly inserts
├── tableau/
│   └── dashboard_files.twb  # Placeholder for Tableau dashboard files
├── drawio/
│   └── star_schema.drawio   # Star schema diagram
└── data/
    └── sample_data.csv      # Optional: CSV export of dummy data


---

## ⭐ Features

- **Dimension Tables**:
  - `dim_branch` – 10 branches based on major US cities
  - `dim_product` – ~20,000 products (perishable and non-perishable)
  - `dim_payment` – Payment methods (Cash, Credit Card, Mobile Pay)
  - `dim_date` – Hourly date-time entries

- **Fact Table**:
  - `fact_sales` – Transaction data including branch, product, payment method, quantity, price, total

- **Python Scripts**:
  - Generate random transactions (1–200 units per transaction)
  - Insert data into PostgreSQL
  - Schedule hourly data refresh to simulate real-time operations

- **Tableau Dashboard**:
  - Daily revenue tracking
  - Sales by hour
  - Top-selling products
  - Payment method analysis
  - Branch-wise revenue map
  - Perishable product alerts

