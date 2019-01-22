---
layout: "post"
title: "Day 23: Big Progress on My App"
date:   2019-01-21 11:22:30 -0600
---

## Today's highlights

The day isn't over yet. I will commit more changes here when there are more highlights.

More random tech learning, more progress on the Windows Server build,

## Updating an entry the day after

Sometimes I am late to update this website. So on the 21st, I actually updated January 20th's article.

## Confidence and encouragement

Now that I've gotten over some design questions, I feel more able to work on SSG. Instead of spending most of my "coding" time just learning stuff, I feel like I can work at a faster pace now. But I'm doing things the right way by really learning the language first before jumping right into some of the problems. This is good because I am really learning what to do rather than learning how to copy and paste from Stack Overflow, which is bad practice in my opinion. 

I have a feeling that the progress on the other features of SSG will go by much faster now that I got the initial put-stuff-into-the-template thing done. It feels really great and empowering to have gotten to this point. I had to do all the frontend web template stuff first, writing it all from scratch in HTML and CSS (well, I guess also using some frontend framework stuff -- but I mean I made it myself, not using a CMS or copying example code).

The remaining parts really aren't that hard to implement. The program might look horribly incomplete, but now that some of the more difficult stuff is done, the seemingly big remainder of the program should go by faster. Not all parts of a program are equally difficult to do. And sometimes, you have to do the hard and time-consuming stuff before you can proceed with the other things.

## Not sure if it will have a GUI

I originally said I wanted Static Site Generator to have a GUI in Tkinter. Will I stick with that after all? I am really not sure. Maybe if people would prefer a graphical program over a command line one. It will take more development time and it will definitely be a challenge, but it might be worth it if it makes a difference in usability. After all, software isn't only made for the developer. It's made for the people who will be using it -- the users. The whole human--computer interaction sub-field is really neat, but not something I am that familiar with. But as designer, developer, tester, and UI/UX person, I am doing it all myself, so I can't really be a pro at every single aspect. I tend to make functional software that isn't very pretty. My frontend web development stuff looks okay because Bootstrap and Google Fonts make it easy to make things look good. But when it comes to native applications, like my Java stuff, and now Python, I don't spend as much time making it look pretty, just as long as it gets the job done. 

## Non-master branch commits don't show up in GitHub contributions

If you're working on a project, and you haven't merged back to master yet, it might look like you're less active on GitHub.

## SQL lesson

Today I will hopefully do the SQL lesson I said I would do yesterday.

I am glad I decide to teach myself SQL. I am eventually planning on continuing with the Udemy course about full stack Python/Django/SQLite development, but I am getting real-world experience with Python with SSG, learning about the limitations of JSON and how a database would be better, learning how databases work on their own (without the context of a Django server), etc. I think this will better prepare me for the full stack stuff later. I really do want to make an IT ticketing system before the 100 days are up. That will be my best project by far, as long as I can actually finish it.

