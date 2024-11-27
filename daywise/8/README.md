## Contents 📑

- [Correlated Sub-Query](#correlated-sub-query-) 🔍
    - [Solution 1](#solution-1-) 💡
    - [Solution 2](#solution-2-) 💡
    - [EXISTS](#exists-) ✅
    - [NOT EXISTS](#not-exists-) ❌
- [SET OPERATORS](#set-operators-) 🔗
    - [UNION](#union)
    - [UNION ALL](#union-all)
    - [INTERSECT](#intersect) 🔀
    - [MINUS](#minus) ➖
- [PSEUDO COLUMNS](#pseudo-columns) 🖋️
- [DDL](#ddl) 🛠️
    - [ALTER TABLE](#alter-table) 🏗️
        - [ADD & DROP](#add--drop) ➕➖
        - [MODIFY](#modify) 🔄
    - [RENAME TABLE]()
- [Privileges - DCL](#privileges-dcl) 🔒
    - [GRANT](#grant) ✅
    - [REVOKE](#revoke) ❌

---

## Correlated Sub-Query 🔍

A **correlated sub-query** is a sub-query that references columns from the outer query. This means the inner query is evaluated for each row processed by the outer query, making it more dynamic.
![Image 1](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img1.png)


### Solution 1 💡



This solution uses an **EXISTS** clause to check if an employee belongs to a "Sales" department.

### Solution 2 💡



This solution uses an **IN** clause to achieve the same result but checks for matching department IDs.

### EXISTS ✅

The **EXISTS** operator checks for the existence of rows in a sub-query. If the sub-query returns any rows, the condition is true.



### NOT EXISTS ❌

The **NOT EXISTS** operator checks for the non-existence of rows in a sub-query. If no rows are returned, the condition is true.



---

## SET OPERATORS 🔗

Set operators allow you to combine the results of two or more SELECT queries into a single result set.

### UNION

The **UNION** operator combines the results of two or more SELECT statements and removes duplicates.



### UNION ALL

The **UNION ALL** operator combines the results of two or more SELECT statements without removing duplicates.



### INTERSECT

The **INTERSECT** operator returns only the rows that are common to both SELECT queries.



### MINUS ➖

The **MINUS** operator returns rows from the first query that are not in the second query.



---

## PSEUDO COLUMNS 🖋️

**Pseudo columns** are special columns in Oracle SQL that provide information about a table without being stored in the table. Common pseudo columns include `ROWID`, `ROWNUM`, `SYSDATE`, and `USER`.



---

## DDL 🛠️

**DDL (Data Definition Language)** is used to define and manage database objects like tables, views, and indexes.

### ALTER TABLE 🏗️

The **ALTER TABLE** statement is used to modify an existing table’s structure.

#### ADD ➕



#### DROP ➖



#### MODIFY 🔄



---

## Privileges - DCL 🔒

**DCL (Data Control Language)** commands are used to manage access to database objects.

### GRANT ✅

The **GRANT** statement provides specific privileges to a user or role.



### REVOKE ❌

The **REVOKE** statement removes previously granted privileges from a user or role.


---
