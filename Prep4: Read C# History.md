# The history of C#
- C# is an object-oriented language. It supports all the good old features of Java's objects.
- C# has support for functional programming in the form of lambdas and immutable types.
- C# is strongly typed! You can't just add a float to an integer unless you explicitly do some form of casting.
- Each version may add new requirements
Last 2 versions :
### C# version 9
C# 9 was released with .NET 5. It's the default language version for any assembly that targets the .NET 5 release. some new features:
- Records.
- Top-level statements.
- Support for code generators
        *Module initializers
        *New features for partial methods
### C# version 10
C# 10 adds the following features:
- Record structs
- global using directives
- Extended property patterns
- Improved definite assignment
 # (Tooling):-
### What is .NET ? 
.NET is an open-source developer platform for building different types of apps.
- use multiple languages, editors, and libraries to build for web, mobile, desktop, games….
-	write .NET apps in C#, F#, or Visual Basic.
-	create .NET apps for many operating systems, including Windows, macOS, Linux, Android, iOS, tvOS, watchOS.
### Managed code 
code whose execution is managed by a runtime and written in one of over twenty high-level programming languages that are available for use with the Microsoft .NET Framework, including C#, J#, Microsoft Visual Basic .NET, .....
- it helps to avoid many typical programming mistakes that lead to security holes and unstable applications.
###	CLR (Common Language Runtime)
it is basic and Virtual Machine component of the .NET Framework.it runs the codes and helps in making the development process easier by providing the various services.
---
# C# Language :
## some of Value types
- Signed integral: sbyte, short, int, long
- Unsigned integral: byte, ushort, uint, ulong
- Unicode characters: char, which represents a UTF-16 code unit
- IEEE binary floating-point: float, double
- High-precision decimal floating-point: decimal
- Boolean: bool.
## Enum types
- enum E {...}. An enum type is a distinct type with named constants. Every enum type has an underlying type, which must be one of the eight integral types. The set of values of an enum type is the same as the set of values of the underlying type.
## Interface types
User-defined types of the form interface I {...}
## Array types
Single-dimensional, multi-dimensional, and jagged. For example: int[], int[,], and int[][]
## Delegate types
User-defined types of the form delegate int D(...)
---
# Arrays :
-  int[] array1 = new int[5];
- int[] array2 = new int[] { 1, 3, 5, 7, 9 };
- int[,] multiDimensionalArray2 = { { 1, 2, 3 }, { 4, 5, 6 } };
