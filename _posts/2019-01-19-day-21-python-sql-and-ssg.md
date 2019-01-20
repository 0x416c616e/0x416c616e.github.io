---
layout: "post"
title: "Day 21: Python, SQL, and SSG"
date:   2019-01-19 11:33:00 -0600
---

## Today's highlights

More Python learning, miscellaneous programming learning, learned about the SQL WHERE clause, updated my website and daily log, made a branch for the SSG test for reading from a JSON file and replacing certain placeholders in a template file (putting content from a content file into a layout file for the site generation). 

## Python

Today I reviewed a lot of Python concepts. I also made assumptions about Python based on my previous programming language knowledge. It turns out I was wrong in a couple of ways. 

You need to use the ```global``` keyword in Python to specify that you're referencing a global variable rather than a local one. No wonder my IDE gave me messages about variable shadowing. I was practically pulling out my hair the other day because of scope issues that I didn't understand. The solution is actually really simple. I never had to use a ```global``` keyword in Java, but Python is not Java. You might think OOP languages are all the same, but there are enough differences for it to be confusing without reviewing a lot of seemingly basic concepts. Some other simple differences include how Java's indentation is optional, whereas indentation is forced in Python. Not only that, but Java supports switch statements, constructor overloading, etc. Python is also dynamically typed, whereas Java is statically typed. 

As I touched on yesterday, I wasted time programming my own command line argument parser in my Static Site Generator app, when it turns out that Python has something cool called argparse, which makes it very easy to parse arguments with minimal effort. I also looked up some other Python things today, like logging, unit testing, and ftplib. There are so many useful modules that come with Python. And speaking of modules, it's good to be able to make your own modules. I don't want my SSG program to have everything in a single .py file, so I will be breaking up the modules for a few things.

Here are my initial plans:

generator.py gets user input and displays text menus and confirm dialogs and all that jazz. There are some submenus listed in the main menu (once you have a project open):

- Settings menu
- Article menu
- Project menu

Each of these have their own submenus and subroutines. I think I should break up, or modularize, the program, to make it easier to read, rather than having everything in the main class and generator.py.

It's true that sometimes you don't need user-defined classes, and Java seems to place too much emphasis on classes, objects, constructors, getters and setters, and that kind of thing. Sometimes a program can be simple, or at least doesn't need so much unnecessary class and subclass hierarchy. But separation of concerns isn't just for MVC, it's even useful for functions.

