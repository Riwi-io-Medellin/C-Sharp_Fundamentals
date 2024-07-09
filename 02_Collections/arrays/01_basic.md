<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="right">
      <a href="./02_array_methods_and_properties.md">Methods and properties▶️</a>
    </td>
  </tr>
</table>

# Arrays in C#

An array is a data structure that allows you to store multiple values of the same type in a single variable. It's like a row of boxes where each box has a number called an index, and you can store one piece of data in each box.

## Characteristics of an Array

1. **Fixed Size:** 
   - Once the size of an array is defined, it cannot be changed. The number of elements it can store is fixed.

2. **Uniform Data Type:** 
   - All elements in an array must be of the same data type, such as `int`, `string`, `bool`, etc.

3. **Index-Based Access:** 
   - Elements in the array can be accessed using indices, starting from 0 up to the array's size minus one.

4. **Contiguous Storage:** 
   - Array elements are stored in contiguous memory locations, which allows for fast access to elements.

5. **Storage Capacity:** 
   - An array can store both primitive data types and objects.

6. **Initialization:** 
   - Arrays can be initialized at the time of declaration or filled later.

### Example Usage

Below is a basic example of how to declare, initialize, and work with an array in C#:

```csharp
// Declare and initialize an array of integers with 5 elements
int[] numbers = new int[5];

// Assign values to each element of the array
numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;
numbers[3] = 40;
numbers[4] = 50;

// Print each element of the array using a for loop
Console.WriteLine("Elements of the array:");
for (int i = 0; i < numbers.Length; i++)
{
    Console.WriteLine(numbers[i]);
}
```

## Initialization types

### 1. Basic Initialization:

You can declare and initialize an array by specifying the size and values of the elements at the same time:

```csharp
int[] numbers = { 10, 20, 30, 40, 50 };
```
In this example, `numbers` is an array of integers with 5 elements initialized with the values 10, 20, 30, 40, and 50.

### 2. Initialization using new:

You can also initialize an array using the `new` keyword along with the size of the array:

```csharp
int[] numbers = new int[5];
```
After initialization, you can assign values to each element of the array individually.

### 2. Initialization with Implicit Size:

If you know the values but not the exact size, you can omit the size and let the compiler determine the size of the array based on the provided values:

```csharp
int[] numbers = new int[] { 10, 20, 30 };
```

