# Session
------------
* Session is a state management mechanism.
* Session is a global variable that is used to store user specific data.
* Session takes memory in `server side`.
* Session can store different-differents data for differents users.
* Default time of session is `20 minuts` in .NET Core but user can adjust is accordingly. Each session request again set it for next 20 minutes.

## Setting Up Session in .NET Core 6
* In Previous versions of .NET Core there was a `startup.cs` file. This file was used to do settings of sessions. But in new versions of .NET Core `6.0` there is no `startup.cs` file so we have to write all settings inside `Program.cs` file by creating a method and then enable the session inside main() function.
* In `Program.cs` create a function with name `ConfigureServices` having parameter `IServiceCollection`.
* Inside this function use methods `AddDistributedMemory()`, `AddSessions()` , `AddMVC()`.
* Now Call this function from main function-

      Ex : ConfigurationServices(builder.services);

* The session is ready and before using it in program we have to enable it for that use below inside main()-

      app.UseSession();

## Setting UP Session in .NET Core 8.0
* In .NET Core 8 Project there is no main function inside `Program.cs`  file.
* Sessions are easy in .NET Core 8. Just follow below steps-
  1. Add Session inside `Program.cs` file by writing below line before `var app = builder.Build();`
 
          builder.Services.AddSession();
    * Note: If you want to define custom time for session timeout then you can use below line as shown below-

          builder.Services.AddSession(x=>x.IdleTimeout=TimeSpan.FromMinutes(10));

  2. Add Below line in `Program.cs` to enable use of session in whole project-

         app.UseSession();

  Note: This line must be added after below line-

        var app = builder.Build();

## Creating and Using Session in .NET Core
* Syntax to create a session Variable:

      HttpContext.Session.SetString("KeyName", "Value");
        OR
      HttpContext.Session.SetInt32("KeyName","KeyValue");

* Syntax to read value of a Session :

      String VarName=HttpContext.Session.GetString("keyName");
      OR
      int VarName=HttpContext.Session.GetInt32("KeyName");

* Example:

      HttpContext.Session.SetString("Name","Amit Patel");
      string str=HttpContext.Session.Getstring("Name");

## Important Facts about Session
* Session is accessible in whole project.
* Session is a heavy weight variable. So it is recomended to not create more sessions in a project.
* Session is generally used in login/logout process to maintain state of current user.
* To remove a specific session variable we have to use `Remove()` function and to remove all session variables we have to use `Clear()` function.

      HttpContext.Session.Remove("KeyName);
      HttpContext.Session.Clear();    





