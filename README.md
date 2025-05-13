# Fabric_DP700_lab03
# 🧪 Delta Lake Lab with Microsoft Fabric

This project is part of a hands-on lab designed to explore working with Delta Tables using Microsoft Fabric, SQL, and PySpark. The lab focuses on creating, managing, and querying Delta Lake tables in both batch and streaming scenarios.

---

## 🔍 Objective of the Lab

The main goals of this lab are:

- To create a **Lakehouse** environment within Microsoft Fabric.
- To work with **Delta Lake** formatted tables.
- To analyze data using both **SQL** and **PySpark**, leveraging Delta Tables that support **batch and streaming data**.

---

## 🔧 Steps Followed

1. **Workspace & Lakehouse Creation**
   - Signed into Microsoft Fabric.
   - Created a new **Workspace**.
   - Created a **Lakehouse** within the workspace for storing data.

2. **Data Upload**
   - Downloaded the `products.csv` file from GitHub.
   - Uploaded the file into a `products` folder inside the Lakehouse.

3. **Read Data with Spark DataFrame**
   - Used **PySpark** to read `products.csv` into a DataFrame with a defined schema.
   - Displayed the data to confirm successful loading.

4. **Create Delta Tables**
   - **Managed Table**: Created a table named `managed_products` (data & metadata are managed by Lakehouse).
   - **External Table**: Created a table named `external_products` (data stored in Files folder; metadata managed by Lakehouse).

5. **Compare Delta Tables**
   - Used `DESCRIBE FORMATTED` in SQL to inspect table properties.
   - Compared file paths to understand storage differences between managed and external tables.

6. **Drop Tables & Observe Data Persistence**
   - Dropped both tables using `DROP TABLE`.
   - Verified that deleting an external table does **not** remove underlying data files, only metadata.

7. **Create Delta Table with SQL**
   - Created a new Delta table named `products` using a SQL statement.
   - Queried the table using both SQL and PySpark.

8. **Time Travel (Versioning)**
   - Applied `UPDATE` to reduce the price of Mountain Bikes by 10%.
   - Used `DESCRIBE HISTORY` to view the change history.
   - Used `.option("versionAsOf", 0)` to load the original version of the data.

9. **SQL Analytics**
   - Created a temporary view called `products_view`.
   - Used SQL to calculate:
     - Product count per category
     - Minimum/maximum/average prices
     - Top 10 categories by product count
   - Visualized the results.
   - Used PySpark to sort data from the SQL view.

---

## 🎓 What I Learned from This Lab

| Topic                      | Summary                                                                 |
|---------------------------|-------------------------------------------------------------------------|
| Microsoft Fabric           | Learned how to create a workspace and lakehouse.                       |
| Delta Lake                 | Used an open-source format with versioning and SQL support.            |
| Managed vs External Tables | Compared storage and metadata handling strategies.                     |
| Time Travel                | Experienced how to access historical versions of Delta tables.         |
| PySpark & SQL Integration  | Performed data analysis by combining PySpark and SQL queries.          |
| Notebook Usage             | Structured the analysis using markdown and code cells in a notebook.   |
| SQL Analytics              | Executed groupings and aggregations for data insights and charts.      |
| Delta Table Management     | Practiced creating, updating, and deleting Delta tables with SQL and PySpark. |

---


## 🛠️ Technologies Used

- Microsoft Fabric
- Delta Lake
- PySpark
- SQL
- Apache Spark Notebooks

---
## Screenshots
<img width="1490" alt="1" src="https://github.com/user-attachments/assets/d36b7f8e-a9c6-440a-b1e8-1bb814943055" />

<img width="1487" alt="2" src="https://github.com/user-attachments/assets/0670c35a-62d5-4a66-8638-c2e9188b28cf" />

<img width="1266" alt="3" src="https://github.com/user-attachments/assets/e6dd81cd-3072-4705-b9bd-c2de88296ffa" />

<img width="1429" alt="4" src="https://github.com/user-attachments/assets/5a839ba1-231f-4880-8497-631987859bf5" />

<img width="1347" alt="5" src="https://github.com/user-attachments/assets/85b9ffb5-d6b6-40a8-9029-eb8c253a3513" />

<img width="1448" alt="8" src="https://github.com/user-attachments/assets/494d04c4-12f5-4ca5-aead-bbcf0c42586f" />

<img width="1429" alt="9" src="https://github.com/user-attachments/assets/2d1a229d-6744-4066-aef1-6bd4c5f80fcb" />
