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


