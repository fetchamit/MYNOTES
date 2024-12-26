# Entity Framework Core
-------------------------
* `Entity Framework Core(EF Core)` is a cross-plateform `ORM` developed by Microsoft for .NET Core and .NET Framework.
* ORM stands for `Object Relational Mapping`. It helps to speed up application development and saves a lot of time to the developers.
* EF Core is used to perform all `database` operations easily. EF Core will generate all required classes to perform CRUD Operations.

## Key Features of EF Core
* Compatible with .NET Core, making it ideal for modern, plateform-independent applications.
* Provides support for `LINQ(Language Integrated Query)`, Allowing developers to query data in a secure manner.
* Tracks changes made to objects and ensures that only modified data is updated in the database.
* Supports various database systems, such as SQL Server, PostgreSQL, MySQL, SQLite, and more..

# Requirement and Setup
* To work with EF Core install below dependencies by going inside Nuget package manager.
  * Core Library for EF

        Install-Package Microsoft.EntityFrameworkCore
  * SQL Server-specific EF Provider

        Install-Package Microsoft.EntityFrameworkCore.SqlServer

  * Tools for migration and scaffolding

        Install-Package Microsoft.EntityFrameworkCore.Tools

  * For design-time operations like scaffolding

        Install-Package Microsoft.EntityFrameworkCore.Design

* EF Core Set up
  * Specify connection strins in appsettings.json

        "ConnectionStrings":{
          "DefaultConnection":"Data Source=localhost;Initial Catalog=KSSDB; Integrated Security=True;"
        }

* Register EF Core services in Program.cs

      services.AddDbContext<ApplicationDbContext>(options=>options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));

* Generate Model by using Scaffolding Command

      Scaffold-DbContext "Data Source=AMIT-PATEL\SQLEXPRESS02; Initial Catalog=EntityDemo; Integrated Security=True; TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models


* Generating Model by using Scaffolding Command to update it from Project

      scaffold-DbContext"Data Source=localhost;Initial Catalog=KSSDB;Integrated Security=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer-OutputDir Models - Force

## Functions in EF Core
Some Important functions to perform database operations in EF Core with Database are given below-

* To add / insert a new record `Add()`
* To show / display all record `ToList()`
* To delee a record `Remove()`
* To display a single record based on PK `Find()`
* To display a single record based on Conditions `SingleOrDefault()`
* To update a record `Entry()`
* After modification in database we have to call a function to save changes in data base `SaveChanges()`









