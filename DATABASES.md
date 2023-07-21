# DATABASES

## TABLE OF CONTENTS

- [General](#general)
  1. What is a Database (DB)?
  2. What is a Database Management System (DBMS)?
  3. What is a Relational Database Management System (RDBMS)?
  4. Mention different DBMS.
  5. Mention some RDBMS.
  6. What is SQL?
  7. Define the SQL subgroups.
  8. What is a Relational Model?
  9. What NoSQL?
  10. What is ACID?
  11. Mention different SQL Data types.
  12. What is Cardinality?
  13. Mention different relationship types in a "Relational model".

<a name="general" />

## General

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

1. DDL (Data defition language): It deals with database schemas and descriptions, of how the data should reside in the database. Some examples of different commands that conform this subgroup are: CREATE, ALTER, DROP, TRUNCATE, RENAME.
2. DML (Data manipulation language): It deals with data manipulation and includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE, etc., and it is used to store, modify, retrieve, delete and update data in a database.
3. DCL (Data control language): It includes commands such as GRANT and mostly concerned with rights, permissions and other controls of the database system.
4. TCL (Transaction control language): It deals with a transaction within a database. Some examples of different commands are: COMMIT, ROLLBACK.

### 8. What is a Relational Model?

It is a way of structuring data in a database, where information is organized into tables with rows and columns. Each table represents an entity, and the relationships between entities are defined through shared values across tables. This model allows for easy data retrieval, manipulation, and ensures data integrity.

### 9. What NoSQL ?

Answer

### 10. What is ACID?

Is a set of properties that you would like to apply when modifying a database.

1. Atomicity

It means that you can guarantee that all statements inside a transaction happens, if something fail, all statements inside a transaction are discarded.

2. Consistency

It means that your data will be consistent; none of the constraints you have on related data will ever be violated.

3. Isolation

Means that one transaction cannot read data from another transaction that is not yet completed. If two transactions are executing concurrently, each one will see the world as if they were executing sequentially, and if one needs to read data that is written by another, it will have to wait until the other is finished.

4. Durability

It is guaranteed that all of the changes have been recorded to a durable medium (ej: Hard drive), and the fact that the transaction has been completed is likewise recorded.

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

### 12. What is Cardinality?

It defines how many instances of one entity are related to instances of another entity.

### 13. Mention different relationship types of cardinality.

There are 3:

1. One to one
It means one entity in a table is related to just one entity in another table.
2. One to Many
It means one entity in a table is related to one or many entities in another table.
3. Many to Many
It means multiple entities in a table can be associated with more than one entity in another table.
