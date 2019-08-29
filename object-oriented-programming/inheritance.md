---
title: Inheritance
parent: Object Oriented Programming
nav_order: 4
description: Inheritance in C# allows you to extend the functionality of an existing class by creating a new class that derives from the inherited class.
---

<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<!-- horizontal_display_ad -->
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-0640869077433160"
     data-ad-slot="8459798581"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>

****
# Inheritance

Inheritance allows you to extend the functionality of an existing class by creating a new class that derives from the inherited class.

****

The following code illustrates inheritance.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            Cylinder myCylinder = new Cylinder();
            myCylinder.Radius = 5;
            myCylinder.Height = 12;

            Console.WriteLine($"The radius of the cylinder is {myCylinder.Height}");
        }
    }
}

public class Circle
{
    public int Radius { get; set; }
}

public class Cylinder : Circle
{
    public int Height { get; set; }
}
```

```
The radius of the cylinder is 12
```

The Circle class has a property named Radius of type integer. 

The Cylinder class inherits from the Circle class. We use the colon (:) to define the inheritance. 

The Cylinder class , because it inherits from the Circle class, will also have a property named Radius. 

## Method Overrides

The override modifier is required to extend or modify the virtual implementation of an inherited method.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            Cylinder myCylinder = new Cylinder();
            myCylinder.Radius = 2;
            myCylinder.Height = 3;
            decimal surfaceArea = myCylinder.CalculateSurfaceArea();

            Console.WriteLine($"The surface area of the cylinder is {surfaceArea}");
        }
    }
}

public class Circle
{
    public int Radius { get; set; }

    public virtual decimal CalculateSurfaceArea()
    {
        return 2 * 3.14M * Radius;
    }
}
public class Cylinder : Circle
{
    public int Height { get; set; }

    public override decimal CalculateSurfaceArea()
    {
        return (2 * 3.14M * Radius * Height) + (2 * 3.14M * Radius * Radius);
    }
}
```

The Circle class has a virtual method called CalculateSurfaceArea() that calculates the surface area of a circle. The 'virtual' keyword is used to declare that this method is a virtual method and can be overridden. 

The Cylinder class inherits from the Circle class, however, the function to calculate the area of a circle is different from the function to calculate the area of a cylinder. 

Therefore, in the Cylinder class, we can override the method to provide a function to calculate the surface area of a cylinder (as shown in the code). We use the keyword 'override' to override the method.

****
## Comments
****
<div id="disqus_thread"></div>
<script>

var disqus_config = function () {
this.page.url = 'https://csharp.rclapp.com/object-oriented-programming/inheritance.html';  
this.page.identifier = 'inheritance'; 
};

(function() {
var d = document, s = d.createElement('script');
s.src = 'https://csharper.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>