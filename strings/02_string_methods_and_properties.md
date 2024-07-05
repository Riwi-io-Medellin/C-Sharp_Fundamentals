<div align="center">
    <a href="../README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="./01_basic.md">◀️strings</a>
    </td>
    <td align="right">
      <a href="./01_basic.md">numbers▶️</a>
    </td>
  </tr>
</table>

## Methods and Properties of Strings in C#


In C#, the `string` type provides a rich set of methods and properties for manipulating and working with text data. Here are some commonly used methods and properties:

### Properties

#### `Length`

The `Length` property returns the number of characters in the string.

Example:
```csharp
string text = "Hello, world!";
int length = text.Length; // length is 13
```

#### `Chars`

Allows access to individual characters in the string by index. Indexing starts at 0 for the first character and `Length - 1` for the last character.

```csharp
string exampleText = "Hello, World!";

Console.WriteLine("First character: " + exampleText[0]); // "H"
Console.WriteLine("Last character: " + exampleText[exampleText.Length - 1]); // "!"
```

### Methods

#### `ToUpper()` and `ToLower()`

These methods return a new string with all characters converted to uppercase or lowercase, respectively.

Example:
```csharp
string message = "Hello, World!";
string upperCaseMessage = message.ToUpper(); // "HELLO, WORLD!"
string lowerCaseMessage = message.ToLower(); // "hello, world!"
```

#### `String Equality Check`
Checks if two strings (`text1` and `text2` in this case) are equal.

```csharp
string text1 = "example";
string text2 = "example";

bool areEqual = text1.Equals(text2);
Console.WriteLine($"Are Text1 and Text2 equal? {areEqual}"); // true
```

#### `IsNullOrEmpty`
Checks if a string is null or empty (string.Empty represents an empty string literal).

```csharp
bool isEmpty = string.IsNullOrEmpty(string.Empty);
bool isNull = string.IsNullOrEmpty(null);
Console.WriteLine($"Is it empty or null? {isEmpty} - {isNull}"); // true & true
```

#### `IsNullOrWhiteSpace`
Checks if a string is null, empty, or consists only of white-space characters.

```csharp
string multipleCharacters = "    "; // Contains only white-space characters

bool isEmptyOrWhiteSpace = string.IsNullOrWhiteSpace(multipleCharacters);
Console.WriteLine($"Is the text empty or whitespace? {isEmptyOrWhiteSpace}"); // true
```

#### `Trim`
Removes leading and trailing white-space characters from a string (`text1` and `text2` in this case).

```csharp
string text1 = "  Hello ";
string text2 = " World  ";

string trimmedText1 = text1.Trim();
string trimmedText2 = text2.Trim();

Console.WriteLine($"Text1 without white-spaces: {trimmedText1}"); // "Hello"
Console.WriteLine($"Text2 without white-spaces: {trimmedText2}"); // "World"
```

#### `Substring(int startIndex)` and `Substring(int startIndex, int length)`

Substring method returns a new string that is a substring of the original string. The first form takes a starting index, and the second form also specifies a length.

Example:

```csharp
string text = "Hello, world!";
string substring1 = text.Substring(7); // "world!"
string substring2 = text.Substring(0, 5); // "Hello"
```

#### `Replace(string oldValue, string newValue)`

Replaces all occurrences of a specified string oldValue with newValue in the current string.

Example:

```csharp
string message = "Hello, World!";
string newMessage = message.Replace("Hello", "Hi"); // "Hi, World!"
```

These methods and properties are fundamental for working effectively with strings in C#, offering a wide range of functionalities from basic operations like case conversion and substring extraction to more complex tasks like searching and replacing substrings.
