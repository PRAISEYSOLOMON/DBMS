# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE:
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### Q1) Create a table employee with employee id ,name and Address

### QUERY:
```
sql
create table employee(
emp_id numeric,
emp_name varchar(10),
addr varchar(40)
);
```
### OUTPUT:

![314389686-2671ac5d-aaa0-47ad-a40e-b98aec9fd58e](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/403e1a7e-76b3-4315-973d-215488651a6f)


### Q2) Insert three rows into emploee table 


### QUERY:
```
insert into employee values(1,'Luffy','EastBlue');
insert into employee values(2,'Shanks','GodValley');
insert into employee values(3,'Grap','MarinFord');
```

### OUTPUT:

![314389770-df4f6c33-3865-42f5-8eea-7983a4503526](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/777a0ac1-ea8d-4284-ab69-1ffd0c1483a9)


### Q3) Start the transaction and create a save point s1.

### QUERY:
```
savepoint A;
```

### OUTPUT:

![314389879-0e6183d9-cffa-4a4d-981b-8ca8cce76155](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/c72eab1f-e506-4428-9159-a27bc156bf88)


### Q4) Perform insertion into employee table.

### QUERY:
```
insert into employee(4,'Robin','EniesLobby');
```

### OUTPUT:

![314389977-02ed557b-5ff4-4136-af8f-2dfe95bb92c4](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/9a4749a4-704d-4966-9002-69090c7419ab)


### Q5)	Display the employee table and create a save point s2 .


### QUERY:
```
sql
select * from employee;
savepoint s2;
```

### OUTPUT:

![314390113-ad07dad2-f802-4b6f-bf2d-0b6e5f271b2d](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/8269f473-3ba1-4fab-8d90-fa463fc7f1db)


### Q6)	Perform updation on any one of the row.


### QUERY:
```
sql
update employee set emp_name='Nico Robin' where emp_id=4;
```

### OUTPUT:

![314390235-31725e7d-70e7-4594-b473-a86ef8bc54f0](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/c9e67ff7-7b49-471c-b059-158230a55cf8)


### Q7) Display the employee table and rollback to  save point s2 


### QUERY:
```
sql
select * from employee;
rollback to s2;
```

### OUTPUT:

![314390323-9dd9f3a6-49dd-4fbd-8f80-5aa0be6eb063](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/da23cafa-241b-4d4b-ad49-b05a578e1e3f)


### Q8) Display the employee table and commit the changes; 


### QUERY:
```
sql
select * from employee;
commit;
```

### OUTPUT:

![314390392-40bbafaf-64f0-485f-a6ac-cdc0216185ed](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/3e4cdd36-a876-4c62-bac0-3027487cdac6)


### Q9) Rollback to save point s1;


### QUERY:
```
sql
rollback to A;
```

### OUTPUT:

![314390491-41617233-9078-4f54-9e9b-a128a48cc4e1](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/ca097537-1f91-4b6f-9134-86ffb7d42904)


### Q10)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
```
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;
```

### OUTPUT:
![314390644-4c1ff36f-d7d7-4520-96dd-8d1286acf99b](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/b3d5ac89-5aab-434f-9a3f-1a0611a9dc6f)


### Q11) Check the user access and display the result 


### QUERY:
```
SHOW GRANTS FOR new_user;
```

### OUTPUT:

![314390865-9e740f36-2b2f-46a7-aecf-42a365a04f88](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/3ab8de11-8ac8-4a7b-b11f-48f1caac4be4)

### Q12) Revoke the privillages.

### QUERY:
```
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;
```

### OUTPUT:

![314390974-b096ddeb-f791-4ae9-9c80-52f253c5c68f](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/c1a5ed80-7245-4053-b140-da9a0ba25425)


## RESULT :
Thus the basic TCL and DCL commands are executed.
