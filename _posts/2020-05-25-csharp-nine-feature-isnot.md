---
layout: post
title: "C# 9 - Logical Patterns: Is Not"
date: 2020-05-25
categories: programming 
tags: [c#, .net, .netcore, .net5, csharp9]

---

Hey, long time no see, huh?

In times of new c# 9 and new dotnet 5, I am very excited to write a little bit about them.

Then, now we can combine the logical operator **not** in **if-conditions**.

In the old way, we used to do:

``` c#
if(!(word is null))
```

Now:

``` c#
if (word is not null)
```
The readibility has improved a lot and it is a good thing.

You can find an examble [here](https://github.com/wendellantildes/dotnet5labs/blob/master/IsNotExample/Program.cs). For more details, see the [official post](https://devblogs.microsoft.com/dotnet/welcome-to-c-9-0/).

<a href="/category/programming" class="badge badge-primary">Programming</a>

  
