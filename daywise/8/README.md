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
    - [MINUS](#minus-) ➖
    - [MISC](#misc)
- [PSEUDO COLUMNS](#pseudo-columns-%EF%B8%8F) 🖋️
- [DDL](#ddl-%EF%B8%8F) 🛠️
    - [ALTER TABLE](#alter-table-%EF%B8%8F) 🏗️
        - [ADD & DROP](#add--drop-) ➕➖
        - [MODIFY](#modify-) 🔄
        - [Changing Data Type of Column](#changing-data-type-of-column)
        - [Copy Rows from One to Another Table](#copy-rows-from-one-to-another-table)
        - [Copy Specific Rows](#copy-specific-rows)
        - [Copy a Table](#copy-a-table)
        - [Copy structure of Table](#copy-structure-of-table)
        - [Rename a Column](#rename-a-column)
        - [Change position of columns in table structure](#change-position-of-columns-in-table-structure)
    - [RENAME TABLE](#rename-table)
- [Privileges - DCL](#privileges---dcl-) 🔒
    - [GRANT](#grant-) ✅
    - [REVOKE](#revoke-) ❌

---

## Correlated Sub-Query 🔍

A **correlated sub-query** is a sub-query that references columns from the outer query. This means the inner query is evaluated for each row processed by the outer query, making it more dynamic.
![Image 1](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img1.png)
![Image 2](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img2.png)

### Solution 1 💡

![Image 3](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img3.png)

This solution uses an **IN** operator to achieve the result.

### Solution 2 💡

![Image 4](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img4.png)

This solution uses **JOINS** to achieve the same result.

![Image 35](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img35.png)

### EXISTS ✅

The **EXISTS** operator checks for the existence of rows in a sub-query. If the sub-query returns any rows, the condition is true.

![Image 5](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img5.png)
![Image 6](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img6.png)
![Image 36](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img36.png)

### NOT EXISTS ❌

The **NOT EXISTS** operator checks for the non-existence of rows in a sub-query. If no rows are returned, the condition is true.

![Image 7](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img7.png)

---

## SET OPERATORS 🔗

Set operators allow you to combine the results of two or more SELECT queries into a single result set.

![Image 8](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img8.png)
![Image 37](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img37.png)
according to Dr. Codd 👆
### UNION

The **UNION** operator combines the results of two or more SELECT statements and removes duplicates.

![Image 9](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img9.png)

### UNION ALL

The **UNION ALL** operator combines the results of two or more SELECT statements without removing duplicates.

![Image 10](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img10.png)

### INTERSECT

The **INTERSECT** operator returns only the rows that are common to both SELECT queries.

![Image 11](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img11.png)

### MINUS ➖

The **MINUS** operator returns rows from the first query that are not in the second query.

![Image 12](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img12.png)

### Misc

![Image 13](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img13.png)
![Image 14](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img14.png)

---

## PSEUDO COLUMNS 🖋️

**Pseudo columns** are special columns in Oracle SQL that provide information about a table without being stored in the table. Common pseudo columns include `ROWID`, `ROWNUM`, `SYSDATE`, and `USER`.

### ROWNUM
![Image 16](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img16.png)
![Image 17](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img17.png)

### ROWID
![Image 18](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img18.png)
![Image 39](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img39.png)
Delete row using `ROWID` :<br>
![Image 42](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img42.png)
Updating a row using `ROWID` :<br>
![Image 40](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img40.png)
![Image 41](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img41.png)
if after update row size increases then the row address or `ROWID` will change.<br>
and now while searching the row won't appear at same sequenced place.

### Note
![Image 19](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img19.png)

---

## DDL 🛠️

**DDL (Data Definition Language)** is used to define and manage database objects like tables, views, and indexes.



### ALTER TABLE 🏗️

The **ALTER TABLE** statement is used to modify an existing table’s structure.<br>
![Image 20](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img20.png)
![Image 21](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img21.png)
![Image 22](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img22.png)

#### ADD & DROP ➕➖
![Image 24](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img24.png)

#### MODIFY 🔄
Decreasing Width of Column :<br>
![Image 25](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img25.png)

#### Changing Data Type of Column
![Image 26](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img26.png)

#### Copy Rows from One to Another Table
![Image 27](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img27.png)

#### Copy Specific Rows
![Image 28](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img28.png)

#### Copy a Table
![Image 48](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img48.png)
![Image 46](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img46.png)
![Image 47](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img47.png)

#### Copy structure of Table
![Image 49](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img49.png)
![Image 30](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img30.png)
![Image 51](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img51.png)
![Image 50](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img50.png)
![Image 32](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img32.png)

#### Rename a Column
![Image 52](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img52.png)

#### Change position of columns in table structure
![Image 53](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img53.png)
![Image 44](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img44.png)

### RENAME TABLE
![Image 23](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/8/images/img23.png)
---

## Privileges - DCL 🔒

**DCL (Data Control Language)** commands are used to manage access to database objects.

### GRANT ✅

The **GRANT** statement provides specific privileges to a user or role.



### REVOKE ❌

The **REVOKE** statement removes previously granted privileges from a user or role.


---
