
Arrays: In C#, an array is a data structure that holds a fixed number of elements of a single, specific data type. The size of an array must be specified at the time of its declaration and cannot be changed later.

``` csharp
int[] array = new int[5]; // declares an array of integers with size 5
```

Collections: Collections in C# are a way to group similar items together. Unlike arrays, collections can be resized dynamically, allowing for more flexibility. Collections come in several types such as Lists, Dictionaries, Queues, Stacks etc.

``` csharp
List<int> list = new List<int>(); // declares a new list of integers
```

List Iteration: There are several ways to iterate over collections in C#. The foreach loop is commonly used to iterate over each item in a collection:

```csharp
List<string> salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };

foreach (var salmon in salmons)
{
    Console.Write(salmon + " ");
}
// Output: chinook coho pink sockeye
```
Alternatively, you can use a `for` loop to iterate over collections by using the index of each element:

```csharp
for (int i = 0; i < salmons.Count; i++)
{
    Console.Write(salmons[i] + " ");
}
// Output: chinook coho pink sockeye
```

Generic Collections: Generic collections are the same as collections, but they are type-safe. This means you specify the type of elements the collection can contain, which provides type checking and eliminates the need for type conversion. The List `<T>`  class is a generic class and can be used for this purpose.

```csharp
List<int> numbers = new List<int>(); // A list that can only contain integers.
```

LINQ: Language Integrated Query (LINQ) in C# is a powerful feature that allows you to work with data in a more intuitive and flexible way. It enables you to write queries directly in C# to manipulate data.

```csharp
var sortedSalmons = from salmon in salmons
                    orderby salmon
                    select salmon;
```

Sorting Collections: In C#, you can sort a collection by using the Sort() method, or by using LINQ.

```csharp

salmons.Sort(); // sorts the list of salmons in-place
Custom Collections: You can also create your own custom collections by implementing certain interfaces such as IEnumerable, ICollection, or IList. 
```








```// Create a list of strings by using a
// collection initializer.
var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };

for (var index = 0; index < salmons.Count; index++)
{
    Console.Write(salmons[index] + " ");
}
// Output: chinook coho pink sockeye
```
The following example removes an element from the collection by specifying the object to remove.

```csharp

// Create a list of strings by using a
// collection initializer.
var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };

// Remove an element from the list by specifying
// the object.
salmons.Remove("coho");

// Iterate through the list.
foreach (var salmon in salmons)
{
    Console.Write(salmon + " ");
}
// Output: chinook pink sockeye
```
- The following example removes elements from a generic list. Instead of a foreach statement, a for statement that iterates in descending order is used. This is because the RemoveAt method causes elements after a removed element to have a lower index value.

```csharp
var numbers = new List<int> { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };

// Remove odd numbers.
for (var index = numbers.Count - 1; index >= 0; index--)
{
    if (numbers[index] % 2 == 1)
    {
        // Remove the element by specifying
        // the zero-based index in the list.
        numbers.RemoveAt(index);
    }
}

// Iterate through the list.
// A lambda expression is placed in the ForEach method
// of the List(T) object.
numbers.ForEach(
    number => Console.Write(number + " "));
// Output: 0 2 4 6 8
```
For the type of elements in the List<T>, you can also define your own class. In the following example, the Galaxy class that is used by the List<T> is defined in the code.

```csharp 
private static void IterateThroughList()
{
    var theGalaxies = new List<Galaxy>
        {
            new Galaxy() { Name="Tadpole", MegaLightYears=400},
            new Galaxy() { Name="Pinwheel", MegaLightYears=25},
            new Galaxy() { Name="Milky Way", MegaLightYears=0},
            new Galaxy() { Name="Andromeda", MegaLightYears=3}
        };

    foreach (Galaxy theGalaxy in theGalaxies)
    {
        Console.WriteLine(theGalaxy.Name + "  " + theGalaxy.MegaLightYears);
    }

    // Output:
    //  Tadpole  400
    //  Pinwheel  25
    //  Milky Way  0
    //  Andromeda  3
}

public class Galaxy
{
    public string Name { get; set; }
    public int MegaLightYears { get; set; }
}
```

- System.Collections.Generic Classes
You can create a generic collection by using one of the classes in the System.Collections.Generic namespace. A generic collection is useful when every item in the collection has the same data type. A generic collection enforces strong typing by allowing only the desired data type to be added.

- The following table lists some of the frequently used classes of the System.Collections.Generic namespace:

- Class	Description
Dictionary `<TKey,TValue>`	Represents a collection of key/value pairs that are organized based on the key.
List `<T>`	Represents a list of objects that can be accessed by index. Provides methods to search, sort, and modify lists.
Queue  `<T>` Represents a first in, first out (FIFO) collection of objects.
SortedList `<TKey,TValue>`	Represents a collection of key/value pairs that are sorted by key based on the associated IComparer `<T>` implementation.
Stack `<T>` Represents a last in, first out (LIFO) collection of objects.

