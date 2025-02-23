Note: If you wants to run anoter person's project in your system then please remove connection string from Web.config file and also remove model from model folder it will looks like "model1.edmx".

After that follow these steps.


------------------------- Steps to connect with database usign Entity Framework in ASP.NET MVC ------------------
Step 1:
Right click on Models folder and choose new item > Then under C# section click on Data section> Choose ADO.NET Entity Data Model and click on Add.
Step 2:
On Next Window choose EF designer from Database. And click next.

Step 3: Click on New Connection
Ensure that in Data Source section "Microsoft SQL Server (SqlClient)" is selected.
Copy servername and paste on servername seciton like "AMIT-PATEL\SQLEXPRESS02".

Check the checkbox of Trust server Certificate.

Choose Database name and click on ok

Step 4: 
You have to visible your connection string on next window if not please connect your database again. and click on next button.

Step 5: Choose Entity Framework 6.x and click on next.

Step 6: check the checkbox of tables and click on finish button.

Note : your model has been created and linked with database.

Now you will see the table schema and do not forgot to save this by pressing Ctrl + s otherwise you will not be able to use it in your application.

Under the model folder go to like that

model1.edmx > model1.context.tt > model1.Context.cs

Copy the class name and make object to interact with database.

Note: If any updates in database tables then you have to delete the model1.edmx file and after that goto Web.config file in your project then remore connection string which is visible you like this

 <add name="EntityDemoEntities" connectionString="metadata=res:///Models.Model1.csdl|res:///Models.Model1.ssdl|res://*/Models.Model1.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=AMIT-PATEL\SQLEXPRESS02;initial catalog=EntityDemo;integrated security=True;trustservercertificate=True;MultipleActiveResultSets=True;App=EntityFramework&quot;" providerName="System.Data.EntityClient" />
 
 After that add new model.
