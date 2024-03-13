# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 

![clg databasee](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/4af15cd8-fb14-4438-8d2b-2968c1a66fa4)

### Relational model

![relational model](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/958b26ed-600a-481e-81d2-a9287e0992d0)

### SQL DDL Schema 
```
CREATE TABLE Courses
(
  Course_code INT NOT NULL,
  Name INT NOT NULL,
  Slot_no INT NOT NULL,
  PRIMARY KEY (Course_code),
  UNIQUE (Slot_no)
);

CREATE TABLE Students
(
  First INT NOT NULL,
  Middle INT NOT NULL,
  Last INT NOT NULL,
  Reg_No INT NOT NULL,
  Email_id INT NOT NULL,
  Phone_no INT NOT NULL,
  Course_code INT NOT NULL,
  DID INT NOT NULL,
  PRIMARY KEY (Email_id, Course_code),
  FOREIGN KEY (Course_code) REFERENCES Courses(Course_code),
  FOREIGN KEY (DID) REFERENCES Department(DID),
  UNIQUE (Reg_No),
  UNIQUE (Phone_no)
);

CREATE TABLE Staffs
(
  Name INT NOT NULL,
  Staff_id INT NOT NULL,
  Salary INT NOT NULL,
  Email_id INT NOT NULL,
  Course_code INT NOT NULL,
  DID INT NOT NULL,
  PRIMARY KEY (Staff_id),
  FOREIGN KEY (Email_id, Course_code) REFERENCES Students(Email_id, Course_code),
  FOREIGN KEY (DID) REFERENCES Department(DID)
);

CREATE TABLE Administration
(
  Trasport INT NOT NULL,
  AdminId INT NOT NULL,
  Food INT NOT NULL,
  Accounts INT NOT NULL,
  Email_id INT NOT NULL,
  PRIMARY KEY (Email_id),
  FOREIGN KEY (Email_id) REFERENCES Students(Email_id)
);

CREATE TABLE Department
(
  DID INT NOT NULL,
  Email_id INT NOT NULL,
  PRIMARY KEY (DID),
  FOREIGN KEY (Email_id) REFERENCES Administration(Email_id)
);

CREATE TABLE HOD
(
  DID INT NOT NULL,
  PRIMARY KEY (DID),
  FOREIGN KEY (DID) REFERENCES Department(DID)
);

CREATE TABLE Offers
(
  DID INT NOT NULL,
  Course_code INT NOT NULL,
  PRIMARY KEY (DID, Course_code),
  FOREIGN KEY (DID) REFERENCES Department(DID),
  FOREIGN KEY (Course_code) REFERENCES Courses(Course_code)
);
```

## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
