<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="../numbers/02_math.md">◀️Math</a>
    </td>
    <td align="right">
      <a href="./02_switch.md">Switch▶️</a>
    </td>
  </tr>
</table>

# Conditional Statements in C#

Conditional statements in C# are used to control the flow of execution based on conditions. They allow your program to make decisions and execute different blocks of code depending on whether certain conditions are true or false. Here are the main types of conditional statements:

## if Statement

The `if` statement checks a condition and executes a block of code if the condition is true.

### Example:

```csharp
int age = 25;
if (age >= 18)
{
    Console.WriteLine("You are an adult.");
}
```

## if-else Statement

The `if-else` statement executes one block of code if the condition is true and another block if the condition is false.

### Example:

```csharp
int num = 0;
if (num > 0)
{
    Console.WriteLine("Number is positive.");
}
else
{
    Console.WriteLine("Number is non-positive.");
}
```

## Ternary Operator

The ternary operator `condition ? trueValue : falseValue` provides a concise way to return one of two values based on a condition.

### Example:

```csharp
int number = 10;
string result = (number % 2 == 0) ? "Even" : "Odd";
Console.WriteLine($"The number is {result}");
```

## if - else if - else Statement

The `if- else if -else` statement allows checking multiple conditions sequentially after an initial `if` statement.

### Example:

```csharp
int score = 75;
if (score >= 90)
{
    Console.WriteLine("Grade: A");
}
else if (score >= 80)
{
    Console.WriteLine("Grade: B");
}
else if (score >= 70)
{
    Console.WriteLine("Grade: C");
}
else
{
    Console.WriteLine("Grade: F");
}
```

## Nested if Statements

Nested `if` statements are used to check conditions within another `if` or `else` block.

### Example:

```csharp
int x = 10, y = 5;
if (x > 0)
{
    if (y > 0)
    {
        Console.WriteLine("Both x and y are positive.");
    }
    else
    {
        Console.WriteLine("x is positive, but y is non-positive.");
    }
}
else
{
    Console.WriteLine("x is non-positive.");
}
```