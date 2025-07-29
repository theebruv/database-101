# Database Course Overview for Beginners

Welcome to your database journey! This guide breaks down complex database concepts into simple, easy-to-understand explanations. Think of databases as digital filing systems that help organize and find information quickly - just like how a library organizes books so you can find exactly what you need.

This document covers everything from basic database concepts to advanced cloud solutions, organized week by week. Each section includes:

-   **Simple explanations** using everyday analogies
-   **Real-world examples** you can relate to
-   **Step-by-step code examples** with detailed explanations
-   **Key terms** defined in plain English

Whether you're completely new to databases or need a refresher, this guide will help you understand how data is stored, organized, and retrieved in the digital world.

---

## Week 1: Introduction to Databases

### Course Overview

Imagine you're organizing a massive library with millions of books. You need a system to:

-   Store books in an organized way
-   Find any book quickly
-   Add new books without chaos
-   Update book information
-   Remove books when needed

That's exactly what databases do with digital information! This course teaches you two main approaches:

**Relational Databases (SQL)**: Like a well-organized library with:

-   Books sorted into categories (tables)
-   A card catalog system (relationships between tables)
-   Strict rules about where everything goes (structure)
-   Examples: Customer information, bank records, school grades

**NoSQL Databases**: Like a flexible storage system that can handle:

-   Different types of items (documents, images, videos)
-   Changing requirements (no fixed structure)
-   Massive amounts of data spread across multiple locations
-   Examples: Social media posts, product catalogs, sensor data

You'll learn to "speak" to these databases using special languages (SQL and NoSQL queries) and build real projects through labs, assignments, and a final case study.

### Course Expectations

-   **What You'll Do**: Over 12 weeks, you'll complete:
    -   **5 Lab Activities** (3% each, total 15%): Practical exercises to build skills.
    -   **2 Assignments** (10% each, total 20%): In-depth tasks to apply concepts.
    -   **2 Tests** (Midterm 20%, Final 20%): Assessments of your understanding.
    -   **Case Study** (25%): A final project to design and analyze a database.
-   **Review the Course Outline**: Check the detailed syllabus to understand the schedule and expectations.

### Software Requirements

-   **Operating System**: Windows is recommended for local development, but you can use other systems like macOS or Linux. Note that technical support is only provided for Windows.
-   **Tools**:
    -   **PgAdmin**: Used for SQL and relational databases (like PostgreSQL).
    -   **MongoDB**: Used for NoSQL databases.
