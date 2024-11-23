## **Contents**
- [Data Types](#datatypes-in-mysql-)
  - [String Data Types](#string-data-types)
    - [CHAR vs VARCHAR](#char-vs-varchar)
    - [BINARY vs VARBINARY](#binary-vs-varbinary)
    - [BLOB](#blob)
    - [TEXT](#text)
    - [ENUM](#enum)
    - [SET](#set)
  - [Numeric Data Types](#numeric-data-types)
    - [Integer Data Types](#integer-data-types)
      - [TINYINT vs SMALLINT vs MEDIUMINT vs INT vs BIGINT](#tinyint-vs-smallint-vs-mediumint-vs-int-vs-bigint)
    - [Fixed-Point Types](#fixed-point-types-exact-value-in-mysql-)
    - [Floating-Point Types](#floating-point-types-approximate-value-in-mysql-)
    - [BIT and BOOLEAN](#bit-and-booleanie-tinyint1-)
  - [Date and Time Data Types](#date-and-time-data-types-in-mysql-%EF%B8%8F)
    - [DATE](#date)
    - [DATETIME](#datetime)
    - [YEAR](#year)
- [Operators]()


# **Datatypes in 'MySQL'** 🔢

In SQL, data types define the **type of data that can be stored** in a database column. They determine what **kind of value is allowed in the column** (such as integers, decimals, dates, etc.) and also define the **amount of space** required for storage, as well as the **operations that can be performed** on the data.


> **NOTE :** <br>
  I am going through Data Types in MySQL only.  <br><br>
  I referred : [MySQL v8.4 Data Types](https://dev.mysql.com/doc/refman/8.4/en/data-types.html)   <br><br>
  We can refer :<br>
  [Oracle OORDBMS v11g Data Types](https://docs.oracle.com/cd/B28359_01/server.111/b28318/datatype.htm#CNCPT012) <br>
  [PostgreSQL v17 Data Types](https://www.postgresql.org/docs/current/datatype.html)

###
---

## **String Data Types**  
These are used to store text or alphanumeric data.
###

### The string data types are :
- CHAR,
- VARCHAR,
- BINARY,
- VARBINARY,
- BLOB,
- TEXT,
- ENUM,
- and SET.
###

### `CHAR` vs `VARCHAR`

| **Attribute**          | **CHAR**                                         | **VARCHAR**                                         |
|------------------------|--------------------------------------------------|----------------------------------------------------|
| **Storage**            | Fixed length                                     | Variable length                                    |
| **Maximum Length**     | Up to 255 characters                             | Up to 65,535 characters (64 KB - 1)               |
| **Default Width**      | 1 (Default width)                                | No default width, must specify the width          |
| **Space Usage**        | Can lead to wastage of hard disk space (padded with spaces) | More efficient, saves disk space (only uses necessary space) |
| **Speed of Retrieval** | Faster for searching and retrieval (fixed size)  | Slower for searching and retrieval (variable size) |
| **Best Use Cases**     | Fixed length data, such as **ROLL NO**, **EMPNO**, **PANNO** | Variable length data, such as **ENAME**, **ADDRESS**, **CITY** |
| **Data Type**          | Any character                                    | Any character                                      |

#### Key Points:

- **CHAR** is best for fixed-length data like IDs, codes, or numbers (e.g., roll number, employee number), where the length is predictable. It’s faster in terms of retrieval but may waste space if the values vary in length.
  
- **VARCHAR** is ideal for data that can vary in length, like names or addresses. It conserves disk space but may have slower retrieval times because of its variable nature.
###

### `BINARY` vs `VARBINARY`

| **Attribute**          | **BINARY**                                         | **VARBINARY**                                         |
|------------------------|----------------------------------------------------|------------------------------------------------------|
| **Storage**            | Fixed length                                       | Variable length                                      |
| **Maximum Length**     | Up to 255 bytes of binary data                     | Up to 65,535 bytes of binary data                    |
| **Default Width**      | No default width, width need not be specified.     | No default width, must specify the width             |
| **Space Usage**        | Uses exactly the specified size, can waste space if the data is smaller than the allocated size | More efficient, uses only as much space as required |
| **Speed of Retrieval** | Faster for searching and retrieval (fixed size)    | Slower for searching and retrieval (variable size)   |
| **Best Use Cases**     | Storing small binary data like **BARCODES**, **PICTURE_CODES**, **QR_CODES**, **FINGERPRINTS**, **SIGNATURES** | Storing larger or variable-length binary data like **STICKERS**, **EMOTICONS**, **EMOJIS**, **ICONS** |
| **Data Type**          | Binary data                                        | Binary data                                          |

#### Key Points:
- **BINARY** is used for storing fixed-length binary data. It is ideal for small, fixed-size items such as **barcodes**, **pictures**, and **signatures** where the size of the data is constant. It’s fast for retrieval but may waste space if the data is smaller than the allocated size.
- **VARBINARY** is used for storing variable-length binary data. It is ideal for storing images, icons, or other binary data where the size of the data can vary. It saves disk space but may have slower retrieval times due to its variable nature.
- both of the above are stored as character strings of 1's and 0's
###

### `BLOB`

In MySQL, **BLOB** (Binary Large Object) is used to store multimedia and binary data. These data types are designed for handling large binary data like images, audio, and video.

#### BLOB Types:

| **Data Type**     | **Description**                                                                            | **Maximum Size**                   | **Example Use Case**                    |
|-------------------|--------------------------------------------------------------------------------------------|------------------------------------|-----------------------------------------|
| **TINYBLOB**      | Used for storing small binary data.                                                         | Up to 255 Bytes                    | Small binary data like thumbnails, icons. |
| **BLOB**          | Stores a moderate amount of binary data.                                                   | Up to 65,535 Bytes (64 KB)         | Images, simple documents, etc.          |
| **MEDIUMBLOB**    | Stores larger amounts of binary data.                                                      | Up to 16,777,215 Bytes (16 MB)     | Audio files, low-quality video.         |
| **LONGBLOB**      | Stores very large amounts of binary data.                                                  | Up to 4,294,967,295 Bytes (4 GB)   | High-quality video, large images.       |

#### Key Points:
- All **BLOB** types store binary data **outside the row**, meaning the data is stored outside the table and linked via a **LOCATOR** in the table row.
- These data types are **not intended for searching** but are primarily used for **displaying** large media.
- **Width does not need to be specified** for any of the BLOB types as they handle variable-length binary data automatically.
###

### `TEXT`

In MySQL, **TEXT** data types are used for storing large amounts of text. These data types are particularly useful when you need to store extensive text data but don't need to perform searches on it.

#### TEXT Types:

| **Data Type**   | **Description**                                                                             | **Maximum Size**                        | **Example Use Case**                |
|-----------------|---------------------------------------------------------------------------------------------|-----------------------------------------|-------------------------------------|
| **TINYTEXT**    | Stores small amounts of text.                                                                | Up to 255 characters                    | Short text like **usernames**, **tags**, or **small descriptions**. |
| **TEXT**        | Stores moderate amounts of text.                                                             | Up to 65,535 characters (64 KB)         | **Remarks**, **comments**, or **feedback**. |
| **MEDIUMTEXT**  | Stores larger amounts of text.                                                               | Up to 16,777,215 characters (16 MB)     | **Experience**, **bio**, or **long-form content**. |
| **LONGTEXT**    | Stores very large amounts of text.                                                           | Up to 4,294,967,295 characters (4 GB)   | **Resumes**, **reviews**, or **large documents**. |

#### Key Points:
- All **TEXT** types store text **outside the row**, meaning the data is stored outside the table and linked via a **LOCATOR** (HD pointer).
- **Width does not need to be specified** for any of the **TEXT** data types, as they handle variable-length text data automatically.
- These data types are not typically used for searching but are designed for columns with **large amounts of text** that need to be displayed or stored, rather than searched.
###

### `ENUM`

The **ENUM** data type in MySQL allows you to store a single value from a predefined list of values. It's ideal for columns where the possible values are limited to a small set of predefined options.

#### Characteristics:
- Stores **one value** from a list of predefined values.
- The list of possible values is set at the time of table creation.
- **ENUM** values are internally stored as **numeric indexes** corresponding to the position of each value in the list.
- **Maximum number of values** allowed is 65,535.

#### Syntax:

```sql
ENUM('value1', 'value2', 'value3', ...);
```
#### Example Use Case:
- Status Column: In an application, a status column might only have values like 'Active', 'Inactive', or 'Pending'.
  ```sql
  CREATE TABLE users (
      id INT,
      status ENUM('Active', 'Inactive', 'Pending')
  );
  ```

#### Key Points:
- **Single-value column**: You can only store one value at a time.
- **Efficient**: Internally stored as numeric indexes, saving space.
- **Use Case**: Perfect for columns like gender, status, payment method, or category
###

### `SET`

The **SET** data type in MySQL allows you to store one or more values from a predefined list of values. It's suitable when you need to store multiple selections or choices in a column.

#### Characteristics:
- Stores **multiple values** from a predefined list of options.
- The values are stored as a set, meaning multiple values can be selected at once.
- **SET** values are internally stored as **bit values**, representing a combination of selections.
- **Maximum number of values** allowed is 64.

#### Syntax:

```sql
SET('value1', 'value2', 'value3', ...);
```

#### Example Use Case:
- **Permissions Column**: A `permissions` column might store multiple selected permissions, such as **'Read'**, **'Write'**, and **'Execute'**.

  ```sql
  CREATE TABLE users (
      id INT,
      permissions SET('Read', 'Write', 'Execute')
  );
  ```

#### Key Points:
- **Multiple-value column**: You can store multiple values simultaneously.
- **Efficient**: Internally stored as bit flags, each value is represented as a bit.
- **Use Case**: Best for columns like **tags**, **features**, **permissions**, or **preferences** where multiple selections are allowed.

###
---

## **Numeric Data Types**
These are used to store numeric data.
###

### The Numeric data types are :
- INTEGER,
- FIXED POINT TYPE,
- FLOATING POINT TYPE,
- BIT AND BOOLEAN
###

### **Integer Data Types**

In MySQL, integer data types are used to store whole numbers (both positive and negative) without any decimal points. These data types differ in the range of values they can store and the amount of storage space they occupy. You can also specify whether the number should be **signed** (allowing negative values) or **unsigned** (only positive values).

> **NOTE:** <br>
  By default, integer data types are signed (allowing both positive and negative numbers), but you can specify `UNSIGNED` to restrict values to non-negative numbers.

###

### `TINYINT` vs `SMALLINT` vs `MEDIUMINT` vs `INT` vs `BIGINT`

| **Data Type**   | **Storage**      | **Signed Range**              | **Unsigned Range**           | **Example Use Case**         |
|-----------------|------------------|-------------------------------|------------------------------|------------------------------|
| **TINYINT**     | 1 Byte           | -128 to 127                   | 0 to 255                     | Storing small numbers, e.g., **age**, **status flags**. |
| **SMALLINT**    | 2 Bytes          | -32,768 to 32,767             | 0 to 65,535                  | Storing medium-sized numbers, e.g., **zip codes**, **item quantities**. |
| **MEDIUMINT**   | 3 Bytes          | -8,388,608 to 8,388,607       | 0 to 16,777,215              | Storing larger numbers, e.g., **product IDs**, **large counters**. |
| **INT / INTEGER**         | 4 Bytes          | -2,147,483,648 to 2,147,483,647 | 0 to 4,294,967,295           | Storing regular integers, e.g., **user IDs**, **transaction IDs**. |
| **BIGINT**      | 8 Bytes          | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | 0 to 18,446,744,073,709,551,615 | Storing very large numbers, e.g., **bank account balances**, **large-scale data tracking**. |

#### Key Points:

- **TINYINT** is the smallest integer type, useful for very small numeric values like flags or status codes.
- **SMALLINT** is ideal for medium-range values, such as population numbers or zip codes.
- **MEDIUMINT** is suitable for slightly larger numbers and is efficient for ranges like **inventory counts** or **log identifiers**.
- **INT** is the most common data type for general-purpose integer storage and can store a wide range of values.
- **BIGINT** is used when you need to store very large values that exceed the range of a standard **INT**.
###

### **Fixed-Point Types (Exact Value)** in MySQL 🔢

In MySQL, **DECIMAL** and **NUMERIC** are used to store exact numeric values with a fixed number of digits. These data types are typically used when you need to store precise values, such as monetary amounts or other values that require exact precision without rounding errors.


### `DECIMAL` vs `NUMERIC`

| **Data Type** | **Storage**            | **Precision**                        | **Scale**                        | **Example Use Case**                    |
|---------------|------------------------|--------------------------------------|----------------------------------|-----------------------------------------|
| **DECIMAL**   | Variable length        | Can specify up to 65 digits          | Can specify up to 30 decimal places | Monetary values, **prices**, **tax rates**, **financial data**. |
| **NUMERIC**   | Variable length        | Same as DECIMAL                      | Same as DECIMAL                  | Used in the same way as **DECIMAL**, often used interchangeably with it. |

#### Key Points:

- **DECIMAL** and **NUMERIC** are essentially the same data type in MySQL, with **NUMERIC** being a synonym for **DECIMAL**. Both are used to store exact numeric values without any rounding errors.
- These types are useful for storing values that require high precision, such as in financial or scientific applications.
- **DECIMAL** and **NUMERIC** allow you to specify the precision (total number of digits) and scale (number of digits after the decimal point).
- These types are particularly useful for storing **monetary values**, where rounding errors can lead to significant problems.

#### Example Use Case:
Price Column: A price column in a table for products might need to store values with exact precision, such as 19.99, 5.50, or 100.00.
```sql
CREATE TABLE products (
    id INT,
    name VARCHAR(100),
    price DECIMAL(10, 2) -- Precision: 10 digits, Scale: 2 decimal places
);
```
###

### **Floating-Point Types (Approximate Value)** in MySQL 🌊

In MySQL, **FLOAT** and **DOUBLE** are used to store approximate numeric values, especially for scientific calculations or situations where precision is not as critical. These data types store numbers in floating-point format, which allows them to represent very large or very small numbers efficiently. However, they can have rounding errors due to the way they store numbers.

### `FLOAT` vs `DOUBLE`

| **Data Type** | **Storage**            | **Precision**                        | **Maximum Size**                  | **Example Use Case**                    |
|---------------|------------------------|--------------------------------------|-----------------------------------|-----------------------------------------|
| **FLOAT**     | 4 bytes (32 bits)       | Approx. 7 decimal digits             | Up to ±3.402823466 × 10^38        | Day to day calculations, **normal measurements**. |
| **DOUBLE**    | 8 bytes (64 bits)       | Approx. 15 decimal digits            | Up to ±1.7976931348623157 × 10^308 | High precision calculations, **physics**, **engineering**, **scientific experiments**,**statistical data**. |

#### Key Points:

- **FLOAT** is used when you need to store numbers with less precision (7 decimal digits). It is often used for approximate values where the precision is not critical but the range is.
- **DOUBLE** is used when higher precision is needed (15 decimal digits). It can store larger values and is ideal for scenarios where small rounding errors can accumulate over time, such as in scientific or engineering applications.
- **FLOAT** and **DOUBLE** are efficient for storing large ranges of values but may introduce small rounding errors due to the inherent nature of floating-point arithmetic.

#### Example Use Case:
- Temperature Column: A temperature column might store values like 23.5, 100.45, or -30.987, where a floating-point approximation is sufficient.
  ```sql
  CREATE TABLE measurements (
      id INT,
      location VARCHAR(100),
      temperature FLOAT     -- Approximate value with 7 decimal digits
  );
  ```
- Distance Column: A distance column might store more precise values for large distances, such as 123456.789123, where a higher precision is needed.
  ```sql
  CREATE TABLE journey (
      id INT,
      route VARCHAR(100),
      distance DOUBLE     -- Approximate value with 15 decimal digits
  );
  ```
###

### `BIT` and BOOLEAN(i.e. TINYINT(1)) 💡

In MySQL, the **BIT** data type is used to store bit-field values. It can store binary values as a series of bits (0's and 1's). The **BIT** type is efficient for storing boolean-like data or binary flags.

#### Characteristics:
- Stores **binary values** (0 or 1).
- Can store multiple **bit values** (e.g., `BIT(8)` stores 8 bits, `BIT(16)` stores 16 bits).
- **No need for a fixed width**, the number of bits can be specified as required (e.g., `BIT(1)` for a single bit, `BIT(8)` for 8 bits).
- **Uses less storage space** compared to other numeric data types (e.g., `TINYINT` or `BOOL`).

#### Syntax:

```sql
BIT(M);
```
Where M is the number of bits to store, and it can range from 1 to 64.

#### Example Use Case:
- Boolean Flags: A BIT(1) column is typically used to store boolean values, such as TRUE or FALSE, 1 or 0.
  ```sql
  CREATE TABLE users (
      id INT,
      active BIT(1)
  );
  ```

- Binary Flags: A BIT(4) column can store multiple binary flags, such as permissions or feature toggles.
  ```sql
  CREATE TABLE employee_flags (
      id INT,
      status BIT(4)   -- Represents 4 flags (e.g., bit[0] = on vacation, bit[1] = on leave, etc.)
  );
  ```

#### Key Points:
- Storage: A BIT column with M bits uses M / 8 bytes of storage (rounded up if necessary). For example, a BIT(8) uses 1 byte of storage, and a BIT(16) uses 2 bytes.
- Storage efficiency: Ideal for storing binary values, like flags or small sets of true/false data, in a compact format.
- Multiple bits: You can store multiple binary values (e.g., BIT(8) for a sequence of 8 bits) in a single column.
- Boolean Representation: In MySQL, BIT(1) can also be used to represent boolean values (0 = FALSE, 1 = TRUE), although BOOL or BOOLEAN are often used as synonyms for TINYINT(1) for better readability.

###
---

## **Date and Time Data Types** in MySQL 🕰️

MySQL provides various data types for storing date and time values. These types allow you to store **dates**, **times**, and **timestamps** with varying levels of precision. These data types are essential when working with events, logs, and timestamps in databases.

### The Date and Time Data Types in MySQL:
- **DATE**
- **DATETIME**
- **TIMESTAMP**
- **TIME**
- **YEAR**


### Summary of Date and Time Data Types:

| **Data Type**   | **Format**           | **Range**                             | **Storage** | **Use Case**                              |
|-----------------|----------------------|---------------------------------------|-------------|-------------------------------------------|
| **DATE**        | `YYYY-MM-DD`         | '1000-01-01' to '9999-12-31'         | 3 Bytes     | Storing dates (e.g., birthdates, events). |
| **DATETIME**    | `YYYY-MM-DD HH:MM:SS`| '1000-01-01 00:00:00' to '9999-12-31 23:59:59'| 8 Bytes   | Storing dates and times (e.g., order timestamps). |
| **TIMESTAMP**   | `YYYY-MM-DD HH:MM:SS`| '1970-01-01 00:00:01' UTC to '2038-01-19 03:14:07' UTC | 4 Bytes | Storing timestamps with time zone adjustment (e.g., user logins). |
| **TIME**        | `HH:MM:SS`           | '-838:59:59' to '838:59:59'           | 3 Bytes     | Storing time intervals (e.g., shift durations). |
| **YEAR**        | `YYYY`               | 1901 to 2155                         | 1 Byte      | Storing year values (e.g., event years). |


### `DATE`
- specifying all 4 digits of year is optional<br>
  e.g. '21-06-22'<br>
  (year values in the range 70-99 are converted to 1970-1999)<br>
  (year values in the range 00-69 are converted to 2000-2069)
 
- Why 1970 is the cut-off year (**Year of Epoch**) ?<br>
  Unix was originally developed in the 60s and 70s so the "start" of Unix Time was set to January 1st 1970 at midnight GMT (Greenwich Mean Time) - this date/time was assigned the Unix Time value of 0.

- date1-date2 -> returns number of days between the 2 dates 
 
-  '1000-01-01' -> 1 <br>
  '1000-01-02' -> 2 <br>
  '1000-01-03' -> 3 
 
- '2021-06-22' -> 2456173 (number of days since '1000-01-01')<br>
  internally date is stored a fixed-length number<br>
  Date occupies 7bytes of storage 


### `DATETIME`

- datetime1-datetime2 -> returns number of days, remainder hours, remainder minutes, remainder seconds between the two


### `YEAR`

- max 4096 columns per table provided the row size <= 65,535 Bytes  
- no limit on number of rows per table provided the table size <= 64 Terabytes

###
---
