---
layout: "post"
title: "Day 12: Enterprise Tech, Git, and Python"
date:   2019-01-07 11:07:30 -0600
---

## Learning outside the classroom

This #100daysofcode challenge is about programming, but I have more of an interdisciplinary skill set that combines IT and computer science. I studied IT in community college before transferring to a university to study computer science, which I am still in the middle of. In addition, I've also taught myself a lot about IT and programming topics that weren't taught in classes. 

So the reason why I'm laerning about hypervisors and VMs, and planning on learning about Windows Server/Active Directory and ticketing systems and whatnot, is because I know it's all useful stuff, even if it wasn't taught in a class. My programming classes taught mostly Java, and some C++ (which I am honestly not a big fan of), but I've realized that Python is really important too. 

## More in-depth project plans

The projects I will complete in the near future are an osTicket ticketing system (running in my Bitnami Debian Linux LAMP VM on my ESXi hypervisor), setting up an old computer with Windows Server to learn about Active directory (my hypervisor has limited resources and I want something a little beefier for Windows Server), and a pfSense firewall with the Suricata IDS plugin. In the past, I was thinking about using Snort instead, but apparently it's in decline and a lot of people have given up on that and switched to Suricata instead. So that's what I'll start with. I haven't forgotten about my Python static site generator project, I'm just thinking of other things to do.

## Bitnami virtual machines

![Bitnami logo](/assets/bitnami_logo.png)

Bitnami is really cool. They have lots of preconfigured full stack development VMs. For example, you can download a LAMP VM, Django VM, and so on. Then you just install it on your hypervisor, and you're good to go. No need to spend a long time setting everything up. The default username and password are both bitnami, and after the initial installation and login, it prompts you to change the password to something more secure. It's as simple as can be for locally-hosted web servers!

## LAMP stack

![Installing Bitnami in ESXi](/assets/bitnami_lamp_esxi1.PNG)

Today, I made a little progress on my osTicket idea by creating an initial bitnami LAMP VM in ESXi. I haven't installed anything in it just yet, but I will use it for at least osTicket and maybe for other projects too, such as my static site generator project. I can use subdomains or different directories to have multiple apps/CMSes/projects on the same web VM. After all, none of these things are really resource-intensive. 

![Bitnami in VMRC](/assets/bitnami_lamp_vmrc1.PNG)

I still have plans to do Python/Django/SQLite development, and my web development class I took in college had me do a MEAN stack project. However, LAMP is still really useful. It's widely used, especially in business and legacy applications. Django and Node might be cool, but they might not be as useful in many workplaces. It's good to stay current, with modern languages and frameworks/platforms, but if you look at things like Ruby on Rails, you can see how learning something new isn't great since it might not have a lot of staying power. Ruby was hot in the mid to late 2000s, but it's been in decline since then. Meanwhile, people still use a lot of older stacks for web development, such as LAMP. LAMP is really a staple of web development, even if people think it's long in the tooth. It's good that I learned Node and MongoDB in college, but jobs I might apply to in the future could still be using MySQL/PHP/Apache, even if it's deemed "uncool" nowadays.

![Bitnami web interface](/assets/bitnami_web_interface.PNG)

One benefit of VMs is that you can have them separated, which is good for security. A good rule of thumb is to have a separate VM for every server-related thing. So one VM for a mail server, one for your Windows Server/AD stuff, one for osTicket, and so on. I think this would fall under the category of "separation of concerns" (though that might not be the right term, but close enough). Even so, because this will all be LAN-only, I don't need to worry about that stuff as much. But for an internet-facing production server, especially without the same resource limitations as my low budget hypervisor, then I wouldn't do it the same way as what I'm doing now.


## osTicket

![osTicket Logo](/assets/osticket-logo.png)

I've managed to set up osTicket within my Bitnami LAMP VM, but I've encountered an error that has made it so I can't continue. I made a forum account on osTicket's website, but it won't let me post a thread asking for help until the account is manually approved. But I'm slowly but surely working towards having a functional ticketing system. 

One issue I noticed is that Bitnami uses /opt/bitnami instead of /var/www so I think it might be a path-related issue, but I'm not entirely sure. 

Also, I'm sort of new to PHP, but it seems like there is a divide between PHP 5.6 and PHP 7.X. It reminds me of Python 2.7 and Python 3.X. A lot of legacy stuff is still stuck on a really old version of PHP, which no longer gets security fixes. Maybe the issue I encountered in osTicket is because I'm using PHP 7.1 instead of 5.6. But on principle, I think it's a really bad idea to stick with an unsupported version of PHP just for the sake of compatibility. You really need to use a version that gets security updates.

## Git

I continued to learn more about git today. In the GitHub Ultimate course on Udemy, I learned about more in-depth git commands and usage.

## Python

Using Udemy and the Python Crash Course book, I learned more about Python today. 

## PowerShell and SSH on Windows

![Powershell SSH screenshot](/assets/powershell_ssh.PNG)

I like that Windows has PowerShell and SSH now. I remember back in the day when you had to install PuTTY in order to do remote access to things. A lot of what I like about macOS is how a lot of programming-related things come with it by default, whereas in Windows 10 you have to install a lot of stuff in WinGW, WSL, and so on. But once you get the hang of it, you can get a similar experience to macOS or GNU/Linux.

Windows 10 isn't as bad as I thought it would be. It's still a perfectly capable development platform, and most of what I use it cross-platform anyway. As a developer, because I myself use many different operating systems and devices, prefer cross-platform stuff, and because of that, I try to make my software cross-platform too. That's why I really like the web, as well as Java and Python. 

I've done some Swift projects for iOS, but I can't help but dislike the fact that I'm basically learning an IDE (Xcode) and language (Swift) just for a single platform. 

## Works on my machine

![Kubernetes logo](/assets/kubernetes-logo.png)

Another modern development in multi-platform deployment is containers and orchestration, like Docker and Kubernetes. I don't know too much about it just yet, but I'd like to incorporate containers into my development workflow in the future. Then you can make sure your projects will work on other people's devices, since it packages all the dependencies in them. I learned from using Jekyll that Ruby can be weird about different versions of Ruby, and using tools like rbenv can be a nuisance. 