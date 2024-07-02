# String in C#

In this example, we explore strings in C# and how to use them effectively.

## Character Type
Characters in C# are defined using single quotes. Examples:

```csharp 
char letter = 'A';
char digit = '1';

Console.WriteLine($"Letter: {letter}"); // "A"
Console.WriteLine($"Digit: {digit}"); // "1"
```
## Strings
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
## String concatenation

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
