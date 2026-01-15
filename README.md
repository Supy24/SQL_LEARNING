# SQL_LEARNING
Here, I will be posting my everyday learning of SQL Concepts

Day1_SQL

Structured Query Language (SQL)
------------------------------------------


What is SQL?
----------

SQL (Structured Query Language) is a programming language

Used to communicate with a database server

Helps in storing, retrieving, updating, and managing data

What is a SQL Server?
----------------

A server is a machine (device) with:

Large memory

High processing power

Always ON

Used to store and manage databases

Popular Database Servers
-----------------------------
No	Database Server	License
1	MySQL	Free
2	Oracle	Paid
3	IBM DB2	Paid
4	MS SQL Server	Free Trial (180 days)

------------------------- INSTALL


SQL Server (Microsoft)

SQL Server: Database engine

SSMS (SQL Server Management Studio): Tool to write & execute queries


🔗 SQL Server Download
https://www.microsoft.com/en-in/sql-server/sql-server-downloads

🔗 SSMS Download
https://learn.microsoft.com/en-us/ssms/install/install


------------------------------------------

Default System Databases in SQL Server
Database	Purpose
master	Server-level configuration
model	Template for new databases
msdb	Jobs, schedules, backups
tempdb	Temporary objects & operations

-------------------------------------------

Why SQL Server?
--------------------------
1-Handles large data

2-Supports new records continuously

3- Multitasking support

4-Multiple users at the same time

5-High security

6-Supports RDBMS (Relational Database Management System)

--------------------------------------

SQL Subsets
Type	Full Form	Purpose
DQL	Data Query Language	Fetch data
DDL	Data Definition Language	Structure
DML	Data Manipulation Language	Data handling
DCL	Data Control Language	Permissions
TCL	Transaction Control Language	Transactions

------------------------------------------------------------
SQL Structure Hierarchy
SERVER
   └── DATABASE
         └── TABLE
               └── ROWS & COLUMNS
                     └── RECORDS
-------------------------------------

SQL Comments

Single-line comment:

-- This is a comment

Case Sensitivity

SQL keywords are NOT case-sensitive

Data may be case-sensitive depending on collation

-----------------------------------------------------

DDL – Data Definition Language

Scope: Structure level

Used to define or modify database objects

DDL Commands

CREATE

ALTER

DROP

TRUNCATE

CREATE Command

Used to create:

DATABASE

TABLE

VIEW

FUNCTION

TRIGGER

-------------------------------

CREATE DATABASE

CREATE DATABASE DB_NAME;

------

CREATE TABLE Syntax

CREATE TABLE TABLE_NAME
(
   COL1 DATATYPE(LENGTH) CONSTRAINTS,
   COL2 DATATYPE(LENGTH) CONSTRAINTS,
   COL3 DATATYPE(LENGTH) CONSTRAINTS,
   COL4 DATATYPE(LENGTH) CONSTRAINTS,
   COL5 DATATYPE(LENGTH) CONSTRAINTS
);

SQL Server Data Types
---------------------------------

Numeric Data Types
Type	Description	Size
TINYINT	Whole number	     1 byte
INT	Whole number	     4 bytes
BIGINT	Large whole numbe     8 bytes
FLOAT	Decimal number	    8 bytes
MONEY	Currency	                   8 bytes
Date & Time
Type	Description	Size
DATE	Date only	3 bytes
Character Data Types
Type	Description
CHAR(n)	Fixed-length characters
VARCHAR(n)	Variable-length characters
NCHAR(n)	Unicode fixed-length
NVARCHAR(n)	Unicode variable-length

----------------------------

-------------- CREATE DATABASE

CREATE DATABASE JAN_BATCH9

---- TO SELECT DATABASE
USE JAN_BATCH9

----------------CREATE TABLE

CREATE TABLE STUDENT_DETAILS
( ID INT,
  NAME VARCHAR(30),
  COLLEGE VARCHAR(20),
  CITY VARCHAR(20),
  PINCODE CHAR(6),
  MOBILE CHAR(10),
  FEE MONEY,
  ADDATA  DATE
  )

  --------TO SHOW TABLE DEFINIITION 

  SP_HELP STUDENT_DETAILS

  --------- INSERT

  INSERT INTO STUDENT_DETAILS (ID,NAME,COLLEGE,CITY,PINCODE,MOBILE,FEE,ADDATA) VALUES(1,'RAM','DU','NOIDA','123456','1234567890',35000,'01-05-2026')


  -----------SELECT

  SELECT * FROM STUDENT_DETAILS


--- 

DDL - CREATE , ALTER , DROP , TRUNCATE


DATABASE
--- TABLE
----Constraints
---- RDBMS

-----ALTER - Modify structure 

----- ADD
----- ALTER
----- Drop

----- Add Column 
----- Change Data type 
----- Drop - Database , Table , Column , Constraints


ALTER TABLE TABLE_NAME
ADD COLUMN_DETAILS

DDL
------------------- Level - Structure 
CREATE 
ALTER
DROP
TRUNCATE

------

DML - Data Manipulation Language
------------------------------------------
                   --------------------------- Scope or Level - Data
                   --------------------------- Transaction

INSERT - INSERT RECORDS INTO TABLE
DELETE - DELETE RECORDS FROM TABLE
UPDATE - MODIFY RECORDS
------------------------------------------

INSERT - INSERT RECORDS INTO TABLE

