---
title: Getting Started
has_children: false
nav_order: 2
---

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

# Getting Started

You will write your code with the Microsoft Visual Studio IDE. You can download the IDE at the following link : 

[Download Visual Studio Community Edition (Free)](https://visualstudio.microsoft.com/downloads/)

## Create a console application

1. Open Visual Studio

2. On the start window, choose **Create a new project**

3. On the **Create a new project** window, enter **console** in the search box. Next, choose **C#** from the Language list, and then choose **Windows** from the Platform list

4. After you apply the language and platform filters, choose the **Console App (.NET Core)** template, and then choose **Next**

5. In the **Configure your new project** window, type or enter **HelloWorld** in the **Project name** box. Select a folder to store the project. Then, choose Create

## The application code

In the code editor, you will see the following C# code:

```csharp
using System;

namespace HelloWorld
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
    }
}

```

The code will write a line of text, 'Hello World', in the console window.

### Run the application

1. In the top menu look for the **HelloWorld** application with a green play button and click it to run the application.

2. Ensure the application is set to run in 'Debug' mode.

3. View the result of your application code in the console window.

4. Close the console window when you are done.

****
## Comments
****
<div id="disqus_thread"></div>
<script>

var disqus_config = function () {
this.page.url = 'https://csharp.rclapp.com/getting-started/getting-started.html';  
this.page.identifier = 'getting-started'; 
};

(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://csharper.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>

