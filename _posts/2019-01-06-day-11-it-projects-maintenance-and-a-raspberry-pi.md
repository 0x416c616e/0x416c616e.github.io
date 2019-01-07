---
layout: "post"
title: "Day 10: IT Projects, Maintenance, and a Raspberry Pi"
date:   2019-01-06 20:12:37 -0600
---

## IT Projects

I am making more in-depth plans for some IT-related projects I want to do. I'm admittedly getting a little sidetracked, when I could be concentrating completely on Python instead. But today I made more concrete ideas for more home lab stuff. It's a combination of projects being useful while also being educational. 

![ESXi logo](/assets/esxi.png)

Here are some ideas I have so far:
- Getting a Cisco Catalyst 2950 or 2960 because I need a multi-port switch, and also it'd be good to get a refresher on Cisco IOS, instead of letting my old IT classes go to waste
- Setting up a pfSense firewall -- DD-WRT seems okay most of the time, but I'd like to set up another dedicated firewall. I used to have one and I'm not sure why I didn't do it again.
- Raspbian wake-on-LAN server -- it will be on 24/7, with sleep mode disabled, and have a cron.weekly script to turn all computers on for weekly backups/updates/scans. Probably the easiest of these projects.
- Setting up another old computer as a second hypervisor, because my budget ESXi hypervisor may or may not be enough for my VM and Docker container needs. It might be good to use a different hypervisor, such as Citrix XenServer, rather than doing everything in ESXi. That way, I'll get experience with multiple platforms instead of just one.
- Nagios SIEM, possibly with the Splunk add-on. SIEMs are a big deal and I think I need to get more experience with enterprise security. Anti-malware software is not a fully-fledged security solution, so things like this are important.
- SnortIDS -- I don't know too much about intrusion detection systems, except that Snort comes up a lot among people who know a thing or two in infosec or IT.
- Bitnami LAMP server VM -- for my upcoming web development projects
- Kubernetes and Docker -- some apps don't need entire VMs. Sometimes, they just need a container. You can have multiple Docker containers and manage them with Kubernetes. 
- osTicket ticketing system -- for tech support tickets, when people have issues with computers or software. This could potentially be in a container, within a Linux VM, within ESXi. Kind of unnecessary to set it up that way, but then I'd learn a lot of useful topics. Probably one of the easiest projects here.
- PiHole DNS sinkhole for ad blocking -- a fun and interesting network-based ad blocking project. Nowadays, because of problems like malvertising, ad blocking is basically a security measure, not just a way to get rid of annoying ads.
- Windows Server -- terms like "active directory" and "domain controller" get brought up a lot in IT and pentesting, so I should get familiar with it.


I spent a lot of the day learning about each of these things. Not exactly related to coding, but infrastructure is still really important. A lot of infrastructural issues are abstracted away from the developer these days, but I think it's goot to maintain a multidisciplinary skill set consisting of both IT and computer science subjects, not just one or the other. There are people in IT who don't know how to code, and people in software development who don't know basic sysadmin stuff. For devops, you need to understand other people's roles, even if it's not your main body of knowledge. At the very least, it will help you understand your coworkers and their jobs better. It makes it easier for people with different roles to work together without problems.

## Maintenance

![Ninite updater](/assets/ninite.png)

I did a lot of maintenance for myself and my relatives. Lots of software updates, malware scans, backups, and things like that. I also taught someone how to do some of these things instead of just doing it for them completely. I try to turn these sessions into a combination of being helpful and educational. This took up a bulk of my day.

Linux makes it easy to install updates, just using the built-in package manager and running these commands:
```
apt-get update
apt-get upgrade
```
On Windows, unless you're doing network imaging/PXE/netBIOS stuff, updating programs individually, such as in a SOHO environment, can be annoying. But Ninite Updater makes it a little more manageable. And for macOS, I use the homebrew package manager. It's not as good as a package manager on Linux, where most packages are supported. There are still unfortunately many things in macOS that you can't install or update in homebrew, but it's better than nothing.

## Raspberry Pi

![Raspberry pi photo](/assets/raspberry_pi.jpg)

As I mentioned in the IT projects list above, I'm planning on doing wake-on-LAN stuff on many devices in order to schedule routine tasks so that they don't have to be done manually. It's good to do things like software updates, malware scans, and file backups when people are asleep. These things are often slow and can affect computer or network performance, so it's best if you're not using your device when it's happening. And what better time to schedule it than when you're not awake?

![Preparing the SD card for Raspbian](/assets/sd_card_rpi.png)

I have a Raspberry Pi that I installed Raspbian on. The HTTP download of Raspbian was very slow, so I used the torrent version instead, and it was a lot faster. 

![Raspberry Pi wake-on-lan](/assets/wake_on_lan_pi.png)

Lastly, I set up SSH on the Raspberry Pi so I can access it on my MacBook or desktop rather than hooking up a keyboard, mouse, and monitor (or KVM) to the Pi itself.

![Logging in to a Raspberry Pi over SSH](/assets/pi_ssh.png)

## More Udemy learning

I did more lessons on Udemy today.

## .gitignore

I added a .gitignore to all my repositories, and made sure to ignore .DS_Store, which is a common annoyance on macOS.