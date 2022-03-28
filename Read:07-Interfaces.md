# Interfaces
- An interface contains definitions for a group of related functionalities that a non-abstract class or a struct must implement.
- An interface may define static methods, which must have an implementation.
- an interface may define a default implementation for members.
- An interface may not declare instance data such as fields, auto-implemented properties, or property-like events.
- you must use an interface if you want to simulate inheritance for structs, because they can't actually inherit from another struct or class.
```
Interfaces are like abstract classes.  They only contain abstract elements and any class that implements them MUST 
use all thier members. Again Like abstract classes, they can't be instantiated.
Classes can use multiple interfaces, but as we know cannot inherit from more than one interface.
```
