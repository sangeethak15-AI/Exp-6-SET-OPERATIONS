# Exp-6-SET-OPERATIONS
### AIM:
The aim of this program is to perform set operations (Union, Union All, Intersect, and Except) between two tables, A and B, in order to combine, find common elements, or identify differences between the tables.

### ALGORITHM:
1. Create table A with attributes ID and name.
2. Create table B with attributes ID and name.
3. Insert values into table A.
4. Insert values into table B.
5. Display the contents of table A.
6. Display the contents of table B.
7. Perform set operations:
a. Union: Combine rows from table A and table B, eliminating duplicates.
b. Union All: Combine rows from table A and table B, including duplicates.
c. Intersect: Find common rows between table A and table B.
d. Except: Find rows in table A that do not exist in table B.
8. Display the results of each set operation.

### PROGRAM:
```sql
create database if not exists MyDatabase;
use MyDatabase;
CREATE TABLE A (
  ID INTEGER PRIMARY KEY,
  name TEXT
);

CREATE TABLE B (
  ID INTEGER PRIMARY KEY,
  name TEXT
);

-- Insert values into table A
INSERT INTO A VALUES (1, 'John');
INSERT INTO A VALUES (2, 'Alice');
INSERT INTO A VALUES (3, 'Bob');

-- Insert values into table B
INSERT INTO B VALUES (2, 'Alice');
INSERT INTO B VALUES (3, 'Bob');
INSERT INTO B VALUES (4, 'Charlie');

-- Display table A
SELECT * FROM A;

-- Display table B
SELECT * FROM B;

SELECT * FROM A
UNION
SELECT * FROM B;

SELECT * FROM A
UNION ALL
SELECT * FROM B;

SELECT * FROM A
INSERTSET;
SELECT * FROM B;

SELECT * FROM A
EXCEPT
SELECT * FROM B;
```
### OUTPUT:
#### The output for table A will be:
<img width="83" alt="a" src="https://github.com/KeerthikaNagarajan/EX-06-SQL/assets/93427089/0c9af9a9-5af8-4de1-9cc6-f5743bc4b1f5">

#### The output for table B will be:
<img width="95" alt="b" src="https://github.com/KeerthikaNagarajan/EX-06-SQL/assets/93427089/f0567d86-96c3-4a0a-934d-6edb104ae24a">

#### Union:
<img width="95" alt="union" src="https://github.com/KeerthikaNagarajan/EX-06-SQL/assets/93427089/1a9af464-718e-4d4b-b49c-19865be302a4">

#### Union All:
<img width="99" alt="UNION ALL" src="https://github.com/KeerthikaNagarajan/EX-06-SQL/assets/93427089/7a1919d1-4e27-4db5-b71b-9b5c074dbd8c">

#### Intersect:
<img width="95" alt="interset" src="https://github.com/KeerthikaNagarajan/EX-06-SQL/assets/93427089/de98b06c-4c7d-4151-a8a7-1d9febfaa9bf">

#### Except:
<img width="91" alt="EXCEPT" src="https://github.com/KeerthikaNagarajan/EX-06-SQL/assets/93427089/804c4cf1-a3e7-4ab9-9746-4955e29aa8b7">

### RESULT:
These results illustrate the outcomes of the set operations performed on tables A and B.



