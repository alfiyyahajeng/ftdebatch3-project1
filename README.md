# ETL Batch Processing - Mini Project 1
This project focuses on creating a simple ETL (Extract, Transform, Load) process for batch processing. It's implementing skills from previous session such as Git, Python, databases, and business intelligence (BI). 
The final output will be a dashboard displaying the following data:
* Order details
* Shipper information
* Payment details
* Voucher details

## 🔑 ETL Process
* **Extract**: Retrieve data from the production database (marketplace) for processing.
* **Transform**: Join multiple tables (orders, payments, shippers, vouchers, and ratings) and apply any necessary data transformations to align with the target schema.
* **Load**: Insert the transformed data into the data warehouse for analytical purposes.

## 🚀 Project Goals
* Create a data warehouse table using a predefined schema.
* Migrate data from the production database (marketplace) to the data warehouse for analysis.
* Enable analysts to use the data warehouse without overloading the production database.

## 🔨 Tech Used 
* Python
* psycopg2
* SQLAlchemy
* sqlparse
* pandas

## ✨ Step by step
1. Install Dependencies by run this script
  ```pip install req.txt```
2. Create conncection postgresql in Dbeaver. Insert schema and data in data warehouse
   * `query/query.sql`: extracting data from the source database
   * `query/dwh_design.sql `: define schema and table in Data Warehouse 
3. Create config.json file
   ```json{
    "marketplace_prod": {
        "host": "",
        "db": "",
        "user": "",
        "password": "",
        "port": ""
    },
    "dwh": {
        "host": "",
        "db": "",
        "user": "",
        "password": "",
        "port": ""
    }
  
4. Execute the ETL Script `main.py`
