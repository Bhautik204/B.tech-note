- **Operators**: Special symbols that perform actions on operands.
- **Types of Operators**:
  - **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`, `++`, `--`
  - **Relational Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=`
  - **Logical Operators**: `&&`, `||`, `!`
  - **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`

#### Example - Arithmetic Operators:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            int ans;
            int x = 20, y = 10;

            ans = (x + y);
            Console.WriteLine("Addition Operator: " + ans);

            ans = (x - y);
            Console.WriteLine("Subtraction Operator: " + ans);

            ans = (x * y);
            Console.WriteLine("Multiplication Operator: " + ans);

            ans = (x / y);
            Console.WriteLine("Division Operator: " + ans);

            ans = (x % y);
            Console.WriteLine("Modulo Operator: " + ans);

            ans = (x++);
            Console.WriteLine("Increment Operator: " + ans);

            ans = (x--);
            Console.WriteLine("Decrement Operator: " + ans);

            Console.ReadLine();
        }
    }
}
```

#### Example - Relational Operators:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            int a = 21, b = 10;

            if (a == b)
                Console.WriteLine("a is equal to b");
            else
                Console.WriteLine("a is not equal to b");

            if (a < b)
                Console.WriteLine("a is less than b");
            else
                Console.WriteLine("a is not less than b");

            if (a > b)
                Console.WriteLine("a is greater than b");
            else
                Console.WriteLine("a is not greater than b");

            // Change value of a and b
            a = 5; b = 20;

            if (a <= b)
                Console.WriteLine("a is either less than or equal to b");

            if (b >= a)
                Console.WriteLine("b is either greater than or equal to a");

            Console.ReadLine();
        }
    }
}
```

#### Example - Logical Operators:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            bool a = true;
            bool b = false;

            Console.WriteLine(a && b);
            Console.WriteLine(a || b);
            Console.WriteLine(!(a && b));

            Console.ReadLine();
        }
    }
}
```

#### Example - Assignment Operators:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            int a = 20;
            int ans;

            ans

 = a;
            Console.WriteLine("= | Value of ans = {0}", ans);

            ans += a;
            Console.WriteLine("+= | Value of ans = {0}", ans);

            ans -= a;
            Console.WriteLine("-= | Value of ans = {0}", ans);

            ans *= a;
            Console.WriteLine("*= | Value of ans = {0}", ans);

            ans /= a;
            Console.WriteLine("/= | Value of ans = {0}", ans);

            Console.ReadLine();
        }
    }
}
```
