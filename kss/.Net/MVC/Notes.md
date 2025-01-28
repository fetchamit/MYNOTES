# Introduction to ASP .NET MVC
-------------------------------
* ASP .NET MVC is a web application framework developed by Microsoft.
* ASP .NET MVC is a development framework for building web pages and web sites. MVC stands for `Model View Controller`.
* MVC is `Open-source` software design pattern.
* ASP .NET MVC framework is a lightweight, highly testable framework that is integrated with existing ASP.NET features.

## Creation of .NET MVC
* Inventor is 
* First official version 1.0, of ASP.NET MVC is released in 2009.
* Latest version of ASP.NET MVC is 5.2.8 that is released in year 2022.

## Features of ASP.NET MVC
* Separation of concern.
* Loosely Coupling.
* Parallel Development.
* Easy to perform unit testing.
* Test Driven Development (TDD) Support.
* Clean URLs.
* Improved Performance.
* More Controlling on HTML.
* Introduced new Concept
  * Filters
  * Web API
  * Scaffolding Template
  * LINQ etc
* Easy to learn and Task Support for Asynchronous Controllers.
* Bundling and Minification.


## Steps to create project of ASP.NET
1. Open Visual Studio and serarch for asp.net mvc template.
2. Now choose the template of "ASP.NET" web application (.NET Framework).
3. Then click Next button and enter the name of project, choose  project url and click on create button.
4. Then new interface will be open in which you need to choose empty application and check the MCV checkbox fromthe list of Add  project and core references 
5. At last click on create button to create new project in .NET MVC.

## Project Pattern and architecture after crating project
* Some important folder is already created when we create any new project like Model, Views, and Controller.
* In .NET we need to add controller of the project manually. There are no any controller is added previously.
* By default controller name is "Home" Controller.
* Note : MVC architecture is same as .NET CORE

## IsPost
*  IsPost is a property in .NET MVC that is used to know postback of a webpage.
*  When page directly comes from server it returns false or when it again goto server from the client, then IsPost returns true.
*  IsPost also returns when any user submit the form after clicking submit button.

## Now Sending data from view to controller
In .NET MVC, we majorly use three ways to send data from view to controller
1. Passing name of form control as action method parameter.                         [same as .NET CORE]
2. Passing object of FormCollection class as action method parameter.
3. Passing object of Model class as action method parameter.                        [same as .NET CORE]

### 2. Passing object of FormCollection class as action method parameter
* THis is one of the way to send data from view to controller.
* We passed object FormCollection inside the action method .
* This is used like key value pair.
* Type conversion is required to read data by using this method.

## To send data from controller to view we used below ways: 
1. ViewBag
2. ViewData
3. TempData
4. Strongly Type View

## Partial View in ASP.NET MVC
* This view works like a sub view or part of any main view.
* It not worked independently. This view is depend on our main View.
* We can use Partial view where some common parts/designing is required in main view pages.
* Generally we used parcial to add the code of markeup language or desinging part.
* One Partial view can be used in one or more than one view pages.

### Steps to create Partial View
* Generally we make partial views in shared folder. So right click on view folder and add a new folder having name `shared`.
* Then right click on shared folder and add view. During adding view you need to check the option of `Used this view as partial view.
* Then click Add/Create view.

### How to use partial in main view
* To use partial view in main we used two ways.

      @Html.Partial("Name_Of_Partial_View");
         OR
      @{Html.RenderPartial("Name_Of_Partial_View");}

## Adding Model in .NET MVC
1. Right click on Model Folder-> Add-> New Item
2. Then choose data from InstallItem(left side) -> ADO .NET Entity data model, then click on Add button.
3. Then choose `EF Designer from DB` option and click on next button.
4. Then click on `new connection ` button to add server setting and database related information.
5. A POP window will open where you need to add your server name, check on trust server certificate option and choose your required database, then click on ok button.
6. Now choose version of entity framework that you want to use and ckick on next button.
7. Then check the database object and click on `Finish` button.