1- Insert records into all columns and order as mention in table no need to mention column name  

2- Insert records in selected columns --- Needed to mention column 

3- Insert Multiple records

4- Insert records as colum order in insert query


---DELETE - DELETE RECORDS FROM TABLE
------------ ALWAYS COME WITH CONDITION 

DELETE FROM  TABLE_NAME
WHERE CONDITION 


-------UPDATE

UPDATE TABLE_NAME
SET COLUMN = VALUE
WHERE  CONDITION 

------------------------------------ TCL-- Transaction Control Language

Transaction Command - Auto-commit 
                - System commit
                

Begin Transaction - change Auto-commit   into  User Commit
Roll Back             - Cancel Last transation 
Save Point           - Roll back conditionaly
Commit               - Paramenet Last Transaction


TCL- Transaction Control Language
-------------------------------------- Scope - Transaction Control
                                                                - DML( Insert , DELETE , UPDATE)


----- QUERY - System Commit- Paranament 
                   - User Control - Begin Transaction 

Rollback - Cancel last Transaction
Save Point - Cancel Conditionaly 
Commit ----


DQL- Data Query Language
---------------------------------
--------------------------------- Scope or Level - Query or Fetch Records
--------------------------------- Select
--------------------------------- Data Analysis - 90%


Select         - Execute the Query
From          - Fetch records from Table    
Where        - Fetch records from Table with Condition 
Group By   - Group on the base of nay column or Summary
Having       - Conditon on the Summary Records
Order by    - Sorting ( Asc or Desc)


---------------From          - Fetch records from Table    

Rules-1 Fetch all(*) records 

     SELECT *(ALL) FROM TABLE_NAME

-----2- SELECT COLUMN REECORDS
 

SELECT COL1,COL2,COL3 FROM TABLE_NAME

---- Multiple Words column name 


SELECT [COL1 name],[COL2 name],COL3 FROM TABLE_NAME


----column name  as name


SELECT [COL1 name] as name ,[COL2 name],COL3  as name FROM TABLE_NAME


-------------- SELECT , FROM , WHERE (FILTER)

---- WHERE - Fetch the conditionally

SELECT * FROM TABLE WHERE COLUMN OPERATOR VALUE


-------------- Group By - Summary
                                   - Base column
                                   - Values
                                   - Agg Function - Sum , min , max,

DQL
-------- Data Query Language
-------- Query or Fetch
-------- Select

------------- Fetch the records from table
-------------- SELECT , FROM , WHERE, GROUP BY , HAVING , ORDER BY 
Select * from Table_name

Select * from Table_name where Condition

Select * from Table_name group by Column 

Select * from Table_name group by Column  having condition 


Select * from Table_name group by Column  having condition  order by colunm


-------------------


WHERE CLAUSE
-------------------- 
------------------- Fetch the records conditionally
-------------------  Data type
-------------------  Operators

Operators
-------------
1- Comparion Operators
2- Logical Operators
3- Null Operators
4- Range Operators
5- Pattern Operators

---------------------------------

1- Comparion Operators - > , < , >= , <= , <>  or =! , Between... and 
   ---text(char, varchar) ---= ,<>  or =!
   --- number -- > , < , >= , <= , <>  or =! , Between... and 
   --- date  --- > , < , >= , <= , <>  or =! , Between... and 


----------------------------------

2- Logical Operators
------------------------- Multiple Conditions
logical and --  all True
logical or    --  any True
logical not   -- True for False , false for True

--- List Operatos - in

---- Null Operators - is

---- Pattern Operators or WildCard- like 

----- In Begining 

where column like 'chac%' 

---- End with

where column like '%cha' 

---In middle  (any where) 

where column like '%cha%' 


where column like '%__cha___%'

Functions
--------------

Text Functions
Math Function (agg functions)
Date Functions
Other Functions

--------------------------

Text Functions
----------------- len , left , right, upper , lower , substring


Functions
-------------
Text
Math
Date and Time Function
others Function
-------------

Top , Round , Distinct , Count (*) ..............

----------------------------------------Join---------------------------------

-------- Fetch the records Single table
-------- Fetch the related records from multiple tables - join 

------ Join

1- Must be a common column b/w tables
2- Common column datatype should be same
3- Number of column will incease
4- It will perform horizontally


----------
 ANSI JOIN  -  ON 
 NON -ANSI - WHERE
------------

--- Types

---- INNER JOIN (BYDEFUALT)
---- LEFT JOIN
---- RIGHT JOIN
---- FULL OUTER JOIN
---- CROSS JOIN
---- SELF JOIN 

-------

Syntax
-----------


SELECT * FROM TABLE1 JOIN_NAME TABLE2 ON TABLE1.CCOLUMN = TABLE2.CCOLUMN



---------- INNER JOIN 

------ Common reocrds from both table  on the base common column 

-------- left join

---- ALL Recored from left table table but only match records from right table  on the base common column


--- RIGHT JOIN

ALL Recored from right table table but only match records from left table  on the base common column


--- full outer join

ALL records from all table but unmatch on both side show as null on the base common column


 VIEW 
 ----------------
                ----- Virtual Table come from Complex DQL Query , it do not save  data physically.


  1- Simply the Query
  2- Reuseability
  3- Security
  4- DQL
  5- Do not allow order by
  6- Mus have name of every column 

-----------
     Create View Viwe_name
     as
            DQL Query   

