## Inheritance

- Inheritance in Object-Oriented Programming (OOP): Inheritance, along with encapsulation and polymorphism, is one of the three primary characteristics of OOP. It allows the creation of new classes that reuse, extend, and modify behavior defined in other classes. The class from which members are inherited is called the base class, and the class that inherits is the derived class.

- Inheritance Hierarchy: A derived class can have only one direct base class, but inheritance is transitive. If Class C is derived from Class B, which is derived from Class A, then Class C inherits the members declared in Class B and Class A.

- Structures vs Classes: Structures do not support inheritance, unlike classes, but they can implement interfaces.

- Default Implementation in Interfaces: Interface declarations may define a default implementation for its members. These implementations are inherited by derived interfaces and by classes that implement those interfaces.

- Access to Base Class Members: When a class is defined to derive from another class, the derived class implicitly gains all the members of the base class, except for its constructors and finalizers.

- Abstract and Virtual Methods: When a base class declares a method as virtual, a derived class can override the method with its own implementation. If a base class declares a member as abstract, that method must be overridden in any non-abstract class that directly inherits from that class.

Abstract Base Classes: You can declare a class as abstract if you want to prevent direct instantiation by using the new operator. An abstract class can be used only if a new class is derived from it.

- Interfaces: An interface is a reference type that defines a set of members. All classes and structs that implement that interface must implement that set of members. A class can implement multiple interfaces even though it can derive from only a single direct base class.

- Preventing Further Derivation: A class can prevent other classes from inheriting from it, or from any of its members, by declaring itself or the member as sealed.

- Derived Class Hiding of Base Class Members: A derived class can hide base class members by declaring members with the same name and signature. The new modifier can be used to explicitly indicate that the member isn't intended to be an override of the base member.


## Abstract Classes and Class Members:

- An abstract class cannot be instantiated. It provides a common definition of a base class that multiple derived classes can share.
Abstract classes may also define abstract methods which have no implementation and must be implemented in a derived class.

- If a virtual method is declared abstract, it is still virtual to any class inheriting from the abstract class. A class inheriting an abstract method cannot access the original implementation of the method.

Example:

```C#
Copy code
public abstract class A
{
    public abstract void DoWork(int i);
} 
```

Sealed Classes and Class Members:

- A sealed class cannot be used as a base class. For this reason, it cannot also be an abstract class.
- Sealed classes prevent derivation. This allows for some runtime optimizations, making calling sealed class members slightly faster.
- A method, indexer, property, or event, on a derived class that is overriding a virtual member of the base class can declare that member as sealed, negating the virtual aspect of the member for any further derived class.

Example:


```public sealed class D
{
    // Class members here.
} 


public class D : C
{
    public sealed override void DoWork() { }
}
```

## Polymorphism in Object-Oriented Programming:

- Polymorphism is one of the three pillars of Object-Oriented Programming (OOP), alongside encapsulation and inheritance. It allows objects of a derived class to be treated as objects of a base class in certain scenarios like method parameters and collections or arrays.
Base classes may define and implement virtual methods, and derived classes can override them. This means they provide their own definition and implementation.
At runtime, when client code calls the method, the Common Language Runtime (CLR) looks up the run-time type of the object, and invokes that override of the virtual method.
Virtual Members:

- Derived classes may override virtual members in the base class, defining new behavior.
- Derived classes may inherit the closest base class method without overriding it.
- Derived classes may define new non-virtual implementations of those members that hide the base class implementations.
Hiding Base Class Members with New Members:

- The 'new' keyword can be used to hide a base class member with the same name in a derived class.
Preventing Derived Classes from Overriding Virtual Members:

- Derived classes can stop virtual inheritance by declaring an override as 'sealed'. This stops further inheritance of the method.
Sealed methods can be replaced by derived classes by using the 'new' keyword.
Accessing Base Class Virtual Members from Derived Classes:

- A derived class that has replaced or overridden a method or property can still access the method or property on the base class using the 'base' keyword.

Example of Polymorphism:

```public class Shape
{
    public virtual void Draw()
    {
        Console.WriteLine("Performing base class drawing tasks");
    }
}

public class Circle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle");
        base.Draw();
    }
}


public class Rectangle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a rectangle");
        base.Draw();
    }
}

public class Triangle : Shape
{
    public override void Draw()
    {
        Console.WriteLine("Drawing a triangle");
        base.Draw();
    }
}

var shapes = new List<Shape>
{
    new Rectangle(),
    new Triangle(),
    new Circle()
};

foreach (var shape in shapes)
{
    shape.Draw();
}
```


In this example, each shape (Rectangle, Triangle, Circle) overrides the Draw method of the Shape base class. However, when called through a Shape reference, the appropriate derived Draw method is invoked, demonstrating polymorphism.

## Object Oriented Programming 

- Object-oriented programming (OOP) is a programming paradigm that focuses on modeling real-world entities as objects that have attributes and behaviors.
- The four basic principles of OOP are abstraction, encapsulation, inheritance, and polymorphism.
Abstraction involves modeling relevant attributes and interactions of entities as classes to define an abstract representation of a system.
Encapsulation is the process of hiding the internal state and functionality of an object and only allowing access through a public set of functions.

- Inheritance allows the creation of new abstractions based on existing abstractions. It enables derived classes to inherit properties and methods from a base class.
Polymorphism enables the implementation of inherited properties or methods in different ways across multiple abstractions.
In C#, classes can be used to represent real-world entities, and objects can be created from these classes.

- The BankAccount class is introduced as an example, which provides an abstraction for the concept of a bank account and demonstrates abstraction and encapsulation.
To create different types of accounts, such as interest-earning accounts, line of credit accounts, and gift card accounts, inheritance is used. New classes are created that inherit from the BankAccount class.

- Each derived class inherits the shared behavior from the base class and can provide its own implementation of additional functionality.
Polymorphism is used to implement specific behaviors for each account type by using virtual methods in the base class and overriding them in the derived classes.
Constructors are responsible for initializing objects. Derived classes must explicitly call the base class constructor using the base() syntax.

- The article provides code examples for implementing new functionalities in the derived classes, such as month-end transactions for interest-earning accounts, line of credit accounts, and gift card accounts.

- The article also discusses the need to handle different overdraft rules for the LineOfCreditAccount class, which is achieved by using a virtual method and overriding it in the derived class.