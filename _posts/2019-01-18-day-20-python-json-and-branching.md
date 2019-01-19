---
layout: "post"
title: "Day 20: Python, JSON, and Branching"
date:   2019-01-18 7:30:00 -0600
---

## Today's highlights

Git, Docker, more Python learning, random Youtube tutorials about programming, learning about build tools, how Java has changed in recent versions, argparse, JSON, SSG project structure ideas, unfortunately not much progress with SSG itself, typosquatting, and sorting retrieved data with SQL.

All of my future sections will have a "today's highlights" section in case my long-winded writing is too much for you.

## More git

I am getting better at using git, slowly but surely. I use GitHub to host my repositories, but I could just as easily set up my own git server. The benefit of using GitHub is that it's not just a git server, but it has a lot of value-added things too, like the fact that it's a portfolio that employers can view to see that you actually know how to code outside of a classroom or bootcamp.

## Branching and merging

I sort of learned about branching a while ago, but I've decided to start using it now. I will at least do feature branches and then merge them back into master when I'm done.

Master is a special branch. Novice git users will push everything to master. But you should really create feature branches, make multiple commits on the feature branch until it's done, and then merge it after you're sure it's done and 

## Commits

Commits should be small and only involve working on a single thing. Don't try to change three different features in a single commit. A feature can take multiple commits to finish. It's like a save state, and you can revert back to it in case you mess up your code. 

Before I started using git, I was afraid of messing things up, because I only had one copy. Or sometimes, I would create a secondary folder called something along the lines of "[timestamp] WORKING BACKUP BEFORE ADDING [feature]."

The problem with not using version control is the lack of ability to roll back to a previous version. Of course, collaboration is another benefit of version control, but not all git projects have multiple contributors, but they can still benefit from using git for commits, among other things.

## Forks and pull requests

I haven't really done much with pull requests yet, because I mostly work on my own open source projects rather than contributing to ones other people made. But my understanding of a pull request is that it's a request to have someone else pull in your data. 

First, you make a fork of the git repository that you want to work on. It won't be a repo you own. A fork is when someone else's project is interesting enough to you that you want to work on it as well, or perhaps just make your own version of it. Not all forks have subsequent pull requests, because maybe you want your fork to go on as its own unique/separate entity. But if you want your fork's changes to be put into the upstream project, you will need to submit a pull request. A pull request is like a merge, except it doesn't get approved automatically. It's called a request because the actual repo maintainer can choose to reject it if they want to. They might reject it because your code doesn't meet their guidelines, it's an unnecessary or unwanted feature, it's messy, or maybe they simply don't accept pull requests from other people. But if they do accept it, the changes you made will be incorporated into the repo. 

Making a fork is like pulling from a remote repo. Making a pull request is like pushing to a remote repo. Having someone fork your project is like having someone pull (or clone) your repo. Having someone submit a pull request to you is like someone remotely wanting you to pull their changes.

## GitHub issues

Issues are a way to report problems, even if you don't have a pull request to fix it. You can also suggest features to be added. I use issues to keep track of a to-do list of features and things to implement. Sometimes, you can revisit your project and realize that things are taking longer than you initially thought, so you decide to cancel some of your planned features. Or maybe you want to decide to add new ones. You can close features, open new ones, or add comments on issues. I comment on issues to note any progress that was made on something that isn't completely finished yet. When a feature issue is finished, the issue gets closed.

On other popular repositories, sometimes people will post bug issues, and then the maintainer will ask them about what was running on their system. A lot of bugs can be hard to diagnose, especially when people have different software on their computers. One particular version of Python might not work well with your software, whereas another one might. Perhaps there is a Windows-specific issue and you'll never notice because you're on Arch Linux. And so on. It can be hard to fix issues. This is why containers are important. I haven't really played around with containers much yet, but I have learned a lot about them anyway.

## Migrating this site to my new static site generator

I hope that this will be one of the last days that my site is made with Jekyll. I am making a lot of great progress on my SSG program, though I don't know how soon it will be before it's finished

## Is software ever really finished?

