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

  ## 📂 SQL Files

- [`create_tables.sql`](./create_tables.sql): Contains all DDL table creation scripts.
- [`insert_data.sql`](./insert_data.sql): Sample data for departments, jobs, employees, and salaries.
- [`procedures.sql`](./procedures.sql): Stored procedure to insert new employees.
- [`views.sql`](./views.sql): View for employee summary reports.

## 🔍 Sample SQL Queries

### List employees with their departments
```sql
SELECT e.first_name, e.last_name, d.department_name
FROM employees e
JOIN departments d ON e.department_id = d.department_id;

### Average salary by department

SELECT d.department_name, AVG(s.salary) AS average_salary
FROM employees e
JOIN departments d ON e.department_id = d.department_id
JOIN salaries s ON e.employee_id = s.employee_id
GROUP BY d.department_name;

### Add an employee via a stored procedure

CALL AddEmployee('Eve', 'Martinez', 'eve.m@example.com', '555-0104', '2023-05-01', 1, 1, 1);

### 📊 Views
A view called "employee_summary" consolidates key employee info:

SELECT * FROM employee_summary;

### 💡 Key Takeaways
• Practiced relational database design with foreign key constraints.

• Gained hands-on experience with JOIN operations and stored procedures.

• Built dynamic queries to support real-world business logic and reporting.

### 📂 How to Use
1. Clone this repository.

2. Import the SQL script into MySQL Workbench.

3. Execute scripts in order:

• Schema and table creation

• Sample data inserts

• Procedures and views

4. Modify or extend as needed to test additional features or enhancements.

### 📬 Contact
Michael B. Mitchell
mbmitchell410@gmail.com
https://linkedin.com/in/michaelm410/

---

Let me know if you’d like a dbdiagram link or a formatted schema diagram to add!
