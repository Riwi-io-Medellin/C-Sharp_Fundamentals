<div align="center">
    <a href="../README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="../README.md.md">◀️introduction</a>
    </td>
    <td align="right">
      <a href="./02_string_methods_and_properties.md">methods and properties▶️</a>
    </td>
  </tr>
</table>
# Strings in C#

In this example, we explore strings in C# and how to use them effectively.Strings are a sequence of characters used to represent text. In C#, strings are handled as objects of the String class, allowing you to perform various operations such as concatenation, search, modification, and more

## Character Type
Characters in C# are defined using single quotes. Examples:

```csharp 
char letter = 'A';
char digit = '1';

Console.WriteLine($"Letter: {letter}"); // "A"
Console.WriteLine($"Digit: {digit}"); // "1"
```
## Strings
A string variable contains a collection of characters surrounded by double quotes

```csharp 
string greeting = "Hello, world!";
string multilineText = @"This is a 
multiline
text.";
```
```csharp 
Console.WriteLine($"Greeting: {greeting}");
Console.WriteLine($"Multiline Text: {multilineText}");
```
## Concatenation types
In C#, you can concatenate strings in several ways:

+ `+ Operator`: Concatenates strings using the `+` operator. It's straightforward and simple.

+ `String Interpolation ($"")`: Allows you to embed variables directly into a string using `${}`. It's useful for including expressions and variables within strings in a readable manner.

+ `string.Concat() Method`: Combines multiple strings into one using the static `Concat()` method of the `string` class. It's efficient for concatenating more than two strings.

Examples:

```csharp 
string firstName = "John";
string lastName = "Smith";

string fullName1 = firstName + " " + lastName;
string fullName2 = $"{firstName} {lastName}";
string fullName3 = string.Concat(firstName, " ", lastName);
```
```csharp 
Console.WriteLine($"Full Name option 1: {fullName1}");
Console.WriteLine($"Full Name option 2: {fullName2}");
Console.WriteLine($"Full Name option 3: {fullName3}");
```
