# EX 3 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:

![314383858-08b3adb1-4eaf-4f81-809f-85c2bbe09858](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/13b9b8dd-7962-4603-b164-1cec4315eb13)

### OUTPUT:

![314383984-ba2b28e8-c07f-4bd2-92a5-c7f9ff5cbcbb](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/5cd04c27-e531-4fa8-89be-fa06d5e030bc)

### Q2) Delete the records from manager table where the salary less than 2750.

### QUERY:

![314384085-2d04b041-76d9-42c8-b53b-09bf9b84f790](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/92ce24df-f75a-4304-871b-291e05026fd2)

### OUTPUT:

![314384197-d457ebd6-dda6-4c5a-a815-0309fecffc7a](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/9e7f866a-fb5a-48ea-9304-3c31e438ff10)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)

### QUERY:

![314384331-d7a19291-a819-4924-a76b-50e57d0e60e5](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/9aebd598-b286-4285-8de1-faaef73b8e43)

### OUTPUT:

![314384445-e36c7577-284c-48b9-9f5a-ceb8a28b31ef](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/d2ff8e1d-0d7a-489f-b29a-ff444e001fed)

### Q4)	List the names of Clerks from emp table.

### QUERY:

![314384588-c9d6cb7f-f046-468f-ba12-f07d5627656c](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/17d09327-4057-4000-85ba-427db0faef12)

### OUTPUT:

![314384660-5690c103-3614-4b56-995c-8aa91fdf0632](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/29e4d247-6349-4e59-b7ea-eb38854f6606)

### Q5)	List the names of employee who are not Managers.

### QUERY:

![314384769-ed2b8bc6-9744-4507-9efa-6ee619b0121a](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/661357f9-9351-4f57-8de1-2b62279fada3)

### OUTPUT:

![314384886-ad292e85-71f6-4973-89e6-b552068d6238](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/bc0f8ef7-f22b-489e-a839-93977eedc31a)

### Q6)	List the names of employees not eligible for commission.

### QUERY:

![314384959-5fc05982-2582-4555-988e-68f98cfbedd5](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/02d88089-ce19-456a-a1db-53070c5e16fe)

### OUTPUT:

![314385053-17b71fea-e260-4aae-be9c-44f9af0f63bf](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/2b92dad8-6b62-4e66-b907-91a933ed42bd)

### Q7)	List employees whose name either start or end with ‘s’.

### QUERY:

![314385153-16563f38-79bb-4d5e-85d1-c3d5b3337913](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/a26fbd3a-8f01-4d9e-b131-31cc6c51ea2f)

### OUTPUT:

![314385253-1dc857c4-be2d-49af-9d8e-51033f6f6438](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/a9b49501-316f-4407-8cbb-3785d5e2534d)

### Q8) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.

### QUERY:

![314385332-3b46d71d-8dc1-4ff5-945e-90edab99fd08](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/c38e6ef6-6fda-49c8-9db4-0dda84c6a5da)

### OUTPUT:

![314385466-8432ddde-ac46-44e8-b704-670b2007c15f](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/a74b1f76-f3b5-4615-9ab6-72cd9473b94e)

### Q9) List the Details of Employees who have joined before 30 Sept 81.

### QUERY:

![314385559-09067236-5cb6-445d-a89a-e45e30b76c0c](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/79bc9b3a-407f-48a7-b268-2c638e93b481)

### OUTPUT:

![314385633-ab5fa265-34fc-4c77-9dfd-e3877f58f825](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/3e7ae569-dd8d-45dd-8e4a-f2236fad3031)

### Q10)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.

### QUERY:

![314385811-cda143f4-74ae-4505-8bf8-420e67dff1a9](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/0987d972-64d2-4f66-b1c8-22fb1e671b00)

### OUTPUT:

![314385883-6d5bb7f4-88f4-4cc7-99ad-9f16adb6052a](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/4d564c73-f3d1-412e-a1b0-b634faa6a78a)

### Q11) List the names of employees not belonging to dept no 30,40 & 10

### QUERY:

![314385967-5fe92e25-66c7-4041-a034-0e916ebc2145](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/1f78826c-0efc-42a6-9d02-845945b9fb7d)

### OUTPUT:

![314386056-4be115c8-0a37-4565-8cc3-6b686cb5c809](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/015776ba-49d6-4148-8ef4-39a355d88fdb)

### Q12) Find number of rows in the table EMP

### QUERY:

![314386129-e08f0ffb-7473-4863-a3a7-d04dbf49002f](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/fe8b6a19-cad5-4c0b-8f60-3b92efdb8fcb)

### OUTPUT:

![314386206-8720bb8d-f4ca-41ef-b287-6fe267c30f09](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/9c34b25f-0b7a-4d90-91df-9e7dfea13938)

### Q13) Find maximum, minimum and average salary in EMP table.

### QUERY:

![314386323-26b1ef0f-e505-4446-86a8-42162134f9a9](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/c7cb876c-705b-48b4-a4e0-ec016cce1c47)

### OUTPUT:

![314386519-3b3eeb1f-6e58-4707-b15c-b9944f49dba6](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/c31d43a3-d855-4486-a3f1-edbbecbe7f47)

### Q14) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:

![314386618-9733bf79-637d-41bc-926b-835580706972](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/134da17e-3157-4fb8-abd4-3d4cf7f736b3)

### OUTPUT:

![314386700-06b2e7cb-0e01-4513-8490-e547e70c9ede](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/b5fa2d26-5b3b-4b9f-835a-1fda4882d8cf)

## RESULT :
Thus the basic DML commands are executed.
