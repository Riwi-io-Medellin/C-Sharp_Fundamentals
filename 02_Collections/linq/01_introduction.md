<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
    <tr>
        <td align="left">
            <a href="../lists/02_list_methods_and_properties.md">◀️list methods and properties</a>
        </td>
        <td align="right">
            <a href="./02_linq_methods.md">LINQ methods▶️</a>
        </td>
    </tr>
</table>

# What is LINQ (Language Integrated Query)

LINQ (Language Integrated Query) is a feature in C# that allows you to write queries and manipulate data in a more intuitive and efficient manner directly within your code. LINQ extends the C# language with SQL-like query capabilities integrated natively into the development environment.

## Features of LINQ

**Integrated Query:** 
LINQ enables writing queries directly in C#, providing a declarative and readable syntax for filtering, sorting, grouping, and projecting data. Queries can be written in two main syntaxes:

- **Query Syntax:** Uses keywords like `from`, `where`, `orderby`, `select`, etc.

```csharp
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };

var query = from num in numbers
            where num > 2
            orderby num descending
            select num;
```

- **Method Syntax:** Uses extension methods on `IEnumerable<T>` and delegates (lambda expressions).

```csharp
var methodQuery = numbers.Where(num => num > 2)
                            .OrderByDescending(num => num);
```

**Operations on Collections:** LINQ works with any collection type that implements `IEnumerable<T>`, including lists, arrays, dictionaries, sets, and more.

## What LINQ is Not

- **Not a Database Engine:** While LINQ allows writing SQL-like queries, it is not a database engine itself. LINQ queries execute against in-memory collections or compatible data providers.

- **Not Exclusive to Relational Databases:** Although commonly used with relational databases through Entity Framework, LINQ is independent of the data source and can be applied to any compatible collection.

## Working with Multiple Collections

LINQ is compatible with a variety of collections in C#, making it extremely versatile and suitable for different programming scenarios:

- **Arrays:** Example of filtering on an array:
```csharp
int[] array = { 1, 2, 3, 4, 5 };
var result = array.Where(x => x > 2);
```

- **Lists:** Example of filtering on a list:
```csharp
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };

var result = numbers.Where(num => num > 2);

foreach (var num in result)
{
    Console.WriteLine(num); // Output: 3, 4, 5
}
```
- **Dictionaries:** Example of filtering on a dictionary:
```csharp
Dictionary<string, int> dictionary = new Dictionary<string, int>
{
    { "one", 1 },
    { "two", 2 },
    { "three", 3 },
    { "four", 4 },
    { "five", 5 }
};
var result = dictionary.Where(pair => pair.Value > 2);
```
- **Sets:** Example of filtering on a set:
```csharp
HashSet<int> set = new HashSet<int> { 1, 2, 3, 4, 5 };
var result = set.Where(x => x % 2 == 0);
```