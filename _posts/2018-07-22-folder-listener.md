---
layout: post
title: "A folder listener in .Net Core and .Net Standard."
date: 2018-07-22
categories: programming 
tags: [c#, .net, .netcore]

---

Salut, tout le Monde

This week I needed to code a solution that listens to a folder and get any pasted file to format it. Who uses .Net probably knows the solution using FileSystemWatcher. This solution works well when we don’t put several files in the folder at once. The problem is when Changed event raises twice or more times for one file . I searched for some workaround to solve this and I didn’t like very much the solutions I found. So, I talked to my friend about my problem and he shared with me a simple solution with threads and for me it worked like magic. So, as I have seen many developers with this problem, I coded an example using .NetCore and .NetStandard. Voilà the  [link](https://github.com/wendellantildes/FolderListener). Any ideas are welcome. 

  <a href="/category/programming" class="badge badge-primary">Programming</a>

  
