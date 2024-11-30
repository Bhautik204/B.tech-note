
#### `Console.WriteLine()` and `Console.Write()`
- **`Console.WriteLine()`**: Prints values or texts to the console with a new line.
- **`Console.Write()`**: Prints values or texts to the console without a new line.

#### Example:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            Console.Write("Welcome to");
            Console.Write(" Darshan University");
            Console.WriteLine("\n-------------------");
            Console.WriteLine("Welcome to ");
            Console.WriteLine("Darshan University");
            Console.ReadLine();
        }
    }
}
```

#### `Console.ReadLine()`
- Reads the next line of characters from the standard input stream and returns a string.

#### Example:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            string name = Console.ReadLine();
            Console.WriteLine("ReadLine Result is :" + name);
        }
    }
}
```

#### `Console.Read()`
- Reads the next character from the standard input stream and returns its ASCII value as an integer.

#### Example:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            int val = Console.Read();
            Console.WriteLine("Read Result is :" + val);
        }
    }
}
```

#### `Console.ReadKey()`
- Obtains the next character or function key pressed by the user.

#### Example:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            while (true)
            {
                ConsoleKeyInfo key = Console.ReadKey();
                Console.WriteLine("\n You pressed " + key.Key);
            }
        }
    }
}
```

#c-sharp 