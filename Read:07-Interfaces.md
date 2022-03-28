# Notes for Read 07 - Interfaces

## Interfaces
[Microsoft Docs - Interfaces](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/interfaces/)

Interfaces are like abstract classes.  They only contain abstract elements and any class that implements them **MUST** use all thier members.
Again Like abstract classes, they can't be instantiated.

Classes can use multiple interfaces, but as we know cannot inherit from more than one interface.

## Back to Basics - What is an Interface?

[Simple Programmer - What is an interface?](https://simpleprogrammer.com/back-to-basics-what-is-an-interface/)

An **interface** allows multiples classes to it.  It is a contract with the class that wants to interface from it. 
It can use the interface IF it uses all of it's members.  
The example given is that a Driver class should not have to have a:
+ DriveBoat()
+ DriveCar()
+ DriveGoKart()

They are all basically using the same set of skills to drive them.  So a **Driver** *class* should have a **Drive** *interface*
to handle all of the general driving instructions.

**Not sure I understand Dependency Injection**

## Keyword Interface

+ Interface cannot be instantiated.
+ You can have also had a body, to provide some defaults to the class that is using the interface.
+ An interface can inherit from MULTIPLE other interfaces.
+ 
[Microsoft Docs - interface keyword](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/interface);

[&lt;--&#91;BACK&#93;](/README.md)
