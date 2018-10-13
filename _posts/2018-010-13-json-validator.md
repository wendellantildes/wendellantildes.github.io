---
layout: post
title: "A folder listener in .Net Core and .Net Standard."
date: 2018-07-22
categories: programming 
tags: [c#, .net, .netcore, leadingZero, webApi]

---

Salut, ça va 

Today we are going to discuss about a problem we face when we send an octal or an hexadecimal number in json. According to the official json specification , it’s not allowed to send these numbers in json, just decimal numbers. 

But, let’s see what happens in Asp .Net Core and Framework Web Api

![useful image]({{site.url}}/assets/json_validator/without_json_validator.png)

As we see above, this problem occurs because the official library in asp. Net implements the octal and decimal parse numbers and there is no way to turn this feature off . In majority of cases, I guess it’s not a problem , but in some cases it’s a huge problem. I faced this problem when at work we let available a resource in rest that updates some bank number accounts. So it was possible to send an hexadecimal number and mess up the original data with the wrong data in octal/hexadecimal. One possible solution was to put the field as string, but for some reasons they preferred to keep this field as an int. So I bring here an example of how we can solve this problem in our web api.

I found a [library](http://www.raboof.com/projects/jsonchecker/) called Json Checker listed on site json.org  and I updated the code to use it in new .Net Core. The implementation is available on [github](https://github.com/wendellantildes/JsonValidator) and via [nuget](https://www.nuget.org/packages/JsonValidatorTool/). 

Furthermore, for those who work with .Net Core Web Api, I coded an extension to validate all the requests with a json body. The implementation is available on [github](https://github.com/wendellantildes/JsonValidatorExtensions) and via nuget [nuget](https://www.nuget.org/packages/JsonValidatorExtensions.NetCore/).

After using JsonValidatorExtensions, now it’s possible to avoid octal and hexadecimal number via Web Api. 

![useful image]({{site.url}}/assets/json_validator/with_json_validator.png)

  <a href="/category/programming" class="badge badge-primary">Programming</a>

  
