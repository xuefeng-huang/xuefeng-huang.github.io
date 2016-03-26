+++
author = "xuefeng huang"
date = "2016-03-26T10:16:00+08:00"
description = "some observation of Android activity"
keywords = ["Android"]
tags = ["Android"]
title = "Android activity finding"
type = "post"

+++

Started making a toy Android app call Chafia recently, it is an education app to show the different coffee names used when ordering in a local coffee shop here in Singapore. It is confusing for a foreigner first arrived here, the terms used consists of lots of Cantonese, Hainan and Hokkien dialect.  
The app has one main activity A and it starts another activity B upon clicking one text view, **A -> B**, on activity B I put up a button to go back to A after clicking that, **B -> A**, I did not kill activity B in this step. What will happen is that if I clicking back button which the phone provides it goes back to B first then to A again instead of exiting from A directly. After some thought, I changed it to killing B by calling finish function before switching to A, this time it worked. It exits from A right away. Seems like I need to know more about activity life cycle next. 

