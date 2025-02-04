📥 Data Import Instructions
This document outlines the steps to import the music store dataset into a SQL database for analysis.

1️⃣ Database Setup
Before importing data, ensure you have a PostgreSQL (or any other preferred SQL database) installed and running.

2️⃣ Creating Tables
To structure the database, create tables matching the dataset schema. Use the following SQL commands to define tables before importing data:

CREATE TABLE table_name (
    column1 DATATYPE,
    column2 DATATYPE,
    ...
);
Refer to the dataset schema to match columns correctly.

3️⃣ Importing Data from CSV
Once tables are created, use the COPY command to import data:

COPY table_name(column1, column2, ...)
FROM 'file_path_with_name.csv'
DELIMITER ',' CSV HEADER;

Example:
COPY employees(id, name, position, salary)
FROM '/path/to/employees.csv'
DELIMITER ',' CSV HEADER;

4️⃣ Verifying Imported Data
After importing, run queries to check the data:

SELECT * FROM table_name LIMIT 10;
Ensure data is correctly formatted and no records are missing.

5️⃣ Handling Import Errors

If errors occur:
Check the CSV format (delimiter, missing values, etc.).
Ensure correct data types in table definitions.
Verify file path and permissions.

6️⃣ Next Steps
Once data is imported, proceed with SQL queries to analyze insights such as customer behavior, revenue trends, and genre popularity.

