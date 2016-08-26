---
layout: post
title: "How to debug Maven Applications in Intellij IDEA"
description: ""
category: quick-fix
tags: [Intellij]
---

在maven工程里面, 本地要进行debug的话, 首先到 Run -> Edit Congfigurations :

<img src="{{ site.url }}/images/posts/201507/img01.png" width="68%"/>

在Run/Debug Congfigurations窗口, 增加一个maven配置:

<img src="{{ site.url }}/images/posts/201507/img02.png" width="68%"/>

在maven配置窗口, 有Parameters, Gerneral, Runner这3个tab, 主要是设置Parameters下面的Command Line:

<img src="{{ site.url }}/images/posts/201507/img03.png" width="68%"/>

比如这里填的是运行一个maven的命令行程序, 使用了maven的Exec Maven Plugin:

```
exec:java -Dexec.mainClass=TopologyMain -Dexec.args=src/main/resources/words.txt
```

设置完之后, 就可以设置断点, 选择刚刚的Maven配置进行debug了.


[参考原文](http://hippieitgeek.blogspot.se/2014/02/how-to-debug-maven-applications-in.html)  
