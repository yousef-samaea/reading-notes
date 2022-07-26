# View Components

*ASP.NET Core MVC, view components are similar to partial views, but they are much more powerful. View components don’t use model*
*binding, and only depend on the data you provide when calling into it. A view component:*

1. Renders a chunk rather than a whole response
2. Includes the same separation-of-concerns and testability benefits found between a controller and view
3. Can have parameters and business logic
4. Is typically invoked from a layout page


*View Components are intended anywhere you have reusable rendering logic that is too complex for a partial view, such as:*

1. Dynamic navigation menus
2. Tag cloud (where it queries the database)
3. Login panel
4. Shopping cart
5. Recently published articles
6. Sidebar content on a typical blog
7. A login panel that would be rendered on every page and show either the links to log out or log in, depending on the log in 
state of the user

A view component consists of two parts, the class and the result it returns Like controllers, a view component can be a POCO, but 
most developers will want to take advantage of the methods and 
properties available by deriving from ViewComponent.


### Creating a view component:

*The view component class*

A view component class can be created by any of the following:

1. Deriving from ViewComponent
2. Decorating a class with the [ViewComponent] attribute, or deriving from a class with the [ViewComponent] attribute
3. Creating a class where the name ends with the suffix ViewComponent

Like controllers, view components must be public, non-nested, and non-abstract classes. The view component name is the class name 
with the “ViewComponent” suffix removed. It can also be explicitly specified using the ViewComponentAttribute.Name property.

*A view component class:*

1.Fully supports constructor dependency injection
2.Does not take part in the controller lifecycle, which means you can’t use filters in a view component

### View component methods

A view component defines its logic in an InvokeAsync method that returns an IViewComponentResult. Parameters come directly from 
invocation of the view component, not from model binding. A view component never directly handles a request. Typically a view 
component initializes a model and passes it to a view by calling the View method. In summary, view component methods:

1. Define an InvokeAsync` method that returns an IViewComponentResult
2. Typically initializes a model and passes it to a view by calling the ViewComponent View method
3. Parameters come from the calling method, not HTTP, there is no model binding
4. Are not reachable directly as an HTTP endpoint, they are invoked from your code (usually in a view). A view component never 
handles a request
5. Are overloaded on the signature rather than any details from the current HTTP request


### View search path
The runtime searches for the view in the following paths:

1) Views/<controller_name>/Components/<view_component_name>/<view_name>
2) Views/Shared/Components/<view_component_name>/<view_name>

The default view name for a view component is Default, which means your view file will typically be named Default.cshtml. You can 
specify a different view name when creating the view component result or when calling the View method.

### Invoking a view component

To use the view component, call @Component.InvokeAsync("Name of view component", <anonymous type containing parameters>) from a 
view. The parameters will be passed to the InvokeAsync method. The PriorityList view component developed in the article is 
invoked from the Views/Todo/Index.cshtml view file. In the following, the InvokeAsync method is called with two parameters:

@await Component.InvokeAsync("PriorityList", new { maxPriority = 2, isDone = false })

### Invoking a view component directly from a controller
View components are typically invoked from a view, but you can invoke them directly from a controller method. While view 
components do not define endpoints like controllers, you can easily implement a controller action that returns the content of a 
ViewComponentResult.

In this example, the view component is called directly from the controller:

  public IActionResult IndexVC()
  {
      return ViewComponent("PriorityList", new { maxPriority = 3, isDone = false });
  }

### Create the view component Razor view :

1. Create the Views/Shared/Components folder. This folder must be named Components.

2. Create the Views/Shared/Components/PriorityList folder. This folder name must match the name of the view component class, or 
the name of the class minus the suffix

3. Create a Views/Shared/Components/PriorityList/Default.cshtml Razor view.

4. Add a div containing a call to the priority list component to the bottom of the Views/Todo/index.cshtml file

