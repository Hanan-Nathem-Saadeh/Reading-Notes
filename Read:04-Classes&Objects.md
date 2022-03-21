# Classes & Memory Management

**class is a reference type.**
 At run time, when you declare a variable of a reference type, the variable contains the value null until :
 - create an instance of the class by using the new operator.==> MyClass myclass = new Myclass();
 - assign it an object of a compatible type that may have been created elsewhere.==> MyClass myclass2 = myclass;
  
**Declaring Classes:**
- class keyword followed by a unique identifier.
- The name of the class must be a valid C# identifier name
- Class body, where the behavior and data are defined. 
- Fields, properties, methods, and events on a class are collectively referred to as class members.
 public class Customer
{
   // Fields, properties, methods and events go here...
}

**Creating objects**

Customer object1 = new Customer();
- you can create an object reference without creating an object at all:
 Customer object2;
 
 **Class inheritance**
 
- When you create a class, you can inherit from any other class
- Done by using derivation
- If a Manager is Inheriting (Receiving all members of the base class except the constructor) from the class Employerr
public class Manager : Employee
{
    // Employee fields, properties, methods and events are inherited
    // New Manager fields, properties, methods and events go here...
}
## The constructor
is a method whose name is the same as the name of its type.

**Constructor syntax**

public class Person
{
   private string last;
   private string first;

   public Person(string lastName, string firstName)
   {
      last = lastName;
      first = firstName;
   }

   // Remaining implementation of Person class.
}

**If a constructor can be implemented as a single statement, you can use an expression body definition.**

 public Location(string name) => Name = name;
 
 **Static Constructors**
 
 A class or struct can also have a static constructor, which initializes static members of the type.
public class Adult : Person
{
   private static int minimumAge;

   public Adult(string lastName, string firstName) : base(lastName, firstName)
   { }

   static Adult()
   {
      minimumAge = 18;
   }
}
## Properties
- A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field.
-  Properties can be used as if they are public data members, but they are actually special methods called accessors. 
* get returns the property value
* set assigns a new value
* value is the keyword used to define the value being assigned by the set accessors.
* Backing fields cannot be directly set outside the object. Protects the values to ensure proper validation
* Property accessors often consist of single-line statements that just assign or return the result of an expression. You can implement these properties as expression-bodied members. Expression body definitions consist of the => symbol followed by the expression to assign to or retrieve from the property.

**Auto Implemented Properties**
- When properties just assign or retrieve a value.
- {get; set;}

## Stack
- Stack is more or less responsible for keeping track of what's executing in our code (or what's been "called").
- Value types are stored in the Stack.
- (FILO) -> First In Last Out.
## Heap
- Heap is responsible for keeping track of our objects.
- Reference Types are stored in the heap.
## Garbage Collection Fundamentals

**Benefits**

- The garbage collector provides the following benefits:
- Frees developers from having to manually release memory.
- Allocates objects on the managed heap efficiently.
- Provides memory safety by making sure that an object cannot use for itself the memory allocated for another object.

**Some Memory Fundamentals**

* Each process has its own, separate virtual address space. All processes on the same computer share the same physical memory and the page file, if there is one.
* Virtual memory can be in three states:
   - Free - The block of memory has no references to it and is available for allocation.
   - Reserved - The block of memory is available for your use and cannot be used for any other allocation request. However, you cannot store data to this memory block until it is committed.
   - Committed - The block of memory is assigned to physical storage.
   
**Memory Allocation**

- When you initialize a new process, the runtime reserves a contiguous region of address space for the process.
- Called the managed heap.
 
**Memory release**

- The garbage collector's optimizing engine determines the best time to perform a collection based on the allocations being made.
- When the garbage collector performs a collection, it releases the memory for objects that are no longer being used by the application.

**Garbage Collection**

- The system has low physical memory. This is detected by either the low memory notification from the OS or low memory as indicated by the host.
- The memory that's used by allocated objects on the managed heap surpasses an acceptable threshold. This threshold is continuously adjusted as the process runs.
- The GC.Collect method is called. In almost all cases, you don't have to call this method, because the garbage collector runs continuously. - This method is primarily used for unique situations and testing.
