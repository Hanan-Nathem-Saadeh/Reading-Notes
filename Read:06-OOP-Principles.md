# Object Oriented Principles (OOP) :

![](./img/OOP.png)

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
  ### Polymorphism :
It is the ability for certain inherited traits to be changed or overridden by deriving classes. In our code, polymorphism is shown in the method sleep which is overridden and changed several times in different levels of inheritance.
### Object-Oriented programming (C#)
* Abstraction ==>  Modeling the relevant attributes and interactions of entities as classes to define an abstract representation of a system.
     - You used Abstraction when you defined classes for each of the different account types. Those classes described the behavior for that type of account.
* Encapsulation ==> Hiding the internal state and functionality of an object and only allowing access through a public set of functions.
     - You used Encapsulation when you kept many details private in each class.
* Inheritance ==> Ability to create new abstractions based on existing abstractions.
     - You used Inheritance when you leveraged the implementation already created in the BankAccount class to save code.
* Polymorphism ==> Ability to implement inherited properties or methods in different ways across multiple abstractions.
     - You used Polymorphism when you created virtual methods that derived classes could override to create specific behavior for that account type.



