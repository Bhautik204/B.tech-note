Sure! Let's dive deeper into constructors and inheritance with more detailed explanations and examples.

---

# C# Fundamentals

## Constructors

### What is a Constructor?

A constructor is a special method in a class that is automatically called when an instance of the class is created. Constructors are used to initialize objects.

### Characteristics of Constructors

1. **Same Name as Class**: A constructor must have the same name as the class it is defined in.
2. **No Return Type**: Constructors do not have a return type, not even `void`.
3. **Automatically Called**: They are called automatically when an object is created.
4. **Can be Overloaded**: Multiple constructors can be defined in a class with different parameter lists.

### Types of Constructors

#### 1. Default Constructor

A default constructor does not take any parameters. If no constructor is defined, C# automatically provides a default constructor.

```csharp
public class Student
{
    public Student()
    {
        // Default constructor
    }
}
```

#### 2. Parameterized Constructor

A parameterized constructor takes one or more arguments. It allows the object to be initialized with specific values at the time of creation.
```csharp
using System;

namespace MyFirstApp
{
    class Program
    {
        public static void Main(string[] args)
        {
            Users user = new Users("Naimish", 30);
            user.GetUserDetails();
            Console.ReadLine();
        }
    }

    public class Users
    {
        public string Name = string.Empty;
        public int Age = 0;

        public Users(string name, int age)
        {
            Name = name;
            Age = age;
        }

        public void GetUserDetails()
        {
            Console.WriteLine("Name: {0} Age: {1}", Name, Age);
        }
    }
}

```
#### 3. Copy Constructor

A copy constructor initializes an object using another object of the same class.

```csharp
using System;

namespace MyFirstApp
{
    public class Users
    {
        public string Name = string.Empty;
        public int Age = 0;

        public Users(string name, int age)
        {
            Name = name;
            Age = age;
        }

        public void GetUserDetails()
        {
            Console.WriteLine("Name: {0} Age: {1}", Name, Age);
        }

        public Users(Users user)
        {
            this.Name = user.Name;
            this.Age = user.Age;
        }
    }

    class Program
    {
        public static void Main(string[] args)
        {
            Users user1 = new Users("Naimish", 30);
            Users user2 = new Users(user1);
            user2.GetUserDetails();
            Console.ReadLine();
        }
    }
}

```

### Constructor Chaining

Constructor chaining is the process of calling one constructor from another constructor in the same class or in the base class.

#### Example:
```csharp
public class Student
{
    public string Name;
    public int Age;

    // Default Constructor
    public Student() : this("Unknown", 0)
    {
    }

    // Parameterized Constructor
    public Student(string name, int age)
    {
        Name = name;
        Age = age;
    }
}
```

#### Usage:
```csharp
public class Program
{
    public static void Main(string[] args)
    {
        Student student = new Student();
        Console.WriteLine("Name: " + student.Name);
        Console.WriteLine("Age: " + student.Age);
    }
}
```
#OOP 
