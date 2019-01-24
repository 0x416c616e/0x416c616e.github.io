---
layout: "post"
title: "Day 26: Initial Setup Module"
date:   2019-01-22 11:22:30 -0600
---

## Initial setup module

For my static site generator project, I finished the ability to either open an existing project or create a new one. Easier said than done... it took me a while, especially for input/regex/project validation (and copying over files from the template folder for a newly-created project)! I have also finalized the project files and JSON structures, for the most part, though I am putting off JSON validation for the time being and I will just assume that projects are valid and haven't been corrupted (this can be a bad assumption later down the road, but for my 'minimum viable product' of the SSG program, I will put JSON schema validation off until later). 

When you first make a project, it has no articles aside from the example one. It has no settings or about page info, which is where the initial setup module comes into play. And then, after that, I will need to make the regeneration module that will allow you to combine templates with content to create the final stuff. But that will come much later.

After I finish the initial setup module (which I've only just started making and haven't completely finished yet), then I can 

## Stubs/prototypes instead of finishing everything all at once

When I designed the initial setup module, first I had to reference the way I structured my JSON in the settings.json and about.json files, which are what will be configured with the initial setup. I also have a text file with a boolean (well, string that needs to be converted to a boolean) called finished_initial_setup.txt, which is an easy way to see if a project has finished the setup or not. Because a user could hit ctrl+c or close the terminal window, they might not have finished it, even if you have the program run the initial setup when they first use it. Because they could quit at any time, that means the only way to check if you can proceed past the initial setup functions is if the boolean in the fniished_initial_setup.txt is True. That's because I've designed it so that there is a function in the module that will overwrite the contents of the file and change it from False to True. There is another function that checks before proceeding.

![](/assets/python_prototype_functions.PNG)

With all these functions, I had the ideas for them -- name, purpose, arguments, and return values -- and I came up with the design for this module faster than I can implement it. So how did I keep track of it all? Well, I certainly didn't just rush in and write it from start to finish. Instead, I came up with a list of requirements and then used the ```pass``` keyword to make empty functions that do nothing. Later, I will finish them. But for the time being, I can at least remember what I'm supposed to make here. This reminds me of C++ function prototyping. It's kind of similar, except that, rather than writing function definitions separately, I will just replace the ```pass``` keyword with the real contents. 

I also used to make UML diagrams in my old CS classes, but that seemed like too much effort and it was too indirect, when instead I can just write stub/prototype functions that don't do anything, but still make it clear what I'm trying to accomplish in the future.

The issue with software development is that you can come up with ideas for things to make faster than you can make them. Whether it's an idea for an entire app, an idea for a class, a module, or even just a function, it takes only a few seconds to come up with ideas, but making it can take a really long time, depending on what it is. 

Some people pretend that they can remember everything. I know I can't, so that's why I like to do things like this in order to write down my thoughts and designs before I forget about them. That's also why self-documenting code, brief comments, and documentation pages, such as wikis or readmes, can be very useful. But the problem with verbose documentation is that a small change to code means you have to read through long documentation to figure out which parts need to be updated. 

## More refurbished server progress

I recently got a computer for free. I upgraded it using a combination of free stuff from salvaged dead computers, and a new SSD that I got for it. In total, it has a dual-core processor, heatsink from a quad-core processor, 12GB of DDR3 RAM, a 120GB SSD, and 2x 500GB drives that I plan on using in RAID 1 for redundancy and better read speeds. I am going to install Windows Server Essentials on it so that it can act as a domain controller.

But first things first: for trust/security reasons, I had to wipe the drives with DBAN, and I also reflashed the BIOS. I am concerned about things like BIOS rootkits and MBR rootkits. When you wipe everything out, for the the BIOS and the hard drives, then there's nothing left than can persist. It took me a while to do all this stuff, and also adding the new SSD and RAM and doing some cleaning and cable management too, since it was dirty and had a lot of cable ties holding everything together. 

But once the final DBAN pass finishes, I will be running memtest86+ to test the RAM and make sure there are no errors. Even though it's for a server, I don't have ECC RAM. Honestly, most of the time, ECC RAM is unnecessary, especially for home lab stuff like this, as opposed to a production environment in a large-scale enterprise. But I still just want to make sure everything is okay. Then I will make a bootable USB drive for WSE and set it up with some sort of remote access so I can use it on my main computer. I have a KVM, but I think it's good to get more experience with ssh (which I already use), RDP, VNC, etc.

