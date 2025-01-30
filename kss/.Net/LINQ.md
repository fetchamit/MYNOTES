# LINQ:

* linq (language integrated query) is a querying syntax integrated language into C# and .NET.
* provides a unified way to query various data source( e.g collection database, xml)
* eliminate the need for sql or othe rquery lang by embedding queries direcly  in C# COde

# History:
* introduse iu: .NET freamwork 3.5 and visual studio code 2008;
* creattor Anders hejsberg the arcthector of C#
* purpose: simplyfi data access and manipulation across deifferbt data type.

# Advantage:

* Unified query sentax
* type sefty and intellisence:
* improprove readability:
* reduse code coplaxity
* intgreation
* debugging and Maintenance

# Lambda Expreation

* A concise way to represent an anonymous function
* Used in linq for definding inline function or conditions
* Syntax:
    (parameter)=>expression_or_statemnt_block

* Example:
    x=>x%2==0(Lambda to filter even number)

* (=>) name is "goes to"

# syntax
* query syntax:
    from<variable>in<data_source>where<conditiopn>selet<result>;

* method syntax:

    data_source.where(x=> <condition>).select(x=> <result>);


# conclusion:

* linq is a power full feature for querying and manupulating data in c#;
* enhance productvity ,ensures compile-time safty and simplifies data operation.
* Lambda expretion make linq queries easy and relibale.