You can have a rough draft of a paper, then the first revision, then the second, and then the final draft. But what if you wanted a third of fourth revision? Maybe you could remove a paragraph here or change the wording there. Editing writing can be an endless cycle. Similarly, software can also be edited and optimized endlessly. There could be all sorts of features you can add, or ways to refactor existing code to make it better. 

The only really obviously important updates are for security and stability, such as if your project has an outdated dependency that has a CVE, so you need to update your code to make it compatible with the more recent version of the dependency. But aside from security (and perhaps stability), it's hard to gauge when exactly a project is really done.

For SSG, I could probably come up with a list of 100 different features I'd like to add, but if I added 100 features to SSG, that time would not be spent making a different app. Sometimes I'd rather have an okay project in my portfolio and then move onto a new project.

The problem is that I have a ton of ideas for apps to make, but not enough time to make them all. So sometimes I end up not polishing something as much as I could have, because why spend so much time polishing something, making it only slightly better, when I can build something entirely new in the same amount of time? 

Obviously, for work, it makes sense to polish things instead of churning out tons of apps. But for my personal portfolio, and for the sake of creativity and learning experiences, I like to branch out and try many different kinds of programming projects.

## Unit testing

I'm not really sure where to start with things like unit testing, continuous integration, etc. I want to start incorporating that kind of stuff into my workflow though.

## Python

I made more progress on learning Python. I didn't actually do much for my Python static site generator today, but I did watch some videos to learn more about Python. I'm not a pro yet so I can still benefit. And for a while, I got bored with some of the Udemy classes, so I instead decided to look up very specific Python topics on Youtube. I learned about Python multidimensional lists, urllib, logging, making modules, exceptions, APIs, etc.

Here is the unfinished project structure for sites made with SSG, by the way:

![](/assets/project_structure_ssg.PNG)

All the files and directories will be copied to a new folder in the projects directory. Notice how these are all in the "templates" folder, because these are the base template files that are used to build the project. There are some working-project files that aren't what you will put on your website. The only files you will end up copying over to your server (or commiting in git) are in the website_files directory. Everything else is project-related.

## I was reinventing the wheel unnecessarily

It turns out there is a very convenient module in Python caled argparse. I will use that in the future instead of making my own method of handling command line arguments, which gave me quite a lot of problems. But even so, for SSG, I think I will just leave it as-is and not mess with anything. I could spend more time refactoring it to make it better, or I could spend that same amount of time working towards finishing the rest of the program. I think I'll go with the latter.

You can always refactor things, make them slightly more efficient, etc. But unless you're doing some computationally-intensive thing that really requires efficiency, and you're doing things like calculating the big O notation stuff for your best/worst/average cases of some algorithm you implemented, then being slightly slower than optimal is just fine. I mean, that's what Python is all about. Nobody who wants high performance stuff uses Python when they could be using C instead. Of course, then there's Cython, which is an interesting superset of Python with C extensions. But the point I'm trying to make is that it's not a good use of my time to refactor this stuff even though I know it's not perfect.

My future Python programs will use argparse to simplify the process of getting command line arguments... that is, if I want to keep on making command line programs instead of doing graphical stuff with Tkinter.

Sometimes, I prefer using command line things. I still use vim for simple editing, and I also use ssh to use my Raspberry Pi. I also use command line git instead of the built-in IDE stuff that does it graphically. Command line programs can be very powerful. That being said, I still like to make graphical stuff every now and then. 

## JSON

I still have to learn about JSON schemas and validation, but so far I have made some basic JSON stuff, like what an article will look like (the content, not the final generated static HTML file):

![](/assets/json_article.PNG)

## JavaFX and Maven/Gradle

The below screenshot shows some of the source code for my EZcrypt program that I made not too long ago. However, it uses JavaFX, and there are some issues with that in newer versions of Java, which decided to remove that and make it separate.

![](/assets/EZcrypt_source.PNG)

I asked about JavaFX in Java 11 on reddit. It turns out that Java 11 no longer comes with Java, and it's called OpenJFX now. My old Java programs currently run in Java 8 because it comes with JavaFX, but if I want it to run in Java 11, I need to download OpenJFX separately and add it to the project. Someone mentioned using something like Maven or Gradle in order to manage dependencies. Apparently Maven and Gradle are used for managing project builds. And apparently I need to know about something called a classpath, but I will have to learn more about that later.

