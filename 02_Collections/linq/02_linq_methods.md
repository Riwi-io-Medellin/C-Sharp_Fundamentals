<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
    <tr>
        <td align="left">
            <a href="../linq/01_introduction.md">◀️LINQ</a>
        </td>
    </tr>
</table>

# Common LINQ Methods in C#

LINQ (Language Integrated Query) provides a rich set of methods for querying and manipulating data in C#. Here are examples of some commonly used LINQ methods:

## 1. Where

The `Where` method filters elements based on a condition.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Where(num => num > 2).ToList();

foreach (var num in result)
{
    Console.WriteLine(num); // Output: 3, 4, 5
}
```

## 2. Select

The `Select` method projects each element of a sequence into a new form.

```csharp
string[] fruits = { "apple", "banana", "cherry" };

var result = fruits.Select(fruit => fruit.ToUpper()).ToList();

foreach (var fruit in result)
{
    Console.WriteLine(fruit); // Output: APPLE, BANANA, CHERRY
}
```

## 3. OrderBy

The `OrderBy` method sorts elements in ascending order.

```csharp
string[] fruits = { "apple", "banana", "cherry" };

var result = fruits.Select(fruit => fruit.ToUpper()).ToList();

foreach (var fruit in result)
{
    Console.WriteLine(fruit); // Output: APPLE, BANANA, CHERRY
}
```

## 4. OrderByDescending

The `OrderByDescending` method sorts elements in descending order.

```csharp
int[] numbers = { 5, 2, 7, 1, 3 };

var result = numbers.OrderByDescending(num => num).ToList();

foreach (var num in result)
{
    Console.WriteLine(num); // Output: 7, 5, 3, 2, 1
}
```

## 5. First

The `First` method returns the first element of a sequence that satisfies a condition.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.First(num => num > 2);

Console.WriteLine(result); // Output: 3
```