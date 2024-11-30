
# C# Fundamentals

## Introduction to C# #

- **C# (C-Sharp)**: A general-purpose, modern, [[Object-Oriented Programming Language]].
- **Pronunciation**: "C sharp"
- **Origin**: Derived from the C family (C++ and Java).
- **First Version**: Released in 2002.
- **Latest Version**: C# 12.0 (November 2023).
- **Developed by**: Microsoft, led by Anders Hejlsberg.
- **Uses**: Mobile, desktop, web applications, web services, websites, games, VR, database applications, etc.
- **Key Features**:
  - **Case-sensitive**: `MyClass` and `myclass` are different.
  - **Object-oriented**: Organise code into objects.
  - **Structured**: Programs can be divided into smaller parts using functions.
  - **Simple to use**: Provides a structured approach and is user-friendly.
  - **Scalable**: Automatically updates and replaces old files.

## .NET Core vs .NET Framework

### .NET Core
- **Released**: 2016
- **Cross-platform**: Runs on Windows, Mac, and Linux.
- **Usage**: Building web apps (ASP.NET Core apps), mobile apps, and Universal Windows Platform apps.
- **Supports**: Micro-services and REST API creation.
- **Performance**: Enhances app performance without hardware changes.

### .NET Framework
- **Released**: 2002
- **Platform**: Windows only.
- **Usage**: Building web apps, desktop apps, and web services.
- **Limitations**: Lower performance, less flexibility, security, and speed compared to .NET Core. 
- Does not support micro-services.

## Key Concepts

### Hello World Program

```csharp
using System;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            // This is a comment.
            Console.WriteLine("Hello World!");
            Console.WriteLine("Press Enter Key to Exit.");
            Console.ReadLine();
        }
    }
}
```

- **using System;**: Imports the System namespace to use existing class methods like `WriteLine()` and `ReadLine()`.
- **namespace HelloWorld**: Defines the scope containing classes.
- **class Program**: Defines a class named Program.
- **static void Main(string[] args)**: The entry point of the application.
  - **static**: Main method is accessible without instantiating the class.
  - **void**: Method does not return a value.
  - **Console.WriteLine()**: Writes a text to the console.
  - **Console.ReadLine()**: Reads input from the console.

### [[Namespaces]]
### [[Console Class Methods]]

### [[Data Types & Variables]]

### [[Operators]]

### [[Arrays]]

### [[Strings]]

### [[Classes & Objects]]

### [[Constructors]]

### [[Inheritance]]

#c-sharp