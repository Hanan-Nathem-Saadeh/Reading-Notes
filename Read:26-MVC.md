# Read: 26 - MVC
## Azure DevOps:
- provides developer services for allowing teams to plan work, collaborate on code development, and build and deploy applications.
- supports a collaborative culture and set of processes that bring together developers, project managers, and contributors to develop software.
- It allows organizations to create and improve products at a faster pace than they can with traditional software development approaches.
- You can use one or more of the following standalone services based on your business needs:
      - Azure Repos provides Git repositories or Team Foundation Version Control (TFVC) for source control of your code. 
      - Azure Pipelines provides build and release services to support continuous integration and delivery of your applications.
      - Azure Boards delivers a suite of Agile tools to support planning and tracking work, code defects, and issues using Kanban and Scrum methods.
      - Azure Test Plans provides several tools to test your apps, including manual/exploratory testing and continuous testing.
      - Azure Artifacts allows teams to share packages such as Maven, npm, NuGet, and more from public and private sources and integrate package sharing into your pipelines.
- When you deploy Azure DevOps Server, you can also configure the following servers or integration points:
       - Build server supports on-premises and cloud-hosted builds.
       - SQL Server and SQL Analysis Server support SQL Server Reports and the ability to create Excel pivot charts based on the cube. 
# MVC
MVC is a design pattern or architecture which helps in developing the web application in a most efficient way when compared with the traditional ASP.NET Web Application.

## traditional ASP.NET web application VS MVC

| traditional ASP.NET web application      | MVC |
| ---------------------------------------------------- | --------------------------------- |
|  the user action and view (UI) are combined|the View only deals with UI of the page and the user actions are defined in Controller|
| follows the View based architecture which is not so efficient | action-based architecture. Based on the action, an appropriate View is displayed|
| the web page heavy which, in turn, makes the trips to server inefficient |  we don’t have View State to store the state information. |
| he response time of the web page is very high which is not user friendly. | the response time is very low|
| testing is tedious task as both View (UI) and Business logic (code behind) are tightly coupled | it enhances the test-driven development by making the UI and action logic loosely coupled |

##  MVC makes the design of the application into three layers namely Model, View, and Controller
1- Model layer represent the objects in our Application. Model is also a class which has all the objects and its properties and methods defined in it.

2- View Layer has all the html controls which define the UI of the application. Here in MVC, we don’t have drag and drop option for controls as we don’t use server controls. Instead we use Razor Engine available with Visual Studio by default which helps in rendering the View.

3- Controller basically handles the request from user. It is the heart of the MVC application as everyone say. It is responsible to handle the request and return a response to user by loading appropriate View with data from Model.

# Tag Helpers in ASP.NET Core

- Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files. For example, the built-in ImageTagHelper can append a version number to the image name.
- A rich IntelliSense environment for creating HTML and Razor markup.
- A way to make you more productive and able to produce more robust, reliable, and maintainable code using information only available on the server.

## Managing Tag Helper scope

### @addTagHelper
```
@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers
@addTagHelper *, AuthoringTagHelpers
```


