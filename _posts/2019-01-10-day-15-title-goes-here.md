---
layout: "post"
title: "Day 15: Title Goes Here"
date:   2019-01-10 0:24:39 -0600
---

## Static DHCP reservations for servers

If you're using DHCP, it can difficult to find servers, unless they are constantly broadcasting their availability. A network I use in my LAN has device drivers for clients that will try and find a network printer that is constantly making its presence known. If you use Wireshark, you will see all the broadcast traffic, which is okay in a small network, but at scale, you can't have everything broadcasting availability to the entire subnet without getting broadcast storms. That's why network segmentation is useful instead of only having a flat network topology. 

But anyway, if you set a bookmark in your browser for a certain local server, and then, for whatever reason, it gets turned off and its IP lease expires, it can get assigned some different address instead when it requests a new address after being put back online. This can make it hard to take inventory and really know all of your assets or where they are. Luckily, routers and/or DHCP servers make it easy to view a table of all DHCP clients, with their lease information, but it's easier to just create static DHCP reservations so that your servers will always have the same internal IP addresses (regardless of NAT or whatever for your WAN setup).

## Windows DHCP Remote Code Execution Vulnerability

Speaking of DHCP, there was recently a serious DHCP security issue in Windows that allows for RCE via specially-crafted DHCP requests. Time to patch. Of course, this would really only affect workstations in an internal LAN, not usually directly-accessible from the outside world because of sane edge firewall ACLs. So while this type of RCE doesn't necessarily mean someone can gain an initial foothold in your network, it does make lateral movement/pivoting a whole lot easier. Imagine if a domain controller used DHCP and you could get remote code execution after merely compromising some random workstation of no value. That's an extreme example, and I doubt people would be using DHCP on a domain controller, but even so. You don't want to make it easier for people to go from lesser assets to more valuable ones.

It's easy for people to make fun of Windows security issues like this, but let's not forget how macOS recently had an issue where you could log in as root by simply not entering any password at all. And Linux has its fair share of CVEs too. 

## In-band vs. out-of-band patching

Depending on the severity of a security issue, you might just wait until the next scheduled patch cycle to apply the new security fix. But if it's really severe, you might do an out-of-band patch, even if it's 2am and you're on vacation. Some threats simply can't wait. Hackers work around the clock and that's why IT operations personnel need to as well -- for better or for worse. It can be easy to dismiss something as being yet another in-band patch, but mitigation is less of a hassle than dealing with the nightmare of incident response and a data breach. Of course, these days, with so many vulnerabilities and patches, it can be overwhelming to the point that you just tune it all out. Oh, another code execution vulnerability? Another privesc CVE? Cool, whatever. We've seen it all before. It's all too easy to become desensitized to really serious security issues because of how common they are. 

## SMB in FreeNAS

I needed to set up an account for myself on a file server.

## No pulse width modulation? No problem!

![](/assets/resistor_cables.jpg)

My, let's say, *creative* PSU fan noise solution has presented one challenge: the Tindie DC fan header board I bought is really simply and thus doesn't support pulse width modulation. But then again, neither do my 3-pin Cooler Master fans. So with no extra fan controller and no PWM control, the fans are at 100% speed, which is high CFM, but too high dB for my personal preferences. I looked in an old box of computer cables I had and came across a Noctua fan resistor cable. It didn't list the resistance on the side, but it did say the model number. So I looked up some specifications online and found out that it's about 150Ω. The problem with this particular fan resistor cable is that it slows my 120mm fans down way too much, to the point that the airflow CFM is next to nothing. 

So I looked online and found some 50Ω 3-pin fan resistor cables instead. With only a third of the resistance, it should let the fans spin much faster, but still slightly less than what they're currently at (full blast). 

## Python

Continued to learn more about Python. Aside from Python Crash Course, I am also doing a self-paced video and programming course on Udemy called Complete Python Bootcamp. There are occasionally exercises, but it's a little less hands-on than the Python Crash Course book. Even though there are programming exercises, they are browser-based, so I don't commit them to my python learning repositories, so it might not look like I'm doing much even when I am. 

The Python Crash Course book and this Udemy course are structured a little differently, so I pick up on bits and pieces from each course and they cover different things that the other doesn't have. It's interesting to do it with multiple perspectives about what's important in this language. 

I am getting closer to feeling more confident in my ability to write at least a command-line static site generator, even if I don't have the Qt GUI framework know-how for the visual frontend compoenents just yet. But that will come later.

## Jekyll Pagination and Disqus Comments

There are too many posts on my site on a single page, rather than breaking things up into multiple pages. I want to change that. I haven't really customized much about Jekyll yet, aside from adding a favicon, which was surprisingly complicated for such a simple feature that is actually much easier when writing a site from scratch.

My other website, [Saint Louis Software](https://saintlouissoftware.com), already uses Disqus for comments on articles and project pages. However, I set up a lot of that site in a really inefficient manual way rather than automating repetitious things. It wasn't made with a static site generation tool like this site was. 

## Google Analytics

As much as I like to talk about privacy, Google Analytics is really nice in a lot of ways. I use it on all my Wordpress sites, as well as my Saint Louis Software site. I'm going to add it to this site too to learn more about traffic stats. Because this particular site is hosted on Github Pages, you can't see any server stats the way you can with a LAMP server and something like awstats. awstats might be inaccurate, but it's still a way to learn about site traffic even when you don't have Google Analytics. But I have absolutely no way of seeing server logs here unless I add Google Analytics.

## More osTicket stuff: error logs from Apache and PHP

I'm still trying to get osticket sorted out. 

## Slow progress on Windows Server project

I want to take a break from doing non-coding tech projects and concentrate more on coding for a while. So for now, the free computer/Windows Server/Active directory stuff is on hold while I do more programming. After all, it's called #100daysofcode, not #100daysofrandomtechstuff.

## KVM

I set up a KVM so that I can use my single mouse and keyboard to control multiple devices. KVM stands for Keyboard, Video and Mouse. Right now, it's just hooked up to my desktop and the on-hold server project. I would have hooked it up to my hypervisor as well, but the hypervisor only has onboard HDMI, and my cheap KVM only has VGA cables for video. Besides, the hypervisor is mostly controlled through the web interface anyway.

I also have some cables so I can use it with my macbook if I really want to, though macOS seems better geared towards touchpad usage instead of a mouse. 

## Auth tokens and passwords accidentally put on GitHub

I've accidentally come across some repositories where people put private credentials in a public repository. Now that's not to say that the entire project needs to be private, but I have a very easy solution:

1. put access tokens, passwords, usernames, etc. in a separate config file. Doesn't matter if it's JSON, txt, csv, whatever. ANYTHING. It just has to be a separate file.
2. create a .gitignore file and put the file name(s) of the config file(s). Only one term per line. 

.gitignore is a really powerful but simple concept in version control becaues you can do lazy commands like git add -A to add all files to commit, yet the files specified in the .gitignore will still be ignored, even though the command supposedly adds all files (it's all except the ones you specifically want to ignore).

**So what does this mean for me?**

It means I might be able to create issues or pull requests telling people to remove this sensitive login information from their repos, and also include some basic steps for how they can do it.

