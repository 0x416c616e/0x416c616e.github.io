---
layout: "post"
title: "Day 14: In The Zone"
date:   2019-01-10 8:23:04 -0600
---

## Static DHCP reservations for servers

If you're using DHCP, it can difficult to find servers, unless they are constantly broadcasting their availability. A network I use in my LAN has device drivers for clients that will try and find a network printer that is constantly making its presence known. If you use Wireshark, you will see all the broadcast traffic, which is okay in a small network, but at scale, you can't have everything broadcasting availability to the entire subnet without getting broadcast storms. That's why network segmentation is useful instead of only having a flat network topology. 

But anyway, if you set a bookmark in your browser for a certain local server, and then, for whatever reason, it gets turned off and its IP lease expires, it can get assigned some different address instead when it requests a new address after being put back online. This can make it hard to take inventory and really know all of your assets or where they are. Luckily, routers and/or DHCP servers make it easy to view a table of all DHCP clients, with their lease information, but 

## Windows DHCP Remote Code Execution Vulnerability

Speaking of DHCP, there was recently a serious DHCP security issue in Windows that allows for RCE via specially-crafted DHCP requests. Time to patch. Of course, this would really only affect workstations in an internal LAN, not usually directly-accessible from the outside world because of sane edge firewall ACLs. So while this type of RCE doesn't necessarily mean someone can gain an initial foothold in your network, it does make lateral movement/pivoting a whole lot easier. Imagine if a domain controller used DHCP and you could get remote code execution after merely compromising some random workstation of no value. That's an extreme example, and I doubt people would be using DHCP on a domain controller, but even so. You don't want to make it easier for people to go from lesser assets to more valuable ones.

It's easy for people to make fun of Windows security issues like this, but let's not forget how macOS recently had an issue where you could log in as root by simply not entering any password at all. And Linux has its fair share of CVEs too. 

## In-band vs. out-of-band patching

Depending on the severity of a security issue, you might just wait until the next scheduled patch cycle to apply the new security fix. But if it's really severe, you might do an out-of-band patch, even if it's 2am and you're on vacation. Some threats simply can't wait. Hackers work around the clock and that's why IT operations personnel need to as well -- for better or for worse. It can be easy to dismiss something as being yet another in-band patch, but mitigation is less of a hassle than dealing with the nightmare of incident response and a data breach. Of course, these days, with so many vulnerabilities and patches, it can be overwhelming to the point that you just tune it all out. Oh, another code execution vulnerability? Another privesc CVE? Cool, whatever. We've seen it all before. It's all too easy to become desensitized to really serious security issues because of how common they are. 

## SMB in FreeNAS

I needed to set up an account for myself on a file server.

## No pulse width modulation? No problem!

My... let's say... *creative* PSU fan noise solution has presented one challenge: the Tindie DC fan header board I bought is really simply and thus doesn't support pulse width modulation. But then again, neither do my 3-pin Cooler Master fans. So with no extra fan controller and no PWM control, the fans are at 100% speed, which is high CFM, but too high dB for my personal preferences. I looked in an old box of computer cables I had and came across a Noctua fan resistor cable. It didn't list the resistance on the side, but it did say the model number. So I looked up some specifications online and found out that it's about 150Ω. The problem with this particular fan resistor cable is that it slows my 120mm fans down way too much, to the point that the airflow CFM is next to nothing. 

So I looked online and found some 50Ω cables instead. With only a third of the resistance, it should let the fans spin much faster, but still slightly less than what they're currently at (full blast). 