The impressive stuff here isn't making a few apps in 100 days. What's more of an accomplishment is learning the stuff you needed to know in order to make said apps. I could have just stuck with Java, or brushed up on MEAN stack (which I guess I don't like as much, now that I think about it, even though I learned it in college), but then I would just be honing my existing skills. Instead of getting hyperspecialized, I want to branch out and have a wide range of programming skills. The scary thing about specialization is... what if you pick a piece of technology that becomes obsolete or unpopular in the future? You're putting all your eggs in one basket. That seems like a huge gamble to me. Do I think I'm smart enough to predict the future of software development trends? No. Instead, I think diversifying your skills is better than going all-in with one or two things. 

It's also true that you can spread yourself too thinly. I don't want to rattle off a couple dozen programming languages during an interview, because then it'll be apparent that I'm not really good at any particular thing. but I at least want to know a few languages and stacks really well rather than just one or two. 

In fact, some of my tech skills already feel either obsolete or I'm getting worse at them for not practicing them. I don't remember much about the Cisco IOS things I learned in community college. I learned so much advanced Cisco IOS and networking protocol stuff that I only vaguely remember now. Not only that, but concepts like NV or SDN might threaten Cisco's business model in the future. And even though I learned C++ at SIUE, I haven't used it in a while and I'm getting worse at it. I haven't done any C++ programming outside of college class assignments, and I don't like the language that much either. Maybe I can re-learn it and do a personal project with it, but otherwise, it might be something I eventually take off of my list of skills on my site and resume. 

I want to get back into Swift for iOS development and get more into Java or maybe even Kotlin for Android development. The way to keep it simple would be to just make simple apps at first that only do something like maybe interacting with a REST API from one of my Wordpress servers, rather than implementing really complicated stuff. Just to get a feel for the tools like Android Studio, the Android API/SDK, etc. I have used Xcode and Swift for some simple iOS apps, but I need to get back into it more.

With all that being said, so far, my main strengths are Java, bash/cli, Python, git, and frontend development (HTML/CSS/JS). And soon, regex and  backend Django/SQL will be other big skills. I also have a lot of other useful tech skills (like security, virtualization, Windows Server, etc) that aren't really relevant to programming, but still help put things in perspective.

## Gifted vs. persistent

I wouldn't really say that I'm a gifted person. But I might be better than some other CS students who don't have personal projects because I am more motivated and persistent and getting experience on my own. Of course, there are plenty of much much smarter people than me... and one common thing among them was personal projects and coding/learning on their own rather than for credit hours/grades. College is better than no college, but it will still only get you so far on its own. It's a stepping stone to start your journey. Graduation signifies a beginning, not an end.

I am putting a lot of effort into programming, even outside of classes/work. The desire to learn and being genuinely interested in what you do is what separates the wheat from the chaff in many cases. 

Imagine if someone went to the gym 5 times per week to do different muscle group routines (rotating to let them heal after lifting). Then, after persisting for a very long time, they reached their fitness goals. And then someone comes along and says they're just "lucky" or "gifted" or something. That's not true at all. It's about what you put into it. 

## Repurposed computer Windows Server progress

A while ago, I wrote about how I got an old computer for free. The person gave it to me for free because they got malware on it and they were afraid to use it, even after I got rid of the malware with Malwarebytes and MSE (which you should run in safe mode rather than normal mode). MBAM isn't perfect. Neither is MSE (called MSE on Win7, or Windows Defender on Win10). Nothing is perfect, really. I always make sure to enable "check for rootkits" but that doesn't guarantee that everything is 100% safe. So rather than risking anything, I came up with some ideas for what to do in order to make it safe before using it.

Firstly, I am, as of the time of writing this, running DBAN to nuke the contents of the hard drives, just in case there was some malware in the Windows 7 installation, or perhaps even an MBR rootkit, which might be harder for security products to detect and remove. Getting rid of everything on the drives is a good start. I might not even use the hard drives it came with, since they're slow and noisy mechanical drives. I got a solid state drive and some new RAM for it as an upgrade to make it run more smoothly. The SSD cost a little money, but not much. And the RAM was free because I salvaged it from someone else's old and broken computer, which had motherboard issues but some of the other components were still fine.

When you become the go-to tech person among your friends and family, you often end up getting somewhat old computer stuff for free. It's not really worth all that much, but I'm going to repurpose some of it anyway. Not only can I use it for learning Windows Server and Active Directory, but it's also good to reduce e-waste. After all, I won't be contributing to e-waste if I actually use an old computer instead of trying to get rid of it.

Anyway, DBAN will take a long time. Another thing I did (before DBAN) was cleaning out the case. It had a lot of dust and cobwebs, but now it's pretty clean. Dusting computers is important for better temperatures, which will make the computer last longer. Not only that, but it's better for your air quality too. Too much dust is bad for you. 

DBAN will take forever, but once that's done, I will install the new RAM and then run memtest86+ to make sure the RAM isn't bad. It may or may not be bad. Whether it's the new sticks from the salvaged dead PC, or the old single stick of RAM currently in it, I have no way of knowing if it's good or not. It's not ECC RAM, which some people swear by, but as long as there are no errors detected by memtest86+, I think it'll be fine, considering that this is for an almost $0 educational home lab rather than some enterprise production environment.

Once DBAN and memtest86+ are done, I will look up the motherboard and download the newest BIOS version and flash the BIOS. I try to do BIOS/UEFI flashing as little as possible, because any hiccups can render the computer unable to POST. But in this case, I don't want to run the risk of having any BIOS rootkits. I think it's an old enough motherboard that it'll only have an old-school Award BIOS or something like that. None of the fancy new-age UEFIs that support boot verification to protect against rootkits. I really doubt that there are any rootkits, but flashing it will get rid of the possibility of there being anything bad on it.

Once all these steps are complete, which might take a couple days (because it's low priority and I'm not putting all my time into doing it), I will make a Windows Server installation USB drive and then install the Windows Server 180 day trial on it. In 180 days, I might be back in school. Or maybe not. But I'd rather not shell out $500 for a Windows Server Essentials license, especially when it's being run on a computer that isn't even worth $500.

In total, the specs will be:
- Dual-core Athlon II X2
- A stock heatsink from a newer quad-core AMD processor (an upgrade from the original heatsink, but still not as good as an aftermarket one)
- 12GB single-channel DDR3 RAM (due to odd number of DIMMS)
- 2x 500GB hard drives for storage
- 1x 120GB SATA III SSD for the operating system (Windows Server Essentials 2019 64-bit)
- Gigabit networking
- Some low-end graphics card I can't recognize at the moment
- Multi-channel fan controller
- Unnecessary
- Old ATX case
- Some Antec power supply

It's far from great, but it's good enough for simply learning how to use Windows Server and Active Directory. 

My room now has three servers, one desktop, and one laptop in it. I also have a tablet, a Kindle, an old iPhone, and a newer Android phone. So much tech. The hypervisor still has plenty of extra capacity for more VMs in the future, but I wanted the Windows Server computer to be separate for better performance and more room for playing around with stuff on ESXi in the future. If I used up 12GB of RAM, 120GB of storage space, and 2 CPU cores on my hypervisor, there wouldn't be that much left on it for other things, especially considering that it's currently running a couple of LAMP VMs and I am planning on running a Bitnami Django VM on it soon too. My desktop has an Ubuntu VM and a local WAMP stack too. So many things running simultaneously, but it allows me to learn new things better.

## Keyboards, KVMs, and familiarity

I only have one mouse and keyboard, but I will either use SSH or my KVM in order to control multiple devices. Right now, the DBAN PC is hooked up to my KVM, so all I have to do is press a button to change which computer the keyboard and mouse go to. Speaking of typing, I have been monitoring my typing lately, and I can get around 125-135wpm, sometimes just a little shy of 140. I used to primarily use my MacBook's chiclet-style scissor switch keyboard, which features low travel, short distance between keys, and relatively low force actuation. It feels slightly perky, isn't silent, isn't as mushy as a typical membrane keyboard, but also isn't as clacky and loud and awkward as a mechanical keyboard. On the other hand, I just got a cheap keyboard and mouse for my desktop, and at first, when I started really getting back into using my desktop with Windows 10, I was having difficulty adjusting to the keyboard because the keys are farther apart, have longer key travel for actuation, feel mushy and not that great, and stick out significantly higher than the low-profile Macbook keyboard. But the more I practice writing and programming, the better it feels.

The best keyboard isn't the one that's the most expensive. The best keyboard is the one you have the most experience writing on. If you get a new keyboard, you will notice how the layout feels different, how the tactile feedback isn't what you're used to, and things like that. It can really disrupt your workflow at first when you initially make the switch. Now I'm noticing that, becuase I'm getting more used to the cheap traditional desktop USB keyboard, my accuracy and speed with my MacBook keyboard is actually getting worse.

This might not seem like a big deal, but it is when you're a programmer. It's taken me a few weeks to get back to maybe 90% of my MacBook keyboard's efficiency, at least back from when I was using it daily as my main computer.

As nice as macOS and laptop portability are, my desktop is much faster and can handle high CPU load for prolonged periods of time, thanks to its large heatsink and numerous fans. The same can't be said for my MacBook air, which is not great at compiling or running computationally-intensive workloads. It's acceptable for casual use, but for programming, it's not so much the speed that's the limitation, but the thermal limitation is what hinders it the most. 

When doing typing tests, I like to listen to a 650-700bpm software metronome to regulate my internal clock. It forces me to type faster and more consistently. I usually get around 650-700 keystrokes per minute, but with varying accuracy. The accuracy determines how the typing software measures your speed. More mistakes will count as a lower number of words per minute, even if you had a higher number of key presses. I used to take typing speed tests while listening to energetic music, but I think a metronome is more efficient.

## Python modules

I started putting my subcomponents of SSG into modules. I learned about ```__init__.py``` and things like that. I also made a project class. I will be adding more classes to my project instead of having everything be local variables. The project class should really be a singleton, but I made it just a regular class for now because it's easier. The project class is used to get, set, or validate the project name. This will be used by generator.py, which is the entry point for the program. The other modules in the program aren't really classes, but they will have various functions and whatnot, similar to interfaces in other programs. These will be used for the separate submenus that the user is prompted to choose from, such as the article menu, settings menu, project menu, etc. There is also a module for the initial project setup.

