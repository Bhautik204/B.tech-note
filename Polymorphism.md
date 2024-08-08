
### Definition

Polymorphism means "many forms", and it allows objects to be treated as instances of their parent class rather than their actual class. The two types of polymorphism in C# are compile-time (method overloading) and runtime (method overriding).

### Benefits

- **Flexibility**: The same interface can be used for different underlying forms (data types).
- **Maintainability**: Makes it easier to handle and maintain code.
- **Reusability**: Reuse existing code with different behaviors.

### Compile-time Polymorphism (Method Overloading)

```csharp
public class MathOperations
{
    // Method to add two integers
    public int Add(int a, int b)
    {
        return a + b;
    }

    // Method to add three integers
    public int Add(int a, int b, int c)
    {
        return a + b + c;
    }
}
```

#### Usage

```csharp
public class Program
{
    public static void Main(string[] args)
    {
        MathOperations math = new MathOperations();
        Console.WriteLine("Sum (2 args): " + math.Add(1, 2));
        Console.WriteLine("Sum (3 args): " + math.Add(1, 2, 3));
    }
}
```

### Runtime Polymorphism (Method Overriding)

```csharp
public class Animal
{
    public virtual void MakeSound()
    {
        Console.WriteLine("Animal makes a sound");
    }
}

public class Dog : Animal
{
    public override void MakeSound()
    {
        Console.WriteLine("Dog barks");
    }
}
```

#### Usage

```csharp
public class Program
{
    public static void Main(string[] args)
    {
        Animal animal = new Dog();
        animal.MakeSound();  // Calls the overridden method in Dog class
    }
}
```

### Interface Polymorphism

An interface can be implemented by multiple classes, and objects of these classes can be treated as objects of the interface type.

```csharp
public interface IMovable
{
    void Move();
}

public class Car : IMovable
{
    public void Move()
    {
        Console.WriteLine("Car is moving");
    }
}

public class Person : IMovable
{
    public void Move()
    {
        Console.WriteLine("Person is walking");
    }
}
```

#### Usage

```csharp
public class Program
{
    public static void Main(string[] args)
    {
        IMovable movable;

        movable = new Car();
        movable.Move();

        movable = new Person();
        movable.Move();
    }
}
```
#OOP 