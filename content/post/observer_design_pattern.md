+++
author = "xuefeng huang"
date = "2016-04-03T15:12:28+08:00"
description = "Java observer design pattern note"
keywords = ["design pattern"]
tags = ["Java"]
title = "Java observer design pattern review"
type = "post"

+++
I tried to study **RxJava** cause it seems popular and I saw a lot people writing articles about it. But after some introduction guides, it seems observer pattern is used heavily hence I read up on some information about observer pattern.  
Java provides observable class which has methods to register observers, notify all observer once certain status is changed etc. All observers must implements observer interface, each observable object maintain a list of observers registered with it, once an event happens in observable it in turn update all observers by calling the function inside the observer interface.  
```java
public void notifyObserver() {   
       // Cycle through all observers and notifies them of
       // price changes           
          for(Observer observer : observers){              
              observer.update(ibmPrice, aaplPrice, googPrice);
               
          }
      }
```
reference:  
- [Observer Design Pattern Tutorial](http://www.newthinktank.com/2012/08/observer-design-pattern-tutorial/)

