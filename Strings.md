
- ##### **Strings**: A collection of characters surrounded by double quotes.
- **String Keyword**: An alias for the `System.String` class.
- **Example**:
  ```csharp
  string Name = "Darshan";
  String UName = "University";
  ```

#### Example - String:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            string firstName = "Steven";
            string lastName = "Clark";

            Console.WriteLine("First Name: " + firstName);
            Console.WriteLine("Last Name: " + lastName);

            Console.ReadLine();
        }
    }
}
```

#### String Methods:
- **ToLower()**: Converts string to lower case.
- **ToUpper()**: Converts string to upper case.
- **Insert()**: Inserts substring into string.
- **LastIndexOf()**: Returns the last index position of specified value.
- **Length**: Returns the length of string.
- **Remove()**: Deletes characters from beginning to specified index.
- **Replace()**: Replaces a character with another character.

#c-sharp 