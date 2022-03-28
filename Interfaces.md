# Interfaces

An interface contains definitions for a group of related functionalities that a non-abstract class or a struct must implement. An interface may define static methods, which must have an implementation.

By using interfaces, you can, for example, include behavior from multiple sources in a class. That capability is important in C# because the language doesn't support multiple inheritance of classes. In addition, you must use an interface if you want to simulate inheritance for structs, because they can't actually inherit from another struct or class.

Any class or struct that implements the IEquatable<T> interface must contain a definition for an Equals method that matches the signature that the interface specifies. As a result, you can count on a class that implements IEquatable<T> to contain an Equals method with which an instance of the class can determine whether it's equal to another instance of the same class,The definition of IEquatable<T> doesn't provide an implementation for Equals. A class or struct can implement multiple interfaces, but a class can only inherit from a single class.

Interfaces can contain instance methods, properties, events, indexers, or any combination of those four member types. Interfaces may contain static constructors, fields, constants, or operators,To implement an interface member, the corresponding member of the implementing class must be public, non-static, and have the same name and signature as the interface member.

###  interface properties:

1.In C# versions earlier than 8.0, an interface is like an abstract base class with only abstract members. A class or struct that implements the interface must implement all its members.

2.Beginning with C# 8.0, an interface may define default implementations for some or all of its members. A class or struct that implements the interface doesn't have to implement members that have default implementations. For more information, see default interface methods.

3.An interface can't be instantiated directly. Its members are implemented by any class or struct that implements the interface.

4.A class or struct can implement multiple interfaces. A class can inherit a base class and also implement one or more interfaces.

### Interfaces are contracts

Interfaces allow us to specify that a particular class meets certain expectations that other classes can rely on,If we have a class that implements an interface, we can be sure that it will support all the methods that are defined in that interface.
At first glance interfaces seem to be similar to concrete inheritance, but there is a key difference.

Concrete inheritance says Car is an Automobile, while an interface says Car implements the Drivable interface.

When a class implements an interface, it does not mean that class IS that interface.  For this reason interfaces that completely describe the functionality of a class are usually wrong.
and Interfaces are always implemented by more than one class

### use dependency injection

These two reasons are probably the most justified causes for incorrectly using interfaces.

I am guilty of justifying the creation of an interface so that I can have something to mock, and I am guilty of creating an interface just for my dependency injection framework, but it doesn’t make it right.

I can’t give you an easy answer here and say that I can solve your unit testing or dependency injection problems without an interface, but I can talk about why we shouldn’t be bending the source code to fit the tool or methodology.

and in the Beginning with C# 11, an interface may declare static abstract members for all member types except fields. This feature enables generic algorithms to specify number-like behavior. You can try this feature by working with the tutorial on static abstract members in interfaces.






