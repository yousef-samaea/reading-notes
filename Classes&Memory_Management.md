# classes

The class keyword is preceded by the access level. Because public is used in this case, anyone can create instances of this class. The name of the class follows the class keyword. The name of the class must be a valid C# identifier name. The remainder of the definition is the class body, where the behavior and data are defined. Fields, properties, methods, and events on a class are collectively referred to as class members.

when you declare a variable of a reference type, the variable contains the value null until you explicitly create an instance of the class by using the new operator, or assign it an object of a compatible type that may have been created elsewhere.
When the object is created, enough memory is allocated on the managed heap for that specific object, and the variable holds only a reference to the location of said object. Types on the managed heap require overhead both when they are allocated and when they are reclaimed by the automatic memory management functionality of the CLR, which is known as garbage collection.

### Constructors:

A class or struct may have multiple constructors that take different arguments. Constructors enable the programmer to set default values, limit instantiation, and write code that is flexible and easy to read.
A constructor is a method whose name is the same as the name of its type. Its method signature includes only an optional access modifier,If a constructor can be implemented as a single statement, you can use an expression body definitionThe previous examples have all shown instance constructors, which create a new object. A class or struct can also have a static constructor, which initializes static members of the type.



### Properties
A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field. Properties can be used as if they are public data members, but they are actually special methods called accessors. This enables data to be accessed easily and still helps promote the safety and flexibility of methods.

Properties enable a class to expose a public way of getting and setting values, while hiding implementation or verification code,Properties can be read-write (they have both a get and a set accessor), read-only (they have a get accessor but no set accessor), or write-only (they have a set accessor, but no get accessor). Write-only properties are rare and are most commonly used to restrict access to sensitive data.

### vStack and Heap 

The Stack is more or less responsible for keeping track of what's executing in our code (or what's been "called").  The Heap is more or less responsible for keeping track of our objects (our data, well... most of it - we'll get to that later.).
 
### Garbage Collection Fundamentals

In the common language runtime (CLR), the garbage collector (GC) serves as an automatic memory manager. The garbage collector manages the allocation and release of memory for an application.

Benefits :
1.Frees developers from having to manually release memory.

2.Allocates objects on the managed heap efficiently.

3.Reclaims objects that are no longer being used, clears their memory, and keeps the memory available for future allocations. Managed objects automatically get clean content to start with, so their constructors don't have to initialize every data field.

4.Provides memory safety by making sure that an object cannot use for itself the memory allocated for another object.




