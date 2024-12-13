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










