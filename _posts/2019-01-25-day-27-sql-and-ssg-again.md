---
layout: "post"
title: "Day 27: SQL and SSG Again"
date:   2019-01-25 1:22:30 -0600
---

## More of the same

Today I did more Python programming for SSG. I am slowly but surely chipping away at the development of it. And more importantly, I've finished all the concrete details for the design, so it's very clear what I need to do. That is the hard part. Once you've figured out what you're going to program, it's not that hard to go and implement it. Programming is only more difficult when you're not sure how to design something, or just coding without any sense of direction. But I like to plan things out before jumping right in and coding. That's why this phase is a lot easier for me now. Project management, sprints, etc. all really matter.

## SQL learning: LIKE and *

I did another SQL chapter today. There are 22 chapters in this book and today I did the 6th one. 

## Limiting distractions

Lately, I've disabled app notificatons on my phone, turned it to silent, and stopped checking it as often as I used to. I also don't read the news or check social media as much as I used to. This really helps me to get more programming and learning done. Small interruptions here and there can really disrupt your productivity. Some people act weird when you don't respond immediately, but I think it's healthier and better for getting things done if you're not spending so much time on a phone or social media platform. I would rather write code or learn a new computer science topic instead of always being immediately available for everything. 

Push notifications aren't a bad idea in general, but many apps misuse them in order to get you to spend more time within the app. But after a while, if apps give you too many notifications, you just start to tune them out, or even uninstall the app because it's annoying.

## Windows Server progress

I finished memtest86+ on it, and surprisingly, all the old RAM sticks were just fine. So it has 12GB of RAM. It's a weird amount, and it will only be running in single-channel mode, due to being an odd number of DIMMs. But that's okay for a low-usage server like this, which is primarily intended to be used educationally, not really at high load.

After finishing memtest86+, I used a tool called Rufus to make a bootable USB installer for Windows Server Essentials 2019. I use a KVM so I can control multiple computers with just one keyboard, video output, and mouse. 

I installed Windows Server Essentials 2019 on it. I installed it on the SSD and then set up the 2x 500GB drives in a mirror, using Windows' Computer Management program. Everything seems good enough.

I had to research Windows 10 versions. You need at least Windows 10 Pro in order for a workstation to be able to connect to a domain. If I want to use some computers with it, I might have to change their versions/licenses. I use a site called Kinguin to buy Windows keys. 

Even though a KVM is convenient, I might just end up using some sort of remote access softare, because I want to move the server somewhere away from my main computer desk. This means the performance will be slightly worse, but nothing too terrible. And it's always good to get experience with important software, such as RDP or VNC or something.

## Factory design pattern

Today, I learned about another kind of design pattern: factory. The example in the video tutorial I watched said it's a method that returns one of several possible classes that share a common super class. The example they used was creating a new enemy in a game. So basically it's an easy way to instantiate objects. I could easily see how the singleton design pattern could be useful in my SSG program, but I'm actually having a hard time seeing how I could implement a factory into it. But maybe that's just because SSG is a relatively simple program. I could definitely see how it could be used in a game, where you can do some randomization instead of having instantiation be the same every time, and it's useful when you don't know ahead of time what class object you'll need. In many cases, you can use different subclasses of the same superclass, though it doesn't fit for every situation. 

One thing I've noticed about learning design patterns is that I try to think about "how can I implement this in my current project?" and sometimes I can't see a good way to do it where it'd be useful instead of forced/shoehorned unnecessarily. And I think that's perfectly fine -- not everything needs to be overengineered. 

In some cases, a factory might involve instantiating classes that inherit from an abstract superclass. The video I watched on this topic gave the example of an EnemyShipFactory design pattern that instantiates objects from the UFOEnemyShip and RocketEnemyShip subclasses of the EnemyShip abstract superclass. 

The next design pattern I will learn is abstract factory, but that can wait until another day.

## Other Python and programming topics

I learned about inheritance and polymorphism in Python. Those aren't new topics to me, but I hadn't done them in Python yet. I also learned about querying JSON APIs in Python. Maybe, at some point, I will write a test program to query one of my Wordpress sites' built-in APIs. Interacting with APIs is very important, because you won't be using everything yourself, and libraries are only for code. APIs are useful not only for features and code, but a lot of APIs are about data. API interaction is more important these days, as more and more programmers are network-connected instead of being isolated and offline-only.

One example of how you could combine APIs with Python is to use the OpenWeatherMap API to get weather data, and then use the Tweepy and the Twitter API in order to make a Twitter bot to tweet out the weather from the weather API. 

Another Python topic I looked up today is recursion, using the Fibonacci sequence as an example problem to solve with it.

I also learned about lambda expressions/anonymous functions in Python. I used them a lot in Java, but I haven't really used them in Python yet. 

## Random stuff

Other stuff I researched today:

- Resume editing
- Mixins
- Sass CSS preprocessor
- Router Entware/Optware -- basically apps/packages you can install on DD-WRT or OpenWRT routers
- Busybox
- SSH honeypots
- Manifest files
- ```xargs```
    - A cool way to pipe output from one command line program as a command line argument for another program.
- Imposter syndrome in tech
- Python xrange function
- Context switching
- The differences between ```input()``` and ```raw_input()``` in Python

## Django 

Today, I downloaded a Bitnami Django stack and set it up on my ESXi hypervisor.

The process of downloading a premade Django VM and then installing it in ESXi only takes a couple of minutes. It's much faster than setting everything up manually. Hypervisors are great in the sense that they allow you to set up many virtual servers quickly and easily without having to always buy new hardware. It's true that I currently have two bare metal servers -- one for FreeNAS, and the other for Windows Server. But most of my servers are virtual machines on my VM server. I feel very comfortable with my virtualization skills, though I think I need to get more into containers instead of just VMs.

## Networking equipment

Because I currently don't have enough network ports for all my servers, I'm ordering a Cisco Catalyst 2950 and some adapter cables so that I can connect my computer to the console port for initially setting up the startup-config in Cisco IOS. From there, I will be able to remotely administrate it. I learned Cisco IOS and routing/switching stuff at College of DuPage, but I haven't used it in a while. This will be useful, because I need a switch, and it'll also be an educational project, kind of like my Windows Server/Active Directory project that's in the works. 

Unlike most consumer-grade switches, a Catalyst 2950 is what's called a managed switch, meaning you can log into it and change a lot of settings. The operating system it's running is called Cisco IOS, which stands for Internetworking Operating System. I have used IOS a lot in the past, whether it was on Cisco Packet Tracer, GNS3, or on lab equipment in a classroom. But I am admittedly a little rusty. 

## Upgrading Windows to Windows 10 Pro

To kind of test the waters, I am only getting one Windows 10 Pro key to upgrade one workstation to see how it goes, before going ahead and upgrading all Windows 10 workstations here to the Pro edition.

## C programming

I read the next chapter of *Teach Yourself C in One Hour a Day*. 

## New git repos

I made new git repos for my notes repositories for learning SQL and C. These are just like my gitUdemyLearning and misc_python_1 repos: just educational notes and testing rather than being fully-fledged apps. 

## Computer Organization and Design book

Today, I read the first chapter of the book *Computer Organization and Design*.

