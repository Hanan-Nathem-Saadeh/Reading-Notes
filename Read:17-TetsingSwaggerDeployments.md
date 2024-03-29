# Read: 17 - Tetsing, Swagger, Deployments

![](./img/Swager.png)

# Swagger (OpenAPI)
- is a language-agnostic specification for describing REST APIs. 
-  It allows both computers and humans to understand the capabilities of a REST API without direct access to the source code.
-  Its main goals are to:
        - Minimize the amount of work needed to connect decoupled services.
        - Reduce the amount of time needed to accurately document a service.
- "Swagger" refers to the family of open-source and commercial products from SmartBear that work with the OpenAPI Specification. 
- offers a web-based UI that provides information about the service, using the generated OpenAPI specification.
- Both Swashbuckle and NSwag include an embedded version of Swagger UI.
- Each public action method in your controllers can be tested from the UI

# Unit Testing

## Creating the Controller under Test

- The ProductController Class that we want to test :

     public class ProductController : Controller
     
     {
          public ActionResult Index()
          
          {
          
               // Add action logic here
               
               throw new NotImplementedException();
               
          }
          

          public ActionResult Details(int Id)
          
          {

               return View("Details");
               
          }}
          
- ProductControllerTest.cs

 [TestClass]
 
     public class ProductControllerTest
     
          [TestMethod]
          
          public void TestDetailsView()
          
          {
               var controller = new ProductController();
               
               var result = controller.Details(2) as ViewResult;
               
               Assert.AreEqual("Details", result.ViewName);}}
               
               }
               
   - The goal is to demonstrate how you can write unit tests for the controllers in your ASP.NET MVC applications.
     
   - build three different types of unit tests:
     
          - You learn how to test the view returned by a controller action
          - how to test the View Data returned by a controller action.
          - and how to test whether or not one controller action redirects you to a second controller action.

# Unit tests of controller logic

- When unit testing controller logic, only the contents of a single action are tested, not the behavior of its dependencies or of the framework itself.
-  A controller unit test avoids scenarios such as filters, routing, and model binding. 
-  If you're writing custom filters and routes, unit test them in isolation, not as part of tests on a particular controller action.
-  The preceding controller:
    - Follows the Explicit Dependencies Principle.
    - Expects dependency injection (DI) to provide an instance of IBrainstormSessionRepository.
    - Can be tested with a mocked IBrainstormSessionRepository service using a mock object framework, such as Moq. 
    - A mocked object is a fabricated object with a predetermined set of property and method behaviors used for testing.

