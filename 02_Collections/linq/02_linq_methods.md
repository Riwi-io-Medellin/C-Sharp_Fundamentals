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

## 6. FirstOrDefault

The `FirstOrDefault` method returns the first element of a sequence that satisfies a condition, or a default value if no such element is found.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.FirstOrDefault(num => num > 5);

Console.WriteLine(result); // Output: 0 (default value for int)
```

## 7. Any

The `Any` method determines whether any elements of a sequence satisfy a condition.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Any(num => num > 3);

Console.WriteLine(result); // Output: True
```

## 8. All

The `All` method determines whether all elements of a sequence satisfy a condition.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.All(num => num > 0);

Console.WriteLine(result); // Output: True
```

## 9. Count

The `Count` method returns the number of elements in a sequence.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Count();

Console.WriteLine(result); // Output: 5
```

## 10. Sum

The `Sum` method computes the sum of the sequence of numeric values.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Sum();

Console.WriteLine(result); // Output: 15
```

## 11. Average

The `Average` method computes the average of the sequence of numeric values.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Average();

Console.WriteLine(result); // Output: 3
```

## 12. Min

The `Min` method returns the minimum value in a sequence.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Min();

Console.WriteLine(result); // Output: 1
```

## 13. Max

The `Max` returns the maximum value in a sequence.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Max();

Console.WriteLine(result); // Output: 5
```

## 14. Take

The `Take` method returns a specified number of contiguous elements from the start of a sequence.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Take(3).ToList();

foreach (var num in result)
{
    Console.WriteLine(num); // Output: 1, 2, 3
}
```

## 15. Skip

The `Skip` method bypasses a specified number of elements in a sequence and then returns the remaining elements.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

var result = numbers.Skip(2).ToList();

foreach (var num in result)
{
    Console.WriteLine(num); // Output: 3, 4, 5
}
```

## 16. Distinct

The `Distinct` method returns distinct elements from a sequence by using the default equality comparer to compare values.

```csharp
int[] numbers = { 1, 2, 2, 3, 4, 4, 5 };

var result = numbers.Distinct();

foreach (var num in result)
{
    Console.WriteLine(num); // Output: 1, 2, 3, 4, 5
}
```