---
layout: essay
type: essay
title: "Behind the Screens: My Journey with UI Frameworks"
# All dates must be YYYY-MM-DD format!
date: 2024-02-22
published: true
labels:
  - UI Design
  - Bootstrap 5
  - Web Development
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## The Reality

Previously, I have worked on website building with premade applications such as RapidWeaver and Wordpress where I simply clicked on and put together icons to publish websites without having to write out a single line of code. I thought website building was easy and fun like that, until I was faced with the reality of what goes on behind the schenes--where the magic occurs in order for me to access web building applications in the first place.

Here, I discovered that User Interface (UI) are heroes of the digital world. Amongst UI, you would probably think of HTML or CSS, but throughout that, one particular framework I have been utilizing is Bootstrap 5.

## Why use a framework instead of raw code?

Bootstrap is one of the most popular frameworks containing of HTML, CSS and JavaScript-based design templates to offer a comprehensive set of tools that streamline the development process. 

```
Q: python date of the previous month

I am trying to get the date of the previous month with python. Here is what i've tried:

str( time.strftime('%Y') ) + str( int(time.strftime('%m'))-1 )

However, this way is bad for 2 reasons: First it returns 20122 for the February of 2012 (instead of 201202) 
and secondly it will return 0 instead of 12 on January.

I have solved this trouble in bash with:

echo $(date -d"3 month ago" "+%G%m%d")

I think that if bash has a built-in way for this purpose, then python, much more equipped, should provide something 
better than forcing writing one's own script to achieve this goal. Of course i could do something like:

if int(time.strftime('%m')) == 1:
    return '12'
else:
    if int(time.strftime('%m')) < 10:
        return '0'+str(time.strftime('%m')-1)
    else:
        return str(time.strftime('%m') -1)
        
I have not tested this code and i don't want to use it anyway (unless I can't find any other way:/)

Thanks for your help!
```

