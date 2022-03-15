# Read: 01 - Exception Handling & Debugging
**Step through your code in debugging mode to find where the problem occurred**
- debugger actively monitors everything that’s happening as the program runs.
-  can pause the app at any point to examine its state.
**To start Debuging -> F5 (or the Debug > Start Debugging menu command or the Start Debugging button Start Debugging in the Debug Toolbar)**
**Set a breakpoint by clicking in the left margin next to a line of code. Or place the cursor on a line and press F9.**
## Steps to Create a sample app:

Open Visual Studio -> choose Create a new project-> Console App for .NET Core -> Choose Next -> Type a project name -> Next -> framework or .NET 5 -> Create .
---
# Exception handling
- is an important aspect of quality software development. When exception handling is not done well, it results in systems behaving unexpectedly or errors not being handled well. When exception handling is done well, it means that the system behave correctly even in abnormal situations.
-  Exeption -> handle errors that occur during execution in a consistent manner
**How to use the try/catch block:**
- Place any code statements that might raise or throw an exception in a try block, and place statements used to handle the exception or exceptions in one or more catch blocks below the try block. Each catch block includes the exception type and can contain additional statements needed to handle that exception type.
- try block followed by one or more catch clauses, which specify handlers for different exceptions.
```
example :- 

    public static void Main()
    {
        try
        {
            string s = null;
            ProcessString(s);
        }
        // Most specific:
        catch (ArgumentNullException e)
        {
            Console.WriteLine("{0} First exception caught.", e);
        }
        // Least specific:
        catch (Exception e)
        {
            Console.WriteLine("{0} Second exception caught.", e);
        }
    }
```
# Some of Common exceptions
* Exception	-> Base class for all exceptions.
* IndexOutOfRangeException -> Thrown by the runtime only when an array is indexed improperly.
* NullReferenceException -> Thrown by the runtime only when a null object is referenced.
* InvalidOperationException ->	Thrown by methods when in an invalid state.
* ArgumentException ->	Base class for all argument exceptions.
* ArgumentNullException	-> Thrown by methods that do not allow an argument to be null.
* ArgumentOutOfRangeException -> Thrown by methods that verify that arguments are in a given range.
