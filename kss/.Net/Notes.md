# Introduction to .NET
**********************
* Microsoft .NET is a plateform that is used to develope the computer software and applications.
* Developed by Microsoft Corporation in 2002.
* Latest Version is ".NET Framework 4.8.1" , released in 9 august 2022.
* Used to develop console, windows, web, mobile, web services based applications.
* NET supports multiple languages like as Visual C++, VB.NET, Visual C#, Visual J++, Python, Pascal, Perl and many more...

## Components of .NET Frameworks:
-------------------------------
* .NET Framework is developed based on two main components-
  1. Framework Class Library(FCL).
  2. Common Language Runtime(CLR).

### 1. Framework Class Library:
----------------------------
* Framework Class Library is a collection of various namespaces, classes, interfaces, and other user define types.
* It provides help to a developer in rapid development. Because it provides built-in functionality so a developer can use that code to develope software.
* Framework Class Library is very rich in term of functionality. .NET framework is easy to use and it is loved by the developers because FCL is just behind the .NET framework.
* FCL is also known as Base Class Library(BCL) or class library or Assembly.
* .NET has "System" namespace. This System namespace works as parent namespace for all libraries.

### 2. Common Language Runtime(CLR):
--------------------------------
* CLR works as a manager in .NET framework.It manages whole process of compilation and execution of code.
* CLR works as compiler in .NET Framework.
* CLR is most important part(component) of .Net Framework.
* CLR uses few below components to perform it's task:
  i. CTS (Common Type System)
  ii. CLS ( Common Language Specification)
  iii. JIT Compiler (Just-in Time)
  iv. Garbage Collector/ Carbage Collection

#### CTS:
--------
* It stands for Common Type System.
* It is used to generate a common data type for all the used languages.
* By creating common data type CTS helps CLR to generate common code for compilation and execution.
* It uses Language type rules to generate common data type.
* In .Net framework base data type is "object". This object data type can be categorized in two below categories-
    Data Type: (Object)
        i) Value Type : int, float, double etc.
        ii) Reference Type: string, object of classes, delegate, etc.

#### CLS:
--------
* It stands for Common Language Specifications.
* CLS is a set of rules that has specification (details) of language rule.
* CLS help CLR to generate common language code for all languages. That are supported by .Net framework.
* All .Net languages code is compiled in an intermediate code.

MSIL / IL : It stands for Microsoft Intermediate language/ Intermediate language. All .Net languages are converted into MSIL after the compilation. It is also known as CIL (Common Intermediate Language).

#### JIT:
-------
* Is is a small compiler that works just at the last movemnt of compilation.
* It coverts MSIL code into machine specific code(binary code).

#### Garbage Collector:
---------------------
* This component works for memory management. It automatically releases the unused or not required memory space time to time.
* It is automatically works to free the memory space. So that a programm can complete fast execution.

# Basic Introduction to C# :
---------------------------
## Histry :
--------
* Developed by Microsoft in 2000.
* Based on Java and C++, but has many additional extensions.
* Java and c# are both being updated to keep up with each other.
* Cross-development with Visual Basics, Visual C++, and many other .Net languages.

## Why to use C#:
---------------
* Pure Object Oriented Language.
* Power of C with ease of Microsoft Visual Basic.
* Easy to learn for everybody.
* Provides More support for Web development.
* More powerful like Java.
* Latest version is C#13, that is released in 2024.

## C# - The Big Ideas
**********************
### A component Oriented Language
#### The First "component oriented" language in the C/C++ family.
  * In OOP a Component is : A reusable program that can be combined with other components in the same system to form an application.
  * Example: a single button in a graphical user interface, a small interest calculator.
  * They can be deployed on different servers and communicate with each other.

#### Always use Main() unlike main() in C/C++.
#### Do not terminate class by semicolon.

# C# Overview :
---------------
* Object Oriented
* Everything belongs to a class
* Complete C# program-

  using System;
  namespace ConsoleTest
  {
    class Class1
    {
      static void Main(string[] args)
        {
        }
    }
  }

# C# Program Structure:
-----------------------
## Namespace
  * Contain types and other namespaces.
