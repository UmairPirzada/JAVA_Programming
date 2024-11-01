# Data Management Overview

This document provides an overview of data management methods, starting from manual file systems to databases and DBMS. We’ll explore different database types and essential database languages.

---

## 1. Manual File System

A **manual file system** is a way of organizing and storing information physically, such as in cabinets, folders, or books. This system relies on people to store, retrieve, and manage data without the aid of computer software.

### Drawbacks of Manual File System
- **Time-consuming**: Locating and retrieving physical records is slow and requires manual effort.
- **Error-prone**: Increased chances of data entry errors and inconsistencies due to manual handling.
- **Limited accessibility**: Only one person can access a physical file at a time, reducing collaboration and efficiency.
- **Space requirements**: Physical files take up space in offices or storage rooms.
- **Security concerns**: Physical data can be easily accessed or removed, making security difficult.
- **Data loss risk**: Physical documents are susceptible to damage or loss from fire, water, or other mishaps.

---

## 2. File-Based System (Computerized)

A **file-based system** is a digital method of storing data in files that can be managed by an operating system or basic software. Data is usually organized in text, spreadsheets, or binary files, accessed sequentially or directly through indexing.

### Drawbacks of File-Based System
- **Data redundancy and inconsistency**: Duplication of data across multiple files can lead to inconsistency.
- **Complex data retrieval**: Accessing data across separate files can be challenging.
- **Lack of data integrity**: No centralized checks exist to ensure data accuracy across files.
- **Limited security**: Security controls in file-based systems are weak, risking unauthorized access.
- **Concurrency issues**: Limited support for multiple users accessing or modifying data simultaneously.
- **Lack of data independence**: Changes in data structure often require modification of application code.

---

## 3. Database and DBMS

A **database** is an organized collection of structured data stored electronically, designed for efficient access, retrieval, and management. 

A **Database Management System (DBMS)** is software that allows users to interact with the database, managing data storage, updates, and retrieval systematically. DBMS provides efficient and controlled data access, reduces redundancy, and improves security.

### Advantages of a DBMS
- **Data integrity**: DBMS ensures data consistency and accuracy through constraints and rules.
- **Improved security**: Provides access control and encryption options to secure sensitive data.
- **Efficient data access**: Indexing and query mechanisms improve data retrieval speed.
- **Data independence**: Separates data from applications, making it easier to change the database structure.
- **Concurrency control**: Allows multiple users to access data simultaneously without conflicts.

### Example: MySQL
**MySQL** is a popular open-source relational database management system (RDBMS) that uses Structured Query Language (SQL) for data management. MySQL is widely used for web applications due to its speed, reliability, and flexibility.

---

## 4. Database Types

### 1. Relational Database
- Stores data in tables (rows and columns) with relationships between them.
- **Examples**: MySQL, PostgreSQL, Oracle Database.

### 2. NoSQL Database
- Handles unstructured or semi-structured data and does not require a fixed schema.
- **Types**: Document-based, Key-Value, Column-family, and Graph.
- **Examples**: MongoDB (document), Redis (key-value), Cassandra (column-family).

### 3. Object-Oriented Database
- Stores data as objects, supporting inheritance, polymorphism, and encapsulation.
- **Examples**: ObjectDB, db4o.

### 4. Hierarchical Database
- Organizes data in a tree-like structure with a single root and child nodes.
- **Examples**: IBM IMS, Windows Registry.

### 5. Network Database
- Allows many-to-many relationships and a network structure for data.
- **Examples**: IDS (Integrated Data Store), CODASYL database.

### 6. Time-Series Database
- Optimized for time-stamped data, used for tracking changes over time.
- **Examples**: InfluxDB, TimescaleDB.

### 7. Graph Database
- Uses nodes and edges to represent and manage relationships between data.
- **Examples**: Neo4j, ArangoDB.

### 8. Cloud Database
- Runs on cloud infrastructure, providing scalability and flexibility.
- **Examples**: Amazon RDS, Google Cloud Firestore.

---

## 5. Database Languages

### 1. Data Definition Language (DDL)
Defines the structure and organization of the database.
- **Commands**: `CREATE`, `ALTER`, `DROP`, `TRUNCATE`
- **Example**:
  ```sql
  CREATE TABLE Students (ID INT, Name VARCHAR(50), Age INT);
  ```

### 2. Data Manipulation Language (DML)
Used to manipulate data within the database.
Commands: INSERT, UPDATE, DELETE, SELECT
Example:
```sql

INSERT INTO Students (ID, Name, Age) VALUES (1, 'John Doe', 20);
```
### 3. Data Control Language (DCL)
Manages permissions and access to the data in the database.
Commands: GRANT, REVOKE
Example:

```sql
GRANT SELECT ON Students TO User1;
```
### 4. Transaction Control Language (TCL)
Manages transactions within the database, ensuring data integrity.
Commands: COMMIT, ROLLBACK, SAVEPOINT
Example:

```sql
BEGIN;
INSERT INTO Students (ID, Name, Age) VALUES (2, 'Jane Doe', 22);
COMMIT;
```
Each language plays a critical role in enabling users to define the structure, manage permissions, manipulate data, and control database transactions.

