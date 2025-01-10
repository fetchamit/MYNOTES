# Entity Framework Core with .NET Core 8
## Calling a stored procedure if result of procedure is not an Entity:
  1. If result of a Stored procedure does not of Entity type then we have to create a custom class inside Model folder and this class must contains all properties that match with the result of stored procedure.
  2. Add a property of your class in `DBContext.cs` file of your project as shown below-

         public virtual DBSet<Name_Of_Your_Class> PropertyName{get;set;}

     Ex:

         public virtual DbSet<ReferCodeGenerator> ReferCodeGenerators { get; set; }

  3. Add Settings related with class properties  in `OnModelCreating` function of `DBContext.cs` file of project.

  Ex:

      modelBuilder.Entity<ClassName>(entity=>
      {
        entity.HasNoKey();
      });

  4. Now you can call stored procedure inside your controller where needed by using below syntax-

         var VarName=Object_Of_DBContext_Class.Name_Of_EntityClass.FromSqlInterpolated(FormatterString).AsEnumberable().SingleOrDefault();

  Note: `FromSqlInterpolated()` function is used to call a procedure if result of procedure not belongs to an entity class.
  Ex:

      var ReferCode = db.ReferCodeGenerators.FromSqlInterpolated($"execsp_get_max_referral_code").AsEnumerable().SingleOrDefault();











