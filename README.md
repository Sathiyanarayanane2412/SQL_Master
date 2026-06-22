# SQL_Master

✅ 1. What is a Database (DB)?
A Database is an organized collection of data stored in a structured way so it can be easily accessed, managed, and updated.
🔹 Example:

Student records in a college (name, roll number, marks)
Bank account details
Employee data in a company

👉 In simple words:

A database is where data is stored.


✅ 2. What is DBMS (Database Management System)?
A DBMS is a software/tool used to create, manage, and interact with databases.
🔹 Examples of DBMS:

MySQL
PostgreSQL
Oracle
SQL Server

🔹 What DBMS does:

Stores data
Retrieves data
Updates data
Deletes data
Ensures security and consistency

👉 In simple words:

DBMS is the software that helps you work with the database.


✅ 3. Types of Databases
Databases are classified based on how data is stored and managed.

🔹 1. Relational Database (RDBMS)

Data stored in tables (rows & columns)
Uses SQL (Structured Query Language)

✅ Examples:

MySQL
PostgreSQL
Oracle

✅ Use Case:

Banking systems
E-commerce websites

👉 Most commonly used type ✅

🔹 2. NoSQL Database

Stores unstructured or semi-structured data
No fixed table structure

✅ Types inside NoSQL:

Document-based (MongoDB)
Key-Value (Redis)
Column-based (Cassandra)
Graph (Neo4j)

✅ Use Case:

Big data applications
Real-time apps (chat, social media)


🔹 3. Object-Oriented Database

Stores data as objects (like Java classes)

✅ Example:

ObjectDB

✅ Use Case:

Complex applications using OOP


🔹 4. Hierarchical Database

Data stored in a tree-like structure (parent-child)

✅ Example:

IBM IMS

✅ Use Case:

Old systems (legacy systems)


🔹 5. Network Database

Data stored as a graph (many-to-many relationships)

✅ Use Case:

Telecom systems (earlier systems)

✅ Final Simple Summary

Database → Place where data is stored
DBMS → Tool to manage that data
RDBMS → Most commonly used database (tables + SQL)
NoSQL → Flexible data storage for modern apps

✅ Types of SQL Commands
SQL commands are mainly divided into 5 categories:

🔹 1. DDL (Data Definition Language)
👉 Used to define or modify database structure
✅ Commands:

CREATE → Create database/table
ALTER → Modify table structure
DROP → Delete table/database
TRUNCATE → Remove all data from table

✅ Example:
SQLCREATE TABLE student (    id INT,    name VARCHAR(50));Show more lines

🔹 2. DML (Data Manipulation Language)
👉 Used to insert, update, delete data
✅ Commands:

INSERT → Add data
UPDATE → Modify existing data
DELETE → Remove data

✅ Example:
SQLINSERT INTO student VALUES (1, 'John');UPDATE student SET name = 'Sam' WHERE id = 1;DELETE FROM student WHERE id = 1;``Show more lines

🔹 3. DQL (Data Query Language)
👉 Used to retrieve data from database
✅ Command:

SELECT

✅ Example:
SQLSELECT * FROM student;Show more lines
👉 Most frequently used SQL command ✅

🔹 4. DCL (Data Control Language)
👉 Used to control access/permissions
✅ Commands:

GRANT → Give permission
REVOKE → Remove permission

✅ Example:
SQLGRANT SELECT ON student TO user1;REVOKE SELECT ON student FROM user1;Show more lines

🔹 5. TCL (Transaction Control Language)
👉 Used to manage transactions
✅ Commands:

COMMIT → Save changes
ROLLBACK → Undo changes
SAVEPOINT → Set a point in transaction

✅ Example:
SQLBEGIN;
UPDATE student SET name = 'Raj' WHERE id = 1;ROLLBACK;
Show more lines

✅ Easy Way to Remember
👉 DDL → Design (structure)
👉 DML → Modify data
👉 DQL → Query data
👉 DCL → Control access
👉 TCL → Transaction safety
✅ Quick Summary Table
<img width="467" height="254" alt="image" src="https://github.com/user-attachments/assets/fa7ad956-c7d5-4e4e-8481-de6d672badaa" />

