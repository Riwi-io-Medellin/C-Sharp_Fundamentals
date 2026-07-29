<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="../methods/01_basic.md">◀️Methods</a>
    </td>
    <td align="right">
      <a href="../../02_Collections/arrays/01_basic.md">Arrays▶️</a>
    </td>
  </tr>
</table>

# Exceptions in C#

An exception is an error that occurs while the program is running (at runtime), such as dividing by zero, converting invalid text to a number, or accessing a position that does not exist in an array. If an exception is not handled, the program crashes. C# provides the `try-catch` structure to handle these errors gracefully.

## try-catch

The code that might fail goes inside the `try` block. If an exception occurs, the program jumps to the `catch` block instead of crashing.

```csharp
try
{
    Console.Write("Enter a number: ");
    int number = int.Parse(Console.ReadLine()); // fails if the input is not a number
    Console.WriteLine($"You entered: {number}");
}
catch (Exception ex)
{
    Console.WriteLine($"Something went wrong: {ex.Message}");
}
```

If the user types `"abc"`, instead of crashing the program prints: `Something went wrong: The input string 'abc' was not in a correct format.`

## Catching Specific Exceptions

You can have multiple `catch` blocks to handle different types of errors in different ways. The most specific exceptions go first.

```csharp
try
{
    Console.Write("Enter a number: ");
    int number = int.Parse(Console.ReadLine());

    int result = 100 / number; // fails if number is 0
    Console.WriteLine($"Result: {result}");
}
catch (FormatException)
{
    Console.WriteLine("The input is not a valid number.");
}
catch (DivideByZeroException)
{
    Console.WriteLine("You cannot divide by zero.");
}
catch (Exception ex)
{
    Console.WriteLine($"Unexpected error: {ex.Message}");
}
```

> [!IMPORTANT]
> The general `catch (Exception)` must always go last. If you put it first, it captures every error and the specific blocks are never reached.

## finally

The `finally` block always runs, whether an exception occurred or not. It is used for cleanup tasks that must happen in any case.

```csharp
try
{
    int number = int.Parse("123");
    Console.WriteLine($"Number: {number}");
}
catch (FormatException)
{
    Console.WriteLine("Invalid format.");
}
finally
{
    Console.WriteLine("This message always appears.");
}
```

## Throwing Exceptions

You can also generate your own exceptions with the `throw` keyword, for example to validate data inside a method.

```csharp
static void SetAge(int age)
{
    if (age < 0)
    {
        throw new ArgumentException("Age cannot be negative.");
    }
    Console.WriteLine($"Age set to {age}");
}
```

## Avoiding Exceptions with TryParse

For conversions, C# offers the `TryParse` methods: instead of throwing an exception, they return `false` if the conversion fails. This is the recommended way to validate user input.

```csharp
Console.Write("Enter your age: ");
string input = Console.ReadLine();

if (int.TryParse(input, out int age))
{
    Console.WriteLine($"You are {age} years old.");
}
else
{
    Console.WriteLine("That is not a valid number.");
}
```

Handling exceptions makes your programs robust: they respond to unexpected situations with clear messages instead of crashing.
