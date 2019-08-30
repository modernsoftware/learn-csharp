---
title: Types
has_children: false
nav_order: 3
description: C# types
---

# Types
C# is a strongly typed language. Every variable must be defined by a type. 

****

The following is a list of common types used in C#:

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
this.page.url = 'https://csharp.rclapp.com/types/types.html';  
this.page.identifier = 'types'; 
};

(function() {
var d = document, s = d.createElement('script');
s.src = 'https://csharper.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
