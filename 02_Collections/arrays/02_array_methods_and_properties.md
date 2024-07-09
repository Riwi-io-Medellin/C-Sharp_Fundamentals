<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
    <tr>
        <td align="left">
            <a href="./01_basic.md">◀️Arrays</a>
        </td>
        <td align="right">
            <a href="../lists/01_basic.md">Lists▶️</a>
        </td>
    </tr>
</table>

# Methods and Properties of Arrays in C#

## Properties

### Length
The `Length` property gets the total number of elements in all the dimensions of the array.
```csharp
  int[] numbers = { 10, 20, 30, 40, 50 };
  int length = numbers.Length; // length = 5
```

### Rank
The `Rank` property gets the number of dimensions (or rank) of the array.
```csharp
int[,] matrix = new int[3, 5];
int rank = matrix.Rank; // rank = 2
```

## Methods

### GetValue and SetValue
The `GetValue` method retrieves the value at a specified position in the array and the `SetValue` method sets a value at a specified position in the array.
```csharp
int[] numbers = { 10, 20, 30, 40, 50 };

int value = (int) numbers.GetValue(2); // value = 30
numbers.SetValue(100, 2); // numbers[2] = 100
```

### CopyTo
The `CopyTo` method copies all the elements of the current array to a specified array starting at a particular index.
```csharp
int[] sourceArray = { 1, 2, 3 };
int[] destinationArray = new int[5];
sourceArray.CopyTo(destinationArray, 2);
// destinationArray = { 0, 0, 1, 2, 3 }
```

### Clone
The `Clone` method creates a shallow copy of the array.
```csharp
int[] numbers = { 10, 20, 30 };
int[] clonedArray = (int[]) numbers.Clone();
```

### Sort
The `Sort` method sorts the elements in a one-dimensional array.
```csharp
int[] numbers = { 30, 10, 20 };
Array.Sort(numbers); // numbers = { 10, 20, 30 }
```

### Reverse
The `Reverse` method reverses the order of the elements in a one-dimensional array.
```csharp
int[] numbers = { 30, 10, 20 };
Array.Sort(numbers); // numbers = { 10, 20, 30 }
```

### IndexOf
The `IndexOf` method returns the index of the first occurrence of a value in a one-dimensional array.
```csharp
int[] numbers = { 10, 20, 30 };
int index = Array.IndexOf(numbers, 20); // index = 1
```

### Find
The `Find` method returns the first element that matches the conditions defined by a specified predicate.
```csharp
int[] numbers = { 10, 20, 30 };
int result = Array.Find(numbers, element => element > 15); // result = 20
```

### FindAll
The `FindAll` method returns all the elements that match the conditions defined by a specified predicate.
```csharp
int[] numbers = { 10, 20, 30, 40 };
int[] results = Array.FindAll(numbers, element => element > 15); // results = { 20, 30, 40 }
```