## Type Declaration
  * Classes, structs, interfaces, enums, and delegates.
## Members
  * Constants, fields, methods, properties, indexers, events, operators, constructors, destructors.

## Learning Strategy of C#
---------------------------
* Data Types
* Operators
* Console I/O
* Conditional Statements
* Loops
* Arrays
* Functions
* OOP's

## Data Type :
--------------
### Integer Types:
* byte, sbyte (8 bit), short (16 bit)
* int, uint(32 bit), long ulong(64 bit)

### Floating Point type
* float (precision of 7 digits)
* double (precision of 15-16 digits)

### Exact Numeric Type
* decimal (28 significant digits)

### Character type
* char (single characters)
* string (rich functionality, by reference type)

### Boolean type
* bool

## Console class and it's functions
* Provides methods for input and output
### Input
* Read (..) - reads a single characters.
* ReadLine(..) - reads a single line of characters.
### Output
* Write(..) - Prints the specified arguments on the console.
* WriteLine(..) - Prints specified data to the console and moves to the next line.
  
# Working with Directories and files in c#:
-------------------------------------------
* C# has a built-in namespace "System.IO" that is used to work with files and folders.
* Files are known as Directory in C#.
* Directory class works for folder and "File" class works for file.
* Directory.CreateDirecotry() function is used to create a new folder using C#.
* Directory.Exists() function is used to check that a folder exists or not.
* Directory.Delete() function is used to remove a folder.
* "FileInfo" class is used to get (read) all information about a file.

======================================
# Starting a System Process using C#
--------------------------------------
* "System.Diagnostics" is a namespace that provides us a class named as "Process". This process class is used to start a system process.
* Process.Start() function starts a process.
* We have to specify name of executable file of process to start a process.
* Ex: Process.start("mspaint.exe");

# Conditional Statements:
-------------------------
* Almost just like C/C++
* Note : It is mandetory that switch statement's default must contain break statement.

# Loops :
----------
i. For loop
ii. While loop
iii. do while loop
iv. for each loop

# Working with Date and Time in C#:
------------------------------------
* In C#, there is a "DateTime" class that is used to work with date and time.
* To get the current date and time we have to use "DateTime.Now". It will return current datetime is DateTime format.
* To Create the object of a specific date time we have to create object of DateTime class as shown below-
  *  DateTime ObjName=new DateTime(year,month,dayno);
  *  Ex: DateTime dt=new DateTime(1999,5,22);
* We can convert a value of any type in string format by using ".ToString()" function.

 # foreach loop :
 -------------------
 * For each is a loop in C# that is used to work with collections like string, array, array of objects etc.
 * For each loop works on the basis of items. It not works on index. It is an item based loop.
 * This loop is used to fetch each item from the collection one by one.
 * Syntax :
   foreach(varName in CollectionName)
   {
   // Statement
   }

 * Note: Here VarName must be a local variable of foreach loop. It is a read only variabl. VarName must be of type of a single item in collection.
 Ex:
string friends="Amar Mohan Suresh Mahesh";
foreach(char ch in friends)
{
Console.Write(ch);
}

# Implementing some delay in program:
--------------------------------------
* To mention some delay between execution of code we have to use "Sleep()" function of "Thread" class.
* Thread class is located under "System.Threading" namespace.
* Sleep() is a static method. We have to specify duration of delay in miliseconds.
* Ex: Thread.Sleep(4000);

# Array in C#:
---------------
* An arrya is a collection of same type of various data items.
* It is used to store bulk data.
* Array works on the basis of index.
* first index of an array is 0 and last index is size-1(length-1);
* C# provides "Length" property in array to find the number of items(size) of an array.
* Syntax to declare an array:
 ** Datatype [] ArrayName= new Datatype[size];
  ** Ex : int [] arr=new int[10];
* Syntax to declare and initialize an array:
* Datatype []ArrayName={item1,item2,.....};
* Ex: string [] name={"amit","vikas","satya",....};