## Installed Docker

![](/assets/ubuntu_docker1.png)

I installed Docker on my Ubuntu VM. I would have installed it in Windows, but apparently it only runs on Windows 10 Enterprise Edition because of Hyper-V or something. Seems weird considering that there are free and open source virtualization options they could have gone with instead, but whatever. I also could have installed it on my MacBook, but it is not a very capable machine compared to my desktop, which has 4 times as many CPU cores and 4 times as much RAM, as well as many times the disk space.

I might use it on my hypervisor instead of my desktop in the future, like setting up a plain old Ubuntu VM and installing it that way, or maybe just leaving it the way it is now.

I haven't really done anything within Docker just yet, but I know it's something I will need to do at some point. As long as you move forward on things a little bit every day, that's all that really matters. You don't have to finish everything all at once.

## Educational hazing

In college, hazing is "I had to endure it, so you do too" and it often involves bullying and things that are completely unnecessary. I'd consider a lot of purists in computer scientists to be practicing their own version of hazing -- giving people bad advice about what to learn. "I learned assembly and C, so people in 2019 should learn them as well" -- I guess learning more low-level languages helps you understand computers and hardware better, and gives you a better appreciation for higher-level languages like Java or Python, but at the same time, it seems like a relatively fruitless endeavor (unless you want to write malware or do reverse engineering, in which case it would actually make sense).

 Odds are you're not going to be getting a job working on embedded systems that are so resource-starved that every megabyte and CPU cycle matters. It's not really worth it. You're better off learning more modern stacks and web frameworks, which will actually be relevant to today's technology. Of course, it would be good to learn C and assembly in addition to them, but for people who are time-limited, such as people going to bootcamps or teaching themselves coding on their own rather than going to college, it doesn't make sense to learn things just because older generations tell you they learned it.

Imagine if seasoned system administrators told new blood that they had to learn Windows Server 2003 before learning more modern stuff. It just doesn't make any sense. Sometimes, old stuff needs to be left in the past. 

Of course, there are always exceptions to the rule, and people will cite anecdotal evidence to claim that what I'm saying is wrong. But really, tech is moving forward, so  you shouldn't be looking backwards.

## Paint-by-numbers programming vs. software design

One thing I've come across is people who go to bootcamps or take online course that "have the student make some apps" that involve the person typing what the instructor or book tells them to *verbatim*. I once watched a video that said something like "by the end of this course, you will have a few apps in your portfolio" but it implied that the person watchning would make it exactly the way they were told to.

In other words, it's like a code walk/code review, but they're typing everything out. that's not real programming, is it? It really irks me. That doesn't really involve much learning at all, does it? You're basically just copying someone else's code at that point while learning only the most basic features of the language.

I design my own projects. The design and implementation of my EZcrypt, FileHider, Static Site Generator, AMP, etc. were designed by me. I came up with the idea for the app, then had to figure out how it would work on my own. 

It's not enough to simply know the syntax of a language. You need to know how to make your own projects, without basing it on someone else's. It's good to sometimes look for solutions to algorithms or runtime errors on Stack Overflow, but that's not what I'm referring to here. The ability to design a program really does matter, and it involves much more than merely writing simple statements and functions, or following along with an instructor's example.

This kind of pseudo-programming is like a coloring book or paint-by-numbers activity, whereas real programmning might be painting from a blank canvas. Sure, you might use libraries or design patterns, or even occasionally use google when you're stuck. But at the end of the day, doing something yourself helps you more than shadowing someone else to an extreme degree.

Make no mistake: even if a lot of people do these kind of cheap tricks for programming, I don't. My programs are mine. 

## Security tool users vs. security developers

A lot of people in information security know how to use many different tools and are familiar with a wide range of topics, including things like RCE, CSRF, file inclusion, disassemblers, reverse shells, privilege escalation exploits, Active Directory, dnscat, port scanning, metasploit, Kali, VMs, firewalls, networking, VLANs, man pages, exploit-db, Tor, VPNs, bash and powershell commands, etc. But what's strange to me is that many of these people don't know how to program, or if they do, they only do shell scripting or basic web stuf like setting up Wordpress. 

