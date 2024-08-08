
### Definition

Abstraction is the concept of hiding the complex implementation details and showing only the essential features of the object. It helps in reducing programming complexity and effort.

### Benefits

- **Simplicity**: Simplifies the design by providing a clear interface.
- **Reusability**: Encourages the reuse of existing code.
- **Security**: Hides the implementation details, protecting the data.

### Example

```csharp
public abstract class Shape
{
    // Abstract method (does not have a body)
    public abstract double GetArea();
}

public class Circle : Shape
{
    private double radius;

    public Circle(double radius)
    {
        this.radius = radius;
    }

    // Override the GetArea method
    public override double GetArea()
    {
        return Math.PI * radius * radius;
    }
}
```

#### Usage

```csharp
public class Program
{
    public static void Main(string[] args)
    {
        Shape shape = new Circle(5);
        Console.WriteLine("Area: " + shape.GetArea());
    }
}
```
#OOP 