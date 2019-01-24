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

I guess I should be using docstrings instead of comments, but whatever.

With all these functions, I had the ideas for them -- name, purpose, arguments, and return values -- and I came up with the design for this module faster than I can implement it. So how did I keep track of it all? Well, I certainly didn't just rush in and write it from start to finish. Instead, I came up with a list of requirements and then used the ```pass``` keyword to make empty functions that do nothing. Later, I will finish them. But for the time being, I can at least remember what I'm supposed to make here. This reminds me of C++ function prototyping. It's kind of similar, except that, rather than writing function definitions separately, I will just replace the ```pass``` keyword with the real contents. 

I also used to make UML diagrams in my old CS classes, but that seemed like too much effort and it was too indirect, when instead I can just write stub/prototype functions that don't do anything, but still make it clear what I'm trying to accomplish in the future.

The issue with software development is that you can come up with ideas for things to make faster than you can make them. Whether it's an idea for an entire app, an idea for a class, a module, or even just a function, it takes only a few seconds to come up with ideas, but making it can take a really long time, depending on what it is. 

Some people pretend that they can remember everything. I know I can't, so that's why I like to do things like this in order to write down my thoughts and designs before I forget about them. That's also why self-documenting code, brief comments, and documentation pages, such as wikis or readmes, can be very useful. But the problem with verbose documentation is that a small change to code means you have to read through long documentation to figure out which parts need to be updated. 

## Progress I made today

Today, here are the features I finished in static site generator:

- Started to design and work on initial_setup_module.py
- Finished more json and file stuff (for the template) -- this is because the initial setup module gets the user to set up basic info about the project and stores it in settings.json and about.json, so I really had to figure out what will go in these files -- about.json is very straightforward, but settings.json has a lot of different settings in it
- Made function prototypes for what will be in the setup module when it's done
- Imported the module in generator.py, which is the entry point for the whole program
- Wrote and tested ```check_if_setup_has_been_completed(project_name)``` in the setup module
- implemented if/else check function call in generator.py's print_numbered_menu(menu, proj) function
    - The setup check will run after a project has been successfully opened -- if the project has never been fully initialized, it will restart the entire process, and only after it's done will it save ```True``` to finished_initial_setup.txt
- Started working on the second function in the initial setup module (not finished yet though): 

![](/assets/initial_setup_module1.PNG)


## More refurbished server progress

I recently got a computer for free. I upgraded it using a combination of free stuff from salvaged dead computers, and a new SSD that I got for it. In total, it has a dual-core processor, heatsink from a quad-core processor, 12GB of DDR3 RAM, a 120GB SSD, and 2x 500GB drives that I plan on using in RAID 1 for redundancy and better read speeds. I am going to install Windows Server Essentials on it so that it can act as a domain controller.

But first things first: for trust/security reasons, I had to wipe the drives with DBAN, and I also reflashed the BIOS. I am concerned about things like BIOS rootkits and MBR rootkits. When you wipe everything out, for the the BIOS and the hard drives, then there's nothing left than can persist. It took me a while to do all this stuff, and also adding the new SSD and RAM and doing some cleaning and cable management too, since it was dirty and had a lot of cable ties holding everything together. 

I finished running DBAN on it, and now I'm running memtest86+ to test the RAM and make sure there are no errors. Even though it's for a server, I don't have ECC RAM. Honestly, most of the time, ECC RAM is unnecessary, especially for home lab stuff like this, as opposed to a production environment in a large-scale enterprise. But I still just want to make sure everything is okay. Then I will make a bootable USB drive for WSE and set it up with some sort of remote access so I can use it on my main computer. I have a KVM, but I think it's good to get more experience with ssh (which I already use), RDP, VNC, etc.

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

## Exceptional handling in Python

So far, I haven't really done official exception handling in Python. Java yells at you if you don't handle exceptions, but Python seems more lax about them. For the initial setup module, I will need to do try/except for the file IO stuff. It's possible that files might be corrupt or something, or just missing, or have the wrong structures that don't conform to the schemas that I have yet to properly validate. But basically, this is another feature of Python I can get experience with -- in a real app, as opposed to something made up for the sake of demonstrating the feature of the language.

## More SQL

Today I did another chapter in the SQL book I've been reading.

Here's what I learned about SQL today:

Putting multiple ```WHERE``` clauses together. You put them together using things called **logical operators**. For example, ```AND``` or ```OR```. Not that different from other languages, aside from being in all caps. 

```SQL
USE some_database;
SELECT some_column, some_other_column
FROM some_table
WHERE some_random_column = 'something' AND some_column > 100;
```

