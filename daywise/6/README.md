## Contents 📑

- [GROUP BY clause](#group-by-clause-) 🧑‍🤝‍🧑
- [HAVING clause](#having-clause-) 🤔
- [Order of Execution](#order-of-execution-)
- [JOINS](#joins-) 🔗
    - [DATA REDUNDANCY](#data-redundancy)
    - [EQUIJOIN](#equijoin-) 🔄
    - [INEQUIJOIN](#inequijoin-) ≠
    - [OUTER JOIN](#outer-join-%EF%B8%8F) ↔️
        - [LEFT OUTER JOIN](#left-outer-join-)
        - [RIGHT OUTER JOIN](#right-outer-join-)
        - [FULL OUTER JOIN](#full-outer-join-)
    - [Conditional SQL JOINS](#conditional-sql-joins)
    - [Mentioning Columns after ON](-mentioning-columns-after-on)
- [CONT](#cont-) 📝

---

## GROUP BY clause 🧑‍🤝‍🧑

The `GROUP BY` clause is used to group rows that have the same values in specified columns into summary rows. It is often used with aggregate functions like `SUM()`, `COUNT()`, `AVG()`, etc.

![Image 2](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img2.png)
![Image 3](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img3.png)
![groupby_working](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/groupby_working.png)
<br>efficiency comparison : <br>

![groupby_efficiency](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/groupby_efficiency.png)
<br>n-dim queries : <br>

![nd](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/nd.png)
![nd_query](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/nd_query.png)

## HAVING clause 🤔

The `HAVING` clause is used to filter the results of a `GROUP BY` operation based on a condition, similar to the `WHERE` clause but for aggregated data.

![Image 4](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img4.png)
![Image 5](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img5.png)
![having](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/having.png)


## Order of Execution 🎢
![Image 6](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img6.png)

---

## JOINS 🔗

![Image 8](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img8.png)
![joins_detail](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/joins_detail.png)
![joins](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/joins.png)


### DATA REDUNDANCY
![data_red](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/data_red.png)
![Image 9](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img9.png)
![driving_driven](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/driving_driven.png)
![Image 10](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img10.png)


### EQUIJOIN 🔄

An `EQUIJOIN` is a type of join where the join condition is based on equality between the columns.

![Image 11](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img11.png)
![inner_join](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/inner_join.png)


### INEQUIJOIN ≠

An `INEQUIJOIN` is a type of join where the join condition is based on inequality (i.e., not equal to) between the columns.

![Image 12](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img12.png)


### OUTER JOIN ↔️

![Image 13](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img13.png)
![Image 14](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img14.png)


An `OUTER JOIN` returns rows that have matching values in one table, along with rows that do not have a match in the other table. There are three types of outer joins:

#### **LEFT OUTER JOIN**: <br>
Returns all rows from the left table and matched rows from the right table.
![left_outer_join](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/left_outer_join.png)<br>
![Image 16](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img16.png)<br>
![Image 18](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img18.png)
![left_outer](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/left_outer.png)

#### **RIGHT OUTER JOIN**: <br>
Returns all rows from the right table and matched rows from the left table.
![right_outer_join](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/right_outer_join.png)
![image 15](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img15.png)
![right_outer](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/right_outer.png)

#### **FULL OUTER JOIN**: <br>
Returns all rows when there is a match in either left or right table.
![full_outer_join](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/full_outer_join.png)
![image 17](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/img17.png)
![full_outer](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/full_outer.png)

### Conditional SQL JOINS
![conditional_joins](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/conditional_joins.png)
![ex1](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/ex1.png)
![ex2](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/ex2.png)
![ex3](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/ex3.png)
![ex4](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/6/images/ex4.png)

### Mentioning Columns after ON
Remember to first mention DRIVING table column on left side of equals-to symbol and then DRIVEN table column on opposite side.

---

## CONT 📝
Continue to next lecture ...
###
---
