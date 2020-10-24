## View

Views are generally used to restrict the user from viewing certain columns and rows. Views display only the data specified in the query, so it shows only the data that is returned by the query defined during the creation of the view. The rest of the data is totally abstract from the end user. 

#### View Creation Syntax
```sql
CREATE VIEW view_name AS  
SELECT columns  
FROM tables  
WHERE conditions; 
```
#### Schema Binding View
```sql
Create View Employee_Details3  
with SCHEMABINDING  
as  
select Emp_Id,Emp_Name,Emp_Salary,Emp_City from DBO.Employee_Details 
```

#### Encrypting a View
```sql
Create View Employee_Details4  
with Encryption  
as  
select Emp_Id,Emp_Name,Emp_Salary,Emp_City from DBO.Employee_Details  
```


