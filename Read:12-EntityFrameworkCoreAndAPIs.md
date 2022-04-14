# Read: 12 - Entity Framework Core and APIs
- we will Get started with EF Core in an ASP.NET MVC web app.

![](./img/R.jpg)

### Create web app
- Start Visual Studio and select Create a new project.
- In the Create a new project dialog, select ASP.NET Core Web Application > Next.
- In the Configure your new project dialog, enter ContosoUniversity for Project name. It's important to use this exact name including capitalization, so each namespace matches when code is copied.
Select Create.
- In the Create a new ASP.NET Core web application dialog, select:
- .NET Core and ASP.NET Core 5.0 in the dropdowns.
- ASP.NET Core Web App (Model-View-Controller).
- Create

### Three ways to develop a model in EF: 

- Generate from exsisting database
- Hand Code a Model to match a database
- Once model is created, use EF Migrations
- Use LINQ <-- should be LIQ (I want it to anyway)

Create controller and views
Use the scaffolding engine in Visual Studio to add an MVC controller and views that will use EF to query and save data.

### The automatic creation of CRUD action methods and views is known as scaffolding.

- In Solution Explorer, right-click the Controllers folder and select Add > New Scaffolded Item.
- In the Add Scaffold dialog box:
- Select MVC controller with views, using Entity Framework.
- Click Add. The Add MVC Controller with views, using Entity Framework dialog box appears:
- bIn Model class, select Student.
- bIn Data context class, select SchoolContext.
- Accept the default StudentsController as the name.

- With EF Core, data access is performed using a model. A model is made up of entity classes and a context object that represents a session with the database. The context object allows querying and saving data. For more information, see Creating a Model.

### API 

**for evry resorce access there are a status code to tel the user what habend the this response like :**

- 200 meaning that is OK.

- 201 meaning that is OK and you create a new resurce.

- 400 meaning that is NOT ok client do somting wronge.

- 404 meaning that resurce Not there or URI is wronge.

- 401 meaning that you dont have the athintction to retch the resurce.

- 500 meaning that somthing wronge in the server.
