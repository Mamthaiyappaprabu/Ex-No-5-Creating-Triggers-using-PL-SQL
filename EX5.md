# Ex. No: 5 Creating Triggers using PL/SQL

### AIM: To create a Trigger using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create salary_log table with following attributes (log_id NUMBER GENERATED ALWAYS AS IDENTITY, empid NUMBER,empname VARCHAR(10),old_salary NUMBER,new_salary NUMBER,update_date DATE);
3. Create a trigger named as log_salary-update.
4. Inside the trigger block, Insert the values into the salary_log table whenever the salary is updated.
5. End the trigger.
6. Update the salary of an employee in employee table.
7. Whenever a salary is updated for the employee it must be logged into the salary_log table with old salary and new salary.
8. Display the employee table, salary_log table.

### Program:

```
CREATE TABLE employee1(empid NUMBER,empname VARCHAR2(20),dept VARCHAR2(20),salary NUMBER);
CREATE TABLE sal_log (log_id NUMBER GENERATED ALWAYS AS IDENTITY,empid NUMBER,empname VARCHAR2(10),old_salary NUMBER,new_salary NUMBER,update_date DATE);
```
```
-- Insert the values in the employee table
insert into employee1 values(1,'PRANAV','MECH',5000000);
 i![Screenshot 2023-10-08 173528](https://github.com/Mamthaiyappaprabu/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/119393563/2fe21e61-f43b-4599-a1f3-70d60ec5a2b3)
nsert into employee1 values(2,'ROHAN','ECE',7000000);
```
## Create employee table

![Screenshot 2023-10-08 173528](https://github.com/Mamthaiyappaprabu/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/119393563/a7be38f3-f7ba-4e06-b6f6-909de560987d)

## Create salary_log table
![Screenshot 2023-10-08 173539](https://github.com/Mamthaiyappaprabu/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/119393563/fde37d85-4198-4e7b-80a0-92462340a622)

## PLSQL Trigger code :
```
SQL> UPDATE employee1
    SET salary = 60000
    WHERE empid = 1;
```
```
SQL> SELECT * FROM employee1;
```
```
SQL> SELECT * FROM sal_log;
```

## Output:
![Screenshot 2023-10-08 172631](https://github.com/Mamthaiyappaprabu/Ex-No-5-Creating-Triggers-using-PL-SQL/assets/119393563/96d4e487-dd32-428f-8166-912b21505fab)


## Result:
The program has been implemented successfully
