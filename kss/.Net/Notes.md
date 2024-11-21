Introduction to .NET
**********************
=> Microsoft .NET is a plateform that is used to develope the computer software and applications.
=> Developed by Microsoft Corporation in 2002.
=> Latest Version is ".NET Framework 4.8.1" , released in 9 august 2022.
=> Used to develop console, windows, web, mobile, web services based applications.
=> >NET supports multiple languages like as Visual C++, VB.NET, Visual C#, Visual J++, Python, Pascal, Perl and many more...

Components of .NET Frameworks:
-------------------------------
=> .NET Framework is developed based on two main components-
  1) Framework Class Library(FCL).
  2) Common Language Runtime(CLR).

1) Framework Class Library:
----------------------------
=> Framework Class Library is a collection of various namespaces, classes, interfaces, and other user define types.
=> It provides help to a developer in rapid development. Because it provides built-in functionality so a developer can use that code to develope software.
=> Framework Class Library is very rich in term of functionality. .NET framework is easy to use and it is loved by the developers because FCL is just behind the .NET framework.
=> FCL is also known as Base Class Library(BCL) or class library or Assembly.
=> .NET has "System" namespace. This System namespace works as parent namespace for all libraries.

2) Common Language Runtime(CLR):
--------------------------------
=> CLR works as a manager in .NET framework.It manages whole process of compilation and execution of code.
=> CLR works as compiler in .NET Framework.
=> CLR is most important part(component) of .Net Framework.
=> CLR uses few below components to perform it's task:
  a) CTS (Common Type System)
  b) CLS ( Common Language Specification)
  c) JIT Compiler (Just-in Time)
  d) Garbage Collector/ Carbage Collection

a) CTS:
--------
=> It stands for Common Type System.
=> It is used to generate a common data type for all the used languages.
=> By creating common data type CTS helps CLR to generate common code for compilation and execution.
=> It uses Language type rules to generate common data type.
=> In .Net framework base data type is "object". This object data type can be categorized in two below categories-
    Data Type: (Object)
        i) Value Type : int, float, double etc.
        ii) Reference Type: string, object of classes, delegate, etc.

b) CLS:
--------
=> It stands for Common Language Specifications.
=> CLS is a set of rules that has specification (details) of language rule.
=> CLS help CLR to generate common language code for all languages. That are supported by .Net framework.
=> All .Net languages code is compiled in an intermediate code.

MSIL / IL : It stands for Microsoft Intermediate language/ Intermediate language. All .Net languages are converted into MSIL after the compilation. It is also known as CIL (Common Intermediate Language).

c) JIT:
-------
=> Is is a small compiler that works just at the last movemnt of compilation.
=> It coverts MSIL code into machine specific code(binary code).

d) Garbage Collector:
---------------------
=> This component works for memory management. It automatically releases the unused or not required memory space time to time.
=> It is automatically works to free the memory space. So that a programm can complete fast execution.

Basic Introduction to C# :
---------------------------
Histry :
--------
=> Developed by Microsoft in 2000.
=> Based on Java and C++, but has many additional extensions.
=> Java and c# are both being updated to keep up with each other.
=> Cross-development with Visual Basics, Visual C++, and many other .Net languages.

Why to use C#:
---------------
=> Pure Object Oriented Language.
=> Power of C with ease of Microsoft Visual Basic.
=> Easy to learn for everybody.
=> Provides More support for Web development.
=> More powerful like Java.
=> Latest version is C#13, that is released in 2024.

C# - The Big Ideas
*******************
# A component Oriented Language
=> The First "component oriented" language in the C/C++ family.
  * In OOP a Component is : A reusable program that can be combined with other components in the same system to form an application.
  * Example: a single button in a graphical user interface, a small interest calculator.
  * They can be deployed on different servers and communicate with each other.

=> Always use Main() unlike main() in C/C++.
=> Do not terminate class by semicolon.

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