## Array Class:
------------
* C# provides a built-in class with name "Array". This class provides us some functions to perform operations on an array.
* Sort(): This function is used to sort the items of an array in ascending order.
* BinarySearch(): This function is used to search an item in an array by using binary search algorithm.
* IndexOf(): This function is used to search item in an array by using linear search algorithm. It returns -1 if item not found otherwise it returns index of search item in array.

## 2D Array
----------
* Two diamentional array is used to store  data in matrix format.
* 2-D arra is used to store large amount of data.
* It stores data in pair of row, column index.
* Syntax to create a 2D array:
* Datatype [,]ArrayName=new Datatype[number_of_rows,number_of_columns];
* int [,]arr=new int[3,2];

  Note: Above array can store max 6 items.
* 2D array is also known as matrix. We have to use nested loop to process the 2D array.

# Strings in C#
--------------
* In C# string is a datatype and string is a class also.
* Ex: Datatype: string
* Ex: class : String
* String is a sequence(collection) of characters.
* Syntax to declare a string variable:
  
* String VarName;
* Ex: string name;

* Syntax to declare and initialize a string variable.
* string VarName="Value";
* Ex: string Name="Amit patel"

Note: In C# string is written inside double cotes.

## Some important properties and methods of String in C#
----------------------------------------------------------
1. Length: Used to find number of characters in a string.
2. ToUpper(): Used to convert a string into uppercase;
3. ToLowser(): Used to convert a string into lowercase.
4. Contains(): used to check a characters or word in given string. If found then it returns true ohterwise returns false.
5. IndexOf(): Used to find first occurance index of a character or word in a given string. If found then it returns index of that item; otherwise it returns -1.
6. LastIndexOf(): Used to find first occurance index of a character or word in a given string. If found then it returns index of that item; otherwise it returns -1.
7. Trim(): Used to remove whitespace from beginning and ending of string.
8. Substring(): Used to get part of a string(substring).
* Syntax1: StringVar.Substring(int StartIndex).
Note: It will provide a substring starting from the specified index and ending to length of main string.
* Syntax2: stringVar.Substring(int startIndex, int Length).
Note: It will provide fixed number of characters starting from the specified start index.
10. split(): Used to break a string into a array.
11. Insert(): Used to insert a string inside a string.
* StrName=FirstString.Insert(Index_from_to_insert_string,"String");

# Static functions
-------------------
* Static functions are special kind of functions in a class.
* If a function is of static type then it can use (call) only static members( variables) and static methods.
* It can not use any non-static members.
* Bydefault all members of a static function are static type.
* Default value of a static function is 0.
* Static functions of a class are called by using the class Name just before the function name.
* Ex: If student class have a static function having name "PrintData()". Then we can call it as given below :
* Student.PrintData();
* No Need to create a object of class for calling static method.
* Static functions can be loaded in memory directly without creating object of it's class.
* "static" is a store specifier. It preserve it's value during program execution. A static variable not losses it's value. static variables are allocated memory in the data segment; not is stack or heap. 


### Branching Statements
-------------------------
1. break:
* It is used to terminate the execution of current block.
* Generally it is used inside switch and loop statements.

2. continue:
* It is used to skip the current iteration of a loop.
* After skiping the current iteration it continues in next iteration.

