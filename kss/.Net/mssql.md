# DataBase Connectivity in .NET
---------------------------------
* Database is used to store data of any software or application permanently.
* In .NET we can connect our software with database by using below mechanisms.
  1. ADO.NET
  2. Entity Framework

Note: Entity Framework internally uses ADO.NET for handling database operations.

* ADO and ADO.NET is two different concept, ADO uses only connected mode of database connection. But in ADO.NET we can establize connection with database in connected and disconnected mode.

# ADO.NET
----------
* ADO stands for "ActiveX Database Object".
* ADO.NET is used to perform database related operation in software of application in .NET.
* It provides three types of dataprovider
  1. SQL Data Provider
     * It is used to connect with MSSQL server database.
  2. OLEDB Data Provider
     * It is used to connect with MSAccess, MySQL database etc
     * OLEDB stands for "Object Linking Embedding Database".
  3. Oracle Data Provider
     * It is used to establish connectivity with oracle database.

* ADO.NET is a collection of various classes and functions, that is used to connect with database and helping to perform operation on it.

# Some Inportant classes used in ADO.NET are as follows.
------------------------------------------------------------
1. SqlConnection class
  * SqlConnection class is used to connect with database.
  * It comes "System.Data.SqlClient" namespace.
  * We pass connectionstring as a parameter in SqlConnection class.
  * ConnectionString is a string that contains information related to our database connectivity like server name, id , password etc.

## ConnectionString
---------------------
"datasource=servername;initial catalog=database;integrated security=true";

### Syntax to making object of SqlConnection class

    SqlConnection con=new SqlConnection(connectionstring);

### Some functions and property Sqlconnection Class
a. State=> This property is used to know the current status of database like is it connecting, closed etc.
b. ConnectionString
 * This property is used to get connection string in SqlConnection class.
 * It generally contains all the information that is required for establishing database connectivity in .NET software or application.

c. Open()
  * This function is used to open the database connection.

d. Closed()
  * This function is used to close or terminate the database connection.
 
2. SqlCommand Class
* This class is located under "System.Data.SqlClient" namespace.
* It is used to set and execute database queries.
* It worked in connected mode.
* Syntax of SqlCommand class

      SqlCommand cmd=new SqlCommand("Command",Object_Of_connectionClass);

For Example: 

    SqlCommand cmd=new SqlCommand("delete from tablename",con);

### Some Function and property of SqlCommand Class
**Connection**
  ** This property is used to set Sql connecton in Sql command class.
* ExecuteNonQuery()
    ** This function is used to execute queries  related insert, update and delete.
    ** This function return the result in int form that is it tell the number of rows affected in int form.
* CommandText
    ** This property is used to set queries in SqlCommand class.
    ** It contains the queries related  to insert, update or delete.



3. SqlDataAdapter class
4. DataTable
5. DataSet









