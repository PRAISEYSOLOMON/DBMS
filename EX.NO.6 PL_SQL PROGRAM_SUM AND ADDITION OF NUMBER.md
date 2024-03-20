# Ex. No: 6 PL/SQL program to perform addition and subtraction of two number 
### DATE: 
### AIM: To create PL/SQL program to perform addition and subtraction of two number.

### Steps:
1. Declare the variable a, b and necessary variables in Declare section.
2. Perform addition of two numbers
3. Perform subtraction of two numbers 
4. Display the result 
5. End the begin section.

### Program:
```
DECLARE
    num1 NUMBER := 10;
    num2 NUMBER := 5;
    result_add NUMBER;
    result_sub NUMBER;
BEGIN
    result_add := num1 + num2;
    result_sub := num1 - num2;
    DBMS_OUTPUT.PUT_LINE('Addition: ' || num1 || ' + ' || num2 || ' = ' || result_add);
    DBMS_OUTPUT.PUT_LINE('Subtraction: ' || num1 || ' - ' || num2 || ' = ' || result_sub);
END;
```

### Output:

![image](https://github.com/PRAISEYSOLOMON/DBMS/assets/119394259/ccef97f8-00b9-4971-aebf-29515ab0b5a3)

### Result:
Thust the program was performed sucessfully.
