# Framework and APIs

### Some things this MVC tutorial has that the Razor Pages tutorial doesn't:

1.Implement inheritance in the data model
2.Perform raw SQL queries
3.Use dynamic LINQ to simplify code
### Some things the Razor Pages tutorial has that this one doesn't:

1.Use Select method to load related data
2.Best practices for EF.

### Prerequisites
1.If you're new to ASP.NET Core MVC, go through the Get started with ASP.NET Core MVC tutorial series before starting this one.
2.Visual Studio 2019 16.8 or later with the ASP.NET and web development workload
3..NET 5.0 SDK

### Solve problems and troubleshoot
If you run into a problem you can't resolve, you can generally find the solution by comparing your code to the completed project. For a list of common errors and how to solve them, see the Troubleshooting section of the last tutorial in the series. If you don't find what you need there, you can post a question to StackOverflow.com for ASP.NET Core or EF Core.


### Create the database context
The main class that coordinates EF functionality for a given data model is the DbContext database context class. This class is created by deriving from the Microsoft.EntityFrameworkCore.DbContext class. The DbContext derived class specifies which entities are included in the data model. Some EF behaviors can be customized. In this project, the class is named SchoolContext,When the database is created, EF creates tables that have names the same as the DbSet property names. Property names for collections are typically plural. For example, Students rather than Student. Developers disagree about whether table names should be pluralized or not. For these tutorials, the default behavior is overridden by specifying singular table names in the DbContext.


### Register the SchoolContext
ASP.NET Core includes dependency injection. Services, such as the EF database context, are registered with dependency injection during app startup. Components that require these services, such as MVC controllers, are provided these services via constructor parameters.


### Initialize DB with test data
EF creates an empty database. In this section, a method is added that's called after the database is created in order to populate it with test data.

The EnsureCreated method is used to automatically create the database. In a later tutorial, you see how to handle model changes by using Code First Migrations to change the database schema instead of dropping and re-creating the database.

### The model
With EF Core, data access is performed using a model. A model is made up of entity classes and a context object that represents a session with the database. The context object allows querying and saving data. For more information

EF supports the following model development approaches:

Generate a model from an existing database.
Hand code a model to match the database.
Once a model is created, use EF Migrations to create a database from the model. Migrations allow evolving the database as the model changes.

Querying
Instances of your entity classes are retrieved from the database using Language Integrated Query (LINQ). For more information.

Saving data
Data is created, deleted, and modified in the database using instances of your entity classes.

### EF O/RM considerations
While EF Core is good at abstracting many programming details, there are some best practices applicable to any O/RM that help to avoid common pitfalls in production apps:

1.Intermediate-level knowledge or higher of the underlying database server is essential to architect, debug, profile, and migrate data in high performance production apps. For example, knowledge of primary and foreign keys, constraints, indexes, normalization, DML and DDL statements, data types, profiling, etc.

2.Performance and stress testing with representative loads. The naïve usage of some features doesn't scale well. For example, multiple collections Includes, heavy use of lazy loading, conditional queries on non-indexed columns, massive updates and inserts with store-generated values, lack of concurrency handling, large models, inadequate cache policy.

3.Security review: For example, handling of connection strings and other secrets, database permissions for non-deployment operation, input validation for raw SQL, encryption for sensitive data.

4.Make sure logging and diagnostics are sufficient and usable. For example, appropriate logging configuration, query tags, and Application Insights.

5.Error recovery. Prepare contingencies for common failure scenarios such as version rollback, fallback servers, scale-out and load balancing, DoS mitigation, and data backups.

6.Application deployment and migration. Plan out how migrations are going to be applied during deployment; doing it at application start can suffer from concurrency issues and requires higher permissions than necessary for normal operation. Use staging to facilitate recovery from fatal errors during migration.

7.Detailed examination and testing of generated migrations. Migrations should be thoroughly tested before being applied to production data. The shape of the schema and the column types cannot be easily changed once the tables contain production data. For example, on SQL Server, nvarchar(max) and decimal(18, 2) are rarely the best types for columns mapped to string and decimal properties, but those are the defaults that EF uses because it doesn't have knowledge of your specific scenario.

### Model seed data
Unlike in EF6, in EF Core, seeding data can be associated with an entity type as part of the model configuration. Then EF Core migrations can automatically compute what insert, update or delete operations need to be applied when upgrading the database to a new version of the model.

### Limitations of model seed data
This type of seed data is managed by migrations and the script to update the data that's already in the database needs to be generated without connecting to the database. 

Troubleshooting
If you run into a problem you can't resolve, compare your code to the completed project. A good way to get help is by posting a question to StackOverflow.com







