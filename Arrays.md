- **Arrays**: A collection of similar types of data.
- **Declaration**:
  ```csharp
  Datatype[] arrayName;
  ```

#### Example - Array:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            int[] ages = new int[5];
            ages[0] = 10;
            ages[1] = 20;
            ages[2] = 30;
            ages[3] = 40;
            ages[4] = 50;

            for (int i = 0; i < ages.Length; i++)
            {
                Console.WriteLine("Age of student {0}: {1}", i + 1, ages[i]);
            }

            Console.ReadLine();
        }
    }
}
```

#c-sharp 