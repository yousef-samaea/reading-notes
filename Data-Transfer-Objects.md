# Data Transfer Objects

DTO refers to "Data Transfer objects" and it is a data container for moving data between layers, They are also termed as transfer objects.
DTO is only used to pass data and does not contain any business logic, They only have simple setters and getters.

### some of thiga you can do using DTO :

1.Remove circular references (see previous section).

2.Hide particular properties that clients are not supposed to view.

3.Omit some properties in order to reduce payload size.

4.Flatten object graphs that contain nested objects, to make them more convenient for clients.

5.Avoid "over-posting" vulnerabilities.

6.Decouple your service layer from your database layer.

### how to Create an ASP.NET Core API project :

1.Launch the Visual Studio IDE.

2.Click on “Create new project.”

3.In the “Create new project” window, select “ASP.NET Core Web Application” from the list of the templates displayed. then 4.Click Next. 

5.In the “Configure your new project” window, specify the name and location for the new project. then6.Click Create. 

7.In the “Create New ASP.NET Core Web Application” window shown next, select .NET Core as the runtime and ASP.NET Core 3.1 (or 8.later) from the drop-down list at the top.

8.Select “API” as the project template to create a new ASP.NET Core API application. 

9.Ensure that the check boxes “Enable Docker Support” and “Configure for HTTPS” are unchecked as we won’t be using those features here.

10.Ensure that Authentication is set as “No Authentication” as we won’t be using authentication either.

11.and last step is to Click Create. 

### Why yoy shold use DTO :

if we using models to pass data between the the coding layers and sending data back to the presentation layer, then we exposing the internal data structures of your application and its easier when we implementing APIs, MVC applications.

### using of DTO :

1. abstraction :

if you would like to change the presentation layer, you can do that easily while the application will continue to work with the existing domain layer, and you can change the domain layer of your application without having to change the presentation layer of the application.

2. data hiding :

using DTOs you can return only the data requested so that will make your code better.


### Immutability of DTOs :

DTO is meant to transport data from one layer of an application to another layer, DTO is often serialized
most cases, the receiver of the data does not need to modify that data after receipt,

### DTO serialization challenges

1.DTO seamlessly so that it can be passed down the wire.

2.Data Transfer Objects typically don’t contain any business logic — they only contain data.

3.Immutability is a desired feature when working with DTOs.

