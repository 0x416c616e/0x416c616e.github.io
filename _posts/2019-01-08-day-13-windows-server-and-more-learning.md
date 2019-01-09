---
layout: "post"
title: "Day 13: Windows Server and More Learning"
date:   2019-01-08 23:57:22 -0600
---

## Free old computer

I got an old computer for free. I am going to turn this into a Windows Server project for learning more about enterprise tech, like Windows Server, Active Directory, and maybe LDAP. 

It will require some preparation first though.

I got this computer for free from someone who I built a new computer for. They didn't want to use their old computer for numerous reasons: for one, they got malware on it. They specifically got something called a browser locker, which is a web page that prevents you from closing your browser and tells you to call a fake tech support number. They unfortunately called and cooperated with the scam number, where the person told them to install remote access software so they could "remove" non-existent problems on their computer. I don't know all of what they did on his computer, but in any case, he got scammed, but I got him to cancel the fraudulent charge that ensued. But he didn't ever want to use that computer again, so I built him a new i3 8100-based computer.

That was a while ago, and the old computer has been sitting and collecting dust ever since. I inquired about it recently and I got it for free. Not only that, but in a closet there was another broken computer with some good RAM, even if the other parts were bad. 

All in all, I ended up with a computer with an old dual-core Athlon II processor, with originally 4GB of DDR3 RAM, but an additional 8GB of DDR3 RAM from the other salvaged computer. So I can potentially have 12GB of RAM, though I need to run memtest86+ on it. And it'd only be running in single-channel mode because of the odd number of DIMMs.

I also went to MicroCenter and got a cheap 120GB SSD for this build, because it had some cheap old hard drives.

Because the previous owner reported that they had malware, I am going to be cautious with it. It's quite possible that nothing persistent is on the computer, but I will take the safe route and run DBAN to nuke the old drives, in case they had any malware within Windows still, or perhaps an MBR rootkit or something. I won't even use the HDDs at all. I will also be reflashing the BIOS (it's old enough that it doesn't have a UEFI) in case of any really sneaky (but also rare) BIOS rootkits. The ways malware can be persistent are in the hard drive, within the OS's partition, in the hard drive's MBR, or in the BIOS. By getting rid of the old drives and updating the BIOS, I should hopefully get rid of any possibility of there being any malware on it. In fact, even doing all this stuff might be overkill for what happened, but I would rather be safe than sorry.

So in total, the new free computer with a $25 upgrade has a dual-core processor, 12GB RAM, and a 120GB SSD. I will be installing Windows Server 2019 Essentials. It has a 180 day trial, and after that point I will probably have another educational license I can use to get it for free. I am basically only setting up this server for learning about enterprise tech stuff anyway, so it's fine for that.

![Rufus making a bootable Windows Server installation flash drive](/assets/rufus_windows_server.PNG)

Just like with my ESXi hypervisor, I used Rufus on my Windows 10 desktop in order to make a bootable drive with an ISO file. I prefer USB installers over optical media. 

## osTicket support

![osTicket issue](/assets/osticket_issue.PNG)

Yesterday, when I made a Bitnami virtual machine on my mini-ITX ESXi hypervisor build, I tried following the osTicket installation instructions so that I could have a LAN support ticket system in order to make tech support issues easier to keep track of, and also because it's good to be familiar with tech that is often used in corporate environments, like a ticketing system. There are many different ticketing systems in use by enterprises, but I chose this one because it's free, open source, and you have the option of self-hosting, which is suitable for my hypervisor. Rather than coming as a container or a fully ready to go VM, it's just a program that you need to install within a LAMP stack server, so I thought I'd take the easy way out and use a prepackaged Bitnami LAMP VM .ova file, which makes it easy to set up a LAMP web server in just a couple minutes. But there might be some complications that make it hard to work with osTicket. For example, most Apache web server stuff will be located in /var/www/apache2/htdocs, but Bitnami has a different way of doing this, and it's /opt/bitnami/apache2/htdocs. I really have no idea if that's the root cause of the problem. It also seems like osticket doesn't support newer versions of PHP very well, but I'd rather not stick with PHP 5.6 if I can avoid it. 

I made an account the other day and it finally got approved, so I made a thread and asked for help with the issue I'm encountering. 

## Musings on open source

Open source isn't always about coding and committing to your own GitHub repositories. Sometimes it involves talking with other people to try and figure out complicated issues. Open source is powered by large communities of people. In this case, I'm participating in this open source community by inquiring about issues related to the osTicket project and its implementations. It's not much, but it's something.

Something I need to do more of in the future is code review, contribute to other repos, and pull requests/issues on public projects that I didn't make. The real power of GitHub is the ability to bring people together to work collaboratively rather than everyone doing their own separate thing. It's like a hackathon I went to in St. Louis, just not in person.

## Weird PSU issue

My desktop's power supply will turn the fan off when it's not too hot, but then it ramps up the fan to full speed when it gets above a certain temperature threshold. This means it's silent most of the time, but very loud every now and then, which is really annoying. So I got a fan breakout board that lets you use a barreljack AC adapter to power DC fans. I picked up 2 120mm Cooler Master fans today and now I'm cooling my weird Corsair power supply externally. It's a strange setup, but it's cheaper and easier than getting a new power supply and redoing all of the cable management in my computer.

## VPNs and captchas

Just an observation of mine, after using a VPN for a long time: one annoyance is how a lot of sites will add a Google or Cloudflare captcha if you're visiting the site from a VPN. I prefer to use a VPN pretty much all the time, but this is one of the few drawbacks. 

## More learning

Continued to do more Python Crash Course book stuff and GitHub Ultimate Udemy course stuff too.

A lot of the Python stuff I've been doing lately is really just review (such as lists, list manipulation, loops, and conditionals), and I'm not learning any new concepts I didn't go over in Java and other previous languages I learned. Of course, there is difference in syntax, and Python's basic types (such as lists instead of arrays), and built-in methods and functions (like title() or sorted()), but these are just really small details. On the whole, an object-oriented language is still object-oriented. 

The differences between Java and Python aren't that great, though if I wanted to learn something like Haskell in the future, that would requrire a lot more effort and involvement, because there is very little overlap between the functional and object-oriented programming paradigms.

I'm not making huge amounts of progress each day, but learning a small amount of Python every single day is better than nothing.

As for git, things like branching and merging are not my strong point just yet. So far, I am making the novice mistake of committing everything to the master branch, but that will change in the near future when I get the hang of things more. You're really supposed to use separate branches for things. It'd also be good for me to get more experience with dealing with git repositories that have many different contributors, because there are issues (and commands) that can come up that you won't deal with if you are only working on solo programming projects. I've learned a lot about git on my own, but I still have a long way to go before I'd consider myself to be an expert on it.

## Raspberry Pi etherwake and systemd

I haven't finalized the Raspberry Pi project just yet, but I am planning on using systemd timers in order to schedule a bash script to run etherwake to wake up certain computers in order to schedule routine maintenance like updates, malware scans, and backups. People used to use cron, but now you use systemd to schedule things, unless you're using a distro with a different init system. For as much as people complain about systemd, it's what's in many distros these days, so you might as well learn how to use it instead of trying to fight it. Distros that use sysvinit will simply be forgotten about, because modern Linux uses systemd, whether you like it or not.

I still haven't figured out the issue of etherwake only being able to wake up computers in sleep mode rather than turning a computer on when it's completely powered off. However, I will look more into this. I posted about the issue on social media and didn't really get any conclusive answers, so I'll have to do more research at a later time.