<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
    <tr>
        <td align="left">
            <a href="./01_basic.md">◀️Basic</a>
        </td>
        <td align="right">
            <a href="#">▶️</a>
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