# Object Oriented Programming
------------------------------
* Object Oriented programming is a concept of writing a computer program in modern way.
* It is a methodology to write computer programs.
* It is very famous and trustful method to write programs.
* "Object Oriented Programming is a methodology that uses concept of object to write computer programs."
* Object Oriented Programming tries to implement the real world human behavior in computer programs.
* Object Oriented Programming is a collection of some concept and when we use that concepts in our program then our program will be an object Oriented program. That concepts are also known as OOP's Concepts or Features of OOP's.
* The Languages that are providing support for concept of object oriented language; are known as Object Oriented Programming Languages(OOP's).
* Example of OOP's Languages are : C++, Java, PHP, C# etc.
* C# is pure object oriented programming language. It supports all concepts of OOP's. It strictly uses concepts of OOP's.

## Features of OOP's / Concepts of OOP's / Pillers of OOP's
-------------------------------------------------------------
1. class
2. Object
3. Data Encapsulation
4. Data Abstraction
5. Inheritance
6. Polymorphism
7. Message Passing

### 1. Class
* Class is a container.
* A class is a collection of various variables and various functions.
* In OOP's; variables of a class are known as " Data members" and functions of a class are known as "data methods". Hence " Class is a collection of various data members and various data methods in a single unit."
* Class provides security to data members and data methods.
* Class implements portability in our program. We can use a class easily from one program to another program also.
* Class provides reuseability to code. We can create object of a class many times.
* "class" keyword is used to create a class.
* Syntax:
  class <class_Name>
  {
    // Data members
    // Data methods
  }

### 2. Object 
---------------
* Object is a run time entity that is used to represent the features of a class. It means object exists in runtime in a program and by using object we can access the features of class.
* Object is a copy of class in memory. Means it is a copy of class that is loaded into memory.
* Object creation means memory initialization. It means when we creates object of a class that time memory will be allocated to all members of class.
* we can create n-numbers of object of a class as per need. All objects of a class takes seprate-seprate memory spaces.
 #### Syntax to create object of a class:
* <ClassName> ObjectName=new <ClassName>();
* Ex: Student s=new Student();

Note: Class is a userdefined datatype also.

### Constructor:
-----------------
* Constructor is a special member function of a class.
* Constructor is used to initialize the members of a class. Means we can assign/allocate some value to the members of a class by using constructor.
* We can perform any operation inside constructor but generally it is used to assign the member of class.

#### Characterics of Constructor
* Name of constructor must be same as name of class.
* Ex: For class Employee constructor name must be "Employee".
* No need to call a constructor function because it automatically executes when we create object of that class.
* A Constructor can not return any value. So need to specify any return type for constructor. Even "void" is also not allowed.
* It is recommended to make a constructor with public access.
* Because it will execute automatically when we create object of a class outside the class.
* A constructor can be type of static type. But it can not be a constant.
* Constructor can have parameters or it can be without any parameters.
* We can create multiple constructor in a class.

##### types of constructor
1. Parameterised/Default constructor
* A constructor that have no parameters is known as default constructor. It assigns default values to members of class.
  
2. Parameterised Constructor
* A Constructor having some parameter is known as parameterised constructor.
  
3. Copy Constructor
* A Constructor that has address of some members in parameter is known as copy constructor. It works on the basis of address of parameters. In C#; pointer is not supported in safe mode. Hence copy constructor is not generally used in C#.

### Destructor
---------------
* Destructor is used to destroy(free/release) memory space occupied of un-necessary variables and objects.
* It improves the performance of program/software.

### 3. Data Encapsulation
* Wrapping of data members and data methods in a single unit is known as "Data Encapsulation".
* Data Encapsulation makes portable to a program/class.
* "class" is used to implement data encapsulation.

### 4. Data Abstraction
* Data Abstraction is used to implement security in our program.
* "Data abstraction means data hiding". To provide only necessary information to the end user without providing details of internal functionality is known as "Data Abstraction".
* Data abstraction can be achieved by using two below concepts.
1. Access Specifiers.
2. Abstract Class.

#### 1. Access Specifiers :
---------------------------
* Access specifiers are used to define the access level or lifespan or programming elements.
* Access specifiers are used before variables, constants, classes,functions etc to define it's access level.
* Access specifiers are also known as access modifiers or protection level.
* In C#; We have 4 types of access specifiers.
A. Private:
* It is most Rectricted access specifiers.
* Private members / functions will be accessible only with-in the block where they are declared.

B. Protected:
* Protected is more usefull in parent-child relationship.
* Protected members of a class will be accessible inside the same class and also inside it's child class.
* Protected members are accessible from the child class located in same assembly and also from the child class located inside another assembly.

C. Public:
* Public is most flexible access specifier.
* Public members of a class will be accessible in whole program.

D. Internal:
* Internal access specifiers is of assembly level.
* Internal members can be accessed from any where in same assembly.

Note: Here assembly is a namespace or a collection of more than one namespaces.

2. Abstract Class:
* We will cover this topic later on after inheritance.


# Assemly:
==============

* an assembly is a collaction of naespace . we can put one or many namespace inside the assembly.
* assebly are also knowm as "class library" or DlL file.
* DlL atand for " Dynamic link library".
* dll is a read to use librtary  that can be dynamicly and quicly used u=in anothe rprogram.
* "Class Library" contain some code without any entry point.

### 5. Inheritence:
===================
* inheritence is the ability ton access the features of the class inside onther class.
* thae class that provides features is known as base class/ parent class/SUperclass/ main class.
* the class the uses features is known as derived class/ child class/sub class.
* inheritence is one of the most importent one of the most importent concept.
* it provide resusiblity of codes
* it is save time and effort of a progrmmer because it provide resusbility.
* in c#: colon symbole is used to inherit a class:

#### Syntanx to inherit the class:


        class <sub_class_name>: <super_class_name>
        {
            // data member...
            // data method....
        }

#### types of inheritence:
========================
* 1) single inheritence

            class-A
                ⬇
                ⬇
            class B

