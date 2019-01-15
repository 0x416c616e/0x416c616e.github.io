---
layout: "post"
title: "Day 17: More Python"
date:   2019-01-15 1:12:33 -0600
---

## Goodbye Qt, hello tkinter

I was originally planning on using Qt for doing Python GUI applications, because I've heard of Qt, QTK+, and JavaFX. I only know JavaFX as far as GUI stuff goes (unless you count web dev frontend development as a GUI). It turns out that the course for Python and Qt I was going to take actually had video tutorials for an outdated version of Python, and the Qt PySide version was out of date too, which meant I couldn't even follow the code examples in the video tutorials because they were for obsolete versions which had different syntax. It would have been a serious struggle to change everything in order to follow along, so I gave up.

I did some research online, and apparently Qt isn't the easiest way to get a GUI program up and running in Python. Modern versions of Python come with tkinter, which is apparently based on Tcl/Tk. I'll admit that I have no prior experience with that, and I've never even really heard of it. But because it actually comes with Python, rather than being a standalone download/installation, that makes it much easier. Ease of development, at least in my opinion, can be more important than framework-specific features. Maybe Qt is more robust in some ways, but I really don't care. The fact that a Python/Qt course on Udemy was outdated and confusing means I'll jump ship to something that is easier to learn and work with. 

I'm not new to GUI development or the idea of event-driven programming, with event listeners for each button, and getting text from text fields, or using file choosers (like in Java, the FileChooser class) to get a file upload from the user. So I'm not learning GUI programming in its entirety, just things that are specific to Python and tkinter, which is easier than starting with absolutely no prior knowledge.

I've found that learning Python is pretty easy because of my prior knowledge of Java. However, sometimes I have to let my previous Java-thinking mindset go because it can get in the way of learning Python due to the differences between them. But as far as basic paradigm and programming stuff goes, I am basically only learning the differences in syntactic sugar, typing systems (dynamic in Python vs. static in Java), some built-in methods, and basic/preferred data structures in Python, like tuples, dictionaries, lists, and things like that. 

## Not putting all your eggs in one basket

I could have much more easily developed my static site generator in Java and JavaFX, because that's what I'm the most experienced in, as far as programming goes. I took multiple Java classes in university, and I've made a lot of Java programs too. Read lots of books on Java and done some online Java courses in addition to my college classes. I've even ventured out of the Oracle API and learned some Apache library stuff. But even so, I think that, rather than continuing to be competent with Java, it's better to get outside my comfort zone and learn a new language and new ways of programming instead of putting all my eggs in one basket. I could just say that I'm a "Java developer" but I really want to transcend beyond being a one-trick pony. I think any developer worth their salt needs to know multiple languages. 

It's true that I've taken a class on C++, and even dabbled in assembly a little, and I also do shell scripting and web development. But even so, Java has, up until recently, been my go-to language, and I want to put an end to that. I will still do Java stuff every now and then, but being comfortable in one language isn't enough.

Python is good because of its easily-readable syntax, as well as its powerful library, third party library support (and big active development community), as well as the fact that Python code is more portable and multi-platform than code written in many other languages, and there are lots of jobs related to it as well.

The point of this static site generator project is to get more competent with Python, in a real way rather than just learning basics from a book. If all you do is read from a book, it's easy for it to go in one ear and out the other. Experiential learning is very powerful.

Technology is always changing, and if your skills aren't changing too, you're actively becoming obsolete. Java has a lot of momentum, and there are lots of jobs and projects for Java, but in the future it could become the next Fortran or COBOL, and I don't want to be a dinosaur programmer who only maintains legacy codebases.

## Reading

In addition to programming, I have also been reading some books about programming too. I am reading many books simultaneously, including *Coders at Work*, *Teach Yourself C*, *Python Crash Course*, *Learn Version Control with Git* and *Teach Yourself SQL in 10 Minutes a Day*. *Coders at Work* is a collection of interviews with seasoned programming veterans. Many of them have great insight into software development. These programmers aren't household names, but the projects they developed certainly are. Many software developer pseudo-celebrities are like that: everybody knows the platforms and apps they've made, but never knew who actually made them. Unsung heroes of technology. 

