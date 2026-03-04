🚀 Databricks Auto Loader Streaming Pipeline
Medallion Architecture (Bronze → Silver → Gold)
📌 Project Overview

This project demonstrates an end-to-end modern data engineering pipeline built using Databricks, PySpark, Delta Lake, and Auto Loader following the Medallion Architecture.

The pipeline ingests traffic and road datasets, processes them through multiple transformation layers, and produces analytics-ready datasets that are visualized in Power BI dashboards.

🏗️ Architecture
                Raw CSV Data
                     │
                     ▼
             ⚡ Auto Loader Ingestion
                     │
                     ▼
                🥉 Bronze Layer
          (Raw Delta Tables Storage)
                     │
                     ▼
                🥈 Silver Layer
      (Data Cleaning & Transformations)
                     │
                     ▼
                🥇 Gold Layer
       (Curated Analytics Data Model)
                     │
                     ▼
                📊 Power BI
             (Dashboard & Insights)
🔄 Pipeline Flow
1️⃣ Data Ingestion (Bronze Layer)

Raw CSV datasets are ingested using Databricks Auto Loader

Streaming ingestion using Structured Streaming

Raw data stored in Delta Tables

Metadata column Extract_Time added

2️⃣ Data Transformation (Silver Layer)

Data cleaning and enrichment steps include:

🧹 Removing duplicate records

🔧 Handling NULL values

🚗 Calculating Electric Vehicle Count

🚙 Calculating Motor Vehicle Count

⏱️ Adding Transformation Timestamp

3️⃣ Curated Data (Gold Layer)

Final business-ready datasets include:

📊 Vehicle Intensity Calculation

🕒 Load timestamp tracking

Optimized tables for analytics

These datasets power the Power BI dashboard.

⚙️ Technologies Used
Technology	Purpose
Databricks	Data engineering platform
PySpark	Data transformation
Auto Loader	Streaming ingestion
Delta Lake	Storage and transaction management
Structured Streaming	Incremental processing
Azure Data Lake	Cloud storage
Power BI	Data visualization
📂 Project Structure
databricks-autoloader-project
│
├── Project_Setup.py
│   └── Creates schemas and raw tables
│
├── Load_to_Bronze.py
│   └── Auto Loader ingestion from landing zone
│
├── Silver_Traffic_Transformations.py
│   └── Data cleaning & derived metrics
│
├── Silver_Roads_Transformations.py
│   └── Road classification transformations
│
├── Gold_Final_Transformations.py
│   └── Final analytics dataset creation
│
└── Common.py
    └── Reusable functions and shared variables
✨ Key Features

✅ End-to-end streaming data pipeline
✅ Medallion Architecture implementation
✅ Modular reusable transformation functions
✅ Data quality handling (duplicates & NULLs)
✅ Delta Lake tables with checkpointing
✅ Analytics-ready Gold datasets
✅ Power BI dashboard integration

📊 Example Derived Metrics
Electric Vehicle Count
EV_Car + EV_Bike
Motor Vehicle Count
Electric_Vehicles_Count
+ Two_wheeled_motor_vehicles
+ Cars_and_taxis
+ Buses_and_coaches
+ LGV_Type
+ HGV_Type
Vehicle Intensity
Motor_Vehicles_Count / Link_length_km
📊 Dashboard (Power BI)

The Gold Layer tables are connected to Power BI to visualize:

🚦 Traffic distribution by region

🔋 Electric vehicle trends

📍 Vehicle intensity analysis

🛣️ Road category insights

🎯 Skills Demonstrated

Data Pipeline Design

Databricks Auto Loader

Structured Streaming

PySpark Transformations

Delta Lake Architecture

Medallion Data Architecture

BI Integration with Power BI

⭐ Future Improvements

Implement CI/CD with Databricks Workflows

Add Delta Live Tables

Implement data quality checks with expectations

Add pipeline monitoring
