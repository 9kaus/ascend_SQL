## Contents 📑

- [NUMBER FUNCTIONS](#number-functions) 🔢
    - [ROUND](#round) 🔄
    - [TRUNCATE](#truncate) ✂️
    - [CEIL & FLOOR](#ceil--floor) ⬆️⬇️
    - [SIGN](#sign) ➕➖
    - [MOD](#mod) ➗
    - [SQRT](#sqrt) √
    - [POWER](#power) ⚡
    - [ABS](#abs) 💪
- [DATE and TIME Functions](#date-and-time-functions) 📅⏰
- [LIST FUNCTIONS](#list-functions) 📋
    - [NULL & IS NOT NULL](#null--is-not-null) 🚫
    - [IFNULL](#ifnull) ❓
    - [GREATEST](#greatest) 🏆
    - [LEAST](#least) 🥇
    - [CASE expression](#case-expression) 🧩
- [SINGLE vs MULTI-ROW FUNCTIONS](#single-vs-multi-row-functions) 🧮
    - [SUM](#sum) ➕
    - [AVG](#avg) 🔢
    - [MIN](#min) 🧑‍💻
    - [MAX](#max) 📈
    - [COUNT](#count) 🔢

---

## NUMBER FUNCTIONS 🔢

![]()

### ROUND 🔄

The `ROUND()` function is used to round a number to a specified number of decimal places.

![]()

### TRUNCATE ✂️

The `TRUNCATE()` function is used to remove the decimal part of a number, effectively truncating it to the nearest integer.



### CEIL & FLOOR ⬆️⬇️

- `CEIL()` returns the smallest integer greater than or equal to the specified number.
- `FLOOR()` returns the largest integer less than or equal to the specified number.



### SIGN ➕➖

The `SIGN()` function returns the sign of a number: 
- 1 for positive numbers
- 0 for zero
- -1 for negative numbers



### MOD ➗

The `MOD()` function returns the remainder of a division.



### SQRT √

The `SQRT()` function returns the square root of a number.



### POWER ⚡

The `POWER()` function returns the result of raising a number to the specified power.



### ABS 💪

The `ABS()` function returns the absolute value of a number (i.e., it removes the sign).



---

## DATE and TIME Functions 📅⏰

This section covers the functions used to manipulate and extract information from date and time values in SQL.

- **CURDATE()**: Returns the current date.
- **NOW()**: Returns the current date and time.
- **DATE_ADD()**: Adds a specified time interval to a date.
- **DATE_SUB()**: Subtracts a specified time interval from a date.
- **DATEDIFF()**: Returns the difference in days between two dates.
- **YEAR(), MONTH(), DAY()**: Extracts the year, month, or day from a date.



---

## LIST FUNCTIONS 📋

### NULL & IS NOT NULL 🚫

- `NULL`: Represents a missing or undefined value.
- `IS NULL`: Checks if a value is NULL.
- `IS NOT NULL`: Checks if a value is not NULL.



### IFNULL ❓

The `IFNULL()` function replaces `NULL` values with a specified value.



### GREATEST 🏆

The `GREATEST()` function returns the largest value from a list of values.



### LEAST 🥇

The `LEAST()` function returns the smallest value from a list of values.



### CASE Expression 🧩

The `CASE` expression provides conditional logic in SQL, similar to an `IF` statement.



---

## SINGLE vs MULTI-ROW FUNCTIONS 🧮

### SUM ➕

The `SUM()` function returns the total sum of a numeric column.



### AVG 🔢

The `AVG()` function returns the average value of a numeric column.



### MIN 🧑‍💻

The `MIN()` function returns the smallest value from a numeric column.



### MAX 📈

The `MAX()` function returns the largest value from a numeric column.



### COUNT 🔢

The `COUNT()` function returns the number of rows in a dataset or the number of non-NULL values in a column.



---