One interesting thing I learned was how Memcached was created by the people who made LiveJournal. This was because of performance issues with their databases. At a large scale, you come across performance challenges that are nonexistent for small websites/apps/companies. Nowadays, LiveJournal is basically a ghost town, a relic from the previous generation of the web. But Memcached is still incredibly useful and relevant to this day, even if some people prefer to use Redis instead.

While *Coders at Work* is a nice palate-cleansing type light read, the other books are much more technical and harder to get through. *Python Crash Course* is a good book because of its numerous exercises. It's like mini-homework assignments, where you're supposed to write short Python programs based on its specifications. They teach you certain concepts about the language. I like these kinds of assignments, because unlike in a traditional classroom setting, you are only concentrating on the learning, not grades and scholarships and deadlines. It's self-paced and independent.

## Non-traditional learning vs. university

It's true that college education has its place. I've learned a lot about IT from my community college classes, and I learned a lot about computer science, programming, and math from my university classes. However, calculus and differential equations aren't really useful in the real world, and feel more like filler classes to get students to take more credit hours, thus giving the university more money. Same with general education requirements. I've enjoyed some history and communications classes I took, but many seemed completely unrelated to what I was studying, and seemed like a waste of time. 

Some people say university is a scam and it isn't worth the money because you can just teach yourself things on your own. It's true that self-learning is hugely important. In fact, a lot of my strongest tech and development skills are things I've learned myself, not taught in classes. But to say that there's no value in university at all is misleading, because a lot of the benefits of university aren't just about learning programming languages and math. The real value is being able to meet people, make friends, work on projects with other people, find jobs and internships (among other opportunities), and things like that. You can learn Java or Python on your own, without going to college, but you'll miss out on many of the other opportunities they provide. SIUE also offered extracurricular organizations, events like hackathons, a nice library, resume editing, and even a career fair. These are all really good.

Additionally, when you're only self-learning, rather than doing self-learning as a supplement to formal education, there are many things you might inadvertently miss out on, or learn the wrong way, because you don't have anyone guiding your education. At the very least, a CS education in university will enumerate a list of topics you need to know. If I mention a topic like physics, you might not know much about it, but you are at least familiar with the subject. You know what the word means and you know it exists. But there are many programming topics that an absolute beginner will not even know that they don't know. If you don't at least have introductory classes in a classroom setting, there will be many concepts you won't teach yourself because you don't even know that they exist. 

So to anyone who is wondering about being self-taught as opposed to going to college, I think they are both important, and what I do is learn basic stuff from my classes and then it helps me learn about additional topics to learn in my own time. If I didn't learn all the basics of programming with Java at SIUE, I wouldn't really know how to teach myself Python. If I didn't network with people and learn about GitHub and Udemy, it would be harder for me to learn. Learning how to learn is a vital skill, more than any fixed tech skill. Something that so-called "tech-savvy" people need is the ability to learn new things quickly. If you have a mental framework for how to find resources to learn something, and then time management skills for sticking with it over time rather than giving up because it takes too long, you will go far in life. Software development requires continual learning.

## Beginners and experts

I don't remember who said this, but I remember someone saying that you should never get into the mindset of thinking you're an expert on something. You might have years of experience in a field and advanced degrees to show for it, but being a self-proclaimed expert means you're past the point of being open to learning new things, and might even think you're too good to learn new stuff, or have some sort of cognitive dissonance about why you don't want or need to learn new things. By contrast, someone who considers themselves to be a beginner will be curious to learn new things, and will be much more okay with admitting that they don't know everything. So a person who thinks like a beginner will be better able to learn and adapt to new things, such as new programming languages and tech that comes out. 

## How to avoid becoming obsolete

