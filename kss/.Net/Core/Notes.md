# .NET Core
--------------

# Introduction to .NET Core
-----------------------------

* .NET Core is a new form of .NET Framework.
* It is free and open source software development framework.
* It is a cross-plateform framework that runs on Windows, macOS, and Linux operating systems.
* .NET Core framework can be used to build different types of applications such as mobile, desktop, web, cloud, IoT, Machine learning, microservices,game etc.
* .NET Core is totally different framework from .NET framework.

## Definition:
.NET Core is a cross-plateform, open-source framework developed by Microsoft for building modern, scalable, and high performance applications. It allows developers to create applications that run on Windows, macOS and Linux.

## Features of .NET Core
--------------------------
* Cross plateform, open source now runs your over linux, windows, Mac, that is wherever you want.
* Fast Development-fast work over the browsers.
* It is based on Model-View-Controller(MVC) architecture.
* Offers flexibility and scalibility to help developers write efficient, reusable and easy to maintain programming codes.
* Entity framework Core integration.
* Middleware architecture.

## .NET Core Advantages
* Free and Open source
* Secure
* Light Weight
* Increase Performance
* Cross Plateform
* Modern Framework

## ASP .NET MVC VS ASP.NET Core
* .NET MVC is old framework but .NET Core MVC is a modern framework.
* .NET MVC is not plateform independent but .NET Core MVC is plateform independent. Means .NET MVC applications can runs only in IIS Server and on a specific OS(Windows/Linux/Mac) but .NET Core applications can run in any web server and in any OS.
* .NET Core MVC is much flexible and modular than .NET MVC.
* .NET MVC framework is slow than .NET Core MVC.
* .NET MVC has not new version of .NET framework but .NET Core MVC has new version of .NET Core.

              User
                | => User interacting with view
              View
                |  => Request to controller and response
              Controller
                |  => Data from model to controller and controller to model
              Model
                |  => Data accessing from database and inserting data
              Database

## Creating first .NET Core WEb App
* Open Visual studio.
* Click on "Create a new project".
* Choose Language C#, All Plateform, All Project Type=>Web.
* Choose Template "ASP.NET Core Web App(MVC)" and click next.
* Give a desired name to your project and create it.

## Important Directories
1. Controller : Handles user requests and contains logic to interact with models and views.
2. Models : Represents the data structure and handles data logic.
3. Views : Contains HTML, CSS, and Razor syntax for rendering UI.
4. wwwroot : Holds static files like CSS, Javascript, and images.
5. Startup.cs : Configures application services and middleware.
6. appsettings.json : Stores configuration settings like connection string etc.

## What is MVC
* It stands for "Model View Controller".
* MVC is a design pattern that defines some rules to create a project. It decides a project in 3 main layers-
1. Model
2. View
3. Controller

* MVC is a framework that provides layered architecture to develop a project. That layers increases the security in project and also provides parallel development.

## Features of MVC
* Parallel Development
* Creates Secure Software
* Layered Architecture
* Loosely Coupling : Different layers can be linked easily
* Clean URL of pages
* Saves time and effort of a programmer
* TDD(Test Driven Development) Support : Software that are developed by using MVC framework; supports testing easily. Means we can test MVC based software easily.

# 1. View
* In MVC; V stands for View.
* View are GUI part of a MVC based project.
* Views are created inside "Views" folder in MVC.
* Views are directly accessible by the users.
* View pages can contains code of C# and HTML. Hence extension on View page is ".cshtml".
* View Pages are processed by a View Engine. View Engine is a Software that is capable to run code of C# and HTML at the same time. In .NET Core "Razor View Engine" is used to process our view pages.
* Types ot View pages in .NET Core
  1. General(Simple) View
  2. Partial View
  3. Layout View(Master View)
 

## Data Transfer from View to Controller in .NET Core MVC
* It is primary task to send data from a View page to controller so that we can perform some action or processing on that data.
* Below are the main paths that are used to send data from a view to controller-
  
  1. Traditional Approach
     * In this method we can fetch data of form controls by using the "Request.Form[]" array.
     * Syntax:

           VarName=Request.Form["KeyName"];
           
     * Note: Here keyname must have to match from a name of input field in view page.
     * In this method we have to perform type conversion forcefully. Because it returns data in string form.

  2. Passing name of form controls as action method parameter
     * This is also a method to send data of a view page to controller.
     * In this method we have to pass parameters in our action method to read the data aof view page.
     * Name of parameter of action method must be same as of form controls(input fields) in view page.
     * In this method we do not have to perform type conversion because it will be automatically performed.

  3. Passing Object of Model class as action method parameter
     * A model class is a special class that has functionality to perform database operations. It has some getters/ setters that are used to read and assign value to properties of class.
     * This is also a method to read data of a view page inside a controller.
     * In this method we have to create a model class with some poperties. In that case; name of properties of model class must be same as name of form controls.
     * This method is more preferred than passin gname of form controls as action method parameter. Because there is no need to pass a logn list of parameters in action method by using this method.
     * In this method type conversion is performed automatically.


