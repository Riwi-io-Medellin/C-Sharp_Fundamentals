<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="/README.md">◀️Introduction</a>
    </td>
    <td align="right">
      <a href="../console/01_basic.md">Console▶️</a>
    </td>
  </tr>
</table>

# Variables and Data Types in C#

A variable is a container that stores a value in memory so it can be used later in the program. In C#, every variable has a **type** that defines what kind of data it can store. C# is a strongly typed language, which means the type of a variable is checked at compile time.

## Declaring Variables

To declare a variable, you write the type followed by the name. You can assign a value at the same time or later.

```csharp
int age;            // declaration
age = 25;           // assignment

string name = "Ana"; // declaration and assignment in one line
```

## Main Data Types

| Type      | Description                          | Example                  |
|-----------|--------------------------------------|--------------------------|
| `int`     | Whole numbers                        | `int age = 25;`          |
| `double`  | Decimal numbers (double precision)   | `double height = 1.75;`  |
| `decimal` | High-precision decimals (money)      | `decimal price = 9.99m;` |
| `char`    | A single character (single quotes)   | `char letter = 'A';`     |
| `string`  | Text (double quotes)                 | `string name = "Ana";`   |
| `bool`    | Logical value: `true` or `false`     | `bool isActive = true;`  |

```csharp
int quantity = 3;
double temperature = 22.5;
decimal salary = 2500.75m;
char initial = 'J';
string city = "Medellín";
bool isRegistered = true;
```

> [!IMPORTANT]
> Use `decimal` (with the `m` suffix) for money and financial calculations, because `double` can introduce small rounding errors.

## The var Keyword

With `var`, the compiler infers the type from the assigned value. The variable is still strongly typed: once inferred, the type cannot change.

```csharp
var count = 10;        // inferred as int
var message = "Hello"; // inferred as string

count = "text"; // ❌ Error: cannot assign a string to an int
```

> [!IMPORTANT]
> A variable declared with `var` must be initialized in the same line, because the compiler needs a value to infer the type.

## Constants

A constant is a value that cannot change after it is declared. Use the `const` keyword and, by convention, initialize it immediately.

```csharp
const double Pi = 3.1416;
const int MaxAttempts = 3;

Pi = 3.15; // ❌ Error: a constant cannot be modified
```

## Comments

Comments are notes in the code that the compiler ignores. They are used to explain what the code does.

```csharp
// This is a single-line comment

/*
This is a
multi-line comment
*/

int age = 25; // comments can also go at the end of a line
```

## Naming Conventions

- Variable names cannot start with a number and cannot contain spaces or special characters (except `_`).
- Use **camelCase** for local variables: `firstName`, `totalPrice`.
- Use descriptive names: `age` is better than `a`.
- C# is case-sensitive: `age` and `Age` are different variables.

```csharp
string firstName = "Laura"; // ✔️ camelCase, descriptive
string x = "Laura";         // ❌ valid but not descriptive
```

Variables are the foundation of every program: all the topics that follow (strings, numbers, conditionals, loops) work with them constantly.
