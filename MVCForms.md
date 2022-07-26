# MVC Forms

MVC forms are part of ASP.NET MVC framework and are the recommended way to work with forms in Sitefinity CMS. MVC technology 
provides a modern, convention-based, mobile-first UI framework to quick and easy setup and design of forms and applications.

### ther are our types of forms:

1.weakly typed synchronous forms
2.strongly typed synchronous forms
3.strongly typed AJAX forms
4.use jQuery with AJAX to post form data

Each form contains three basic elements: a <form> element, <input> elements (which the user can type to), and some type of a 
submit button.

firs step isto create a new controller, view, and model (which is really a class that contains auto-implemented properties. The 
model will be used by the strongly-typed form examples). for examble if we name the controller “Form” (this will create a new 
file called “FormController.cs” in the Controllers folder) and add a view for its Index action method.

### Weakly Typed Synchronous Forms
This is the quickest way to post a form. Each <input>'s name must match one parameter’s name in the method the form is posted to. 
The characters or digits that users type into <input> elements become part of the <input>’s value attribute and since <input>
values are passed from client to server by matching names, make sure there are no typos.

### Strongly Typed Synchronous Forms
In a strongly typed form, we pass from the client to the server an object (the model) whose properties contain the <input> values 
instead of passing many primitives. An advantage of using strongly typed forms is easier maintainability. Unlike weakly typed 
forms, typos are unlikely to happen. Also, the method the form is posted to has fewer parameters.

### What is a View in ASP.NET Core MVC Application?
In the Model-View-Controller (MVC) pattern, the View is the component that contains logic to represent the model data (the model 
data provided to it by a controller) as a user interface with which the end-user can interact. The Views in MVC are HTML 
templates with embedded Razor mark-up which generate content that sends to the client. In our upcoming articles, we will discuss 
the Razor syntax in detail.

view in ASP.NET Core MVC Application is responsible for UI i.e. application data presentation. That means we display information 
about the website on the browser using the views only. A user generally performs all the actions on a view such as a button 
click, form, list, and other UI elements.

By default, Views are available inside the Views folder at the root. Usually, views are grouped into folder names with 
applications controller. Generally, views are grouped based on features.

Usually, each controller will have its own folder in which the controller-specific view files are going to be stored. The 
controller-specific folders are going to be created within the Views folder only. The point that you need to remember is the view 
file name is the same as the action method name of a controller with the “.cshtml” extension.


### steps to create mvc 

1.Step1: Setting MVC Service and MVC Middleware
In order to make your ASP.NET Core Web Application as an MVC application, we need to set up required MVC Services and MVC 
Middleware to the request processing pipeline. And this can be done within the ConfigureServices and Configure method of the 
Startup class which is present inside the Startup.cs class file.

Step2: Creating Controllers

Step3: Creating Index View
Views are going to be created inside the folder whose name is the same as the Controller name. We want to create a view for the 
Index action method of Home Controller. So, let us first add the Home folder inside the View folder. To do so, right-click on the 
Views folder and then select the Add => New Folder option which will add a new folder and then simply rename the folder as Home;
Right-click on the Home folder and then select Add => View option which will open the Add View window as shown in the below 
image. Here, you need to select the Razor View item and then click on the Add button.

### View() vs View(object model) Extension Methods:

If we are using the View() or View(object model) extension method to return a view, then it will look for the view file with the 
same name as the action method name. If you want to pass some model data then you need to use the overloaded version which takes 
object model as input parameter else you can simply use the View() extension method which does not take any parameter.

### Advantages of Using Views in ASP.NET Core MVC Application

The Views in MVC application provides the separation of concerns (codes). It separates the user interface from the business logic 
or you can say from the rest of the application. The ASP.NET Core MVC views use the Razor syntax which makes it easy to switch 
between the HTML markup and C# code. The Common or repetitive aspects of the application’s user interface can be easily reused 
between views using layout and shared directives or partial views.

### CSS

Isolate CSS styles to individual pages, views, and components to reduce or avoid:

1.Dependencies on global styles that can be challenging to maintain.
2.Style conflicts in nested content.

To add a scoped CSS file for a page or view, place the CSS styles in a companion .cshtml.css file matching the name of the .
cshtml file. In the following example, a Index.cshtml.css file supplies CSS styles that are only applied to the Index.cshtml page 
or view.

### CSS preprocessor support
While CSS isolation doesn't natively support CSS preprocessors such as Sass or Less, integrating CSS preprocessors is seamless as 
long as preprocessor compilation occurs before the framework rewrites the CSS selectors during the build process. Using Visual 
Studio for example, configure existing preprocessor compilation as a Before Build task in the Visual Studio Task Runner Explorer.







