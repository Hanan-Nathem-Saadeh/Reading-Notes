# Read: 27 - MVC Forms
## Views in ASP.NET Core MVC
- In the Model-View-Controller (MVC) pattern, the view handles the app's data presentation and user interaction.
-  A view is an HTML template with embedded Razor markup. Razor markup is code that interacts with HTML markup to produce a webpage that's sent to the client.
-  In ASP.NET Core MVC, views are .cshtml files

## Benefits of using views
- The app is easier to maintain because it's better organized. Views are generally grouped by app feature.
- The parts of the app are loosely coupled. You can build and update the app's views separately from the business logic and data access components.
- It's easier to test the user interface parts of the app because the views are separate units.
- Due to better organization, it's less likely that you'll accidentally repeat sections of the user interface.
# Creating a view
 To create a view, add a new file and give it the same name as its associated controller action with the .cshtml file extension.
 To create a view that corresponds with the About action in the Home controller, create an About.cshtml file in the Views/Home folder.
 
 ---
 
-  Views are typically returned from actions as a ViewResult, which is a type of ActionResult. Your action method can create and return a ViewResult directly, but that isn't commonly done. Since most controllers inherit from Controller, you simply use the View helper method to return the ViewResult
## Pass data to views
Pass data to views using several approaches:

- Strongly typed data: viewmodel
- Weakly typed data
ViewData (ViewDataAttribute)
ViewBag 

## the differences between ViewData and ViewBag  
ViewBag isn't available by default for use in Razor Pages PageModel classes.

- ViewData  
Derives from ViewDataDictionary, so it has dictionary properties that can be useful, such as ContainsKey, Add, Remove, and Clear.
Keys in the dictionary are strings, so whitespace is allowed. Example: ViewData["Some Key With Whitespace"]
Any type other than a string must be cast in the view to use ViewData.
- ViewBag  
Derives from Microsoft.AspNetCore.Mvc.ViewFeatures.Internal.DynamicViewData, so it allows the creation of dynamic properties using dot notation (@ViewBag.SomeKey = <value or object>), and no casting is required. The syntax of ViewBag makes it quicker to add to controllers and views.
Simpler to check for null values. Example: @ViewBag.Person?.Name
  
  