Security is an issue that related to technology and software. I don't think it really makes much sense to learn about security without learning how to program. It's true that you don't really need to write your own exploits or tools when there are plenty of ones that already exist, but if all you do is run tools, your work can be automated. Running Nessus or nmap followed by Metasploit to exploit some vulnerability and get a shell isn't a big deal. I've done a lot of labs that involve doing just that. What's more impressive is making your own stuff, which can differentiate you from derivative pentesters/security researchers. 

I have found file upload vulnerabilities on a lot of websites, though I'm not sure how I should go about disclosing this issue because I don't have much experience with bug bounties or responsible disclosure. 

I am also writing some proof-of-concept tools, like Abyss Dropper, which will be a later project of mine. It's for multi-stage malware payloads. The point of this tool is not for it to be used maliciously, but rather it's a learning experience where I have to think about tricky threats more, which helps me grow as a developer because it makes me more mindful about security.

At the end of the day, your first line of defense is and always will be your software developers. Not your IT staff, not antivirus, not IDS, not a web application firewall, not a security operations center. But the people who develop the software you use. 

Just like how I mentioned that security people need to know programming, programmers need to know security. You can't say you're a developer and then choose to ignore security issues, especially if you're a web developer. There's no excuse for not learning at least OWASP top 10 vulnerability categories these days, if not more than that.

Security can't just be tacked on later. Security needs to be a design consideration from the get-go. A web application firewall is just a bandaid put on top of bad code. I'm not saying people should abandon WAFs and monitoring tools entirely, I'm just saying you can't put all your trust that these tools will secure you completely (then again, nothing is 100% secure).

## Yet another app idea

I have more ideas for apps than I'll ever be able to make. It really sucks sometimes. But oh well. 

I have decided to make a WebExtensions browser add-on for blocking typosquatting domains. 

My first browser extension might even be something easier, just a button that copies an empty string to the clipboard (a feature I really want because I use LastPass and sometimes you copy passwords, and then I want to clear my clipboard right after that). 

But once I learn the very basics about WebExtensions and how to write browser extensions, after the copy button thing, I will make an add-on that blocks typos of domain names.

I am planning on writing a WebExtensions browser addon that blocks typo domains. It uses regex to block domains that are like alexa top 1000 (or is it 500? I forget) domains, but off by one character (one extra key press, one character omitted, or one wrong substitute character).

Don't actually go to any of the sites listed below! They are merely examples for typos in domain names, but they may or may not be malicious. That's why I put the brackets around the periods so that they aren't domains you can just copy and paste into a browser.

Here are some examples of the domains it will block:
- google[.]co -- wrong TLD
- goggle[.]com
- ffacebook[.]com
- facebokk[.]com
- fzcebook[.]com
- onstagram[.]com
- youtub[.]com
- eddit[.]com
- redit[.]com
- twittter.[.]com
- wwwgithub[.]com (forgot to delimit subdomain)
- wwwfacebook[.]com
- netflix[.]om -- even if it isn't a valid TLD yet, TLD typos are still blocked

Typosquatting is the act of registering a domain that is similar to a real website, in hopes of getting traffic when peole accidentally type it wrong. Typosquatting domains are often used for scams, phishing, or malware.

Here are some developer-related typos it will block:
- localhost8000[.]com (when you really meant localhost:8000)
- localhost80[.]com (generic web server)
- localhost[.]com
- localhost5000[.]com (Django)
- localhost3001[.]com (Node)
- 127.0.0.1[.]com -- the domain is 1[.]com with sub/tertiary domains