* 2) multi label inheritence

                class A
                    ⬇
                    ⬇
                Class B
                    ⬇
                    ⬇
                Class C
                    ⬇⬇
                    ⬇
                class D
* 3) hierarichal inheritence

                class A
                    |
            --------------------
            |                   |
            ⬇                 ⬇
          Class B            Class C


* 4) hybride inheritence

                 class A
                   ⬇
                   ⬇
                class B
                   ⬇
         ⬅⬅⬅⬅  ➡➡➡➡➡⤵
        ⬇                   ⬇
        ⬇                   ⬇
    class C               Class D


* note:- Multiple inheritence is not supprot in c#

## 6. Polymorphism
* Polymorphism means "One thing in many form".
* Poly means many and morphism means "form". Hence polymorphism means one thing in many form.
* We can use same function name for different-2 purpose by using Polymorphism. It makes easy to remember name of functions for a developer.
* Types of Polymorphism
A. Compile-time Polymorphism(Early Binding).
B. Run-time Polymorphism(Late Binding).

### A.Compile-time Polymorphism
* When a function call decides actual function during compilation process of programm then it is known as compile time polymorphism.
* Function Overloading is known as compile time polymorphism.

### B. Run time Polymorphism
* When a function call decides actual function during run time of programm then it is known as run time polymorphism.
* Function Overriding is known as Run time polymorphism.

### Function Overloading
* To define more than one function having same function name and different-2 signature(Syntax/parameters) is known as function overloading.
* All overloaded functions are defined in same class.
* We can overload a function in two below basis-
 A. On the basis of number of parameters.
 Ex: int Add(int num1,int num2)
     int Add(int num1,int num2,int num3)

 B. On the basis of type of parameters.
  Ex: void PrintMax(int num1,int num2);
      void PrintMax(float num1,float num2);

Note: We can not overload a function on the basis of it's return type.

### Function Overriding
* To define more than one function with same function name and same signature (syntax/ parameters) is known as function overriding.
* Function overriding is used to redefine(to give a new definition to a function of base class) a function of base class inside child class.
* By using function overriding a child class can change definition of function of base class as per need.
* To perform function overriding we need two classes - Parent and Child class.
* To make Overridable function we need to use a virtual or abstract function in base class.

#### Virtual Function
* Virtual functio is a specia function of a class. This function can be re-defined by it's child classes.
* "virtual" keyword is used to create a virtual function.
* Virtual function has a default definition in base class also.
* It is not mandatory for child classes to override virtual function of base class.
* It is optional for child class to override a virtual function of base class.
* To override a virtual function in child class we have to use "override" keyword.

## Abstract Function:
-------------------
* An Abstract funciton is a function of base class that have not any definition, it has declaration only.
* It is mandatory for child class to override abstract function of base class or child class can also be declared as an abstract class then it can deny(ignore) to override abstract function of base class.
* An Abstract is a function without definition in base class.
* Abstract function is created by using "abstract" keyword.
* We have to use "override" keyword in child class during function overriding.
* Syntax to create an abstract function -
  
      <access_specifier> abstract <return_type> FunctionName(list_of_parameters);

Note: Abstract functions are terminated by using semicolen in base class. It does not have any body.

