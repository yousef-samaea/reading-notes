# Testing and Swagger and Deployments

### Swagger :

Swagger Codegen can simplify your build process by generating server stubs and client SDKs for any API, defined with the OpenAPI

Swagger (OpenAPI) is a language-agnostic specification for describing REST APIs. It allows both computers and humans to understand the capabilities of a REST API without direct access to the source code.

**Swagger using for :**

1.Minimize the amount of work needed to connect decoupled services.
2.Reduce the amount of time needed to accurately document a service.

**some propertes:**

1.OpenAPI is a specification.
2.Swagger is tooling that uses the OpenAPI specification. For example, OpenAPIGenerator and SwaggerUI.

**Swagger UI**

Swagger UI offers a web-based UI that provides information about the service. This is built using the Swagger Specification and embedded inside the Swashbuckle package and hence it can be hosted in our ASP.NET Core app using middlewares.

### Tests for ASP.NET MVC Applications :

**Steps:**

1.Add a new unit test project to the MVC module solution:

a.In Visual Studio's Solution Explorer, right-click on your MVC module solution and select Add > New Project
b.In the Add New Project dialog, select Unit Test Project, enter a name, and select the local folder to store it in.

2.Add the necessary MVC and DNN assembly references.

Add references to the following assemblies, as well as others that your module specifically needs:
a.DotNetNuke
b.DotNetNuke.Web.Mvc
c.System.Web.Mvc

3.Use Moq to simulate a data store.

4.Create the unit test.

5.Retrofit the ItemController.Edit() method to work with unit tests.

### Unit test controller logic :

its so important because Automated tests can detect errors before the app is deployed to a production environment.

*Unit tests involve testing a part of an app in isolation from its infrastructure and dependencies*

**A controller unit test avoids scenarios such as :**

1.filters.
2.routing.
3.model binding.

The HTTP GET Index method has no looping or branching and only calls one method.
The unit test for this action:

1.Mocks the IBrainstormSessionRepository service using the GetTestSessions method. GetTestSessions creates two mock brainstorm sessions with dates and session names.

2.Executes the Index method.

3.Makes assertions on the result returned by the method:
a.A ViewResult is returned.
b.The ViewDataDictionary.Model is a StormSessionViewModel.
c.There are two brainstorming sessions stored in the ViewDataDictionary.Model.

When ModelState isn't valid, the same ViewResult is returned as for a GET request. The test doesn't attempt to pass in an invalid model.

**the app exposes functionality as a web API on the api/ideas route:**

1.A list of ideas (IdeaDTO) associated with a brainstorming session is returned by the ForSession method.

2.The Create method adds new ideas to a session.