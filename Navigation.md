# Navigation
ASP.NET MVC routing is a pattern matching system that is responsible for mapping incoming browser requests to specified MVC controller actions.

its application registers one or more patterns with the framework's route table to tell the routing engine what to do with any requests that matches those patterns.

### Properties of Route:

1.Route Name: A route is a URL pattern that is mapped to a handler.
2.URL Pattern: A URL pattern can contain literal values and variable placeholders
3.Defaults: When you define a route, you can assign a default value for a parameter
4.Constraints: A set of constraints to apply against the URL pattern to more narrowly define the URL that it matches.

basicly The default ASP.NET MVC project templates add a generic route that uses the following URL convention to break the URL for a given request into three named segments.

### Conclusion:
 
The controller and action values in the route are not case-sensitive. URL route patterns are relative to the application root, so they don't need to start with a forward slash (/) or virtual path designator (~/).

### Endpoint:

The MapGet method is used to define an endpoint. An endpoint is something that can be:

1.Selected, by matching the URL and HTTP method.
2.Executed, by running the delegate.

### Routing concepts:
The routing system builds on top of the middleware pipeline by adding the powerful endpoint concept. Endpoints represent units of the app's functionality that are distinct from each other in terms of routing, authorization, and any number of ASP.NET Core's systems.

### how route templates are defined:

1.Templates with more segments are considered more specific.
2.A segment with literal text is considered more specific than a parameter segment.
3.A parameter segment with a constraint is considered more specific than one without.
4.A complex segment is considered as specific as a parameter segment with a constraint.
5.Catch-all parameters are the least specific. See catch-all in the Route template.

### Route template reference:

okens within {} define route parameters that are bound if the route is matched, and its a valid route, since there's no literal value between {controller} and {action}.

### Addresses:

Addresses are an extensible concept that come with two implementations by default:

1.Using endpoint name (string) as the address
2.Using route values (RouteValuesAddress) as the address

### URL generation process:

the URL generation algorithm:

1.Processes the endpoints iteratively.
2.Returns the first successful result.

### Guidance for library authors
This section contains guidance for library authors building on top of routing. These details are intended to ensure that app developers have a good experience using libraries and frameworks that extend routing.