* Abstract functions can be created within only abstract class.

## Abstract Class:
------------------
* An Abstract class is a collection of various abstract and non-abstract function.
* Abstract class is a special class. we can not instantiate an abstract class.
* We can't create object of an abstract class.
* Abstract class is only for inheritance.
* Data abstraction is used to implement data security(hiding) in program. We can achieve abstraction by using abstract class.Because this class can be used  only by it's child classes.
* "abstract" keyword is used to create an class abstract class.
* Syntax:
  
      <Access_Specifier> abstract class <ClassName>
      {
          // Data methods/ Abstract functions
          // Data members
      }

## Sealed Class
--------------
* Sealed class is a special class in C#.
* A Sealed class is a class that can not be inherited by any other class.
* A sealed class can't have any child class.
* "sealed" keyword is used to define a sealed class.

        Syntax:
          <access specifier> sealed class <Class Name>
          {
              // Data Members
              // Data methods
          }
  
### Abstract function VS Virtual function
----------------------------------------
1. Abstract function can be initialize by using "abstract" keyword and Virtual functions are initialize by using "virtual" keyword.
2. Abstract function can be initialize only and no need to define it's body in base class, But in other hand a virtual function can be initialize and define both in base class.
3. Abstract functions can be initialized only on abstract clsss and in case of Virtual function it is not mandetory to initialized only on abstract class.
4. An Abstract function can be strictly defined in child class but in case of virtual function it is not mandetory.
5. An Abstract function is terminated by using semicolen(;) and virtual function has no termination.
  
## Interface
-------------
* An interface is a complete abstract class.
* An interface is a special type that has only function declaration.
* Interface is a collection of various abstract methods. All the methods of interface are by default public and abstract. Also no need to write public and abstract keyword.
* In C# we can't declare a data member(variable) inside an interface.
* We can not create object of interface. It is used by child classes.
* Interface is used to implement some concept like multiple inheritance. We can inherit one class and multiple interfaces inside a child class.
* It is mandatory child class to define (Implement) all methods of an interface.
* "interface" keyword used to define an interface.

      Syntax :
      <Access_specifiers> interface <Interface_Name>{
        // Declaration of Abstract methods
        }

### Abstract Class VS Interface


## Random Class in C#
----------------------
* Random class in C# is used to random number, captcha, random foldername etc.
* Random class is belongs from "System" namespace.
* It is a class basically used to generate random number.
* Ex: We can use this class to generate OTP etc.
* Syntax to create Random class

      Random ObjectName=new Random();

* Random class have Next() function that is used to get number within the given range.
* Next function returns the int type of value.
* Example:

      Syntax :
      ObjectOfRandomclass.Next(MinValue,MaxValue);
      Example:
      Random rd=new Random();
      rd.Next(1,100);

## Delegate in C# :
* Delegate is a user defined datatype in C#.
* It is located inside "System" namespace.
* Delegate is a reference type variable.
* "Delegate is used to store address(reference) of a function."
* Delegate is a function pointer.
* Delegate can store address of a function that has same signature. So it is necessary to have same signature of delegate and corresponding function.
* Delegates are generally used to create event handlers(A code to handle events like as click, change, etc).
* Syntax to create a Delegate:

      <Access_Specifiers> delegate <Return_Type> DelegateName(List_Of_Parameters);

  Example :

      public delegate void Show(string msg);

Syntax to assign address of a function to a delegate:

      DelegateName ObjectName=new DelegateName(Name_Of_Function);
Example :

    Show s=new Show(test);

Syntax to call a function using delegate:

    ObjName_Of_Delegate(List_Of_arguments);
    Ex:s(45,32);
    
Note: Delegate is independent from Object. It can store address of functions of another class also.

# Exception Handling in C#:
----------------------------
## What is an Exception ?
* An exception is a run-time error.
* An exception is a run-time fault in our program code that was unexpected by the programmer/user.

## What is Exception handling ?
* Exception handling is a process to handle the exceptions.
* It is a process that is written or implemented by a programmer it it's code so that this code can work as an alternative code when an exceptions occurs in code.