# Razor block
* It is a block of code that is written in a View page.
* Razor block is used to write code of C# with in HTML page.
* We can use Razor block one or many times.
* Syntax:

      @{
         // C# code here
      }

# Controllers in .NET Core MVC
--------------------------------
* Controller is most important part of an MVC based application.
* In MVC; C stands for Controller.
* Controllers are created in form of a class.
* All controller classes must have to inherit a built-class that is "Controller".
* This built-in class is located under "Microsoft.AspNetCore.MVC.Controller" namespace.
* All controller classes must have to use "Controller" suffix in class name.
* Example : HomeController, AdminContrller, etc.
* A controller class is a collection of various types of methods.
* Methods of a controller class are known as "Controller methods".
* In .Net Core MVC; All Controllers are created inside "Controllers" folder.

## Controllers methods are two types:
1. Action Method
2. Non action Method

## 1. Action Method
* Action methods are used to process a HTTP request.
* Action methods are directly executable from a view page.
* That methods processes the request and generetes response for View page.
* Action methods must be public. It can not be private.
* Action method can not be a static method.
* We can have n number of action methods inside a controller.

* Types of Action method
  1. GET
  2. POST
  3. PUT
  4. DELETE

  Note: Generally there are two main types of action methods-
  1. GET
  2. POST

  # 1. GET Action Method
  * When a view page loaded directly from server then it processes a get action method.
  * When a user submits a form by using "GET" method in form tag; in that case also a GET action method executes.
  * Name of this action method must be same as name of View page.
  * Get Action method is default type of an action method or we can use [HttpGet] attribute to define an action method as a Get action method.
  * We can have parameters in action methods.

  # 2. POST Action Method
  * Post Action methods executes when a user submits the form by using "POST" method in form tag.
  * It is generally used to read and process the user entered data.
  * We have to define `[HttpPost]` attribute in post action method.
  * Name of get and post action methods must be same for a specific view. It means we have to `Overload` get and post action methods.
  * Note: All action methods have to perform some result to display in View page. There is a built-in class "ActionResult". The result is prepared in form of this class-`ActionResult` . But in `.NET Core` We have to return instance of `"IActionResult"` interface to implement more security in software. `IActionResult` interface works as parent of `"ActionResult"` class.
  * In needed; then we can return `"JsonResult,RedirectResult, ContentResult or FileResult etc.` from our action methods. These are also built-in classes and located inside parent-child hierarchy of `"ActionResult"` class.

# 2. Non-Action Method
* That methods are normal methods of C#.
* Non action methods are not directly accesible from View pages.
* We can use private, public, protected, etc access specifier before a non action methods as per our need.
* Non action methods can be static methods.
* That methods are normal UDF.
* We can use `[NonAction]` attribute before a non action method.
* we can have n numbers of non action methods in a controller.
* Non action methods are used by action methods to perform some tasks.

# Data Transfer from Controller(Action Method) to View
--------------------------------------------------------
* In .NET Core it is also an important task to transfer data from `controller to view`.
* Many of the times we have to display some data/result/ response to user in View Page after processing in action method.
* We have `4 below methods` to transfer some data from Controller to View.
  
      A. View Data
      B. View Bag
      C. Temp Data
      D. Strongly Typed View

## A. View Data
----------------
* View Data is a built-in object of `"ViewDataDicrionary"` class.
* It can store various data in Key/ Value pair.
* We can store any type of Data in ViewData but during reading data from a ViewData; We have to perform type conversion .
* Scope of View Data is one action method to one View page.

      Syntax:
      ViewData["KeyName"]=Value;
      Ex: ViewData["name"]="Ram Kumar";

## B. View Bag
---------------
* ViewBag is also an object of `ViewDataDictionary` class.
* It uses a dynamic expression to store and read data.
* We can store any type of data in ViewBag.
* There is no need to perform any type conversion in ViewBag.
* Scope of a ViewBag is from one action method to one View page.

      Syntax:
      ViewBag.DynamicExpression=Content/Value;
      Ex:
      ViewBag.msg="Welcome to .NET Core";

