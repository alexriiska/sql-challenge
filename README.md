# sql-challenge

## Background
It’s a beautiful spring day, and it’s been two weeks since you were hired as a new data engineer at Pewlett Hackard. Your first major task is a research project on employees of the corporation from the 1980s and 1990s. All that remains of the database of employees from that period are six CSV files.
In this assignment, you will design the tables to hold data in the CSVs, import the CSVs into a SQL database, and answer questions about the data. In other words, you will perform data modeling, data engineering, and data analysis.


## Data Modeling
Inspect the CSVs and sketch out an ERD of the tables


## Data Engineering
* Use the provided information to create a table schema for each of the six CSV files. Remember to specify data types, primary keys, foreign keys, and other constraints.
* For the primary keys, verify that the column is unique. Otherwise, create a composite key, which takes two primary keys to uniquely identify a row.
* Be sure to create tables in the correct order to handle foreign keys.
* Import each CSV file into the corresponding SQL table.

![QuickDBD-Free Diagram](https://user-images.githubusercontent.com/49711676/169715584-8364415c-34e9-498d-b786-d076fe92caca.png)

## Data Analysis

Once you have a complete database, perform these steps:

### 1. List the following details of each employee: employee number, last name, first name, sex, and salary.
SELECT employees.emp_no, employees.last_name, employees.first_name, employees.sex, salaries.salary
FROM employees
INNER JOIN salaries 
ON employees.emp_no = salaries.emp_no
ORDER BY employees.emp_no


### 2. List first name, last name, and hire date for employees who were hired in 1986.


### 3. List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.


### 4. List the department of each employee with the following information: employee number, last name, first name, and department name.


### 5. List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."


### 6. List all employees in the Sales department, including their employee number, last name, first name, and department name.


### 7. List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.


### 8. List the frequency count of employee last names (i.e., how many employees share each last name) in descending order.
