## SQL Server Function Types

SQL Server supports two types of functions 
* User Defined function: User defined functions are create by a user.
* System Defined Function: System functions are built in database functions. 

### User Defined Functions
 
SQL Server support two types of user defined functions:
* Table Valued Functions
* Scalar Valued Functions

### Table Valued Functions
In this type of function, we select a table data using a user created function. 

```sql

Create function Fun_EmployeeInformation()      
returns table       
as      
return(select * from Employee  )    

```

### Scalar function

Now we are getting an Employee table with two different data joined and displayed in a single column data row. Here create a two-column join function as in the following:

```sql

create function fun_JoinEmpColumnInfo  
(  
   @EmpContact nchar(15),  
   @EmpEmail nvarchar(50),  
   @EmpCity varchar(30)  
)  
returns nvarchar(100)  
as  
begin return(select @EmpContact+ ' ' +@EmpEmail + ' ' + @EmpCity)  
end

```