-   **Helpful Resources**:
    -   [W3Schools](https://www.w3schools.com/): Beginner-friendly tutorials for SQL and more.
    -   [AWS Workshops](https://workshops.aws/): Practical guides for cloud database tools.

### What is SQL?

**SQL** (Structured Query Language) is like learning to speak to a database. Just as you might ask a librarian "Can you find me all books by Stephen King published after 2010?", SQL lets you ask a database questions like "Show me all students with grades above 85."

**Real-world analogy**: Imagine SQL as a universal translator between you and a very organized, but literal-minded assistant who manages your data. This assistant can:

-   **Store new information**: "Please add this new student to our records"
-   **Find specific data**: "Show me all students in Computer Science"
-   **Update existing records**: "Change John's grade from B to A"
-   **Remove outdated information**: "Delete all records from students who graduated"
-   **Organize and summarize**: "Count how many students are in each major"

**Simple example**: A student database table might look like this:

```
| Student_ID | Name    | Major           | Grade |
|------------|---------|-----------------|-------|
| 001        | Alice   | Computer Science| A     |
| 002        | Bob     | Mathematics     | B+    |
| 003        | Carol   | Computer Science| A-    |
```

With SQL, you could ask: "Show me all Computer Science students" and get Alice and Carol's information instantly.

-   **Learn More**: [AWS: What is SQL?](https://aws.amazon.com/what-is/sql/)

### SQL Background

-   **Purpose**: SQL is used to manage **relational databases**, where data is organized in tables with defined relationships.
-   **History**: Developed by IBM in the 1970s and standardized by the American National Standards Institute (ANSI).
-   **Uses**: Widely used in data analysis, software development, data science, and data engineering.

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

-   **Data Complexity**: Simple tables or varied data types?
-   **Scalability**: How much data will you store?
-   **Data Types**: Structured (tables) or unstructured (documents, graphs)?

### Relational Data Model

-   **Developed**: By IBM in 1970.
-   **Key Concepts**:
    -   **Tables**: Represent entities (e.g., "Students" table for student data).
        -   **Primary Key**: A unique identifier for each row (e.g., `student_id`).
        -   **Rows (Tuples)**: Individual records (e.g., one student’s data).
        -   **Columns (Attributes)**: Characteristics of the entity (e.g., `name`, `age`).
    -   **Keys**:
        -   **Primary Key**: Ensures each row is unique (e.g., no two students have the same `student_id`).
        -   **Foreign Key**: Links tables by referencing a primary key in another table (e.g., a `class_id` in the "Students" table links to the "Classes" table).
    -   **Integrity Rules**:
        -   **Entity Integrity**: Primary keys can’t be null (empty).
        -   **Referential Integrity**: Foreign keys must match a valid primary key in another table or be null.
-   **Popularity**: Relational models are the most common, but NoSQL is gaining traction for flexibility.

### NoSQL Data Models

NoSQL databases are designed for scalability and flexibility, handling data that doesn’t fit neatly into tables. They include:

-   **Document**: Stores data as JSON-like documents (e.g., MongoDB).
-   **Graph**: Stores data as nodes and edges for relationships (e.g., Neo4j).
-   **Key-Value**: Stores data as simple key-value pairs (e.g., Redis).
-   **Example (Key-Value)**: A key like `student_001` might point to a value like `name: John, age: 20`.

### Other Data Models

Less common models include:

-   **Hierarchical**: Data in a tree-like structure (parent-child, like a family tree). Used in older systems like IBM’s IMS.
-   **Network**: Allows multiple parent-child links, more flexible but complex.
-   **Object-Oriented**, **Flat**, **Context**, **Semantic**: Specialized models not covered in this course.

### Basic SQL Queries

Think of SQL queries as polite requests to your database assistant. Just like you might ask a librarian "Could you please show me all books by Shakespeare?", you ask the database "Could you please show me all students in Computer Science?"

**The CRUD Operations** (Create, Read, Update, Delete) - the four basic things you can do with data:

-   **CREATE TABLE**: Builds a new table (like setting up a new filing cabinet with labeled drawers).

    ```sql
    CREATE TABLE Students (
        student_id INT,
        first_name VARCHAR(255),
        last_name VARCHAR(255)
    );
    ```

    _Explanation_: Creates a table called `Students` with three columns:

    -   `student_id` (INT = integer/whole number)
    -   `first_name` (VARCHAR(255) = text up to 255 characters)
    -   `last_name` (VARCHAR(255) = text up to 255 characters)

    Think of this as creating a spreadsheet with column headers ready for data.

-   **DROP TABLE**: Deletes a table.
    ```sql
    DROP TABLE Students;
    ```
    _Explanation_: Removes the `Students` table entirely.
-   **SELECT**: Retrieves data (like asking "Show me what's in the filing cabinet").

    ```sql
    SELECT * FROM Students;
    ```

    _Explanation_: Gets all columns (`*` means "everything") from the `Students` table. The `;` marks the end of the query (like a period at the end of a sentence).

    **What you might see:**

    ```
    | student_id | first_name | last_name |
    |------------|------------|-----------|
    | 1          | Alice      | Johnson   |
    | 2          | Bob        | Smith     |
    ```

-   **SELECT with Conditions**:
    ```sql
    SELECT first_name, last_name FROM Students WHERE age > 20;
    ```
    _Explanation_: Gets `first_name` and `last_name` for students older than 20.
-   **SELECT with Sorting**:
    ```sql
    SELECT * FROM Students ORDER BY age DESC;
    ```
    _Explanation_: Gets all student data, sorted by `age` in descending order (`DESC`).
-   **INSERT**: Adds new data (like filing a new document in the cabinet).

    ```sql
    INSERT INTO Students (student_id, first_name, last_name, age)
    VALUES (5, 'John', 'Doe', 20);
    ```

    _Explanation_: Adds a new student record with specific information:

    -   Student ID: 5
    -   First name: John
    -   Last name: Doe
    -   Age: 20

    **Important**: The order of values must match the order of column names you specify!

-   **UPDATE**: Modifies existing data (like correcting information in a file).

    ```sql
    UPDATE Students SET age = 25 WHERE student_id = 3;
    ```

    _Explanation_: Changes the `age` to 25 for the student with `student_id=3`.

    **Be careful!** Always use WHERE to specify which record to update. Without WHERE, you'd change ALL students' ages to 25!

-   **DELETE**: Removes data (like shredding a document).

    ```sql
    DELETE FROM Students WHERE student_id = 3;
    ```

    _Explanation_: Permanently removes the student with `student_id=3` from the database.

    **Warning!** This is permanent! Always double-check your WHERE condition. Without WHERE, you'd delete ALL students!

### Resources

-   [W3Schools SQL Syntax](https://www.w3schools.com/sql/sql_syntax.asp)
-   [AWS: What is SQL?](https://aws.amazon.com/what-is/sql/)
-   [GeeksforGeeks: Hierarchical Model](https://www.geeksforgeeks.org/hierarchical-model-in-dbms/)
-   [TutorialsPoint: Network Data Model](https://www.tutorialspoint.com/Network-Data-Model)
-   [W3Schools: SQL Create Table](https://www.w3schools.com/sql/sql_create_table.asp)
-   [PostgreSQL Windows Download](https://www.postgresql.org/download/windows/)
-   [Context Model Overview](https://why-change.com/2021/02/09/a-context-model-in-5-minutes/)

---

## Week 2: Advanced SQL and Database Structures

### Database Warehouses

A **data warehouse** is a special database designed for analyzing large amounts of data, unlike operational databases (RDBMS/NoSQL) that handle daily transactions. Data warehouses use **denormalized schemas** (like Star or Snowflake) to make complex queries faster for reporting and analytics.

-   **Star Schema**: A central "fact" table (e.g., sales data) connected to "dimension" tables (e.g., products, customers).
-   **Snowflake Schema**: A more complex version of Star, with dimension tables broken into sub-tables for efficiency.

### Online Transaction Processing (OLTP)

-   **Purpose**: Handles many short, fast operations like inserting, updating, or deleting data (e.g., retail purchases, banking transactions).
-   **Features**: Uses RDBMS, frequent incremental backups (every few hours or minutes).

### Online Analytical Processing (OLAP)

-   **Purpose**: Analyzes complex data for insights (e.g., data mining, business reports).
-   **Features**: Less frequent backups (daily, monthly, or yearly), optimized for multidimensional analysis.

### ETL (Extract, Transform, Load)

**ETL** moves data from OLTP databases to OLAP data warehouses:

1. **Extract**: Pull data from the source (e.g., a retail database).
2. **Transform**: Clean or reformat data for analysis.
3. **Load**: Store data in the data warehouse.
   Many tools automate ETL, covered in Week 4.

### SQL Command Categories

SQL commands are grouped into:

-   **DML (Data Manipulation Language)**: Manages data (e.g., `SELECT`, `INSERT`, `UPDATE`, `DELETE`).
-   **DDL (Data Definition Language)**: Defines database structure (e.g., `CREATE`, `ALTER`, `DROP`, `TRUNCATE`).
-   **DCL (Data Control Language)**: Manages permissions (e.g., `GRANT`, `REVOKE`).

### Aggregate Functions

**Aggregate functions** are like having a calculator that works on entire columns of data. Instead of looking at individual records, they give you summary information about groups of data.

**Think of it like analyzing a class of students:**

-   **COUNT**: "How many students are in the class?"

    ```sql
    SELECT COUNT(*) AS total_students FROM Students;
    ```

    _Result_: `total_students: 25` (counts all rows)

-   **SUM**: "What's the total of all test scores?"

    ```sql
    SELECT SUM(test_score) AS total_points FROM Students;
    ```

    _Result_: `total_points: 2150` (adds up all test scores)

-   **AVG**: "What's the average age of students?"

    ```sql
    SELECT AVG(age) AS average_age FROM Students;
    ```

    _Result_: `average_age: 20.5` (calculates the mean)

-   **MAX/MIN**: "Who's the oldest and youngest?"
    ```sql
    SELECT MIN(age) AS youngest_age, MAX(age) AS oldest_age FROM Students;
    ```
    _Result_: `youngest_age: 18, oldest_age: 24`

**Real-world example**: A store manager might ask:

-   "How many products do we have?" (COUNT)
-   "What's our total inventory value?" (SUM of price × quantity)
-   "What's the average product price?" (AVG)

### Nested Queries (Subqueries)

**Subqueries** are queries inside other queries for complex results:

-   **Example**:

    ```sql
    SELECT * FROM Students WHERE class_id = (
        SELECT class_id
        FROM Students
        GROUP BY class_id
        ORDER BY COUNT(student_id) DESC
        LIMIT 1
    );
    ```

    _Explanation_: Finds students in the most populated class. The inner query counts students per class, sorts by count, and limits to one class ID.

-   **Complex Example**:
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
    _Explanation_: Returns classes with more students than the "English" class. `HAVING` filters aggregate results.

### Common Table Expressions (CTEs)

**CTEs** create temporary result sets for cleaner, more readable queries:

-   **Syntax**:
    ```sql
    WITH cte_name (column1, column2, ...)
    AS (
        -- CTE query
    )
    -- Main query
    ```
-   **Example**:
    ```sql
    WITH AverageAge AS (
        SELECT AVG(age) AS avg_age FROM Students
    )
    SELECT first_name, last_name, age
    FROM Students, AverageAge
    WHERE age > AverageAge.avg_age;
    ```
    _Explanation_: Finds students older than the average age, using a CTE to compute the average.

### Window Functions

**Window functions** calculate values for each row based on a "window" of related rows:

-   **Example**:
    ```sql
    SELECT order_id, customer_id, amount, SUM(amount)
    OVER (PARTITION BY customer_id ORDER BY order_id) AS running_total
    FROM Orders
    ORDER BY customer_id, order_id;
    ```
    _Explanation_: Calculates a running total of order amounts per customer, partitioned by `customer_id`.

### Handling NULL Values

**NULL** means missing data. Handle it with:

-   **Check for NULL**:
    ```sql
    SELECT * FROM Students WHERE age IS NULL;
    SELECT * FROM Students WHERE age IS NOT NULL;
    ```
-   **Update NULL**:
    ```sql
    UPDATE Students SET last_name = 'Smith' WHERE last_name IS NULL;
    ```
-   **CASE for Display**:
    ```sql
    SELECT CASE
        WHEN first_name IS NULL THEN 'Unknown First Name'
        ELSE first_name
    END
    FROM Students;
    ```

### String Operations

**String operations** manipulate text:

-   **CONCAT**: Joins strings (e.g., `SELECT CONCAT('Hello', ' ', 'World');` → `Hello World`).
-   **LENGTH**: Counts characters (e.g., `SELECT LENGTH('Hello');` → `5`).
-   **UPPER/LOWER**: Changes case (e.g., `SELECT UPPER('hello');` → `HELLO`).
-   **TRIM**: Removes spaces (e.g., `SELECT TRIM('   HELLO   ');` → `HELLO`).
-   **SUBSTRING**: Extracts part of a string (e.g., `SELECT SUBSTRING('Hello World', 1, 5);` → `Hello`).
-   **REPLACE**: Replaces text (e.g., `SELECT REPLACE('Hello World', 'World', 'Everyone');` → `Hello Everyone`).
-   **POSITION**: Finds text position (e.g., `SELECT POSITION('World' IN 'Hello World');` → `7`).

### Date and Time Operations

**Date/time functions** handle dates:

-   **NOW**: Current date/time (e.g., `SELECT NOW();` → `2023-07-27 12:34:56`).
-   **DATE/TIME**: Extracts date or time (e.g., `SELECT DATE(NOW());` → `2023-07-27`).
-   **DATE_ADD**: Adds time (e.g., `SELECT DATE_ADD(NOW(), INTERVAL 1 DAY);` → next day).
-   **DATEDIFF**: Days between dates (e.g., `SELECT DATEDIFF('2023-07-28', '2023-07-27');` → `1`).
-   **TIMESTAMPDIFF**: Time difference (e.g., `SELECT TIMESTAMPDIFF(MINUTE, '2023-07-27 12:34:56', '2023-07-27 12:54:56');` → `20`).

### SQL Joins

**Joins** combine data from multiple tables:

-   **INNER JOIN**:
    ```sql
    SELECT A.column_1, B.column_2
    FROM table_1 A
    INNER JOIN table_2 B ON A.student_id = B.student_id;
    ```
    _Explanation_: Returns rows with matching `student_id` in both tables. `A` and `B` are aliases for clarity.
-   **Other Joins**:
    -   **LEFT JOIN**: All rows from the left table, matching rows from the right.
    -   **RIGHT JOIN**: All rows from the right table, matching rows from the left.
    -   **FULL JOIN**: All rows from both tables, with matches where available.
    -   **SELF JOIN**: Joins a table with itself.
    -   **NON-EQUI JOIN**: Uses non-equality conditions (e.g., `A.column_1 < B.column_2`).
-   **Example**:
    ```sql
    SELECT classes.class_name
    FROM Classes LEFT JOIN Students ON classes.id = students.class_id
    WHERE students.id IS NULL;
    ```
    _Explanation_: Finds classes with no students.

### SQL Views

**Views** are virtual tables based on a query, acting like permanent CTEs:

-   **Create View**:
    ```sql
    CREATE VIEW StudentInfo AS
    SELECT student_id, first_name, last_name, enrolled
    FROM Students
    WHERE enrolled = 1;
    ```
-   **Update View**:
    ```sql
    CREATE OR REPLACE VIEW StudentInfo AS
    SELECT student_id, first_name, last_name, class, enrolled
    FROM Students
    WHERE enrolled = 1;
    ```
-   **Drop View**:
    ```sql
    DROP VIEW StudentInfo;
    ```
-   **Benefits**: Simplifies queries, enhances security by limiting data access, ensures consistency.
-   **Limitations**: Slower for complex queries, read-only, dependent on underlying tables.

### SQL Indexes

**Indexes** speed up data retrieval but slow down modifications:

-   **Clustered Index**: Sorts table data physically (one per table).
    ```sql
    CREATE CLUSTERED INDEX idx_name ON table_name (column1, column2);
    ```
-   **Non-Clustered Index**: Uses pointers, allows multiple indexes.
    ```sql
    CREATE NONCLUSTERED INDEX idx_name ON table_name (column1, column2);
    ```

### Resources

-   [SQL Aggregate Functions](https://mode.com/sql-tutorial/sql-aggregate-functions/)
-   [SQL Window Functions](https://mode.com/sql-tutorial/sql-window-functions/)
-   [SQL NULL Values](https://www.w3schools.com/sql/sql_null_values.asp)
-   [Star Schema Diagram](https://en.wikipedia.org/wiki/Star_schema#/media/File:Star-schema.png)

---

## Week 3: Database Architecture

### What is Database Architecture?

**Database architecture** refers to the tools, technologies, and design choices used to store, manage, and access data. It’s like planning a house: you decide the layout based on needs like size, speed, and reliability.

### Factors Affecting Architecture

-   **Data Size**: How much data will you store?
-   **Data Type**: Structured (tables) or unstructured (documents)?
-   **Performance**: How fast do queries need to run?
-   **Scalability**: Can the database grow with demand?
-   **Reliability**: How much downtime is acceptable?
-   **Concurrency**: How many users access the database at once?

### Database Architecture Tiers

Think of tiers like floors in a building - each floor has a specific purpose and they work together:

-   **Single-Tier**: Like a one-room apartment - everything (app and data) on one machine.

    -   **Example**: A simple desktop app with a local database file
    -   **Pros**: Simple, fast for small use
    -   **Cons**: Hard to share, doesn't scale well

-   **Two-Tier**: Like a house with a basement - App on client, database on server.

    -   **Example**: A company app on your computer connecting to a shared database server
    -   **Pros**: Better than single-tier, can share data
    -   **Cons**: Gets slow with many users

-   **Three-Tier**: Like a modern office building - Separates UI, application logic, and data for scalability.
    -   **Example**: A web application (like online banking)
    -   **Floor 1 (Presentation)**: What you see (website, mobile app)
    -   **Floor 2 (Application)**: Business logic (processing your requests)
    -   **Floor 3 (Data)**: Database storage
    -   **Pros**: Very scalable, secure, maintainable
    -   **Cons**: More complex to set up
    -   **External Schema (User View)**: What users see, customized by access level.
    -   **Conceptual Schema**: Logical view of tables, relationships, and constraints.
    -   **Internal Schema**: Physical storage details (e.g., data blocks, indexes).
    -   **Learn More**: [Three-Level Schema Architecture](https://www.tutorialspoint.com/explain-the-three-level-schema-architecture-in-dbms)

### Benefits of Three-Tier Architecture

-   **Scalability**: Scale each layer independently.
-   **Maintainability**: Update one layer without affecting others.
-   **Security**: Apply different security measures per layer.
-   **Flexibility**: Switch technologies easily.
-   **Performance**: Optimize each layer for its task.

### SMP vs. MPP Architecture

-   **SMP (Symmetric Multiprocessing)**:
    -   Processors share one memory pool.
    -   Easy to program, scalable by adding processors.
-   **MPP (Massively Parallel Processing)**:
    -   Each processor has its own memory, connected via a network.
    -   Highly scalable, suited for big data (e.g., Google BigQuery, Amazon Redshift).

### Bronze, Silver, Gold Layers

In **data warehouses**, data is organized into layers:

-   **Bronze (Raw)**: Unprocessed data, minimally cleaned, for engineers.
-   **Silver (Cleansed)**: Cleaned and normalized data for analysis.
-   **Gold (Consumption)**: Optimized, business-ready data for end-users.

### Data Warehouse vs. Operational Database

-   **Data Warehouse**:
    -   For analytics and reporting.
    -   Denormalized schemas (Star/Snowflake).
    -   Complex queries, historical data.
-   **Operational Database**:
    -   For daily transactions (OLTP).
    -   Normalized schemas, real-time updates.

### Data Structures

-   **Structured**: Organized in tables (e.g., MySQL).
-   **Semi-Structured**: Flexible with tags (e.g., JSON in MongoDB).
-   **Unstructured**: No fixed format (e.g., files in Amazon S3).

---

## Week 4: SQL Wrap-Up

### Set Operations

Combine results from multiple queries:

-   **UNION**: Merges unique rows from two queries.
    ```sql
    SELECT emp_position FROM Employees
    UNION
    SELECT contractor_position FROM Contractors;
    ```
-   **EXCEPT (MINUS)**: Returns rows in the first query not in the second.
    ```sql
    SELECT emp_position FROM Employees
    EXCEPT
    SELECT contractor_position FROM Contractors;
    ```
-   **INTERSECT**: Returns common rows.
    ```sql
    SELECT emp_position FROM Employees
    INTERSECT
    SELECT contractor_position FROM Contractors;
    ```

### ACID Properties

**ACID** ensures reliable transactions:

-   **Atomicity**: Transactions complete fully or not at all (e.g., a bank transfer either happens or doesn’t).
-   **Consistency**: Ensures data follows rules (e.g., no negative balances).
-   **Isolation**: Transactions don’t interfere (e.g., one user’s transfer doesn’t affect another’s balance check).
-   **Durability**: Committed transactions are saved, even after crashes.

### Normalization

**Normalization** organizes data to reduce redundancy and ensure integrity:

-   **1NF (First Normal Form)**: No repeating groups, atomic values.
-   **2NF**: 1NF + non-key attributes depend on the entire primary key.
-   **3NF**: 2NF + no non-key attributes depend on other non-key attributes.
-   **BCNF**: A stricter version of 3NF.
-   **Example**: Split a table with customer, sales, and book data into separate tables to avoid duplication.

### Referential Integrity

Ensures relationships between tables stay consistent (e.g., foreign keys match primary keys). RDBMS enforces this with constraints, preventing invalid data or deletions that break links.

### Data Governance

**Data governance** manages data quality, security, and usability:

-   **Stewardship**: Assign stewards to maintain data quality and security.
-   **Management**: Handle data collection, storage, and access.
-   **Security**: Protect data with encryption, access controls, and compliance with laws.

### ETL vs. ELT

-   **ETL (Extract, Transform, Load)**: Transform data before loading into a warehouse. Suited for complex transformations.
-   **ELT (Extract, Load, Transform)**: Load raw data, then transform in the warehouse. Faster for large datasets.
-   **Factors**: Technology, data volume, transformation complexity, latency, and cost.

### Incremental Load

Loads only new or updated data:

-   **Timestamp**: Use `createdAt` or `updatedAt` to track changes.
-   **Change Tracking**: Logs inserts, updates, deletes.
-   **Change Data Capture (CDC)**: Tracks actual data changes.

### Upsert Logic

**Upsert** (Update or Insert):

-   Inserts new records or updates existing ones.
-   Example (PostgreSQL):
    ```sql
    INSERT INTO Students (id, name) VALUES (1, 'John')
    ON CONFLICT (id) DO UPDATE SET name = EXCLUDED.name;
    ```

### Resources

-   [Database Normalization](https://www.databasestar.com/database-normalization/)
-   [Google: Data Governance](https://cloud.google.com/learn/what-is-data-governance)
-   [AWS: Data Governance](https://aws.amazon.com/what-is/data-governance/)

---

## Week 5: Conceptual and Logical Modeling

### Entity-Relationship Model (ER Model)

An **ER Model** is a blueprint for designing a database:

-   **Entities**: Objects like `Students` or `Courses`.
-   **Attributes**: Properties (e.g., `Student_ID`, `Name`).
-   **Relationships**: Connections (e.g., one instructor teaches many courses).
-   **Cardinality**: How many instances relate (e.g., one-to-many).
-   **Ordinality**: Minimum relationships (e.g., a course must have at least one instructor).
-   **Keys**: Primary (unique identifier), Foreign (links tables).
-   **Composite Attributes**: Can be split (e.g., `Full Name` → `First Name`, `Last Name`).
-   **Derived Attributes**: Calculated (e.g., `Age` from `Date of Birth`).

### ERD Types

-   **Conceptual ERD**: High-level, no data types, focuses on entities and relationships.
-   **Logical ERD**: Adds column types, primary/foreign keys, and normalization.
-   **Physical ERD**: Final blueprint, specific to the DBMS (e.g., PostgreSQL’s `createdAt` fields).

### External Tables

**External tables** point to data outside the database (e.g., CSV files, Amazon S3):

-   **Pros**: No data duplication, cost-effective, supports varied formats.
-   **Cons**: Slower performance, limited features, security challenges.
-   **PostgreSQL Example**:
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
-   **S3 Example**: Use `s3_fdw` to connect to Amazon S3 (requires third-party module).
-   **Security Considerations**: Authentication, access control, data validation, encryption, and compliance with laws (e.g., data sovereignty for medical data).

---

## Week 6: Query Optimization and Cloud Administration

### Partitioning Tables

**Partitioning** splits a large table into smaller pieces for better performance:

-   **Types**:
    -   **Range**: By value ranges (e.g., sales by year).
    -   **List**: By specific values (e.g., by country).
    -   **Hash**: Uses a hash function to distribute data evenly.
    -   **Composite**: Combines multiple types.
-   **Benefits**: Faster queries, easier maintenance, scalability.

### Hash Functions

A **hash function** converts data into a fixed-size value (hash) for:

-   **Data Retrieval**: Fast lookups in hash tables.
-   **Cryptography**: Ensuring data integrity.
-   **Load Balancing**: Distributing data across servers.
-   **Properties**: Uniform, deterministic, fast, resistant to reverse-engineering.

### Cloud Database Security and Privacy

-   **Authentication**: Use usernames, MFA, or RBAC (e.g., AWS IAM).
-   **Encryption**: In-transit (SSL/TLS) and at-rest (AWS KMS).
-   **Auditing**: Log activities with AWS CloudTrail, monitor with CloudWatch.
-   **Firewall/Network**: Use Security Groups, VPCs for isolation.
-   **Data Masking/Anonymization**: Protect sensitive data.
-   **Backups**: Regular snapshots, Multi-AZ for recovery.
-   **Privacy**: Classify data, ensure compliance (e.g., GDPR), manage data sovereignty.

### Cloud Database Recovery

Protects against:

-   Hardware/software failures, human errors, natural disasters, cyberattacks.
-   **Recovery Types**:
    -   **Backup/Restore**: Regular backups for recovery.
    -   **Point-in-Time Recovery**: Restore to a specific moment.
    -   **Failover**: Switch to a standby database.
    -   **Replication**: Keep real-time copies.
-   **Objectives**:
    -   **RPO**: How much data loss is acceptable?
    -   **RTO**: How quickly must recovery happen?
-   **Steps**: Plan, implement, test, monitor, update.

### Cloud Database Auto-Scaling

**Auto-scaling** adjusts resources dynamically:

-   **Types**:
    -   **Horizontal**: Add more instances (scaling out).
    -   **Vertical**: Increase instance power (scaling up).
    -   **Read/Write**: Scale reads with replicas, writes with stronger nodes.
    -   **Scheduled/Dynamic/Predictive**: Based on schedules, metrics, or predictions.
-   **Pros**: Cost-efficient, reliable, high performance.
-   **Cons**: Latency, cost monitoring, consistency challenges.

### Cloud Database Mirroring

**Mirroring** keeps real-time database copies:

-   **Components**: Principal server (main), mirror server (copy), optional witness.
-   **Types**:
    -   **Synchronous**: Ensures data consistency, may add latency.
    -   **Asynchronous**: Faster, with slight data lag.
-   **Pros**: High availability, data protection, load balancing.
-   **Cons**: Latency, cost, complexity.

### Failover Clusters

**Failover clusters** ensure availability by switching to standby nodes:

-   **Components**: Nodes, shared storage, cluster software, networking.
-   **Types**: Active/Passive, Active/Active, N+1.
-   **Pros**: High availability, scalability.
-   **Cons**: Complex, costly, data consistency challenges.

---

## Week 8: Introduction to Amazon Cloud

### Amazon Web Services (AWS)

**AWS**, launched in 2006, is a cloud platform offering computing, storage, networking, analytics, and more. Used by companies like Airbnb and Slack, it’s compliant with HIPAA, GDPR, and PIPEDA.

### AWS Advantages

-   **Scalability**: Adjust resources based on demand.
-   **Cost-Effective**: Pay only for what you use.
-   **Flexibility**: Supports many languages and platforms.
-   **Global Reach**: Data centers worldwide.
-   **Community**: Large developer ecosystem.

### Use Cases

-   Web hosting, big data analytics, backups, IoT, software development.

### Amazon RDS

**RDS** is a managed relational database service supporting MySQL, PostgreSQL, SQL Server, and more:

-   **Features**:
    -   **Automated Backups**: Daily snapshots stored in S3.
    -   **Read Replicas**: Offload read traffic.
    -   **Multi-AZ**: Ensures availability with failover.
    -   **Security**: VPC, encryption, IAM.
    -   **Monitoring**: CloudWatch for metrics and alerts.
    -   **Scalability**: Vertical (upgrade instance) or horizontal (add replicas).
-   **Maintenance**: Configurable maintenance windows.

### Amazon VPC

**VPC** (Virtual Private Cloud) is a private network in AWS:

-   **Components**:
    -   **Subnets**: Public (internet-accessible) or private.
    -   **Internet Gateway**: Connects VPC to the internet.
    -   **Route Tables**: Direct network traffic.
    -   **Security Groups/NACLs**: Control traffic at instance/subnet levels.
    -   **VPC Peering**: Connects VPCs.
    -   **NAT/VPN/Direct Connect**: Manage external access.
-   **Features**: Isolation, customization, high availability.

### Subnet Groups

**DB Subnet Groups** in RDS ensure high availability:

-   Include subnets from multiple Availability Zones.
-   Support failover during outages.
-   Immutable VPC but flexible subnets.

### Private vs. Public VPCs

-   **Public VPC**: Subnets with internet access (e.g., for web servers).
-   **Private VPC**: No direct internet access, uses NAT or VPN (e.g., for databases).
-   **Hybrid**: Combines public and private subnets.

### VPC Security Best Practices

-   **Least Privilege**: Limit access.
-   **VPC Flow Logs**: Monitor traffic.
-   **NACLs/Security Groups**: Control traffic.
-   **AWS Config/GuardDuty**: Audit and detect threats.
-   **PrivateLink**: Secure service access.
-   **Encryption**: Protect data in transit and at rest.

### Resources

-   [AWS VPC Sharing](https://aws.amazon.com/blogs/architecture/using-vpc-sharing-for-a-cost-effective-multi-account-microservice-architecture/)
-   [AWS RDS Module](https://awsacademy.instructure.com/courses/3781/modules/items/462304)
-   [AWS VPC Module](https://awsacademy.instructure.com/courses/3781/modules/items/462265)

---

## Week 9: Introduction to NoSQL and MongoDB

### What is NoSQL?

**NoSQL** (Not Only SQL) databases are like flexible storage containers that can adapt to whatever you put in them, unlike traditional SQL databases which are like rigid filing cabinets with fixed compartments.

**Real-world analogy**:

-   **SQL Database**: Like a traditional office filing system with labeled folders, specific forms, and strict rules about what goes where
-   **NoSQL Database**: Like a modern storage unit where you can put boxes of any size and shape, and organize them however makes sense for your stuff

**Key advantages of NoSQL**:

-   **Scale**: Can spread data across many computers (like having multiple storage units)
-   **Schema-less**: No fixed structure - you can store different types of data without redesigning everything
-   **Performance**: Optimized for specific tasks (like finding things quickly vs. complex analysis)
-   **Flexibility**: Easy to change and adapt as your needs evolve

**When to use NoSQL**:

-   Social media posts (different formats, lots of users)
-   Product catalogs (varying product attributes)
-   Real-time analytics (need speed over complex relationships)
-   Mobile apps (need to work offline and sync later)

### Types of NoSQL Databases

Think of these as different types of storage solutions for different needs:

**1. Document Databases** (like MongoDB)

-   **Analogy**: Like storing complete files in folders, where each file can have different contents
-   **What it stores**: JSON-like documents (think of them as digital forms that can have different fields)
-   **Best for**: Product catalogs, user profiles, content management
-   **Example**: Storing customer information where some customers have different fields (some have phone numbers, others don't)

**2. Key-Value Databases** (like Redis)

-   **Analogy**: Like a giant dictionary or phone book - you look up a name (key) to get information (value)
-   **What it stores**: Simple pairs: "customer123" → customer data
-   **Best for**: Caching (storing frequently accessed data), session management, shopping carts
-   **Example**: Storing user login sessions

**3. Column Databases** (like Cassandra)

-   **Analogy**: Like a spreadsheet where you can add columns dynamically and efficiently store sparse data
-   **What it stores**: Data organized by columns rather than rows
-   **Best for**: Time-series data, IoT sensor data, analytics
-   **Example**: Storing temperature readings from thousands of sensors over time

**4. Graph Databases** (like Neo4j)

-   **Analogy**: Like a social network map showing how people are connected
-   **What it stores**: Nodes (entities) and edges (relationships)
-   **Best for**: Social networks, recommendation engines, fraud detection
-   **Example**: "Alice is friends with Bob, who works at Company X, which is located in City Y"

### NoSQL Data Example

```json
{
	"id": "1",
	"username": "JohnDoe",
	"email": "john.doe@email.com",
	"password": "2bgh54h3b124b13b1h3b12h4"
}
```

### SQL vs NoSQL: When to Use What?

**Choose SQL (Relational) when you need**:

-   **Strict data consistency** (like banking - every transaction must be perfect)
-   **Complex relationships** between data (like a school system with students, courses, teachers, grades all connected)
-   **Well-defined structure** that won't change much
-   **ACID compliance** (transactions that must be 100% reliable)
-   **Examples**: Banking systems, inventory management, payroll systems

**Choose NoSQL when you need**:

-   **Flexibility** to change data structure frequently
-   **Massive scale** (millions of users, huge amounts of data)
-   **Speed** over perfect consistency
-   **Different types of data** in the same system
-   **Examples**: Social media platforms, content management, real-time analytics, mobile apps

### BASE Properties

NoSQL often uses **BASE** instead of ACID (think of it as being more relaxed about perfection in exchange for speed and flexibility):

-   **Basically Available**: System stays accessible even if some parts fail (like a website that still works even if one server goes down)
-   **Soft State**: Data might be in transition and changing (like social media feeds that update gradually)
-   **Eventually Consistent**: Data becomes consistent over time, but might be slightly different across locations temporarily (like how a viral post might take a few seconds to appear on all users' feeds)

**Real-world example**: When you post on social media, your friends might see it at slightly different times, but eventually everyone sees the same post. This is "eventual consistency" - good enough for social media, but not acceptable for bank transfers!

### ACID vs. BASE

-   **ACID**: Prioritizes consistency (e.g., banking).
-   **BASE**: Prioritizes availability (e.g., social media).
-   **Behavior**: ACID rolls back on failure; BASE continues with possible outdated data.

### NoSQL vs. RDBMS

-   **NoSQL**: Dynamic schema, no standard query language, BASE.
-   **RDBMS**: Fixed schema, SQL, ACID.

### MongoDB Overview

**MongoDB** is a document-based NoSQL database:

-   **Document-Based**: Stores data in BSON (Binary JSON).
-   **Schema-less**: Flexible document structures.
-   **Scalability**: Horizontal scaling across servers.
-   **Speed**: Fast reads/writes by storing related data together.

### MongoDB Special Data Types

-   **ObjectId**: Unique document identifier.
-   **ISODate**: Stores dates (e.g., `ISODate("2023-08-17T00:00:00Z")`).
-   **Timestamp**: Non-real-world time tracking.

### MongoDB CRUD Operations

Using MongoDB’s Node.js driver:

-   **Create**:
    ```javascript
    db.collection("students").insertOne({ name: "John Doe" });
    db.collection("students").insertMany([{ name: "John Doe" }, { name: "Jane Smith" }]);
    ```
-   **Read**:
    ```javascript
    db.collection("students").find({}); // All records
    db.collection("students").findOne({ name: "John Doe" }); // One record
    db.collection("students").find({ name: /^John/ }); // Names starting with 'John'
    ```
-   **Update**:
    ```javascript
    db.collection("students").updateOne({ name: "John Doe" }, { $set: { grade: 12 } }); // Updates one record
    db.collection("students").updateMany({ name: /^John/ }, { $set: { status: "graduated" } }); // Updates multiple
    ```
-   **Delete**:
    ```javascript
    db.collection("students").deleteOne({ name: "John Doe" });
    db.collection("students").deleteMany({ status: "graduated" });
    ```

### MongoDB Joins

Use `$lookup` to join collections:

```javascript
db.students.aggregate([
	{
		$lookup: {
			from: "grades",
			localField: "id",
			foreignField: "student_id",
			as: "studentGrades",
		},
	},
]);
```

_Explanation_: Joins `students` with `grades` using `id` and `student_id`.

### MongoDB Array Operations

-   **Insert Array**:
    ```javascript
    db.students.insertOne({
    	name: "John Doe",
    	subjects: ["English", "Math"],
    });
    ```
-   **Add to Array**:
    ```javascript
    db.students.updateOne({ name: "John Doe" }, { $push: { subjects: "French" } });
    db.students.updateOne({ name: "John Doe" }, { $push: { subjects: { $each: ["French", "Physics"] } } });
    ```
-   **Remove from Array**:
    ```javascript
    db.students.updateOne({ name: "John Doe" }, { $pull: { subjects: "French" } });
    db.students.updateMany({ name: "John Doe" }, { $pull: { scores: { $lt: 50 } } }); // Removes scores < 50
    ```

### MongoDB Atlas

**MongoDB Atlas** is a managed cloud service for MongoDB, supporting AWS, Azure, and Google Cloud. Ideal for Lab 5.

### Resources

-   [MongoDB Atlas Registration](https://www.mongodb.com/cloud/atlas/register)
-   [MongoDB Atlas Tutorial](https://www.mongodb.com/basics/mongodb-atlas-tutorial)

---

## Week 10: Introduction to DynamoDB

### What is DynamoDB?

**DynamoDB** is AWS’s managed NoSQL database, designed for speed and scalability:

-   Handles any amount of data and traffic.
-   Optimized for low-latency, high-throughput applications.

### Key Features

-   **Managed Service**: AWS handles setup, patching, and backups.
-   **Scalability**: Auto-scales tables without downtime.
-   **High Availability**: Replicates data across multiple Availability Zones.
-   **Fast Performance**: Single-digit millisecond latency.
-   **Flexibility**: Supports key-value and document models.
-   **Data Types**: String, number, binary, Boolean, lists, maps, sets.
-   **Global Tables**: Replicates data across regions.
-   **Serverless**: Pay only for used resources.
-   **ACID Transactions**: Ensures reliable complex operations.
-   **Event-Driven**: Integrates with AWS Lambda for real-time actions.

### Core Components

-   **Tables**: Store data.
-   **Items**: Rows in a table.
-   **Attributes**: Columns in an item.
-   **Primary Key**: Unique identifier (partition key or partition + sort key).
-   **Indexes**: Secondary indexes for complex queries.

### Integrations

-   **AWS Services**: Lambda, API Gateway, S3, CloudFormation.
-   **External**: Elasticsearch, relational databases, third-party tools.

### Access Control

-   **IAM**: Manages permissions via policies.
-   **Resource-Based Policies**: Control access to DynamoDB resources.
-   **Attribute-Based**: Restrict access to specific attributes.
-   **VPC Endpoints**: Keep traffic within a VPC.

### Resources

-   [DynamoDB Labs](https://amazon-dynamodb-labs.workshop.aws/game-player-data/plan-model/step2.html)

---

## Week 11: Applications of Machine Learning

### Physical Denormalization

**Normalization** reduces redundancy but can slow queries due to joins. **Denormalization** adds redundant data to speed up queries:

-   **Example**: Instead of joining `Orders` and `Products` tables, store product names in `Orders` to avoid joins, trading redundancy for speed.
-   **Trade-offs**: Faster queries but more storage and potential inconsistency.

### Query Execution

Steps in running a SQL query:

1. **Parsing**: Check syntax.
2. **Optimization**: Choose the fastest plan using indexes and data size.
3. **Execution**: Run the plan (e.g., scan tables, join data).
4. **Presentation**: Format and return results.
   Denormalization reduces joins, speeding up execution.

### Distributed Architecture

**Distributed architecture** splits tasks across multiple computers:

-   **Scalability**: Add machines to handle more load.
-   **Fault Tolerance**: System works if one node fails.
-   **Latency**: Place resources closer to users.
-   **Concurrent Processing**: Multiple nodes process tasks simultaneously.
-   **Types**:
    -   **Client-Server**: Clients request from a central server.
    -   **Three-Tier**: Adds a middle tier for logic.
    -   **Peer-to-Peer**: Nodes act as both clients and servers.
    -   **Master-Slave**: Master directs slave nodes.
    -   **Microservices**: Independent services communicate.
    -   **Grid Computing**: Nodes solve large problems.
    -   **Lambda/Kappa**: For big data processing.
    -   **Blockchain**: Distributed ledger with consensus.

### Challenges

-   **Data Consistency**: Ensuring all nodes have the same data.
-   **Network Partition**: Handling network failures.
-   **Security**: Protecting multiple nodes.
-   **Resource Management**: Allocating tasks efficiently.

### Machine Learning in Databases

**Machine learning (ML)** enhances databases by:

-   **Handling Data Volume**: Automates analysis of large datasets.
-   **Real-Time Analytics**: Speeds up decision-making.
-   **Complex Queries**: Optimizes joins and subqueries.
-   **Data Quality**: Cleans dirty or missing data.

### ML Applications

-   **Query Optimization**:
    -   Predicts best join order or index usage.
    -   Optimizes caching based on usage patterns.
-   **Data Compression**:
    -   Recognizes patterns for efficient compression.
    -   Chooses lossy vs. lossless compression.
-   **Data Sharding**:
    -   Analyzes query patterns to minimize cross-shard queries.
    -   Balances shards to avoid bottlenecks.
-   **Data Partitioning**:
    -   Predicts load to optimize partitioning.
    -   Clusters data for faster access.

### Google BigQuery ML

Integrates ML into databases for query optimization and analytics.

### Future of ML in Databases

-   **In-Database ML**: Run models within the database.
-   **Distributed ML**: Scale ML across nodes.
-   **Adaptive Optimization**: Continuously improve queries.
-   **Security**: Detect threats in real-time.
-   **Explainable AI**: Transparent ML models.

### Resources

-   [BigQuery ML](https://cloud.google.com/bigquery/docs/introduction)
-   [Bit-Swap ML](https://bair.berkeley.edu/blog/2019/09/19/bit-swap/)

---

## This enhanced markdown file organizes the course content into clear sections, simplifies technical terms, and adds explanations to make concepts accessible for beginners while retaining all original content.

--

## Summary: Your Database Journey

Congratulations! You've learned about the fundamental concepts of databases. Here's a quick recap of your journey:

### Week 1-2: The Basics

-   **Databases** are organized systems for storing and retrieving data
-   **SQL** is the language for talking to relational databases
-   **Basic operations** (CRUD): Create, Read, Update, Delete data
-   **Tables, rows, and columns** are the building blocks of relational databases

### Week 3-4: Getting More Advanced

-   **Database architecture** is like city planning for data
-   **Normalization** reduces data redundancy and improves integrity
-   **Joins** connect related data across multiple tables
-   **Aggregate functions** summarize data (count, sum, average)

### Week 5-6: Design and Optimization

-   **ER models** help design database structure before building
-   **Indexes** speed up data retrieval (like a book's index)
-   **Query optimization** makes databases run faster
-   **Cloud databases** offer scalability and managed services

### Week 8-9: Modern Solutions

-   **AWS** provides cloud-based database services
-   **NoSQL** offers flexibility for modern applications
-   **Different database types** serve different purposes
-   **Choosing the right tool** depends on your specific needs

### Key Takeaways for Beginners

**1. Start Simple**: Begin with basic SQL queries and gradually work up to complex operations.

**2. Think in Real-World Terms**:

-   Tables = Spreadsheets
-   Databases = Filing systems
-   Queries = Questions you ask your data
-   Relationships = How different pieces of information connect

**3. Practice Makes Perfect**: The best way to learn databases is by doing. Try creating simple databases for things you know (like a personal movie collection or recipe database).

**4. Choose the Right Tool**:

-   Need strict consistency and complex relationships? → SQL databases
-   Need flexibility and massive scale? → NoSQL databases
-   Need managed cloud services? → AWS RDS or DynamoDB

**5. Security Matters**: Always consider who can access your data and how to protect it.

### Next Steps

-   Practice with real databases using tools like PostgreSQL or MongoDB
-   Try cloud services like AWS RDS for hands-on experience
-   Build a small project that interests you
-   Join database communities and forums to learn from others

Remember: Every expert was once a beginner. Take your time, practice regularly, and don't be afraid to experiment. Databases are powerful tools that can help you organize and understand data in amazing ways!