* Exception handling is  a collections of few below blocks in C#.
  1. try block
  2. catch block
  3. finally block

## 1. Try block
* This block contains some code that can generate an exception.
* The code that have chances to occure some exception can be written in try block.

## 2. Catch block
* This block contains exception handling code.
* when an exceptin occurs inside code of try block then program control moves to catch block and executes code of catch block.
* We must have to define at-least one catch for a try block.
* We can define multiple catch block for a single try block to handle different-different types of exceptions.
* We can pass object of corresponding exception handling class in catch block to handle specific type of exception.
* Example :

      catch(IOException ex){
          //Exception handling code
      }
      catch(DivideByZero dz){
          // Exception handling code
      }

Note: "Exception" class is a base class for all type of exceptions. So we can catch all type of exceptions when we pass object of "Exception" class in catch block. It is optional to pass object of an exception handling class in catch block.

## 3. Finally block
* It is an optional block of exception handling code.
* It contains some common code that we want run or execute in all situations/conditions.
* Either an  Exception occurs or not; finally block executes it's code.
* Note: Exception handling is a process that continues alternate exception of our program so that suddenly execution will not stop.

# Collections in C#
* Collections are used to store multiple items.
* Collections are used to process large amount of data.
* Collections provides us features for data manipulation(Addition of data, deletion of data, Updation of data and displaying of data).
* Before C# 2.0; It was just collections. But now in C# there are two types of collections-
  1. Generic Collection
    * Generic collection works on the specific type of data as defined by the programmer.
    * List, IList, Dictionary, Stack, Queue
  
  2. Non-Generic Collection
    * Non-Generic Collections works on different types of data.
    * Generally it stores objects.
    * ArrayList, SortedList, Stack, Queue are non-geniric collection. 

# A) List
-----------
* List is  a class that works as collection.
* We can create any specific type of list by using List class.
* List has rich features for addition, updation, deletion, etc.
* Syntax to create a list

      List<Type> ObjectName=new List<Type>();

Example :

    List<string>lst=new List<string>();

# B) IList
-------------
* IList is an interface.
* It is a also a collection. It comes in both Category -Generic and Non-Generic.
* IList is used to fetch(Iterate) the items.
* IList provides only a readonly copy of items. It provides fast method to fetch the items.
* It does not have the methods to perform manipulation in Data.
* IList works as iterator to fetch data.
* It can store Object of a related class.
* Example:

      IList<string> lst=new List<string>();

# C) Dictionary
-----------------
* It is a generic collection .
* Dictionary is used to store items in key-value pair . We can findout values from the dictionary based on their keys.
* It provides fast way to search items from collection.
* Syntax:

      Dictionary<Key_type,Value_type> Object_name=new Dictionary<Key_type,Value_type>();
      Ex:
      Dictionary<int,string>stu=new Dictionary<int,string>();

Note: Dictionary is a collection of various objects of `KeyValuePair` structure.

* `TryGetValue()` is a function of Dictionary that is used to find / search a value in dictionary based on key.
* Example :

      string str = string.Empty;
      bool r=emp.TryGetValue(1011,out str);
      if(r==true)
          Console.WriteLine("Item found in dictionary. value is : "+str);
      else 
        Console.WriteLine("Item not found in Dictionary");

# D) Stack
-----------
* Stack is a also a collection.
* Stack can be generic and non-generic type also.
* It is used to store multiple items in LIFO(List in First Out) manner.
* Stack has `push()` ,`pop()` and `peek()` methods to perform sequantially data addition ,deletion and display.
* Syntax :

      Syntax of Non Generic stack:
      Stack ObjName=new Stack();
            Or
      Syntax of Generic stack :
      Stack<type> ObjName=new Stack<type>();

# E) Queue
------------
* Queue is also a collection.
* It is used to store multiple data.
* Queue is Generic and Non-Generic type both.
* We can display item of queue from beginning (start) by using the Peek() function.
* Queue is based on FIFO(First in First Out).
* Syntax of Non-Generic Queue:

      Queue ObjName=new Queue();
      Ex: Queue q=new Queue();

