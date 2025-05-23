# Final Lab Task 1 - MySQL Basics

## Task 1: Create a table named $\color{orange}{\textsf{employee}}$ with the following fields:
- **employee_id**: Unique integer, auto-increment, primary key.
- **employee_name**: String (VARCHAR) with up to 255 characters, not null.
- **manager_id**: Integer, foreign key referencing **employee_id** in the same table (**employees)**.
## Task 2: Create a table named $\color{orange}{\textsf{departments}}$ with the following fields:
- **department_id**: Unique interger, auto-increment,primary key.
- **department_name**: String (VARCHAR) with up to 255 characters, not null.
## Task 3: Create a table named $\color{orange}{\textsf{employee departments}}$ with the following fields:
- **employee_id**: Interger, foreign key referencing **employee_id** in **employees**.
- **department_id**: Interger, foreign key referencing **department_id** in **departments**.
- Composite primary key (**employee_id**, **department_id**).
## Task 4: Create a table named $\color{orange}{\textsf{employee projects}}$ with the following fields:
- **employee_id**: Interger, foreign key referencing **employee_id** in **employees**.
- **project_name**: String (VARCHAR) with up to 255 characters, not null.
## Task 5: Create a table named $\color{orange}{\textsf{managers}}$ with the following fields:
- **manager_id**: Unique interger, auto_increment, primary key.
- **employee_id**: Interger, foreign key referencing **employee_id** in **employees**.

## Query Statements & Table Structure:
### Task 1:
#### Query:
![screenshot](images/Employee.png)
#### Table:
![screenshot](images/Employee_tbl.png)
### Task 2:
#### Query:
![screenshot](images/Department.png)
#### Table:
![screenshot](images/Department_tbl.png)
### Task 3:
#### Query:
![screenshot](images/Employee_dept.png)
#### Table:
![screenshot](images/Employee_dept_tbl.png)
### Task 4:
#### Query:
![screenshot](images/Employee_proj.png)
#### Table:
![screenshot](images/Employee_proj_tbl.png)
### Task 5:
#### Query:
![screenshot](images/Manager.png)
#### Table:
![screenshot](images/Manager_tbl.png)
## ER Diagram:
![screenshot](images/ER_DIAGRAM.png)

