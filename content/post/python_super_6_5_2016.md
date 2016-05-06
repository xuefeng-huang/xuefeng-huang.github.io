+++
author = "xuefeng huang"
date = "2016-05-06T15:48:38+08:00"
description = "Understand Python super()"
keywords = ["Python"]
tags = ["Python"]
title = "Python super() and MRO"
type = "post"

+++
I have been wondering how super() works in Python, it has been added to solve the multi-inheritance initialization problem. I have read through some documents explaining of it. Now I am more clear. It does not call the parent directly as its name suggests, instead it searches the MRO list and returns the next class based on the current class, the following code explains better:  
```
def super(cls, inst):
    mro = inst.__class__.mro()
    return mro[mro.index(cls) + 1]
```
it searches the MRO list provided by ```inst```, and return the next class from it. The MRO uses an algorithm called C3 in which children precede their parents and the order of appearance in base classes is respected.  
super() only works on new style classes in Python 2 though.

reference:  
<ul>
    <li>[https://laike9m.com/blog/li-jie-python-super,70/ (Chinese)](https://laike9m.com/blog/li-jie-python-super,70/)</li>
    <li>[https://rhettinger.wordpress.com/2011/05/26/super-considered-super/](https://rhettinger.wordpress.com/2011/05/26/super-considered-super/)</li>
</ul>

