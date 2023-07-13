## Classes

- Classes and Reference Types in C#: In C#, a type that is defined as a class is a reference type. When you declare a variable of a reference type, the variable initially contains the value null until you explicitly create an instance of the class with the new keyword, or assign it an object of a compatible type.

- Memory Allocation: When an object is created, memory is allocated on the managed heap for that object, and the variable holds a reference to the location of that object. The memory used by an object is reclaimed through the CLR's automatic memory management functionality, known as garbage collection.

- Declaring Classes: Classes are declared using the class keyword followed by a unique identifier. An optional access modifier can precede the class keyword. The class body defines the behavior and data of the class, which includes fields, properties, methods, and events (class members).

- Creating Objects: Objects are instances of a class and can be created using the new keyword followed by the class name. The reference to the object is passed back to the programmer. You can create an object reference without creating an object, but it's not recommended because trying to access an object through such a reference will fail at runtime.

- Constructors and Initialization: When creating an instance of a class, you often want to ensure that its fields and properties are initialized to useful values. This can be achieved in several ways: accepting default values, field initializers, constructor parameters, and object initializers.

- Class Inheritance: Classes in C# support inheritance, a key characteristic of object-oriented programming. A class can inherit from any other class that isn't defined as sealed, and other classes can inherit from your class and override class virtual methods. A class can only directly inherit from one base class but can indirectly inherit multiple base classes and implement multiple interfaces.

- Abstract and Sealed Classes: A class can be declared as abstract, which means it contains abstract methods with a signature definition but no implementation. Abstract classes can't be instantiated. A sealed class doesn't allow other classes to derive from it.

- Partial Classes: Class definitions can be split between different source files using the partial keyword.

## Constructors

- Role of Constructors: Whenever an instance of a class or struct is created, its constructor is called. Constructors allow programmers to set default values, limit instantiation, and write flexible and easy-to-read code.

- Initialization Process: Initializing a new instance involves several steps. Instance fields are set to zero, field initializers run (starting with the most derived type), base type field initializers run, base instance constructors run (starting from Object through each base class to the direct base class), then the instance constructor for the type runs. If there are any object initializers, they run after the instance constructor, in the textual order.

- Constructor Syntax: A constructor is a method with the same name as its type, it doesn't include a return type. Its method signature includes only an optional access modifier and a parameter list.

- Expression Body Definition: If a constructor can be implemented as a single statement, an expression body definition can be used.

- Static Constructors: A class or struct can have a static constructor, which initializes static members of the type. Static constructors are parameterless and if one is not provided, the C# compiler initializes static fields to their default value.

- Order of Constructor Execution: If the static constructor hasn't run, it runs before any of the instance constructor actions take place.


## Properties

- Properties: These are members that provide a mechanism to read, write, or compute the value of a private field. They allow a class to expose a public way of getting and setting values, while hiding implementation or verification code.

