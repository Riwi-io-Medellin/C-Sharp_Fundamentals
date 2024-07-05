<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="../strings/02_string_methods_and_properties.md">◀️Methods and properties (string)</a>
    </td>
    <td align="right">
      <a href="#">Math▶️</a>
    </td>
  </tr>
</table>

# Numbers in C#
Numeric types in C# are essential for working with data that involves quantities, measurements, and mathematical calculations in programs. Each numerical type has specific characteristics, such as range and precision, that make them suitable for different situations.

## Numerical Data Types in C#
In C#, the main numeric data types are:

### Integer Types:

+ **byte**: Represents unsigned integers of 8 bits (0 to 255).
+ **sbyte**: Represents signed integers of 8 bits (-128 to 127).
+ **short**: Represents signed integers of 16 bits (-32,768 to 32,767).
+ **ushort**: Represents unsigned integers of 16 bits (0 to 65,535).
+ **int**: Represents signed integers of 32 bits (-2,147,483,648 to 2,147,483,647).
+ **uint**: Represents unsigned integers of 32 bits (0 to 4,294,967,295).
+ **long**: Represents signed integers of 64 bits (-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807).
+ **ulong**: Represents unsigned integers of 64 bits (0 to 18,446,744,073,709,551,615).

### Floating-Point Types:

+ **float**: Represents single-precision floating-point numbers (approximately ±1.5 x 10^-45 to ±3.4 x 10^38 with a precision of 7 digits).
+ **double**: Represents double-precision floating-point numbers (approximately ±5.0 x 10^-324 to ±1.7 x 10^308 with a precision of 15-16 digits).
+ **decimal**: Represents high-precision decimal numbers (approximately ±1.0 x 10^-28 to ±7.9 x 10^28 with a precision of 28-29 digits).

### examples
```csharp
int age = 30; // age = 30
double salary = 2500.75; // salary = 2500.75
decimal price = 99.99m; // price = 99.99

int sum = 10 + 5; // sum = 15
double multiplication = 3.5 * 2.0; // multiplication = 7.0
decimal division = price / 3.0m; // division = 33.33
```