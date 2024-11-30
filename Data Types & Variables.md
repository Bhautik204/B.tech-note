
- **Variables**: Containers for storing data values.
- **Common Data Types**:
  - **int**: Integer numbers.
  - **double**: Floating-point numbers.
  - **char**: Single characters.
  - **string**: Text.
  - **bool**: Boolean values (`true` or `false`).

#### Declaring Variables:
```csharp
int num = 15;
double number = 15.50;
char value = 'B';
string name = "Darshan University";
bool isClosed = false;
```

#### Example:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        static void Main(string[] args)
        {
            int number = 10;
            string name = "Darshan University";
            double percentage = 10.23;
            char gender = 'M';
            bool isVerified = true;

            Console.WriteLine(number);
            Console.WriteLine(name);
            Console.WriteLine(percentage);
            Console.WriteLine(gender);
            Console.WriteLine(isVerified);
            Console.ReadLine();
        }
    }
}
```

### Rules for Declaring Variables:
- Must start with an alphabet or underscore.
- No white space allowed within the variable name.
- Cannot use reserved keywords.
- Once declared with a type, it cannot be re-declared with a new type.

#c-sharp 