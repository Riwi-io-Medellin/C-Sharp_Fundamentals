<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
    <tr>
        <td align="left">
            <a href="./01_basic.md">◀️Lists</a>
        </td>
        <td align="right">
            <a href="../linq/01_introduction.md">LINQ▶️</a>
        </td>
    </tr>
</table>

# Methods and Properties of Lists in C#

Lists in C# (`List<T>`) provide several useful methods and properties for managing and manipulating collections of elements.
## Properties

### Count
The `Count` property returns the number of elements currently in the list.
```csharp
List<int> numbers = new List<int> { 10, 20, 30 };
int count = numbers.Count; // Returns 3
```

### Capacity
The `Capacity` property indicates the total number of elements that the list can currently hold without resizing.
```csharp
List<int> numbers = new List<int>(10); // Initializes with capacity of 10
int capacity = numbers.Capacity; // Returns 10
```

### IsReadOnly
The `IsReadOnly` property indicates whether the list is read-only, meaning its elements cannot be modified.
```csharp
List<int> numbers = new List<int> { 10, 20, 30 };
bool isReadOnly = numbers.IsReadOnly; // Returns false (default)
```

## Methods

### Adding Elements to a List
You can add elements to a list using the `Add` method:
```csharp
List<int> numbers = new List<int>();
numbers.Add(60); // Adds the number 60 to the end of the list

// You can also add multiple elements at once using the AddRange method:
numbers.AddRange(new int[] { 70, 80, 90 }); // Adds numbers 70, 80, and 90 to the end of the list
```

### Accessing Elements in a List
You can access elements in a list using the index, just like with arrays:
```csharp
List<int> numbers = new List<int> { 10, 20, 30 };
int firstNumber = numbers[0]; // Accesses the first element (10)
```

### Finding Elements in a List
You can find elements in a list using the Find method, which returns the first element that matches the specified condition:
```csharp
List<int> numbers = new List<int> { 10, 20, 30 };
int result = numbers.Find(number => number > 20); // Finds the first element greater than 20
```

To find all elements that match a condition, you can use the FindAll method:

```csharp
List<int> numbers = new List<int> { 10, 20, 30 };
List<int> results = numbers.FindAll(number => number > 20); // Finds all elements greater than 20
```

### Modifying Elements in a List
You can modify elements in a list by accessing them through their index:
```csharp
List<int> numbers = new List<int> { 10, 20, 30 };
numbers[0] = 100; // Changes the first element from 10 to 100
```

### Sorting a List
You can sort the elements of a list using the Sort method:
```csharp
List<int> numbers = new List<int> { 30, 10, 20 };
numbers.Sort(); // Sorts the list in ascending order (10, 20, 30)
```

### Removing Elements from a List
You can remove elements from a list using the `Remove` method (which removes the first occurrence of a specified value):
```csharp
List<int> numbers = new List<int> { 10, 20, 30 };
numbers.Remove(30); // Removes the first occurrence of the value 30
```
You can also remove elements by their index using the RemoveAt method:
```csharp
List<int> numbers = new List<int> { 10, 20, 30 };
numbers.RemoveAt(1); // Removes the element at index 1 (20)
```
To remove all elements from the list that match a condition, you can use the `RemoveAll` method:
```csharp
List<int> numbers = new List<int> { 10, 20, 30, 40, 50 };
numbers.RemoveAll(number => number > 30); // Removes all elements greater than 30
```