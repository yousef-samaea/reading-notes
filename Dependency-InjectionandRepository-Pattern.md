# Dependency Injection & Repository Pattern

A dependency is an object that another object depends on.

### Dependency injection addresses these problems through:

1.The use of an interface or base class to abstract the dependency implementation.

2.Registration of the dependency in a service container. ASP.NET Core provides a built-in service container, IServiceProvider. Services are typically registered in the app's Program.cs file.

3.Injection of the service into the constructor of the class where it's used. The framework takes on the responsibility of creating an instance of the dependency and disposing of it when it's no longer needed.

### n dependency injection terminology, a service:

1.Is typically an object that provides a service to other objects, such as the IMyDependency service.

2.Is not related to a web service, although the service may use a web service.

### Register groups of services with extension methods

The ASP.NET Core framework uses a convention for registering a group of related services. The convention is to use a single Add{GROUP_NAME} extension method to register all of the services required by a framework feature. For example, the AddControllers extension method registers the services required for MVC controllers.

## Service lifetimes

1.Inject the service into the middleware's Invoke or InvokeAsync method. Using constructor injection throws a runtime exception because it forces the scoped service to behave like a singleton. The sample in the Lifetime and registration options section demonstrates the InvokeAsync approach.

2.Use Factory-based middleware. Middleware registered using this approach is activated per client request (connection), which allows scoped services to be injected into the middleware's constructor.

### Service registration methods

Registering a service with only an implementation type is equivalent to registering that service with the same implementation and service type. This is why multiple implementations of a service cannot be registered using the methods that don't take an explicit service type. These methods can register multiple instances of a service, but they will all have the same implementation type.

### Design services for dependency injection

When designing services for dependency injection:

1.Avoid stateful, static classes and members. Avoid creating global state by designing apps to use singleton services instead. 

2.Avoid direct instantiation of dependent classes within services. Direct instantiation couples the code to a particular implementation. 

3.Make services small, well-factored, and easily tested.

If a class has a lot of injected dependencies, it might be a sign that the class has too many responsibilities and violates the Single Responsibility Principle (SRP). Attempt to refactor the class by moving some of its responsibilities into new classes.

## The Repository pattern

Repositories are classes or components that encapsulate the logic required to access data sources. They centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer.

### Define one repository per aggregate

For each aggregate or aggregate root, you should create one repository class. In a microservice based on Domain-Driven Design (DDD) patterns, the only channel you should use to update the database should be the repositories. This is because they have a one-to-one relationship with the aggregate root, which controls the aggregate's invariants and transactional consistency. It's okay to query the database through other channels (as you can do following a CQRS approach), because queries don't change the state of the database. However, the transactional area (that is, the updates) must always be controlled by the repositories and the aggregate roots,

### Enforce one aggregate root per repository

It can be valuable to implement your repository design in such a way that it enforces the rule that only aggregate roots should have repositories. You can create a generic or base repository type that constrains the type of entities it works with to ensure they have the IAggregateRoot marker interface, better way to have the code enforce the convention that each repository is related to a single aggregate is to implement a generic repository type, It assumes the repository class has delivered those. Once your logic modifies the domain entities, it assumes the repository class will store them correctly. The important point here is to create unit tests against your domain model and its domain logic.

### The difference between the Repository pattern

A data access object directly performs data access and persistence operations against storage. A repository marks the data with the operations you want to perform in the memory of a unit of work object (as in EF when using the DbContext class), but these updates aren't performed immediately to the database.

A unit of work is referred to as a single transaction that involves multiple insert, update, or delete operations. In simple terms, it means that for a specific user action, such as a registration on a website, all the insert, update, and delete operations are handled in a single transaction,These multiple persistence operations are performed later in a single action when your code from the application layer commands it. The decision about applying the in-memory changes to the actual database storage is typically based on the Unit of Work pattern.

### Abstraction

The idea with this pattern is to have a generic abstract way for the app to work with the data layer without being bother with if the implementation is towards a local database or towards an online API.

### Compromise

I chose to compromise and go half way between the repository and my old DAOs. I have my interface with all the CRUD methods. I also add one more method readById(K id). This interface will cover most of my basic use cases.

## SOLID Code

The SOLID Principals of software development is the brain child or Robert “Uncle Bob” Martin. In the early 2000 he described five principals that software developers could use to guide them in creating software that was well designed, high quality and easier to maintain than what was being produced at the time. These five ideas are simple, promote good practices in software design and development, and go a long way to help us in our practice of TDD.

### Single Responsibility Principle

You can logically extend that to say that every class or method in your application should have exactly one (a single) job or responsibility. The short way of saying this is that each method and each class should be responsible for one, and only one task, As a virtual shopping cart it would be logical for the class to hold a collection of items that a user has added to the cart to purchase and perhaps a way to communicate with a service for the user to checkout. To extend this example let’s say that the site has a loyalty rewards program that rewards points to customers based on purchases. Any functionality to award, track or manage points would not be appropriate to add to the shopping cart. That functionality should reside in a separate service. The shopping cart should not be responsible for, or actually have any concept of the rewards program. 

### The Open/Close Principle

The Open/Close Principle (OCP) is very closely related to the previously discussed topics of Encapsulation and Inheritance. In fact it’s fair to say the OCP is concept that unifies these two tenants of OOP. OCP states that software, be it a method or a class, should be open for extension, but closed to modification. To get a better idea of what this means, I’m going tackle each one of those statements individually. When developer write software they are often reliant on libraries of classes from other developers, solutions or even third party providers. In order to keep the appeal of these components broad, their functionality is often designed to provide a generalized form of their purpose. In many cases we are able to use the components in these libraries “as-is” meaning that the generalized functionality provided is sufficient for the given need. On occasion however a more specialized version of these components may be required. At other times we simply need the base component to function differently than it normally does.Just as you wouldn’t want to add a basement to a finished house, making modifications to fundamental parts of code significantly increases the chance of introducing bugs or side effects.  It is better to use extensions (like adding a patio room) to add on to or alter functionality of a module through polymorphism than to continually edit the base code by adding switch statements.

### Single Responsibility Principle

A class should have one, and only one, reason to change
Did you ever have a Swiss Army knife?  64 features, but you could never get to the one you needed.  And who uses the toothpick from a knife anyway?  Yuck!  Code that does too much is very much like that Swiss Army knife – trying to be all things to all scenarios results in overly complex and fragile code.  Keeping your methods short and of singular purpose brings clarity and ease of maintainability to your software.

### Liskov Substitution Principle

If you are at a restaurant, and order a salad, the way you eat it (and when it gets served) doesn’t vary just because this time you ordered a Caesar Salad and last time you ordered a house salad.  In the same way, derived classed must be able to be used by the client code without any adverse effects on the function of the client code.





