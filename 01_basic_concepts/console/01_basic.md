<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="../variables/01_basic.md">◀️Variables</a>
    </td>
    <td align="right">
      <a href="../strings/01_basic.md">Strings▶️</a>
    </td>
  </tr>
</table>

# Console Input and Output in C#

The `Console` class allows a program to communicate with the user through the terminal: printing messages (output) and reading what the user types (input). It is the main way to interact with console applications.

## Console.WriteLine and Console.Write

`Console.WriteLine()` prints a message and moves to the next line. `Console.Write()` prints a message but stays on the same line.

```csharp
Console.WriteLine("Hello, world!"); // prints and jumps to the next line
Console.Write("Enter your name: "); // prints and stays on the same line
```

You can print variables using string interpolation (`$""`):

```csharp
string name = "Carlos";
int age = 28;

Console.WriteLine($"Name: {name}, Age: {age}"); // Name: Carlos, Age: 28
```

## Console.ReadLine

`Console.ReadLine()` reads a full line of text typed by the user and returns it as a `string`.

```csharp
Console.Write("Enter your name: ");
string name = Console.ReadLine(); // waits for the user to type and press Enter

Console.WriteLine($"Welcome, {name}!");
```

> [!IMPORTANT]
> `Console.ReadLine()` always returns a `string`, even if the user types a number. To work with numbers, you must convert the input first.

## Reading Numbers

To read numeric input, combine `Console.ReadLine()` with a conversion method like `int.Parse()` or `Convert.ToDouble()`.

```csharp
Console.Write("Enter your age: ");
int age = int.Parse(Console.ReadLine());

Console.Write("Enter your height: ");
double height = Convert.ToDouble(Console.ReadLine());

Console.WriteLine($"You are {age} years old and {height}m tall.");
```

> [!IMPORTANT]
> If the user types something that is not a number, `int.Parse()` throws an error and the program crashes. The exceptions section explains how to handle this safely with `try-catch` or `int.TryParse()`.

## Complete Example

This small program combines output, input, and conversion:

```csharp
Console.Write("Enter the product name: ");
string product = Console.ReadLine();

Console.Write("Enter the price: ");
decimal price = decimal.Parse(Console.ReadLine());

Console.Write("Enter the quantity: ");
int quantity = int.Parse(Console.ReadLine());

decimal total = price * quantity;
Console.WriteLine($"Total for {quantity} x {product}: {total:C}");
```

With input and output covered, you are ready to build interactive programs using the topics that follow: strings, numbers, conditionals, and loops.