I think I might even use a separate module for a sub-component even within the above submenus, which is the regeneration ability. When you want to refresh stuff, the program will use the regeneration module (that I have yet to write) to combine the JSON article info (in many different JSON files and directories because it's not all the same and should be divided accordingly based on what it is), along with some other text file information, and use that with some logic to determine pagination algorithm stuff and then finally put everything into the right copied template files which will then yield the final static HTML pages, which contain the content and the layout.

I'm not 100% competent with my understanding of MVC, but I get the general idea, and my subfolders aren't model, view, and controller, at least not right now, but it's the same basic idea. Something contains your content, something else has your templating, and something else contains the logic to put the content into the templates to create/deliver the finished product.

Today I will be trying out making a branch. It will be a testing/feature branch where I will be making a test in my testing subdirectory to test out opening a JSON file and then opening a template file and finding and replacing placeholders with the values from certain keys in the JSON. This is not the only JSON stuff I need to do for this program, but you have to try things one at a time rather than trying to implement a ton of complicated things all at once. I am of the mindset that you will only be able to successfully make a complex program by subdividing it into smaller pieces and making sure each small piece does what you want it to. If the JSON test is successful, I will then add a JSON schema to it and make sure it validates properly, or maybe even make a separate subprogram that only validates dummy JSON from a dummy schema just for testing it out, and then I will add that to the test program that only does the JSON read and find-and-replace stuff in the template. 

There are multiple steps here before I ever integrate that into the "real" program. This stuff will probably be in the site generation module. The article creation module will be easier because all it does is read input from the user and then write it do a JSON file on disk. It also has to do some regular expression for validating input, and maybe have a weird workaround to accept multi-line text input (```input()``` by default will stop accepting input from the user when they hit enter, which makes accepting linebreaks more difficult), etc. There is a lot of stuff to do for this project, and a lot of it is planning and testing, not just writing the program from start to finish.

I have yet to do any formal unit testing from the Python unittest module, but I have always performed my own manual testing. I write extra print statements, just to let me know what's happening, even if I don't get any errors. I eventually comment them out or delete them. In the future, I should probably use the Python logger module instead of these print statements, where the data goes away when you close your terminal. Logging is useful so you can analyze what went wrong or what went right, or how something you changed affected how the program runs or performs. But anyway, in addition to print statements to show the status of things, or at least show where the program execution is when you do something, I also write subprograms that are intended to be mini/simple versions of a feature I want to implement into the main program. Sometimes I even write 100% useless programs that aren't even a subprogram or mockup of a bigger feature I really want to use. 

Sometimes I will make useless programs for the sake of learning about that feature. I have looked up things called katas, which are more about algorithms, but that's not what I'm talking about here (although katas and other programming exercises/challenges are good too). But these ones are for demonstrating a feature of a language so I will know how to use it in the future if I need it. And sometimes you really need to learn about features you can't immediately figure out a use for, because when you only have partial knowledge about a programming language, you might be making poor design choices and using antipatterns because there are useful things you should be using that you simply don't know about. Case in point for my recent Python learning: the argparse module. I didn't even know it existed, let alone that it would make it so much easier to write the same code I agonized over for a few hours. I also didn't know about the global keyword, another thing that would have saved me some headaches. So making seemingly useless small programs that demonstrate a programming feature aren't always a waste of time. They can help you increase your repetoire of tools and ideas for designing software or solving problems in the future.

My future programs will definitely use argparse, logger, unittest, and more. But then again, sometimes overengineering things is a bad thing. That's a common problem in Java. I'm not just referring to boilerplate, but the whole enterprise attitude of everything needing to be extensible and whatnot. Sometimes you can make a program in a very simple way and it's still okay. But what I'm saying here is that I'll be able to use argparse or logger or unittest if I actually need to, now that I know they exist and I have a basic understanding of how to use them.

## Standard libraries vs. third party

I am of the mindset that standard libraries are almost always better than third party ones. If you can do something in the language with no addditional libraries or frameworks, you should. It can force you to think about something more. When you use a library, you might choose it because it contains a class or function that does exactly what you want it to, and you can import it and use it without ever having to think too hard about how it achieves the desired effects. It can be convenient, but it also gets you into sloppy habits for programming. Sometimes, you really need an external library. But don't use them if you don't really have to, because there might just be something in the standard library that does something similar anyway, even if it's not 100% of what you're looking for. But odds are that you can tweak it in some way to suit your needs. 

I was originally looking up the Qt GUI framework for Python when Python actually has built-in GUI stuff called tkinter. That would have been a mistake to start with something like that right off the bat.

### Shebangs

I first learned about shebangs (```#!```) in community college when I took a course about Linux and Unix. Among other things, the class taught command line utilities, vim, pipes, man pages, SSH, and shell scripting. The shebang for a shell script might be something like ```#!/bin/bash```. Of course, you can also specify environment variables rather than absolute paths, just in case there are some non-standard locations for installations. Additionally, not all systems will have the same default shell, so ```#!/bin/sh``` isn't a very good idea. You can always do ```echo $SHELL``` to see your current shell, but now I'm getting slightly off-topic.

Shebangs aren't just for shell scripts. They're sometimes (but not always) used in python too. A shebang, like ```#!/usr/bin/env python3```, isn't actually necessary to run a Python script in an editor, or by specifically running it with ```python3 whatever.py```. But if you mark a .py file as executable and try to execute it like ```./whatever.py```, if there is no shebang, your computer might not know how to execute it. It depends on a number of things, like your path variable and operating system. For example, on my Windows machine, ```python``` is used to run python3, but on my mac, I have to use ```python3```. And PyCharm doesn't require you to use a shebang, but if you only run your programs in an IDE, and especially with just a default build configuration, then you can miss out on how a lot of people will be running the program (most notably a terminal window).

## My favorite editors and terminals

I like command line stuff a whole lot. I feel very comfortable doing text-based commands. I think it's inexcusable for someone to be a programmer and not know their way around a shell. Some things are simply more efficient with command line as opposed to a GUI. On Windows, I know use ConEmu. Below is what my current workflow looks like. Some peole say cmder is better than ConEmu, but it was buggy for me, and their site didn't even have an SSL certificate, which isn't reassuring. So I will stick with ConEmu.

Click to view full size screenshot (1080p):

<a href="/assets/conemu.png"><img src="/assets/conemu_thumbnail.png"></a>

I prefer IDEs and graphical editors, such as VS Code, PyCharm, and IntelliJ. I use VS Code for web development and I've even used it for C/C++ even though CLion is arguably a better option for that. PyCharm is for Python, and IntelliJ IDEA is for Java. 

I also use vim for some basic stuff, like editing markdown files, or doing quick fixes, but I honestly don't prefer it for more serious work. Of course, it's good to use it occasionally, because then you are forced to learn about compiling, linking, loading, etc. One issue with modern IDEs is that all you have to do is click the build or run button and then it does everything for you. If you get lazy and always let your editor do all the heavy lifting for you, then you might not even realize what it's doing. So it's good to use vim every now and then so you really understand what's going on. I also use terminals for git. In fact, that's probably what I use it for the most. I also use terminals for system utilities, software updates, SSH, package managers, shell scripts, troubleshooting, making directories, navigating to different directories like File Explorer or Finder, etc.

ConEmu is my favorite terminal (or I guess terminal emulator) for Windows. For most of my sessions, I use Git Bash within it. Git Bash can be used by itself, but it doesn't offer tabs or splitting the screen like a graphical multiplexer (not a fan or screen or tmux, really). I currently have some path variable issues, so I will use the default cmd shell for running python. I could fix it later, but then it becomes a slippery slope of spending lots of time configuring things and not spending as much time developing. Time is a zero-sum game, and the more time you spend on one thing, the less time you have for other things.

On Linux, I like Terminator, because it's similar to ConEmu in the sense that you can split the screen into multiple terminals. I've been using Terminator for many years more than any other terminal program.

For macOS, I will use iTerm2 or sometimes just the default terminal. iTerm2 has some good default settings, though you can easily just change the macOS terminal settings and your bash or zsh settings to make it better. One major thing I dislike about the default terminal program is the default color scheme and text settings -- in terms of text size, color, and lack of syntax highlighting. But something like zsh and oh-my-zsh can fix that. zsh is an interesting shell and supports a lot of advanced features that bash doesn't have. However, if you get used to writing scripts for zsh, compatibility can be an issue. It's like using a dvorak keyboard when most people use qwerty, or insisting on using Esperanto instead of English. Sometimes, ubiquity is more important than quality. The same could be said for programming languages too, and it's why I use Python and Java instead of some obscure language with very few users (and subsequently few job opportunities).

## Correct vs. concise

Sometimes I say Linux instead of GNU/Linux. I know Linux is just a kernel, not an OS. Sometimes I say terminal instead of terminal emulator. Sometimes I say database instead of database management system. I know markup languages aren't programming languages, but I might still lump them into a "languages" or skills section on my site or resume. This is not due to ignorance of the differences between these concepts (and many others I didn't list), it's just because it's fewer words/syllables. 

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

## Other random learning

Learned more about Docker, AWS EC2, JavaScript (just review because I haven't done JS stuff in a while), PHP, Kotlin replacing Java for Android development, code smells, refactoring, Python pass-by-object-reference, PyPy, clean code, python unit testing, code katas, etc. I am doing a lot of in-depth learning for Python, git, SQL, and JSON. But I also do a lot of cursory research, where I only find out really basic stuff about a wide range of topics. Some of them are topics I learn a whole lot more about later. Some are topics I will only know on a surface level. But I try to keep up with many different programming-related topics. I try to avoid technological tunnel vision. 