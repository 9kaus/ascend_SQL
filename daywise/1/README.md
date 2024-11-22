## **Origin of the Word "Computer"** 🖥️

The word "Computer" is derived from the French word **"Computaire"**, which means **to compute** or **to calculate**.

---

## **Data Processing Flow** 🔄

### (Input) → (Processing) → (Output)

> **Data** ➔ **Computer** ➔ **Information**  
  *(Raw facts)* ➔ *(Processing)* ➔ *(Processed data)*



#### Example:

| **Input**    | **Processing**                           | **Output**                       |
|--------------|------------------------------------------|----------------------------------|
| 22021984     | Converting raw data into meaningful information | 22nd February, 1984 (Formatted date) |
| 22021984     | Converting .... | (22) - 021984 <br>(Telephone Number)


### Conclusion:
- **Processing**: The work done by the computer to convert raw data into **information** (data on which action can be taken or decisions can be made by management).
###
---

## **Database**  
A **Database** is a collection of **large amounts of data** stored in an organized manner.
###

### Basics : DBMS and RDBMS 📊

| **Attribute**                         | **DBMS**                                      | **RDBMS**                                      |
|-------------------------------------|----------------------------------------------|----------------------------------------------|
| **Full Form**                       | **Database Management System**               | **Relational Database Management System**     |
| **Definition**                      | Readymade software that helps manage your data | A type of DBMS that stores data in a relational format (tables), using rows and columns |
| **ANSI Definition**                 | A collection of programs that allows you to insert, update, delete, and process data | A collection of programs that allows you to insert, update, delete, and process data while ensuring data integrity and supporting relationships through tables (relations) |
| **Examples**                | MS Excel, dBase, FoxBASE, FoxPro, Clipper, DataEase, Dataflex, Advanced Revelation, DB Vista, Quattro Pro, etc.| Informix (fastest because we write commands in assembly), Oracle, Sybase, MS SQL Server, Ingres, Postgres, Unify, Non-Stop, DB2 (from IBM), CICS, TELON, IDMS, MS Access, Paradox, Vatcom SQL, MySQL, etc.|

###

### In-Detail Comparison : DBMS vs RDBMS 📊

