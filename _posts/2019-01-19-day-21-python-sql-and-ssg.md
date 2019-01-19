---
layout: "post"
title: "Day 21: Python, SQL, and SSG"
date:   2019-01-19 11:33:00 -0600
---

## Today's highlights

This is where I'll write today's highlights.

## Python

Today I reviewed a lot of Python concepts. I also made assumptions about Python based on my previous programming language knowledge. It turns out I was wrong in a couple of ways. 

### The global keyword

You need to use the ```global``` keyword in Python to specify that you're referencing a global variable rather than a local one. No wonder my IDE gave me messages about variable shadowing. I was practically pulling out my hair the other day because of scope issues that I didn't understand. The solution is actually really simple. I never had to use a ```global``` keyword in Java, but Python is not Java. You might think OOP languages are all the same, but there are enough differences for it to be confusing without reviewing a lot of seemingly basic concepts. Some other simple differences include how Java's indentation is optional, whereas indentation is forced in Python. Not only that, but 

### Shebangs

I first learned about shebangs (```#!```) in community college when I took a course about Linux and Unix. Among other things, the class taught command line utilities, vim, pipes, man pages, SSH, and shell scripting. The shebang for a shell script might be something like ```#!/bin/bash```. Of course, you can also specify environment variables rather than absolute paths, just in case there are some non-standard locations for installations. Additionally, not all systems will have the same default shell, so ```#!/bin/sh``` isn't a very good idea. You can always do ```echo $SHELL``` to see your current shell, but now I'm getting slightly off-topic.

Shebangs aren't just for shell scripts. They're sometimes (but not always) used in python too. A shebang, like ```#!/usr/bin/env python3```, isn't actually necessary to run a Python script in an editor, or by specifically running it with ```python3 whatever.py```. But if you mark a .py file as executable and try to execute it like ```./whatever.py```, if there is no shebang, your computer might not know how to execute it. It depends on a number of things, like your path variable and operating system. For example, on my Windows machine, ```python``` is used to run python3, but on my mac, I have to use ```python3```. And PyCharm doesn't require you to use a shebang, but if you only run your programs in an IDE, and especially with just a default build configuration, then you can miss out on how a lot of people will be running the program (most notably a terminal window)

## My favorite editors and terminals

I like command line stuff a whole lot. I feel very comfortable doing text-based commands. I think it's inexcusable for someone to be a programmer and not know their way around a shell. Some things are simply more efficient with command line as opposed to a GUI. On Windows, I know use ConEmu. Below is what my current workflow looks like. Some peole say cmder is better than ConEmu, but it was buggy for me, and their site didn't even have an SSL certificate, which isn't reassuring. So I will stick with ConEmu.

Click to view full size screenshot (1080p):

<a href="/assets/conemu.png"><img src="/assets/conemu_thumbnail.png"></a>

I prefer IDEs and graphical editors, such as VS Code, PyCharm, and IntelliJ. I use VS Code for web development and I've even used it for C/C++ even though CLion is arguably a better option for that. PyCharm is for Python, and IntelliJ IDEA is for Java. 

I also use vim for some basic stuff, like editing markdown files, or doing quick fixes, but I honestly don't prefer it for more serious work. Of course, it's good to use it occasionally, because then you are forced to learn about compiling, linking, loading, etc. One issue with modern IDEs is that all you have to do is click the build or run button and then it does everything for you. If you get lazy and always let your editor do all the heavy lifting for you, then you might not even realize what it's doing. So it's good to use vim every now and then so you really understand what's going on. I also use terminals for git. In fact, that's probably what I use it for the most. I also use terminals for system utilities, software updates, SSH, package managers, shell scripts, troubleshooting, making directories, navigating to different directories like File Explorer or Finder, etc.

ConEmu is my favorite terminal (or I guess terminal emulator) for Windows. For most of my sessions, I use Git Bash within it. Git Bash can be used by itself, but it doesn't offer tabs or splitting the screen like a graphical multiplexer (not a fan or screen or tmux, really). I currently have some path variable issues, so I will use the default cmd shell for running python. I could fix it later, but then it becomes a slippery slope of spending lots of time configuring things and not spending as much time developing. Time is a zero-sum game, and the more time you spend on one thing, the less time you have for other things.

