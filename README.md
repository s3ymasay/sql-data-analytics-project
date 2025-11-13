# SQL Data Analytics Project

A comprehensive collection of SQL scripts for exploratory data analysis, business intelligence, and reporting. This project demonstrates various analytical techniques including database exploration, KPI calculation, trend analysis, cumulative metrics, customer segmentation, and performance reporting.

Built with Microsoft SQL Server and T-SQL, focusing on data analysis best practices and business insights.

---

## Project Overview

This repository contains SQL queries designed for data analysis and business intelligence on a data warehouse. Each script focuses on a specific analytical theme, showcasing practical approaches to real-world business questions.

The analysis is performed on a **Gold Layer** dataset containing customer, product, and sales data from a fictional retail business.

---

## Key Features

- **Database Exploration**: Understanding data structure, schemas, and relationships
- **Dimension Analysis**: Exploring unique values and categories across dimensions
- **Date Range Exploration**: Identifying temporal boundaries of the dataset
- **Measures & Metrics**: Calculating key business indicators (KPIs)
- **Magnitude Analysis**: Quantifying data distribution across categories
- **Ranking Analysis**: Identifying top and bottom performers
- **Change Over Time**: Tracking trends and temporal patterns
- **Cumulative Analysis**: Running totals and moving averages
- **Performance Analysis**: Year-over-year and comparative metrics
- **Data Segmentation**: Customer and product categorization
- **Part-to-Whole Analysis**: Understanding proportions and contributions
- **Business Reports**: SQL views for customer and product insights

---

## Project Structure

```
sql-data-analytics-project/
├── README.md
├── .gitignore
│
├── datasets/                           # Gold layer data (CSV format)
│   ├── gold.dim_customers.csv         # Customer dimension
│   ├── gold.dim_products.csv          # Product dimension
│   └── gold.fact_sales.csv            # Sales fact table
│
└── scripts/                            # SQL analysis scripts
    ├── 00_init_database.sql           # Database setup and data loading
    ├── 01_database_exploration.sql    # Database structure exploration
    ├── 02_dimensions_exploration.sql  # Dimension values analysis
    ├── 03_date_range_exploration.sql  # Temporal boundaries
    ├── 04_measures_exploration.sql    # Key metrics and KPIs
    ├── 05_magnitude_analysis.sql      # Data distribution by category
    ├── 06_ranking_analysis.sql        # Top/bottom performers
    ├── 07_change_over_time_analysis.sql   # Trend analysis
    ├── 08_cumulative_analysis.sql     # Running totals
    ├── 09_performance_analysis.sql    # YoY comparisons
    ├── 10_data_segmentation.sql       # Customer/product segments
    ├── 11_part_to_whole_analysis.sql  # Contribution analysis
    ├── 12_report_customers.sql        # Customer insights view
    └── 13_report_products.sql         # Product insights view
```

---

## Technologies Used

- **Database**: Microsoft SQL Server
- **Language**: T-SQL
- **Techniques**: Window functions, CTEs, aggregations, date functions
- **Tools**: SQL Server Management Studio (SSMS)

---

## Getting Started

### Prerequisites

- Microsoft SQL Server (2016 or later)
- SQL Server Management Studio (SSMS)

### Setup

**Step 1: Configure Data Path**

Update the file path in `scripts/00_init_database.sql`:

- Default path: `C:\sql\sql-data-analytics-project\datasets\csv-files\`
- Use Find & Replace to update to your path
- Or copy datasets to the default location

**Step 2: Initialize Database**

Run the initialization script to create the database and load data:

```sql
scripts/00_init_database.sql
```

This will:
- Create the `DataWarehouseAnalytics` database
- Create the `gold` schema
- Create dimension and fact tables
- Load data from CSV files

**Step 3: Run Analysis Scripts**

Execute scripts in any order based on your analytical needs:

```sql
-- Explore the database structure
scripts/01_database_exploration.sql

-- Calculate key metrics
scripts/04_measures_exploration.sql

-- Analyze trends over time
scripts/07_change_over_time_analysis.sql

-- Create business reports
scripts/12_report_customers.sql
scripts/13_report_products.sql
```

---

## Analysis Categories

### **Exploration (Scripts 01-03)**
Understanding the data landscape, structure, and temporal boundaries.

### **Metrics & Magnitude (Scripts 04-05)**
Calculating KPIs and quantifying data distribution across dimensions.

### **Ranking & Comparison (Script 06)**
Identifying top performers, worst performers, and relative standings.

### **Temporal Analysis (Scripts 07-08)**
Tracking trends, changes over time, and cumulative metrics.

### **Advanced Analytics (Scripts 09-11)**
Year-over-year performance, customer segmentation, and contribution analysis.

### **Business Reports (Scripts 12-13)**
Pre-built SQL views for customer and product insights with calculated KPIs:
- Customer segments (VIP, Regular, New)
- Age groups and demographics
- Recency, frequency, monetary metrics
- Product performance tiers
- Average order values and monthly trends

---

## Sample Insights

The scripts enable answers to business questions such as:

- **Sales Performance**: What is the total revenue, average order value, and sales trend?
- **Customer Behavior**: Who are our top customers? What segments do they fall into?
- **Product Performance**: Which products generate the most revenue? Which are underperforming?
- **Geographic Analysis**: Which countries contribute most to sales?
- **Temporal Trends**: How do sales vary by month, quarter, or year?
- **Growth Metrics**: What is our year-over-year growth rate?

---

## Acknowledgments

Developed during the SQL Data Analytics course by Baraa Khatib Salkini. The analytical framework was provided by the course, with all SQL implementations and query optimization independently developed.