| **Feature**                                      | **DBMS (e.g., MS Excel, FoxPro)**                                               | **RDBMS (e.g., Oracle, MySQL)**                                                    |
|--------------------------------------------------|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **1.1 Data Storage**                             | Uses files or flat files to store data                                          | Stores data in tables (relations), which consist of rows and columns |
| **1.2 Naming Conventions (Nomenclature)**        | a. Field <br> b. Record <br> c. File<br>![Naming Convention in DBMS](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/1.naming_convention_dbms.png)| a. Column, Attribute, Key <br> b. Row, Tuple, Entity <br> c. Table, Relation, Entity class   |
| **2.1 Relationships between Data**               | No relationships between data                                                   | Supports relationships between data using Primary and Foreign Keys |
| **2.2 Relationship Between 2 files/tables**<br>![Relational Database Management System](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/2.reltn_dbms.png)| Maintained programmatically| Can be specified at the time of table creation (e.g. Foreign key constraint)|
| **3. Programming Requirement**                   | More programming                                                                | Less programming                                                                  |
| **4. Software Development Time**                 | More time required for software development                                     | Less time required for software development                                       |
| **5. Network Traffic**                           | High network traffic                                                            | Low network traffic                                                               |
| **6. Processing Location** <br>![Client-Server DBMS vs RDBMS](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/3.client_server_dbms_vs_rdbms.png)| Processing on Client machine|Processing on Server machine (known as Client-Server architecture)|
| **7. Client-Server Architecture**                | Not supported                                                                   | Supported by most RDBMS                                                           |
| **8. Speed & Cost**                              | Slow and expensive   <br>![Cost in DBMS](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/5.cost_dbms.png)| Faster (in terms of network speed) and cheaper (in terms of hardware cost, network cost, infrastructure cost) <br>![Cost in RDBMS](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/5.cost_rdbms.png)|
| **9. Locking Mechanism**                         | File level locking   <br>![File Level Locking in DBMS](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/4.1.file_level_locking_dbms.png)|Row level locking (internally, every row is a file)  <br>![Row Level Locking in RDBMS](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/4.2.row_level_locking_rdbms.png)|
| **10. Multi-user Support**| Not suitable for multi-user|Suitable for multi-user<br>![Multi-User RDBMS](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/6.multi_user_rdbms.png)|
| **11. Distributed Databases**                    | Not supported                                                                   | Supported by most RDBMS (e.g., banking system)|
| **12. Security**    <br>[ref image](https://github.com/9kaus/ascend_SQL/blob/main/daywise/1/images/7.1.security.png) <br>[ref image](https://github.com/9kaus/ascend_SQL/blob/main/daywise/1/images/7.2.login_security_rdbms.png) <br>[ref image](https://github.com/9kaus/ascend_SQL/blob/main/daywise/1/images/7.3.object_level_security.png)                           | Limited security :<br> a. Dependent on OS for security.(can be made password protected with help of OS)<br>b. Allows access to data through OS.(still file can be accessed)<br>c. Security is not an in-built feature.<br>(file can be deleted) | Advanced security features, including roles, privileges, and access control.<br> Multiple levels of security: <br> a. Logging in security (MySQL database username and password) <br> b. Command level security (permission to issue MySQL commands) <br> c. Object level security (access to tables and other objects of other users) |
| **13. Data Integrity**                           | Data integrity is not enforced                                                  | Data integrity is ensured using constraints like primary keys, foreign keys, unique keys, etc. |
| **14. Normalization**                            | No support for normalization                                                    | Supports normalization (1NF, 2NF, 3NF) to eliminate redundancy and ensure consistency |
| **15. Query Language**                           | No standardized query language                                                  | Uses SQL (Structured Query Language) for querying and managing data |
| **16. Transaction Management**                   | No transaction management                                                       | Supports ACID properties (Atomicity, Consistency, Isolation, Durability) for safe transaction processing |
###

### Learning about popular RDBMS

#### Oracle
- Most popular (because it has the best tools for software development)
- Makes programming very easy
- OODBMS + RDBMS
- Product of Oracle Corporation (founded in 1977, by the people who wrote SQL source code for IBM).
  ![ref image](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/9.sql_history.png)
- #1 largest overall software company in the world
- #1 largest DB software company in the world
- Works on 113 OS
- 10/10 of top 10 companies in the world use Oracle

#### Sybase
- Going down
- Recently acquired by SAP

#### MS SQL Server
- Good RDBMS from Microsoft
- Only works with Windows OS

#### Open-source free RDBMS: (character based) (text based)
- Ingres
- Postgres
- Unify
- Non-Stop

#### DB server has to be a mainframe (supercomputer):
- DB2 (good RDBMS from IBM)
- CICS
- TELON
- IDMS

#### Single-user PC based RDBMS:
- MS Access
- Paradox
- Vatcom SQL

#### MySQL
- MySQL was launched by a Swedish company in 1995
- Its name is a combination of "My", the name of co-founder Michael Widenius' daughter, and "SQL"
- MySQL is an open-source RDBMS
- MySQL was initially free, but now only MySQL Community Edition is free.
- Enterprise and other commercial versions are paid but less cost than Oracle.
- Most widely used open-source RDBMS
- Part of the widely used LAMP open-source web application software stack (and other "AMP" stacks)
  ![ref image](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/8.AMP_stack.png)
- Free-software open-source projects that require an RDBMS often use MySQL
- WordPress, Facebook, Twitter, Flickr, YouTube, Google (though not for searches, they have BigTable), WhatsApp, Instagram, etc.
- Sun Microsystems acquired MySQL in 2008
- Oracle Corporation acquired Sun Microsystems in 2010
###
---

## **Tools in MySQL**

*MySQL command line client*
* MySQL client software  
* Used for running SQL commands, MySQL commands, MySQL PL programs, etc.  
* Character based (text based)  
* Interface with database  
  
*MySQL Workbench*
* MySQL client software  
* Used for running SQL commands, MySQL commands, MySQL PL programs, etc.  
* GUI based (Graphical User Interface) interface with database  
  
*MySQL PL*
* MySQL Programming Language  
* Programming language from MySQL  
* Used for database programming  
  e.g. HRA_CALC, TAX_CALC, ATTENDANCE_CALC, etc.

![Connector Excel Notifier](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/connector_excel_notifier.png)
![Enterprise Backup](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/enterprise_backup.png)
![Backup 1](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/backup1.png)
![Backup 2](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/backup2.png)
![Backup 3](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/backup3.png)
![High Availability Encryption Manager](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/1/images/highavailability_encryption_manager.png)

*MySQL Query Analyzer*
* for query tuning

###
---

## **SQL**

* Structured Query Language - used in all RDBMS.
* SQL commonly pronounced as "Sequel"  
* 9 main statements : 
    - Create, Drop, Alter  
      Insert, Update, Delete  
      Grant, Revoke, Select  
* Conforms to ANSI standards (e.g. 1 character = 1 Byte)  
* Conforms to ISO standards (for QA)  
* Common for all RDBMS  
* Initially founded by IBM (1975-77)  
* Initially known as RQBE (Relational Query by Example)
* 90% source code was written in C & C++ and 10% assembly
* IBM gave RQBE free of cost to ANSI  
* ANSI renamed RQBE to SQL  
* Now controlled by ANSI  
* In 2005, source code of SQL was rewritten in Java (100%)
###
---

## **Learning More About SQL**

SQL is further segregated in major groups :

### Commands common for all RDBMS: 

- 4 sub-divisions of SQL:
  - **DDL** (Data Definition Language): Create, Drop, Alter
  - **DML** (Data Manipulation Language): Insert, Update, Delete
  - **DCL** (Data Control Language) : Grant, Revoke
  - **DQL** (Data Query Language): Select

### Extra in Oracle, PostgreSQL and MySQL:

Not an ANSI standard

- **DTL** (Data Transaction Language) / **TCL** (Transaction Control Language) : Commit, Rollback, Savepoint
  
- **DDL**: Rename, Truncate


### Extra in Oracle RDBMS only:

Not an ANSI standard

- **DML** : Merge, Upsert

###

### Rules for table names, column names, and variable names:  
* Oracle : Max 30 characters & MySQL : Max 64 characters 
* A - Z, a - z, 0-9 allowed  
* Has to begin with an alphabet 
* Special characters $, #, _ is allowed
* In MySQL, to use special characters in table name and column name, then enclose it in backticks \`  \` e.g. \`EMP#\`
* 134 reserved words not allowed
---