## C. TempData
---------------
* TempData is a built-in object of `TempDataDictionary`.
* TempData works in Key/Value pair.
* We can store any type of data in tempdata but during reading data from a TempData; we have to perform type conversion.
* Scope of a TempData is from one action method to one View page and also for the one next view page.

      Syntax:
      TempData["key"]=Value;
      Ex:
      TempData["name"]="Ramesh kumar";

Note: 
* It is only used to data in termporary format.
*  We can used tempdata to read data from it only one time after reading data from tempdata  it's value gets null.
* Similarly we can set the data from TempData only one time.
*  To access data in whole project we use conept of session variable.

## D. Strongly Typed View
--------------------------
* This is used to send data from controller to view.
* This is generally used to send data from controller to view of model specific data.
* To show data of model class in view page we used strongly type view.
* We should add below namespace to show the data in view page

      @using projectName.Models
      @model className
  
Example :

    @using Demo1.Models
    @model Customer


# .NET Core MVC Request Life Cycle
------------------------------------
* .NET Core request life cycle is a combination of various stages that are used to process a HTTP request.
* This life cycle begins from a HTTP Request and ends by generating and displaying the response to end user.
* Various stages of .NET Core Life cycle
1. Middleware
2. Routing
3. Controller Intialization
4. Action Method Execution
5. Result Execution
6. View Routing

## 1. Middleware 
* Middleware component forms the basic building block of an application.
* Middleware stage is a collection of few components that are combined to form  a request(requests).
* That component handles incomming requests.
* All HTTP request comes direct to this middleware; hence its role is very important.
* It Handles all request carefully and creates a log of all requests. This process is also known as request pipeline.

## 2. Routing
* Routing is a process to map an incomming HTTP request to specific responsible Controller and action method.
* It defines that where this request will be processed.

## 3. Controller Initialization
* Controllers are created as a class.
* So to execute/use a code of a controller we have to create object of that controller.
* The process of creating or initializing an object of a controller is called "Controller Initialization". In ASP.NET Core, This process is done automatically by the framework. When a request is made, the framework creates an instance of the controller class and invokes its constructor.

## 4. Action Method Execution
* In this code of specific action method will be executed as per the given conditions and code.
* If needed; then it can communicate with Models(database layer).
* It creates response to display in a View Page.

## 5. Result Execution
* During this stage generated response is executed and it will be prepared as HTTP response.
* This is a process of generating/converting response to HTML format.

## 6. View Rendering
* In this stage HTTP response will be displayed inside View page.
* Content of View page will be updated with new response.

        HTTP Request --> Middleware --> Routing --> Controller Initialzation
                                                                      |
        <--------------------------------------------------------------
        |                            
        --> Action method Execution --> Result Execution -->View Result --> View Rendering --> Response


# Models
----------
* In MVC, M stands for Model.
* In .NET Core Models folder is created automatically when we create any new project.
* Model is generally use and handle database command.
* We careate any class having getter setter property inside the Models folder.
* Getter and Setter property of any class is used to read and write the properties of a class.
* To Use Models data inside any view page or inside the controller we have to use below namespace that is -

      @using ProjectName.Models;

* Strongaly typed view is used to show data of model specific class.
* Model can not directly communicate with view or we can say model can not sent data to view directly, hence we used controller as a mediater to transfer the data of model to view or view to model.

# Master Page / Layout Page
------------------------------
* Master page is also known as Layout page.
* We can make Layout page inside the shared folder. However in .NET Core we do not need to make the shared folder manually because it will created automatically when we created any .NET Core project.
* Shared folder is located inside the views folder we used master page or layout page to write that part of the code that is common among all the pages .
* For Example generally menu, header and footer part is common to all pages. So we write these section in layout page.
* The view page that uses the layout or master page is known as child page.
* We need to use RenderBody() in layout page to render the child pages or to use child pages.
* The section we define RenderBody() method on that section child pages will be render or exist.
* In one layout page we can only one RenderBody(). We can not use multiple RenderBody() inside the single layout page.

## How to link pages by using Helper class
--------------------------------------------

      @Html.ActionLink("Text Name","Action Methods","Controller Name","Parameters",new{HTML Attributes});
      Example:
      @Html.ActionLink("Home","Index","Home",null,new{@class="nav-link active"})








