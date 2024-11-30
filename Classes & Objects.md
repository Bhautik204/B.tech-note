
- **Class**: A blueprint for objects that defines attributes and behaviors.
- **Object**: An instance of a class.

#### Example - Class Declaration:
```csharp
public class Users
{
    public int id = 0;
    public string name = string.Empty;

    public void GetUserDetails()
    {
        Console.WriteLine("Enter your user id:");
        id = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("Enter your name:");
        name = Console.ReadLine();
        Console.WriteLine("Id: {0} Name: {1}", id, name);
        Console.ReadLine();
    }
}
```

#### Example - Object Creation:
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            Users user = new Users();
            user.GetUserDetails();
        }
    }
}
```

#c-sharp 