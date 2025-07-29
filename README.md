# Database Course Overview for Beginners

This document provides a beginner-friendly overview of a database course, covering key concepts from relational and NoSQL databases to cloud-based solutions like Amazon Web Services (AWS). Each section introduces fundamental database concepts, SQL and NoSQL operations, and modern database architectures, making it easy for newcomers to understand.

---

## Week 1: Introduction to Databases

### Course Overview
This course introduces you to databases, which are like organized digital filing cabinets for storing and managing data. You'll learn about two main types: **relational databases** (like organized spreadsheets with tables) and **NoSQL databases** (more flexible for handling diverse data). You'll explore how to design databases, create tables, and use **SQL** (Structured Query Language) and **NoSQL** to interact with data. The course includes hands-on labs, assignments, tests, and a final project (case study) to apply what you've learned.

### Software Requirements
- **Operating System**: Windows is recommended for local development, but you can use other systems like macOS or Linux.
- **Tools**:
  - **PgAdmin**: Used for SQL and relational databases (like PostgreSQL).
  - **MongoDB**: Used for NoSQL databases.
- **Helpful Resources**:
  - [W3Schools](https://www.w3schools.com/): Beginner-friendly tutorials for SQL and more.
  - [AWS Workshops](https://workshops.aws/): Practical guides for cloud database tools.

### What is SQL?
**SQL** (Structured Query Language) is a language used to manage and manipulate data in **relational databases**, which store data in tables with rows and columns. Think of it like a librarian who helps you find, add, update, or delete books in a library catalog. SQL lets you:
- Store new data.
- Update or remove existing data.
- Search and retrieve specific information.
- Optimize database performance.

For example, a relational database might store student information with columns like `Name`, `ID`, and `Grade`, where each row represents one student.

- **Learn More**: [AWS: What is SQL?](https://aws.amazon.com/what-is/sql/)

### SQL Background
- **Purpose**: SQL is used to manage **relational databases**, where data is organized in tables with defined relationships.
- **History**: Developed by IBM in the 1970s and standardized by the American National Standards Institute (ANSI).
- **Uses**: Widely used in data analysis, software development, data science, and data engineering.

### Database Management Systems (DBMS)
A **DBMS** is software that acts like a bridge between users (or applications) and the database. It lets you run queries to interact with data. There are two main types:
1. **Relational DBMS (RDBMS)**:
   - Stores data in structured tables with rows and columns.
   - Uses SQL for queries.
   - Examples: MySQL, PostgreSQL, Oracle, Microsoft SQL Server.
2. **NoSQL DBMS**:
   - Handles flexible, non-tabular data (like documents or graphs).
   - Doesn’t rely only on SQL; uses other query methods.
   - Examples: MongoDB, Redis, DynamoDB.

Choosing a DBMS depends on:
- **Data Complexity**: Simple tables or varied data types?
- **Scalability**: How much data will you store?
- **Data Types**: Structured (tables) or unstructured (documents, graphs)?

### Relational Data Model
- **Developed**: By IBM in 1970.
- **Key Concepts**:
  - **Tables**: Represent entities (e.g., "Students" table for student data).
    - **Primary Key**: A unique identifier for each row (e.g., `student_id`).
    - **Rows (Tuples)**: Individual records (e.g., one student’s data).
    - **Columns (Attributes)**: Characteristics of the entity (e.g., `name`, `age`).
  - **Keys**:
    - **Primary Key**: Ensures each row is unique (e.g., no two students have the same `student_id`).
    - **Foreign Key**: Links tables by referencing a primary key in another table (e.g., a `class_id` in the "Students" table links to the "Classes" table).
  - **Integrity Rules**:
    - **Entity Integrity**: Primary keys can’t be null (empty).
    - **Referential Integrity**: Foreign keys must match a valid primary key in another table or be null.
- **Popularity**: Relational models are the most common, but NoSQL is gaining traction for flexibility.

### NoSQL Data Models
NoSQL databases are designed for scalability and flexibility, handling data that doesn’t fit neatly into tables. They include:
- **Document**: Stores data as JSON-like documents (e.g., MongoDB).
- **Graph**: Stores data as nodes and edges for relationships (e.g., Neo4j).
- **Key-Value**: Stores data as simple key-value pairs (e.g., Redis).
- **Example (Key-Value)**: A key like `student_001` might point to a value like `name: John, age: 20`.

### Other Data Models
Less common models include:
- **Hierarchical**: Data in a tree-like structure (parent-child, like a family tree). Used in older systems like IBM’s IMS.
- **Network**: Allows multiple parent-child links, more flexible but complex.
- **Object-Oriented**, **Flat**, **Context**, **Semantic**: Specialized models not covered in this course.

### Basic SQL Queries
SQL queries let you interact with data. Here are common commands with examples:
- **CREATE TABLE**: Builds a new table.
  ```sql
  CREATE TABLE Students (
      student_id INT,
      first_name VARCHAR(255),
      last_name VARCHAR(255)
  );
  ```
  *Explanation*: Creates a table called `Students` with columns for `student_id`, `first_name`, and `last_name`.
- **DROP TABLE**: Deletes a table.
  ```sql
  DROP TABLE Students;
  ```
  *Explanation*: Removes the `Students` table entirely.
- **SELECT**: Retrieves data.
  ```sql
  SELECT * FROM Students;
  ```
  *Explanation*: Gets all columns (`*`) from the `Students` table. The `;` marks the end of the query.
- **SELECT with Conditions**:
  ```sql
  SELECT first_name, last_name FROM Students WHERE age > 20;
  ```
  *Explanation*: Gets `first_name` and `last_name` for students older than 20.
- **SELECT with Sorting**:
  ```sql
  SELECT * FROM Students ORDER BY age DESC;
  ```
  *Explanation*: Gets all student data, sorted by `age` in descending order (`DESC`).
- **INSERT**: Adds new data.
  ```sql
  INSERT INTO Students (student_id, first_name, last_name, age)
  VALUES (5, 'John', 'Doe', 20);
  ```
  *Explanation*: Adds a new student with `student_id=5`, `first_name=John`, `last_name=Doe`, and `age=20`.
- **UPDATE**: Modifies existing data.
  ```sql
  UPDATE Students SET age = 25 WHERE student_id = 3;
  ```
  *Explanation*: Changes the `age` to 25 for the student with `student_id=3`.
- **DELETE**: Removes data.
  ```sql
  DELETE FROM Students WHERE student_id = 3;
  ```
  *Explanation*: Deletes the student with `student_id=3`.

### Resources
- [W3Schools SQL Syntax](https://www.w3schools.com/sql/sql_syntax.asp)
- [AWS: What is SQL?](https://aws.amazon.com/what-is/sql/)
- [GeeksforGeeks: Hierarchical Model](https://www.geeksforgeeks.org/hierarchical-model-in-dbms/)
- [TutorialsPoint: Network Data Model](https://www.tutorialspoint.com/Network-Data-Model)
- [W3Schools: SQL Create Table](https://www.w3schools.com/sql/sql_create_table.asp)
- [PostgreSQL Windows Download](https://www.postgresql.org/download/windows/)
- [Context Model Overview](https://why-change.com/2021/02/09/a-context-model-in-5-minutes/)

---

## Week 2: Advanced SQL and Database Structures

### Database Warehouses
A **data warehouse** is a special database designed for analyzing large amounts of data, unlike operational databases (RDBMS/NoSQL) that handle daily transactions. Data warehouses use **denormalized schemas** (like Star or Snowflake) to make complex queries faster for reporting and analytics.

- **Star Schema**: A central "fact" table (e.g., sales data) connected to "dimension" tables (e.g., products, customers).
- **Snowflake Schema**: A more complex version of Star, with dimension tables broken into sub-tables for efficiency.

### Online Transaction Processing (OLTP)
- **Purpose**: Handles many short, fast operations like inserting, updating, or deleting data (e.g., retail purchases, banking transactions).
- **Features**: Uses RDBMS, frequent incremental backups (every few hours or minutes).

### Online Analytical Processing (OLAP)
- **Purpose**: Analyzes complex data for insights (e.g., data mining, business reports).
- **Features**: Less frequent backups (daily, monthly, or yearly), optimized for multidimensional analysis.

### ETL (Extract, Transform, Load)
**ETL** moves data from OLTP databases to OLAP data warehouses:
1. **Extract**: Pull data from the source (e.g., a retail database).
2. **Transform**: Clean or reformat data for analysis.
3. **Load**: Store data in the data warehouse.
Many tools automate ETL, covered in Week 4.

### SQL Command Categories
SQL commands are grouped into:
- **DML (Data Manipulation Language)**: Manages data (e.g., `SELECT`, `INSERT`, `UPDATE`, `DELETE`).
- **DDL (Data Definition Language)**: Defines database structure (e.g., `CREATE`, `ALTER`, `DROP`, `TRUNCATE`).
- **DCL (Data Control Language)**: Manages permissions (e.g., `GRANT`, `REVOKE`).

### Aggregate Functions
**Aggregate functions** summarize data:
- **COUNT**: Counts rows (e.g., `SELECT COUNT(*) AS total_students FROM Students;` counts all students).
- **SUM**: Adds values in a column.
- **AVG**: Calculates the average (e.g., `SELECT AVG(age) AS average_age FROM Students;`).
- **MAX/MIN**: Finds the highest/lowest value (e.g., `SELECT MIN(age) AS youngest_age, MAX(age) AS oldest_age FROM Students;`).

### Nested Queries (Subqueries)
**Subqueries** are queries inside other queries for complex results:
- **Example**:
  ```sql
  SELECT * FROM Students WHERE class_id = (
      SELECT class_id
      FROM Students
      GROUP BY class_id
      ORDER BY COUNT(student_id) DESC
      LIMIT 1
  );
  ```
  *Explanation*: Finds students in the most populated class. The inner query counts students per class, sorts by count, and limits to one class ID.

- **Complex Example**:
  ```sql
  SELECT class_name
  FROM Classes
  WHERE id IN (
      SELECT class_id
      FROM Students
      GROUP BY class_id
      HAVING COUNT(id) > (
          SELECT COUNT(id)
          FROM Students
          WHERE class_id = (
              SELECT id FROM Classes WHERE class_name = 'English'
          )
      )
  );
  ```
  *Explanation*: Returns classes with more students than the "English" class. `HAVING` filters aggregate results.

### Common Table Expressions (CTEs)
**CTEs** create temporary result sets for cleaner, more readable queries:
- **Syntax**:
  ```sql
  WITH cte_name (column1, column2, ...)
  AS (
      -- CTE query
  )
  -- Main query
  ```
- **Example**:
  ```sql
  WITH AverageAge AS (
      SELECT AVG(age) AS avg_age FROM Students
  )
  SELECT first_name, last_name, age
  FROM Students, AverageAge
  WHERE age > AverageAge.avg_age;
  ```
  *Explanation*: Finds students older than the average age, using a CTE to compute the average.

### Window Functions
**Window functions** calculate values for each row based on a "window" of related rows:
- **Example**:
  ```sql
  SELECT order_id, customer_id, amount, SUM(amount)
  OVER (PARTITION BY customer_id ORDER BY order_id) AS running_total
  FROM Orders
  ORDER BY customer_id, order_id;
  ```
  *Explanation*: Calculates a running total of order amounts per customer, partitioned by `customer_id`.

### Handling NULL Values
**NULL** means missing data. Handle it with:
- **Check for NULL**:
  ```sql
  SELECT * FROM Students WHERE age IS NULL;
  SELECT * FROM Students WHERE age IS NOT NULL;
  ```
- **Update NULL**:
  ```sql
  UPDATE Students SET last_name = 'Smith' WHERE last_name IS NULL;
  ```
- **CASE for Display**:
  ```sql
  SELECT CASE
      WHEN first_name IS NULL THEN 'Unknown First Name'
      ELSE first_name
  END
  FROM Students;
  ```

### String Operations
**String operations** manipulate text:
- **CONCAT**: Joins strings (e.g., `SELECT CONCAT('Hello', ' ', 'World');` → `Hello World`).
- **LENGTH**: Counts characters (e.g., `SELECT LENGTH('Hello');` → `5`).
- **UPPER/LOWER**: Changes case (e.g., `SELECT UPPER('hello');` → `HELLO`).
- **TRIM**: Removes spaces (e.g., `SELECT TRIM('   HELLO   ');` → `HELLO`).
- **SUBSTRING**: Extracts part of a string (e.g., `SELECT SUBSTRING('Hello World', 1, 5);` → `Hello`).
- **REPLACE**: Replaces text (e.g., `SELECT REPLACE('Hello World', 'World', 'Everyone');` → `Hello Everyone`).
- **POSITION**: Finds text position (e.g., `SELECT POSITION('World' IN 'Hello World');` → `7`).

### Date and Time Operations
**Date/time functions** handle dates:
- **NOW**: Current date/time (e.g., `SELECT NOW();` → `2023-07-27 12:34:56`).
- **DATE/TIME**: Extracts date or time (e.g., `SELECT DATE(NOW());` → `2023-07-27`).
- **DATE_ADD**: Adds time (e.g., `SELECT DATE_ADD(NOW(), INTERVAL 1 DAY);` → next day).
- **DATEDIFF**: Days between dates (e.g., `SELECT DATEDIFF('2023-07-28', '2023-07-27');` → `1`).
- **TIMESTAMPDIFF**: Time difference (e.g., `SELECT TIMESTAMPDIFF(MINUTE, '2023-07-27 12:34:56', '2023-07-27 12:54:56');` → `20`).

### SQL Joins
**Joins** combine data from multiple tables:
- **INNER JOIN**:
  ```sql
  SELECT A.column_1, B.column_2
  FROM table_1 A
  INNER JOIN table_2 B ON A.student_id = B.student_id;
  ```
  *Explanation*: Returns rows with matching `student_id` in both tables. `A` and `B` are aliases for clarity.
- **Other Joins**:
  - **LEFT JOIN**: All rows from the left table, matching rows from the right.
  - **RIGHT JOIN**: All rows from the right table, matching rows from the left.
  - **FULL JOIN**: All rows from both tables, with matches where available.
  - **SELF JOIN**: Joins a table with itself.
  - **NON-EQUI JOIN**: Uses non-equality conditions (e.g., `A.column_1 < B.column_2`).
- **Example**:
  ```sql
  SELECT classes.class_name
  FROM Classes LEFT JOIN Students ON classes.id = students.class_id
  WHERE students.id IS NULL;
  ```
  *Explanation*: Finds classes with no students.

### SQL Views
**Views** are virtual tables based on a query, acting like permanent CTEs:
- **Create View**:
  ```sql
  CREATE VIEW StudentInfo AS
  SELECT student_id, first_name, last_name, enrolled
  FROM Students
  WHERE enrolled = 1;
  ```
- **Update View**:
  ```sql
  CREATE OR REPLACE VIEW StudentInfo AS
  SELECT student_id, first_name, last_name, class, enrolled
  FROM Students
  WHERE enrolled = 1;
  ```
- **Drop View**:
  ```sql
  DROP VIEW StudentInfo;
  ```
- **Benefits**: Simplifies queries, enhances security by limiting data access, ensures consistency.
- **Limitations**: Slower for complex queries, read-only, dependent on underlying tables.

### SQL Indexes
**Indexes** speed up data retrieval but slow down modifications:
- **Clustered Index**: Sorts table data physically (one per table).
  ```sql
  CREATE CLUSTERED INDEX idx_name ON table_name (column1, column2);
  ```
- **Non-Clustered Index**: Uses pointers, allows multiple indexes.
  ```sql
  CREATE NONCLUSTERED INDEX idx_name ON table_name (column1, column2);
  ```

### Resources
- [SQL Aggregate Functions](https://mode.com/sql-tutorial/sql-aggregate-functions/)
- [SQL Window Functions](https://mode.com/sql-tutorial/sql-window-functions/)
- [SQL NULL Values](https://www.w3schools.com/sql/sql_null_values.asp)
- [Star Schema Diagram](https://en.wikipedia.org/wiki/Star_schema#/media/File:Star-schema.png)

---

## Week 3: Database Architecture

### What is Database Architecture?
**Database architecture** refers to the tools, technologies, and design choices used to store, manage, and access data. It’s like planning a house: you decide the layout based on needs like size, speed, and reliability.

### Factors Affecting Architecture
- **Data Size**: How much data will you store?
- **Data Type**: Structured (tables) or unstructured (documents)?
- **Performance**: How fast do queries need to run?
- **Scalability**: Can the database grow with demand?
- **Reliability**: How much downtime is acceptable?
- **Concurrency**: How many users access the database at once?

### Database Architecture Tiers
- **Single-Tier**: Everything (app and data) on one machine.
- **Two-Tier**: App on client, database on server.
- **Three-Tier**: Separates UI, application logic, and data for scalability.
  - **External Schema (User View)**: What users see, customized by access level.
  - **Conceptual Schema**: Logical view of tables, relationships, and constraints.
  - **Internal Schema**: Physical storage details (e.g., data blocks, indexes).
  - **Learn More**: [Three-Level Schema Architecture](https://www.tutorialspoint.com/explain-the-three-level-schema-architecture-in-dbms)

### Benefits of Three-Tier Architecture
- **Scalability**: Scale each layer independently.
- **Maintainability**: Update one layer without affecting others.
- **Security**: Apply different security measures per layer.
- **Flexibility**: Switch technologies easily.
- **Performance**: Optimize each layer for its task.

### SMP vs. MPP Architecture
- **SMP (Symmetric Multiprocessing)**:
  - Processors share one memory pool.
  - Easy to program, scalable by adding processors.
- **MPP (Massively Parallel Processing)**:
  - Each processor has its own memory, connected via a network.
  - Highly scalable, suited for big data (e.g., Google BigQuery, Amazon Redshift).

### Bronze, Silver, Gold Layers
In **data warehouses**, data is organized into layers:
- **Bronze (Raw)**: Unprocessed data, minimally cleaned, for engineers.
- **Silver (Cleansed)**: Cleaned and normalized data for analysis.
- **Gold (Consumption)**: Optimized, business-ready data for end-users.

### Data Warehouse vs. Operational Database
- **Data Warehouse**:
  - For analytics and reporting.
  - Denormalized schemas (Star/Snowflake).
  - Complex queries, historical data.
- **Operational Database**:
  - For daily transactions (OLTP).
  - Normalized schemas, real-time updates.

### Data Structures
- **Structured**: Organized in tables (e.g., MySQL).
- **Semi-Structured**: Flexible with tags (e.g., JSON in MongoDB).
- **Unstructured**: No fixed format (e.g., files in Amazon S3).

---

## Week 4: SQL Wrap-Up

### Set Operations
Combine results from multiple queries:
- **UNION**: Merges unique rows from two queries.
  ```sql
  SELECT emp_position FROM Employees
  UNION
  SELECT contractor_position FROM Contractors;
  ```
- **EXCEPT (MINUS)**: Returns rows in the first query not in the second.
  ```sql
  SELECT emp_position FROM Employees
  EXCEPT
  SELECT contractor_position FROM Contractors;
  ```
- **INTERSECT**: Returns common rows.
  ```sql
  SELECT emp_position FROM Employees
  INTERSECT
  SELECT contractor_position FROM Contractors;
  ```

### ACID Properties
**ACID** ensures reliable transactions:
- **Atomicity**: Transactions complete fully or not at all (e.g., a bank transfer either happens or doesn’t).
- **Consistency**: Ensures data follows rules (e.g., no negative balances).
- **Isolation**: Transactions don’t interfere (e.g., one user’s transfer doesn’t affect another’s balance check).
- **Durability**: Committed transactions are saved, even after crashes.

### Normalization
**Normalization** organizes data to reduce redundancy and ensure integrity:
- **1NF (First Normal Form)**: No repeating groups, atomic values.
- **2NF**: 1NF + non-key attributes depend on the entire primary key.
- **3NF**: 2NF + no non-key attributes depend on other non-key attributes.
- **BCNF**: A stricter version of 3NF.
- **Example**: Split a table with customer, sales, and book data into separate tables to avoid duplication.

### Referential Integrity
Ensures relationships between tables stay consistent (e.g., foreign keys match primary keys). RDBMS enforces this with constraints, preventing invalid data or deletions that break links.

### Data Governance
**Data governance** manages data quality, security, and usability:
- **Stewardship**: Assign stewards to maintain data quality and security.
- **Management**: Handle data collection, storage, and access.
- **Security**: Protect data with encryption, access controls, and compliance with laws.

### ETL vs. ELT
- **ETL (Extract, Transform, Load)**: Transform data before loading into a warehouse. Suited for complex transformations.
- **ELT (Extract, Load, Transform)**: Load raw data, then transform in the warehouse. Faster for large datasets.
- **Factors**: Technology, data volume, transformation complexity, latency, and cost.

### Incremental Load
Loads only new or updated data:
- **Timestamp**: Use `createdAt` or `updatedAt` to track changes.
- **Change Tracking**: Logs inserts, updates, deletes.
- **Change Data Capture (CDC)**: Tracks actual data changes.

### Upsert Logic
**Upsert** (Update or Insert):
- Inserts new records or updates existing ones.
- Example (PostgreSQL):
  ```sql
  INSERT INTO Students (id, name) VALUES (1, 'John')
  ON CONFLICT (id) DO UPDATE SET name = EXCLUDED.name;
  ```

### Resources
- [Database Normalization](https://www.databasestar.com/database-normalization/)
- [Google: Data Governance](https://cloud.google.com/learn/what-is-data-governance)
- [AWS: Data Governance](https://aws.amazon.com/what-is/data-governance/)

---

## Week 5: Conceptual and Logical Modeling

### Entity-Relationship Model (ER Model)
An **ER Model** is a blueprint for designing a database:
- **Entities**: Objects like `Students` or `Courses`.
- **Attributes**: Properties (e.g., `Student_ID`, `Name`).
- **Relationships**: Connections (e.g., one instructor teaches many courses).
- **Cardinality**: How many instances relate (e.g., one-to-many).
- **Ordinality**: Minimum relationships (e.g., a course must have at least one instructor).
- **Keys**: Primary (unique identifier), Foreign (links tables).
- **Composite Attributes**: Can be split (e.g., `Full Name` → `First Name`, `Last Name`).
- **Derived Attributes**: Calculated (e.g., `Age` from `Date of Birth`).

### ERD Types
- **Conceptual ERD**: High-level, no data types, focuses on entities and relationships.
- **Logical ERD**: Adds column types, primary/foreign keys, and normalization.
- **Physical ERD**: Final blueprint, specific to the DBMS (e.g., PostgreSQL’s `createdAt` fields).

### External Tables
**External tables** point to data outside the database (e.g., CSV files, Amazon S3):
- **Pros**: No data duplication, cost-effective, supports varied formats.
- **Cons**: Slower performance, limited features, security challenges.
- **PostgreSQL Example**:
  ```sql
  CREATE EXTENSION IF NOT EXISTS file_fdw;
  CREATE SERVER csv_server FOREIGN DATA WRAPPER file_fdw;
  CREATE FOREIGN TABLE employees_external (
      id INTEGER,
      name TEXT,
      department TEXT,
      salary FLOAT
  )
  SERVER csv_server
  OPTIONS (
      FORMAT 'csv',
      HEADER 'true',
      FILENAME '/path/to/your/csv/file.csv'
  );
  ```
- **S3 Example**: Use `s3_fdw` to connect to Amazon S3 (requires third-party module).
- **Security Considerations**: Authentication, access control, data validation, encryption, and compliance with laws (e.g., data sovereignty for medical data).

---

## Week 6: Query Optimization and Cloud Administration

### Partitioning Tables
**Partitioning** splits a large table into smaller pieces for better performance:
- **Types**:
  - **Range**: By value ranges (e.g., sales by year).
  - **List**: By specific values (e.g., by country).
  - **Hash**: Uses a hash function to distribute data evenly.
  - **Composite**: Combines multiple types.
- **Benefits**: Faster queries, easier maintenance, scalability.

### Hash Functions
A **hash function** converts data into a fixed-size value (hash) for:
- **Data Retrieval**: Fast lookups in hash tables.
- **Cryptography**: Ensuring data integrity.
- **Load Balancing**: Distributing data across servers.
- **Properties**: Uniform, deterministic, fast, resistant to reverse-engineering.

### Cloud Database Security and Privacy
- **Authentication**: Use usernames, MFA, or RBAC (e.g., AWS IAM).
- **Encryption**: In-transit (SSL/TLS) and at-rest (AWS KMS).
- **Auditing**: Log activities with AWS CloudTrail, monitor with CloudWatch.
- **Firewall/Network**: Use Security Groups, VPCs for isolation.
- **Data Masking/Anonymization**: Protect sensitive data.
- **Backups**: Regular snapshots, Multi-AZ for recovery.
- **Privacy**: Classify data, ensure compliance (e.g., GDPR), manage data sovereignty.

### Cloud Database Recovery
Protects against:
- Hardware/software failures, human errors, natural disasters, cyberattacks.
- **Recovery Types**:
  - **Backup/Restore**: Regular backups for recovery.
  - **Point-in-Time Recovery**: Restore to a specific moment.
  - **Failover**: Switch to a standby database.
  - **Replication**: Keep real-time copies.
- **Objectives**:
  - **RPO**: How much data loss is acceptable?
  - **RTO**: How quickly must recovery happen?
- **Steps**: Plan, implement, test, monitor, update.

### Cloud Database Auto-Scaling
**Auto-scaling** adjusts resources dynamically:
- **Types**:
  - **Horizontal**: Add more instances (scaling out).
  - **Vertical**: Increase instance power (scaling up).
  - **Read/Write**: Scale reads with replicas, writes with stronger nodes.
  - **Scheduled/Dynamic/Predictive**: Based on schedules, metrics, or predictions.
- **Pros**: Cost-efficient, reliable, high performance.
- **Cons**: Latency, cost monitoring, consistency challenges.

### Cloud Database Mirroring
**Mirroring** keeps real-time database copies:
- **Components**: Principal server (main), mirror server (copy), optional witness.
- **Types**:
  - **Synchronous**: Ensures data consistency, may add latency.
  - **Asynchronous**: Faster, with slight data lag.
- **Pros**: High availability, data protection, load balancing.
- **Cons**: Latency, cost, complexity.

### Failover Clusters
**Failover clusters** ensure availability by switching to standby nodes:
- **Components**: Nodes, shared storage, cluster software, networking.
- **Types**: Active/Passive, Active/Active, N+1.
- **Pros**: High availability, scalability.
- **Cons**: Complex, costly, data consistency challenges.

---

## Week 8: Introduction to Amazon Cloud

### Amazon Web Services (AWS)
**AWS**, launched in 2006, is a cloud platform offering computing, storage, networking, analytics, and more. Used by companies like Airbnb and Slack, it’s compliant with HIPAA, GDPR, and PIPEDA.

### AWS Advantages
- **Scalability**: Adjust resources based on demand.
- **Cost-Effective**: Pay only for what you use.
- **Flexibility**: Supports many languages and platforms.
- **Global Reach**: Data centers worldwide.
- **Community**: Large developer ecosystem.

### Use Cases
- Web hosting, big data analytics, backups, IoT, software development.

### Amazon RDS
**RDS** is a managed relational database service supporting MySQL, PostgreSQL, SQL Server, and more:
- **Features**:
  - **Automated Backups**: Daily snapshots stored in S3.
  - **Read Replicas**: Offload read traffic.
  - **Multi-AZ**: Ensures availability with failover.
  - **Security**: VPC, encryption, IAM.
  - **Monitoring**: CloudWatch for metrics and alerts.
  - **Scalability**: Vertical (upgrade instance) or horizontal (add replicas).
- **Maintenance**: Configurable maintenance windows.

### Amazon VPC
**VPC** (Virtual Private Cloud) is a private network in AWS:
- **Components**:
  - **Subnets**: Public (internet-accessible) or private.
  - **Internet Gateway**: Connects VPC to the internet.
  - **Route Tables**: Direct network traffic.
  - **Security Groups/NACLs**: Control traffic at instance/subnet levels.
  - **VPC Peering**: Connects VPCs.
  - **NAT/VPN/Direct Connect**: Manage external access.
- **Features**: Isolation, customization, high availability.

### Subnet Groups
**DB Subnet Groups** in RDS ensure high availability:
- Include subnets from multiple Availability Zones.
- Support failover during outages.
- Immutable VPC but flexible subnets.

### Private vs. Public VPCs
- **Public VPC**: Subnets with internet access (e.g., for web servers).
- **Private VPC**: No direct internet access, uses NAT or VPN (e.g., for databases).
- **Hybrid**: Combines public and private subnets.

### VPC Security Best Practices
- **Least Privilege**: Limit access.
- **VPC Flow Logs**: Monitor traffic.
- **NACLs/Security Groups**: Control traffic.
- **AWS Config/GuardDuty**: Audit and detect threats.
- **PrivateLink**: Secure service access.
- **Encryption**: Protect data in transit and at rest.

### Resources
- [AWS VPC Sharing](https://aws.amazon.com/blogs/architecture/using-vpc-sharing-for-a-cost-effective-multi-account-microservice-architecture/)
- [AWS RDS Module](https://awsacademy.instructure.com/courses/3781/modules/items/462304)
- [AWS VPC Module](https://awsacademy.instructure.com/courses/3781/modules/items/462265)

---

## Week 9: Introduction to NoSQL and MongoDB

### What is NoSQL?
**NoSQL** (Not Only SQL) databases are flexible, schema-less systems for handling unstructured or semi-structured data:
- **Scale**: Distributes data across servers.
- **Schema-less**: No fixed structure, easy to adapt.
- **Performance**: Fast for specific workloads, avoids complex joins.

### Types of NoSQL Databases
- **Document**: JSON/BSON documents (e.g., MongoDB).
- **Column**: Column-based storage (e.g., Cassandra).
- **Key-Value**: Simple key-value pairs (e.g., Redis).
- **Graph**: Nodes and edges for relationships (e.g., Neo4j).
- **Use Cases**: Catalogs, caching, social networks, time-series data.

### NoSQL Data Example
```json
{
    "id": "1",
    "username": "JohnDoe",
    "email": "john.doe@email.com",
    "password": "2bgh54h3b124b13b1h3b12h4"
}
```

### BASE Properties
NoSQL often uses **BASE** instead of ACID:
- **Basically Available**: System stays accessible even if some nodes fail.
- **Soft State**: Data may change without input due to eventual consistency.
- **Eventually Consistent**: Data becomes consistent over time.

### ACID vs. BASE
- **ACID**: Prioritizes consistency (e.g., banking).
- **BASE**: Prioritizes availability (e.g., social media).
- **Behavior**: ACID rolls back on failure; BASE continues with possible outdated data.

### NoSQL vs. RDBMS
- **NoSQL**: Dynamic schema, no standard query language, BASE.
- **RDBMS**: Fixed schema, SQL, ACID.

### MongoDB Overview
**MongoDB** is a document-based NoSQL database:
- **Document-Based**: Stores data in BSON (Binary JSON).
- **Schema-less**: Flexible document structures.
- **Scalability**: Horizontal scaling across servers.
- **Speed**: Fast reads/writes by storing related data together.

### MongoDB Special Data Types
- **ObjectId**: Unique document identifier.
- **ISODate**: Stores dates (e.g., `ISODate("2023-08-17T00:00:00Z")`).
- **Timestamp**: Non-real-world time tracking.

### MongoDB CRUD Operations
Using MongoDB’s Node.js driver:
- **Create**:
  ```javascript
  db.collection('students').insertOne({ name: 'John Doe' });
  db.collection('students').insertMany([{ name: 'John Doe' }, { name: 'Jane Smith' }]);
  ```
- **Read**:
  ```javascript
  db.collection('students').find({}); // All records
  db.collection('students').findOne({ name: 'John Doe' }); // One record
  db.collection('students').find({ name: /^John/ }); // Names starting with 'John'
  ```
- **Update**:
  ```javascript
  db.collection('students').updateOne(
      { name: 'John Doe' },
      { $set: { grade: 12 } }
  ); // Updates one record
  db.collection('students').updateMany(
      { name: /^John/ },
      { $set: { status: 'graduated' } }
  ); // Updates multiple
  ```
- **Delete**:
  ```javascript
  db.collection('students').deleteOne({ name: 'John Doe' });
  db.collection('students').deleteMany({ status: 'graduated' });
  ```

### MongoDB Joins
Use `$lookup` to join collections:
```javascript
db.students.aggregate([{
    $lookup: {
        from: 'grades',
        localField: 'id',
        foreignField: 'student_id',
        as: 'studentGrades'
    }
}]);
```
*Explanation*: Joins `students` with `grades` using `id` and `student_id`.

### MongoDB Array Operations
- **Insert Array**:
  ```javascript
  db.students.insertOne({
      name: 'John Doe',
      subjects: ['English', 'Math']
  });
  ```
- **Add to Array**:
  ```javascript
  db.students.updateOne(
      { name: 'John Doe' },
      { $push: { subjects: 'French' } }
  );
  db.students.updateOne(
      { name: 'John Doe' },
      { $push: { subjects: { $each: ['French', 'Physics'] } } }
  );
  ```
- **Remove from Array**:
  ```javascript
  db.students.updateOne(
      { name: 'John Doe' },
      { $pull: { subjects: 'French' } }
  );
  db.students.updateMany(
      { name: 'John Doe' },
      { $pull: { scores: { $lt: 50 } } }
  ); // Removes scores < 50
  ```

### MongoDB Atlas
**MongoDB Atlas** is a managed cloud service for MongoDB, supporting AWS, Azure, and Google Cloud. Ideal for Lab 5.

### Resources
- [MongoDB Atlas Registration](https://www.mongodb.com/cloud/atlas/register)
- [MongoDB Atlas Tutorial](https://www.mongodb.com/basics/mongodb-atlas-tutorial)

---

## Week 10: Introduction to DynamoDB

### What is DynamoDB?
**DynamoDB** is AWS’s managed NoSQL database, designed for speed and scalability:
- Handles any amount of data and traffic.
- Optimized for low-latency, high-throughput applications.

### Key Features
- **Managed Service**: AWS handles setup, patching, and backups.
- **Scalability**: Auto-scales tables without downtime.
- **High Availability**: Replicates data across multiple Availability Zones.
- **Fast Performance**: Single-digit millisecond latency.
- **Flexibility**: Supports key-value and document models.
- **Data Types**: String, number, binary, Boolean, lists, maps, sets.
- **Global Tables**: Replicates data across regions.
- **Serverless**: Pay only for used resources.
- **ACID Transactions**: Ensures reliable complex operations.
- **Event-Driven**: Integrates with AWS Lambda for real-time actions.

### Core Components
- **Tables**: Store data.
- **Items**: Rows in a table.
- **Attributes**: Columns in an item.
- **Primary Key**: Unique identifier (partition key or partition + sort key).
- **Indexes**: Secondary indexes for complex queries.

### Integrations
- **AWS Services**: Lambda, API Gateway, S3, CloudFormation.
- **External**: Elasticsearch, relational databases, third-party tools.

### Access Control
- **IAM**: Manages permissions via policies.
- **Resource-Based Policies**: Control access to DynamoDB resources.
- **Attribute-Based**: Restrict access to specific attributes.
- **VPC Endpoints**: Keep traffic within a VPC.

### Resources
- [DynamoDB Labs](https://amazon-dynamodb-labs.workshop.aws/game-player-data/plan-model/step2.html)

---

## Week 11: Applications of Machine Learning

### Physical Denormalization
**Normalization** reduces redundancy but can slow queries due to joins. **Denormalization** adds redundant data to speed up queries:
- **Example**: Instead of joining `Orders` and `Products` tables, store product names in `Orders` to avoid joins, trading redundancy for speed.
- **Trade-offs**: Faster queries but more storage and potential inconsistency.

### Query Execution
Steps in running a SQL query:
1. **Parsing**: Check syntax.
2. **Optimization**: Choose the fastest plan using indexes and data size.
3. **Execution**: Run the plan (e.g., scan tables, join data).
4. **Presentation**: Format and return results.
Denormalization reduces joins, speeding up execution.

### Distributed Architecture
**Distributed architecture** splits tasks across multiple computers:
- **Scalability**: Add machines to handle more load.
- **Fault Tolerance**: System works if one node fails.
- **Latency**: Place resources closer to users.
- **Concurrent Processing**: Multiple nodes process tasks simultaneously.
- **Types**:
  - **Client-Server**: Clients request from a central server.
  - **Three-Tier**: Adds a middle tier for logic.
  - **Peer-to-Peer**: Nodes act as both clients and servers.
  - **Master-Slave**: Master directs slave nodes.
  - **Microservices**: Independent services communicate.
  - **Grid Computing**: Nodes solve large problems.
  - **Lambda/Kappa**: For big data processing.
  - **Blockchain**: Distributed ledger with consensus.

### Challenges
- **Data Consistency**: Ensuring all nodes have the same data.
- **Network Partition**: Handling network failures.
- **Security**: Protecting multiple nodes.
- **Resource Management**: Allocating tasks efficiently.

### Machine Learning in Databases
**Machine learning (ML)** enhances databases by:
- **Handling Data Volume**: Automates analysis of large datasets.
- **Real-Time Analytics**: Speeds up decision-making.
- **Complex Queries**: Optimizes joins and subqueries.
- **Data Quality**: Cleans dirty or missing data.

### ML Applications
- **Query Optimization**:
  - Predicts best join order or index usage.
  - Optimizes caching based on usage patterns.
- **Data Compression**:
  - Recognizes patterns for efficient compression.
  - Chooses lossy vs. lossless compression.
- **Data Sharding**:
  - Analyzes query patterns to minimize cross-shard queries.
  - Balances shards to avoid bottlenecks.
- **Data Partitioning**:
  - Predicts load to optimize partitioning.
  - Clusters data for faster access.

### Google BigQuery ML
Integrates ML into databases for query optimization and analytics.

### Future of ML in Databases
- **In-Database ML**: Run models within the database.
- **Distributed ML**: Scale ML across nodes.
- **Adaptive Optimization**: Continuously improve queries.
- **Security**: Detect threats in real-time.
- **Explainable AI**: Transparent ML models.

### Resources
- [BigQuery ML](https://cloud.google.com/bigquery/docs/introduction)
- [Bit-Swap ML](https://bair.berkeley.edu/blog/2019/09/19/bit-swap/)

---