There are definitely some dinosaurs in tech, some of whom are against higher-level languages like Python, or full stack web apps rather than native clients, and instead tell people we all need to learn C and pointers and manual memory management, because that's what they did, so apparently everyone else needs to do it too. And yes, there is a continual erosion of privacy, like with Google Analytics and all that jazz, but it's not going to kill you. What will be the death of your career is opting out of modern tech. That's a bigger threat to you than some small amount of data collection. And sure, there are new security issues for web development, like CSRF or RFI, that weren't a problem for previous generations of tech. Though C and C++ were arguably more dangerous languages because of how easy it was for the programmer to have some memory-related issue that could lead to buffer overflows and whatnot, but I digress. 

The reality of the matter is that the world is changing, so best practices for programming in the past, and advice for which languages to learn, have actually become outdated. Perl, C, and other such languages haven't really adapted for the modern development landscape. Many people also cling to desktop-centric computing ideas, when we're actually shifting more towards IoT and mobile. Web is also hugely important. Java's mantra is "write once, run anywhere" but that's more true for web than for Java applications. Older programmers, especially ones who espouse purist ideals of privacy and security, will talk about how mobile platforms, cloud, and other modern stuff is terrible. But if you choose to opt out of modern tech trends, you are resigning yourself to obscurity. 

I take a more pragmatic approach to these issues of modernity, privacy, development preferences, and so on. If it's widely used, I should consider learning or using it, whether I like it or not. Additionally, you need to stay up to date with development news, and figure out if something is popular but in decline, or popular and becoming more prevalent. Think not just about the current status of something, but how it'll be used in the near future. Will there be more people using it, or fewer? Is it only being used for legacy development? What are some compelling reasons to learn this particular thing over other things? 

I use many different platforms, many different IDEs, languages, frameworks, etc. Hindsight is 20/20, but it's hard for us to see who the winners and losers of our day will be. So instead of betting on a specific thing, it's best to dabble in many different things, so that, when many eventually fail and become abandoned, you're not going down with the ship, because you still have other options due to your diversified skill set.

One example of this issue is Ruby. It used to be hugely popular for web development, but it's been in continual decline in recent years. That's not a big deal for someone who knows Ruby in addition to many other languages, but for Ruby purists, this is really bad. Who knows what modern tech will still be around in 5-10 years? The only way to ensure that your usefulness as a developer will continue on is if you had a broad range of skills. Sometimes, breadth can be more important than depth. 

## JSON refresher

Watched a half hour video about JSON again, because I'm planning on using JSON for my static site generator. I learned it in the past, but it's been a while. A lot of my tech skils are like that -- I knew a lot about it at one point, but because I haven't used it recently, I've forgotten some things about it. It takes less time to re-learn compared to learning something for the first time, but it can still take a little while to get back into the swing of things.

## Static site generator

![](/assets/ssg_text_menu.PNG)

My idea for my static site generator, at least for right now, is to get user input to make articles. It will use the input() function to get user input for things like the title, date, file name of the leading image, first paragraph, and remainder of the post body text. This will then be stored as JSON as an article file, and there might also be a config file somewhere. 

I'm thinking I will have a single Python script that prompts the user to select options from a menu (text-based for now), so you can create a new project, open an existing project, create a new post, view existing posts, edit an existing post, delete an existing post, change site info (such as author name, social media links, and the static about page), etc. Then there will also be a function to regenerate the static pages. 

This static site generator can be used in conjunction with git and GitHub Pages in order to make a static site. Once I have a working text-based version, I will replace this Jekyll site with my own statically-generated site. The content will be the same, but the layout will be different.

## More Python

![Python learning screenshot](/assets/python_learning123.PNG)

Still doing more Python learning. Pretty simply stuff, but it's still something.

## Backburner project: SQL

![]()

Even though my Lamp 7.1 VM wasn't useful for osTicket (and I will probably just not use osTicket at all!), I still had the 7.1 VM on my hypervisor, just turned off and not really doing anything. Well I've decided that I should use it for the SQL in 10 Minutes book I'm reading, because the book contains some exercises and files and whatnot. But you need to have a database and DBMS in order to use it, so you can make tables and rows and all that jazz. 

