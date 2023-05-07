Exercise 1 (5 marks):
_____________________
Create a database schema for the online consultation and therapy website. The database should contain the following tables:-

Doctor table:- The table should contain the attributes such as id, name, specialization, etc.
Appointments table:- The table should contain information related to appointments set up by doctors and patients.
Patient table:- The table should contain information on patients.
Reviews table:- This table should contain reviews posted by patients.
NOTE:- Use proper constraints on the attributes such as primary key, not null and etc.


-- creating a database TELETHERAPY for online consultation and therapy website
CREATE DATABASE TELETHERAPY;

-- creating table doctor in the TELETHERAPY database. 
CREATE TABLE doctor (
	  DOC_ID INT PRIMARY KEY,
    DOC_NAME VARCHAR(30) NOT NULL,
    SPECIALIZATION VARCHAR(15) NOT NULL
    );

-- creating table appointments in the TELETHERAPY database. 
CREATE TABLE appointments ( 
    APPOINT_ID INT PRIMARY KEY,
    PATIENT_ID INT ,                                      
    PATIENT_NAME VARCHAR(40) NOT NULL,                    
    DOC_ID INT ,                        
    DOC_NAME VARCHAR(40) NOT NULL,                 
    APPOINT_DATE DATE NOT NULL,                    
    APPOINT_TIMINGS TIME NOT NULL,                 
    APPOINT_DURATION VARCHAR(10) NOT NULL          
    );

-- creating table patients in the TELETHERAPY database. 
CREATE TABLE PATIENTS (
    PATIENT_ID INT PRIMARY KEY,
    PATIENT_NAME VARCHAR(40) NOT NULL,
    AGE INT NOT NULL,
    GENDER VARCHAR(10) NOT NULL,
    MOBILE INT NOT NULL,
    SYMPTOMS VARCHAR(80) NOT NULL
    );

-- creating table reviews in the TELETHERAPY database. 
CREATE TABLE REVIEWS (
    PATIENT_ID INT PRIMARY KEY,
    PATIENT_NAME VARCHAR(40) NOT NULL,
    DOC_ID INT NOT NULL,
    DOC_NAME VARCHAR(40) NOT NULL,
    REVIEWS VARCHAR(200) NOT NULL
    );
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------    
Exercise 2 (5 marks):
______________________

Contact Table :-
______________

Id | Email |fname | lname |company |Active_flag |opt_out
123 |a@a.com |Kian |Seth  |ABC      |1           |1
133 |b@a.com |Neha |Seth  |ABC      |1           |0
234 |c@c.com |Puru |Malik |CDF      |0           |0
342 |d@d.com |Sid  |Maan  |TEG      |1           |0

QUESTIONS:
---------
	CREATE TABLE CONTACT (
		Id INT PRIMARY KEY,
		Email VARCHAR(30) NOT NULL,
		fname VARCHAR(20) NOT NULL,
    lname VARCHAR(10) NOT NULL,
		company VARCHAR(20) NOT NULL,
		Active_flag BOOL NOT NULL,
    opt_out bool NOT NULL
    );


INSERT INTO CONTACT VALUES (123,'a@a.com','Kian','Seth','ABC',1,1),(133,'b@a.com','Neha','Seth','ABC',1,0),
(234,'c@c.com','Puru','Malik','CDF',0,0),(342,'d@d.com','Sid','Maan','TEG',1,0);
SELECT * FROM CONTACT;

-- Select all columns from the contact table where the active flag is 1
SELECT * FROM CONTACT WHERE Active_flag = 1;
-- Deactivate contacts who are opted out 
UPDATE CONTACT SET Active_flag = 0 WHERE opt_out = 1;
-- Delete all the contacts who have the company name as ‘ABC’
DELETE FROM CONTACT WHERE company = 'ABC';
-- Insert a new row with id as 658, name as ‘mili’, email as ‘mili@gmail.com’, the company as ‘DGH’, active flag as 1, opt-out flag as 1
INSERT INTO CONTACT VALUES (658,"mili@gmail.com", "mili","Iyer","DGH", 1 ,1);
-- Pull out the unique values of the company column 
SELECT DISTINCT(COMPANY) FROM CONTACT;
-- Update name “mili” to “niti”.
UPDATE CONTACT SET fname = "niti" where fname = "mili";
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Exercise 3 (10 marks):
_____________________

Sample table: customer

customer_id |   cust_name    |    city    | grade | salesman_id 

-------------+----------------+------------+-------+-------------

        3002 | Nick Rimando   | New York   |   100 |        5001

        3007 | Brad Davis     | New York   |   200 |        5001

        3005 | Graham Zusi    | California |   200 |        5002

        3008 | Julian Green   | London     |   300 |        5002

        3004 | Fabian Johnson | Paris      |   300 |        5006

        3009 | Geoff Cameron  | Berlin     |   100 |        5003

        3003 | Jozy Altidor   | Moscow     |   200 |        5007

        3001 | Brad Guzan     | London     |       |        5005


CREATE TABLE CUSTOMER (
	  customer_id INT PRIMARY KEY,
    cust_name VARCHAR(40) NOT NULL,
    city VARCHAR(30) NOT NULL,
    grade VARCHAR(10),
    salesman_id int NOT NULL
    );

INSERT INTO CUSTOMER VALUES (3002, "Nick Rimando", "New York", 100, 5001), (3007, "Brad Davis", "New York", 200, 5001),
	(3005, "Graham Zusi", "California", 200, 5002), (3008, "Zulian Green", "London", 300, 5002),
    (3004, "Fabian Johnson", "Paris", 300, 5006), (3009, "Goeff Cameron", "Berlin", 100, 5003),
    (3003, "Jozy Altidor", "Moscow", 200, 5007), (3001, "Brad Guzan", "London",' ', 5005);
SELECT * FROM CUSTOMER;

Sample table: salesman

 salesman_id |    name    |   city   | commission 

-------------+------------+----------+------------

        5001 | James Hoog | New York |       0.15

        5002 | Nail Knite | Paris    |       0.13

        5005 | Pit Alex   | London   |       0.11

        5006 | Mc Lyon    | Paris    |       0.14

        5007 | Paul Adam  | Rome     |       0.13

        5003 | Lauson Hen | San Jose |       0.12
        
CREATE TABLE SALESMAN (
	  salesman_id INT PRIMARY KEY,
    name VARCHAR(40) NOT NULL,
    city VARCHAR(30) NOT NULL,
    commission FLOAT NOT NULL
    );
    
INSERT INTO SALESMAN VALUES (5001, "James Hoog", "New York", 0.15), 
(5002, "Nail Knite", "Paris", 0.13),(5005, "Pit Alex", "London", 0.11),
(5006, "Mc Lyon", "Paris", 0.14),(5007, "Paul Adam", "Rome", 0.13),
(5003, "Lauson Hen", "San Jose", 0.12);
SELECT * FROM SALESMAN;
Question:-
__________
A SQL query to find those customers with a grade less than 100. It should return cust_name, customer city, grade, salesman, and salesman city. The result should be 
ordered by ascending customer_id.

SELECT cust_name, C.city, grade, S.name, S.city FROM CUSTOMER C, SALESMAN S 
WHERE C.salesman_id = S.salesman_id AND C.grade < 100
ORDER BY customer_id;

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
