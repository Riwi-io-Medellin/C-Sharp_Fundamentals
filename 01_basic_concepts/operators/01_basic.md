<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="../numbers/02_math.md">◀️Math</a>
    </td>
    <td align="right">
      <a href="../condicionals/01_basic.md">Condicionals▶️</a>
    </td>
  </tr>
</table>

# Operators in C#

Operators in C# are symbols that perform operations on variables and values. They are the building blocks of any expression, from simple arithmetic to complex logical conditions. Here are the main types of operators:

## Arithmetic Operators

Arithmetic operators are used to perform common mathematical operations.

| Operator | Name           | Example  |
|----------|----------------|----------|
| `+`      | Addition       | `x + y`  |
| `-`      | Subtraction    | `x - y`  |
| `*`      | Multiplication | `x * y`  |
| `/`      | Division       | `x / y`  |
| `%`      | Modulus        | `x % y`  |

```csharp
int x = 10;
int y = 3;

int sum = x + y;        // sum = 13
int difference = x - y; // difference = 7
int product = x * y;    // product = 30
int quotient = x / y;   // quotient = 3
int remainder = x % y;  // remainder = 1
```

> [!IMPORTANT]
> When both operands are integers, the division discards the decimal part. To get a decimal result, at least one operand must be a decimal type: `10.0 / 3 // 3.3333...`

## Increment and Decrement Operators

These operators increase or decrease the value of a variable by 1.

```csharp
int counter = 5;

counter++; // counter = 6
counter--; // counter = 5
```

The position of the operator matters when it is used inside an expression: `++counter` (prefix) increments the value before using it, while `counter++` (postfix) uses the value first and then increments it.

```csharp
int a = 5;
int b = ++a; // a = 6, b = 6 (increments first, then assigns)

int c = 5;
int d = c++; // c = 6, d = 5 (assigns first, then increments)
```

## Assignment Operators

Assignment operators are used to assign values to variables. The compound operators combine an arithmetic operation with the assignment.

| Operator | Example  | Equivalent to |
|----------|----------|---------------|
| `=`      | `x = 5`  | `x = 5`       |
| `+=`     | `x += 3` | `x = x + 3`   |
| `-=`     | `x -= 3` | `x = x - 3`   |
| `*=`     | `x *= 3` | `x = x * 3`   |
| `/=`     | `x /= 3` | `x = x / 3`   |
| `%=`     | `x %= 3` | `x = x % 3`   |

```csharp
int score = 10;

score += 5; // score = 15
score -= 3; // score = 12
score *= 2; // score = 24
```

## Comparison Operators

Comparison operators compare two values and return a boolean result (`true` or `false`). They are essential for conditional statements.

| Operator | Name                     | Example  |
|----------|--------------------------|----------|
| `==`     | Equal to                 | `x == y` |
| `!=`     | Not equal to             | `x != y` |
| `>`      | Greater than             | `x > y`  |
| `<`      | Less than                | `x < y`  |
| `>=`     | Greater than or equal to | `x >= y` |
| `<=`     | Less than or equal to    | `x <= y` |

```csharp
int x = 10;
int y = 5;

bool isEqual = x == y;      // isEqual = false
bool isNotEqual = x != y;   // isNotEqual = true
bool isGreater = x > y;     // isGreater = true
bool isLessOrEqual = x <= y; // isLessOrEqual = false
```

> [!IMPORTANT]
> Do not confuse `=` (assignment) with `==` (comparison). Using `=` inside a condition is a common beginner mistake.

## Logical Operators

Logical operators combine boolean expressions and are commonly used to build complex conditions.

| Operator | Name | Description                                     |
|----------|------|-------------------------------------------------|
| `&&`     | AND  | Returns `true` if both expressions are true     |
| `\|\|`   | OR   | Returns `true` if at least one expression is true |
| `!`      | NOT  | Reverses the result of the expression           |

```csharp
int age = 25;
bool hasLicense = true;

bool canDrive = age >= 18 && hasLicense; // canDrive = true
bool isMinorOrSenior = age < 18 || age >= 65; // isMinorOrSenior = false
bool isNotAdult = !(age >= 18); // isNotAdult = false
```

## Ternary Operator

The ternary operator (`? :`) is a shorthand for an `if-else` statement. It evaluates a condition and returns one of two values.

```csharp
int age = 20;
string message = age >= 18 ? "You are an adult." : "You are a minor.";
// message = "You are an adult."
```

These operators are used constantly in every C# program and are the foundation for the conditional statements covered in the next section.
