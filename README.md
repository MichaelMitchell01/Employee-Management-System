- # Employee Management System (MySQL)

This project is a relational database built using MySQL and MySQL Workbench to simulate an employee management system for a fictional company. It includes core database components such as employees, departments, job roles, and salaries, and demonstrates the use of SQL queries, views, and stored procedures.

## 🛠 Tools Used

- MySQL Workbench 8.0.41 CE (64-bit)
- MySQL Server 8.4
- SQL (DDL, DML, stored procedures, views)

## 📁 Schema Overview

The system includes the following tables:

- `departments`: Stores department names.
- `jobs`: Stores job titles.
- `employees`: Stores employee personal and job-related info.
- `salaries`: Tracks employee salary history.

### Entity Relationship Diagram

> <img width="308" alt="ERD" src="https://github.com/user-attachments/assets/64656370-df95-426e-8383-d29ba330f29b" />

## ⚙️ Features

- Create and manage employee records, job roles, and departments.
- Track salary history using a normalized salary table.
- Use stored procedures for employee creation.
- Generate departmental salary averages and employee summaries.
- Create reusable views for reporting.

## 🔍 Sample SQL Queries

### List employees with their departments
```sql
SELECT e.first_name, e.last_name, d.department_name
FROM employees e
JOIN departments d ON e.department_id = d.department_id;
