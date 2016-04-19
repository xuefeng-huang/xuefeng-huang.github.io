+++
author = "xuefeng huang"
date = "2016-04-19T17:54:33+08:00"
description = "Python virtualenv notes"
keywords = ["Python"]
tags = ["Python"]
title = "Python virtualenv notes"
type = "post"

+++
virtualenv is good to work with. Here is some best practice when using it:  
<ol>
<li>create .virtualenvs folder in home directory</li>
<li>use ```virtualenv foldername``` to create virtualenv in that .virtualenvs</li>
<li>put all project code in home directory dev folder</li>
<li>activate virtualenv and navigate to the correct folder in dev</li>
</ol>
But there is a handy tool out there to manage all there steps, **virtualenvwrapper**.  
first add the following to the .profile in the home directory  
```sh
export PROJECT_HOME=$HOME/dev
source /usr/local/bin/virtualenvwrapper.sh
```
this will let the wrapper know where all project code is, then use ```mkvirtualenv name``` to make virtualenv in .virtualenvs folder and it automatically activates it. After that, go to the actual code folder in dev and type ```setvirtualenvproject``` to bind the virtualenv to the project folder. There is an even easier command ```mkproject name```, it create a virtualenv and a project folder in dev, link them up, switch to the project folder all in one step. To switch between projects, just issue ```workon name``` to activate that virtualenv and go inside the project folder. Neat!