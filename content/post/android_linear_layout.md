+++
author = "xuefeng huang"
date = "2016-04-12T16:44:46+08:00"
description = "Layout_weight in LinearLayout"
keywords = ["Android"]
tags = ["Android"]
title = "understand Layout_weight in LinearLayout"
type = "post"

+++
I always think that when specify layout_weight for views inside LinearLayout would calculate the width or height of all views based on the whole parent layout. But it is not.  
It turns out to be that they share the remaining space of the parent layout, according to what the weight is assigned to them. The trick to set their width or height to 0dp is so that the remaining space is the width or height of the parent layout. So the views on the layout would share the space not affected by the content already inside the view. Kinda important concept.

