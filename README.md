# Data Mining Database Validator - Project README

## Overview
This project is designed to validate, analyze, and visualize storm event data using both a MySQL database and CSV files. The workspace contains Jupyter notebooks and a large storm events dataset, supporting both data engineering and data science workflows.

## Files in This Repository

### 1. `StormEvents_details-ftp_v1.0_d2011_c20250520.csv`
- **Description:**
  - The main dataset containing detailed records of storm events for the year 2011.
  - Used as the source for both database uploads and direct CSV analysis.

### 2. `cap4770_mysql.ipynb`
- **Purpose:**
  - Demonstrates how to connect to a MySQL database from a Jupyter notebook.
  - Shows how to install required packages (e.g., `mysql-connector-python`, `seaborn`, `plotly`).
  - Contains code to:
    - Connect to the MySQL database and list available tables.
    - Query storm event data from the database.
    - Calculate and visualize damage costs, event frequencies, monthly trends, and geographic distributions.
    - Create a variety of data visualizations (bar charts, pie charts, scatter plots, etc.) using `matplotlib`, `seaborn`, and `plotly`.
  - Includes fallback logic to work with the CSV file if the database connection fails.

### 3. `cap47770_db_validator.ipynb`
- **Purpose:**
  - Focuses on validating the integrity and completeness of the data between the CSV file and the MySQL database.
  - Contains code to:
    - Connect to the MySQL database and display available tables.
    - Count and compare the number of records in the CSV file and the database table.
    - Upload all records from the CSV file to the database using both SQLAlchemy and direct MySQL connector methods.
    - Verify that the upload was successful by comparing record counts and displaying basic database statistics (e.g., unique event types, date range).
  - Provides troubleshooting and alternative upload methods if the primary upload fails.

## Getting Started
1. **Install Required Packages:**
   - Use the provided notebook cells to install Python packages such as `mysql-connector-python`, `sqlalchemy`, `seaborn`, and `plotly`.
2. **Database Setup:**
   - Ensure you have a MySQL server running and a database named `cap4770` with appropriate user credentials.
   - The notebooks assume the table name is `StormEvents_details` (case-sensitive).
3. **Run the Notebooks:**
   - Start with `cap47770_db_validator.ipynb` to validate and upload the data.
   - Use `cap4770_mysql.ipynb` for advanced analysis and visualizations.

## Notes
- The notebooks are designed to be robust: if the database is unavailable, analysis can proceed using the CSV file.
- All code is written in Python and intended for use in Jupyter Notebook environments.
- The project is suitable for data mining, data validation, and exploratory data analysis coursework or research.

## Author
- UWF CAP4770 Final Project

---
