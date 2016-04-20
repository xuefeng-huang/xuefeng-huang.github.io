+++
author = "xuefeng huang"
date = "2016-04-20T17:11:09+08:00"
description = "Django template variable lookup"
keywords = ["Python"]
tags = ["Python", "Django"]
title = "Django template variable lookup"
type = "post"

+++
when use the dot notation such as ```{{ user.name }}``` in Django template. Django will do the following 4 steps to look up the variable on object ***user***  
<ol>
    <li>dictionary lookup (use name as a key)</li>
    <li>attribute lookup</li>
    <li>method call</li>
    <li>list index lookup (use name as a index)</li>
</ol>
Cheers