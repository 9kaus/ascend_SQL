## Contents 📑

- [GROUP FUNCTIONS](#group-aggregate-functions) 📊
- [GROUP BY clause](#group-by-clause) 🧑‍🤝‍🧑
- [HAVING clause](#having-clause) 🤔
- [JOINS](#joins) 🔗
    - [EQUIJOIN](#equijoin) 🔄
    - [INEQUIJOIN](#inequijoin) ≠
    - [OUTER JOIN](#outer-join) ↔️
- [CONT](#cont) 📝

---

## GROUP / AGGREGATE FUNCTIONS 📊

![Image 1](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img1.png)

## GROUP BY clause 🧑‍🤝‍🧑

The `GROUP BY` clause is used to group rows that have the same values in specified columns into summary rows. It is often used with aggregate functions like `SUM()`, `COUNT()`, `AVG()`, etc.



## HAVING clause 🤔

The `HAVING` clause is used to filter the results of a `GROUP BY` operation based on a condition, similar to the `WHERE` clause but for aggregated data.


---

## JOINS 🔗

### EQUIJOIN 🔄

An `EQUIJOIN` is a type of join where the join condition is based on equality between the columns.



### INEQUIJOIN ≠

An `INEQUIJOIN` is a type of join where the join condition is based on inequality (i.e., not equal to) between the columns.



### OUTER JOIN ↔️

An `OUTER JOIN` returns rows that have matching values in one table, along with rows that do not have a match in the other table. There are three types of outer joins:
- **LEFT OUTER JOIN**: Returns all rows from the left table and matched rows from the right table.
- **RIGHT OUTER JOIN**: Returns all rows from the right table and matched rows from the left table.
- **FULL OUTER JOIN**: Returns all rows when there is a match in either left or right table.


---

## CONT ... next lecture 📝

---