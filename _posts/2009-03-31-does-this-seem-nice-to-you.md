---
title: Does this seem nice to you?
date: 2009-03-31 15:58
author: aabs
category: .NET, humour, programming
slug: does-this-seem-nice-to-you
status: published
...

After years of recoiling at the sight of code like this, am I supposed now to embrace it in a spirit of reconciliation?

``` {.wp-block-syntaxhighlighter-code}
namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            dynamic blah = GetTheBlah();
            Console.WriteLine(blah);
        }

        private static dynamic GetTheBlah()
        {
            if (DateTime.Now.Millisecond % 3 == 0)
                return 0;
            else
                return "hello world!";
        }
    }
}
```

need to wash my hands.
