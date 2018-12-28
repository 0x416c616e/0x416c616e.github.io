---
layout: "post"
title: "The First of 100 Days"
date:   2018-12-27 23:00:06 -0600
---

## Introduction

Hi there! I'm Alan and this is my new website for the [#100DaysOfCode](https://www.100daysofcode.com/) challenge. I'm not new to software development (I'm studying CS in college), but I'd like to spend the next 100 days honing my skills and making sure I program at least one hour per day, but hopefully a whole lot more than that. This isn't my only website though. Check out [Saint Louis Software](https://saintlouissoftware.com), as that's my main website, at least for now.

Every single day, I will post a brief summary of what I've been programming and what I learned. Maybe other people can learn from my experiences. If not, it at least serves as a way to motivate me to program more regularly.

## Jekyll

![Jekyll logo](/assets/jekyll.png)

I've used other tech for developing sites in the past, like doing a full MEAN stack project for a web development class, and CMSes like Wordpress for simple sites without much effort, and I've done some LAMP-based sites with an emphasis on a responsive frontend, using things like jQuery, Bootstrap, HTML5, and CSS3, especially for width-related media queries. But this time around, I wanted this #100DaysOfCode project's website to be rather simple, so instead of doing everything frmo scratch, or simply installing a CMS I've already used, I opted for Jekyll. Jekyll is an interesting static page generator project, not suitable for all types of websites due to its static nature. But it's interesting in the sense that it reduces attack surface (at least compared to traditional content management systems) because the software runs client-side and merely generates static pages for you to commit to a git repo, which can then correspond to a website (if you're using something like Github Pages, which I am in this case). 

Jekyll posts are made with Markdown, which is also used for readmes on GitHub, among other things. It's really simple, though Jekyll's config files are written in YAML. There are so many different markup languages that it's hard to keep track of it all, but it's good to learn new things.

Jekyll is Ruby-based, and I'm honestly not a big fan of Ruby. If I really had to choose a scripting language, I'd go with Python instead. I also noticed that setting up Jekyll's numerous dependencies is actually a really annoying process on Windows, though macOS comes with a lot of programming-related things already installed, which simplifies the process significantly. MinGW is very unintuitive. But even so, I've set up Jekyll on both my Windows desktop and my MacBook Air. It's good to get used to different OSes, IDEs, etc. instead of getting into a comfort zone where you're only good with one particular set of tools. But now I'm going on a tangent.

So far, I just recently learned about Jekyll, so I could set this site up. My current programming project that I'm working on is EZcrypt, which is a Java-based file encryption and decryption tool. 

## EZcrypt

![EZcrypt screenshot (work in progress)](/assets/ezcrypt.png)

Won't be winning any awards for UI design, but that's not the point. I might make it look better in the future too. But for right now, I am just concentrating on making it work, as opposed to trying to make it pretty.

Encrypting and decrypting are important, aren't they? For everything from full disk encryption to HTTPS, encryption is important for both *data in motion* and *data at rest*. But sometimes encryption can be complicated and not exactly beginner-friendly. That's why I'm making EZcrypt, which aims to make file encryption and decryption easier and more accessible for the average person. I'm making it with Java, JavaFX, the Apache Commons IO library, and IntelliJ. 

## Dependencies and build environments

![macOS Mojave](/assets/macosmojave.png)

I recently did a fresh installation of macOS Mojave on my MacBook Air, specifically opting to not carry over any settings cruft from my previous installation of macOS Sierra (I skipped High Sierra due to people on Twitter reporting a lot of bugs with it). In doing so, I had to reset and reconfigure a lot of my development environments, because I decided not to go with a dotfiles approach to transferring everything over because I had some issues with path variables and homebrew spewing out error messages and whatnot. 

That's not to say that dotfile repos are a bad approach, and I will be utilizing them in the future. But even so, a clean OS installation was good for now and fixed some issues I had with path and package management stuff, which would have been more complicated to troubleshoot. However, I noticed that I had to really re-learn how to set up my build environment again. Knowing how to program in Java doesn't necessarily mean you're an expert at clicking through menus in an IDE to set up your proper toolchain.

![Project SDK](/assets/projectsdk.png)

One thing I learned is that JDK 11 no longer includes JavaFX, even though it was supported in previous versions. You have to install it separately now, because I guess Oracle only wants the JDK to be for core stuff and any optional modules will no longer be a part of it. So instead of setting up some separate complicated dependency, I just decided to recreate the older stuff I had before, using the old JDK 8 and changing the IntelliJ project structure to not use Java 11, even though I have it installed. 

## Containers are cool

![Docker logo](/assets/docker.png)

I guess this issue of "works on my machine" and having trouble finding the *exact* versions of software dependencies to make something run are why containerization is getting popular these days. I eventually want to get more into Docker and Kubernetes for just this reason. If all the dependencies are contained with a container, rather than leaving the installation as a frustrating exercise for the person setting everything up, then I think the process of getting something up and running will be much easier and less time-consuming.

## Version Control

![GitHub logo](/assets/github.png)

Most of my projects are publically available on GitHub. I mentioned EZcrypt, which is on GitHub and released under the GNU GPLv3 license. I will make an effort to create .JAR files for my Java projects so you can run them with ease. I encourage you to check out my projects. Not only do I have a lot of current projects there, but I have a lot of plans for future things I'll be making in the near future. GitHub profiles are a great online portfolio which can help you stand out among other candidates applying for the same development jobs. The 'contributions' section is a good way to gauge how active someone is with programming. Getting a computer science degree by itself isn't enough, you need to also prove to people that you know how to program outside of a classroom environment. And that's precisely what I'm doing here with this 100-day coding challenge.

![GitHub contributions](/assets/github_contributions.png)

But that's all for now. Check back for future blog posts about software development!