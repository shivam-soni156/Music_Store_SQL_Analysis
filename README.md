# Music Store Data Analysis with SQL

## Project Overview
This project focuses on analyzing data from a music store to gain valuable business insights using only SQL. The objective is to assist the store in understanding its growth, identifying customer behavior, and making data-driven decisions.

---

## Objectives
- Analyze the music store's sales and customer data.
- Provide actionable insights based on SQL queries.
- Answer key business questions, such as identifying top customers, revenue-generating locations, and popular genres.

---

## Dataset Information
The database consists of 11 tables with relationships between them, representing various aspects of the music store, including customers, employees, invoices, and tracks.

### Key Tables:
- **Employee:** Information about store employees.
- **Customer:** Details of customers.
- **Invoice:** Records of customer purchases.
- **Track:** Information about individual music tracks.
- **Genre:** Music genres available.

---

## Data Import Process
To set up the database, follow these steps:

1. **Create Tables:** Create tables according to the provided CSV schema.
2. **Import Data:** Use the following command to import CSV data:

   ```sql
   COPY table_name(column1, column2, ...)
   FROM 'file_path_with_name.csv'
   DELIMITER ',' CSV HEADER;
   ```

---

## Key Insights and SQL Queries
### **Set 1: Basic Insights**
1. **Senior-most employee based on job title:**
   Query: Use the `employee` table and `ORDER BY` the `job_title` column.
2. **Countries with the most invoices:**
   Query: Use `GROUP BY` on the `invoice` table to count occurrences and sort by the `country` column or another relevant field.
3. **Top 3 invoice values:**
   Query: Use `ORDER BY` the `total_amount` column and `LIMIT 3` on the `invoice` table.
4. **City with the highest revenue:**
   Query: Sum `invoice` totals and `GROUP BY` city.
5. **Best customer:**
   Query: Join `customer` and `invoice` tables and aggregate spending.

### **Set 2: Moderate Insights**
6. **Rock music listeners (ordered by email):**
   Query: Join `customer` and `genre` tables.
7. **Top 10 rock music artists:**
   Query: Join `artist` and `track` tables and count tracks.
8. **Tracks longer than the average song length:**
   Query: Calculate average song length and filter results.

### **Set 3: Advanced Insights**
9. **Customer spending on artists:**
   Query: Use CTEs to aggregate spending data across tables.
10. **Most popular genre by country:**
    Query: Use `ROW_NUMBER()` and CTEs to rank genres.
11. **Top customer by spending for each country:**
    Query: Use recursive methods or CTEs with `ROW_NUMBER()`. Recursive methods are beneficial when dealing with hierarchical or sequential data, while CTEs help simplify complex queries by breaking them into manageable parts.

---

## SQL Techniques Used
- **JOIN Operations:** To connect related tables.
- **Aggregate Functions:** For sums, averages, and counts.
- **Common Table Expressions (CTEs):** For temporary result sets.
- **Window Functions:** Efficient ranking using `ROW_NUMBER()`.
- **Recursive Queries:** Optimized data retrieval.

---

## How to Reproduce
1. **Set Up Database:** Follow the data import instructions.
2. **Run Queries:** Execute the queries in `SQL_QUERIES/music_store_analysis.sql`.

---

## Contributions
Contributions are welcome! If you have suggestions or additional insights, feel free to create a pull request.

---

## Contact
For any questions or suggestions, please reach out via GitHub.

