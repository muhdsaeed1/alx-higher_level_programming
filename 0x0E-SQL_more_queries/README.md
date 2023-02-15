
## SQL Joins 

A JOIN clause is used to combine rows from two or more tables, based on a related column between them.

SQL Join statement is used to combine data or rows from two or more tables based on a common field between them. Different types of Joins are as follows: 

INNER JOIN
LEFT JOIN
RIGHT JOIN
FULL JOIN


The simplest Join is INNER JOIN. 


INNER JOIN

This JOIN returns all records from multiple tables that satisfy the specified join condition. It is the simple and most popular form of join and assumes as a default join. If we omit the INNER keyword with the JOIN query, we will get the same output.

INNER JOIN Syntax

The following syntax illustrates the use of INNER JOIN in SQL Server:

SELECT columns    
FROM table1    
INNER JOIN table2 ON condition1    
INNER JOIN table3 ON condition2    
INNER JOIN Example

Let us first create two tables "Student" and "Fee" using the following statement:

CREATE TABLE Student (      
  id int PRIMARY KEY IDENTITY,     
  admission_no varchar(45) NOT NULL,  
  first_name varchar(45) NOT NULL,      
  last_name varchar(45) NOT NULL,  
  age int,  
  city varchar(25) NOT NULL      
);    
  
CREATE TABLE Fee (   
  admission_no varchar(45) NOT NULL,  
  course varchar(45) NOT NULL,      
  amount_paid int,    
);  
Next, we will insert some records into these tables using the below statements:

INSERT INTO Student (admission_no, first_name, last_name, age, city)       
VALUES (3354,'Luisa', 'Evans', 13, 'Texas'),       
(2135, 'Paul', 'Ward', 15, 'Alaska'),       
(4321, 'Peter', 'Bennett', 14, 'California'),    
(4213,'Carlos', 'Patterson', 17, 'New York'),       
(5112, 'Rose', 'Huges', 16, 'Florida'),  
(6113, 'Marielia', 'Simmons', 15, 'Arizona'),    
(7555,'Antonio', 'Butler', 14, 'New York'),       
(8345, 'Diego', 'Cox', 13, 'California');  
  
  
INSERT INTO Fee (admission_no, course, amount_paid)       
VALUES (3354,'Java', 20000),       
(7555, 'Android', 22000),       
(4321, 'Python', 18000),    
(8345,'SQL', 15000),       
(5112, 'Machine Learning', 30000);  
Execute the SELECT statement to verify the records:

Table: Student

SQL Server JOINS
Table: Fee

SQL Server JOINS
We can demonstrate the INNER JOIN using the following command:

SELECT Student.admission_no, Student.first_name, Student.last_name, Fee.course, Fee.amount_paid  
FROM Student  
INNER JOIN Fee  
ON Student.admission_no = Fee.admission_no;  

SQL Server JOINS

In this example, we have used the admission_no column as a join condition to get the data from both tables. Depending on this table, we can see the information of the students who have paid their fee.





