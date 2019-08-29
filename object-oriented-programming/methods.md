---
title: Methods
parent: Object Oriented Programming
nav_order: 2
---

# Methods

A method carries out a function within a class.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            Square mySquare = new Square(4);
            int area = mySquare.CalculateArea();

            Console.WriteLine($"The area of a square with side {mySquare.Side} is {area}");
        }
    }
}

public class Square
{
    public Square(int side)
    {
        Side = side;
    }

    public int Side { get; set; }

    public int CalculateArea()
    {
        return Side * Side;
    }
}
```

```
The area of a square with side 4 is 16
```

In the Square class, we have a method named CalculateArea, this method does not take any arguments. 

The method uses the Side property to calculate the area of the square. The method returns an integer value for the area (Side * Side).
