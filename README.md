# Data-Migration-Between-Databases-Simulated-


COMPANY NAME: CODTECH IT SOLUTIONS

NAME: SANEMI VALECHA

INTERN ID: CT04DZ135

DOMAIN NAME: SQL INTERNSHIP

DURATION: 4 WEEKS

MENTOR NAME: NEELA SANTOSH


In real-world software systems, data is often required to be transferred or migrated from one database to another. This process is called Database Migration. Migration is necessary during technology upgrades (e.g., moving from MySQL to PostgreSQL), shifting infrastructure (like moving to the cloud), consolidating databases, or integrating third-party systems.

Task 3 in the internship required me to understand and simulate how data migration is carried out between two different databases. While actual migration between MySQL and PostgreSQL or other platforms typically involves tools and configurations, this task focused on demonstrating the concept using Microsoft SQL Server. The idea was to show how we can export data from one table and prepare it for import into another environment.

🔄 Simulated Environment Setup
For this simulation, I created a table called Employees in SQL Server. This table included some sample employee records with fields like EmployeeID, Name, and DepartmentID. The idea was to simulate exporting this data for use in another database by creating a copy of the table and its data — mimicking a typical migration workflow.

I then used the SQL Server SELECT INTO command to copy the entire contents of the Employees table into a new table called Exported_Employees. This step represents the export stage in a real migration, where data is usually extracted from the source system and stored in a transitional table or file (e.g., CSV, SQL dump, etc.).

Command used:

sql
Copy
Edit
SELECT * INTO Exported_Employees FROM Employees;
This command:

Creates a new table called Exported_Employees

Copies all rows and columns from the Employees table

Preserves the structure and data types of the original table

After running this command, SQL Server returned the message:

scss
Copy
Edit
(4 row(s) affected)
This indicated that the migration simulation had succeeded, copying all four employee records into the new table.

📤 Import in a Real-World Scenario
In a real-world migration between databases (e.g., MySQL → PostgreSQL), this intermediate data would be:

Exported to a .CSV file or SQL script

Transferred to the new database server

Imported into the new system using platform-specific commands

For example, in PostgreSQL, the following command could be used:

sql
Copy
Edit
COPY Employees FROM '/path/to/employees.csv' DELIMITER ',' CSV;
Similarly, in MySQL, you could use LOAD DATA INFILE to import a CSV.

💡 What I Learned
This task helped me understand how migration is more than just copying data. It involves:

Preserving data types and relationships

Validating data consistency

Handling NULLs, constraints, and foreign keys

Writing platform-compatible queries

Although I performed the task within a single SQL Server environment, the logical process of:

Extracting data

Copying it into a clean structure

Preparing it for re-use

...perfectly represents what real migrations entail.

✅ Conclusion
Task 3 gave me a clear understanding of how data can be moved between different environments. Even though I didn’t actually use MySQL or PostgreSQL, the simulation using SELECT INTO demonstrated the key migration steps. This knowledge is applicable to real-life roles in data engineering, system integration, and database administration, where clean and consistent migration of data is often critical to success.

OUTPUTS
