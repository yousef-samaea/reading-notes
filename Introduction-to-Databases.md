# Introduction to Databases

Database is a collection of related data and data is a collection of facts and figures that can be processed to produce information.

## Characteristics

DBMS was a new concept then, and all the research was done to make it overcome the deficiencies in traditional style of data management.

### DBMS characteristics:

1. Real-world entity − A modern DBMS is more realistic and uses real-world entities to design its architecture. It uses the behavior and attributes too

2. Relation-based tables − DBMS allows entities and relations among them to form tables.

3. Isolation of data and application − A database system is entirely different than its data. A database is an active entity, whereas data is said to be passive, on which the database works and organizes.

4. Less redundancy − DBMS follows the rules of normalization, which splits a relation when any of its attributes is having redundancy in values.

5. Consistency − Consistency is a state where every relation in a database remains consistent. There exist methods and techniques, which can detect attempt of leaving database in inconsistent state.

6. Query Language − DBMS is equipped with query language, which makes it more efficient to retrieve and manipulate data. A user can apply as many and as different filtering options as required to retrieve a set of data.

7. ACID Properties − DBMS follows the concepts of Atomicity, Consistency, Isolation, and Durability (normally shortened as ACID). These concepts are applied on transactions, which manipulate data in a database.

8. Multiuser and Concurrent Access − DBMS supports multi-user environment and allows them to access and manipulate data in parallel. Though there are restrictions on transactions when users attempt to handle the same data item.

9. Multiple views − DBMS offers multiple views for different users. A user who is in the Sales department will have a different view of database than a person working in the Production department.

10. Security − Features like multiple views offer security to some extent where users are unable to access data of other users and departments. DBMS offers methods to impose constraints while entering data into the database and retrieving the same at a later stage.

### Users
A typical DBMS has users with different rights and permissions who use it for different purposes.

1. Administrators − Administrators maintain the DBMS and are responsible for administrating the database. They are responsible to look after its usage and by whom it should be used. They create access profiles for users and apply limitations to maintain isolation and force security.

2. Designers − Designers are the group of people who actually work on the designing part of the database. They keep a close watch on what data should be kept and in what format. They identify and design the whole set of entities, relations, constraints, and views.

End Users − End users can range from simple viewers who pay attention to the logs or market rates to sophisticated users such as business analysts.

## What is a Schema?

Obtaining schema information from a database is accomplished with the process of schema discovery. Schema discovery allows applications to request that managed providers find and return information about the schema database, also known as metadata, of a given database,Different database schema elements such as tables, columns, and stored-procedures are exposed through schema collections.

Each of the .NET Framework managed providers implement the GetSchema method in the Connection class, and the schema information that is returned from the GetSchema method comes in the form of a DataTable.

The .NET Framework Data Providers for
1.OLE 2.DB, 3.ODBC 4.Oracle 4.SqlClient provide a GetSchemaTable method that returns a DataTable describing the column metadata of the DataReader,The .NET Framework Data Provider for OLE DB also exposes schema information by using the GetOleDbSchemaTable method of the OleDbConnection object. 

## Database supports the following types of keys :

1. Super Key.
2. Minimal Super Key.
3. Candidate Key.
4. Primary Key.
5. Unique Key.
6. Alternate Key.
7. Composite Key.
8. Foreign Key.

all of the web pages currently display the time along with the date, although all you care about for this field is the date. By using data annotation attributes, you can make one code change that will fix the display format in every view that shows the data. To see an example of how to do that, you'll add an attribute to the EnrollmentDate property in the Student class.

### how to use Database modifaiar:

in program.cs, add a using statement for the System.ComponentModel.DataAnnotations namespace and add DataType and DisplayFormat attributes to the EnrollmentDate property.

The DataType attribute is used to specify a data type that's more specific than the database intrinsic type. In this case we only want to keep track of the date, not the date and time. The DataType Enumeration provides for many data types, such as Date, Time, PhoneNumber, Currency, EmailAddress, and more. The DataType attribute can also enable the application to automatically provide type-specific features. For example, a mailto: link can be created for DataType.EmailAddress, and a date selector can be provided for DataType.Date in browsers that support HTML5.

### The DisplayFormat attribute is used to explicitly specify the date format:

[DisplayFormat(DataFormatString = "{0:yyyy-MM-dd}", ApplyFormatInEditMode = true)]

The DataType attribute conveys the semantics of the data as opposed to how to render it on a screen

### benefits that you don't get with DisplayFormat:

1. The browser can enable HTML5 features (for example to show a calendar control, the locale-appropriate currency symbol, email links, some client-side input validation, etc.).

2. By default, the browser will render data using the correct format based on your locale.

## attribute :

1.The StringLength attribute
You can also specify data validation rules and validation error messages using attributes.

2.The Column attribute
You can also use attributes to control how your classes and properties are mapped to the database.

3.The Required attribute 
The Required attribute makes the name properties required fields.

4.The Display attribute
The Display attribute specifies that the caption for the text boxes should be "First Name", "Last Name", "Full Name", and "Enrollment Date" instead of the property name in each instance

5.The Key attribute
There's a one-to-zero-or-one relationship between the Instructor and the OfficeAssignment entities. An office assignment only exists in relation to the instructor it's assigned to, and therefore its primary key is also its foreign key to the Instructor entity.

6.The DatabaseGenerated attribute
The DatabaseGenerated attribute with the None parameter on the CourseID property specifies that primary key values are provided by the user rather than generated by the database.

7.The Column attribute
Earlier you used the Column attribute to change column name mapping. In the code for the Department entity









