# Object Oriented Principles

### Inheritance

it is one of the three primary characteristics of object-oriented programming. Inheritance enables you to create new classes that reuse, extend, and modify the behavior defined in other classes. The class whose members are inherited is called the base class, and the class that inherits those members is called the derived class.

Interface declarations may define a default implementation for its members. These implementations are inherited by derived interfaces, and by classes that implement those interfaces. For more information on default interface methods, see the article on interfaces,When you define a class to derive from another class, the derived class implicitly gains all the members of the base class, except for its constructors and finalizers.

### Abstract and virtual methods
When a base class declares a method as virtual, a derived class can override the method with its own implementation. If a base class declares a member as abstract, that method must be overridden in any non-abstract class that directly inherits from that class. If a derived class is itself abstract, it inherits abstract members without implementing them. Abstract and virtual members are the basis for polymorphism, which is the second primary characteristic of object-oriented programming. For more information, see Polymorphism.

### Abstract base classes
we can declare a class as abstract if you want to prevent direct instantiation by using the new operator. An abstract class can be used only if a new class is derived from it. An abstract class can contain one or more method signatures that themselves are declared as abstract. These signatures specify the parameters and return value but have no implementation (method body). An abstract class doesn't have to contain abstract members; however, if a class does contain an abstract member, the class itself must be declared as abstract. Derived classes that aren't abstract themselves must provide the implementation for any abstract methods from an abstract base class.

## Abstract and Sealed Classes and Class Members

1.The abstract keyword enables you to create classes and class members that are incomplete and must be implemented in a derived class.

2.The sealed keyword enables you to prevent the inheritance of a class or certain class members that were previously marked virtual.

The purpose of an abstract class is to provide a common definition of a base class that multiple derived classes can share. For example, a class library may define an abstract class that is used as a parameter to many of its functions,Abstract methods have no implementation, so the method definition is followed by a semicolon instead of a normal method block. Derived classes of the abstract class must implement all abstract methods.

## Polymorphism

Polymorphism is often referred to as the third pillar of object-oriented programming, after encapsulation and inheritance.

Polymorphism is a Greek word that means "many-shaped" and it has two distinct aspects:

* At run time, objects of a derived class may be treated as objects of a base class in places such as method parameters and collections or arrays. When this polymorphism occurs, the object's declared type is no longer identical to its run-time type.

* Base classes may define and implement virtual methods, and derived classes can override them, which means they provide their own definition and implementation. At run-time, when client code calls the method, the CLR looks up the run-time type of the object, and invokes that override of the virtual method. In your source code you can call a method on a base class, and cause a derived class's version of the method to be executed.

You can use polymorphism to solve this problem in two basic steps:

1.Create a class hierarchy in which each specific shape class derives from a common base class.
2.Use a virtual method to invoke the appropriate method on any derived class through a single call to the base class method.

The designer of the derived class has different choices for the behavior of virtual methods:

1.The derived class may override virtual members in the base class, defining new behavior.
2.The derived class may inherit the closest base class method without overriding it, preserving the existing behavior but enabling further derived classes to override the method.
3.The derived class may define new non-virtual implementation of those members that hide the base class implementations.

## Object-Oriented programming


The four basic principles of object-oriented programming are:

1.Abstraction Modeling the relevant attributes and interactions of entities as classes to define an abstract representation of a system.
2.Encapsulation Hiding the internal state and functionality of an object and only allowing access through a public set of functions.
3.Inheritance Ability to create new abstractions based on existing abstractions.
4.Polymorphism Ability to implement inherited properties or methods in different ways across multiple abstractions.

Over time, needs change, and related account types are requested:

1.An interest earning account that accrues interest at the end of each month.
2.A line of credit that can have a negative balance, but when there's a balance, there's an interest charge each month.
3.A pre-paid gift card account that starts with a single deposit, and only can be paid off. It can be refilled once at the start of each month.

### Different overdraft rules
The last feature to add enables the LineOfCreditAccount to charge a fee for going over the credit limit instead of refusing the transaction.

One technique is to define a virtual function where you implement the required behavior. The BankAccount class refactors the MakeWithdrawal method into two methods. The new method does the specified action when the withdrawal takes the balance below the minimum.

