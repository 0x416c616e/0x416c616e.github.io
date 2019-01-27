---
layout: "post"
title: "Day 28: Starting the article module"
date:   2019-01-26 1:05:38 -0600
---

## Static site generator app progress

I broke my big static site generator app into multiple modules. They all do separate features. An app is a big project with many different facets, and it can seem overwhelming if you can't break it down into smaller problems to solve.

Today I did more work on my static site generator program. I have finished the initial setup module and now I'm working on the article module. This module, when completed, will the the user perform actions related to articles. I guess you could also call them posts instead of articles.

I made a new branch in the git repo called article-menu. Lately, I have been getting better at branching and merging.

The kind of website that SSG generates is a blog, basically. You can use it for news about a company, hence articles, or it can be for personal posts, which you could call posts or blog entries. In any case, you want the ability to do a few things here:

- Create a new article
- Read an existing article
- Update/edit an existing article
- Delete an existing article

In addition, I also have plans for another function that will let you see the names of all the articles you have in your project.

So far, I finished the function for updating an existing article. Depending on your operating system, it will open a different text editor. On Windows, it will open the article JSON file in notepad. Notepad isn't great, but it's guaranteed to be on all computers with Windows. On macOS, it will open the file in TextEdit, which also isn't great, but again, it's guaranteed to come with macOS. And on Linux, it will open gedit, which is a simple editor that comes with many distros. Some distros might not have gedit, and instead it could make more sense to use something like vi or vim, or maybe nano, but because this program is supposed to be user-friendly, I decided to go with gedit instead, which is better for less tech-savvy people. After all, if someone knows about vim and all its keyboard commands, they might not even need a static site generator in the first place. SSG is aimed at less technical people (or perhaps tech-savvy people who just want to put less effort into making a website).

## The problem with fast tutorials

It has taken me weeks to learn a lot of new git features. There are plenty of video tutorials, online articles, etc. that will tell you all of the git commands all in one go. Maybe you can find a video that teaches all of this in half an hour to an hour. But the problem is that you won't really comprehend it. It takes time and experience to truly understand it. If you try really condensed learning, you might find that your retention falls flat.

Slow and steady is important. That's why I'm trying to do at least a little bit of programming each and every day. I am learning Python, JSON, SQL, advanced git stuff, etc. But not all in a single day.

One thing I've learned about learning is that you need time to process what you've learned. You can't learn 500 things in one day, even if you are capable of reading that much material. But repetition helps reinforce learning. The more you practice something, or read over it again, the better you will understand it. If all you want is to put stuff into your short-term memory, such as doing a "brain dump" for an exam, then you can just power through material all in one go. But you'll forget it all pretty quickly. The way to get things into your long-term memory is to revisit them again and again. I use git for every single one of my projects, and now I do branching and merging, which is why I'm getting good with it. And because I'm actually writing software in Python, I won't forget things that I wouldn't remember if I simply learned Python and did nothing with the knowledge.

I think part of the reason why some people find computer science to be difficult is that they will only listen to a lecture or do homework, but won't do anything else in order to really learn it well.

## Random learning

- git fetch
- Python xrange function
- Context switching
- The differences between ```input()``` and ```raw_input()``` in Python
- Pair programming
- Memoization (not a typo)
- Random numbers in Python -- ```randint(min, max)``` seems to be the most useful
- More in-depth Python file IO -- appending, reading, CSV parsing, etc.
- Monte Carlo simulations
- Number theory

## Networking equipment

Because I currently don't have enough network ports for all my servers, I'm ordering a Cisco Catalyst 2950 and some adapter cables so that I can connect my computer to the console port for initially setting up the startup-config in Cisco IOS. From there, I will be able to remotely administrate it. I learned Cisco IOS and routing/switching stuff at College of DuPage, but I haven't used it in a while. This will be useful, because I need a switch, and it'll also be an educational project, kind of like my Windows Server/Active Directory project that's in the works. 

Unlike most consumer-grade switches, a Catalyst 2950 is what's called a managed switch, meaning you can log into it and change a lot of settings. The operating system it's running is called Cisco IOS, which stands for Internetworking Operating System. I have used IOS a lot in the past, whether it was on Cisco Packet Tracer, GNS3, or on lab equipment in a classroom. But I am admittedly a little rusty. 

## Upgrading Windows to Windows 10 Pro

To kind of test the waters, I am only getting one Windows 10 Pro key to upgrade one workstation to see how it goes, before going ahead and upgrading all Windows 10 workstations here to the Pro edition.

## Pomodoro technique for studying

I learned (well, got reminded of) a learning technique called pomodoro. It involves studying/coding/whatever for 25 minutes, then taking a 5 minute break. I use the Toggle browser extension in order to keep track of this. It has a pomodoro mode. 

When you're learning difficult things like programming, it can take a toll on your mind. After a while, you start to burn out and your learning capability decreases. It's dry and difficult to get through, so a short break can really help. A small break will make you feel better, which will increase your productivity during the next 25 minute study phase.

Manually keeping track of the time would be annoying, but the Chrome extension makes it easy.

