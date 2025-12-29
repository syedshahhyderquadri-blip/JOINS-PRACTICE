#creating tables into databse #
CREATE TABLE Students1 (
    Student_ID INT PRIMARY KEY,
    Name VARCHAR2(100),
    Course VARCHAR2(50)
);

CREATE TABLE Companies1 (
    Company_ID INT PRIMARY KEY,
    Company_Name VARCHAR2(100)
);

CREATE TABLE Job_Postings1 (
    Job_ID INT PRIMARY KEY,
    Company_ID INT,
    Job_Title VARCHAR2(100)
);

CREATE TABLE Applications1 (
    Application_ID INT PRIMARY KEY,
    Student_ID INT,
    Job_ID INT,
    Status VARCHAR2(50)
);

#inserting values in databse#

#Students1 values insertion#
INSERT INTO Students1 VALUES (1, 'Alice', 'CSE');
INSERT INTO Students1 VALUES (2, 'Bob', 'ECE');
INSERT INTO Students1 VALUES (3, 'Charlie', 'ME');

#Companies1 values insertion#
INSERT INTO Companies1 VALUES (201, 'InnovaTech Solutions');
INSERT INTO Companies1 VALUES (202, 'BluePeak Systems');
INSERT INTO Companies1 VALUES (203, 'NovaCore Labs');

#Postings1 values insertion#
INSERT INTO Job_Postings1 VALUES (301, 201, 'Junior Software Developer');
INSERT INTO Job_Postings1 VALUES (302, 202, 'Data Support Engineer');
INSERT INTO Job_Postings1 VALUES (303, 204, 'System Analyst');

#Applications1 values insertion#
INSERT INTO Applications1 VALUES (101, 1, 301, 'Applied');
INSERT INTO Applications1 VALUES (102, 2, 302, 'Shortlisted');
INSERT INTO Applications1 VALUES (501, 11, 301, 'Applied');
INSERT INTO Applications1 VALUES (502, 12, 302, 'Shortlisted');
INSERT INTO Applications1 VALUES (503, 15, 301, 'Applied');


#Performing join operstions#
#innerjoin#
SELECT s.Student_ID, s.Name, a.Status
FROM Students1 s
INNER JOIN Applications1 a
ON s.Student_ID = a.Student_ID;

#leftjoin#
SELECT s.Student_ID, s.Name, a.Status
FROM Students1 s
LEFT JOIN Applications1 a
ON s.Student_ID = a.Student_ID;

#rightjoin#
SELECT c.Company_Name, j.Job_Title
FROM Companies1 c
RIGHT JOIN Job_Postings1 j
ON c.Company_ID = j.Company_ID;

#fulljoin#
SELECT s.Student_ID, s.Name, a.Status
FROM Students1 s
FULL JOIN Applications1 a
ON s.Student_ID = a.Student_ID;
