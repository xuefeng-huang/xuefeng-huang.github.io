+++
author = "xuefeng huang"
date = "2016-03-23T10:45:13+08:00"
description = "thought about Java static method"
keywords = ["Java"]
tags = ["Java"]
title = "Java static method"
type = "post"

+++
As we all kown that in Java static method using non-static member variable is not allowed. But why is that? I watched a Java training video yesterday and the author used proof by contridiction to think about why. Looking at it from another point of view:  
Assuming that we can use non-static member in a static method, then that member must belongs to an object, but when invoking static method there is no object needed. So the variable in static method should not be a normal instant variable. The assumption make earlier is not true. That's it, <em>#powerOfLogic</em> 
