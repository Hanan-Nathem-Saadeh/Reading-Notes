Read:31 View Components
Microsoft Docs: View components in ASP.NET Core
View components are similar to partial views, but they're much more powerful. View components don't use model binding, and only depend on the data provided when calling into it.

A view component:

Renders a chunk rather than a whole response.
Includes the same separation-of-concerns and testability benefits found between a controller and view.
Can have parameters and business logic.
Is typically invoked from a layout page.
View components are intended anywhere you have reusable rendering logic that's too complex for a partial view, such as:

Dynamic navigation menus
Tag cloud (where it queries the database)
Login panel
Shopping cart
Recently published articles
Sidebar content on a typical blog
A login panel that would be rendered on every page and show either the links to log out or log in, depending on the log in state of the user
A view component consists of two parts: the class and the result is returns. Most developers will want to take advantage of the methods and properties available by deriving from ViewComponent.

When considering if view components meet an app's specifications, consider using Razor Components instead. Razor Components also combine markup with C# code to produce reusable UI units. Razor Components are designed for developer productivity when providing client-side UI logic and composition.

Marius Schulz: View Components in ASP.NET Core MVC
As part of ASP.NET MVC 6, a new feature called view components has been introduced. View components are similar to child actions and partials views, allowing you to create reusable components with (or without logic).

Before ASP.NET Core, you would've probably used a child action to create a reusable component that requires some code for its logic. ASP.NET MVC 6, however, doesn't have child actions anymore. You can now choose between a partial view or a view component, depending on the requirements for the feature you're implementing.
