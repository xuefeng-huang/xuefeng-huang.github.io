+++
author = "xuefeng huang"
date = "2016-04-18T18:30:55+08:00"
description = "find longest palindrome algorithm"
keywords = ["Algorithm"]
tags = ["Algorithm"]
title = "find longest palindrome in a given string"
type = "post"

+++
Problem:  
find the longest palindrome in a string, empty string will return 0  
solution:  
<script src="https://gist.github.com/xuefeng-huang/8d255586e72f2e8bf47ecdc96cd8b402.js"></script>
it use ```i``` as a window and ```j``` as a starting point of the window to each possible length of the palindrome, it tests with the whole length of the string first, the outer loop will decrease the window each time by 1, once it find a match just return the window size which would be the longest value. Cheers
