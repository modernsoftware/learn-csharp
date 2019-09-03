---
title: Abstract Factory
parent: Design Patterns
nav_order: 4
description: In the C# abstract factory method a factory creates other factories, and these factories in turn create objects derived from interfaces.
---

# Abstract Factory
A factory that creates other factories, and these factories in turn create objects derived from interfaces.

****

The Abstract Factory Method is a frequently used creational design pattern.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("What meal do you prefer? (V)egan or (M)eat?");
            char input = Console.ReadKey().KeyChar;
            ICuisineFactory cuisineFactory;
            switch (input)
            {
                case 'V':
                    cuisineFactory = new VegetableDishFactory();
                    break;
                case 'M':
                    cuisineFactory = new MeatDishFactory();
                    break;
                default:
                    throw new NotImplementedException();
            }
            IMeal meal = cuisineFactory.Create();
            Console.WriteLine($"\nI got a {meal.Get()}");
        }
    }
}

// Abstract factory
public interface ICuisineFactory
{
    IMeal Create();
}

// Concrete factory A
public class VegetableDishFactory : ICuisineFactory
{
    public IMeal Create()
    {
        return new VegetableSoup();
    }
}

// Concrete factory B
public class MeatDishFactory : ICuisineFactory
{
    public IMeal Create()
    {
        return new Steak();
    }
}

// Abstract product
public interface IMeal
{
    string Get();
}

// Concrete product A
public class Steak : IMeal
{
    public string Get()
    {
        return "steak";
    }
}

// Concrete product B
public class VegetableSoup : IMeal
{
    public string Get()
    {
        return "vegetable soup";
    }
}
```

```
What meal do you prefer? (V)egan or (M)eat?
M
I got a steak
```

The ICuisineFactory interface is used to create the VegetableDishFactory and the MeatDishFactory.

These factories in turn create objects from the VegetableSoup and Steak classes using the IMeal interface.

****
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
## Comments
****
<div id="disqus_thread"></div>
<script>

var disqus_config = function () {
this.page.url = 'https://csharp.rclapp.com/design-patterns/abstract-factory.html';  
this.page.identifier = 'abstract-factory'; 
};

(function() {
var d = document, s = d.createElement('script');
s.src = 'https://csharper.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>