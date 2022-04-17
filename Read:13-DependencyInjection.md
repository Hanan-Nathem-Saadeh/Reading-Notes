# Readings: Dependency Injection & Repository Design Pattern

![](./img/Depandancy1.jpg)

## dependency injection (DI) 
- software design pattern, which is a technique for achieving Inversion of Control (IoC) between classes and their dependencies.
- A dependency is an object that another object depends on.
- A class can create an instance of the MyDependency class to make use of its WriteMessage method. 
- Example of adding interface dependency
services.AddScoped<IMyDependency, MyDependency>();
- By using the DI pattern, the controller or Razor Page:
    - Doesn't use the concrete type MyDependency, only the IMyDependency interface it implements. That makes it easy to change the implementation without modifying the controller or Razor Page.
    - Doesn't create an instance of MyDependency, it's created by the DI container.
 -  Each requested dependency in turn requests its own dependencies.
 - The container resolves the dependencies in the graph and returns the fully resolved service.
 - The collective set of dependencies that must be resolved is typically referred to as a dependency tree, dependency graph, or object graph.
 ## Service lifetimes
To use scoped services in middleware, use one of the following approaches:
   - Inject the service into the middleware's Invoke or InvokeAsync method. Using constructor injection throws a runtime exception because it forces the scoped service to behave like a singleton. 
   - Use Factory-based middleware. Middleware registered using this approach is activated per client request (connection), which allows scoped services to be injected into the middleware's constructor.
   ## The Repository pattern