Now that I have an easy-to-use virtual machine that already has MySQL set up, I'm going to follow along and do some more database-related stuff.

It's true that my SIUE CS234 class supposedly taught about databases, but it crammed so many topics into a single class and it was more about noSQL databases anyway, since the class's big final project was MEAN stack, and I didn't even end up doing that much database stuff in it anyway. But as cool as new stuff like MEAN is, I think I will be using SQLite for my IT ticketing system web app (the next project I will do once my static site generator is more or less finished), mostly because I know someone else who learned SQLite and they referred me to a Udemy video course that teaches Python/Django/SQLite development. But the two SQL books and the exercises I'm doing right now involve MySQL. Not a big deal to have a slightly different DBMS when they both involve SQL though. 

MongoDB (and Mongoose) were weird in the sense that they were basically JSON as a database. Apparently it's more flexible, and yeah, you can enforce database schema stuff, so it's not just free-for-all JSON (well, technically BSON), but it seemed weird that something more associated with frontend was on the backend. Same thing with Node/Express using JavaScript -- for a backend web server. I guess the whole thing about MEAN is it's very much centered around web development, and maybe they think JavaScript's frontend ubiquity means that developers are already well-versed in it anyway, so you might as well try and implement it elsewhere for the sake of developer competence with it. 

But as cool and modern as these things may seem, it still seems important to learn SQL, even if it's not as hip or trendy as MongoDB. 

They both have their own issues. MongoDB has host binding issues, where it can be easy to accidentally let your database be public, and SQL has SQL injection, which is older than I am, but is still a problem to this day. I once did a SQL injection workshop at SIUE, and it was fun because I actually managed to inject JavaScript into a database row, which was a little bit beyond the scope of what the project was supposed to be about. I made it so that viewing a web page would run JavaScript that was being retrieved from what I injected into the database. 

But yeah, databases (and database management systems) are important, and I will be learning more about them in the future. 

## WAMP and MySQL Workbench

![Bitnami WAMP screenshot](/assets/wamp1.PNG)

The PDF for the book exercises instead recommends using MySQL and the MySQL workbench program, so I am actually setting this up with WAMP within Windows, locally, on my desktop. The instructions included text files full of SQL queries to populate the otherwise blank database they had you make. It's not real data for any useful application, it's all just made up for demonstration/learning purposes, going by the SQL book.

![](/assets/mysql_workbench1.PNG)

I followed the instructions in the PDF that was mentioned in the link in the book Teach Yourself SQL in 10 Minutes. There were a couple issues with the instructions, but I figured it out anyway.

![](/assets/mysql_workbench2.PNG)

Here, you can see the dummy data that the book wants you to use in order to follow some exercises to learn about SQL.

![](/assets/mysql_workbench3.PNG)


## Data structures and types

I decided to review some data structures I already know, as well as learning some new ones. I looked up info on graphs, maps, hashmaps, generics, and trees. I've also been learning things Python uses, like dictionaries, tuples, and lists. 

## Other random learning

Did a refresher on modal view controller architecture, extract-transform-load, entity-relationship models, design patterns, ajax, create-read-update-delete, Python standard library, Python modules (especially the os and sys modules), regular expression, if \__name__ == '\__main__', sys.argv command line arguments, Python file IO, etc.

## Simple text-based Python RPG

I said the IT ticketing system would be my next big project after I finish my static site generator, but I'm thinking that I should do something more limited in scope first, that also demonstrates a lot of concepts that I haven't really used much in the static site genreator. I don't actually any play video games, but I have made a couple. I've made a 2D RPG in Java, though because I made it before I started using version control, my IDE somehow deleted some important files in it and it doesn't work anymore. It would require a lot of changes to fix. Another game I made was a self-playing text-based RPG in C++, which would log statistics to a CSV file so you could view information about what happened after the fact. Opening the CSV in Excel would show you a graph. But that's getting a little off-topic now.

