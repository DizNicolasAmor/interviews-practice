# DATABASES

## TABLE OF CONTENTS

- [BASIC](#basic)
  1. What is a Database (DB)?
  2. What is a Database Management System (DBMS)?
  3. What is a Relational Database Management System (RDBMS)?
  4. Mention different DBMS.
  5. Mention some RDBMS.
  6. What is SQL?
  7. Define the SQL subgroups.
  8. What is a Relational Model?
  9. What is NoSQL?
  10. What is ACID?
  11. Mention different SQL Data types.
- [Intermediate](#intermediate)
  12. What is Cardinality?
  13. Mention different relationship types of cardinality.
  14. What is database normalization?
  15. How would you optimize a slow-performing SQL query?
  16. What are the differences between a clustered and a non-clustered index?
  17. What's the purpose of the GROUP BY clause in SQL?
  18. How does the concept of a view work in databases?
  19. What is database denormalization?
  21. What are triggers in databases, and when would you use them?
  22. How do you handle concurrency issues in a database?
- [Advanced](#advanced)
  23. Discuss the CAP theorem and its implications for distributed databases.
  24. Explain the concept of sharding in database architecture.
  25. Discuss various types of NoSQL databases and their use cases.
  26. How does database indexing impact query performance?
  27. Explain the concept of a database transaction isolation level.
  28. Discuss ACID compliance in distributed databases.
  29. How would you approach database schema versioning and migration in a large-scale application?
  30. What are CTEs (Common Table Expressions), and how do they work in SQL?
  31. Explain the differences between horizontal and vertical scaling in databases.
  32. Discuss the role of database caching in optimizing performance.
  33. How would you design a database to handle a high-traffic, write-intensive application?

<a name="basic" />

## BASIC

### 1. What is a Database?

A database is an organized collection of data stored in a computer.

### 2. What is a Database Management System (DBMS)?

DBMS are specially designed software applications that interact with the user, other applications and the database itself to capture and analyze data. The general purpose of a Database Management System is allow the definition, creation, querying, update and administration of a database.

### 3. Mention different DBMS.

Some Database Management Systems are **MySQL**, **PostgreSQL**, **MariaDB**, **Microsoft SQL Server**, **Oracle**, **MongoDB**, **Apache Cassandra**, **Redis**, **Apache CouchDB**.

### 4. What is a Relational Database Management System (RDBMS)?

This term defines how data is stored in a Database Management System (DBMS). Since DBMS is a generic term, it does not contain information of how data should be exactly stored. It could be stored in files, graphs, key-value, relational tables, etc... In this case the data is stored using tables following the Relational Model.

### 5. Mention some RDBMS

Some RDBMS could be **MySQL**, **MariaDB**, **Microsoft SQL Server**, **PostgreSQL**.

### 6. What is SQL?

SQL refers to **Structured Query Language**. It is a standarized language mostly used by Relational Database Management Systems.

### 7. Define the SQL subgroups

SQL consists in 4 different subgroups that build the language itself.

1. **DDL (Data defition language)**: It deals with database schemas and descriptions, of how the data should reside in the database. Some examples of different commands that conform this subgroup are: `CREATE`, `ALTER`, `DROP`, `TRUNCATE`, `RENAME`.
2. **DML (Data manipulation language)**: It deals with data manipulation and includes most common SQL statements such `SELECT`, `INSERT`, `UPDATE`, `DELETE`, etc., and it is used to store, modify, retrieve, delete and update data in a database.
3. **DCL (Data control language)**: It includes commands such as GRANT and mostly concerned with rights, permissions and other controls of the database system.
4. **TCL (Transaction control language)**: It deals with a transaction within a database. Some examples of different commands are: `COMMIT`, `ROLLBACK`.

### 8. What is a Relational Model?

It is a way of structuring data in a database, where information is organized into tables with rows and columns. Each table represents an entity, and the relationships between entities are defined through shared values across tables. This model allows for easy data retrieval, manipulation, and ensures data integrity.

### 9. What is NoSQL?

NoSQL is a term for a category of databases that diverge from the traditional relational model. It stands for "Not Only SQL" or "Non-SQL," emphasizing the use of alternative data models, like document-oriented, key-value, column-family, or graph databases. NoSQL databases are designed for scalability, high performance, and flexibility in handling large volumes of unstructured or semi-structured data.

### 10. What is ACID?

Is a set of properties that you would like to apply when modifying a database.

1. **Atomicity**: it means that you can guarantee that all statements inside a transaction happens, if something fail, all statements inside a transaction are discarded.
2. **Consistency**: it means that your data will be consistent; none of the constraints you have on related data will ever be violated.
3. **Isolation**: it means that one transaction cannot read data from another transaction that is not yet completed. If two transactions are executing concurrently, each one will see the world as if they were executing sequentially, and if one needs to read data that is written by another, it will have to wait until the other is finished.
4. **Durability**: it is guaranteed that all of the changes have been recorded to a durable medium (ej: Hard drive), and the fact that the transaction has been completed is likewise recorded.

### 11. Mention different SQL Data types.

1. CHARACTER
2. VARCHAR
3. BOOLEAN
4. INTEGER
5. SMALLINT
6. BIGINT
7. DECIMAL
8. FLOAT
9. DATE
10. TIMESTAMP

<a name="intermediate" />

## INTERMEDIATE

### 12. What is Cardinality?

It defines how many instances of one entity are related to instances of another entity.

### 13. Mention different relationship types of cardinality.

There are 3:

1. **One to one:** it means one entity in a table is related to just one entity in another table.
2. **One to many:** it means one entity in a table is related to one or many entities in another table.
3. **Many to many:** it means multiple entities in a table can be associated with more than one entity in another table.

### 14. What is database normalization?

It is a process in database design that minimizes data redundancy (it avoids duplications) by structuring data logically across tables, reducing anomalies and improving organization.

It involves breaking down large tables into smaller, related tables and applying specific rules (normal forms) to structure data efficiently.

### 15. How would you optimize a slow-performing SQL query?

- Ensuring proper indexing.
- Minimizing the use of wildcards in WHERE clauses.
- Avoiding functions on indexed columns.
- Rewriting the query, breaking it into smaller steps, and analyzing execution plans to identify bottlenecks for improvement.

### 16. What are the differences between a clustered and a non-clustered index?

- **Clustered index**: determines the physical order of data in a table, allowing only one per table and directly impacting how data is stored.
- **Non-clustered indexes**: don't alter the physical order, instead creating a separate structure to optimize query speed, allowing multiple indexes per table.

### 17. What's the purpose of the GROUP BY clause in SQL?

It is used to aggregate data based on specific columns, allowing grouping of rows that share common values. It enables the application of aggregate functions like SUM, COUNT, AVG, etc., to perform calculations and generate summary results for each group within the dataset.

### 18. How does the concept of a view work in databases?

- It is a virtual table derived from one or multiple tables through a predefined query.
- It doesn't store data itself but presents a tailored perspective of the underlying tables.
- It simplifies complex queries.
- It enhances security by restricting access to specific columns or rows.
- It offers a consistent interface for users or applications to retrieve information.

### 19. What is database denormalization?

It involves intentionally introducing redundancy into a database by relaxing normalization rules. It aims to optimize query performance by reducing the number of joins needed to retrieve data.

### 21. What are triggers in databases, and when would you use them?

Triggers are special routines that automatically execute in response to certain events, like INSERT, UPDATE, or DELETE operations on a table. They're used to enforce business rules, maintain data integrity, log changes, or automate tasks.

### 22. How do you handle concurrency issues in a database?

complete
