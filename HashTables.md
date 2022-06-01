# Hash Tables

The Hashtable in C# is a collection that stores (Keys, Values) pairs. Here, the Keys are used to find the storage location. A 
HashTable is immutable and cannot have duplicate entries. The .Net Framework has provided a HashTable class that contains all the 
functionality required to implement a hashtable without any extra coding.

A hashtable is a general-purpose dictionary collection. Each item within the collection is a DictionaryEntry object with two 

properties: a key object and a value object. These are known as Key/Value pairs. When items are added to a hash table, a hash 
code is generated automatically. This code is hidden from the developer. All access to the table's values is achieved using the 
key object for identification. As the items in the collection are sorted according to the hidden hash code, the items should be 
considered to be randomly ordered.

### The Hashtable Collection
 
The Base Class libraries offers a Hashtable Class that is defined in the System.Collections namespace, so you don't have to code 
your own hash tables. It processes each key of the hash that you add every time and then uses the hash code to look up the 
element very quickly. The capacity of a hash table is the number of elements the hash table can hold. As elements are added to a 
hash table, the capacity is automatically increased as required through reallocation. It is an older .Net Framework type.
 
 ### Declaring a Hashtable
 
The Hashtable class is generally found in the namespace called System.Collections. So to execute any of the examples, we have to 
add using System.Collections; to the source code. The declaration for the Hashtable is:

<!-- Hashtable HT = new Hashtable();   -->

This new Hashtable has the limited capacity and when the limit is reached then the capacity is automatically increased to allow 
for further storage. Since the nature of the Hashtable dictionary is that the capacity is always considered to be approximate we 
can set the initial approximate capacity by passing the integer parameter to the constructor as: 

<!-- Hashtable HT = new Hashtable(100);   -->

This is useful when the maximum size of the collection is known because it removes the need of resizing the hash table and also 
it increases the performance.

### Properties of Hashtable
 
Some of the important properties of a hash table are:

1. Comparer: Gets or Sets the IComparer to use for the Hash Table.
2. Count: Gets the number of key/value pairs contained in the hash table.
3. IsReadOnly: Get a value indicating whether the hash table is read-only.
4. Item: Gets or Sets the value associated with the specified Key.
5. Keys: Gets an ICollection containing the keys in the hash table.
6. Values: Gets an ICollection containing the values in the hash table.

### Methods of Hashtable
 
Some of the important methods of a hash table are:

1. Add: Adds an element with the specified key and value in the hash table.
2. Clear: Removes all the elements in the hash table.
3. ContainsKey: Determined whether the hash table contains a specified key or not.
4. ContainsValue: Determined whether the hash table contains a specified value or not.

A hash table does not maintain an ordered collection; there is no specific order to the collection of keys or values obtained. 
Each element is a key/value pair stored in a DictionaryEntry object. A key cannot be a nullptr, but a value can be.

### Advantages of Hashtable

1. It allows the execution time of look up, retrieve, and set operations to remain nearly constant, even for large sets.
2. It has the ability to locate the items qickly even when the amount of data is huge.
3. No requirement to scan through the entire data set to find an item or to sort the set in order to perform a Binary search.
4. The key can be hashed and the value's location found directly, if the key for a desired data value is known.







