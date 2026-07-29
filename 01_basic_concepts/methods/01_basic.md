<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="../loops/01_basic.md">◀️Loops</a>
    </td>
    <td align="right">
      <a href="../exceptions/01_basic.md">Exceptions▶️</a>
    </td>
  </tr>
</table>

# Methods in C#

A method is a block of code that performs a specific task and can be executed (called) whenever you need it. Methods allow you to reuse code, organize your program into smaller pieces, and avoid repeating the same logic in multiple places.

## Declaring and Calling a Method

A basic method has a return type, a name, and a body. The `void` keyword means the method does not return any value.

```csharp
static void SayHello()
{
    Console.WriteLine("Hello, world!");
}
```

To execute a method, you call it by its name followed by parentheses:

```csharp
SayHello(); // Hello, world!
SayHello(); // Hello, world! (can be called as many times as needed)
```

> [!IMPORTANT]
> By convention, method names in C# use **PascalCase**: `SayHello`, `CalculateTotal`, `GetUserName`.

## Parameters

Parameters allow you to pass values to a method so it can work with different data each time it is called.

```csharp
static void GreetUser(string name)
{
    Console.WriteLine($"Hello, {name}!");
}

GreetUser("Ana");    // Hello, Ana!
GreetUser("Carlos"); // Hello, Carlos!
```

A method can receive multiple parameters, separated by commas:

```csharp
static void ShowProduct(string product, decimal price)
{
    Console.WriteLine($"{product} costs {price:C}");
}

ShowProduct("Laptop", 1500.99m); // Laptop costs $1,500.99
```

## Return Values

A method can return a result using the `return` keyword. The return type replaces `void` in the declaration.

```csharp
static int Add(int a, int b)
{
    return a + b;
}

int result = Add(5, 3); // result = 8
Console.WriteLine(Add(10, 20)); // 30
```

```csharp
static bool IsAdult(int age)
{
    return age >= 18;
}

bool canVote = IsAdult(20); // canVote = true
```

> [!IMPORTANT]
> A method with a return type other than `void` must always return a value of that type. If you forget the `return`, the compiler shows an error.

## Passing Parameters by Reference (ref)

By default, parameters are passed **by value**: the method receives a copy of the variable, so any change made inside the method does not affect the original.

```csharp
static void AddTen(int number)
{
    number += 10; // modifies only the copy
}

int myNumber = 5;
AddTen(myNumber);
Console.WriteLine(myNumber); // 5 (the original did not change)
```

With the `ref` keyword, the parameter is passed **by reference**: the method works directly with the original variable, so any change inside the method is reflected outside.

```csharp
static void AddTen(ref int number)
{
    number += 10; // modifies the original variable
}

int myNumber = 5;
AddTen(ref myNumber);
Console.WriteLine(myNumber); // 15 (the original changed)
```

> [!IMPORTANT]
> The `ref` keyword must be written in both places: in the method declaration and in the call. Also, the variable must be initialized before being passed with `ref`, otherwise the compiler shows an error.

A classic example is a method that swaps the values of two variables, which is impossible with parameters passed by value:

```csharp
static void Swap(ref int a, ref int b)
{
    int temp = a;
    a = b;
    b = temp;
}

int x = 1;
int y = 2;
Swap(ref x, ref y);
Console.WriteLine($"x = {x}, y = {y}"); // x = 2, y = 1
```

## Output Parameters (out)

The `out` keyword also passes a parameter by reference, but with a different purpose: it is used when the method **produces** a value and needs to deliver it to the caller. The difference with `ref` is that the variable does not need to be initialized before the call — the method is **required** to assign it a value before returning.

```csharp
static void GetSquare(int number, out int result)
{
    result = number * number; // the method must assign the out parameter
}

int square; // no need to initialize it
GetSquare(5, out square);
Console.WriteLine(square); // 25
```

You can even declare the variable directly in the call, which is the most common style:

```csharp
GetSquare(7, out int anotherSquare);
Console.WriteLine(anotherSquare); // 49
```

## Returning Multiple Values with out

Since `return` can only return one value, `out` is the classic way to make a method deliver several results at once.

```csharp
static void Divide(int dividend, int divisor, out int quotient, out int remainder)
{
    quotient = dividend / divisor;
    remainder = dividend % divisor;
}

Divide(17, 5, out int q, out int r);
Console.WriteLine($"Quotient: {q}, Remainder: {r}"); // Quotient: 3, Remainder: 2
```

> [!IMPORTANT]
> In short: use `ref` when the method needs to **modify** a variable that already has a value, and `out` when the method needs to **produce and deliver** a new value.

The most famous use of `out` in C# is `int.TryParse(input, out int age)`: the method returns a `bool` indicating whether the conversion worked, and delivers the converted number through the `out` parameter. You will see it in action in the next section, exceptions.

## Optional Parameters

You can give a parameter a default value. If the caller does not provide it, the default is used.

```csharp
static void Greet(string name, string greeting = "Hello")
{
    Console.WriteLine($"{greeting}, {name}!");
}

Greet("Ana");            // Hello, Ana!
Greet("Ana", "Welcome"); // Welcome, Ana!
```

## Method Overloading

Two methods can have the same name if their parameters are different. The compiler chooses the right one based on the arguments you pass.

```csharp
static int Multiply(int a, int b)
{
    return a * b;
}

static double Multiply(double a, double b)
{
    return a * b;
}

int intResult = Multiply(3, 4);        // uses the int version, intResult = 12
double doubleResult = Multiply(2.5, 2); // uses the double version, doubleResult = 5.0
```

Methods are the bridge to Object-Oriented Programming: classes group related methods and data together, as you will see in the OOP section.
