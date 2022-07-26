# Collections & Enums

## Collections:

Collections provide a more flexible way to work with groups of objects. Unlike arrays, the group of objects you work with can grow and shrink dynamically as the needs of the application change, A collection is a class, so you must declare an instance of the class before you can add elements to that collection.

### how to Use a Simple Collection : 

// Create a list of strings.
var salmons = new List<string>();
salmons.Add("chinook");
salmons.Add("coho");
salmons.Add("pink");
salmons.Add("sockeye");

// Iterate through the list.
foreach (var salmon in salmons)
{
    Console.Write(salmon + " ");
}
// Output: chinook coho pink sockeye


## Kinds of Collections:

Some of the common collection classes are described in this section:

1.System.Collections.Generic classes

2.System.Collections.Concurrent classes

3.System.Collections classes


### System.Collections.Generic Classes

You can create a generic collection by using one of the classes in the System.Collections.Generic namespace. A generic collection is useful when every item in the collection has the same data type. A generic collection enforces strong typing by allowing only the desired data type to be added.


### System.Collections.Concurrent Classes

In .NET Framework 4 and later versions, the collections in the System.Collections.Concurrent namespace provide efficient thread-safe operations for accessing collection items from multiple threads, The classes in the System.Collections.Concurrent namespace should be used instead of the corresponding types in the System.Collections.Generic and System.Collections namespaces whenever multiple threads are accessing the collection concurrently.

### System.Collections Classes

The classes in the System.Collections namespace do not store elements as specifically typed objects, but as objects of type Object, Whenever possible, you should use the generic collections in the System.Collections.Generic namespace or the System.Collections.Concurrent namespace instead of the legacy types in the System.Collections namespace.

### Implementing a Collection of Key/Value Pairs

The Dictionary<TKey,TValue> generic collection enables you to access to elements in a collection by using the key of each element. Each addition to the dictionary consists of a value and its associated key. Retrieving a value by using its key is fast because the Dictionary class is implemented as a hash table.

### Sorting a Collection

The following example illustrates a procedure for sorting a collection. The example sorts instances of the Car class that are stored in a List. The Car class implements the IComparable interface, which requires that the CompareTo method be implemented.

Each call to the CompareTo method makes a single comparison that is used for sorting. User-written code in the CompareTo method returns a value for each comparison of the current object with another object. The value returned is less than zero if the current object is less than the other object, greater than zero if the current object is greater than the other object, and zero if they are equal. 


## Enumeration types :

An enumeration type (or enum type) is a value type defined by a set of named constants of the underlying integral numeric type. To define an enumeration type, use the enum keyword and specify the names of enum members, By default, the associated constant values of enum members are of type int; they start with zero and increase by one following the definition text order.

### Enumeration types as bit flags

If you want an enumeration type to represent a combination of choices, define enum members for those choices such that an individual choice is a bit field. That is, the associated values of those enum members should be the powers of two. Then, you can use the bitwise logical operators | or & to combine choices or intersect combinations of choices, respectively. To indicate that an enumeration type declares bit fields.

### The System.Enum type and enum constraint

The System.Enum type is the abstract base class of all enumeration types. It provides a number of methods to get information about an enumeration type and its values. For more information and examples, see the System.Enum API reference page.

### Conversions

For any enumeration type, there exist explicit conversions between the enumeration type and its underlying integral type. If you cast an enum value to its underlying type, the result is the associated integral value of an enum member.







