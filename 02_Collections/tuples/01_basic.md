<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
    <tr>
        <td align="left">
            <a href="../lists/02_list_methods_and_properties.md">◀️List methods and properties</a>
        </td>
        <td align="right">
            <a href="../linq/01_introduction.md">LINQ▶️</a>
        </td>
    </tr>
</table>

# Tuples in C#

A tuple is a lightweight structure that groups several values, possibly of different types, into a single unit. Unlike arrays and lists, which store many elements of the same type, a tuple combines a fixed set of related values without needing to create a class.

## Creating a Tuple

A tuple is created by writing the values between parentheses, separated by commas.

```csharp
var person = ("Ana", 25);

Console.WriteLine(person.Item1); // Ana
Console.WriteLine(person.Item2); // 25
```

By default, the elements are accessed with the names `Item1`, `Item2`, `Item3`, and so on, in the order they were declared.

## Named Elements

The `ItemN` names are not descriptive, so tuples allow you to give each element a meaningful name. This makes the code much easier to read.

```csharp
var person = (Name: "Ana", Age: 25);

Console.WriteLine(person.Name); // Ana
Console.WriteLine(person.Age);  // 25
```

You can also declare the names in the type of the variable:

```csharp
(string Name, int Age) person = ("Carlos", 30);

Console.WriteLine($"{person.Name} is {person.Age} years old."); // Carlos is 30 years old.
```

> [!IMPORTANT]
> Always prefer named elements over `Item1`, `Item2`... A tuple like `(decimal Price, int Quantity)` explains itself; `(Item1, Item2)` forces the reader to guess.

## Returning Multiple Values from a Method

The most common use of tuples is returning several values from a method with a single `return`. This is the modern alternative to `out` parameters, covered in the methods section.

```csharp
static (int Quotient, int Remainder) Divide(int dividend, int divisor)
{
    return (dividend / divisor, dividend % divisor);
}

var result = Divide(17, 5);
Console.WriteLine($"Quotient: {result.Quotient}, Remainder: {result.Remainder}");
// Quotient: 3, Remainder: 2
```

## Deconstruction

A tuple can be "unpacked" into separate variables in a single line. This is called deconstruction.

```csharp
var (name, age) = ("Laura", 28);

Console.WriteLine(name); // Laura
Console.WriteLine(age);  // 28
```

It works naturally with methods that return tuples:

```csharp
var (quotient, remainder) = Divide(17, 5);
Console.WriteLine($"Quotient: {quotient}, Remainder: {remainder}");
```

If you do not need one of the values, you can ignore it with a discard (`_`):

```csharp
var (quotient, _) = Divide(17, 5); // ignores the remainder
```

## Comparing Tuples

Two tuples are equal if all their elements are equal, compared in order. This makes them handy for comparing several values at once.

```csharp
var pointA = (2, 3);
var pointB = (2, 3);

Console.WriteLine(pointA == pointB); // True
```

## Tuples in Collections

Tuples can be combined with the collections you already know, for example a list of pairs:

```csharp
var products = new List<(string Name, decimal Price)>
{
    ("Laptop", 1500.99m),
    ("Mouse", 25.50m),
    ("Keyboard", 45.00m)
};

foreach (var (name, price) in products)
{
    Console.WriteLine($"{name}: {price:C}");
}
```

Tuples are ideal for grouping a few related values temporarily. When the group of data has its own behavior or is used throughout the program, a class is the better choice, as you will see in the OOP section.
