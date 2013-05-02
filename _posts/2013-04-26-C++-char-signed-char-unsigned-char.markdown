---
layout: post
title: "C++ -- char VS signed char VS unsigned char"
date: 2013-04-24
comments: true
categories: blog
tags: [C++] 
---
**学习中......**<br/><br/>
**WHAT**<br/>
<code>char</code>:字符类型，但是不确定是有符号还是无符号类型，由编译器相关的。<br/>
<code>signed char</code>:有符号字符类型。一个字节大小，范围：-128 至 127<br/>
<code>unsigned char</code>：无符号字符类型。一个字节大小，范围：0 至 255<br/>
<br/>

**IDIOMS**<br/>

* 务必显式指定char类型的符号，因为char类型的符号是不确定的，在跨平台的应用中，直接使用char类型的程序容易出错。

**PROBLEM**<br/>

* 为什么signed char的范围是-128至127？<br/>
由于有符号char的0有两种方法：负零(1000 0000)和正零(0000 0000)。但是零并没有正负之分，所以把负零(1000 0000)定义为-128，因此signed char的范围为-128至127。

---

引用<br/>
1. [http://www.cnblogs.com/chenleiustc/archive/2011/04/09/2010647.html](http://www.cnblogs.com/chenleiustc/archive/2011/04/09/2010647.html)<br/>