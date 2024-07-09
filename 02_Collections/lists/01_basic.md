<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
      <td align="left">
      <a href="../arrays/02_array_methods_and_properties.md">◀️Array methods an properties</a>
    </td>
      <td align="right">
         <a href="./02_list_methods_and_properties.md">List methods an properties▶️</a>
      </td>
  </tr>
</table>

# List in C#

A `List<T>` is a generic collection in C# that can store a variable number of elements. Unlike arrays, lists can dynamically change their size, which means you can add or remove elements after the list has been created.

## Characteristics of a List

1. **Dynamic Size:** 
   - Lists can grow or shrink dynamically as elements are added or removed.
   - There is no need to specify the size of the list at the time of creation.

2. **Index Access:**
   - Elements in a list can be accessed by index, similar to arrays.
   ```csharp
   List<int> numbers = new List<int> { 10, 20, 30 };
   int firstNumber = numbers[0]; // Accesses the first element
   ```

3. **Generic Type:**
   - Lists in C# are generic, meaning they can store any data type, specified at the time of creation.
   ```csharp
   List<string> words = new List<string>();
   ```

### Example Usage

Below is a basic example of how to declare, initialize, and work with a list in C#:

```csharp
// Declare and initialize a list of integers
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };

// Add an element to the list
numbers.Add(6);

// Access elements of the list
Console.WriteLine("The first number is: " + numbers[0]); // Output: The first number is: 1

// Iterate through the list using a foreach loop
Console.WriteLine("Numbers in the list (using foreach):");
foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```

## Initialization types

In C#, there are several ways to initialize a list:

### 1. Using Collection Initializer:

```csharp
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };
```

### 2. Using Constructor

```csharp
List<int> emptyList = new List<int>();
```

### 3. Adding Elements Individually

```csharp
List<string> fruits = new List<string>();
fruits.Add("Apple");
fruits.Add("Banana");
fruits.Add("Orange");
```

### 4. Using Array to List Conversion

```csharp
string[] colorsArray = { "Red", "Green", "Blue" };
List<string> colorsList = new List<string>(colorsArray);
```

These examples illustrate different ways to initialize and populate a List<T> in C#. Each method has its use case depending on whether you're starting with existing data or building the list dynamically.