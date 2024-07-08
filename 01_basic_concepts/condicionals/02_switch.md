<div align="center">
    <a href="/README.md">Home</a>
</div>
<table align=center>
  <tr>
    <td align="left">
      <a href="./01_basic.md">◀️Conditional Statements</a>
    </td>
    <td align="right">
      <a href="./02_string_methods_and_properties.md">Switch▶️</a>
    </td>
  </tr>
</table>

# Switch Statement in C#

The `switch` statement in C# evaluates a single expression and matches its value against a list of possible cases, executing the corresponding block of code for the first match found. This is useful for simplifying complex conditional logic involving multiple `if-else` statements.

## Classic switch Statement

The classic `switch` statement checks the value of a variable against multiple cases and executes the block of code associated with the matching case.

### Example:

```csharp
int dayOfWeek = 3;
switch (dayOfWeek)
{
    case 1:
        Console.WriteLine("Monday");
        break;
    case 2:
        Console.WriteLine("Tuesday");
        break;
    case 3:
        Console.WriteLine("Wednesday");
        break;
    case 4:
        Console.WriteLine("Thursday");
        break;
    case 5:
        Console.WriteLine("Friday");
        break;
    case 6:
        Console.WriteLine("Saturday");
        break;
    case 7:
        Console.WriteLine("Sunday");
        break;
    default:
        Console.WriteLine("Invalid day");
        break;
}
```

## Switch Statement with Logical Operators

The `switch` statement can also be used with logical operators such as `or` or `and` to create more complex case conditions. However, logical operations within case labels are not directly supported. To achieve similar functionality, you need to use a combination of if statements within the switch cases.

### Example:

```csharp
char grade = 'B';
int credits = 15;

switch (grade)
{
    case 'A':
        if (credits >= 12)
            Console.WriteLine("Excellent student with full credits.");
        else
            Console.WriteLine("Excellent student.");
        break;
    case 'B':
        if (credits >= 12)
            Console.WriteLine("Good student with full credits.");
        else
            Console.WriteLine("Good student.");
        break;
    case 'C':
        if (credits >= 12)
            Console.WriteLine("Average student with full credits.");
        else
            Console.WriteLine("Average student.");
        break;
    default:
        Console.WriteLine("Invalid grade.");
        break;
}
```