## Trigger

The first and most important things in everyone's mind is, “What are triggers and why we do we use them?” So a trigger is nothing but a special kind of Stored Procedure.
 
A trigger is a special kind of Stored Procedure or stored program that is automatically fired or executed when some event (insert, delete and update) occurs.

#### Types of Triggers
 
In SQL Server we can create the following 3 types of triggers:
* Data Definition Language (DDL) triggers - In SQL Server we can create triggers on DDL statements (like CREATE, ALTER and DROP) and certain system-defined Stored Procedures that does DDL-like operations.
* Data Manipulation Language (DML) triggers - In SQL Server we can create triggers on DML statements (like INSERT, UPDATE and DELETE) and Stored Procedures that do DML-like operations. DML Triggers are of two types.
* Logon triggers - Logon triggers are a special type of triggers that fire when a LOGON event of SQL Server is raised. This event is raised when a user session is being established with SQL Server that is made after the authentication phase finishes, but before the user session is actually established. Hence, all messages that we define in the trigger, such as error messages, will be redirected to the SQL Server error log. Logon triggers do not fire if authentication fails. We can use these triggers to audit and control server sessions, such as to track login activity or limit the number of sessions for a specific login.

#### Trigger Syntax 

```sql

CREATE TRIGGER triggerName ON table   
AFTER INSERT |After Delete |After Upadte  
AS BEGIN  
  
INSERT INTO dbo.UserHistory............  
  
END  

```
