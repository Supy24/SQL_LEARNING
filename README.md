SQL Learning Notes

Topic: SQL Fundamentals & Database Basics

🔹 What is SQL?

SQL (Structured Query Language) is a standard programming language used to:

Communicate with a database server

Store data

Retrieve data

Update records

Manage and control databases

SQL is the backbone of data storage and analysis in most business systems.

🔹 What is a SQL Server?

A server is a high-performance machine that is:

Always ON

Equipped with large memory

Designed for high processing power

Used to store, manage, and secure databases

🔹 Popular Database Servers
Database Server	License
MySQL	Free
Oracle	Paid
IBM DB2	Paid
MS SQL Server	Free Trial (180 days)
🔹 Microsoft SQL Server Components

SQL Server → Database Engine (stores & manages data)

SSMS (SQL Server Management Studio) → Tool to write and execute queries

Downloads:

SQL Server

SSMS

🔹 Default System Databases in SQL Server
Database	Purpose
master	Server-level configuration
model	Template for new databases
msdb	Jobs, schedules, backups
tempdb	Temporary objects & operations
🔹 Why SQL Server?

Handles large volumes of data

Supports continuous data entry

Allows multitasking

Supports multiple users simultaneously

High security

Based on RDBMS (Relational Database Management System)

🔹 SQL Structure Hierarchy

SERVER
└── DATABASE
    └── TABLE
        └── ROWS & COLUMNS
            └── RECORDS

🔹 SQL Comments & Case Sensitivity

Single line comment:
-- This is a comment

SQL keywords are not case-sensitive

Data may be case-sensitive depending on collation

🔶 SQL Subsets (Command Categories)
Type	Full Form	Purpose
DQL	Data Query Language	Fetch data
DDL	Data Definition Language	Structure
DML	Data Manipulation Language	Data handling
DCL	Data Control Language	Permissions
TCL	Transaction Control Language	Transactions
🔶 DDL – Data Definition Language

Scope: Structure level

Used to define or modify database objects.

Common DDL Commands:

CREATE

ALTER

DROP

TRUNCATE

Used to create:

DATABASE

TABLE

VIEW

FUNCTION

TRIGGER

🔹 CREATE DATABASE
CREATE DATABASE JAN_BATCH9;

🔹 CREATE TABLE
CREATE TABLE STUDENT_DETAILS (
ID INT,
NAME VARCHAR(30),
COLLEGE VARCHAR(20),
CITY VARCHAR(20),
PINCODE CHAR(6),
MOBILE CHAR(10),
FEE MONEY,
ADDATA DATE
);


Check table structure:

SP_HELP STUDENT_DETAILS;

🔶 SQL Server Data Types
Numeric

TINYINT – 1 byte

INT – 4 bytes

BIGINT – 8 bytes

FLOAT – Decimal

MONEY – Currency

Date & Time

DATE – Date only

Character

CHAR(n) – Fixed length

VARCHAR(n) – Variable length

NCHAR(n) – Unicode fixed

NVARCHAR(n) – Unicode variable

🔶 DML – Data Manipulation Language

Scope: Data level

Commands:

INSERT

UPDATE

DELETE

INSERT Example
INSERT INTO STUDENT_DETAILS 
VALUES (1,'RAM','DU','NOIDA','123456','1234567890',35000,'01-05-2026');

DELETE
DELETE FROM TABLE_NAME WHERE condition;

UPDATE
UPDATE TABLE_NAME SET column = value WHERE condition;


⚠️ DELETE and UPDATE should always be used with WHERE condition.

🔶 TCL – Transaction Control Language

Scope: Transaction control (works with DML)

BEGIN TRANSACTION

COMMIT → Save permanently

ROLLBACK → Undo last transaction

SAVEPOINT → Partial rollback

🔶 DQL – Data Query Language

Scope: Fetch & analyze data (most used – ~90%)

Key clauses:

SELECT

FROM

WHERE

GROUP BY

HAVING

ORDER BY

Example structure:

SELECT columns  
FROM table  
WHERE condition  
GROUP BY column  
HAVING condition  
ORDER BY column;

🔶 WHERE Clause & Operators
Comparison:

> < >= <= = <> BETWEEN

Logical:

AND, OR, NOT

List:

IN

NULL:

IS NULL, IS NOT NULL

Pattern:

LIKE

Examples:

Starts with: 'cha%'

Ends with: '%cha'

Anywhere: '%cha%'

🔶 Functions
Text:

LEN, LEFT, RIGHT, UPPER, LOWER, SUBSTRING

Aggregate:

SUM, MIN, MAX, COUNT, DISTINCT

Other:

TOP, ROUND

🔶 JOINS – Combining Multiple Tables

Used to fetch related data from more than one table.

Conditions:

Common column must exist

Data type must be same

Columns increase horizontally

Types of Joins:

INNER JOIN

LEFT JOIN

RIGHT JOIN

FULL OUTER JOIN

CROSS JOIN

SELF JOIN

Syntax:

SELECT *
FROM TABLE1
JOIN TABLE2
ON TABLE1.column = TABLE2.column;

🔶 VIEW

A virtual table created from complex SELECT queries.

Advantages:

Simplifies queries

Reusability

Security

No physical data storage

Rules:

Based only on DQL

No ORDER BY

Each column must have a name

🔶 SET OPERATORS

UNION → Unique records

UNION ALL → Duplicates allowed

INTERSECT → Common records

EXCEPT → Records in first query but not second
