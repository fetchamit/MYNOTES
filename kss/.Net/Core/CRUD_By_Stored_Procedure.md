# CRUD Operations using Stored Procedure with Entity Framework Core 8.0
-------------------------------------------------------------------------
## What is `Stored Procedure`?
* It is a procedure stored in database.
* Stored procedure ia a pre compiled `SQL Code` that can be called in a software again and again.
* Stored procedure improves speed of software because it is a collection of pre compiled commands so no need to compile a procedure. It directly executes.
* Stored Precedures are more secure than normal SQL commands. It overcomes by the SQL injunction and parameter theft issue.
* Create command is used to create a procedure. Alter command is used to modify a procedure. Drop command is used to remove a procedure. `exec` or `execute` statement is used to run/ call a procedure.

## Types of Procedure
1. System Procedure
2. User Defined Procedure

* Note : A Store procedure can return a numeric value. We can pass different-2 types of parameters in a procedure.

## Syntax to create a procedure

    Create procedure <Procedure_Name>
      @Parameter_1_Name DataType(Size),
      @Parameter_2_Name DataType(Size),
      ...
    AS
    Begin
        // Statements
    End

## Calling a stored procedure from entity framework core

* Generate `Entity Framework Core Model` classes in your project.
* Two below functions are used in most of the times to call a stored procedure-
  1. FromSqlRaw()
  2. ExecuteSqlRaw()

## 1. FromSqlRaw():
* Generally this function is used to execute a select command.
* This function returns object/list of objects of entity class.
* Syntax:

      Obj_Of_DB_contextClass.NameOfTable.FromSqlRaw(@"Procedure_name with parameters").ToList();

## 2. ExecuteSqlRaw():
* Generally this function is used to execute an insert, update or delete command.
* This function does not returns the object of Entity class.
* Syntax:

      ObjectOfDBContextClass.Database.ExecuteSqlRaw(@"ProcedureNameWithparameters");

Note: We can write any static Sql command also inside `ExecuteSqlRaw()` function or we can pass stored procedure.
* In `Entity Framework Core` we can not call a stored procedure that returns related data(`joins`).

* We have two different ways to pass a parameter in stored procedure from Entity Framework Core-
    1. By using {} bracket

      Ex: db.Student.FromSqlRaw(@"Procedure_Name'{ParameterName}');
  
    2. By Creating object of SqlParameter class of `System.Data.SqlClient` namespace.
  
      SqlParameter para=new SqlParameter("@paraName",ParaValue);
      db.Student.FromSqlRaw(@"ProcedureName",para);    
    
     














  