RPGs are a good example that would require things like classes, subclasses, inheritence, polymorphism, objects, control flow, variables, globals, user input, file IO, error handling, etc. The static site generator is good, but can really just be a single Python file and has a lot of while loops and performs file IO. Not much else to it. I guess it also involves some HTML and CSS and even JavaScript, but it's not a really great way to incorporate a lot of the features of Python, so I want to do that before moving onto a really daunting project like a full stack web app IT ticketing system.

The best way to learn a programming language is to learn experientially but also iteratively. Your first app in a language should not be super complicated. You work your way up from smaller projects and eventually increase complexity. If you start too big to begin with, you're destined to fail. 

## Yes, I really do need 32GB of RAM (for VMs and more)

![](/assets/booting_vm_resource_usage.PNG)

A couple days ago, I decided to make an Ubuntu VM, running locally on my desktop as opposed to on my hypervisor, which might not have been the best decision. I decided not to put it on my boot SSD, because it has limited capacity and it's just a slow-ish SATA III SSD anyway, as opposed to the faster NVMe M.2 drive on my mini-ITX hypervisor. But I thought a WD blue would be sufficient for a VM. I guess it technically works, but booting is painfully slow. 

The point of me making the VM was to get more experience with Linux again. I started using Ubuntu and Debian over a decade ago, but I haven't used it as my daily driver OS in a few years. I have a MacBook running macOS, and my desktop runs Windows 10 natively, though now with different VMs for various things. 

Because I write web, Java, and Python software, I want to be able to properly test my programs and websites on many different platforms. I can simply install the dependencies, like JDK, and other stuff like Python comes with Linux anyway. 

But it's not just that the hard drive is slow. My settings for the VM make it even slower. By default, it was only given access to 1 CPU core and 1GB of RAM.

VM CPU and RAM settings haven't been an issue for my non-graphical VMs on my hypervisor, even with extremely limited resources allocated to them, simply becaues they are command line only, not running any sort of desktop environment. Because my local VM has the default Ubuntu DE, it requires a lot more power. One big limitation I can't change though is that it's using a Virtualbox virtualized graphics card rather than a real one. I guess I could do a hardware pass-through, but that's too involved for me, and all it really needs is more sufficient CPU and RAM usage rather than a GPU. It might have even been dipping into swap, which would have explained the higher disk usage. Should've checked with htop before I changed it, but oh well.

![](/assets/vm_cpu_setting.PNG)

Now I've changed it to 2 CPU cores and 4GB of RAM. I have 32GB of RAM and only use around half of it most of the time, so I can afford to use a little more if it means my Ubuntu VM will be snappier.

![](/assets/resource_usage_after_vm_change.PNG)

After changing the VM settings and rebooting, it boots up noticeably faster now, and it's far more performant, though still nowhere near as fast as a native OS installation. 

![](/assets/ubuntu_vm_neofetch.PNG)

Now I can test things on macOS Mojave, Windows 10, and Ubuntu 18.04 LTS -- with decent performance on all three, too. I used to have a Windows 10 VM on my MacBook, but it was sluggish and increased resoruce usage and temperature to an unacceptable degree. My MacBook is slower and has less RAM and disk space than my desktop. Resources are cheaper in a desktop than in a laptop, and cooling is better with larger heatsinks and fans in a desktop too. So virtualization really isn't great on something compact and expensive like a laptop. Getting a higher-performance laptop would cost more than my desktop and laptop combined, so that's not really a good solution.

That all being said, I encountered some issues with being able to install the correct version of Java to run my Java 8 JAR file. Just like how there's a difference between PHP 5.6 and PHP 7.X, and there's a difference between Python 2.7 and Python 3.X, there is also a difference in compatibility between Java 8 and Java 11. My projects are made with JavaFX, which comes with Java 8 by default, but it got removed in Java 11 for some reason. Not really sure why. So I can either figure out how to set up JavaFX externally, or just use Java 8.

But as it turns out, installing Java 8 in Ubuntu is a little tricky. I will look into it later, but not now.