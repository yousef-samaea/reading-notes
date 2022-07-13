# Factory Method

Factory Method is a creational design pattern that provides an interface for creating objects in a superclass, but allows 
subclasses to alter the type of objects that will be created.

The Factory Method pattern suggests that you replace direct object construction calls (using the new operator) with calls to a 
special factory method. Don’t worry: the objects are still created via the new operator, but it’s being called from within the 
factory method. Objects returned by a factory method are often referred to as products.

At first glance, this change may look pointless: we just moved the constructor call from one part of the program to another. 
However, consider this: now you can override the factory method in a subclass and change the class of products being created by 
the method.

There’s a slight limitation though: subclasses may return different types of products only if these products have a common base 
class or interface. Also, the factory method in the base class should have its return type declared as this interface.

### client code

The code that uses the factory method (often called the client code) doesn’t see a difference between the actual products 
returned by various subclasses. The client treats all the products as abstract Transport. The client knows that all transport 
objects are supposed to have the deliver method, but exactly how it works isn’t important to the client.

### Structure

The Creator class declares the factory method that returns new product objects. It’s important that the return type of this 
method matches the product interface.

You can declare the factory method as abstract to force all subclasses to implement their own versions of the method. As an 
alternative, the base factory method can return some default product type.

Note, despite its name, product creation is not the primary responsibility of the creator. Usually, the creator class already has 
some core business logic related to products. The factory method helps to decouple this logic from the concrete product classes. 
Here is an analogy: a large software development company can have a training department for programmers. However, the primary 
function of the company as a whole is still writing code, not producing programmers.

# Pseudocode

The base Dialog class uses different UI elements to render its window. Under various operating systems, these elements may look a 
little bit different, but they should still behave consistently. A button in Windows is still a button in Linux.

When the factory method comes into play, you don’t need to rewrite the logic of the Dialog class for each operating system. If we 
declare a factory method that produces buttons inside the base Dialog class, we can later create a subclass that returns 
Windows-styled buttons from the factory method. The subclass then inherits most of the code from the base class, but, thanks to 
the factory method, can render Windows-looking buttons on the screen.

For this pattern to work, the base Dialog class must work with abstract buttons: a base class or an interface that all concrete 
buttons follow. This way the code within Dialog remains functional, whichever type of buttons it works with.

Of course, you can apply this approach to other UI elements as well. However, with each new factory method you add to the Dialog,
 you get closer to the Abstract Factory pattern. Fear not, we’ll talk about this pattern later.

### Applicability




