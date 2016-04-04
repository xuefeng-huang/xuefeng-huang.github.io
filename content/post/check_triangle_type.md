+++
author = "xuefeng huang"
date = "2016-04-04T11:10:29+08:00"
description = "how to check triangle type given 3 sides"
keywords = ["algorithm"]
tags = ["Algorithm"]
title = "how to check triangle type given length of 3 sides"
type = "post"

+++
solved this problem on Codewars about checking for triangle type, the 3 sides of the triangle are given, the program need to determine whether a triangle can be formed, it is a right angle, acute type or obtuse type.  
At first I thought about calculating the angle between 2 sides, but that would be a lot work to be carried out. Turns out according to Pythagorean Theorem there is a simple way to check that:  
1. sort given 3 sides, a > b > c<br>
2. if a + b <= c, they cannot form a triangle<br>
3. if a^2 + b^2 = c^2, it is right angel<br>
4. if a^2 + b^2 > c^2, it is acute<br>
5. if a^2 + b^2 < c^2, it is obtuse<br>
cheer. **#power_of_math**