If you accidentally hit ctrl+enter in a browser, it will add .com to whatever you wrote, which can be dangerous when you're trying to access a local server instead of something online, or even when you're just trying to search for something. Maybe my add-on should disable that somehow. Or maybe the user can just disable it manually, such as in about:config or whatever the current-day version of it is (I haven't changed advanced browser configurations in a while).

## One more SQL lesson: the ORDER BY clause of the SELECT statement

I did another lesson from the SQL book I'm reading. It isn't related to my Python/JSON project, but it will be useful for my future full stack web development projects, such as my planned IT ticketing system, which will be a monumental project, at least compared to everything else I've made.

I've noticed that JSON is nice and all, but it would be better to store all this data in a database. I guess I could use MongoDB like I learned in college, which is basically *JSON: The Database*, but I've looked at a lot of job listings that really want people to know SQL. My college class very briefly covered it, but the emphasis was on noSQL instead, so I am teaching myself about relational databases and how to use them.

Here's what I learned about SQL today (this is my version of the Feynman technique, explaining it to an audience on the internet):

So in the last SQL lesson I did, and I should be doing these daily instead of once every couple days, I learned about the SELECT statement so you can retrieve data. But that data might be in seemingly random order. It makes more sense to sort it. And technically it's not "random" per se, just not sorted, and displayed based on how it's stored in the database. But to you, it will look random. Changes made to the database can also change the order stuff appears in. So you really need to sort stuff on your own. You can't just use a SELECT statement by itself. You need ORDER BY.

Ever been to an online shopping site like Amazon and sorted stuff based on price? That requires querying databases and sorting. They might use slightly different stuff for their particular systems, but the general idea is that the ability to sort data is very important. I've learned about sorting data in programs before, but usually either stuff running in RAM, or contents from a file. Never database sorting. It's not that much different. Sorting is still sorting. Amazon probably has more sophisticated infrastructure though, like in-memory database caching, CDNs, distributed stuff, etc. The database I am working with is very simple by comparison: just a local MySQL database running on my computer. It's not even on my hypervisor, just my desktop. But it also simplifies everything and makes it less of a hassle to learn this way.

In my old Java classes, we had to implement sorting algorithms from scratch instead of using built-in sorting methods. While that's good for learning, it's kind of unnecessary for real-world stuff, especially when the O(n) complexity of your own simple algorithm probably isn't as good as what the language provides, which is probably more optimized. 

In this particular lesson about SQL, the implementation details about how the data is sorted simply don't matter. You don't care how your car accelerates when you hit the gas, you just care that it does. That's abstraction, and it's a key feature of most kinds of technology, computers or otherwise.

The way to sort data in SQL is with ORDER BY.

## What is a clause?

SQL statements, such as SELECT, can have multiple clauses. 

```
USE databasename;
SELECT *
FROM tablename
WHERE something=something
ORDER BY some_column;
```

The all-caps words are the clauses. They are the pieces that make up a complete statement.

In the above case, It's technically 2 statements. One to use a certain database, and then the next to retrieve some data with certain additional clauses.

So what does ORDER BY do? What things can you order something by? It has to be a column. SQL databases are made up of multiple tables. A table can have rows (also known as records) and columns. If you have ever seen an Excel spreadsheet, it's just like that. In fact, Microsoft has a database called Access which will look very familiar to anyone who has ever used Excel. Though many database professionals regard Access as a toy database. And that's why I'm using MySQL (technically a DBMS, not a database, but you get the idea). 

Anyway, here is an example of ordering data:

![](/assets/order_by_sql1.PNG)

## Pseudo-languages

There are some pseudo-languages I have to learn, like regular expression and SQL. They are very different from general purpose languages like Python or Java, but still languages nonetheless. You really understand what general purpose means once you get more into specialized things that can only do certain things. I guess sed and awk are also kind of like that, for pattern matching and whatnot.

## Disappointed

It's getting to be the end of the day and I feel kind of disappointed with the progress I made today. Maybe I didn't do enough, or maybe I thought I'd do more programming on my SSG project. But for one reason or another, I ended up doing other things, and it didn't feel very productive. I'm not sure if that's because I'm just setting unrealistic goals for myself, or if I really do need to pick up the pace.

I will try to pick up the pace tomorrow and do a lot more Static Site Generator coding. That will be my top priority. I doubt I will get it finished tomorrow, but I at least want to finish the JSON schema and validation stuff as well as testing the find-and-replace part for putting the JSON contents into the HTML files. I guess I could also use JavaScript for that, but I'd rather do this with Python because that's what I'm supposed to be learning right now (according to myself). JS isn't that interesting to me and people use it for way too many things. I know a little bit about it, and I've done some JS projects before, but I don't want to become a everything-should-be-JS kind of developer.
