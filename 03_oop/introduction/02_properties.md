<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
    <tr>
        <td align="left">
            <a href="./01_basic.md">◀️Basic</a>
        </td>
        <td align="right">
            <a href="./03_constructors.md">Constructors▶️</a>
        </td>
    </tr>
</table>

# Properties in Classes

Properties in C# are class members that provide a flexible way to read, write, or compute the values of private fields. Properties are used as data access methods, allowing greater control over how class field values are accessed and modified.

## Definition and Use of Properties

A property typically consists of a get block and a set block. The get block is used to return the property value, while the set block is used to assign a value to the property.

```csharp
public class Person
{
    private string name;
    private int age;

    public string Name
    {
        get { return name; }
        set { name = value; }
    }

    public int Age
    {
        get { return age; }
        set
        {
            if (value >= 0)
            {
                age = value;
            }
        }
    }
}

```
In this example, the Person class has two private fields, name and age. Public properties Name and Age are used to access and modify these fields.

```csharp
Person person = new Person();
person.Name = "John";
person.Age = 30;

Console.WriteLine($"Name: {person.Name}, Age: {person.Age}"); // Name: John, Age: 30
```

## Properties with Methods
You can also use methods to access and modify field values. This approach provides more control and is useful when additional logic is needed.

Instead of using a property, you might define a method to get or set a value.

```csharp
public class Person
{
    private string name;
    private int age;

    // Method to get the name
    public string GetName()
    {
        return name;
    }

    // Method to set the name
    public void SetName(string name)
    {
        this.name = name;
    }

    // Method to get the age
    public int GetAge()
    {
        return age;
    }

    // Method to set the age with validation
    public void SetAge(int age)
    {
        if (age >= 0)
        {
            this.age = age;
        }
    }
}
```
In this example, methods `GetName`, `SetName`, `GetAge`, and `SetAge` are used to access and modify the `name` and `age` fields. This approach allows for additional validation or logic when setting values.

```csharp
Person person = new Person();
person.SetName("Lucas");
person.SetAge(37);

Console.WriteLine($"Name: {person.GetName()}, Age: {person.GetAge()}"); // Name: Lucas, Age: 37
```

## Automatic Properties
Automatic properties allow you to define a property without explicitly declaring a private field. The compiler takes care of creating the private field in the background.

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}
```
In this example, the properties `Name` and `Age` are automatic properties. There is no need to explicitly declare private fields for these properties.

```csharp
Person person = new Person();
person.Name = "Maria";
person.Age = 25;

Console.WriteLine($"Name: {person.Name}, Age: {person.Age}"); // Name: Maria, Age: 25
```