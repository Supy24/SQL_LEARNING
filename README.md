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
