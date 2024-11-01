# 2. Manual File System

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

# 3. Introduction to DBMS (Database Management System)

## Table of Contents
- [What is DBMS?](#what-is-dbms)
- [Key Features of DBMS](#key-features-of-dbms)
- [Types of DBMS](#types-of-dbms)
  - [Subtypes of DBMS](#subtypes-of-dbms)
- [Database Languages](#database-languages)
  - [Data Definition Language (DDL)](#data-definition-language-ddl)
  - [Data Manipulation Language (DML)](#data-manipulation-language-dml)
  - [Data Control Language (DCL)](#data-control-language-dcl)
  - [Transactional Control Language (TCL)](#transactional-control-language-tcl)
  - [Data Query Language (DQL)](#data-query-language-dql)
- [Paradigm Shift from File System to DBMS](#paradigm-shift-from-file-system-to-dbms)
- [Advantages of DBMS](#advantages-of-dbms)
- [Disadvantages of DBMS](#disadvantages-of-dbms)
- [Applications of DBMS](#applications-of-dbms)
- [Conclusion](#conclusion)

A database is a collection of interrelated data that helps in the efficient retrieval, insertion, and deletion of data from the database and organizes the data in the form of tables, views, schemas, reports, etc. For example, a university database organizes the data about students, faculty, admin staff, etc., which helps in the efficient retrieval, insertion, and deletion of data from it.

## What is DBMS?
A Database Management System (DBMS) is a software system designed to manage and organize data in a structured manner. It allows users to create, modify, and query a database, as well as manage the security and access controls for that database. A DBMS provides an environment to store and retrieve data conveniently and efficiently.

## Key Features of DBMS
- **Data Modeling**: A DBMS provides tools for creating and modifying data models, defining the structure and relationships of the data in a database.
- **Data Storage and Retrieval**: A DBMS is responsible for storing and retrieving data from the database and can provide various methods for searching and querying the data.
- **Concurrency Control**: A DBMS provides mechanisms for controlling concurrent access to the database, ensuring that multiple users can access the data without conflicting with each other.
- **Data Integrity and Security**: A DBMS enforces data integrity and security constraints, such as constraints on data values and access controls restricting who can access the data.
- **Backup and Recovery**: A DBMS provides mechanisms for backing up and recovering data in the event of a system failure.

## Types of DBMS
DBMS can be classified into two main types:
- **Relational Database Management System (RDBMS)**: Data is organized in tables, each having a set of rows and columns. The data is related through primary and foreign keys.
- **NoSQL**: Data is organized in key-value pairs, documents, graphs, or column-based formats, designed to handle large-scale, high-performance scenarios.

### Subtypes of DBMS
- **Relational Database Management System (RDBMS)**: Uses SQL (Structured Query Language) to query and manipulate data organized into tables.
- **NoSQL DBMS**: Designed for high-performance scenarios and large-scale data, storing data in various non-relational formats.
- **Object-Oriented DBMS (OODBMS)**: Stores data as objects, allowing for complex data representations and relationships.

## Database Languages
### Data Definition Language (DDL)
DDL deals with database schemas and descriptions, defining how the data should reside in the database. Common commands include:
- `CREATE`: To create a database and its objects (tables, indexes, views, stored procedures, functions, triggers).
- `ALTER`: Alters the structure of an existing database.
- `DROP`: Deletes objects from the database.
- `TRUNCATE`: Removes all records from a table and deletes the allocated spaces.
- `COMMENT`: Adds comments to the data dictionary.
- `RENAME`: Renames an object.

### Data Manipulation Language (DML)
DML handles data manipulation and includes common SQL statements such as:
- `SELECT`: Retrieves data from a database.
- `INSERT`: Inserts data into a table.
- `UPDATE`: Updates existing data within a table.
- `DELETE`: Deletes all records from a database table.
- `MERGE`: Performs UPSERT operation (insert or update).
- `CALL`: Calls a PL/SQL or Java subprogram.
- `EXPLAIN PLAN`: Provides interpretation of the data access path.
- `LOCK TABLE`: Manages concurrency control.

### Data Control Language (DCL)
DCL acts as an access specifier to the database, granting and revoking permissions to users. Commands include:
- `GRANT`: Grants permissions for running DML commands.
- `REVOKE`: Revokes permissions for running DML commands.

### Transactional Control Language (TCL)
TCL manages transactional data. Some commands include:
- `ROLLBACK`: Cancels or undoes changes made in the database.
- `COMMIT`: Applies or saves changes in the database.
- `SAVEPOINT`: Saves data on a temporary basis.

### Data Query Language (DQL)
DQL is a subset of DML, primarily focused on retrieving data. The most common command is:
- `SELECT`: Retrieves data from a table without modifying it.

## Paradigm Shift from File System to DBMS
A file system manages data using files on a hard disk, allowing users to create, delete, and update files. For instance, in a file-based University Management System, student data may be scattered across various departments, leading to issues such as:

- **Redundancy of Data**: Same data copied in many places; updating requires multiple changes.
- **Inconsistency of Data**: Multiple copies of the same data may not match, leading to inconsistencies.
- **Difficult Data Access**: Users must know exact file locations, making data retrieval cumbersome.
- **Unauthorized Access**: File systems can lead to unauthorized data access.
- **No Concurrent Access**: File systems do not allow multiple users to access the same data simultaneously.
- **No Backup and Recovery**: File systems lack mechanisms for data backup and recovery.

These issues prompted the shift from file systems to DBMS.

## Advantages of DBMS
- **Data Organization**: Allows structured data storage and retrieval.
- **Data Integrity**: Enforces data integrity constraints.
- **Concurrent Access**: Enables multiple users to access data simultaneously.
- **Data Security**: Manages data security and access controls.
- **Backup and Recovery**: Provides data backup and recovery options.
- **Data Sharing**: Allows collaborative data access among multiple users.

## Disadvantages of DBMS
- **Complexity**: Can be complex to set up and maintain.
- **Performance Overhead**: May add performance overhead in high-concurrency scenarios.
- **Scalability**: Can limit application scalability due to synchronization mechanisms.
- **Cost**: High costs associated with purchasing, maintaining, and upgrading DBMS.
- **Limited Use Cases**: Not all applications require a DBMS, and simpler solutions may suffice.

## Applications of DBMS
- **Enterprise Information**: Sales, accounting, human resources, manufacturing, online retailers.
- **Banking and Finance**: Customer details, accounts, loans, banking transactions.
- **University**: Student course enrollment information, grades, staff roles.
- **Airlines**: Reservation and scheduling systems.
- **Telecommunications**: Maintenance of prepaid and postpaid billing systems.

## Conclusion
A Database Management System (DBMS) is an essential tool for efficiently managing, organizing, and retrieving large volumes of data across various industries. Its ability to handle data securely, ensure integrity, support concurrent access, and provide backup and recovery options makes it indispensable for modern data-driven applications. While DBMSs come with complexities and costs, their benefits in terms of data management and security far outweigh the challenges, making them a crucial component in any data-centric environment.
