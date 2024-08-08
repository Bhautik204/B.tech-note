### What is Inheritance?

Inheritance is a fundamental concept in object-oriented programming (OOP) that allows a class (derived class) to inherit properties and methods from another class (base class).

### Benefits of Inheritance

1. **Code Reusability**: Reuse existing code without rewriting it.
2. **Code Maintenance**: Easier to manage and maintain the code.
3. **Extensibility**: Extend the functionality of existing classes.
### Disadvantages of Inheritance
1. T**ight Coupling**: tight coupling between base class and derived class , make the  code more difficult to maintain.
2. **Complexity**: Increase complexity of code by introducing additional levels of abstraction.
3. **Fragility**: Make code more fragile by creating dependencies between the base class and derived class 
#### Syntax:
```csharp
class DerivedClass : BaseClass
{
    // Derived class members
}
```
### Types of Inheritance

#### 1. Single Inheritance

A derived class inherits from a single base class.
##### Example - Single Inheritance:
```csharp
class Teacher
{
    public void Teach()
    {
        Console.WriteLine("Teach");
    }
}

class Student : Teacher
{
    public void Learn()
    {
        Console.WriteLine("Learn");
    }
}

class Program
{
    static void Main(string[] args)
    {
        Teacher t = new Teacher();
        t.Teach();

        Student s = new Student();
        s.Learn();
        s.Teach();

        Console.ReadKey();
    }
}
```


#### 2. Multi-Level Inheritance

A class is derived from another derived class, creating a chain of inheritance.
#####  Example - Multi-level Inheritance:
```csharp
class Teacher
{
    public void Teach()
    {
        Console.WriteLine("Teach");
    }
}

class Student : Teacher
{
    public void Learn()
    {
        Console.WriteLine("Learn");
    }
}

class SemFour : Student
{
    public void FourthSem()
    {
        Console.WriteLine("Semester Four Students");
    }
}

class Program
{
    static void Main(string[] args)
    {
        Teacher t = new Teacher();
        t.Teach();

        Student s = new Student();
        s.Learn();
        s.Teach();

        SemFour sem = new SemFour();
        sem.Learn();
        sem.Teach();
        sem.FourthSem();

        Console.ReadKey();
    }
}
```


#### 3. Hierarchical Inheritance

Multiple derived classes inherit from a single base class.
#####  Example:
```csharp
class Person
{
    public void Walk()
    {
        Console.WriteLine("Walking...");
    }
}

class Teacher : Person
{
    public void Teach()
    {
        Console.WriteLine("Teaching...");
    }
}

class Student : Person
{
    public void Learn()
    {
        Console.WriteLine("Learning...");
    }
}
public class Program
{
    public static void Main(string[] args)
    {
        Teacher teacher = new Teacher();
        teacher.Teach();
        teacher.Walk();

        Student student = new Student();
        student.Learn();
        student.Walk();
    }
}
```

### Base Keyword

The `base` keyword is used to access members of the base class from within a derived class.

#### Example:
```csharp
class Person
{
    public string Name;

    public Person(string name)
    {
        Name = name;
    }
}

class Student : Person
{
    public Student(string name) : base(name)
    {
    }

    public void Display()
    {
        Console.WriteLine("Name: " + Name);
    }
}
```

#### Usage:
```csharp
public class Program
{
    public static void Main(string[] args)
    {
        Student student = new Student("John");
        student.Display();
    }
}
```
#OOP 