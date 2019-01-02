---
layout: "post"
title: "Day 6: Python and Server Plans"
date:   2019-1-1 21:01:22 -0600
---

## Ordering parts for a new server

Because my current project involves generating static websites, I need a server to test this out on. I could use shared hosting like what I use for my current websites, but I've never liked the idea of making changes directly to a production environment, so I'm getting parts to build a server so I can test things out locally before making live changes. This is better for stability and security.

I'm not just building any kind of server. It's specifically for ESXi, so it will be acting as a hypervisor that can run multiple virtual machines for various things. I've used VPSes and shell accounts on servers before, and I've used Virtualbox VMs within a host OS before, but I've never had a type 0 hypervisor before. This will be useful experience.

The benefit of using a hypervisor for multiple VMs is that I can have only one physical server, but then use VMs to make many logical servers, with different OSes and containers and whatnot. I plan on eventually branching out and doing more than LAMP and MEAN, but maybe also learning Kubernetes/Docker, and other modern things like that. There's more to servers than web hosting. Containers and container orchestration are very interesting topics. 

The installer for ESXi is an ISO, a relic from the past when people used optical media to install OSes. I will have to use a tool such as Rufus in order to make a bootable flash drive instead of burning an install CD/DVD, because this mini-ITX build doesn't have room for an optical drive. My desktop has a DVD drive, but I never use it. It's just taking up space. 

I ordered parts online and tomorrow I'll do an in-store pickup and then build the server and set things up.

## Specs

The specs for my soon-to-be hypervisor are as follows:

- **CPU:** Intel i3 8100 quad-core CPU (I've built other desktops with this and it's just fine for the workloads I'll use on it). For most desktops, I prefer to get overclockable versions of processors and then get a beefier heatsink. However, because this will be a small build (mini ITX), I am going to use a non-K processor and a stock cooler because of space and power limitations. But that's fine for a hypervisor.
- **RAM:** 16GB (2x8GB) DDR4 2400MHz RAM. Should be enough for a decent number of VMs. And if I really need more VMs, I can always run some in VMware or Virtualbox on my desktop, which has 32GB of DDR3 RAM.
- **Motherboard:** ASRock H370M-ITX. It's an 1151 board that will work with this RAM and CPU. Someone left a negative review of the board saying it had trouble with 32GB of RAM, even though it's listed as supporting up to 32GB. However, I am only using 16GB, so I think it should be fine.
- **GPU:** just onboard graphics because it's a server and thus doesn't need graphics performance at all.
- **SSD:** Intel 545s 512GB. This will be my first time using an NVMe M.2 SSD as opposed to SATA III. It's very fast and just lies flat on the motherboard, so it doesn't take up much space and won't require extra cable management. It's a good compromise between speed and storage. Some SSDs are slower and cheaper per GB, and some SSDs are much faster but also more expensive per GB. This is somewhere in between, but it will be good enough for my VMs. Boot time isn't hugely important for something that will be on 24/7, but responsiveness for VMs is useful. In the future, I might even get more SATA SSDs because VMs can sometimes be disk-intensive. I've heard that SSDs wear out faster than HDDs, but this should be good enough at least for starting out.
- **Case and power supply:** Inwin Chopin mini-ITX case with included 150W PSU. I'm used to computers requiring much higher wattage, so it's impressive that this build will actually run on a lower-end power supply like this.I researched other people's builds with this case and PSU and other people got even more power-hungry CPUs to work on it.
- **Network interface card:** it's true that the motherboard I picked out actually does have built-in networking: in fact, it has not just one, but *two* gigabit ethernet ports. However, I will be installing ESXi on this, and after reading a lot about it, NIC compatibility seems like it can be an issue, so I got a cheap NIC that is guaranteed to work with ESXi. Some people with the onboard NIC that comes with this mobo complained about it not working. This might not be the case anymore, and there might be a weird workaround to get it to work, but I'd rather spend a little more and get something that I know for a fact will work out of the box.

## Not what it used to be

This is all ordered from MicroCenter, one of the few remaining computer parts stores. Stores like MicroCenter and Fry's Electronics seem to be dying out in favor of online warehouses like Newegg and Amazon. Also, mainstream tech stores like Best Buy are much less about computer parts and more about phones and tablets these days.

Low and mid-range computers seem to be dying out in favor of tablets and smartphones. Computers used to be a general-purpose device for communication, web browsing, getting work done, and so on. But now, most people are fine with Android and iOS devices instead. Desktop computers seem to be more niche, for creative professionals who do CAD/drawing/multimedia editing, people who play games, and programmers. Mobile devices have the benefit of better power efficiency and more user-friendly software, but the productivity software, like IDEs/compilers/etc, simply isn't there. I've tried using ChromeOS and Android for software development, but they were miserable experiences, so I will stick with macOS/Windows 10/Linux for serious work.

## Python, git, and user-friendliness

I am continuing to lean more about Python and git, using low-cost courses on Udemy. It will be a while before I really learn enough to make my static site generator program, but considering that I already have experience with Java, JavaFX, and web development, it's not like I'm a complete beginner here. 

This site is currently made with Jekyll, but in the future I might actually convert it to my own static site generator tool. Installing Jekyll is a surprisingly complicated experience, and doesn't that defeat the whole purpose? Jekyll is supposed to be an easier alternative than writing your own static site. But setting up MinGW and the path variable and a lot of other programming dependencies on Windows seems to involve more technical skills than the target audience for a "push button, receive website" program.

My static site generator will include all dependencies and be 100% graphical. Jekyll is command line-based and harder to use for novices. I can personally use it just fine, but I'm a CS student with years of experience in developing software and using Unix/Linux shells. Making software easier to use is hugely important, and that's why I'm going to make my project easier than Jekyll.

The goal of my current project is to learn Python and Qt through experience, but also to make a useful tool that can help people make websites very easily without any coding knowledge at all.

That's all for today. Check back tomorrow for another day of coding!