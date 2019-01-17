---
layout: "post"
title: "Day 19: Documentation and Software Engineering"
date:   2019-01-17 9:13:12 -0600
---

## Don't just write code, write documentation too!

What's immediately obvious to you, as the developer, will not be immediately obvious to the people tryinh to use it. I recently wrote a TON of documentation explainnig what my static site generator is, what it can (or I guess *will*) do, how you can use it, etc.

I painstakingly explained each of the directories and files, and the general methodology for using it and what it does when you use it. That's also in addition to the more beginner-friendly plain English explanations that basically just say that you can use it to make websites, don't have to code in order to use it, and you need to have Python installed on your computer in order for it to run.

I will eventually have to separate out the more in-depth technical documentation from the friendlier easy stuff, but for now, I put it all in the readme.md file. Check out the SSG repo [here](https://github.com/0x416c616e/staticsitegenerator).

If your program has bad documentation and is difficult to install or use, people will just use a similar app that is easier. People take the path of least resistance. Everyone is busy. Everyone has things to do. Nobody wants to spend unnecessary time learning a complicated thing when they can just use something simpler instead. 

## Software engineering

Writing documentation really forced me to flesh out my kind of vague ideas about the app. I made a sample project folder called example, within the projects subdirectory, and you can see that 


## Adding dependency and usage information in READMEs

Today, I added basic info and instructions for using my software. For example, I listed the specific versions of Java to use my old Java programs with, and mentioned how to run them using ```java -jar filename.jar```.