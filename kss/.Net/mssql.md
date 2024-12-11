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
# 1. SqlConnection class
  * SqlConnection class is used to connect with database.
  * It comes "System.Data.SqlClient" namespace.
  * We pass connectionstring as a parameter in SqlConnection class.
  * ConnectionString is a string that contains information related to our database connectivity like server name, id , password etc.

## ConnectionString
---------------------
"data source=servername;initial catalog=database;integrated security=true";

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
a. Connection
  * This property is used to set Sql connecton in Sql command class.
b. ExecuteNonQuery()
* This function is used to execute queries  related insert, update and delete.
* This function return the result in int form that is it tell the number of rows affected in int form.
c. CommandText
* This property is used to set queries in SqlCommand class.
* It contains the queries related  to insert, update or delete.



3. SqlDataAdapter class
* This class is located in "System.Data.SqlClient" namespace.
* It is used to fetch record from the data source like table in disconnected mode.
* SqlDataAdapter is used to work with datasource in disconnected mode.
* Syntax of SqlDataAdapter

      SqlDataAdapter ObjectName=new SqlDataAdapter(command,ObjectOfConnectionClass);

Note: Syntax of SqlDataAdapter and SqlCommandClass is almost same.
* SqlDataAdapter works as a bridge between data source and virtual storage..
* It is used to connect data source to any virtual devices like DataTable, DataSet to Our Data Source.
  
a.Fill()
* Fill is a function of SqlDataAdapter class.
* It is used to fill the record of datasource to any virtual storage.
* Generally it used to insert queried data inside the virtual storage.
* Syntax :

      Object_Of_SqlDataAdapter.Fill();

Example :

    sq.Fill(Object_Of_DataTable/Object_Of_DataSet);
    OR
    sq,Fill(dt);

Notes: 
* SqlDataAdapter is used to work with database in disconnected mode.
* It is not required to open of close the database connectivity when we used SqlDataAdapter.
* Opening and closing of connectivity will be done automatically.
 
# 4. DataTable
* DataTable is a class that works like a virtual storage.
* It is located under "System.Data" namespace.
* DataTable is used to store the data and act as a virtual device.
* DataTable is a collection of multiple rows.
* Syntax of Creating Object of DataTable:

      DataTable dt=new DataTable();

Note: It have rows and columns property.



# 5. DataSet
* DataSet is a class that can be used as a virtual device.
* DataSet is collection of multiple tables.
* It is used to store Data in disconnected mode of connection.
* DataSet have Tables property to access the data of specific table.
* Syntax of DataSet

      DataSet ds=new DataSet();

Example :

    ds.Tables[0];









