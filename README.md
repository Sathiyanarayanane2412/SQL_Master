# SQL_Master
# 📘 DBMS & SQL – Interview Preparation Notes

This repository contains my structured notes for **Database and SQL concepts** for interview preparation.

---

# 🔹 1. What is a Database (DB)?

A **Database** is an organized collection of data stored in a structured way so it can be easily accessed, managed, and updated.

### ✅ Examples:
- Student records
- Banking systems
- Employee management systems

👉 **In simple words:**
A database is a place where data is stored.

---

# 🔹 2. What is DBMS (Database Management System)?

A **DBMS** is software used to create, manage, and manipulate databases.

### ✅ Examples:
- MySQL  
- PostgreSQL  
- Oracle  
- SQL Server  

### ✅ Functions:
- Store data  
- Retrieve data  
- Update and delete data  
- Maintain security  
- Ensure consistency  

👉 **In simple words:**
DBMS is a tool used to manage the database.

---

# 🔹 3. Types of Databases

## ✅ 1. Relational Database (RDBMS)
- Data stored in tables (rows & columns)
- Uses SQL

**Examples:** MySQL, PostgreSQL, Oracle  

👉 Most commonly used database ✅

---

## ✅ 2. NoSQL Database
- Stores unstructured or semi-structured data
- Flexible schema

### Types:
- Document → MongoDB  
- Key-Value → Redis  
- Column → Cassandra  
- Graph → Neo4j  

---

## ✅ 3. Hierarchical Database
- Tree-like structure (Parent → Child)

👉 Used in older systems

---

## ✅ 4. Network Database
- Graph structure (many-to-many relationships)

---

## ✅ 5. Object-Oriented Database
- Stores data as objects (like Java classes)

---

✅ Easy Way to Remember
👉 DDL → Design (structure)
👉 DML → Modify data
👉 DQL → Query data
👉 DCL → Control access
👉 TCL → Transaction safety
✅ Quick Summary Table
<img width="467" height="254" alt="image" src="https://github.com/user-attachments/assets/fa7ad956-c7d5-4e4e-8481-de6d672badaa" />

---

# 🚀 Interview Tip

✅ Focus heavily on:
- Joins  
- Group By & Having  
- Subqueries  
- Indexing  
- Transactions  

---
#Question with solution
# 🔹 Basic SQL & DBMS Interview Q&A

---

## ✅ 1. What is SQL?

SQL (Structured Query Language) is a programming language used to interact with databases.  
It is used to **store, retrieve, update, and delete data**.

---

## ✅ 2. What is a Database?

A **Database** is an organized collection of data stored in a structured format.

👉 Example:
- Student records
- Bank accounts
- Employee details

---

## ✅ 3. What is DBMS?

DBMS (Database Management System) is software used to **create, manage, and manipulate databases**.

👉 Examples:
- MySQL  
- PostgreSQL  
- Oracle  

👉 It helps in:
- Data storage  
- Data retrieval  
- Data security  

---

## ✅ 4. What is RDBMS?

RDBMS (Relational Database Management System) is a type of DBMS where data is stored in **tables (rows and columns)** and relationships are maintained between tables.

👉 Examples:
- MySQL  
- PostgreSQL  

---

## ✅ 5. Difference between DBMS and RDBMS?

| Feature | DBMS | RDBMS |
|--------|------|------|
| Structure | Stores data as files | Stores data in tables |
| Relationship | No relation support | Supports relationships |
| Normalization | Not applied | Applied |
| Examples | File system | MySQL, PostgreSQL |

---

## ✅ 6. What is a Table?

A **Table** is a structure in a database that stores data in **rows and columns**.

👉 Example:
A student table with columns: `id`, `name`, `age`

---

## ✅ 7. What is a Row and Column?

- **Row** → A single record in a table  
- **Column** → A field or attribute of data  

👉 Example:

| id | name | age |
|----|------|-----|
| 1  | John | 20  |

- Row → (1, John, 20)  
- Column → id / name / age  

---

## ✅ 8. What is a Primary Key?

A **Primary Key** uniquely identifies each record in a table.  
It cannot be **NULL or duplicate**.

```sql
CREATE TABLE student (
    id INT PRIMARY KEY,
    name VARCHAR(50)
);
```
## ✅ 9. What is a Foreign Key?

A **Foreign Key** is a column (or set of columns) used to create a relationship between two tables.  
It refers to the **Primary Key of another table**.

👉 Purpose:
- Maintains **data integrity**
- Links related data between tables

### ✅ Example:

```sql
CREATE TABLE student (
    id INT PRIMARY KEY,
    name VARCHAR(50)
);

CREATE TABLE orders (
    order_id INT,
    student_id INT,
    FOREIGN KEY (student_id) REFERENCES student(id)
);
```
## ✅ 10. What is a Unique Key?

A **Unique Key** is a constraint used to ensure that all values in a column (or combination of columns) are **unique (no duplicates allowed)**.

👉 Key Points:
- Prevents duplicate values  
- Allows **one NULL value** (in most databases)  
- A table can have **multiple UNIQUE keys**  

---

### ✅ Example:

```sql
CREATE TABLE student (
    id INT PRIMARY KEY,
    email VARCHAR(100) UNIQUE
);
```
## ✅ 9. What is GROUP BY?

`GROUP BY` is used to **group rows that have the same values** in one or more columns and perform **aggregate operations** on each group.

---

### 👉 Key Points:

- Groups rows based on column values  
- Used with aggregate functions:
  - `COUNT()`
  - `SUM()`
  - `AVG()`
  - `MIN()`
  - `MAX()`  
- Every column in `SELECT` must be:
  - Included in `GROUP BY`
  - OR used inside an aggregate function  
- Often used with `HAVING` to filter grouped results  
- Works after `WHERE` in query execution  

---

### ✅ Syntax:

```sql
SELECT column_name, AGG_FUNCTION(column_name)
FROM table_name
GROUP BY column_name;
```
### ✅ Example Table:

| id | name | dept | salary |
|----|------|------|--------|
| 1  | A    | IT   | 50000  |
| 2  | B    | HR   | 40000  |
| 3  | C    | IT   | 60000  |
| 4  | D    | HR   | 45000  |

##1. Count Employees per Department
```

SELECT dept, COUNT(*) AS total_employees
FROM employee
GROUP BY dept;
```
##2. Total Salary per Department
```

SELECT dept, SUM(salary) AS total_salary
FROM employee
GROUP BY dept
```
##3. Average Salary per Department
```

SELECT dept, AVG(salary) AS avg_salary
FROM employee
GROUP BY dept;
```
##4.Maximum Salary per Department
```

SELECT dept, MAX(salary) AS max_salary
FROM employee
GROUP BY dept;
```

## ✅ 🔹 5. GROUP BY with Multiple Columns

```sql
SELECT dept, salary, COUNT(*)
FROM employee
GROUP BY dept, salary;
```
---

# ⚖️ WHERE vs HAVING
```md
# ⚖️ WHERE vs HAVING

| Feature | WHERE | HAVING |
|--------|-------|--------|
| Filters | Rows | Groups |
| Used before GROUP BY | ✅ | ❌ |
| Used after GROUP BY | ❌ | ✅ |
| Supports aggregate functions | ❌ | ✅ |
```md
# 🔥 Author

**Sathiyanarayanan**  
Java Backend Developer Aspirant 🚀