![](/assets/sql_and_operator.PNG)

In the above query, both of the things used with ```AND``` need to be true in order for them to be retrieved. Simple boolean logic.

```OR``` just means only one or the other has to be true.

I took a class at SIUE called Reasoning and Argumentation. It went over boolean stuff like this. And even aside from gen ed classes like that, it's useful for many programming situations, even outside of SQL. For example, control flow stuff like while loops and if/elif/else clauses.  

You can also combine multiple operators. You could use an ```AND``` followed by some operand and then another operator, such as an ```OR``` followed by another operand. They can be as simple or complicated as you want them to be. However, be careful about order of operations. As with any other language, parentheses help make order of operations clearer.

```SQL
IN
```

Next up, there an operator called ```IN```. It's used for ranges.

![](/assets/sql_in_operator.PNG)

And finally... the last operator in the chapter: ```NOT```

```NOT``` in sequel is just like using ```!``` in other programming languages, or even ```not``` in Python.

## Other books I've been reading

I'm still slowly but surely reading Coders at Work, Learn Version Control with Git, Learn SQL in 10 Minutes, Python Crash Course, and The Manga Guide to Databases. I used to prefer physical books, but nowadays, I'd rather get an e-book and read it on a Kindle Fire because it takes up significantly less space. When I recently moved from St. Louis to Chicago, I couldn't take everything with me because I was moving by myself and just using my car. I didn't feel like renting a truck or anything. So I got rid of most of my physical copies of books, but I still get to keep all of my e-books on my Kindle and computer. 

## Lack of interactivity with this site

This site is basically just default Jekyll, with a couple slight tweaks here and there. But rather than customizing Jekyll, I'll be incorporating Disqus comment functionality into my static site generator so that people will be able to leave comments that way. I see not much point in customizing a project someone else made when instead I can just focus on my own project. This site is still unfortunately using Jekyll, but it'll be a while before my static site generator is completely done and I'll be able to migrate this site fully over to it. Makes me wonder if I'll ever finish with the IT ticketing system before the 100 days are up. If I spend the rest of this #100daysofcode challenge on just the static site generator, learning Python/Django/SQL, and then the ticketing system, I might not have time to do anything else. I guess that's fine. I just had unrealistic expectations about how much I'd get done.

## What the IT ticketing system will entail

In an enterprise environment, employees or other staff/volunteers/personnel need the ability to contact IT staff. While there are IT offices, people can also submit support tickets online or even over the phone (though depending on how the person contacted the IT department, it might be the IT staff who have to end up writing the ticket on behalf of the person calling in). Some places are absolutely required to do ticketing, for SLAs or something, and other places just choose to do it because it's useful. 

A ticketing system makes it easy to keep track of the support requests users have for the IT employees in an organization, whether it's a college or a business or whatever. Sometimes, there might be a public-facing ticketing system for a website. Other times, a ticketing system might be internal and only for people on company networks/VPNs. But in any case, people need to be able to submit requests for tech support. 

What a user sees and what the IT staff see are very different. A user will be able to put in their contact information, select categories from dropdown menus, etc. This is all web-based, mind you. Then, they can submit the ticket to the IT ticketing system server and it will be entered into the backend database. Depending on how complicated the ticketing system is (mine will be very simple!), some might notify people about it. A lot of IT software involves dashboards, where IT staff can log in to see the status of things. There are two types of IT ticketing system accounts: the admin account and regular IT staff. The system administrator of an organization might have the admin account, and they use it for setting up the ticketing system, changing settings, installing updates, and adding or deleting accounts for IT help desk/call center staff. These IT accounts have more limited privileges, but they can still log in to view and complete tickets. 

A ticketing system might have a knowledgebase, which is a list of canned responses to common problems that come up time and time again. They do not need to rewrite the same thing over and over again, and instead can just click a button to add that knowledgebase answer to a ticket. They can also ask the user about the issue. They might require more details. The ticketing system will mail the IT staff's response to the user. Sometimes, someone might want to only use the email/messaging aspect to make appointments to meet with someone in person, because that's a preference for some people. In some cases, they might need to take their tech to the IT department, or the IT department might have to come to their office/cubicle in order to look at their workstation. At a university, you will find that more people go to the IT department rather than the IT department going to them. But in any case, these are all done through messages in the IT ticket. An IT ticket is sort of like a forum thread, but more professional and not social. 

