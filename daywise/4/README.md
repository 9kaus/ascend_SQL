## **Contents** 
- [TRANSACTION PROCESSING](#transaction-processing)
    - [COMMIT](#commit)
    - [ROLLBACK](#rollback)
    - [SAVEPOINT](#savepoint)
    - [ROLLBACK TO SAVEPOINT](#rollback-to-savepoint)
- [READ and WRITE Consistency](#read-and-write-consistency)
    - [ROW LOCKING](#row-locking)
        - [OPTIMISTIC ROW LOCKING](#optimistic-row-locking)
        - [PESSIMISTIC ROW LOCKING](#pessimistic-row-locking)
- [STRING FUNCTIONS](#string-functions)
    - [CONCAT](#concat)
    - [UPPER and LOWER](#upper-and-lower)
    - [Capitalizing Initial Word](#capitalizing-initial-word)
    - [PADDING](#padding)
    - [TRIMMING](#trimming)
    - [SUBSTR](#substr)
    - [REPLACE](#replace)
    - [TRANSLATE](#translate)
    - [INSTR](#instr)
    - [LENGTH](#length)
    - [ASCII](#ascii)
        - [Dual Table](#dual-table)
    - [CHAR and SOUNDEX](#char-and-soundex)
- [HW](#hw)
###
---

# **Transaction Processing**
You can read more about TRANSACTIONS, ACID properties & WAL's by visiting below links :<br>
- [Transactions](https://github.com/9kaus/ascend_SQL/blob/main/daywise/4/Transactions,ACID&WALs/1.Transactions.md)
- [ACID & WALs](https://github.com/9kaus/ascend_SQL/blob/main/daywise/4/Transactions,ACID&WALs/2.ACID&WALs.md)
- [Transaction States](https://github.com/9kaus/ascend_SQL/blob/main/daywise/4/Transactions,ACID&WALs/3.TransactionStates.md)

## COMMIT
The `COMMIT` statement is used to save all changes made during the current transaction to the database. Once committed, the changes become permanent, and the transaction cannot be rolled back.<br>
![Image 1](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img1.png)

## ROLLBACK
The `ROLLBACK` statement is used to undo all changes made during the current transaction. It reverts the database to its previous state before the transaction started, ensuring no partial or erroneous data changes are saved.
![Image 2](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img2.png)

## SAVEPOINT
A `SAVEPOINT` is a point within a transaction to which you can roll back without affecting the entire transaction. It allows you to set intermediate recovery points within long-running transactions.
![Image 3](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img3.png)

## ROLLBACK TO SAVEPOINT
The `ROLLBACK TO SAVEPOINT` statement undoes all the changes made after a specific savepoint. This enables partial rollback, allowing for more fine-grained control of transaction behavior.
![Image 4](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img4.png)
###
---

# **Read and Write Consistency**
![Image 5](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img5.png)
![visible_before_commit](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/visible_before_commit.png)

## ROW LOCKING
Row locking is a method of controlling concurrent access to data in a database. It ensures that once a row is being updated by a transaction, no other transactions can modify or lock the same row simultaneously.
![Image 6](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img6.png)

### OPTIMISTIC ROW LOCKING
Optimistic row locking assumes that no conflict will occur and allows transactions to proceed without locking resources. However, conflicts are checked before committing, and if a conflict is found (another transaction has modified the same data), the transaction is rolled back.
![Image 7](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img7.png)

### PESSIMISTIC ROW LOCKING
Pessimistic row locking assumes that conflicts are likely, and it locks the data when it is first accessed. This prevents other transactions from modifying or accessing the locked row until the transaction is completed.
![Image 8](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img8.png)


before commit :
![before_commit](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/before_commit.png)
<br>
after commit :
![after_commit](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/after_commit.png)

###
---

# **String Functions**
we will use this table throughout learning functions ...
![Image 9](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img9.png)

## CONCAT
The `CONCAT` function is used to join two or more strings together. It combines the given strings into one continuous string.

### CONCAT function
![Image 10](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img10.png)

### CONCAT operator (supported only in Oracle & PostgreSQL)
![Image 11](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img11.png)

## UPPER and LOWER
- `UPPER` converts all characters in a string to uppercase.<br>
    ![Image 12](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img12.png)
- similarly we have `LOWER` which converts all characters in a string to lowercase.

## Capitalizing Initial Word
This function capitalizes the first letter of each word in a string, while leaving the remaining letters in lowercase, making text more readable or properly formatted.<br>
![Image 13](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img13.png)

## PADDING
Padding is used to add extra characters (usually spaces or zeros) to the left or right of a string to ensure that it reaches a certain length.
![Image 14](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img14.png)

## TRIMMING
The `TRIM` function removes unwanted characters from the beginning and end of a string. Typically used to remove leading or trailing spaces.
![Image 15](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img15.png)

## SUBSTR
The `SUBSTR` function extracts a substring from a string, starting from a given position and optionally continuing for a specified length.
![Image 16](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img16.png)

## REPLACE
The `REPLACE` function replaces occurrences of a specified substring within a string with a new substring.
![Image 17](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img17.png)

## TRANSLATE
The `TRANSLATE` function replaces characters in a string with other characters, one-to-one, based on a mapping you define.
![Image 18](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img18.png)

## INSTR
The `INSTR` function returns the position of the first occurrence of a substring within a string. It can also be used to locate the occurrence of characters.<br>
![Image 19](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img19.png)

## LENGTH
The `LENGTH` function returns the number of characters in a string, including spaces.<br>
![Image 20](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img20.png)

## ASCII
The `ASCII` function returns the ASCII (numeric) value of the first character in a string.<br>
![Image 21.1](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img21.1.png)

### Dual Table
The DUAL table is a special one-row, one-column table used in Oracle databases for queries that need a dummy table, such as when selecting system values or performing calculations without needing to query actual data tables.<br>
![Image 21.2](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img21.2.png)

## CHAR and SOUNDEX
- The `CHAR` function converts a number into its corresponding character using the ASCII code.
- The `SOUNDEX` function returns a four-character code representing how a string sounds, which is useful for phonetic matching or similarity comparisons.
<br>

![Image 22](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/img22.png)
###
---

# **HW**
![hw](https://raw.githubusercontent.com/9kaus/ascend_SQL/main/daywise/4/images/hw.png)
###
---