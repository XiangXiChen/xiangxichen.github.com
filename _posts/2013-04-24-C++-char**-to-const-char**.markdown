---
layout: post
title: "C++ -- char** to const char**"
date: 2013-04-24
comments: true
categories: blog
tags: [C++] 
---
**学习中......**<br/><br/>
**PROBLEMS**<br/>
<code>
char** t;<br/>
const char** t1 = t;//invalid conversion from char** to const char**. but WHY?<br/><br/>
//A workaround<br/>
char** t;<br/>
const char* t2 = *t;//Convert to const char* first.<br/>
const char** t1 = &t2;//OK, here, but WHY?<br/>
</code>
<br/>

---

引用<br/>
1. [http://www.cnblogs.com/chenleiustc/archive/2011/04/09/2010647.html](http://www.cnblogs.com/chenleiustc/archive/2011/04/09/2010647.html)<br/>