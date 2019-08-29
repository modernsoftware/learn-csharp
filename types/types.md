---
title: Types
has_children: false
nav_order: 3
---

# Types
C# is a strongly typed language. Every variable must be defined by a **type**. The following is a list of common types used in C#:

- string
- int
- long
- bool
- double
- decimal

## Strings

The string type is used for text. The following code shows an example of use of the string variable.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            string name = "Anil";
            Console.WriteLine($"Hello {name}");
        }
    }
}
```

```
Hello Anil
```

## Integers

Integers (**int**) are used to represent whole numbers (e.g. 3, 5, etc.). The range for the int type is :  -2,147,483,648 to 2,147,483,647.

The **long** type has a greater range : -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            int x = 1;
            int y = 3;
            int sum = x + y;
            Console.WriteLine($"Sum : {sum.ToString()}");
        }
    }
}
```

```
Sum : 4
```

## Bool

The type bool is used to represent true or false(Boolean) values.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            bool b = true;
            Console.WriteLine($"{b.ToString()}");
        }
    }
}
```

```
True
```

## Arrays

You can store multiple variables of the same type in an array data structure. You declare an array by specifying the type of its elements. Note the index starts from 0.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            int[] numbers = { 3, 0, 4, 8, 2 };
            int a = numbers[3];
            Console.WriteLine($"The fourth number in the array is : {a.ToString()}");
        }
    }
}

```

```
The fourth number in the array is : 8
```
