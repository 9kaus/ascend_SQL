## Contents 📑

- [NUMBER FUNCTIONS](#number-functions-) 🔢
    - [ROUND](#round-) 🔄
    - [TRUNCATE](#truncate-) ✂️
    - [CEIL & FLOOR](#ceil--floor-) ⬆️⬇️
    - [SIGN](#sign-) ➕➖
    - [MOD](#mod-) ➗
    - [SQRT](#sqrt-) √
    - [POWER](#power-) ⚡
    - [ABS](#abs-) 💪
- [DATE and TIME Functions](#date-and-time-functions-) 📅⏰
- [LIST FUNCTIONS](#list-functions-) 📋
    - [NULL & IS NOT NULL](#null--is-not-null-) 🚫
    - [IFNULL](#ifnull-) ❓
    - [GREATEST](#greatest-) 🏆
    - [LEAST](#least-) 🥇
    - [CASE expression](#case-expression-) 🧩
- [SINGLE vs MULTI-ROW FUNCTIONS](#single-vs-multi-row-functions-) 🧮
    - [SUM](#sum-) ➕
    - [AVG](#avg-) 🔢
    - [MIN](#min-) 🧑‍💻
    - [MAX](#max-) 📈
    - [COUNT](#count-) 🔢

---

## NUMBER FUNCTIONS 🔢

![Image 1](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img1.png)
<br>will use this table

### ROUND 🔄

The `ROUND()` function is used to round a number to a specified number of decimal places.

![Image 2](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img2.png)

### TRUNCATE ✂️

The `TRUNCATE()` function is used to remove the decimal part of a number, effectively truncating it to the nearest integer.

![Image 3](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img3.png)

### CEIL & FLOOR ⬆️⬇️

- `CEIL()` returns the smallest integer greater than or equal to the specified number.<br>
![Image 4](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img4.png)
- `FLOOR()` returns the largest integer less than or equal to the specified number.
![Image 5](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img5.png)


### SIGN ➕➖

The `SIGN()` function returns the sign of a number: 
- 1 for positive numbers
- 0 for zero
- -1 for negative numbers

![Image 6](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img6.png)


### MOD ➗

The `MOD()` function returns the remainder of a division.
![Image 7](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img7.png)


### SQRT √

The `SQRT()` function returns the square root of a number.
![Image 8](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img8.png)


### POWER ⚡

The `POWER()` function returns the result of raising a number to the specified power.
![Image 9](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img9.png)


### ABS 💪

The `ABS()` function returns the absolute value of a number (i.e., it removes the sign).
![Image 10](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img10.png)


---

## DATE and TIME Functions 📅⏰

This section covers the functions used to manipulate and extract information from date and time values in SQL.

- **CURDATE()**: Returns the current date.
- **NOW()**: Returns the current date and time.
- **DATE_ADD()**: Adds a specified time interval to a date.
- **DATE_SUB()**: Subtracts a specified time interval from a date.
- **DATEDIFF()**: Returns the difference in days between two dates.
- **YEAR(), MONTH(), DAY()**: Extracts the year, month, or day from a date.

![Image 11](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img11.png)
![Image 12](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img12.png)


---

## LIST FUNCTIONS 📋

![Image 13](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img13.png)

### NULL & IS NOT NULL 🚫

- `NULL`: Represents a missing or undefined value.
- `IS NULL`: Checks if a value is NULL.
- `IS NOT NULL`: Checks if a value is not NULL.

![Image 14](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img14.png)

### IFNULL ❓

The `IFNULL()` function replaces `NULL` values with a specified value.

![Image 15](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img15.png)
![Image 16](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img16.png)
![Image 17](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img17.png)

### GREATEST 🏆

The `GREATEST()` function returns the largest value from a list of values.

![Image 18](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img18.png)

### LEAST 🥇

The `LEAST()` function returns the smallest value from a list of values.

![Image 19](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img19.png)

### CASE Expression 🧩

The `CASE` expression provides conditional logic in SQL, similar to an `IF` statement.

![Image 20](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img20.png)
![Image 21](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img21.png)
![Image 22](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img22.png)


### DUAL table 🧮

![Image 23](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img23.png)

---

## SINGLE vs MULTI-ROW FUNCTIONS 🧮

![Image 24](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img24.png)

### SUM ➕

The `SUM()` function returns the total sum of a numeric column.

![Image 25](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img25.png)

### AVG 🔢

The `AVG()` function returns the average value of a numeric column.

![Image 26](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img26.png)

### MIN 🧑‍💻

The `MIN()` function returns the smallest value from a numeric column.

![Image 27](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img27.png)

### MAX 📈

The `MAX()` function returns the largest value from a numeric column.

![Image 28](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img28.png)

### COUNT 🔢

The `COUNT()` function returns the number of rows in a dataset or the number of non-NULL values in a column.

![Image 29](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/5/images/img29.png)

---