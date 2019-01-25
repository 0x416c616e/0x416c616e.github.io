---
layout: "post"
title: "Day 27: SQL and SSG Again"
date:   2019-01-25 1:22:30 -0600
---

## More of the same

Today I did more Python programming for SSG. I am slowly but surely chipping away at the development of it. And more importantly, I've finished all the concrete details for the design, so it's very clear what I need to do. That is the hard part. Once you've figured out what you're going to program, it's not that hard to go and implement it. Programming is only more difficult when you're not sure how to design something, or just coding without any sense of direction. But I like to plan things out before jumping right in and coding. That's why this phase is a lot easier for me now. Project management, sprints, etc. all really matter.

## SQL learning

I did another SQL chapter today. 

## Windows Server progress

I finished memtest86+ on it, and surprisingly, all the old RAM sticks were just fine. So it has 12GB of RAM. It's a weird amount, and it will only be running in single-channel mode, due to being an odd number of DIMMs. But that's okay for a low-usage server like this, which is primarily intended to be used educationally, not really at high load.

After finishing memtest86+, I used a tool called Rufus to make a bootable USB installer for Windows Server Essentials 2019. I use a KVM so I can control multiple computers with just one keyboard, video output, and mouse. 

I installed Windows Server Essentials 2019 on it. I installed it on the SSD and then set up the 2x 500GB drives in a mirror, using Windows' Computer Management program. Everything seems good enough.

I had to research Windows 10 versions. You need at least Windows 10 Pro in order for a workstation to be able to connect to a domain. If I want to use some computers with it, I might have to change their versions/licenses. I use a site called Kinguin to buy Windows keys. 

## Factory design pattern

Today, I learned about another kind of design pattern: factory.

