<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
    <tr>
        <td align="left">
            <a href="./02_properties.md">◀️Properties</a>
        </td>
        <td align="right">
            <a href="#">▶️</a>
        </td>
    </tr>
</table>

# Constructors in C#

Constructors in C# are special methods that are automatically called when an instance of a class is created. They are used to initialize the object's state and set default values for its fields. Constructors can be overloaded to provide different ways to initialize objects.

## Basic Constructor

A constructor has the same name as the class and does not have a return type. Its main purpose is to initialize the object's fields or properties when the object is instantiated.

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    // Constructor
    public Person()
    {
        Name = "mario";
        Age = 21;
    }
}

```
In this example, the `Person` class has a constructor that initializes `Name` to `"mario"` and `Age` to `21`. This constructor is called when a new instance of `Person` is created without any arguments.

```csharp
Person person = new Person();
Console.WriteLine($"Name: {person.Name}, Age: {person.Age}"); // Name: mario, Age: 21
```
> [!IMPORTANT]
> all objects are created with the same data by default and therefore it is not good practice to leave them said

## Parameterized Constructor

Constructors can also take parameters to initialize the object with specific values.

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    // Parameterized Constructor
    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }
}
```
In this example, the `Person` class has a parameterized constructor that allows you to set `Name` and `Age` when creating an instance of `Person`.

```csharp
Person person = new Person("John", 30);
Console.WriteLine($"Name: {person.Name}, Age: {person.Age}"); // Name: John, Age: 30
```

## Overloaded Constructors

You can have multiple constructors in a class, each with different parameters. This is known as constructor overloading.

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    // It is left empty to access the properties and methods of the class without having to create a new object.
    public Person(){}

    // Parameterized Constructor
    public Person(string name)
    {
        Name = name;
        Age = 0;
    }

    // Parameterized Constructor with Age
    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }
}
```
In this example, the Person class has three constructors:

1. It is left empty to access the properties and methods of the class without having to create a new object.
2. The second constructor initializes Name with a specified value and Age to 0.
3. The third constructor initializes both Name and Age with specified values.

```csharp
Person instance = new Person();
Person person2 = new Person("Maria");
Person person3 = new Person("Carlos", 40);

Console.WriteLine($"Person2 - Name: {person2.Name}, Age: {person2.Age}"); // Name: Maria, Age: 0
Console.WriteLine($"Person3 - Name: {person3.Name}, Age: {person3.Age}"); // Name: Carlos, Age: 40
```