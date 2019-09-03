---
title: Attributes
has_children: false
nav_order: 7
description: C# attributes provide a method of associating metadata with assemblies, classes, methods, properties, etc.
---

# Attributes
Attributes provide a method of associating metadata with assemblies, classes, methods, properties, etc.

****

After an attribute is associated with an entity, the attribute can be queried at run time.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            // Get the attribute
            Attribute[] attrs = Attribute.GetCustomAttributes(typeof(Adder));
            foreach (Attribute attr in attrs)
            {
                if (attr is Developer)
                {
                    Developer developer = (Developer)attr;
                    Console.WriteLine($"{developer.GetName()} wrote the class {nameof(Adder)}");
                }
            }
        }
    }
}
// Use the attribute
[Developer("Anil")]
public class Adder
{
    public int Execute(int x, int y)
    {
        return x + y;
    }
}
// Create an attribute
[AttributeUsage(AttributeTargets.Class)]
public class Developer : Attribute
{
    private string Name;

    public Developer(string name)
    {
        Name = name;
    }

    public string GetName()
    {
        return Name;
    }
}
```

```
Anil wrote the class Adder
```

The Developer attribute has a property called Name that we will use to identity the developer who wrote a class.

We add the attribute to the Adder class and specify the name of the developer who wrote the class as metadata for the class.

Finally, we locate the Developer custom attribute for the Adder class and use it to print the name of the developer who wrote the class in the console window.

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
this.page.url = 'https://csharp.rclapp.com/attributes.html';  
this.page.identifier = 'attributes'; 
};

(function() {
var d = document, s = d.createElement('script');
s.src = 'https://csharper.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>

