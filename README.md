# QL

CREATE DATABASE `3001_db1`;
USE `3001_db1`;

CREATE TABLE 3001_departments (
    dept_no CHAR(4) NOT NULL PRIMARY KEY,
    dept_name VARCHAR(40) NOT NULL UNIQUE
);

CREATE TABLE 3001_employees (
    emp_no INT(11) NOT NULL PRIMARY KEY,
    birth_date DATE NOT NULL,
    first_name VARCHAR(14) NOT NULL,
    last_name VARCHAR(16) NOT NULL,
    gender ENUM('M', 'F') NOT NULL,
    hire_date DATE NOT NULL
);

INSERT INTO 3001_departments VALUES ('D001', 'HR');
INSERT INTO 3001_departments VALUES ('D002', 'IT');
INSERT INTO 3001_departments VALUES ('D003', 'Marketing');

INSERT INTO 3001_employees VALUES 
(1, '1995-06-15', 'Alice', 'Smith', 'F', '2020-01-01'),
(2, '1990-11-23', 'Bob', 'Johnson', 'M', '2019-03-15'),
(3, '1998-02-10', 'Charlie', 'Lee', 'M', '2021-07-20');

-- View departments
SELECT * FROM 3001_departments;

-- View employees
SELECT * FROM 3001_employees;
