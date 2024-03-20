# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:

### 1) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
```
create table students(
    registernumber integer,
    name varchar(50),
    age integer,
    address varchar(60),
    phonenumber integer
    
);
```
### OUTPUT:

![image](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/5c333d62-8baf-4b25-97f5-e5c62c37f988)


### 2) Alter the above student table by adding another attribute department

### SQL QUERY: 
```
alter table students
add department char(80);
```
### OUTPUT:

![image](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/6759c732-9298-4b65-8353-b8b6c53f1cbf)

### 3) Rename the student table to mystudent

### SQL QUERY: 
```
alter table students rename to mystudent;
```
### OUTPUT:

![image](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/c078909e-a5e7-4b0a-ba78-720afa92a55a)


### 4) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
```
truncate table students
```
### OUTPUT:

![image](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/be0ed95c-7721-4aa5-87bf-de30a7503d86)

### 5) Drop the mystudent table
 
### SQL QUERY:

```
drop table students

```

### OUTPUT:

![image](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/7d986525-8baf-4f4f-9c5a-1e22a34db18c)









## Result:
         Thus the basic DDL commands in SQL are executed. 


