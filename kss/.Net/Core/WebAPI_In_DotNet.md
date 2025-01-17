# Introduction to WEB API
-----------------------
* API stands for `Application Programming Interface`.
* Web API is an `API` over the web which can be accessed using `HTTP Protocol`.
* Web API is a `concept` and not a technology.
* A Web API is an application porgramming interface for web.
* Web API is a method to access data and workflow from an application without using the application itself.
* API is a set of `subroutine definition (Function definitions), protocols and tools for building software and applications`.

## Definition of API
` API is actually some kind of interface which is having a set of functions. These set of functions will allow programmers to acquire some specific features or the data of an application.`

## Concepts of WEB API

    Web Application           _____    Http Request------>                                _________
    Mobile Application        _____|____________________________________________________ | WEB API |
    Win form Application      _____|   <----Http Response Data(Json,XML,Other format)    |_________|

## Advantages  of API
* Reusable: Multiple users and apps can easily use and reuse.
* Secure : Need permission authentication to access.
* Increase performance: Fast Execution.
* Plateform Independent : API are plateform independent. We can use it in any OS.
* Uses HTTP : No any additional protocol needed. It uses HTTP.
* Content Negoatiation: Default support for JSON and XML client can negoatiate about format.

## What is REST API
* REST stands for `REpresentational State Transfer`.
* REST is an architectural style that defines a set of constraints to be used for creating web services. In other words, REST is a specific web architecture model.
* REST API is a way of accessing web services in a simple and flexible way without having any processing.
* In HTTP there are five methods that are commonly used in a REST-based Architecture that is `POST, GET, PUT, PATCH and DELETE`. These correspond to `create, read, update, and delete or(CRUD)` operations respectively.
  
## WEB API Controllers
* A controller class handles HTTP Requests.
  * Web API controllers derive from ApiController.
  * ASP.NET Web API by default maps HTTP requests to specific methods called `actions`.

* Get a list of all posts
  * Http Method : `GET`.
  * Relative URI : `/api/posts`
  * Method : `Get()`

* Get a post by Id
  * Http Method : `GET`.
  * Relative URI : `/api/posts/id`.
  * Method : `Get(int id)`

* Create a new post
  * Http Method : `POST`.
  * Relative URI : `/api/posts`
  * Method : `Post(PostModel value)`.

* Update a post
  * Http Method : `PUT`.
  * Relative URI : `/api/posts/id`
  * Method : `Put(int id,PostMethod value)`

* Delete a post
  * Http Method : `DELETE`.
  * Relative URI : `/api/posts/id`
  * Method : `Delete(int id)`

* Get a post by Category
  * Http Method : `GET`.
  * Relative URI : `/api/posts?category=news`
  * Method : `Get(string category)`

## Limitations of API
* Complexity : API's can be comlex, It need more efforts.
* Security concerns: Need to do more care about security from hackers.
* Web Connections : After creation, client needs internet connection always.