- Get and Set Accessors: These are special methods used to return and assign property values. An init property accessor (C# 9 onwards) assigns a new value only during object construction.

- Access Levels of Properties: Properties can be read-write (both a get and a set accessor), read-only (a get accessor but no set accessor), or write-only (a set accessor, but no get accessor).

- Expression Body Definitions: When properties consist of single-line statements that assign or return an expression, these can be implemented as expression-bodied members.

- Auto-implemented Properties: If the get and set accessors of a property only assign a value to or retrieve a value from a backing field without extra logic, auto-implemented properties can be used. The C# compiler automatically provides the backing field.

- Different Accessibilities: Auto-implemented properties can declare different accessibilities for the get and set accessors, commonly a public get accessor and a private set accessor.

- Required Properties: From C# 11, the required keyword can be added to force client code to initialize any property or field during object creation.

- Understanding properties is crucial in C# as it enables encapsulation - a pillar of Object-Oriented Programming (OOP). It allows developers to protect fields by reading and writing to them through properties and implementing any additional logic as needed.

1. What’s the difference between a static and an instance constructor?

- Instance Constructor: It is used to create and initialize an instance of a class. It can take parameters, which are used to initialize member variables of an instance. Each time you create a new object or an instance of a class, the instance constructor gets called. You can have multiple instance constructors in a class through constructor overloading, each with a different set of parameters.

- Static Constructor: It is used to initialize the type itself, rather than an instance of the type. It is called automatically before any static members are referenced or any static methods are called. It cannot take parameters because you can't explicitly call it. It is mainly used for initializing static fields or to perform a particular action that needs to be performed once only. A class can have only one static constructor.

2. How does the use of a static constructor differ from setting properties/values?

- Static Constructor: It's used to initialize static fields in a class and to execute code that needs to be run only once, before creating any instance of a class or referencing any static members. It's not involved in setting or getting instance field values and does not interact with instance properties.

- Setting Properties/Values: Properties (and fields) in a class hold data. When you create an instance of a class, you often assign initial values to these properties (or fields). These initial values can be passed in via instance constructors. Unlike a static constructor, these operations pertain to the specific instance of the class and not the class itself.

## Stack and Heap

- Stack and Heap: These are two places where .NET framework stores items in memory as the code executes. The Stack keeps track of what's executing in the code, whereas the Heap keeps track of objects.

- Stack vs. Heap: The Stack operates as a series of boxes (frames), stacking another box on top every time a method is called. Once a method finishes, the box is discarded and the control returns to the previous box. The Heap, on the other hand, holds information and can be accessed at any time without constraints.

- Memory Management: The Stack is self-maintaining, discarding unused memory blocks automatically. The Heap, however, relies on Garbage Collection (GC) to keep it clean and free of unused data.

- Data Types on Stack and Heap: There are four types of data that go into the Stack and Heap: Value Types, Reference Types, Pointers, and Instructions.

- Value Types vs Reference Types: Value Types always go where they were declared. If they're declared within a method, they are placed on the Stack. However, if they're declared within a Reference Type, they're placed on the Heap.

- Pointers: Pointers or References are chunks of space in memory that point to another space in memory. These are managed by the CLR.

- Understanding Value Types and Reference Types: When dealing with Reference Types, we are working with pointers to the type, not the object itself. With Value Types, we're working with the actual object. This can lead to different behavior when manipulating variables of these types.

- Impact of GC on Performance: Garbage Collection can be expensive in terms of performance as it halts all running threads to clean and reorganize the Heap. Thus, developers should be mindful of what's being stored in the Stack and Heap when writing high-performance code.

- Difference in Behavior of Value Types and Reference Types: When you assign a Value Type variable to another, a copy is made. But, when you assign one Reference Type variable to another, both point to the same object. Any change made through one variable reflects in the other.

1. Knowing what you now know about the stack and the heap, how might you rethink the way you did projects in previous courses, to make more effecient use of memory?

Use of Value vs Reference Types: Knowing that value types are stored on the stack and reference types are stored on the heap, I would more carefully consider which type of variable to use. For smaller, short-lived variables, value types might be more appropriate. For larger data structures or ones that need to be shared across multiple methods or objects, reference types would be the way to go.

Passing by Reference vs Value: When passing large structures (like arrays or large objects) to methods, I would consider passing them by reference instead of by value. This would avoid creating unnecessary copies and instead use pointers, saving memory and improving performance.

Avoiding Memory Leaks: Understanding how garbage collection works, I would be more careful to set objects to null when I'm done with them, to allow them to be collected. I'd be especially careful with event handlers, as forgetting to unregister them can lead to memory leaks.

Optimizing Recursions: With recursive functions, I'd be more aware that each recursive call adds a new layer to the stack. This could lead to a stack overflow for deep recursion. I might refactor to use iterative solutions where possible.

## Garbage Collection

Benefits of Garbage Collection (GC) in CLR:

Frees developers from having to manually release memory.
Efficiently allocates objects on the managed heap.
Reclaims objects no longer in use, clears their memory, and keeps it available for future allocations.
Provides memory safety by ensuring an object can't use memory allocated for another object.
Fundamentals of Memory:

Each process has its own separate virtual address space. All processes on the same computer share the same physical memory and the page file.
Developers work with virtual address space and never manipulate physical memory directly.
The garbage collector allocates and frees virtual memory on the managed heap.
Virtual memory can be free, reserved, or committed.
Free: The memory has no references to it and is available for allocation.
Reserved: The memory is available for your use but can't be used for any other allocation request until it's committed.
Committed: The memory is assigned to physical storage.
Virtual address space can get fragmented leading to allocation inefficiencies.
The page file is used even if physical memory pressure is low.
Memory Allocation:

When a new process is initialized, the runtime reserves a contiguous region of address space for the process. This is called the managed heap.
The managed heap maintains a pointer to the address where the next object will be allocated.
All reference types are allocated on the managed heap.
Memory for new objects is allocated sequentially as long as address space is available.

Memory Allocation: The runtime allocates memory from the managed heap for an object, which is almost as fast as allocating memory from the stack. New objects are stored contiguously in the managed heap for quick access.

Memory Release: The garbage collector (GC) releases memory for objects not in use. It determines unused objects by examining the application's roots. Memory is compacted only when a collection identifies a significant number of unused objects.

Large Objects: Memory for large objects is allocated in a separate heap to improve performance. This memory is usually not compacted to avoid moving large objects.

Conditions for GC: Garbage collection occurs when physical memory is low, memory used by allocated objects on the managed heap surpasses an acceptable threshold, or the GC.Collect method is called.

The Managed Heap: The garbage collector reserves memory in segments to store and manage objects. This memory is known as the managed heap.

Generations in GC: The managed heap is divided into three generations, 0, 1, and 2, to handle long-lived and short-lived objects separately. Garbage collection primarily happens with the reclamation of short-lived objects.

Ephemeral Generations: Generations 0 and 1, being short-lived, are known as ephemeral generations. These are allocated in the ephemeral segment of the memory.

GC Phases: A garbage collection has three phases - marking, relocating, and compacting.

Unmanaged Resources: Unmanaged resources require explicit cleanup. For objects that encapsulate unmanaged resources, it's recommended to provide a public Dispose method. It's also important to provide a way to release these resources if Dispose isn't called, either by using a safe handle or overriding the Object.Finalize() method.

1. Compare “Garbage Collection” in C# with the lifecycle of normal household items.

-comparing to the lifecycle of a waterbottle

Creation/Allocation (Acquisition of a Water Bottle): In the context of C#, when you create an object using the new keyword, memory is allocated on the heap. This is similar to buying a new water bottle. The bottle is now yours, and you have a place for it in your kitchen (the memory allocated in your program).

Usage (Use of the Water Bottle): Just like using the water bottle for its purpose (drinking water), in C#, the object created would be used in the program for the purpose it was created for.

De-Reference (Stop Using the Water Bottle): Now, suppose you've decided to stop using the water bottle because it's old and worn out. You don't throw it away just yet, but you no longer use it. Similarly, in C#, an object becomes eligible for garbage collection when it's no longer accessible, i.e., it's no longer referenced by any part of your program.

Collection (Deciding to Dispose of the Water Bottle): Once you've decided to get rid of the bottle, you place it in the trash can. In C#, this would be when the Garbage Collector decides to free up the memory used by de-referenced objects. Garbage Collector determines that the objects are no longer in use because they can't be reached from the roots of the application.

Compaction (Taking Out the Trash): Finally, when the trash is taken out, the bottle is physically gone from your home, freeing up space. In C#, this would be when the Garbage Collector compacts the memory, shifting the remaining referenced objects to clear up a continuous free space, and updating the references accordingly.
