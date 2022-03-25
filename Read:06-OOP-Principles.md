# Object Oriented Principles (OOP) :
 The primary characteristics of object-oriented programming :
 - Inheritance.
 - encapsulation.
 - polymorphism.
    
### Inheritance
enables you to create new classes that reuse, extend, and modify the behavior defined in other classes.

**base class** ==> The class whose members are inherited.

**derived class** ==> 
- the class that inherits those members.
- the derived class implicitly gains all the members of the base class except for its constructors and finalizers.
- The derived class reuses the code in the base class without having to reimplement it.
- You can add more members in the derived class.
- The derived class extends the functionality of the base class.

**direct base class** ==> A derived class can have only one direct base class.
---
  **Example**
  
  base class ==> Animal
  
  derived class ==> Mammal and Reptile.
  ![](./img/Animals.jpg)
  
  **Abstract and virtual methods**
  
  - When a base class declares a method as virtual, a derived class can override the method with its own implementation
  - If a base class declares a member as abstract, that method must be overridden in any non-abstract class that directly inherits from that class.
  - If a derived class is itself abstract, it inherits abstract members without implementing them. 
  ### Abstract
  - The abstract keyword enables you to create classes and class members that are incomplete and must be implemented in a derived class.
  (put the keyword abstract before the class definition).
  - An abstract class is one that CANNOT be instantiated. It's is meant to be a base for which to build off of, and not to be used alone.
  - if a member is abstract, the object that inherits it MUST implement it.
  
