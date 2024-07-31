<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="right">
      <a href="./02_properties.md">Properties▶️</a>
    </td>
  </tr>
</table>

# Introduction to Object-Oriented Programming in C#

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of "objects," which can contain data in the form of fields (attributes or properties) and code in the form of procedures (methods). In C#, OOP allows you to organize and structure code in a way that makes it easier to understand, maintain, and scale.

## Classes and Objects

To work with objects in C#, you first need to define a class. A class is a blueprint that describes the data and behaviors of the objects that will be created from it. An object is an instance of a class, meaning it is a concrete realization of the structure defined by the class.

### Creating a Class

A class in C# is defined using the class keyword, followed by the class name and a body that contains its members (properties, methods, etc.)

```csharp
public class Person
{
    // Properties of the class
    public string Name { get; set; }
    public int Age { get; set; }

    // Constructor of the class
    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    // Method of the class
    public void IntroduceYourself()
    {
        Console.WriteLine($"Hello, my name is {Name} and I am {Age} years old.");
    }
}
```

### Constructors

A constructor is a special method that is called automatically when a new instance of the class is created. Its main purpose is to initialize the object's data. In C#, the constructor has the same name as the class and does not have a return type.

In the example above, the constructor of the `Person` class takes two parameters (`name` and `age`) and assigns them to the corresponding properties.

### Creating Objects
To create an object in C#, you use the `new` keyword, followed by the class name and the necessary arguments for the constructor.

```csharp
// Creating an object of the Person class
Person person1 = new Person("John", 30);

// Creating another object of the Person class
var person2 = new Person("Mario", 25);

// Calling the IntroduceYourself method of the object
person1.IntroduceYourself(); // Hello, my name is Jhon and I am 30 years old.
person2.IntroduceYourself(); // Hello, my name is Mario and I am 25 years old.
```
## The Pillars of Object-Oriented Programming in C#
Object-Oriented Programming (OOP) is built upon four fundamental principles: Inheritance, Encapsulation, Polymorphism, and Abstraction. These pillars help in designing robust, maintainable, and scalable software systems.

### Inheritance
Inheritance allows a class to inherit properties and methods from another class. This promotes code reuse and establishes a natural hierarchy between classes.

### Encapsulation
Encapsulation involves hiding the internal state and behavior of an object, exposing only what is necessary. This is achieved using access modifiers to ensure controlled access.

### Polymorphism
Polymorphism allows objects of different classes to be treated as objects of a common base class. This is achieved through method overriding and interfaces, enabling different behaviors to be accessed through the same interface.

### Abstraction
Abstraction simplifies complex systems by highlighting the essential features while hiding non-essential details. This is typically done using abstract classes and interfaces.