This probably sounds more like something a sysadmin would do, right? Or at least someone who wants to become one. Ticketing systems, servers, hypervisors, domain controllers... that doesn't sound like things a software developer would do, right? Well, maybe. But I am not strictly into software development. I have IT skills and an IT education as well. I like to consider myself more well-rounded with tech compared to developers who never venture outside of an IDE or terminal. It's good to know the other kinds of tech that will be in an enterprise environment. 

In high school, I started learning about computers on my own, even though I never had any classes about tech and none of my friends or family were into computers either. But even so, I built computers, repaired them, installed Linux with a text-based installer, etc. I also did things like water cooling and overclocking. Then, in community college, I studied IT and learned about computer repair, hardware, networking (TCP/IP and OSI stuff), Linux, shell scripting, and a lot of stuff about Cisco IOS. Then I studied CS instead because I don't want to be strictly IT-only. IT is more about managing/fixing/monitoring things. I like software development because it allows you to create things instead of only maintaining things. But I also like IT stuff. I don't want to be the kind of developer who is 100% software-focused and clueless about tech infrastructure and hardware. But as good as Cisco IOS and Linux are, you need to learn about Windows Server stuff like AD/LDAP as well, because even if you prefer Linux, AD has its place in the enterprise. 

I am going to convert a lot of the computers on the LAN here to Windows 10 Enterprise and then set them up with my new domain controller. I might also look into seeing if I can use FreeNAS with it too, so that I don't have to maintain so many separate local accounts on different machines for different users. A central server that manages all logins sounds good. It might be unnecessary for a home network, but it's good from the standpoint of being able to learn more about useful tech. 

## TechLead

I've found TechLead's videos on Youtube to be very informative and interesting. He makes videos about software engineering, tech interview skills, and random programming topics. I don't usually watch non-tutorial Youtube videos much, but these are really great and relevant to #100daysofcode.

## Ways to reduce e-waste

Due to some repainting, I had to move my FreeNAS server away from where it was plugged in (in a closet, out of the way). In the future, I will set it up again. It's just an old computer that was repurposed, like many of my other projects that involve learning things and using servers that don't really need to be super fast. 

Some people think recycling means putting something in a recycle bin. For me, I think actually using tech instead of throwing it out is a good way to recycle, in a way. Electronic waste, or e-waste, is a big problem these days. People want the latest phone or computer, but what happens to all the old ones? Many don't get sold on something like craigslist or ebay, and instead just end up in dumps. But I'm reusing these old computers, which is good.

## Learning more about cloud, infrastructure, etc.

Today, I looked up Hashicorp Terraform, Ansible, Chef, Puppet, infrastructure as code, Vagrant, Vagrant on ESXi, Docker, Kubernetes, unikernel VMs, hypercoverged infrastructure, infrastructure as a service, software-defined networking, network functions virtualization, devops, etc. I have more experience with VMs and hypervisors, but I think I want to get more into containers and container orchestration instead so I can eventually experiment with microservices architecture. 

## A better way to learn Python

Starting today, I am looking through the official Python tutorial [here](https://docs.python.org/3/tutorial/index.html). This might be a better way to learn more in-depth stuff. The problem with many Python programming tutorials is that they assume you don't anything about programming at all, and they only go over really basic stuff. But the thing is... I'm bored with looking at tutorials that only teach hello world stuff, basic data structures and algorithms, etc. I already know all these basic concepts, which I learned in Java and many other languages too already. I don't need a condescending chapter that painstakingly explains what basic control structures are, or what a class is. All I need is something that explains the implementation of these features in the language, not what they are in general. I know what a function is, I know what a module is, I know what inheritence is, etc. Just get to the point and tell me how to do it in this particular language without all the partonizing stuff.

While it's true that introductory programming tutorials are important for beginners, there is definitely a market for programming language tutorials that assume the person using it already knows at least one other language. The problem with beginner-friendly tutorials is that they are often very slow and don't include very advanced topics. 

## More SQL

Today I did another chapter in the SQL book I've been reading.