Once the ticket is solved, it will be closed. Sometimes, it might be closed because the IT staff was able to help the person fix the issue. Other times, the person needing support might forget about it and not respond, in which case the ticket can be closed due to inactivity. Time is important. There will typically be a queue or back log of tickets to respond to. It's like a game of whack-a-mole: you close one ticket, and two new ones are submitted. Tickets can be assigned priorities and due dates. A simple way to write a very minimal ticketing system would be to just add a default deadline for everything, like maybe a week or so. This one-size-fits-all solution isn't great, but you need to start small instead of having a billion bells and whistles for your app.

There are titles and message bodies for the support tickets, much like email. And a signed in IT user can sort the tickets by things like due date. If there are lots of tickets, it might use pagination in order to break it into multiple pages. Let's say, 25 tickets per page, so if there are 49 tickets, there will be the main page with 25, and then if they click to go to the next page, they will get the other 24. By default, it would make sense for the tickets that are about to expire the soonest to appear at the top, because that means those people have been waiting the longest.

The ticketing system needs a form of authentication that will only allow logged in accounts to view the tickets. The tickets in the web app combine the template system for the frontend, with queries to the database to retrieve records about tickets. Because of all the tech involved in this, it's considered a full-stack web app. And because people use mobile devices and computers these days, the frontend would need to be reponsive and mobile-friendly, ensuring it looks good on phones, tablets, and computers -- and in multiple browsers in each.

But the frontend stuff isn't the hard part. The backend stuff, like the logic for logging people in, the model-view-controller architecture (or whatever the Django equivalent is), the database, the tables in the database, etc.

That all being said, my personal IT ticketing system will be made with Bootstrap for the frontend, Python/Django/SQLite/Linux for the backend, and I will be using git for version control, putting it all on GitHub. I've gotten a better grasp on git and Python thanks to doing the static site generator, among other projects.

It's important to make sure that I do logging and unit testing, instead of manual stuff like what I've done in the past. I will be learning the Django/SQLite stuff with a Udemy video series, though most of the learning will come through making the app.

Now that I have the main ideas for the app, it won't be too hard to start working on it and making a "minimum viable product" version of it. I will run the web server on my hypervisor. The idea for the app came from me using osTicket, another ticketing system, and encountering errors with it. I figured I might as well write my own as a good experience for programming, and it's something I can put on a resume too.

The only real issues with this project will be time management and scope creep. I can't have it do too many things or else it'll never get done. So basically, at least for the first release of the program, it will be a very simple ticketing system, more useful for small-scale stuff instead of serious enterprises. But I can always add more features in the future -- just as long as I code it in such a way that it's self-documenting and easily-estensible. This isn't a Java project, but when I was learning Java, extensibility and future usage were highly emphasized. It is an enterprise language, after all.

But with over a quarter of my 100 days of code already over, I need to sacrifice cool features for the sake of time. I watched a TechLead video and he said that a single fisheye lens feature for a photography app he made took him over a month. Just for a single feature in a single app! That's a lot of work. I can't make anything that will take that long just for a small part of it. There are so many parts to this that I'll have to be quick on all of them, simply because there are so many of them.

I think that, if I make an ultra-minimalist product, I can get the It ticketing system done before the 100 days are over. That's my new goal: just finish static site generator and make a basic ticketing system.

The good thing is that I already have a very solid idea about what the app will do, and more importantly, what it won't do. Software engineering and design are all about thinking and planning. It's way more than just coding. And as you can see here, I've already done a lot of the planning. I'll make more in-depth plans before jumping right into it though.

I will also try to incorporate some of my new knowledge of design patterns, but I won't do it excessively. At least singleton seems easy to understand and very useful. 

I would like to reiterate that the ideas I have here for a ticketing system are all my own. I couldn't even log in to osTicket because it gave me an error message. So it's not as if I'm just copying something else. The fact that I have to make my own decisions for what to code is what makes this project great -- it's not one of those paint-by-numbers coding projects where someone tells you exactly what to do. I have to figure it out myself, and that's what makes it simultaneously interesting and challenging. 

## Deleting repositories

In order to have fewer distractions and temptations to waste time on other apps before the ticketing system, I deleted a lot of my other future project repos that I would've wasted time on if I didn't do this. These weren't half-finished projects, they were ones I'd barely started on at all, and the issue is that I can come up with a few dozen app ideas in the time it takes me to make a single app. That means my backlog of apps to make is ever-increasing, with no end in sight. So every now and then, I have to prune this list of things to do. I am going to stick with the ticketing system, because it's a useful and educational project, but some of the other fun or interesting ideas I had were less useful and wouldn't look as good on a resume.

And aside from deleting some projects I'd otherwise probably not have the time to get to, I also made some other repos private to showcase only my current educational projects or finished/semi-finished apps.

