<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="../condicionals/02_switch.md">◀️Switch</a>
    </td>
    <td align="right">
      <a href="../methods/01_basic.md">Methods▶️</a>
    </td>
  </tr>
</table>

# Loops in C#

Loops in C# are used to execute a block of code repeatedly as long as a condition is met. They allow you to automate repetitive tasks instead of writing the same code multiple times. Here are the main types of loops:

## for Loop

The `for` loop is used when you know in advance how many times you want to execute a block of code. It has three parts: an initializer, a condition, and an iterator.

```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine($"Iteration: {i}");
}
// Iteration: 0
// Iteration: 1
// Iteration: 2
// Iteration: 3
// Iteration: 4
```

- **Initializer** (`int i = 0`): runs once, before the loop starts.
- **Condition** (`i < 5`): checked before each iteration; the loop runs while it is `true`.
- **Iterator** (`i++`): runs after each iteration.

## while Loop

The `while` loop executes a block of code as long as a condition is true. The condition is evaluated **before** each iteration, so if it is false from the start, the block never runs.

```csharp
int counter = 0;
while (counter < 3)
{
    Console.WriteLine($"Counter: {counter}");
    counter++;
}
// Counter: 0
// Counter: 1
// Counter: 2
```

> [!IMPORTANT]
> Always make sure the condition eventually becomes false (for example, by updating the counter inside the loop). Otherwise you will create an infinite loop and the program will never stop.

## do-while Loop

The `do-while` loop is similar to `while`, but the condition is evaluated **after** each iteration. This guarantees that the block of code runs at least once, even if the condition is false.

```csharp
int number = 10;
do
{
    Console.WriteLine($"Number: {number}");
    number++;
} while (number < 5);
// Number: 10 (runs once even though the condition is false)
```

This loop is useful for scenarios like menus, where you need to show the options at least once before asking the user if they want to continue.

## foreach Loop

The `foreach` loop is used to iterate over the elements of a collection (such as arrays or lists) without using an index. It is the simplest way to go through all the elements one by one.

```csharp
string[] fruits = { "apple", "banana", "cherry" };

foreach (string fruit in fruits)
{
    Console.WriteLine(fruit);
}
// apple
// banana
// cherry
```

> [!IMPORTANT]
> Inside a `foreach`, the iteration variable is read-only: you cannot modify the elements of the collection through it. If you need to modify elements, use a `for` loop with an index instead.

## break and continue

These keywords allow you to control the flow of a loop:

- `break`: stops the loop completely and continues with the code after it.
- `continue`: skips the rest of the current iteration and jumps to the next one.

```csharp
for (int i = 0; i < 10; i++)
{
    if (i == 5)
    {
        break; // stops the loop when i is 5
    }
    Console.WriteLine(i);
}
// 0, 1, 2, 3, 4
```

```csharp
for (int i = 0; i < 5; i++)
{
    if (i == 2)
    {
        continue; // skips the iteration when i is 2
    }
    Console.WriteLine(i);
}
// 0, 1, 3, 4
```

Loops are essential for working with the collections covered in the next section, where `for` and `foreach` are used constantly to go through arrays and lists.