On Linux, I like Terminator, because it's similar to ConEmu in the sense that you can split the screen into multiple terminals. I've been using Terminator for many years more than any other terminal program.

For macOS, I will use iTerm2 or sometimes just the default terminal. iTerm2 has some good default settings, though you can easily just change the macOS terminal settings and your bash or zsh settings to make it better. One major thing I dislike about the default terminal program is the default color scheme and text settings -- in terms of text size, color, and lack of syntax highlighting. But something like zsh and oh-my-zsh can fix that. zsh is an interesting shell and supports a lot of advanced features that bash doesn't have. However, if you get used to writing scripts for zsh, compatibility can be an issue. It's like using a dvorak keyboard when most people use qwerty, or insisting on using Esperanto instead of English. Sometimes, ubiquity is more important than quality. The same could be saif for programming languages too, and it's why I use Python and Java instead of some obscure language with very few users (and subsequently few job opportunities).

## Correct vs. concise

Sometimes I say Linux instead of GNU/Linux. I know Linux is just a kernel, not an OS. Sometimes I say terminal instead of terminal emulator. Sometimes I say database instead of database management system. This is not due to ignorance of the differences between these concepts (and many others I didn't list), it's just because it's fewer words/syllables. 

## Another SQL book chapter

I like the way the book implies that you can just learn one concept a day. You don't have to learn everything all at once. I think part of why people think programming is hard is because they ask bad questions like "how do I make an app?" or "how do I program?" as if there's a simple answer that can be summed up in a sentence or two. Instead of thinking you need to learn SQL in a single setting, or hoping there will be a single short video that explains it all (and that you'll somehow absorb just by passively watching), this method of learning a single concept a day and actively following along with your own local database is great. Yesterday, I learned the ORDER BY clause in SQL. Today, I am learning the WHERE clause.

```
WHERE
```

Even before reading this chapter, I had some prior experience with using the WHERE clause, but only for SQL injection. If you use ```WHERE 1=1``` then it will choose everything, because 1 is always equal to 1. One interesting thing about this is that you only use one equal sign for evaluating a boolean value. In other languages, you use ```=``` for assignment and ```==``` as a comparison operator. But here ```=``` is simply comparison.

## Genuinely enjoying programming

Last year when I once did some networking in St. Louis (I'm in Chicagoland again now), I met up with someone I met through a teacher because we had a mutual experience of studying abroad in China. He introduced me to someone who does IT supply chain management and offers mentoring to people. We were talking, and he asked what I like to do for fun. Programming isn't just what I'm studying and what I want to do career-wise, it's also my main hobby. When I said I like to program and do tech stuff, his response was something like "no, but what do you do for FUN?" and he was implying that tech is boring busywork. Maybe he thinks his supply chain work isn't very interesting or something. I just said I like to travel, which is true. But it seemed weird to me that he doubted that someone could genuinely enjoy programming outside of work. 

Is it so wrong to really like what I'm studying? I'm very passionate about technology. I love what I do because it's useful and I can directly apply what I'm learning. I can learn about a prorgamming concept in a book or class, and then immediately go and write software that incorporates that new concept. I am very much an experiential learner, so this is great for me. I like to make software. It's my personal form of self-actualization. Designing my own personal projects makes me feel accomplished. Writing software for other people makes me feel smart and useful. It boosts my confidence. It's not just about money. Lawyers make good money too, but I could never do something like that because it just isn't interesting to me. I am good at computer science stuff because I genuinely like it.

But it seems that, all too often people want to differentiate themselves from other programmers, and cite things like "work-life balance" to imply that there is something wrong with actually liking what you do for a living. I disagree with this attitude. Of course it's good to do other things. But if you really dislike tech so much that you can't understand why someone would do it for a hobby, then maybe it's not the right field for you. It's certainly the right field for me though. You don't have to hate your job in order to "have a life."

Someone might pay me to make them a website or build a computer for them, and after I'm done, I might go write code for one of my personal projects. Is that really so bad? I like other things too, but I still enjoy programming, even if it's not for a job.



