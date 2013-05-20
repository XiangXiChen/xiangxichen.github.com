---
layout: post
title: "C++ -- About Return Type"
date: 2013-04-24
comments: true
categories: blog
tags: [C++] 
---
**学习中......**<br/><br/>
**PROBLEMS**<br/>
1.类成员函数的返回值。<br/>
<code>
//返回类成员变量的类型为类对象
class AClass{<br/>
public:<br/>
	std::string getFeild(){ return mField; }<br/>
	const std::string& getFeildBetter(){ return mField; }<br/>
private:<br/>
	std::string mField;<br/>
}<br/>
void fun(const char* str);
void main(){<br/>
	AClass a;
	fun(a.getFeild().c_str());//Bad, Might be Crash
	fun(a.getFeildBetter().c_str());//No problem.
}
</code>
<br/>

---

引用<br/>