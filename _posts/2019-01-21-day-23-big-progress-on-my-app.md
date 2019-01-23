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

## Python classes

I am making some classes and objects in Python. I've done this all before in Java, but Python isn't Java, and so I'm learning it more in-depth now.

## Python regex and input validation

I am working on validating the input from the user for the project name, for either opening a project, or making a new one. I need to finish a couple things before I can proceed with the articles, settings, etc.

Once I get the program to the point where it checks the name, makes a new project by coping template files over to the new directory with the project name provided by the user, then it will be relatively easy to work on all of the other submenu features, like the article menu, settings menu, project menu, etc. These things all require having a project open, so I need to work on this sequentially. Then, after this feature is all said and done, then I can work on the other submenus out of order because they are not dependent on one another. I will also have to finalize the json and json schema stuff because all of these menus rely on json heavily. But I am getting farther along and it feels good knowing that my software is slowly but surely coming to life.

Sometimes I doubt myself and my ability to make the complicated software I want to make. And it seems like, for every big project, it's always more complicated than I think it will be. This was supposed to be a project that only took me a couple days, and it's ended up taking me over two weeks and I'm still not done.

## GitHub Ultimate course

I have been neglecting this course for a while, but I really want to learn it right before proceeding. Today, I finished the 5th chapter in it, which covered branching and merging (a hugely important -- and also kind of difficult (at first, anyway) -- concept). Now I am incorporating branching into my currently-active repositories, such as staticsitegenerator.

## Advanced algorithms and data structures

I've been watching Youtube videos about interview questions for a few days now. Some of them have gone over algorithms I am not familiar with yet, like flood fill, and trying to figure out, in a 2D grid, which tiles have the most tiles around them with the same color. Flood fill algorithm. I heard someone mention that at the hackathon I went to earlier this year. There are also other katas and algorithms and whatnot that I need to practice on my own if I hope to be successful with these types of interviews. I can do really basic stuff like fizzbuzz, implementing basic data structures, reversing a string, and so on. But not all questions are equally easy. I am also learning more about hashmaps and hash tables, but I don't understand them 100% just yet, though things like stacks/queues/trees/arrays/linked lists make sense to me.

I haven't actually taken a data structures and algorithms course just yet, so maybe I will learn this stuff then. But it's always good to learn things on your own, even if NEIU or wherever will offer classes related to it.

## Healthcare stuff

Moving closer towards doing more healthcare stuff. Depending on how long it takes, there might be some interruptions with my #100daysofcode challenge.

## Closing GitHub issues

Issues on GitHub can be related to adding new features, or fixing things that already exist. Think of it like a public to-do list for an open source project. I closed a couple staticsitegenerator repo issues today. For example, today I used my graphics tablet to draw a new favicon for the site. It just says SSG, but I drew the letters and did some color blending/smudging to make it seem a little more artsy instead of just being a text layer on a plain circle. Now, the site has the proper favicon, with the acronym for the project, rather than the old SFR favicon, which didn't really make sense, and I was only using it as a placeholder for a while.

## Computing big O time complexity

O(n), O(n^2), O(logn), O(1), O(2^n) etc are all possible time spaces for how long it will take an algorithm to run, whether you're talking about worst case, average case, or best case scenario. At one point in time, I remembered how to calculate this stuff. But because it's been a while, I might need to learn this again. Some Youtube videos about succeeding in interviews mentioned that big O notation might be asked during interviews, and it's also mentioned in Cracking the Coding Interview, which is a book I am slowly but surely reading. 

## Regular expressions

Python has a module called ```re``` which can be used for pattern matching. I learned regex back in community college, but it's been a while since I used it and I've forgotten a lot of the specifics, even if I remember the vague overarching concepts behind it.

For my SSG project name stuff, for either opening a project or making a new one, it has to have a valid name.

But before getting into technical regex stuff, I have to lay out the basics of what my project_name string can and cannot be:
- Cannot be 'quit' or 'example' or 'template' or 'testing' or 'test' or 'projects' because those are reserved words. I have an example project.
- No spaces or or quotes or newlines or slashes or basically anything not just plain alphanumeric aside from dashes or underscore for separators
- Cannot be one character long, because my text menus have special meanings behind numbers
- Cannot contain special characters, just uppercase letters, lowercase letters, numbers, and ```-``` or ```_```
- I don't really know what a practical limit length is, but I'll just say 32 characters to keep it simle. That's pretty long anyway.

For the reserved words, I can just do simple checks. But I need to proceed with regex after that.

## Input validation of untrusted user data

You might not be able to trust what the user provides to you. They might not necessarily be malicious, but they might just be giving you incorrect or invalid information. For example, spaces in a folder name can cause problems, and slashes designate subdirectories, which is confusing in a file path. Also, . means the current directory, whereas .. means the parent directory relative to the current working directory. If you don't validate things like that, you can end up with path traversal bugs, which, for a networked application, are serious security issues that can lead to people grabbing things like ../../../../../../../../../../../../etc/passwd or ../../../../../../../../../../../../etc/shadow, which is not good.

Other examples of needs for input validation include SQL injection, overflows, fuzzing, insecure deserialization, "trust zones" (that assume certain input has already been validated and is now trustworthy if it made it that far), etc.

For my personal SSG project, there isn't really so much a security concern, but if the user provides bad information, it can cause problems. What if they enter nothing and just hit enter? Then I have to check to make sure the input isn't null. I also have to make sure it isn't too long, because path length can't be unlimited. And there are some reserved words that my program uses for commands and/or other directories. The word 'quit' is used to quit or end input for certain things, getting out of menu loops. So having the user be able to make a project called quit would cause problems, and then they might not be able to open it in the future. It would only harm that particular user, nobody else. It's not hacking, just preventing bugs and inconveniences/undefined behavior.

