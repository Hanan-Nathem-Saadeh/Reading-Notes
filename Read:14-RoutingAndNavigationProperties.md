# Read: 14 - Routing and Navigation Properties
# ASP.NET MVC Routing
- The ASP.NET Routing module is responsible for mapping incoming browser requests to particular MVC controller actions
- ASP.NET Routing is enabled in your application's Web configuration file (Web.config file)
- There are four sections in the configuration file that are relevant to routing: 
     - the system.web.httpModules section.
     - the system.web.httpHandlers section.
     - the system.webserver.modules section.
     - and the system.webserver.handlers section.
- a route table is created in the application's Global.asax file : which  is a special file that contains event handlers for ASP.NET application lifecycle events.

### Listing 1 - Global.asax.cs

![](./img/Listing1-Global.asax.cs.png)

- When an MVC application first starts, the Application_Start() method is called. This method, in turn, calls the RegisterRoutes() method. The RegisterRoutes() method creates the route table.
- The default route table contains a single route (named Default). The Default route maps the first segment of a URL to a controller name, the second segment of a URL to a controller action, and the third segment to a parameter named id.

**Imagine that you enter the following URL into your web browser's address bar:**

/Home/Index/3 ---> The Default route maps this URL to the following parameters:

- controller = Home

- action = Index

- id = 3

### Listing 2 - HomeController.cs

![](./img/Listing-HomeController.cs.png)

### Listing 3 - HomeController.cs (Index action with no parameter)

![](./img/listing3.png)

### Listing 4 - HomeController.cs (Index action with nullable parameter)

![](./img/Listing4.png)
### Listing 5 - HomeController.cs (Index action with Id parameter)
![](./img/listing5.png)

# Routing in ASP.NET Core
- Routing is responsible for matching incoming HTTP requests and dispatching those requests to the app's executable endpoints.
- Endpoints are the app's units of executable request-handling code.
- Endpoints are defined in the app and configured when the app starts.
- The endpoint matching process can extract values from the request's URL and provide those values for request processing.
- Apps can configure routing using:
      - Controllers
      - Razor Pages
      - SignalR
      - gRPC Services
      - Endpoint-enabled middleware such as Health Checks.
      - Delegates and lambdas registered with routing.
  - All ASP.NET Core templates include routing in the generated code. Routing is registered in the middleware pipeline in Startup.Configure.
  - Routing uses a pair of middleware, registered by UseRouting and UseEndpoints:
         - UseRouting adds route matching to the middleware pipeline. This middleware looks at the set of endpoints defined in the app, and selects the best match based on the request.
         - UseEndpoints adds endpoint execution to the middleware pipeline. It runs the delegate associated with the selected endpoint.
 - An ASP.NET Core endpoint is:
     - Executable: Has a RequestDelegate.
     - Extensible: Has a Metadata collection.
     - Selectable: Optionally, has routing information.
     - Enumerable: The collection of endpoints can be listed by retrieving the EndpointDataSource from DI.
