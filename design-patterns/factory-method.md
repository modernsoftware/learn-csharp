---
title: Factory Method
parent: Design Patterns
nav_order: 3
description: In the C# factory method responsibility for instantiating objects is deferred to a factory.
---

![banner](/banner.png)

# Factory Method
The responsibility for instantiating objects is delegated to a factory.

****

The Factory Method is a frequently used creational design pattern.

```csharp
using System;

namespace LearnCSharp
{
    class Program
    {
        static void Main(string[] args)
        {
            // Object creation is delegated to the factory
            MessageSenderFactory factory = new MessageSenderFactory();
            IMessageSender myMessageSender = factory.Create("sms");
            Console.WriteLine($"{myMessageSender.TransmitMessage()}");
        }
    }
}

// Factory
public class MessageSenderFactory
{
    public IMessageSender Create(string senderType)
    {
        if(senderType == "email")
        {
            return new Email();
        }
        else if(senderType == "sms")
        {
            return new SMS();
        }
        else
        {
            throw new NotImplementedException();
        }
    }
}

// Interface
public interface IMessageSender
{
    string TransmitMessage();
}

// Concrete class A
public class Email : IMessageSender
{
    public string TransmitMessage()
    {
        return "Message sent with email";
    }
}

// Concrete class B
public class SMS : IMessageSender
{
    public string TransmitMessage()
    {
        return "Message sent with SMS";
    }
}
```

```
Message sent with SMS
```

The MessageSenderFactory has been delegated the responsibility for creating the objects (Email and SMS).

The IMessageSender defines the interface for the objects (Email and SMS) that the factory creates.

****
## Comments
****
<div id="disqus_thread"></div>
<script>

var disqus_config = function () {
this.page.url = 'https://csharp.rclapp.com/design-patterns/factory-method.html';  
this.page.identifier = 'factory-method'; 
};

(function() {
var d = document, s = d.createElement('script');
s.src = 'https://csharper.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>