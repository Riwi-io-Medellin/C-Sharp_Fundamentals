<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="./01_basic.md">◀️Numbers</a>
    </td>
    <td align="right">
      <a href="../condicionals/01_basic.md">Condicionals▶️</a>
    </td>
  </tr>
</table>

# Math Class in C#

The `Math` class in C# provides a collection of static methods for performing mathematical operations. Here are some commonly used methods:

## Basic Mathematical Operations

`Math.Abs(value)`: Returns the absolute value of a number.
```csharp
double absoluteValue = Math.Abs(-10.5); // absoluteValue = 10.5
```

`Math.Pow(base, exponent)`: Returns a specified number raised to the power of another number.
```csharp
double powerResult = Math.Pow(2, 3); // powerResult = 8
```

`Math.Sqrt(value)`: Returns the square root of a specified number.
```csharp
double sqrtValue = Math.Sqrt(16); // sqrtValue = 4
```

`Math.Min(a, b)`: Returns the smaller of two numbers.
```csharp
int minValue = Math.Min(10, 5); // minValue = 5
```

`Math.Max(a, b)`: Returns the larger of two numbers.
```csharp
int maxValue = Math.Max(10, 5); // maxValue = 10
```

## Trigonometric Functions

`Math.Sin(angle)`, `Math.Cos(angle)`, `Math.Tan(angle)`: Returns the sine, cosine, and tangent of the specified angle (in radians).
```csharp
double sinValue = Math.Sin(Math.PI / 2); // sinValue = 1
```

## Rounding and Ceiling/Floor Functions

`Math.Round(value)`: Rounds a decimal value to the nearest integer.
```csharp
double roundedValue = Math.Round(3.6); // roundedValue = 4
```

`Math.Round(value,decimals)`: Rounds a decimal value to a specified number of decimal places
```csharp
double roundedValue = Math.Round(3.14159, 2); // roundedValue = 3.14
```

`Math.Ceiling(value)`: Returns the smallest integer greater than or equal to the specified number.
```csharp
double ceilingValue = Math.Ceiling(3.2); // ceilingValue = 4
```

`Math.Truncate(value)`: Returns the integral part of a decimal number, removing any fractional digits.
```csharp
double truncatedValue = Math.Truncate(3.75); // truncatedValue = 3
```

`Math.Floor(value)`: Returns the largest integer less than or equal to the specified number.
```csharp
double floorValue = Math.Floor(3.8); // floorValue = 3
```

## Constants

`Math.PI`: Represents the mathematical constant π (pi).
```csharp
double piValue = Math.PI; // piValue = 3.14159265358979
```

These methods provide essential functionality for various mathematical calculations in C# applications.