* Syntax of generic Queue

      Queue<Type> ObjectName=new Queue<Type>();
      Ex: Queue<int> nums=new Queue<int>();

Note: Queue has  a method `ToArray()` that is used to convert items of a Queue into an Array. `Enqueue()` method is used to add a new item in Queue. `Dequeue()` method is used to delete an item from a Queue.

# F) LinkedList
-----------------
* LinkedList is a collection of generic type.
* It is used to store multiple tiems.
* In C# this Linked List is internally a doubly Linked List.
* We can add and remove items from Linked List from both ends(start and end).

## Methods
1. AddFirst(): Used to add an item from beginning.
2. AddLast(): Used to add an Item from the end.
3. Remove(): Used to delete specific item from list.
4. Find(): Used to search an item in the list. It returns the search value.
5. Contains(): Used to check whether the given item is available in list or not.

## Properties
1. First.Value: Used to fetch(print) first value of the list.
2. Last.Value: Used to fetch(print) last value of the List.
3. Count: Used to find number of nodes(items) in the List.

Note:  If list is empty then `First` and `Last` properties will returns `null`.

      LinkedList<string> list = new LinkedList<string>();
      list.AddFirst("Satna");
      list.AddFirst("Agara");
      list.AddFirst("Jalaun");
      list.AddFirst("Prayagraj");
      if (list.Count > 0)
      {
        //var res=list.Remove("hello");     // returns false if item not found
        // var res = list.Find("hello");   // returns empty string if item not found
        // var res = list.Contains("satna");   // returns false if not found
        // Console.WriteLine(res);
        // Adding before an item on linked list
         LinkedListNode<string> mynode = list.Find("Agara");  // It finds the node 
         list.AddBefore(mynode, "Hello");
        
        foreach(string item in list)
      {
        Console.WriteLine(item);
      }

    }
    else
      {
        Console.WriteLine("List is Empty");
    }


# G) ArrayList
---------------
* ArrayList is a non-generic collection.
* It is like Array but it has more functionality to manipulate data.

      Syntax :
      ArrayList ObjName=new ArrayList();
      Ex :
      ArrayList mylist=new ArrayList();

Note: Unlike array we can store any type of data in an ArrayList.

# H) SortedList
----------------
* SortedList can be generic and non-generic both type of collection.
* It works on Key/value pair and store bulk records.
* SortedList automatically sorts the items in ascending order.
* It also has method to manipulate data easily.
* Syntax :

      SortedList ObjectName=new SortedList();
      Ex :
      SortedList sl=new SortedList();

Adding item in sorted list:

    ObjectName.Add("Key","Value");
    Ex: sl.Add(45,"Ramesh");

Note: It sorts the item based on Keys.


# I) IEnumberable

* Ienumberable is an interface that is located under "System.Collections.Generic" namespace. So it can be considerd as generic collection but remember that it is not a class.
* IEnumberable works as enumerator so it is very good to fetch data.
* IEnumberable is good for accessing data form the object in memory(means objects that are loaded in memory(RAM) right now) Ex: List,Array, Array of Object etc.
* IEnumberable is best when we have to access data in objects from LINQ.
* While executing a select command in a database using IEnumberable then it executes that command at server side and loads response in memory and executes filter at client side.
* As it is an interface so we can not create it's object; We have to assign object of a class that is available in IEnumberable hierarchy.
* Syntax:

      IEnumberable<Type> InstanceName=Object;

Ex:

    IEnumerable<int> x=new List<int>();

Note: IEnumberable has a function `MoveNext()` that is used to fetch next item from enumerator and It also has a property `Current` that is used to get current item from enumerator.

# J) IQuerable 
* IQuerable is also an interface.
* It is located under `System.Linq` namespace.
* IQuerable is also used to iterate data.
* IQuerable is good for accessing out memory data. Means it is good for accessing data from a remote database, Web api, Any external service etc.
* IQuerable is used for transfering data from LINQ to SQL.
* When we execute a select command in database using IQuerable then it executes select command at server side with all given filters then loades data into memory.
* Syntax :

      IQuerable<Type> InstanceName=ObjectName;

Example:

      IQuerable<string> str=new List<string>();




