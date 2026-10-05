# DBMS_lab-mst

-- Question 3: Banking Management System
-- A. Theory:
-- Explain the difference between WHERE, ORDER BY, and GROUP BY clauses in SQL. Explain the purpose of aggregate functions such as COUNT(), SUM(), AVG(), MAX(), and MIN(). Also explain how aliases are used with columns and tables in SQL.
-- B. Practical:
-- Create a Banking Management System using Customer and Account tables.
-- Create Customer and Account tables with suitable attributes.
-- Apply appropriate Primary Key and Foreign Key constraints.
-- Apply suitable NOT NULL, UNIQUE, DEFAULT, and CHECK constraints.
-- Insert at least 5 customers and 5 account records.
-- Display accounts having a balance greater than a given amount.
-- Display accounts in descending order of their balance.
-- Calculate the total balance of all accounts using an aggregate function.
-- Find the maximum and minimum account balance.
-- Update the balance of a particular account.
-- Delete an account based on a suitable condition.
-- Display the final account records.
-- Question 4: College Course Management System
-- A. Theory:
-- Explain the purpose of DISTINCT, LIKE, IN, BETWEEN, and IS NULL operators in SQL. Explain how these operators are used with the WHERE clause to filter records. Also explain the difference between COUNT(*) and COUNT(column_name).
-- B. Practical:
-- Create a College Course Management System using Course and Faculty tables.
-- Create Course and Faculty tables with suitable attributes.
-- Apply appropriate Primary Key and Foreign Key constraints.
-- Apply suitable NOT NULL, UNIQUE, DEFAULT, and CHECK constraints.
-- Insert at least 5 faculty records and 5 course records.
-- Display courses having credits between 2 and 4.
-- Display courses whose names start with a particular letter using LIKE.
-- Display courses belonging to a selected set of departments using IN.
-- Display unique department names using DISTINCT.
-- Update the faculty assigned to a particular course.
-- Delete a course based on a suitable condition.
-- Add a new column to the Course table using ALTER.
-- Display the final Course records.




CREATE database Bank;
USE Bank;

CREATE TABLE Customer(
Account_no INT PRIMARY KEY,
Name varchar(100),
Balance INT);

create table acc(
Account_no INT primary key,
Balance INT NOT NULL default(0.0));

insert into Customer Values
(1,'Abhi',50000),
(2,'Raj',100000),
(3,'Vani',20000),
(4,'Rahul',60000),
(5,'Yash',500000);

insert into acc Values
(1,50000),
(2,100000),
(3,20000),
(4,60000),
(5,500000);


select* from customer
where Balance>50000;


select* from customer
order by Balance desc;

select sum(Balance) from customer;

select max(Balance) from customer;

select min(Balance) from customer;

update customer
Set Balance=10000 where Name= 'Vani';

delete from customer
where Name = 'Rahul';

select* from customer;





