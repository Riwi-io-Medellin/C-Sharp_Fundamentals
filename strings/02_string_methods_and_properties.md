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
### Methods

#### `ToUpper()` and `ToLower()`

These methods return a new string with all characters converted to uppercase or lowercase, respectively.

Example:
```csharp
string message = "Hello, World!";
string upperCaseMessage = message.ToUpper(); // "HELLO, WORLD!"
string lowerCaseMessage = message.ToLower(); // "hello, world!"
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