For additional information, see Commonly Used Collection Types, Selecting a Collection Class, and System.Collections.Generic.


- System.Collections.Concurrent Classes
In .NET Framework 4 and later versions, the collections in the System.Collections.Concurrent namespace provide efficient thread-safe operations for accessing collection items from multiple threads.

- The classes in the System.Collections.Concurrent namespace should be used instead of the corresponding types in the System.Collections.Generic and System.Collections namespaces whenever multiple threads are accessing the collection concurrently. For more information, see Thread-Safe Collections and System.Collections.Concurrent.



- Removing Elements From Collections: In C#, you can remove elements from a collection in several ways. Using the Remove method, you can remove an item by specifying the item itself:

```csharp
var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };
salmons.Remove("coho"); // removes "coho" from the list
```

- You can also use the RemoveAt method to remove an item at a specific index. Note that when you use RemoveAt, the indices of the subsequent items will shift down:

```csharp

var numbers = new List<int> { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
for (var index = numbers.Count - 1; index >= 0; index--)
{
    if (numbers[index] % 2 == 1)
    {
        numbers.RemoveAt(index);
    }
}
```

- Custom Classes in Collections: Collections can also contain custom classes. This enables you to group objects of the same class together:

```csharp
public class Galaxy
{
    public string Name { get; set; }
    public int MegaLightYears { get; set; }
}

var theGalaxies = new List<Galaxy>
{
    new Galaxy() { Name="Tadpole", MegaLightYears=400},
    new Galaxy() { Name="Pinwheel", MegaLightYears=25},
    new Galaxy() { Name="Milky Way", MegaLightYears=0},
    new Galaxy() { Name="Andromeda", MegaLightYears=3}
};
```

- Types of Collections: .NET provides various types of collections for different purposes:

- Generic Collections: Provided by System.Collections.Generic, these collections enforce strong typing, meaning they only allow elements of a specified type. Classes include Dictionary `<TKey,TValue>`, List `<T>`, Queue `<T>`, SortedList `<TKey,TValue>`, and Stack `<T>`.

- Concurrent Collections: Provided by System.Collections.Concurrent, these collections are designed to be safe to use from multiple threads concurrently. They should be used whenever multiple threads are accessing the collection at the same time. Examples include BlockingCollection `<T>`, ConcurrentDictionary `<TKey,TValue>`, ConcurrentQueue `<T>`, and ConcurrentStack `<T>`.

- The choice of which collection type to use depends on the specific requirements of your program, including factors like what operations you need to perform on the collection, how many elements the collection will contain, and whether you need thread-safety.

Enumeration Types: An enumeration (or enum) is a distinct type consisting of a set of named constants called the enumerator list. In C#, you define an enum using the enum keyword. By default, the underlying type of these enumeration elements is int.

```csharp

enum Season
{
    Spring,
    Summer,
    Autumn,
    Winter
}
```
Specifying Underlying Type and Values: You can specify a different underlying type (any integral type except char) and explicitly set the values for the enumeration elements.

```csharp

enum ErrorCode : ushort
{
    None = 0,
    Unknown = 1,
    ConnectionLost = 100,
    OutlierReading = 200
}
```
Enum as Bit Flags: You can use an enum to represent a combination of choices (flags) by assigning powers of two to its members. Apply the Flags attribute to indicate that an enum represents bit fields.

```csharp

[Flags]
public enum Days
{
    None      = 0,
    Monday    = 1,
    Tuesday   = 2,
    Wednesday = 4,
    // ...
    Weekend   = Saturday | Sunday
}
```
Then, you can use bitwise operators to combine or check flags.

System.Enum Type: This is the abstract base class of all enum types, providing various methods to get information about an enumeration type and its values. It can also be used as a constraint for type parameters in generic code.

Conversions: You can explicitly convert (cast) an enum to its underlying type, and vice versa. If you cast an enum to its underlying type, you'll get the integer associated with that enum member.

```csharp

Season a = Season.Autumn;
Console.WriteLine($"Integral value of {a} is {(int)a}");  // Output: Integral value of Autumn is 2
```
You can also convert integer values back to an enum. However, the value must correspond to a defined enum member, otherwise, the integer value itself will be displayed.

```csharp

var c = (Season)4;
Console.WriteLine(c);  // Output: 4
```
You can use Enum.IsDefined to check if a certain value corresponds to an enum member.

Boxing and Unboxing: Enumeration types can be boxed and unboxed to and from the System.Enum type. This means you can convert an enum value to System.Enum (boxing) and back to the specific enum type (unboxing).


