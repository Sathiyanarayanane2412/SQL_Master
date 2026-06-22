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
# 🔥 Top 100 SQL Interview Questions

## 🔹 Basic SQL Questions

1. What is SQL?
2. What is a database?
3. What is DBMS?
4. What is RDBMS?
5. Difference between DBMS and RDBMS?
6. What is a table?
7. What is a row and column?
8. What is a primary key?
9. What is a foreign key?
10. What is a unique key?
11. What is a composite key?
12. What is a candidate key?
13. What is normalization?
14. Types of normalization (1NF, 2NF, 3NF)?
15. What is denormalization?
16. What is NULL?
17. Difference between NULL and NOT NULL?
18. What is a constraint?
19. Types of constraints?
20. What is default constraint?

---

## 🔹 DDL & DML Questions

21. Difference between DELETE, TRUNCATE, and DROP?
22. What is ALTER command?
23. What is CREATE command?
24. What is INSERT command?
25. What is UPDATE command?
26. What is DELETE command?
27. Can we rollback DELETE?
28. Can we rollback TRUNCATE?
29. What is AUTO_INCREMENT?
30. What is schema?

---

## 🔹 SELECT Queries

31. What is SELECT statement?
32. Difference between SELECT * and SELECT columns?
33. What is WHERE clause?
34. What is ORDER BY?
35. What is GROUP BY?
36. What is HAVING?
37. Difference between WHERE and HAVING?
38. What is DISTINCT?
39. What is LIMIT?
40. What is alias in SQL?

---

## 🔹 Joins (Very Important)

41. What are joins?
42. Types of joins?
43. What is INNER JOIN?
44. What is LEFT JOIN?
45. What is RIGHT JOIN?
46. What is FULL JOIN?
47. What is CROSS JOIN?
48. Difference between INNER and LEFT JOIN?
49. What is SELF JOIN?
50. Real-time example of joins?

---

## 🔹 Aggregate Functions

51. What are aggregate functions?
52. COUNT vs SUM?
53. AVG function usage?
54. MAX and MIN?
55. Can aggregate functions use WHERE?
56. What is GROUP BY with aggregate?
57. What is HAVING with aggregate?
58. What happens if GROUP BY is not used?
59. Difference between COUNT(*) and COUNT(column)?
60. Aggregate functions with NULL values?

---

## 🔹 Subqueries

61. What is a subquery?
62. Types of subqueries?
63. What is correlated subquery?
64. Subquery vs JOIN?
65. What is EXISTS?
66. What is IN operator?
67. Difference between IN and EXISTS?
68. Nested subqueries?
69. Can subquery return multiple rows?
70. Performance of subqueries?

---

## 🔹 Indexing

71. What is an index?
72. Types of indexes?
73. Clustered vs Non-clustered index?
74. How index improves performance?
75. Disadvantages of index?
76. When not to use index?
77. Composite index?
78. Unique index?
79. Index vs primary key?
80. How to create index?

---

## 🔹 Transactions & TCL

81. What is a transaction?
82. Properties of transaction (ACID)?
83. What is COMMIT?
84. What is ROLLBACK?
85. What is SAVEPOINT?
86. What is isolation level?
87. Dirty read?
88. Non-repeatable read?
89. Phantom read?
90. How to handle transactions?

---

## 🔹 Advanced SQL

91. What is view?
92. Types of views?
93. What is materialized view?
94. What is stored procedure?
95. What is function in SQL?
96. Difference between procedure and function?
97. What is trigger?
98. Use case of triggers?
99. What is CTE (Common Table Expression)?
100. What is window function?

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
``

# 🔥 Author

**Sathiyanarayanan**  
Java Backend Developer Aspirant 🚀
