---
layout: "post"
title: "Day 7: Building a Hypervisor"
date:   2019-01-02 17:03:25 -0600
---

## ESXi

I didn't do that much coding today, but I did build an important device for my upcoming projects. But tomorrow I'll pick up the pace for doing Python and git learning.

### Building a Mini-ITX computer

First things first, I had to pick up the hardware I reserved for an in-store pickup yesterday. This was a really quick project, now that I think about it.

This was my first time dealing with such a small form factor. I wanted something compact and power efficient, while still good enough to handle a few VMs to use for web development, among other things.

![Hypervisor hardware](/assets/hypervisor_build0.jpg)

This is the hardware I picked out for this build. The above photo shows a quad-core i3 8100, an ASRock LGA1151/H370 chipset Mini-ITX board, 2x8GB DDR4 RAM DIMMs, a 512GB Intel 545S NVMe M.2 SSD, a gigabit NIC that I ended up not using after all, and an Inwin Chopin mini-ITX case that also includes a power supply. No graphics card because it's a server and thus doesn't need graphical capability.

![i3 8100 virtualization features](/assets/i3_8100_virtualization_features.PNG)

As you can see, the processor supports useful virtualization features, which is important for an ESXi hypervisor that will be running multiple virtual machines.

![Inwin Chopin case open](/assets/hypervisor_build1.jpg)

While it's unusually compact for a computer, that also means there isn't much room to work with. The incldued PSU is non-modular, which can present some issues for cable management and fitting.

![](/assets/hypervisor_build2.jpg)

The motherboard is really small, with only 2 DIMM slots and a single PCIe 16x slot, though there isn't even enough space in the case to use it at all. I don't need it for my hypervisor purposes, but the board features dual onboard gigabit ethernet, which I assume can make it useful for pfSense or SnortIDS setups. One port for going outbound to the intenet, the other to a switch on your internal network. Certainly beats the ancient Motorola CPUs in the old Cisco IOS equipment I used back when I was studying IT (before switching to CS).

I've set up custom DD-WRT and pfSense routers before, but that's a topic for another day.

Another interesting feature of the board is the built-in 802.11ac wireless, but I don't think ESXi even has drivers for it, so I'll just stick with the wired ethernet connection instead.

![](/assets/hypervisor_build3.jpg)

The board boasts a single M.2 slot, with mounting holes for different sizes, because I guess not all of them are the same length. I've never installed an NVMe M.2 drive before, but I appreciate the lack of extra cabling required. No need for SATA and SATA power connectors. The drive gets power and data transfer pins on the single slot labeled "Ultra M.2." It's really small and felt very fragile though.

Intel stock coolers usually have a pretty bad reputation, but I don't realy have much choice here because of how small the case is. Nothing else will fit. Many parts in this computer have next to no clearance at all.

![](/assets/hypervisor_build4.jpg)

Before doing any sort of elaborate cable management, I just booted it up for an initial test to see if I wired up the front panel connector properly, and also just to make sure I didn't accidentally make some egregious error. It's been about a year since the last time I built a computer.

![](/assets/hypervisor_build5.jpg)

After verifying that everything worked properly, I hid away the cables, some of which could fit behind the motherboard tray. There's actually a rear compartment for additional drives and cable management. 

![](/assets/hypervisor_build6.jpg)

The idle temps seemed fine, and I'm noticing that UEFIs these days are getting more complex. 

![](/assets/hypervisor_build7.jpg)

I didn't even need to change the boot order. It automatically booted from my install drive that I made using a program called Rufus. As long as you research hardware compatibility ahead of time, installing ESXi is a breeze.

![](/assets/hypervisor_build8.png)

I edited out some personal information, like hostname and IP address, but here's the end result: a quiet, compact, power-efficient hypervisor. I use it as a monitor stand now. Because ESXi is primarily controlled via the web interface, I can plug it in with just power and ethernet, no keyboard/mouse/video, and it's still perfectly functional. Similar to the [FreeBSD file server I built a while ago](https://saintlouissoftware.com/file_server.html), at least in that regard.

### It's a cool small computer, but what can you do with it?

First and foremost, I'm thinking of using it for a Bitnami LAMP VM, though for the time being I'm getting back to coding. 

The current programming project is a static site generator, kind of like jekyll but more user-friendly and simplistic. This involves learning Python and Qt, but it also involves interacting with a web server. I'd rather make changes to a local server instead of something on the internet, like my CloudLinux Namecheap shared servers I use with Softaculous/cPanel for websites. It's better to practice and make mistakes offline rather than online. This hypervisor is only locally accessible. 

That being said, the static site generator project only involves generating HTML pages client-side and then merely pushing static files to a server, not really doing anything backend. But that's the whole point of a static site generating tool -- it's supposed to reduce complexity and attack surface on the server, unlike convenient-but-insecure CMSes like Wordpress, which put a lot of extra vulnerable stuff server-side rather than this client-oriented approach that I'm sticking with, at least for now.

Not only will this ESXi hypervisor build be useful for my static site generator project, but there are plenty of VMware appliances, Bitnami VMs, and Docker containers that I can run later for doing other full stack projects, whether it's PHP, Node, or Django. I will probably do a Django/SQLite project after this one's done, though who knows how long it'll take.

### What's the point?

Programming projects like this aren't just about the end result. It's less about the program being made and more about the experience and learning involved. I'm learning about ESXi, VMs, Python, Qt, and version control. Quite often, you'll find that programmers add something to a project not just because it benefits the project, but also because they want to learn that new kind of tech. I could've very easily done this entire project in Java and JavaFX, but I am already quite familiar with both of them. The only way to grow your skill set as a developer is to branch out and use new things you've never used before. 

A developer might unnecessarily incorporate TensorFlow into a project simply because the developer wants to learn TensorFlow. Experiential learning beats reading books and documentation. There's nothing wrong with that for personal open source projects. I wouldn't necessarily take this attitude and apply it to work-related projects though.

Technology is changing all the time. Are you? It's not good to let your skills stagnate. If you're not learning new things, you're actively getting behind, tech-wise. I don't want to be the kind of person who puts all their eggs in one basket and only gets good at one programming language or one way of thinking. Some people still code in Fortran and COBOL, but I'd rather keep up with new stuff instead of sticking to tried-and-true things that won't lead to better opportunities.

### Back to coding

Lately I've been doing too many tech things that, while useful, are not really very relevant to coding. So in the coming days, I'll be focusing much more on programming and less on this stuff. I still haven't set up all the VMs I want, nor have I properly configured everything in ESXi yet. However, this is a big enough project that it's okay to break it up into multiple days. A little progress per day is better than none at all. You don't have to finish everything all in one go, but you do need to chisel away at goals/projects.

