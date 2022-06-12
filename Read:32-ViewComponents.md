# Read:32 View Components
## View components in ASP.NET Core
View components are similar to partial views, but they're much more powerful. View components don't use model binding, and only depend on the data provided when calling into it.  

***A view component:***

- Renders a chunk rather than a whole response.
- Includes the same separation-of-concerns and testability benefits found between a controller and view.
- Can have parameters and business logic.
- Is typically invoked from a layout page.
- View components are intended anywhere you have reusable rendering logic that's too complex for a partial view, such as:

## Creating A View Component
To create a view component, we can:

- create a class that derives from the base ViewComponent class.
- create a class with the [ViewComponent] attribute.
- create a class with a name that ends with the ViewComponent suffix.
- Any one or even a combination of the three will suffice.

Let's create a sample view componenet with the following code using all three methods:

```
[ViewComponent(Name = "Example")]
public class ExampleViewComponent : ViewComponent
{
    // Stuff and things here...
}
```

## View component methods

- Define an InvokeAsync method that returns a Task<IViewComponentResult> or a synchronous Invoke method that returns an IViewComponentResult.  
- Typically initializes a model and passes it to a view by calling the ViewComponent.View method.  
- Parameters come from the calling method, not HTTP. There's no model binding.  
- Aren't reachable directly as an HTTP endpoint. They're typically invoked in a view. A view component never handles a request.  
- Are overloaded on the signature rather than any details from the current HTTP request.  

* Invoke a view component
  
  ```
  @await Component.InvokeAsync("Name of view component",
                             {Anonymous Type Containing Parameters})
  ```
 
  ```
   @await Component.InvokeAsync("PriorityList",
                     new { 
                         maxPriority =  ViewData["maxPriority"],
                         isDone = ViewData["isDone"]  }
                     )
  ```


- When considering if view components meet an app's specifications, consider using Razor Components instead. Razor Components also combine markup with C# code to produce reusable UI units. Razor Components are designed for developer productivity when providing client-side UI logic and composition.

- Marius Schulz: View Components in ASP.NET Core MVC
As part of ASP.NET MVC 6, a new feature called view components has been introduced. View components are similar to child actions and partials views, allowing you to create reusable components with (or without logic).

- Before ASP.NET Core, you would've probably used a child action to create a reusable component that requires some code for its logic. ASP.NET MVC 6, however, doesn't have child actions anymore. You can now choose between a partial view or a view component, depending on the requirements for the feature you're implementing.
